
# Contributing to ACI Rental

We'd love for you to contribute to our source code and to make ACI Rental even better than it is
today!

Here are the guidelines we'd like you to follow:

 - [Issues and Bugs](#issue)
 - [Submission Guidelines](#submit)
 - [Contributing as an 'insider'](#insider)
 - [Contributing as an 'outsider'](#outsider)
 - [Getting started](#started)
 - [Coding Format](#format)
 - [More information](#moreinfo)

## <a name="issue"></a> Found an Issue?

If you find a bug in the source code or a mistake in the documentation, you can help us by
submitting an issue to this repository. Even better you can submit a Pull Request
with a fix.

## <a name="submit"></a> Submission Guidelines

### Submitting an Issue
If your issue appears to be a bug and hasn't been reported, open a new issue. Help us to maximize
the effort we can spend fixing issues and adding new features, by not reporting duplicate issues.
Providing the following information will increase the chances of your issue being dealt with
quickly:

* **Overview of the Issue** - if an error is being thrown a non-minified stack trace helps
* **Reproduce the Error** - provide details, if possible, on how to reproduce the error
* **Related Issues** - has a similar issue been reported before?
* **Suggest a Fix** - if you can't fix the bug yourself, perhaps you can point to what might be causing the problem (line of code or commit)

## <a name="insider"></a> Contributing as an 'insider'
Please follow the steps below when you are a member of this repository and would like to contribute.
### Submitting a Pull Request
Before you submit your pull request consider the following guidelines:

* Search the repositories for an open or closed Pull Request
  that relates to your submission. You don't want to duplicate effort.
* Make a branch with the following conventions:
	* Issue for the bug or feature exists
	* Starts with the number of the issue
	* Branch is based on `dev`
	* Ex: `45-add-rental-page` or `46-fix-login-null-exception`
* Create your patch and run/create the appropriate tests
* Follow our [Coding Format](#format).
* Commit your changes using a descriptive commit message that uses the imperative, present tense: “change” not “changed” nor “changes”.
    
    ```shell
    git commit -a
    ```    
    Note: the optional commit  `-a`  command line option will automatically “add” and “rm” edited files.
* Push your branch to GitHub:

    ```shell
    git push origin 45-add-rental-page
    ```


In GitHub, send a pull request to `[aci-frontend/aci-backend]:dev`.
If we suggest changes, then:

* Make the required updates.
* Re-run the application and make sure any and all tests are still passing.
* Commit your changes to your branch (e.g. `45-add-rental-page`).
* Push the changes to your branch (this will update your Pull Request).
If the PR gets too outdated we may ask you to rebase and force push to update the PR:

```shell
git fetch upstream
git rebase upstream/master
git push origin my-fix-branch -f
```

That's it! Thank you for your contribution!

## <a name="outsider"></a> Contributing as an 'outsider'
Please follow the steps below when you are not a member of this repository, but would still like to contribute to this project.

### Submitting a Pull Request
Before you submit your pull request consider the following guidelines:

* Search the repositories for an open or closed Pull Request
  that relates to your submission. You don't want to duplicate effort.
* [Fork](https://help.github.com/articles/fork-a-repo/) either the front-end, backend or both.
* [Clone](https://help.github.com/articles/cloning-a-repository/) your copy.
    ```shell
    git clone https://github.com/YOUR_USERNAME/[aci-frontend/aci-backend].git
    cd [aci-frontend/aci-backend]/
    ```
* After cloning, set a new remote [upstream](https://help.github.com/articles/configuring-a-remote-for-a-fork/) (this helps to keep your fork up to date)
    
    ```shell
    git remote add upstream https://github.com/SieBrum/[aci-frontend/aci-backend].git
    ```

* Make your changes in a new git branch:

    ```shell
    git checkout -b my-fix-branch dev
    ```

* Create your patch and run appropriate tests.
* Follow our [Coding Format](#format).
* Commit your changes using a descriptive commit message that uses the imperative, present tense: "change" not "changed" nor "changes".

    ```shell
    git commit -a
    ```
  Note: the optional commit `-a` command line option will automatically "add" and "rm" edited files.

* Push your branch to GitHub:

    ```shell
    git push origin my-fix-branch
    ```

In GitHub, send a pull request to `[aci-frontend/aci-backend]:dev`.
If we suggest changes, then:

* Make the required updates.
* Re-run the application and make sure any and all tests are still passing.
* Commit your changes to your branch (e.g. `my-fix-branch`).
* Push the changes to your GitHub repository (this will update your Pull Request).

If the PR gets too outdated we may ask you to rebase and force push to update the PR:

```shell
git fetch upstream
git rebase upstream/master
git push origin my-fix-branch -f
```

That's it! Thank you for your contribution!

#### After your pull request is merged

After your pull request is merged, you can safely delete your branch and pull the changes
from the main (upstream) repository:

* Delete the remote branch on GitHub either through the GitHub web UI or your local shell as follows:

    ```shell
    git push origin --delete my-fix-branch
    ```

* Check out the master branch:

    ```shell
    git checkout dev -f
    ```

* Delete the local branch:

    ```shell
    git branch -D my-fix-branch
    ```

* Update your master with the latest upstream version:

    ```shell
    git pull --ff upstream master
    ```
## <a name="started"></a> Getting started
### Frontend
Start out by cloning the repository:
Insiders (please refer to [Contributing as an 'insider'](#insider) for more information)
```shell
mkdir ACI && cd ACI
git clone https://github.com/SieBrum/aci-frontend.git
```
Outsiders (please refer to [Contributing as an 'outsider'](#outsider) for more information):
```shell
mkdir ACI && cd ACI
git clone https://github.com/<YOUR_USERNAME>/aci-frontend.git
```
After this, install all the packages:
```shell
npm install
```
After this the application can be started using:
```shell
npm run
```
### Backend
Start out by cloning the repository:
Insiders (please refer to [Contributing as an 'insider'](#outsider) for more information):
```shell
cd ACI
git clone https://github.com/SieBrum/aci-backend.git
```
Outsiders (please refer to [Contributing as an 'outsider'](#outsider) for more information):
```shell
cd ACI
git clone https://github.com/<YOUR_USERNAME>/aci-backend.git
```
After this the project can be started using Visual Studio or the dotnet command line. 
To run multiple services:
```
Right click solution -> Startup project -> Mutliple startup projects -> set the desired microservices to 'Start'
```
   
## <a name="format"></a> Coding Format
Please read our [code conventions](https://github.com/SieBrum/aci-docs/blob/main/CODE_CONVENTIONS.md) to ensure code quality and readability.

## <a name="moreinfo"></a> More information
For more information about contribution, design-choices, deployment and code quality, please refer to the folder `docs` in this repository.
