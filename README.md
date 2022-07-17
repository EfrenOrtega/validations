# Validations 
 

## Description:
 - There are two scripts to validate any &lt;input> html but each one works with different Framework CSS (Bootstrap and Tailwind)
 - This script was created by me in a school project, here the repository: https://github.com/KevinJaramilloLievano/CINE_06_03.git \
 
## Types of Validations:
1. only-words
2. samePassword
3. only-numbers
4. maxLength- (This is to set a maximum of characters)
5. required
6. email



## How use it?
1. You need download the script in your project.
2. Make a index.js and import the script to validate there and call it:
   ```javascript
   import validations from 'path/.js';
   validations();
   ```
3. You need to call the index.js in your HTML
   ```html
   <script src='PATH../index.js' type="module"></script>
   ```
4. Now you need to put data-validation on any &lt;input> to validate. Each input to validate needs to have a name
   ```html
   <input data-validation name="input" ...>
   ```
5. You need to assing to data-validation the type of validation(s). The types of validations inside the data-validation need to be separated:
   ```html
   <input data-validation="required only-words maxLength-120" ...>
   ```
6. Finally you need to create div element with data-warn, inside the form element:
   ```html
   <form ...>
   ...
    <div data-warn></div>
   ...
   </form>
   ```


## How to get the validation result?
There is an export variable in each script called: signalToValidation this variable will store
the validation result and you will be able to access to it with this line in your script:
```javascript
import {signalToValidation} from 'path/.js'
```


## How to add more types of validations?
There is an array called typeValidations which stored objects, each object is a type of validation
and you can make more objects.



### The object attributes are:
- name -> 'name of the validation that must be added as the value of the data-validation.'
- inputs -> Empty Array
- methodValidation(targetInput, $warn, estatusAnterior, required, displaywarnings)
