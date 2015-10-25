# mocha-slack-reporter
Mocha reporter that posts to Slack
## Usage
### Options
```js
reporterOptions = {
  username: "MCBrandenburg",
  channel: "#test",
  team: "team",
  token: "dhgahsgj",
  failIcon: ":warning:",
  passIcon: ":smile:",
  endIcon: ":bulb:",
  minimal: true,
  failureOnly:true
}
```
*minimal* If true, complete stats and failures will be sent.

*failureOnly*  If true only failures will be sent

#### Note: If both are true, will function like minimal

## Running the reporter
```js
mocha.reporter(slackReporter, reporterOptions);
mocha.run(function(failures) {
  process.on("exit", function() {
    process.exit(failures);
  });
});
```
