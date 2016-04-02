# Easy Bake Testing
### What we get out of the box with Ember
QUnit
- This is not an Ember-specific framework
- Ember Test Helpers
- Testem (test runner for QUnit)
- Ember Acceptance Test Helpers

Ember Acceptance Test Helpers
- Async: `click`, `fillIn`, etc.
- Sync: Anything that involves getting information in the current state
- `andThen`: Waits for all async behavior before the next step

All test instructions are executed in order

### Unit Tests
Should be completely isolated. Only testing the code itself, not user interaction

### Acceptance Tests (We call them Functional)
Tests for user interactions

### Integration Tests
Tests important workflows under more specific conditions (user types, etc)

### Mocks, Spies, and Stubs
They help us isolate unit Tests
- Sinon.js is a good option (has an ember addon)
- Mocks are preprogrammed API calls
- Spies are good for handling a set number of calls of a certain type
- Stubs are a type of Spy

Mirage is a good solution for mocking API calls
- Sinon offers mocks but Mirage is better (why?)
- Can also be used outside of testing, when an API isn't ready but you want to prepare the front-end

### Other Test Frameworks
- Jasmine: Behavior-Driven Test Framework
  - Doesn't have any dependencies
  - Doesn't even depend on a DOM
- Chai: Assertion Library
  - Apparently it's a pain to use with Ember and QUnit
- Mocha: Similar to QUnit but can use any assertion library (Good if you want to use Chai)
- Selenium: End to End Testing
  - Difficult to hook up to Ember and very slow runtime

### Best Practices
- UI changes make tests brittle when class names change
  - Page Object helps with that (theres an ember addon)
  - [Relevant blog post here](http://martinfowler.com/bliki/PageObject.html)
- Write test helpers to keep things DRY
- Keep tests discrete and isolated
- There should be mostly acceptance tests, followed by integration, followed by unit

This talk is a follow up to one she did last year: https://vimeo.com/146960505
