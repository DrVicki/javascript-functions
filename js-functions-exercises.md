## JavaScript Function: Exercise-1 with Solution

Write a JavaScript function to reverse a number.
  - Sample Data and output:
      - Example x = 32243;
      - Expected Output: 34223

![image](https://user-images.githubusercontent.com/47826697/165140320-b87851fa-0ee2-4a71-b34f-82f0ba84865a.png)

### Sample Solution:

<details open>
<summary>Click for solution & Explanation!</summary>

  **HTML Code**:

```
<!DOCTYPE html>
<html>
<head>
<meta charset=utf-8 />
<title>Reverse a number</title>
</head>
<body>
  
</body>
</html>
```

### JavaScript Code:

```
function reverse_a_number(n)
{
	n = n + "";
	return n.split("").reverse().join("");
}
console.log(Number(reverse_a_number(32243)));
```
  
  **Explanation**:
Assume n = 1000.
Convert a number to a string :
Code : -> n = n + "";
Note : There are different ways to convert number to string :

  - String literal -> str = "" + num + "";
  - String constructor -> str = String(num);
  - toString -> str = num.toString();
  - String Literal simple -> str = "" + num;

  The ```split()``` method is used to split a String object into an array of strings by separating the string into substrings.
Code : ```console.log('1000'.split(""));```
Output : ```["1", "0", "0", "0"]```

The ```reverse()``` method is used to reverse an array in place. The first array element becomes the last and the last becomes the first.
Code : ```console.log(["1", "0", "0", "0"].reverse());```
Output : ```["0", "0", "0", "1"]```

The ```join()``` method is used to join all elements of an array into a string.
Code : ```console.log(["1", "0", "0", "0"].reverse().join(""));```

  The Number constructor contains constants and methods for working with numbers. Values of other types can be converted to numbers using the ```Number()``` function.
Output : 1
  ![image](https://user-images.githubusercontent.com/47826697/165141299-ad1e9b0e-4fdc-4710-9065-03051f8c4a41.png)

</details>


## JavaScript Function: Exercise-2 with Solution

Write a JavaScript function which checks whether a passed string is palindrome or not?

**Note**: A palindrome is word, phrase, or sequence that reads the same backward as forward, e.g., madam or nurses run.

![image](https://user-images.githubusercontent.com/47826697/165141765-a98abc35-ccef-43ab-85b1-fe196ad29f1a.png)

<details open>
<summary>Click here for solution & Explanation!</summary>

  **HTML Code**:

```
<!DOCTYPE html>
<html>
<head>
<meta charset=utf-8/>
<title>A passed string is palindrome or notlt;/title>
</head>
<body>
  
</body>
</html>
```
**JavaScript Code**:

```
  // Write a JavaScript function that checks whether a passed string is palindrome or not? 

function check_Palindrome(str_entry){
// Change the string into lower case and remove  all non-alphanumeric characters
   var cstr = str_entry.toLowerCase().replace(/[^a-zA-Z0-9]+/g,'');
	var ccount = 0;
// Check whether the string is empty or not
	if(cstr==="") {
		console.log("Nothing found!");
		return false;
	}
// Check if the length of the string is even or odd 
	if ((cstr.length) % 2 === 0) {
		ccount = (cstr.length) / 2;
	} else {
// If the length of the string is 1 then it becomes a palindrome
		if (cstr.length === 1) {
			console.log("Entry is a palindrome.");
			return true;
		} else {
// If the length of the string is odd ignore middle character
			ccount = (cstr.length - 1) / 2;
		}
	}
// Loop through to check the first character to the last character and then move next
	for (var x = 0; x < ccount; x++) {
// Compare characters and drop them if they do not match 
		if (cstr[x] != cstr.slice(-1-x)[0]) {
			console.log("Entry is not a palindrome.");
			return false;
		}
	}
	console.log("The entry is a palindrome.");
	return true;
}
check_Palindrome('madam');
check_Palindrome('nurses run');
check_Palindrome('fox');
```
                             **Sample Output**:
```
The entry is a palindrome.
The entry is a palindrome.
Entry is not a palindrome.
```
                             
![image](https://user-images.githubusercontent.com/47826697/165142381-7e021c51-366d-407a-b5dc-9e9a01757f91.png)


</details>

## JavaScript Function: Exercise-3 with Solution

Write a JavaScript function which generates all combinations of a string.
  Example string: 'dog'
  Expected Output: d,o,do,g,dg,og,dog

![image](https://user-images.githubusercontent.com/47826697/165142778-3452df58-6c84-4e4c-9933-74fa8a4489fa.png)

  <details open>
<summary>Click here for solution & explanation!</summary>

    **HTML Code**:
```
<!DOCTYPE html>
<html>
<head>
<meta charset=utf-8 />
<title>Combination of a string</title>
</head>
<body>
  
</body>
</html>
```
**JavaScript Code**:

```
 //Write a JavaScript function that generates all combinations of a string.
function substrings(str1)
{
var array1 = [];
  for (var x = 0, y=1; x < str1.length; x++,y++) 
  {
   array1[x]=str1.substring(x, y);
    }
var combi = [];
var temp= "";
var slent = Math.pow(2, array1.length);

for (var i = 0; i < slent ; i++)
{
    temp= "";
    for (var j=0;j<array1.length;j++) {
        if ((i & Math.pow(2,j))){ 
            temp += array1[j];
        }
    }
    if (temp !== "")
    {
        combi.push(temp);
    }
}
  console.log(combi.join("\n"));
}

substrings("dog");
```
                                      **Sample Output**:
```
d
o
do
g
dg
og
dog
```
![image](https://user-images.githubusercontent.com/47826697/165143330-33ce2af9-d5ca-43bb-80d0-340c29832d3a.png)

                                      
</details>

## JavaScript Function: Exercise-4 with Solution

Write a JavaScript function which returns a passed string with letters in alphabetical order.
Example string: 'webmaster'
Expected Output: 'abeemrstw'

**Note**: Assume punctuation, numbers, and symbols are not included in the passed string..
    
![image](https://user-images.githubusercontent.com/47826697/165143653-253a5680-4e15-44f7-98a1-f639d90855f9.png)

<details open>
<summary>Ckick here to see solution & Explanation!</summary>

  **HTML Code**:

  ```
<!DOCTYPE html>
<html>
<head>
<meta charset=utf-8 />
<title>Returns a passed string with letters in alphabetical order</title>
</head>
<body>
  
</body>
</html>
```

  **JavaScript Code**:

```
function alphabet_order(str)
  {
return str.split('').sort().join('');
  }
console.log(alphabet_order("webmaster"));
```
  **Sample Output**:
```
abeemrstw
```
  **Explanation**:

The ```split()``` method is used to split a String object into an array of strings by separating the string into substrings.
Code : ```console.log('32243'.split(""));```
Output : ```["3", "2", "2", "4", "3"]```

The ```sort()``` method is used to sort the elements of an array in place and returns the array.
Code : ```console.log(["3", "2", "2", "4", "3"].sort());```
Output : ```["2", "2", "3", "3", "4"]```

The ```join()``` method is used to join all elements of an array into a string.
Code : ```console.log(["2", "2", "3", "3", "4"].join(""));```
Output :``` "22334"```
  
![image](https://user-images.githubusercontent.com/47826697/165144256-011bd27e-a311-4092-a233-421253606354.png)

</details>
