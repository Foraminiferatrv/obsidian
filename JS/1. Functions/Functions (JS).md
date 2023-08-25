Functions are [[First-class Functions]] in JS, because they can be passed to other functions, returned from functions, and assigned to variables and properties. They can also have properties and methods just like any other object. What distinguishes them from other objects is that functions can be called.


Arguments are always [_passed by value_](https://en.wikipedia.org/wiki/Evaluation_strategy#Call_by_reference) and never _passed by reference_. This means that if a function reassigns a parameter, the value won't change outside the function. More precisely, object arguments are [_passed by sharing_](https://en.wikipedia.org/wiki/Evaluation_strategy#Call_by_sharing), which means if the object's properties are mutated, the change will impact the outside of the function. For example: 

```JS
function updateBrand(obj) {
  // Mutating the object is visible outside the function
  obj.brand = "Toyota";
  // Try to reassign the parameter, but this won't affect
  // the variable's value outside the function
  obj = null;
}

const car = {
  brand: "Honda",
  model: "Accord",
  year: 1998,
};

console.log(car.brand); // Honda

// Pass object reference to the function
updateBrand(car);

// updateBrand mutates car
console.log(car.brand); // Toyota
```