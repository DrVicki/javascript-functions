

## The Fortune Teller

Why pay a fortune teller when you can just program your fortune yourself?

Write a function named ``tellFortune`` that:

  - takes 4 arguments: number of children, partner's name, geographic location, job title.
  - outputs your fortune to the screen like so: "You will be a X in Y, and married to Z with N kids."
  - Call that function 3 times with 3 different values for the arguments.

<details open>
<summary>Click here to see solution!</summary>
  
```
  function tellFortune(jobTitle, geoLocation, partner, numKids) {
    var future = 'You will be a ' + jobTitle + ' in ' + geoLocation + ' and married to ' +
   partner + ' ' + ' with ' + numKids + ' kids.';
    console.log(future);
}

tellFortune('bball player', 'spain', 'Shaq', 3);
tellFortune('stunt double', 'Japan', 'Ryan Gosling', 3000);
tellFortune('Elvis impersonator', 'Russia', 'The Oatmeal', 0);
```
</details>


## The Puppy Age Calculator

You know how old your dog is in human years, but what about dog years? Calculate it!

Write a function named ```calculateDogAge``` that:

  - takes 1 argument: your puppy's age.
  - calculates your dog's age based on the conversion rate of 1 human year to 7 dog years.
  - outputs the result to the screen like so: "Your doggie is NN years old in dog years!"
  - Call the function three times with different sets of values.
  - Bonus: Add an additional argument to the function that takes the conversion rate of human to dog years.

<details open>
<summary>Click here to see solution!</summary>
  
```
function calculateDogAge(age) {
    var dogYears = 7*age;
    console.log("Your doggie is " + dogYears + " years old in dog years!");
}

calculateDogAge(1);
calculateDogAge(0.5);
calculateDogAge(12);
```
</details>


## The Lifetime Supply Calculator

Do you ever wonder how much a "lifetime supply" of your favorite snack is? Wonder no more!

Write a function named ```calculateSupply``` that:

  - takes 2 arguments: age, amount per day.
  - calculates the amount consumed for rest of the life (based on a constant max age).
  - outputs the result to the screen like so: "You will need NN to last you until the ripe old age of X"
  - Call that function three times, passing in different values each time.
  - Bonus: Add an additional argument to the function which takes the conversion rate of human to dog years.
  - Accept floating point values for amount per day, and round the result to a round number.

<details open>
<summary>Click here to see solution!</summary>
  
```
function calculateSupply(age, numPerDay) {
  var maxAge = 100;
  var totalNeeded = (numPerDay * 365) * (maxAge - age);
  var message = 'You will need ' + totalNeeded + ' cups of tea to last you until the ripe old age of ' + maxAge;
  console.log(message);
}

calculateSupply(28, 36);
calculateSupply(28, 2.5);
calculateSupply(28, 400);
```
</details>



## The Geometrizer

Create 2 functions which calculate properties of a circle, using the definitions here.

  - Create a function called ```calcCircumfrence```:
  - Pass the radius to the function.
  - Calculate the circumference based on the radius, and output ```"The circumference is NN"```.

  - Create a function called ```calcArea```:
  - Pass the radius to the function.
  - Calculate the area based on the radius, and output ```"The area is NN"```.

<details open>
<summary>Click here to see solution!</summary>
  
```
function calcGeometry(radius) {
  var circumference = Math.PI * 2*radius;
  console.log("The circumference is " + circumference);
  var area = Math.PI * radius*radius;
  console.log("The area is " + area);
}
```
</details>


## The Temperature Converter

It's hot out! Let's make a converter based on the steps here.

-  a function called ```celsiusToFahrenheit```:
-  Store a celsius temperature into a variable.
-  Convert it to fahrenheit and output ```"NN°C is NN°F"```.

  - Create a function called ```fahrenheitToCelsius```:
  - Now store a fahrenheit temperature into a variable.
  - Convert it to celsius and output ```"NN°F is NN°C"```.

<details open>
<summary>Click here to see solution!</summary>
  
```
function celsiusToFahrenheit(celsius) {
  var celsiusInF = (celsius*9)/5 + 32;
  console.log(celsius + '°C is ' + celsiusInF + '°F');
}

function fahrenheitToCelsius(fahrenheit) {
  var fahrenheitInC = ((fahrenheit - 32)*5)/9;
  console.log(fahrenheit + '°F is ' + fahrenheitInC + '°C');
}onsole.log("The area is " + area);
}
```
</details>
