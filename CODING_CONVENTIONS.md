# Coding Conventions
## Front-end
### Quality assurance
To assure quality in the front-end TSLint is used. When creating a pull-request the code is automatically linted by the pipeline. You can run the linter locally by using `ng lint`.


### Naming conventions
When creating a new component we have a strict naming convention to main readability. Please make sure the following steps are followed when creating new components:

* An issue exists relating to the component.
* A branch exists relating to the issue.
* You are working on the branch relating to the issue.
* The name of the component is:
	* All lower case
	* Name starts with: `app`
	* A `-` between words
	* The name ends with what the component is going to be used for (i.e page, dialog, menu)
	* The module being used is the default `app.module.ts`
	* Ex: `ng new component app-student-rental-page --module=app.module.ts`


## Backend
### Quality assurance
When creating a pull request the pipeline is going to automatically push your code to the SonarCloud environment. We ask you to try and fix as many code smells and bugs relating to your own code as possible.

### Coding conventions
For the backend we use the standard [C# coding conventions](https://docs.microsoft.com/en-us/dotnet/csharp/fundamentals/coding-style/coding-conventions). When contributing pay extra attention to the following points:

* Names of methods are relating to the functionality and contain non to almost non duplicate code.
* Methods are commented with: a summary what the functionality does, details about the parameters the method receives and what the method returns.
* All methods are thoroughly tested in the dedicated test projects.  
* Names of variables are readable and describe what kind of data they hold.
* The `ocelot.Production.json` and `ocelot.Development.json` are both updated with the possible new endpoints.
