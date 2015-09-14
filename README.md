## Todo RPG

### Details

[TodoMVC](http://todomvc.com/) + [HabitRPG](https://habitrpg.com) = **TodoRPG**

We're going to view, create, and mark as completed a bunch of tasks that need to be completed in our bleeding edge, pre-alpha, state-of-the-art Task Management database\*. Each task will have a point value assigned to it.

\* - Do be advised that the Task Management database is currently unstable, and will reset every time the `npm start` script is run. This is a known bug. We're working on fixing this problem in a future release. Please continue to donate to our Kickstarter.

### Normal Mode

Users should, at a minimum, be able to:

* View all tasks (with their completed/incomplete state, and point values)
* View all completed tasks (and hide the incomplete tasks)
* View all incompleted tasks (and hide the complete tasks)
* Mark an incomplete task as completed
* Mark a completed task as incomplete again
* Create a new task (with a point value)
* View the total number of "experience" points earned from completed tasks

You can make use of the following routes, which are provided already on your server.

* **GET** `/tasks` - Returns all tasks
* **GET** `/tasks/complete` - Returns all completed tasks
* **GET** `/tasks/incomplete` - Returns all incomplete tasks
* **GET** `/tasks/:taskId` - Returns a single task with the specified ID
* **POST** `/tasks` - Creates a new task. In the data sent to the route, you need to pass in the parameters `task` with the task name, and `value` with the point value.
* **PUT** `/tasks/:taskId` - Edits the task using the data sent to the route.

**What does this look like?** That's 100% up to you! Make it something you're proud of, though; this will form a part of your eventual portfolio to show to potential employers.

### Hard Mode

This assignment may be pretty challenging (and definitely substantive), so if you're used to getting into and through Hard Mode, don't get discouraged if you get tripped up here.

That said, hopefully you'll be able to get through it and still want some more. If that's the case, then implement the following features...

1. Make it **responsive**! It should work as well on my phone as my computer, and not look hideous on either.

2. A **statistics view**. This can either be on the same page as the rest of the content, or on another page. Make sure that it displays:

* The number of experience points earned
* The number of levels gained
* The number of experience points until the next level
* The number of tasks completed 
* The percentage of tasks completed

All of these are available through the **GET** `/stats` route, which is also already created for you.

