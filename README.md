# Basic PHP TODO Application

Using either CakePHP, Symfony, Laravel, or Yii

> Before you can start, you should prepare your development environment.

## This test requires:

- access to the internet
- a php capable IDE (we suggest PhpStorm)
- working setup of PHP 7.1+
- mySQL 5.8+ (recommended)
- composer ([getcomposer.org](https://getcomposer.org/doc/00-intro.md#installation-linux-unix-macos))
- nginx or alternative simple web server

## Setting up your development environment

In order to develop an application using any of the above frameworks, you might want to use a virtual development environment instead of the built-in server or WAMP/LAMP. Homestead is an easy-to-use Vagrant box to get a virtual environment up and running quickly.

Before you can use Homestead, you need to install and configure Vagrant and Homestead as explained in the Homestead documentation.

## Resources

- [Homestead Documentation](https://laravel.com/docs/homestead)
- [Vagrant Documentation](https://www.vagrantup.com/)

## Application User Stories

The below user stories will provide details for what features the application should have.

*Story #1* - As an authenticated user, I want to create a task.

*Acceptance criteria*

- Given I’m on the create task screen,
- And I’m logged in,
- I can see four required input fields on the page
  - task name (text)
  - description (text area)
  - status (select list - Not Started, In Progress, Completed)
  - assign user (select list),
- then I fill all the above required input fields,
- And I press the “Submit” button
- I should be redirected to the home page
- And I see the new task


*Story #2* - As an unauthenticated user, I can view all the tasks

*Acceptance criteria*

- Given that I’m on the homepage,
- I can see all the tasks in a table,
- With five columns (name, description, status, username, action),
- And I can see the "edit" and "delete" links within the action column,
- The tasks are paginated with 10 records on each page,

*Story #3* - As an unauthenticated user, I can log in

*Acceptance criteria*

- Given that I'm on the homepage,
- I can see a login link,
- When I press the login link, 
- Then I'm redirected to the "login" page,
- And I can see two required input fields on the page
  - username
  - password
- Then I fill all the above required fields with the correct details,
- And I press the "Login" button,
- Then I should be redirected to the home page,
- And I see a logout link,
- But I do not see a login link

*Story #4* - As an authenticated user, I can update a task

*Acceptance criteria*

- Given that I'm on the homepage,
- I can see a list of tasks each with an edit link,
- And I press the edit link for task #1,
- Then I am redirected to the edit task page,
- I can see three required input fields on the page
  - task name (text)
  - description (text area)
  - status (select list - Not Started, In Progress, Completed)
- Then I fill all the above required input fields,
- And I press the “Submit” button,
- Then I should be redirected to the home page,
- And I see the task with updated data

*Story #5* - As an authenticated user, I can delete a task

*Acceptance criteria*

- Given that I'm on the homepage,
- I can see a list of tasks each with a delete link,
- Add I press the delete link for task #1,
- Then I see a confirmation popup with a confirm button,
- And I press the confirm button,
- Then I am redirected to the home page,
- And I cannot see task #1 listed on the homepage

## Add / Edit Task Form Notes
- When submitting the form, validation rules should be enforced
- If at least one field fails validation, the form should not be submitted
- A validation error should be displayed to the user for every field that fails validation

## Bonus User Story

If time permits or you want to have some more fun, feel free to implement the below user story.

As an unauthenticated user, I can filter tasks based on status

*Acceptance criteria*

- Given that I’m on the homepage,
- I can see all the tasks in a table as described in Story #2,
- And I can also see a dropdown filter that contains the available task statuses,
- And I can see a search button,
- I select a status from the dropdown,
- And I press the search button,
- I can only see the tasks with the selected status.

## General Notes
1) If you're looking for a timeframe estimate, we estimate this application to take roughly 5-7 hours of development time. We don't want you to worry too much about time though. We understand that everyone has busy lives and generally not much free time so we want you to focus on quality of code instead of sheer speed.

2) There may be questions that arise during development. We encourage you to ask as many questions as you'd like. If you do have questions please send them to [Derek Fulginiti](mailto:dfulginiti@harborcompliance.com) and he will get back to you as soon as possible.

3) When you begin your application please create a repository and send an email to [Derek Fulginiti](mailto:dfulginiti@harborcompliance.com) containing a link to the repo. We encourage you to commit early and often so that it's easy for us to track your thought processes and workflow patterns.

Happy Coding!
