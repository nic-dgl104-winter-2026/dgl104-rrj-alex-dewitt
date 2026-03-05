

# WEEK 9

## RESEARCH ON DESIGN PATTERNS

### Singleton Pattern

**Summary**

The Singleton pattern is used when a program should only create one instance of a class and reuse it everywhere. Instead of creating multiple objects, the program makes one shared instance that the whole application can access. This helps keep things consistent when dealing with shared resources and stuff.

**Real-world example**

A common real-world use is a logging system. If every part of a program created its own logger, the logs could become messy or inconsistent. Instead, one shared logger instance is used across the whole application.

**Concrete example**

class Logger {
  constructor() {
    if (Logger.instance) {
      return Logger.instance;
    }
    Logger.instance = this;
  }

  log(message) {
    console.log("Log:", message);
  }
}

const logger1 = new Logger();
const logger2 = new Logger();

console.log(logger1 === logger2); // true


### Observer Pattern

**Summary**

The Observer pattern is used when one object needs to notify other objects when something changes. The main object is called the subject, and the objects receiving updates are called observers. When the subject updates, it automatically sends notifications to all observers.

**Real-world example**

A good example is notifications on social media. When someone you follow posts something, your app gets notified and updates your feed. The account posting would be subject, and all followers are observers.

**Concrete example**

class Subject {
  constructor() {
    this.observers = [];
  }

  subscribe(observer) {
    this.observers.push(observer);
  }

  notify(message) {
    this.observers.forEach(o => o.update(message));
  }
}

class Observer {
  update(message) {
    console.log("New update: ", message);
  }
}

const subject = new Subject();
const user = new Observer();

subject.subscribe(user);
subject.notify("New post available");


### Factory Pattern

**Summary**

The Factory pattern is used to create objects without being specific on exactly which class will be created. Instead of using constructors everywhere, a factory method decides which object to make based on conditions.

**Real-world example**

This pattern is often used in systems that create different types of objects depending on the situation. For example, a messaging app might create different message types such as text messages, image messages, or video messages.

**Concrete example**

class NotificationFactory {
  createNotification(type) {
    if (type === "email") {
      return new EmailNotification();
    }
    if (type === "sms") {
      return new SMSNotification();
    }
  }
}

class EmailNotification {
  send() {
    console.log("Sending email");
  }
}

class SMSNotification {
  send() {
    console.log("Sending SMS");
  }
}

const factory = new NotificationFactory();
const notification = factory.createNotification("email");

notification.send();


### Adapter Pattern

**Summary**

The Adapter pattern let two pieces of code to work together even if their interfaces don’t match. It works like a translator between systems so they can communicate without changing their original code.

**Real-world example**

Adapters are commonly used when working with third-party APIs or I think some older systems. If a library returns data in a format your app doesn’t expect, an adapter can convert that data into the format your program needs.

**Concrete example**

class OldUserService {
  fetch_user() {
    return { first_name: "Alex", last_name: "Dewitt" };
  }
}

class UserServiceAdapter {
  constructor(oldService) {
    this.oldService = oldService;
  }

  getUserName() {
    const user = this.oldService.fetch_user();
    return `${user.first_name} ${user.last_name}`;
  }
}

const oldService = new OldUserService();
const adapter = new UserServiceAdapter(oldService);

console.log(adapter.getUserName());



### Open Source Contributions – Summary and Reflection

After reading the “How to Contribute to Open Source” guide from GitHub, I learned that contributing to open source is not just writing code. Many projects actually need help with things like documentation, design, organizing issues, and helping other people. This surprised me because I originally thought open source contributions were mostly about coding. The guide also explained how open source projects are usually organized, with roles such as authors, maintainers, contributors, and community members. It also showed how tools like issue trackers and pull requests are used to discuss problems and review changes before they are added to a project.

Another important thing I learned is that communication is a big part of contributing. Contributors should give clear context when reporting issues or suggesting changes, and they should check documentation or previous discussions before asking questions. Being respectful and patient is also important because maintainers are often volunteers who review contributions in their free time.

In terms of how I would like to contribute, I think starting with smaller tasks would be the best approach. For example, I could help improve documentation, fix small bugs, or work on beginner-friendly issues. This would help me understand how a project works before trying to make larger contributions. Overall, this guide made open source seem much less intimidating and showed me that there are many ways to participate and learn from real projects.



### Project 1 – Appwrite

Source: https://goodfirstissue.dev
Repository: https://github.com/appwrite/appwrite

I found the Appwrite repository while browsing the Good First Issue website. Appwrite is an open source backend platform that helps developers build web, mobile, and AI applications. It provides features such as authentication, databases, storage, messaging, and hosting.

When exploring the repository, I noticed that it has a lot of stars and many contributors, which suggests that the project is very active. On the Good First Issue page I also saw several open issues such as bug reports and feature requests. This shows that the project is actively maintained and that contributors are working on making it better.

One interesting thing I discovered is that the project labels beginner-friendly issues, which makes it easier for new contributors to find tasks they can work on. This makes the repository a good project for someone who wants to start contributing to open source.

### Project 2 – Learn Git

Source: https://up-for-grabs.net
Repository: https://github.com/rcallaby/Learn-Git

I found the Learn-Git repository while looking through beginner-friendly open source projects. This repository is designed as a tutorial to help people learn how to use Git and GitHub. It includes guides that explain how to fork a repository, clone it to your computer, create branches, make edits, and submit pull requests.

One interesting file in the repository is the "First Contributions" guide, which walks beginners through the process of making their first contribution to an open source project. The instructions explain each step clearly and show how contributors can add their name to a file and submit a pull request. Projects like this exist to help new developers learn the open source workflow without needing to write complex code.

While exploring the repository, I noticed that it is fairly active and designed specifically for learning. The project also includes documentation and instructions that make it easy for beginners to understand how Git works. This makes it a good project for someone who is new.

### Project 3 – Godot Game Engine

Source: https://www.codetriage.com
Repository: https://github.com/godotengine/godot

While browsing CodeTriage I found the Godot repository. Godot is an open source game engine that developers use to create 2D and 3D games. It includes tools for graphics, physics, scripting, and scene management, letting developers build complete games inside the engine.

The project is very active and has a large community of contributors. The repository has many open issues and pull requests, which shows that developers are constantly improving the engine and fixing bugs. Because the project is widely used in game development, there are many different types of contributions, including code improvements, documentation updates, and bug fixes.

One interesting thing I discovered is how large the community around Godot is. Even though the project is complex, contributors can still help by working on smaller issues, reporting bugs, or improving documentation.

