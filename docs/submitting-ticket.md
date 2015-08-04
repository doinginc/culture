**[⬅ Back to Coding Culture](../README.md)**

# Submitting a Ticket

**ATTENTION:** While creating tickets is the only way to assign a task to be completed, it is equally important to not flood the development team with tickets that are not actually necessary ( might be a duplicate, already being worked on, not actually an issue, etc ).  So before you create a ticket, please contract a lead engineer or product owner and make sure that the item you wish to create a ticket for should, in fact, have a ticket created for it.  Sprintly users abusing this privilege will have their permissions removed to create tickets.

## Introduction

To submit a ticket, login to our [Sprintly Dashboard](https://sprint.ly) and click the **Add item** button at the top of the page.

You will need to choose the type of ticket you are going to submit:

* **Story:** Usually encapsulate new features or meatier initiatives. Use them as mini projects. A good rule of thumb is if it requires more than one concrete step and/or requires more than one person to complete, it's a story. _e.g. As a user, I want Search integration so that I can find what I am looking for with ease_.
* **Task:**  Discrete units of work. _e.g. Add field foo to table bar._
* **Defect:** Things that aren't working that need to be fixed. Some customers also use these for maintenance tasks. _e.g. The CSS isn't rendering correctly in IE6._
* **Test:** Any work related to QA, automated testing, and acceptance tests. _e.g. Create a new Selenium test for the forgot password flow._

**Note:** Stories are a special type of item. They can have sub-items. This means you can create an unlimited number of tasks, defects, and tests grouped under a story. Each sub-item can be individually assigned and gets its own item detail (permalink) page.

## Creating a New Item

**Please use our [Ticket Template](../templates/ticket-template.md) to make sure you are entering all the information we will need to complete the item you are about to create.**

To create a new item, click the green "Add item" button in the top right of the header.

Next you will want to choose an appropriate item type.

![add item](http://cl.ly/image/3h3m1u092s1U/Screenshot%2012%3A21%3A12%2012%3A35%20PM-2.png&key=afea23f29e5a4f63bd166897e3dc72df)

Once you've selected a type and filled out the required fields, it would be a good idea to add a few tags to classify your new item.

### What should I use tags for?

You can use tags for all sorts of things. We suggest using tags extensively for classification. Below is a sampling of ways to use tags:

* **Tracking sprints/iterations** Tag things like `#sprint1`, `#sprint2`
* **Tracking milestones** Give major milestones code names and use tags to track them `#v1.0.0`
* **Components, platforms, etc.** Common tags in this space might be `#api` or `#mobile`

### Who should I assign it to?

If you're not sure who you should assign something to, assign it to a team lead or manager who can route the ticket appropriately.

### Where did my newly created item go?

Most newly created items should go to Someday. You can get to Someday by selecting the Organizer from the header menu and selecting the Triage tab just below the filter bar.

### Is there a character limit?

The `title` field of Tasks, Defects and Tests have a character limit of 255 characters. For Stories, each of the individual `Who`, `What` & `Why` fields have a limit of 255 characters.

### Editing an Item

Click the gear icon and select Edit Item. Make your edits and click Update to save your changes. While in edit mode, you may have the option of changing the item type. Click on the new item type that you want it changed into and select Update. Since stories are unique in that they have sub-items, Stories cannot be changed into a task, defect or test.
