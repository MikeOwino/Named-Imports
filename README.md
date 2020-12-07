# Named-Imports

o import objects stored in a variable, we use the import keyword and include the variables in a set of {}.

In the order.js file, for example, we would write:

import { specialty, isVegetarian } from './menu';
 
console.log(specialty);
Here specialty and isVegetarian are imported.
If we did not want to import either of these variables, we could omit them from the import statement.
We can then use these objects as in within our code. For example, we would use specialty instead of Menu.specialty.
### QQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQQ

1.
Let’s remove any reference to Airplane in our code since we are no longer exporting this module.

For example, Airplane.availableAirplanes should be modified to availableAirplanes.

Again, you will see a ReferenceError in the console for now, but we will fix that in our next step.

Checkpoint 2 Passed

Hint
Remove the module Airplane from this line:

function displayFuelCapacity() {
  availableAirplanes.forEach(function(element) {
    ...
  });
}
 
displayFuelCapacity();
2.
Change the import statement such that it imports the availableAirplanes, flightRequirements, and meetsStaffRequirements variables.

Now, modify any instance of the Airplane.availableAirplanes variable, so that you only use availableAirplanes.

Checkpoint 3 Passed

Hint
import {availableAirplanes, flightRequirements, meetsStaffRequirements} from './airplane';
 
3.
Define a function displayStaffStatus().

Checkpoint 4 Passed

Hint
function displayStaffStatus() {
 
}
4.
Within the body of the displayStaffStatus() function, use the forEach to iterate over the availableAirplanes array.

Specifically, the forEach() should take a function as a parameter. The function should in turn take element as a parameter.

Checkpoint 5 Passed

Hint
function displayStaffStatus() {
  availableAirplanes.forEach(function(element){});
}
5.
Within the displayStaffStatus() function, use console.log() to output the element’s name. We’ll add more in the next step.

Checkpoint 6 Passed

Hint
function displayStaffStatus() {
  availableAirplanes.forEach(function(element) {
   console.log(element.name);
  });
}
6.
Continuing within the displayStaffStatus() function, modify the console.log() statement to output

(element name) + ' meets staff requirements: ' + (true/false)
To do this, we can call the meetsStaffRequirements method, passing in two parameters element.availableStaff and flightRequirements.requiredStaff.

Checkpoint 7 Passed

Hint
function displayStaffStatus() {
  availableAirplanes.forEach(function(element) {
   console.log(element.name + ' meets staff requirements: ' + meetsStaffRequirements(element.availableStaff, flightRequirements.requiredStaff) );
  });
}
7.
Call the displayStaffStatus() function.

Checkpoint 8 Passed

Hint
displayStaffStatus();
