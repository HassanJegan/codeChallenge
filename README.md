# codeChallenge

The source files and my code changes can be found in sr-code-challenge-dotnet-Hassan-Ndow.zip

There also appeared to be a bug with the model Employee's property: DirectReports where it would always return null from the EmployeeRepository's GetById method. 

Adding the line
_employeeContext.Employees.ToList(); 

before the line 
return _employeeContext.Employees.SingleOrDefault(e => e.EmployeeId == id);

seems to resolve the issue but I decided to leave that code out and just focus on the requirements provided in the sr-code-challenge-dotnet/ReadMe.md file.
