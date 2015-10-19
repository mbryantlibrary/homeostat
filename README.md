#homeostat

A key aspect of [TDD](http://agiledata.org/essays/tdd.html) is, well, running tests. Developers practicing TDD are often advised to keep unit test suites as quick to execute as possible in order to encourage more test runs. However this often doesn't take into account the effort required to actually run the test suite (e.g. clicking a button in an IDE or switching to a shell and typing a command). What if we could automate this process so that the developer doesn't have to think about it? This is [Continuous Testing](https://en.wikipedia.org/wiki/Continuous_test-driven_development): the developer gets instant feedback on their changes when they save a file, speeding up development time.

Similar tools exist, e.g. Karma/Grunt Watch, [Autotest](https://github.com/grosser/autotest) and [Infinitest](http://infinitest.github.io/), but these are generally language-specific tools and provide limited feedback. **Homeostat** is a Continuous Testing tool designed to work fully, with any testing tool that can output in a [JUnit-style XML format](http://junitpdfreport.sourceforge.net/managedcontent/PdfTranslation), otherwise it works with any command-line based test utility. It works by watching for changes to specified files, running a prespecified test command and parsing the XML report output, displaying the results in a browser window.

Homeostat is not designed to be a Continuous Integration server; it is designed to provide rapid feedback during development.

###Features planned for v0.5
- Watches a prespecified list of files for changes
- Runs a series of prespecified utilities when the files change
- Displays test results in a browser window
