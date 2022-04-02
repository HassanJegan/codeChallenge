# codeChallenge

The source files and my code changes can be found in sr-code-challenge-dotnet-Hassan-Ndow-v2.zip (v2 has null checking added for a Compensation's Employee object)

There also appeared to be a bug with the model Employee as its property: DirectReports would always return null from the EmployeeRepository's GetById method, as well as the Compensation's property: Employee. 

Adding the line
_employeeContext.Employees.ToList(); 

before the line 
return _employeeContext.Employees.SingleOrDefault(e => e.EmployeeId == id);

seems to resolve the issue but I decided to leave that code out and just focus on the requirements provided in the sr-code-challenge-dotnet/ReadMe.md file.
