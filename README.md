# WorkAroundExplorer


WorkAround is a research organization that provides data on salary trends in the tech industry. WorkAround now wants to release a new web application called WorkAround Explorer to make their data more easily viewable. This web app should allow users to choose specific roles and companies in the tech industry to see the following information:

The salary for the chosen role at the chosen company.
The industry average for the chosen role.
The average salary at the chosen company across all roles.
The industry average salary across all roles and all companies.


Much of the user interface has already been designed by front-end developers, however, the core data and functionality are either missing or need to be connected together using modules. Your task is to help your team members out by using your import and export expertise!


These first four tasks will focus on rendering the <input> elements using the names of the companies and the different roles available in the collected salary data.



1.
Open salaryData.js where you will find the collected data in the variable salaryData. Below are four functions for filtering down this data.

You need to:

Export the four functions from salaryData.js using ES6 named export syntax.
Export the salaryData array as the default export.



2.
Open up main.js and take a look at the function renderInputButtons(). This function accepts an array of labels that are used to create individual radio-style <input> elements. The function also accepts a string that is used as the name for that input group.

Currently, this function is being called twice with the variables companies and roles as the first arguments. However, each of these variables are assigned empty arrays.

Instead, you will use the getRoles() and getCompanies() functions from salaryData.js to initialize these variables.

First, at the top of main.js, use ES6 named import syntax to import getRoles and getCompanies from salaryData.js. Check the file system to determine the relative path from main.js.



3.
Now, replace the empty arrays assigned to companies and roles with function calls to getCompanies() and getRoles(), respectively.



4.
As mentioned before, even if you correctly completed the previous two tasks, the radio-style <input> elements still will not render and some of the columns have disappeared. This is because we are now required to specify that main.js is using modules.

In index.html, add a type attribute to <script src='main.js'> with the correct value to indicate that the main.js script is using modules.

After completing this task, all three columns should render again and you should see the radio-style <input> elements rendered in your application!



5.
Great job! You now have radio-style <input> elements for the different companies and roles represented in the salary dataset. Try selecting a combination of company and role and you’ll see that the data isn’t being calculated. Instead, all four values are showing up as $0.

Open up workAroundModule.js where you will find four functions that each calculate a different data value that we want to display. They are currently incomplete.

To complete these four functions, you will need some data from salaryData.js.

Import the functions getDataByRole() and getDataByCompany() from salaryData.js using named import syntax.
Import salaryData from salaryData.js using the default import syntax.
Note: The reason these functions are in a separate module from salaryData.js is to achieve separation of concerns. salaryData.js is concerned only with providing access to raw data while workAroundModule.js is concerned with digging into the data to find precise values.



6.
Each of the incomplete functions in workAroundModule.js contains an empty array ([]) that needs to be replaced. You will need to use the appropriate imported data/functions from the salaryData.js module to replace these arrays.



7.
As a final step, to make these functions available to main.js, export the four functions using named export syntax.



8.
We are all set up now to use the functions defined in workAroundModule.js to calculate and render the data based on the user’s input selections.

In main.js, import the four functions from workAroundModule.js.



9.
And finally, take a look at updateResults(). This function is called any time the user selects one of the radio input elements.

At the top of the definition of updateResults(), the company and role selected by the user are extracted from the <input> elements. These values can be used in combination with the imported functions from workAroundModule.js to calculate the four variables below:

const averageSalaryByRole = 0;
const averageSalaryByCompany = 0;
const salary = 0;
const industryAverageSalary = 0;


As you can see, they are all assigned to 0 rather than the appropriate calculated data. Replace each 0 with a call to the appropriate imported function from workAroundModule.js using either (or both) company and role as arguments.




Congrats! You’ve helped WorkAround build their WorkAround Explorer application using a modular approach. The end result is a well-organized program with clear boundaries for each of its separate concerns.



