## AngularJS & Angular
There are two major versions that differ a lot from each other due to complete rewrite of framework  
Angular 1.x : AngularJS  
Angular 2+ : Angular  

## Pre-requisites
**IDE:** Visual Studio Code. (https://visualstudio.microsoft.com/downloads/)  
**Stack:** Angular 4  

## Basics

**File extensions:**  
`.html:`            html for Component  
`.scss, css, sass:` Cascading style sheets .scss is what we will be using  
`.ts:`              typescript file which will be compiled to javascript file during compilation  
`.spec.ts:`         test classes for karma  

 **Component:**  
  The component is the core building block of Angular 2 applications. It represents a reusable piece of UI that is usually depicted by a custom html element.  
  
 **Typescript/Es6 Module:**  
  Generally, a module will contain code that encapsulates a specific functionality. The module will expose this functionality to the rest of the application by defining a series of exports that other parts of the system can then import.  
  
 **Angular Module:**   
 Angular 2 modules and the new NgModule decorator let us declare in one place all the dependencies and components of our application without the need to do it on a per-component basis (like we used to do in previous versions)  
 
 **Decorator:** 
 Similar to Annotations in java except it decorated and calls the function internally.  
 **`` ` `` :** to write multi-line string in html template.  Backticks are used to define the new ES6 template strings. They are a new great feature of ES6 that let’s you write multiline strings natively and insert any expression directly within a string with a very straightforward syntax.  
 
 **classes in Javascript:**  
 ES6 brought classes to JavaScript amongst a host of other features. If you are a software developer with a strong typed language as background this will probably be great news for you. Don’t be fooled though, JavaScript classes are just syntactic sugar over the existing prototypical inheritance model.  
 
 **Type Annotations:**  
 TypeScript let’s you add type annotation to your variable and function declarations. This helps you with better tooling like intellisense and to catch type errors.  
 
 **Type of data Bindings:**  
Interpolation: {{}}        e.g. {{propertyName}}  
one way data Binding: []   e.g. [src]  
event binding: ()          e.g. (click)    
Two-way data Binding: [()] e.g. [(person.name)]  

**Lint:** process of finding issues before compile time only. A code was developed in C named Lint that found issues before compilation only.

## Installations
Node  
npm  
Angular-cli  
Update and install  
npm uninstall -g @angular/cli  
npm cache verify  
npm install -g @angular/cli@latest  

## Module 1: Scaffolding/starting project  
You can quick start angular2 project in two ways:
1. https://angular.io/guide/setup (for learning purpose, structure already available to start with)  
2. https://angular.io/guide/quickstart : Angular CLI (Preferred)  

**A. Install angular-cli and ceate new Project**
     command will create "angular-get-started" project with routing already configured alon with scss for styling
     ```cmd   
        npm install -g @angular/cli@latest
        ng new angular-get-started --routing --style scss
        ***after 7-10 minutes project created***
     ```   
   
**B. Folder structure of newly created project**  
```node	
  angular-get-started
    - src
      - app                        # your app source code (and specs)
      	 - app.component.html      # html for App component  
	 - app.component.scss      # styling for App component  
	 - app.component.ts        # controller for App component 
	 - app.component.spec.ts   # test file for App component  
	 - app.module.ts           # App Module
	 - app-routing.module.ts   # Routing module
      - assets                     # static assets like images, etc (same as resources folder in Java)
      - environments               # here you can define different environment configuration (prod, dev, etc)
         - environment.ts          # ng serve --dev 
	                             (to make this run, there must be environments entry in .angular-cli.json)
 	 - environment.prod.ts     # ng serve --prod
      - index.html                 # the entry point to your app
      - main.ts 		   # it is defined in .angular-cli.json, it bootstraps AppModule 
      - styles.scss                # the global styles for your app
 Server used : lite-server (need to check where it is defined)
 
 # dependency management
  angular-get-started
    - node_modules          # the source code of your app dependencies
                            # you do not commit this folder, generated after npm install
    - package.json          # all dependencies are defined here (same as pom.xml in Maven)
	                    # npm reads all the dependencies and downloads into node_modules
			    
 # Angular-cli configuration (Important file)
  .angular-cli.json        
  
 # TypeScript configuration
 angular-get-started
    - tsconfig.json         # TypeScript compiler configuration
    - tslint.json           # TypeScript linting configuration
	
 # Testing
 angular-get-started
    - e2e                   # a folder with end to end tests
    - karma.conf.js         # karma test runner configuration
    - protractor.conf.js    # protractor e2e tests configuration
	
 # Git specific
 angular-get-started
    - .gitignore
    - README.md
```

**C. Start Project**
webpack will build the project and serve it in browser because of -o parameter passed while serving
```cmd
ng serve --open
#the short-hand syntax is: ng s -o
```

**D. Create Component**
```cmd
ng g c -it -is person-details
#ng generate component --inline-template --inline-style
```
**Note:** Angular CLI relies on Webpack to inject styles and JavaScript files when they are needed.

## Module 2: Generators
Angular-cli intoduces generators that creates files and do respective mappings related to it as well   
e.g.: ng generate interface person (ng g i person)  
      ng generate --inline-template person-list (ng g c -it person-list)  
This will generate a new folder person-list and will place a TypeScript and a style files within that folder. Since we have selected the --inline-template option, instead of using an external template file the component will use the template property inside the @Component decorator to define an inline template
	  
**1. Create domain model** 
   new file > person.ts > export interface Person { id : number  .....}  
   *create person.ts in src/app folder. the reason for keeping model (and later services ) in the root app folder makes it easy to reuse in different modules.  
                             **OR**  
 **angular-cli:** ng generate interface person (ng g i person)
 
**2. Create Component**
   Each component should be place in its own folder to keep all related files to that component in one place.  
   a. Create Folder people-list  
   b. Create Component people-list.component.ts   
   (we will use inline template and inline style for this else there will be 2 more files in this folder)   
   c. As we do not have any service now we can return hard-coded data from our component. Define person array with the help of person model created above.  
   d. use Structural directive *ngFor to repeat this array and print on html.  
   e. add this component in app.module.ts on the declarations.  
   f. use the app-people-list selector in the app.component.html  
                              **OR**   
 **angular-cli:** ng generate --inline-template person-list (ng g c -it person-list)

## Module 3: Fetch data from services
  a. create heroservice.ts > @Injectable() export class HeroService  
  b. use constructor injection to inject this service in person-list component.  
  c. if you start the server now you will see "Error: No provider for HeroService!"  
  d. add this service in app.module.ts in the providers array.  
                              **OR**  
 **angular-cli:** ng generate service heroservice (ng g s heroservice)  
	          ng generate service heroservice --module app ()  

**References:**
Style-guide: https://angular.io/guide/styleguide  
good reference: https://www.barbarianmeetscoding.com/blog/categories/angular2-step-by-step/  
