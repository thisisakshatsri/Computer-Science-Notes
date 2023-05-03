# Angular Basics

# What is Angular?

Angular is a JavaScript framework for building web applications.
It's maintained by Google and has a large community of developers contributing to it.
Angular is built on TypeScript, a superset of JavaScript that adds features like static typing, interfaces, and classes.
Getting Started with Angular
To get started with Angular, you'll need to install Node.js and the Angular CLI (Command Line Interface).
You can create a new Angular project using the ng new command, followed by the name of your project.
Once your project is created, you can run it using the ng serve command. This will start a local development server that you can access in your browser at http://localhost:4200.
Components
In Angular, components are the building blocks of your application.
A component is a TypeScript class with a decorator that specifies its metadata, such as its template and styles.
You can create a new component using the ng generate component command, followed by the name of your component.
Templates
Templates are the HTML markup that defines the view for your component.
In Angular, you use a special syntax called "interpolation" to bind data from your component to your template.
You can also use directives like *ngIf and *ngFor to conditionally render elements in your template.
Services
Services are used to provide functionality that can be shared across multiple components.
A service is a TypeScript class with a decorator that specifies its metadata, such as its provider.
You can create a new service using the ng generate service command, followed by the name of your service.
Dependency Injection
In Angular, you use dependency injection to provide instances of services to your components.
Dependency injection is a design pattern that allows you to write more modular and testable code.
You can use the constructor of your component to specify the dependencies that it needs.