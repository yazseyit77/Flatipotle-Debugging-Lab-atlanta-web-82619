# React Debugging Lab

Flatiron School has decided to dabble in the food industry and just opened up a brand new fast casual Mexican restaurant (not at all a clone of a certain popular restaurant). Engineers were hired to design a web app to allow users to submit orders online, but they mysteriously disappeared and left everything broken. It's now your job to try to find all the bugs and fix the app!

## Setup

* Clone this repository and `cd` into it
* Run `npm install` or `yarn install` to install dependencies
* Run `npm start` or `yarn start` to start the app locally

## Deliverables

A working example of this app is shown in this gif:

![Jest watch mode](./public/example.gif)


1. A user should be able to see an order form with options for protein, fillings, toppings, and sides.
2. A user should be able to select as many proteins, fillings, toppings, and sides as they desire.
3. A user should be able to submit the form with their selections and see their order(s) listed under "All Orders."
4. If a user selects any sides, they should be able to click on a button to view their side choices.


## Helpful Things to Keep In Mind

* **Read** the errors you receive in your browser and console
* `console.log`, `debugger`, and **React Dev Tools** are your friends
* Did we *return* the values we want?
* Why would **this** be undefined?
* Did we import and export our components correctly?
* Did we pass down the *props* that we need?
* How do we change state?

## Errors
1. **App.js**:
  * Did not return Order component when mapping through `this.state.orders`
  * Did not pass down addOrder() to Form component
  * State is set with `:` instead of `=`
  * Form and Order components imported from incorrect path
2. **Form.js**:
  * handleSubmit() and handleChange() should be arrow functions
  * `event` argument not passed into handleSubmit() and handleChange()
  * handleChange() passed down as `handleOnChange` prop but used as `handleChange` in children components
3. **FillingForm.js**:
  * onChange should be `props.handleChange` instead of `this.props.handleChange`
4. **ProteinForm.js**:
  * Props not passed down into component
5. **SideForm.js**:
  * Did not export component
6. **Order.js**:
  * `handleClick` function does not use set state to change state
  * Did not import Side component
