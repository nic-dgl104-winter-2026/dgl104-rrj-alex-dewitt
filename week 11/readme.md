

# WEEK 11

# OOP Summary and Reflection (JavaScript)

## Applying OOP in My Task Management System

For my programming assignment, I can apply OOP in JavaScript by organizing my task management system into objects that have both data and behavior.

In this project, a task is an example of an object. Each task has stuff like:
- title
- assigned user
- due date
- priority
- status

It also has actions, like:
- being created
- being edited
- being marked as completed
- being deleted

Using OOP lets me to group this data and behavior together, which makes the code easier to understand and maintain.

### Example: Task Class

I can use a class to represent a task:

class Task {
  constructor(title, assignedTo, dueDate, priority) {
    this.id = Date.now();
    this.title = title;
    this.assignedTo = assignedTo;
    this.dueDate = dueDate;
    this.priority = priority;
    this.status = "To Do";
  }

  markComplete() {
    this.status = "Completed";
  }

  updatePriority(newPriority) {
    this.priority = newPriority;
  }
}

JavaScript is definitely OOP capable. It supports classes, objects, constructors, inheritance, and methods, so it can be used in an object oriented way pretty well. Though, JavaScript is not only an OOP language. It is considered a multi-paradigm language, which means it also supports other programming styles. It also supports procedural programming and functional programming. For example, I can write simple step by step functions, use loops and if/else, or use array methods like map, filter, in a more functional style.

Because of this, I would say JavaScript supports OOP. For my assignment, this is helpful because I can combine OOP for organizing tasks and users with regular functions for things like the interface, or saving data in localStorage. That makes JavaScript a good fit for this project because it lets me choose the style that makes the most sense for each part of the program.

