# RCT-101-D4-state-managment-WE---THEORY

1)what is the difference between Props and State?

props (short for “properties”) and state are both plain JavaScript objects. While both hold information that influences the output of render, they are different in one important way: props get passed to the component (similar to function parameters) whereas state is managed within the component (similar to variables declared within a function).

2)Explain the useState API? explore

const [state, setState] = useState(initialState);
Returns a stateful value, and a function to update it.

During the initial render, the returned state (state) is the same as the value passed as the first argument (initialState).

The setState function is used to update the state. It accepts a new state value and enqueues a re-render of the component.

setState(newState);
During subsequent re-renders, the first value returned by useState will always be the most recent state after applying updates

3)Explain the how map, filter, reduce work

map() method: It applies a given function on all the elements of the array and returns the updated array. It is the simpler and shorter code instead of a loop. The map is similar to the following code:

function triple(n){
    return n*3;
}    
arr = new Array(1, 2, 3, 6, 5, 4);
  
var new_arr = arr.map(triple)
console.log(new_arr)

filter() method: It filters the elements of the array that return false for the applied condition and returns the array which contains elements that satisfy the applied condition. It is a simpler and shorter code instead of the below code using a loop:

arr = new Array(1, 2, 3, 6, 5, 4);
var new_arr = arr.filter(function (x){
    return x % 2==0;
});
  
console.log(new_arr)

reduce() method: It reduces all the elements of the array to a single value by repeatedly applying a function. It is an alternative of using a loop and updating the result for every scanned element. Reduce can be used in place of the following code:

function product(a, b){
    return a * b;
}
arr = new Array(1, 2, 3, 6, 5, 4);
  
var product_of_arr = arr.reduce(product)
console.log(product_of_arr)
