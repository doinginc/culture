**[⬅ Back to Coding Culture](../README.md)**

# Testing Standards

This is pretty straight forward.  A Pull request into a Doing Github project **requires testing**. If you are adding, changing or removing anything you should really make sure you have written a test for it.  You should use your projects existing testing environment when adding new tests.

**Here are the different kinds of tests you should consider writing tests for:**

## Unit Test:

Unit Testing is a software development process in which the smallest testable parts of an application, called units, are individually and independently scrutinized for proper operation.

## Integration Test:

Integration Testing is the phase in software testing in which individual software modules are combined and tested as a group. It occurs after Unit Testing and before Acceptance Testing.

## Sanity Test:

Sanity Testing is preliminary testing to reveal simple failures severe enough to reject a prospective software release.

## Regression Test:

Regression Testing is a type of software testing that seeks to uncover new software bugs, or regressions, in existing functional and non-functional areas of a system after changes such as enhancements, patches or configuration changes, have been made to them.

## Acceptance Test:

Acceptance Testing is a test conducted to determine if the requirements of a specification or contract are met.

## System Test:

System Testing is conducted on a complete, integrated system to evaluate the system's compliance with its specified requirements. System testing falls within the scope of black box testing, and as such, should require no knowledge of the inner design of the code or logic.

## Pre-flight Check:

Pre-flight Checks are tests that are repeated in a production-like environment, to alleviate the 'builds on my machine' syndrome. Often this is realized by doing an acceptance or smoke test in a production like environment.
