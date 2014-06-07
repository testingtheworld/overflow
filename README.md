# DBC Overflow

## Learning Competencies

## Summary

Let's get our feet wet building a substantial Rails application from the
ground up: a [StackOverflow](stackoverflow.com) clone.  The goal is to focus on
building a well-structured Rails application with a good mixture of front-end
and back-end features.

Use the "DBC Rails stack": enable rspec, shoulda, and factory_girl, but disable
coffeescript and Sass. Remember, to create a new Rails application without the
default testing framework run:

```text
$ rails new dbc_overflow -T
```

## Release 0: User Authentication

### Objective

Pretty much every application on the internet has users divided into two
primary classes: those we know and those we don't know (yet).  We need to
provide a different experience for these two classes of users.

### Features

We'll revisit some of the ideas which you learned in Phase 2 Portfolio
Challenges.  We want to have a logged-in and logged-out experience.  Implement
the following features:

* An anonymous user visits a front-end "landing page" for the app which
  describes the application by name
* An anonymous user can sign up
* An registered user can log in
* A logged in user can log out
* A logged in user sees a different landing page for '/' than an anonymous
  user

### Acceptance Criteria

Controller tests demonstrate that the features are successfully implemented.
If additional models are created, please include unit tests.

## Release 1:  Question CRUD

### Features

* An anonymous user / authenticated user can see a list of questions
* An anonymous user / authenticated user can click on a question to see it ( and maybe some stub
  text indicated responses will come later!)
* An authenticated user can post a question
* An authenticated user can edit their own question, can delete their own
  question

### Acceptance Criteria

Controller tests demonstrate that the features are successfully implemented.
If additional models are created, please include unit tests.

You have now developed a **critical path** which is the story of an
unauthenticated user logging in, posting a new question, and then viewing that
question and then deleting that question and validating the deletion.  This one
"story" validates a lot of the functionality of your application.  You should
drive this as an _integration test_ using Capybara.

## Release 2:  Answers and Comments

### Features

* Authenticated users can provide an answer to a question and can delete / edit their
  own answers
* Authenticated users can provide an comment to a question and can delete / edit their
  own comments
* Authentication users can see a list of their comments
* Authentication users can see a list of their answers
* Any user can visit a question page and can see the question and its answers
  and comments

Expand your integration test to cover this addition to your _critical path_.

## Notes

These instructions are left deliberately ambiguous, both to give you
flexibility in your implementation and because clarifying ambiguous
requirements is at least 30% of an engineer's job.  At least.

## Additional Feature Ideas

If you have free time, feel free to...

* Expand your tests
* The person who posted a question can declare one of the user-submitted answers "the best."
* Users should be able to see questions sorted three ways: highest-voted, most recent, and "trending."
* Responses should be sorted chronologically, with oldest first.  Answers should be sorted by "the best" first, followed by most highly-voted.
