# react-search-table  

![image](https://github.com/vegadelalyra/react-search-table/assets/77188420/bc371169-6b8a-4e10-acab-4d6b4f3d2cd3)   



Thinking in React!    
https://react.dev/learn/thinking-in-react

## Thought Process [3 phases]

How to think in React ought to take 3 big moments:   

### 1- Break the app apart into components.    
 
### 2- Describe the different visual states for each component.    

### 3- Connect the components together so the data wil flow through!     

## Technical Process [5 steps]    

Let's break down how to REACT your code!   

### (1) Break the UI into a component hierarchy 

### (2) Build a static version in React    

### (3) Find the minimal but complete representation of UI state    

### (4) Identify where your state should live   

### (5) Add inverse data flow     

# REACT STATES   

## What is state and what is not?  

Identify what would be a state with these 3 disclaimers:   

1- Does it remain unchanged over time? If so, it isn’t state.   

2- Is it passed in from a parent via props? If so, it isn’t state.    

3- Can you compute it based on existing state or props in your component? If so, it definitely isn’t state!  

#### What’s left is probably state.   

## How to guess the owner of each state? 

1- Identify every component that renders something based on that state.   

2- Find their closest common parent component—a component above them all in the hierarchy.        

3- Decide where the state should live:   
    1. Often, you can put the state directly into their common parent.       
    2. You can also put the state into some component above their common parent.    
    3. If you can’t find a component where it makes sense to own the state, create a new component solely for holding the state and add it somewhere in the hierarchy above the common parent component.   

### Components Hierarchy for this exercise     

FilterableProductTable
    SearchBar
    ProductTable
        ProductCategoryRow
        ProductRow    
   
### React States and its owners for this exercise  

State: Search input text   
Owned by: FilterableProductTable   

State: Value of the checkbox   
Owned by: FilterableProductTable   

## KEY TAKEAWAYS   

State is reserved only for interactivity!    

Component hierarchy must be planned to render the data model.      

Building a static version requires a lot of typing and no thinking, but adding interactivity requires a lot of thinking and not a lot of typing. So start on visuals, then logic.      

In simpler projects, it’s usually easier to go top-down, and on larger projects, it’s easier to go bottom-up.   

Props and states are "models" data in React: Props are like inheritable parameters that goes from parents to children components, whereas states tracks changes interactively done.  

States can be passed as props.   

# React + Vite

This template provides a minimal setup to get React working in Vite with HMR and some ESLint rules.

Currently, two official plugins are available:

- [@vitejs/plugin-react](https://github.com/vitejs/vite-plugin-react/blob/main/packages/plugin-react/README.md) uses [Babel](https://babeljs.io/) for Fast Refresh
- [@vitejs/plugin-react-swc](https://github.com/vitejs/vite-plugin-react-swc) uses [SWC](https://swc.rs/) for Fast Refresh
