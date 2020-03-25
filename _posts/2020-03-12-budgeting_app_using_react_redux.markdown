---
layout: post
title:      "Budgeting app using React/Redux"
date:       2020-03-12 11:38:21 -0400
permalink:  budgeting_app_using_react_redux
---


For my final project at Flatiron school I created a budgeting app where you can add budget amounts for certain dates onto any selected category.  I used a Ruby API on the backend and React with Redux on the frontend. 

Redux is a state management tool for JavaScript applications! It uses reducer functions which take in an action and the previous state in order to execute the next state.

My reducer function consisted of the following:


```export default function categoryReducer(state = {categories: []}, action) {
    switch (action.type) {
        case 'FETCH_CATEGORIES':
            return {categories: action.payload} 

        case 'ADD_BUDGET':
            let categories = state.categories.map(category => {
                if (category.id === action.payload.id) {
                    return action.payload
                } else {
                    return category}
                })
            return {...state, categories: categories}  

        case 'DELETE_BUDGET':
            let categoriesTwo = state.categories.map(category => {
                if (category.id === action.payload.id) {
                    return action.payload
                } else {
                    return category}
            })
            return {...state, categories: categoriesTwo}
            default:
                return state
            }
        }```
				
	And I used three actions:
	
	
**	1. Fetching Categories:
**

``` export function fetchCategories() {
    return (dispatch) => {
      fetch('http://localhost:3000/api/v1/categories')
      .then(resp => resp.json())
      .then(categories => dispatch({
        type: 'FETCH_CATEGORIES',
        payload: categories
      }))
    }
  }```
	
	
**	2. Deleting Budgets:
**	

```export const deleteBudget = (budgetId, categoryId) => {
    return (dispatch) => {
      return fetch(`http://localhost:3000/api/v1/categories/${categoryId}/budgets/${budgetId}`, {
        method: 'DELETE'
      })
      .then(response => response.json())
      .then(category => dispatch({type: 'DELETE_BUDGET', payload: category}))
    }
  }```
	
	
**	3. Adding Budgets:
**


    return (dispatch) => {
      fetch(`http://localhost:3000/api/v1/categories/${categoryId}/budgets`, {
        method: 'POST',
        headers: {
          'Content-Type': 'application/json'
        },
        body: JSON.stringify(budget)
      })
      .then(response => response.json())
      .then(category => {
          if (category.error) {
            alert(category.error)
          } else {
            dispatch({type: 'ADD_BUDGET', payload: category})
          }
        }
      )
    }
  }```
	
	
