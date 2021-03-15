# simple-cucumber-demo
Basic cucumber framework used for running automation tests on Jenkins.

## Running locally
To run locally and generate HTML reports, use this maven goal *verify*. HTML reports should be generated under target/cucumber-html-reports
```
mvn verify
```

## Jenkins
Install [Cucumber HTML report plugin](https://plugins.jenkins.io/cucumber-reports). Create a simple job and use this repository in the repository url field. In the post build actions, select option Cucumber reports and point to the location of the cucumber json report. Run the project as a maven goal *test*.

```
mvn test
```
## Tags
You can pass a custom tag using terminal. Available tags are **@smoke**, **@regression**. 

```
mvn test -Dcucumber.filter.tags="@smoke"
```
## Browsers
You can pass change using command line argument BROWSER
```
mvn test -DBROWSER=firefox

```
