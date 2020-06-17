<!-- PROJECT LOGO -->
<br />
<p align="center">
  <a href="https://github.com/akhilben/angular-best-practices">
    <img src="images/logo.svg" alt="Logo" width="100%">
  </a>

  <p align="center"> <b>
    :star: A curated list of Angular best practices and tips for building scalable and performant enterprise level applications. :star: </b>
    <br />
    <a href="https://github.com/akhilben/angular-best-practices/issues">Report Bug</a>
    ·
    <a href="https://github.com/akhilben/angular-best-practices/issues">Request Feature</a>
  </p>
</p>

<br />

<!-- ABOUT THE PROJECT -->
## `🌟 Preface`

This repo serves as a reference handbook for both starters and experienced developers to look at from time to time to refresh memory and to develop better :notebook:.

> :warning: **_Warning_** : The contents in this document are just general suggestions taken from the Angular community on how to do stuff. As there can be many solutions to a problem, just take the contents as mere suggestions for developing a good application, make use of it if you think it suits your application.

Do lookout (and don't ignore :eyes:) for the **_Tips_** section to find out how to do things more better. Make sure to **expand the collapse** of a section; it's there just for a better user experience. Get the summarized points labelled as **_Takeaway_** at the end of each section if you don't want to spend your time to read the whole.

Now, step in to find some of the recommended good practices and tips for building awesome Angular applications :confetti_ball: :tada:.

<br />

<!-- TABLE OF CONTENTS -->
## `📑 Table of Contents`

* [Preface](#-preface)

* [IDE and Plugins](#sunglasses-ide-and-plugins)

* [Using Starter Kits](#tada-using-starter-kits)

* [Commit Guidelines](#snowflake-commit-guidelines)

* [Configuring Your Project](#construction_worker-configuring-your-project)

* [Folder Structure](#books-folder-structure)

* [Performance Cheatsheet](#zap-performance-cheatsheet)

	* [Function calls in templates](#1-avoid-function-calls-in-templates)
	
	* [Use trackBy](#2-use-trackby-with-ngfor)
	
	* [Tree shakable providers](#3-use-tree-shakable-providers)
	
	* [Unsubscribe observables](#4-unsubscribe-observables)
	
	* [Async pipe](#5-use-async-pipe)
	
	* [Lazy load modules](#6-lazy-load-modules)
	
	* [Preloading strategy](#7-use-preloading-strategy)
	
	* [Lazy load components](#8-lazy-load-components)
	
	* [ChangeDetectionStrategy.OnPush](#9-use-changedetectionstrategyonPush)
	
	* [Disable change detection](#10-disable-change-detection)
	
	* [Run outside angular](#11-run-outside-angular)
	
	* [Other techniques](#other-performance-optimisation-techniques)

* [Contributing](#contributing)

* [License](#license)

* [Acknowledgements](#acknowledgements)

<br />

<!-- CHOOSING IDE -->
## `😎 IDE and Plugins`
<details>
  <summary>Click to expand</summary>
There are several powerful free and paid IDE's available in the market today. Choosing the right IDE is very important for development since not all IDE's are great for every language/framework/library. Have added a list of awesome plugins/extensions for IDE's below for a smooth development.

1. <img src="images/code.svg" alt="VS Code" width="30" height="30" vertical-align="middle"> &nbsp; <b>[Visual Studio Code](https://code.visualstudio.com/)</b><br />
   VS Code is a very powerful code editor from Microsoft which is highly recommended for working with Angular. Why? It has a great <b>support for TypeScript</b> out of the box. Moreover, it has <b>syntax highlighting</b> and autocomplete with <b>IntelliSense</b>, which provides smart completions based on variable types, function definitions, and imported modules. Adding up to many other powerfull features, it is <b>highly customizable with tons of extensions</b>, especially for Angular. Below is a list of few vs code extensions that are useful while developing Angular applications. <br />
   * [TS Lint](https://marketplace.visualstudio.com/items?itemName=ms-vscode.vscode-typescript-tslint-plugin):<br />
   A must have extension which marks the code where you have a problem and display a <b>list of warnings & errors</b> on hovering it. It even have an <b>autofix problems</b> functionality. This will help you to adhere to the recommented styleguides and conventions for Angular.<br />
   * [Angular Language Service](https://marketplace.visualstudio.com/items?itemName=Angular.ng-template):<br />
   This extension provides a rich editing experience <b>for Angular templates</b>, both inline and external templates including <b>completions lists, AOT diagnostic messages, quick info and go to definition</b><br />
   * [Angular Snippets](https://marketplace.visualstudio.com/items?itemName=johnpapa.Angular2):<br />
   This extension adds <b>snippets for Angular for TypeScript, HTML and NgRx</b>. This will help you save a lot of time while developing applications. Just type part of a snippet, press enter, and the snippet unfolds! [Angular 8 Snippets](https://marketplace.visualstudio.com/items?itemName=Mikael.Angular-BeastCode) is also another similar, honorable mention.
   * [Angular Schematics](https://marketplace.visualstudio.com/items?itemName=cyrilletuzi.angular-schematics):<br />
   This extension allows you to <b>generate Angular schematics with a Graphical User Interface</b>. This extension promote Angular good practices, by improving component generation with the suggestion of different component types. Use this extension to <b>quickly generate component, module, service</b> etc. [Angular Files](https://marketplace.visualstudio.com/items?itemName=alexiv.vscode-angular2-files) is also another similar, honorable mention.
   * [Prettier - Code formatter](https://marketplace.visualstudio.com/items?itemName=esbenp.prettier-vscode):<br />
   Prettier is an opinionated <b>code formatter</b>. It enforces a consistent style by parsing your code and re-printing it with its own rules that take the maximum line length into account, wrapping code when necessary.<br />
   * [GitLens — Git supercharged](https://marketplace.visualstudio.com/items?itemName=eamodio.gitlens):<br />
   GitLens supercharges the Git capabilities built into Visual Studio Code. It helps you to <b>visualize code authorship</b> at a glance via Git blame annotations and code lens, seamlessly <b>navigate and explore Git repositories</b>, gain valuable <b>insights via powerful comparison commands</b>, and so much more.
   
   
2. <img src="images/webstorm.svg" alt="WebStorm" width="30" height="30" vertical-align="middle"> &nbsp; <b>[WebStorm](https://www.jetbrains.com/webstorm/)</b><br />
 One of the smartest and most powerful IDE's for developing Javascript applications available out there. WebStorm by IntelliJ is a highly recommended pick for developing Angular applications with built-in <b>support for TypeScript</b> out of the box. WebStorm comes with <b>intelligent code completion, on-the-fly error detection, powerful navigation and refactoring for Typescript and stylesheet languages</b>. WebStorm is fully packed with a variety of <b>built-in developer tools</b> and various other features and thus saves your time juggling multiple plugins for seamless development. Below is a list of few WebStorm plugins that are useful while developing Angular applications. <br />
   * [Angular and AngularJS](https://plugins.jetbrains.com/plugin/6971-angular-and-angularjs):<br />
  This all-in-one framework integration plugin packs tons of features such as: <b>code completion</b> for components, built-in and custom directives, and methods in both templates and ts files; <b>navigation</b> from the component, custom directives and event handlers to their definition; <b>code snippets</b> and <b>Angular CLI integration</b>.<br />
   * [Prettier](https://plugins.jetbrains.com/plugin/10456-prettier):<br />
   This plugin adds support for Prettier, an opinionated <b>code formatter</b>. It enforces a consistent style by parsing your code and re-printing it with its own rules that take the maximum line length into account, wrapping code when necessary.<br />
   * [GitToolBox](https://plugins.jetbrains.com/plugin/7499-gittoolbox):<br />
   This plugin <b>extends Git Integration</b> with additional features such as <b>status display, auto fetch, inline blame annotation, commit dialog completion, behind notifications</b> and more.  
 
 <br />
   
 >Do check out the [Angular IDE](https://www.genuitec.com/products/angular-ide/) by Codemix, which is a dedicated, powerful IDE for Angular.
 
 </details>  
   
 <br />
   
| :heart: _Takeaway_ : Use your favorite IDE ([Visual Studio Code](https://code.visualstudio.com/) or [WebStorm](https://www.jetbrains.com/webstorm/) recommended) along with awesome plugins for a smooth development experience. |
| :--- |

<br />

🔝 [Back to Contents](#bookmark_tabs-table-of-contents)

<br />
  
<!-- STARTER KITS -->
## `🎉 Using Starter Kits`
<details>
  <summary>Click to expand</summary>
  
There is no doubt that the Angular CLI's `ng new` command generates a decent base app to kick-start your project. But sometimes, we want more. Angular starter kits/boilerplates will heavily **reduce the development time for initial setups** - from basic recommended folder structure to interceptors and guards, these seeds have many features readily available. Below are some of the most used and well maintained Angular starter kits:

1. [Angular, NgRx and Angular Material Starter](https://github.com/tomastrajan/angular-ngrx-material-starter) : As the name suggests, the stack includes **Angular, NgRx, Angular Material and Bootstrap 4**. This starter has a **strong application structure** that is easily scalable and suitable for big projects. It also packs **basic interceptors, error-handlers, auth-guards, ngrx files, Travis CLI etc.** used along with a TODO application example.

2. [ngX Starter Kit](https://github.com/ngx-rocket/starter-kit) : Generated using [ngx-Rocket](https://github.com/ngx-rocket/generator-ngx-rocket), this starter kit includes **modern tools** and workflow based on angular-cli, **best practices** from the community, a **scalable base template** and a good learning base. This starter kit comes pre-equipped with **Bootstrat 4, Font Awesome, RxJS, ng-bootstrap, ngx-translate and Lodash**. The starter also includes a basic **login screen, interceptors, guards etc.

3. [ngx-admin](https://akveo.github.io/ngx-admin/) : One of the most widely used Angular **admin dashboard template** based on **Angular 9+, Bootstrap 4+ and Nebular**. This template packs all the features and more that you will need for an admin dashboard template.

</details>

<br />
   
| :heart: _Takeaway_ : Use starters/boilerplates to save initial setup time and for a smooth start. |
| --- |

<br />

🔝 [Back to Contents](#bookmark_tabs-table-of-contents)

<br />

## `❄️ Commit Guidelines`
 <details>
  <summary>Click to expand</summary>

Usually developers tend to add some random commit messages which doesn't actually add any value to the project. By using some precise rules over how the commit messages are formatted can lead to more readable messages that are easy to follow when looking through the project history. We can even generate changelogs from such commit messages :astonished:! It's recommended to follow the commit guidelines from the [official Angular repo](https://github.com/angular/angular/blob/22b96b9/CONTRIBUTING.md#-commit-message-guidelines).<br />
* Each commit message consists of a **header**, a **body**, and a **footer (optional)**. The header has a special format that includes a type, and a subject: <br />
  ```
  <type>: <subject>
  <BLANK LINE>
  <body>
  <BLANK LINE>
  <footer>
  ```
* The `type` can be any of the following:<br />
  - **docs**: Documentation only changes
  - **feat**: A new feature
  - **fix**: A bug fix
  - **perf**: A code change that improves performance
  - **refactor**: A code change that neither fixes a bug nor adds a feature
  - **test**: Adding missing tests or correcting existing tests

* The `footer` should contain a closing reference issue if any.

<br />

Eg:
```
fix: no password validations

length and pattern validations for password

PR Close #11721
```
<br />

> :bulb: **_Tip_** : Use [Conventional Changelog](https://github.com/conventional-changelog/conventional-changelog) or it’s [standard version](https://github.com/conventional-changelog/standard-version) to generate changelogs and release notes from project's commit messages and metadata with this commit guideline.

</details>

<br />
   
| :heart: _Takeaway_ : It's recommended to follow the commit guidelines of the [official Angular repo](https://github.com/angular/angular/blob/22b96b9/CONTRIBUTING.md#-commit-message-guidelines); consisting of a header, a body, and a footer (optional). Use these commits for generating changelogs. |
| :--- |

<br />

🔝 [Back to Contents](#bookmark_tabs-table-of-contents)

<br />

<!-- CONFIGURING -->
## `👷 Configuring Your Project`

<details>
  <summary>Click to expand</summary>
  
  There is no doubt that Angular CLI has covered most of the recommended configurations out of the box for us. But we can still make it better :heart_eyes_cat:!
  
  ### TSLint
  Angular CLI generates a basic set of tslint rules for us for **static code analysis** using [codelyzer](https://github.com/mgechev/codelyzer) by [Minko Gechev](https://github.com/mgechev). Below is the recommended configuration:
  ```js
  {
  // The rules component-selector and directive-selector have the following arguments:
  // [ENABLED, "attribute" | "element", "prefix" | ["listOfPrefixes"], "camelCase" | "kebab-case"]
  "component-selector": [true, "element", ["cmp-prefix1", "cmp-prefix2"], "kebab-case"],
  "directive-selector": [true, "attribute", ["dir-prefix1", "dir-prefix2"], "camelCase"],

  "component-max-inline-declarations": true,
  "contextual-lifecycle": true,
  "no-conflicting-lifecycle": true,
  "no-host-metadata-property": true,
  "no-input-rename": true,
  "no-inputs-metadata-property": true,
  "no-output-native": true,
  "no-output-on-prefix": true,
  "no-output-rename": true,
  "no-outputs-metadata-property": true,
  "no-queries-metadata-property": true,
  "prefer-inline-decorator": true,
  "template-banana-in-box": true,
  "template-no-negated-async": true,
  "use-lifecycle-interface": true,
  "use-pipe-transform-interface": true,

  // The rules component-class-suffix and directive-class-suffix have the following arguments:
  // [ENABLED, "suffix" | ["listOfSuffixes"]]
  // Where "suffix" is/are your custom(s) suffix(es), for instance "Page" for Ionic components.
  "component-class-suffix": [true, "Component"],
  "directive-class-suffix": [true, "Directive"]
}
```

<br />

> :bulb: **_Tips_** : Want to add more rules on top of the Angular CLI configuration? It's highly recommended to use the [Angular TSLint Preset](https://github.com/mgechev/tslint-angular) by [Minko Gechev](https://github.com/mgechev).<br />
It's highly recommended to use [Husky 🐶](https://github.com/typicode/husky) to check for lint issues on a git commit hook and avoid bad commit/push.

<br />

### Prettier
The **opinionated code formatter**, prettifies our code to look even more beautiful :heart_eyes:. First step is to install the Prettier plugin in your favorite IDE (go to [Choosing IDE](#sunglasses-choosing-ide)) or `npm install prettier` to make your team members reference the same configuration file regardless of the IDE. Don't forget to set the _format on save_ option in your IDE.

```js
// For VS Code
“editor.formatOnSave”: true
```
Great :clap:! But, how will the prettier and tslint work together? It’s simple, we can **leave the code-quality rules for TSLint** to handle, and we can have **Prettier take care of formatting rules** by removing formatting rules from tslint.json.

<br />

> :gift: **_Resources_** : Check out [Setting up Prettier in an Angular CLI Project](https://medium.com/@victormejia/setting-up-prettier-in-an-angular-cli-project-2f50c3b9a537) by [Victor Mejia](https://medium.com/@victormejia).

<br />

> :bulb: **_Tip_** : Use [tslint-config-prettier](https://github.com/prettier/tslint-config-prettier) to use TSLint and Prettier without conflicts.

 <br />
 
 ### Aliasing Folders
 You might have come across some import statements in codes which is way too long and dirty, like this ```import { RandomService } from '../../../../core/services/random.service'``` :dizzy_face:. To avaoid such situations, we can use aliases for folder paths **making the imports cleaner, readable and consistent**. So, how will we do this? Head to the `tsconfig.json` in your project root and add aliases to the `paths` property:
 
 ```json
 "paths": {
      "@app/*": ["./src/app/*"],
      "@shared/*": ["./src/app/shared/*"],
      "@core/*": ["./src/app/core/*"],
      "@env/*": ["environments/*"]
    }
```
Awesome :sunglasses:! Now we can import with more cleaner statements like : 
```js
import { RandomService } from '@core/services/random.service'
```
 <br />
 
 Ok, but hold on, what about imports for style processors like scss? Angular have a solution for that as well :beers:. Head on to `angular.json` and add a property to the `options` property (the property inside which you add additional scripts/styles).
 
 ```json
 "stylePreprocessorOptions": {
		"includePaths": [
			"src/theme/"
		]
	}
 ```
 
 (:page_with_curl: Note that we have included the path in assumption that scss files are inside `theme` folder) Cool :snowman:! Now we can import like :
 
 ```css
 @import "variables";
 ```
 <br />
 
 > :gift: **_Resources_** : <br />
 	1. Check out [6 Best Practices & Pro Tips when using Angular CLI](https://medium.com/@tomastrajan/6-best-practices-pro-tips-for-angular-cli-better-developer-experience-7b328bc9db81) by [@tomastrajan](https://medium.com/@tomastrajan). <br />
 	2. Check out [Angular - Shortcut to Importing Styles Files in Components](https://scotch.io/tutorials/angular-shortcut-to-importing-styles-files-in-components) on [scotch.io](https://scotch.io/)
 
 </details>

<br />
   
| :heart: _Takeaway_ : Setup tslint for code quality rules and Prettier for code formatting rules and use pre-commit hooks to check for lint issues. Add aliases for folders to remove relative paths in import statements. |
| :--- |

<br />

🔝 [Back to Contents](#bookmark_tabs-table-of-contents)

<br />

<!-- FOLDER STRUCTURE -->
## `📚 Folder Structure`

<details>
  <summary>Click to expand</summary>
  
  Finding a scalable and clean folder structure architecture is always hard. Without a proper architecture, you will end up having a really clumsy and hard to maintain piece of codes :worried:. There are several blogs/repos which specifies a proper architecture for Angular applications, and each one is a bit different. This section is just a suggestion for architecting a proper folder structure; so just take away the main points and choose a suitable one for yourself (blogs and repos attached in `resources` at the end of this section). **A good guideline to follow is to split our application into at least three different modules — Core, Shared and Feature.** Okay, let's dive into it one by one :dolphin:.
	
### Core Module
Ideally, the `CoreModule` contains files that are singleton, that is, those files which we only need to load at run-time. The module can contain **singleton services, core components, guards, interceptors, constants, enums and core models**. The core module should be imported only once, which is inside `AppModule`.

```
|-- 📁 core
|      |-- 📁 components
|      |      |-- 📁 shells
|      |      |-- 📁 header
|      |      |-- 📁 page-not-found
|      |      ...
|      |-- 📁 guards
|      |      |-- 📄 auth.guard.ts
|      |      ...
|      |-- 📁 interceptors
|      |      |-- 📄 api-prefix.interceptor.ts
|      |      |-- 📄 error-handler.interceptor.ts
|      |      ...
|      |-- 📁 services
|      |      |-- 📄 utility.service.ts
|      |      |-- 📄 authentication.service.ts
|      |      ...
|      |-- 📁 enums
|      |-- 📁 models
|      |-- 📁 constants
|      |-- 📄 core.module.ts
|      |-- 📄 ensureModuleLoadedOnceGuard.ts
|      |-- 📄 logger.service.ts
```
<br />

> :bulb: **_Tips_** : Add a check in the `CoreModule` constructor and throw an error if already loaded or add a guard for the same to avoid accidental imports (refer [here](https://github.com/ngx-rocket/starter-kit/blob/master/src/app/%40core/core.module.ts)) .<br />
Add a logger system in `logger.service.ts` file (refer [here](https://github.com/ngx-rocket/starter-kit/blob/master/src/app/%40core/logger.service.ts)).

<br />

### Shared Module
`SharedModule` is the module where all our **shared or _dumb components_, directives and pipes** go. We can also **add any third-party components/directives/pipes** (like [Angular Material](https://material.angular.io/) components) which will be needed throughout our application, to the `imports` and `exports` of the module. This module can be then imported to each _feature module_.

```
|-- 📁 shared
|      |-- 📁 components
|      |      |-- 📁 loader
|      |      |-- 📁 confirmation-dialog
|      |      ...
|      |-- 📁 directives
|      |      |-- 📄 drag-drop.directive.ts
|      |      |-- 📄 scroll-spy.directive.ts
|      |      ...
|      |-- 📁 pipes
|      |      |-- 📄 custom-date.pipe.ts
|      |      |-- 📄 safe.pipe.ts
|      |      ...
|      |-- 📁 models
|      |      |-- 📄 user.ts
|      |      |-- 📄 api-response.ts
|      |-- 📄 shared.module.ts
```
<br />

> :page_with_curl: **_Note_** : Don't forget to add the components, directives and pipes to the `exports` inside `shared.module.ts`.

<br />

### Feature Modules
It's recommended to create feature modules **for every independent feature** of our application. Ideally, **feature modules shouldn't be dependant on other modules other than the services provided by CoreModule and features exported by SharedModule**. A feature module directory can contain `components`, `pages`, `services` etc. that is specific to the corresponding feature.
<br /><br />
The `pages` folder contains higher level components or even lazy loaded modules. We can refer to a `page` as the parent component which contains several other child components which ultimately makes up a _page_. The `components` folder contains components which are consumed by various `pages` of the corresponding feature.

```
|-- 📁 modules
|      |-- 📁 home
|      |      |-- 📁 components
|      |      |      |-- 📁 table
|      |      |      ...
|      |      |-- 📁 pages
|      |      |      |-- 📁 home
|      |      |      |-- 📁 details
|      |      |      ...
|      |      ...
|      |      |-- 📄 home-routing.module.ts
|      |      |-- 📄 home.module.ts
|      |-- 📁 users
|      |      |-- 📁 components
|      |      |-- 📁 pages
|      |      ...
|      |      |-- 📄 users-routing.module.ts
|      |      |-- 📄 users.module.ts
```

<br />

### Styling
It's preferred  to add a `theme` folder inside `src` to include custom themes and scss variables.

```
|-- 📁 theme
|      |-- 📁 partials
|      |-- 📄 variables.scss
|      |      ...
|      |-- 📄 theme.scss
```
Now we can import the `theme.scss` in our main `styles.scss` where we add global styles and import other style files.

</details>

<br />

> :gift: **_Resources_** : <br />
 	1. Check out [Choosing The Right File Structure for Angular in 2020 and Beyond 📕!](https://itnext.io/choosing-the-right-file-structure-for-angular-in-2020-and-beyond-a53a71f7eb05) by [Mathis Garberg](https://itnext.io/@mathis.garberg). <br />
 	2. Check out [How to architect epic Angular app in less than 10 minutes! ⏱️😅](https://medium.com/@tomastrajan/how-to-build-epic-angular-app-with-clean-architecture-91640ed1656) by [Tomas Trajan](https://medium.com/@tomastrajan). <br />
	3. Check out [Angular Folder Structure](https://medium.com/@motcowley/angular-folder-structure-d1809be95542) by [Tom Cowley](https://medium.com/@motcowley). <br />
	4. Check out the excellent folder structure in these [starter kits](#tada-using-starter-kits).
	
<br />

| :heart: _Takeaway_ : Split our application into at least three different modules — Core, Shared and Feature; below is the bigger picture 🖼️ : |
| :--- |

```
src/                         
|-- 📁 app                   
|      |-- 📁 core            	    core module (singleton services, single-use components, interceptors, guards etc.)
|      |-- 📁 shared          	    shared module  (common components, directives and pipes)
|      |-- 📁 modules         	    feature modules (each containing pages, components, services etc.)
|      |-- 📄 app.component.*
|      |-- 📄 app.module.ts          
|      |-- 📄 app-routing.module.ts  
|      +- ...
|-- 📁 assets
|-- 📁 environments
|-- 📁 theme                  	    app global scss variables, partials and theme
|-- 📁 translations/                translations files
|-- 📄 index.html
+- ...
|-- 📄 main.ts
```

<br />

🔝 [Back to Contents](#bookmark_tabs-table-of-contents)

<br />

## `⚡ Performance Cheatsheet`
<details open>
  <summary>Click to expand</summary>

It's a known fact that Angular is a highly performant framework. But we can make it better by following some best practices. Let's jump in to the list of such best practices :nerd_face: :

### 1. Avoid function calls in templates.
<details>
  <summary>Click to expand</summary>

It is not a good practice to write function calls for computing values inside the templates. And if it's a complex function, a big NO :skull:.

```html
<tr *ngFor="let book of books">{{calculatePrice(book)}}</tr> ❌
```

#### Why?
Angular will run your function in each of it's change detection cycle (which is quite frequent) and if the function is a complex one, this will impose a serious effect on the performance.

#### Solution:
There may be some cases where this is unavoidable, but for most cases this can be avoided by:
1. **Creating a property in the ts file and setting the value to it once.**

	```js
	this.books = this.books.map(book => ( { ...books, price: calculatePrice(book)  } );
	```
2. **Using pure pipes** : A pure pipe is a pipe that will always always return the same output for an input. Angular executes a pure pipe only when it detects a pure change to the input value because it already knows that the pipe will return the same value for the same input.

	```js
	@Pipe({
		name: 'dummy',
		pure: true
	})
	export class somePipe implements PipeTransform {
		transform(value: any, args?: any): any {
			 // logic
		}
	}
	```
	
	> :gift: **_Resources_** : Check out [The essential difference between pure and impure pipes in Angular and why that matters](https://indepth.dev/the-essential-difference-between-pure-and-impure-pipes-in-angular-and-why-that-matters/) by [Max Koretskyi
](https://indepth.dev/author/maxkoretskyi/)

</details>

### 2. Use trackBy with ngFor
<details>
  <summary>Click to expand</summary>

When using `*ngFor` to loop over an array which might change over time, it is recommended to use `trackBy` **to track array items with unique identifier**.

#### Why?
When an array changes (eg: when we push a new item to array), Angular will remove all the DOM elements associated with that array and create all of it again. This is because Angular has no knowledge of which items have been removed or added.

#### Solution:
Use `trackBy`. If we provide a `trackBy` function, Angular can track which items have been added or removed in the array according to the unique identifier. It then has to create or destroy the DOM elements for only those items that have changed. Cool :gem:! Now, this is how we dot it:

```html
<tr *ngFor="let book of books; trackBy: trackByFn"">{{book.name}}</tr>
```

and then in your `component.ts`:

```js
trackByFn(index: number, book: Book) {
    return item.id;
}
```
<br />

> :gift: **_Resources_** : Check out [Angular — Improve Performance with trackBy](https://netbasal.com/angular-2-improve-performance-with-trackby-cc147b5104e5) by [Netanel Basal](https://netbasal.com/@NetanelBasal)

</details>

### 3. Use tree-shakable providers
<details>
  <summary>Click to expand</summary>

Make your services **tree-shakable by using the `providedIn` attribute** of the `@Injectable()` decorator instead of explicitely specifying in the `providers` attribute of a module/component :palm_tree:.

#### Why?
If your service is tree-shakable, Angular can exclude the code in the final build bundle provided that it's not used anywhere. This can help reduce the overall bundle size :tada:.

#### Solution:
By default, value for `providedIn` is `root`. This will provide your service at the root injector level and can be injected anywhere in your application. Angular 9+ comes with a couple of other options as well:

1. `platform` - The use case comes when you are running multiple [angular elements (web components)](https://angular.io/guide/elements) in a single page. Your service will now become a global singleton at the platform-level, and is shared between all of the Angular applications on your page.
2. `any` - Angular will provide a unique instance of your service for every module that injects it.

```js
import { Injectable } from '@angular/core';

@Injectable({  
   providedIn: 'root' // or 'any' or 'platform'
})
export class SomeService { 
}
```

<br />

> :gift: **_Resources_** : Check out [Dependency injection with Angular 9](https://blog.angulartraining.com/dependency-injection-with-angular-9-63ce524496d9) by [Alain Chautard](https://blog.angulartraining.com/@angulartraining)

</details>

### 4. Unsubscribe observables
<details>
  <summary>Click to expand</summary>

When you subscribe to observables, make sure to unsubscribe them in the `ngOnDestroy` method :eyes:.

#### Why?
If you fail to unsubscribe your observables, chances are there that **memory leaks** might happen since your observable stream is left open even after that component is destroyed. This will lead to uexpected behaviours and serious performance issues :scream:.

#### Solution:
There are various ways to unsubscribe observables:
1. We can make use of `takeUntil` to listen to the changes until another observable emits a value.
	```js
	private _destroy$ = new Subject();

	public ngOnInit(): void {
	  sampleObservable$
	  .pipe(
	    // listen to the observable until this._destroy$ emits a value
	    takeUntil(this._destroy$)
	  )
	  .subscribe(item => // logic);
	}

	public ngOnDestroy(): void {
	  this._destroyed$.next();
	  this._destroyed$.complete();
	}
	```
2. If you need to subscribe to an observable only once, use `take(1)`. 📄 Note that you will need to use `takeUntil` to avoid any  memory leaks caused when the subscription hasn’t received a value before the component got destroyed.
	```js
	sampleObservable$
	.pipe(
	  take(1),
	  takeUntil(this._destroy$)
	)
	.subscribe(item => // logic);
	```

3. Using `unsubscribe()` method of `Subscription`. Using this method, you have to `add()` your observables (if you have multiple :train:) to the `Subscription` and destroy on `ngOnDestroy` with the `unsubscribe()` method.

	```js
	private _subscriptions$ = new Subscription();

	public ngOnInit (): void {
	  // we can add multiple observables to _subscriptions$ with add()
	  this._subscriptions$.add(
	    sampleObservable1$
	    .subscribe(item => // logic)
	  );
	}

	public ngOnDestroy (): void {
	  this._subscriptions$.unsubscribe();
	}
	```
	
<br />

> :bulb: **_Tip_** : Make use of lint rules to detect any unsubscribed observables. Check out [rxjs-tslint](https://github.com/ReactiveX/rxjs-tslint) for TSLint rules targeting RxJS.

<br />

> :gift: **_Resources_** : Check out [6 Ways to Unsubscribe from Observables in Angular](https://blog.bitsrc.io/6-ways-to-unsubscribe-from-observables-in-angular-ab912819a78f) by [Chidume Nnamdi](https://blog.bitsrc.io/@kurtwanger40)

</details>

### 5. Use async pipe
<details>
  <summary>Click to expand</summary>

In the previous section, we learnt about unsubscribing observables. But there is a much more efficient way for the same problem, the magical `async` pipe :dizzy:. It's recommended to avoid subscribing to observables from components and instead subscribe to the observables from the template.

#### Why?
Because subscriptions can lead to memory leaks if not properly unsubscribed and it's an additional overhead to do so :weary:.

#### Solution:
Fear not! Angular have a magic potion up the sleeves just for **automatically managing subscriptions** - `async` pipe :crystal_ball:. Yes, it magically handles the subscriptions for us; no more memory leaks by forgetting to unsubscribe observables :smirk:. Use it whenever it's possible to.

```html
<p>{{ someObservable$ | async }}</p>

<p>{{ (someOtherObservable$ | async).value }}</p>
```

</details>

### 6. Lazy load modules
<details>
  <summary>Click to expand</summary>

Lazy loading is said to be one of the most powerfull feature of Angular. It's recommended to **lazy load your feature modules whenever it's possible to.**

#### Why?
By default, webpack (the default bundler of Angular), bundles all your code into one large bundle. This will largely increase the initial rendering time since the browser has to downlaod that one single large file initially itself, leading to a bad user experience :rage:.

#### Solution:
Angular offers a powefull solution to that problem. **Split your code to separate bundles and load them on demand :muscle:.** And we do that via 'lazy loading'. This will **reduce the initial rendering time** since the browser has to download only a small file that contains the code for just your initial page. The browser will be fed the other files on-demand, i.e, when the user needs it (by navigating to a certain page).

```js
// Note that the below syntax is valid for Angular 8 and above. 
{ path: 'home',  loadChildren: () => import('./home.module').then(module => module.HomeModule) }
```

> :page_facing_up: **_Note_** : **Do not lazy load the default route**, as the browser will have to download an extra lazy loaded chunk after downloading the main chunk and parse it. This will slow down the initial rendering time.

</details>

### 7. Use preloading strategy
<details>
  <summary>Click to expand</summary>

Preloading strategy is a concept which can be used along with lazy loading to make our application much more faster. You can use Angular's default `PreloadAllModules` strategy, or you can even write your own cutom strategies depending upon the requirements :truck:.

#### Why
When we lazy load a module, there is a possible latency since the browser loads the lazy loaded chunk and parse it only when we navigate to that module. This will lead to a bad user experience since the user might be required to wait for sometime until the page gets loaded :construction:.

#### Solution:
Use preloading strategy to **load lazy loaded modules in the background after all the eager loaded modules are ready**. This eliminates the possible latency when navigating to a lazy loaded module, but still has the benefit of faster initial loading of the app because the initial module(s) get loaded first. Such a cool feature :snowflake:! We can do that in various ways:

1. **PreloadAllModules** : This is the default preloading strategy of Angular. This will load all the lazy loaded modules in the background once all the eager loaded modules are ready.
	```js
	imports: [
	  ...
	  RouterModule.forRoot(routes, { preloadingStrategy: PreloadAllModules })
	],
	```
	
2. **Custom strategy** : We may not always want to preload all the modules. Some modules might be a less used module which we don't wan't to preload. Or you may want to preload the modules based on some conditions, say, by checking user's bandwidth. We can write a custom preloading strategy for that :heart_eyes_cat:.
	```js
	import { Observable } from 'rxjs/Observable';
	import { PreloadingStrategy, Route } from '@angular/router';

	export class CustomPreloadStrategy implements PreloadingStrategy {
	  preload(route: Route, preload: Function): Observable<any> {
	    if (someCondition) {
	      return preload();
	    }	
	    return Observable.of(null);
	  }
	}
	```
	
	And in the `AppModule`:
	
	```js
	imports: [
	  ...
	  RouterModule.forRoot(routes, { preloadingStrategy: CustomPreloadStrategy })
	],
	```
	
<br />

> :bulb: **_Tips_** : It's highly recommended to use [ngx-quicklink](https://github.com/mgechev/ngx-quicklink) by [Minko Gechev](https://github.com/mgechev) which automatically downloads the lazy-loaded modules associated with all the visible links on the screen using [Intersection Observer](https://developer.mozilla.org/en-US/docs/Web/API/Intersection_Observer_API). It also checks if the user isn't on a slow connection before preloading :fire:. <br />
Or, make use of machine learning by predictively preloading modules with [Guess.js](https://github.com/guess-js/guess) :crystal_ball:.

<br />

> :gift: **_Resources_** : <br />
 	1. Check out [Preloading in Angular](https://alligator.io/angular/preloading/) on [alligator.io](https://alligator.io/). <br />
 	2. Check out [Route preloading strategies in Angular](https://web.dev/route-preloading-in-angular/) by [Minko Gechev](https://web.dev/authors/mgechev/).
	
</details>

### 8. Lazy load components

> :page_facing_up: **_Note_** : This feature is only supported in Angular 9+.

<details>
  <summary>Click to expand</summary>

Yes, it's also possible to lazy load components or modules without a route with Angular's Ivy engine :fire:. We can use this awesome feature to reduce the load/rendering time again!

#### Why?
Sometimes, you might have some components that are rarely used, say, an info popup that the users use very rarely. Pre loading the code for such components doesn't make any sense. If we can remove such components and load only those components that are necessary for the initial rendering, there will be a considerable gain in the rendering speed :zap:.

#### Solution:
Let's check out how to lazy load components through the below steps :

1. First step is to create a container element for the component to be rendered in and get hold of that container in component using `@ViewChild`.

	```html
	<ng-container #someContainer></ng-container>
	```
	In your component:
	
	```js
	@ViewChild('someContainer', {read: ViewContainerRef}) someContainer: ViewContainerRef;
	```
	
2. Use `ComponentFactoryResolver` and `Injector` to create an instance of the component.

	```js
	constructor(
	  private injector: Injector,
	  private cfr: ComponentFactoryResolver
	) {}
	```
	
3. Use async-await to lazy load the component.

	```js
	async lazyLoadComponent() {
	  const { LazyComponent } = await import('./lazy.component');
	  const componentFactory = this.cfr.resolveComponentFactory(LazyComponent);
	  const { instance } = this.someContainer.createComponent(componentFactory, null, this.injector);
		
	  // Use the instance to pass down values to LazyComponent like this:
	  instance.someProperty = 'dummy property';
		
	  // Get hold of emitted values from LazyComponent:
	  instance.someEmitter.pipe(
	    takeUntil(instance.destroy$)
	  ).subscribe(() => // Do something);
	}
	```
	
4. Sometimes you will need to import other modules (like `SharedModule`) to include some features in your component. We can create a dedicated module for the lazy loaded component and add it to the `lazy.component.ts` file.

	```js
	@NgModule({
	  declarations: [ LazyComponent ],
	  imports: [ CommonModule, SharedModule ]
	})
	
	// Remove export statement to avoid accidental imports in other files.
	class LazyCompModule {
	}
	```
	
<br />

> :gift: **_Resources_** : <br />
 	1. Check out [Angular 9: Lazy Loading Components](https://johnpapa.net/angular-9-lazy-loading-components/) by [John Papa](https://github.com/johnpapa). <br />
 	2. Check out [Lazy load Angular components](https://medium.com/angular-in-depth/lazy-load-components-in-angular-596357ab05d8) by [Kevin Kreuzer](https://medium.com/@kevinkreuzer).
	
</details>

### 9. Use ChangeDetectionStrategy.OnPush
<details>
  <summary>Click to expand</summary>

Angular gives us an option to choose the `ChangeDetectionStrategy` of a component. By default, the value is `Default`. It's recommended to change that to `OnPush` strategy to maximise the performance :ok_hand:.

#### Why?
By default, Angular run its change detection cycle on all the components whenever there occurs some changes, like a simple click event or when we recieve data from ajax calls. Running change detection cycle on every such events are costly and may affect the performance when the app grows.

#### Solution:
We can minimize these checks by setting our component's `changeDetection` to `ChangeDetectionStrategy.OnPush`. This will tell Angular to run change detection cycle only when:

1. The `Input` reference changes.
2. Some event occurs in the component or any of the children.

```js
@Component({
  selector: 'app-selector',
  ...
  changeDetection: ChangeDetectionStrategy.OnPush
})
```
<br />

> :page_facing_up: **_Note_** : Make use of `detectChanges()` or `markForCheck()` functions of `ChangeDetectorRef` to explicitely run the change detection cycle if required.

<br />

> :gift: **_Resources_** : Check out [🚀 A Comprehensive Guide to Angular onPush Change Detection Strategy](https://netbasal.com/a-comprehensive-guide-to-angular-onpush-change-detection-strategy-5bac493074a4) by [Netanel Basal](https://netbasal.com/@NetanelBasal).

</details>

### 10. Disable change detection
<details>
  <summary>Click to expand</summary>

It is recommended to detach and reattach the change detector whenever required, for components where data changes happen frequently :wrench:.

#### Why?
Running change detection cycle frequently when data changes occur constantly is very costly and can lead to performance issues :small_red_triangle_down:.

#### Solution:
Use the `detach()` method of `ChangeDetectorRef` to detach the change detector so that Angular won't run any change detection cycle unless you explicitely says to, by calling `reattach()` or `detectChanges()`. The `reattach()` method can be used to re attacch the change detector when some frequent complex calculations have been finished. The `detectChanges()` can be used to detect the changes once, whenever required.

```js
constructor(private cdRef: ChangeDetectorRef) {
  cdRef.detach();
  
  // to check and update view every 5sec for a frequently changing component
  // or use this.cdRef.reattach() when frequent complex calculations have been finished
  setInterval(() => {
    this.cdRef.detectChanges();
  }, 5000);
}
```

<br />

> :gift: **_Resources_** : Check out [Everything you need to know about change detection in Angular](https://indepth.dev/everything-you-need-to-know-about-change-detection-in-angular/) by [Max Koretskyi](https://indepth.dev/author/maxkoretskyi/).

</details>

### 11. Run outside angular
<details>
  <summary>Click to expand</summary>

Angular make use of `NgZone`, which is a wrapper for `Zone` APIs, to detect when to run change detection cycle. Zones wrap asynchronous browser APIs, and notifies when an asynchronous task has started or ended. Angular takes advantage of these APIs to get notified when any asynchronous task like xhr calls or any user events is done to run it's change detection mechanism :angel:. So it is recommended to use the `runOutsideAngular` method of the `NgZone` instance to minimize running change detection cycles.

#### Why?
For the same reason in the above section - running change detection cycle frequently when data changes occur constantly is very costly and can lead to performance issues :small_red_triangle_down:.

#### Solution:
We can run complex functions that don't necessarily require a change detection cycle to run (inorder to reflect something in the view) inside the callback of `runOutsideAngular()`.

```js
constructor(private zone: NgZone) {
}

someComplexFunction() {
  this.zone.runOutsideAngular(() => {
    // your complex logic
  });
}
```
<br />

> :page_facing_up: **_Note_** : Make use of `run()` method to explicitely run the change detection cycle if required.

<br />

> :gift: **_Resources_** : Check out [Using Zones in Angular for better performance](https://blog.thoughtram.io/angular/2017/02/21/using-zones-in-angular-for-better-performance.html) by [Pascal Precht](https://twitter.com/PascalPrecht).

</details>

### Other performance optimisation techniques
<details>
  <summary>Click to expand</summary>

#### 1. Add API caching mechanisms
While most of the time it is, not all the API responses are dynamic. Sometimes some of the responses do not change often. We can store those values from the API by adding a caching mechanism and return that when subsequent calls to that APIs are made. In this way we can reduce the ajax calls and significantly improve the speed of our application as we don't have to wait for the network.

<br />

> :bulb: **_Tip_** : Use [cashew](https://github.com/ngneat/cashew) 🐿, an awesome, flexible library that caches HTTP requests in Angular. Caching is nut a problem anymore :wink:!

<br />

#### 2. Use service workers
Make use of service workers to cache our static assets(images, icons and fonts) and build artifacts(JS and CSS bundles). This can significantly improve the rendering time and make our application lightning fast :zap: by reducing the number of network requests needed. You can even make your application work when offline serving from the saved cache :beers:!

<br /> 

We can make our application a Progressive Web App (PWA), by adding `@angular/pwa` package. Play with the generated `ngsw-config.json` to to define what and how to cache. With this feature, we can add our web application to our mobile phone's home screen and make our web app to look and feel like a native mobile application by adding application icons, splash screens etc. We can even release the application in Google Playstore just like any mobile application with [Trusted Web Activity](https://developers.google.com/web/android/trusted-web-activity) :scream: :scream:!

<br />

> :gift: **_Resources_** : <br />
	1. Check out [Getting started with service workers](https://angular.io/guide/service-worker-getting-started) in the official Angular docs. <br />
	2. Check out [Angular Service Worker - Step-By-Step Guide for turning your Application into a PWA](https://blog.angular-university.io/angular-service-worker/) on [Angular University](https://blog.angular-university.io/). <br />
	3. Check out [How to build Progressive Web Apps with Angular.](https://scotch.io/tutorials/how-to-build-progressive-web-apps-with-angular) by [Eniola Lucas](https://scotch.io/@enirate).
	
<br />

#### 3. App Shell
We can improve the user experience by quickly launching a static rendered page (a skeleton common to all pages) while the browser downloads the full client version and switches to it automatically after the code loads. This will significantly reduce the time for the first paint since the browser just need to render HTML and CSS without the need for initialize any Javascript. Such a cool feature :hushed:!

<br />

We can make use of the Angular CLI to automatically generate an app shell for us with the command `ng generate app-shell`. Or thinking ahead, we can make use of Angular Universal to pre-render a static app shell :milky_way:. Do check out the resources to know more about it.

<br />

> :gift: **_Resources_** : <br />
	1. Check out [App shell](https://angular.io/guide/app-shell) in the official Angular docs. <br />
	2. Check out [Angular App Shell - Boosting Application Startup Performance](https://blog.angular-university.io/angular-app-shell/) on [Angular University](https://blog.angular-university.io/). 
	
<br />

#### 4. Web Workers
By default, our code usually runs in a single thread. This leaves behind a problem of unresponsive ui if some computationally intensive tasks are being performed. But thanks to Angular's support for web workers, we can run such tasks in another thread in the background without blocking our main execution thread :sun_with_face:. In huge and complex applications, we can even go to an extend where we run our entire application (including change detection) in a Web Worker and leave the main UI thread responsible only for rendering.

<br />

> :gift: **_Resources_** : Check out [Web Workers in Angular](https://angular.io/guide/web-worker) in the official Angular docs.

<br />

#### 5. Web Assembly

> :warning: **_Warning_** : Although most of the modern browsers support web assembly, it's still in a premature state and might be unstable. So use at your own risk :grin:!

If someone wants to go the extra mile for performance, web assembly is for you! So what exactly is web assembly :confused:? In a nutshell, it is a low-level assembly-like language with a size- and load-time-efficient binary format which can run in near native speed. Okay, so what has it got to do with Javascript :no_mouth:? 

WebAssembly is designed to run alongside JavaScript — using the WebAssembly JavaScript APIs, you can load WebAssembly modules into a JavaScript app and share functionality between the two. Meaning, we can write our code in C/C++, Rust etc., compile it into a web assembly module and use it with our Angular application :boom:. In short, we can run our computationally intensive tasks in web assembly and make full use of it's lightning speed :sparkles:!

<br />

> :gift: **_Resources_** : <br />
	1. Check out [Web Assembly](https://developer.mozilla.org/en-US/docs/WebAssembly) in MDN. <br />
	2. Check out [Examples of how to use WebAssembly within Angular](https://github.com/boyanio/angular-wasm) by [Boyan Mihaylov](https://github.com/boyanio). <br />
	3. Check out [Using Web Assembly to speed up your Angular Application](https://malcoded.com/posts/web-assembly-angular/) by [Lukas Marx](https://twitter.com/malcoded).

</details>

<!-- Main details tag close -->
</details>

<br />

> :gift: **_Resources_** : <br />
	1. Do check out this awesome repo : [angular-performance-checklist](https://github.com/mgechev/angular-performance-checklist) by [Minko Gechev](https://github.com/mgechev) and find out more pro performance tips :heart_eyes:. <br />
	2. Check out [Best practices for a clean and performant Angular application](https://www.freecodecamp.org/news/best-practices-for-a-clean-and-performant-angular-application-288e7b39eb6f/) by [Vamsi Vempati](https://twitter.com/_VamsiVempati_). <br />
	3. Check out [Optimizing the Performance of Your Angular Application](https://netbasal.com/optimizing-the-performance-of-your-angular-application-f222f1c16354) by [Netanel Basal](https://netbasal.com/@NetanelBasal).
	4. Check out [15 Angular Performance Tips & Tricks](https://angular-guru.com/blog/angular-performance-tips) on [The Angular Guru](https://angular-guru.com/).
	
<br />

| :heart: _Takeaway_ : |
| :--- |
|	1. Make use of pure pipes to avoid function calls in templates |
|	2. Use `trackBy` with `*ngFor` to minimize DOM manipulations by tracking array items with a unique identifier. |
|	3. Use `providedIn` attribute to make your services tree shakable. |
|	4. Unsubscribe your observables to avoid memory leaks and use async pipe whenever possible to make Angular handle the subscriptions. |
|	5. Lazy load modules and components to separate build bundles and load them on demand. Make use of preloading strategies to avoid possible latency while loading the lazy loaded chunk. |
|	6. Use a combination of `ChangeDetectionStrategy.OnPush`, `ChangeDetectorRef` and `NgZone` methods to minimize the number of change detection cycles. |
|	7. Use service workers, app shell and api caching to further improve the performance. |

<br />

🔝 [Back to Contents](#bookmark_tabs-table-of-contents)

<br />

<!-- ROADMAP -->
## `Roadmap`

See the [open issues](https://github.com/github_username/repo/issues) for a list of proposed features (and known issues).

<br />

<!-- CONTRIBUTING -->
## `Contributing`

Contributions are what make the open source community such an amazing place to be learn, inspire, and create. Any contributions you make are **greatly appreciated**.

1. Fork the Project
2. Create your Feature Branch (`git checkout -b docs/AmazingDoc`)
3. Commit your Changes (`git commit -m 'Add some AmazingDoc'`)
4. Push to the Branch (`git push origin docs/AmazingDoc`)
5. Open a Pull Request

<br />

<!-- LICENSE -->
## `License`

Distributed under the MIT License. See `LICENSE` for more information.



<!-- CONTACT : TODO-->



<!-- ACKNOWLEDGEMENTS : TODO -->
