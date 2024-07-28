<!-- PROJECT LOGO -->
<br />
<p align="center">
  <a href="https://github.com/akhilben/angular-awesome">
    <img src="images/logo.svg" alt="Logo" width="100%">
  </a>

  <p align="center"> <b>
    :star: A curated collection of best practices and valuable tips for building scalable and performant Angular v18+ applications. :star: </b>
    <br />
    <a href="https://github.com/akhilben/angular-awesome/issues">Report Bug</a>
    ·
    <a href="https://github.com/akhilben/angular-awesome/issues">Request Feature</a>
  </p>
</p>

[![GitHub contributors](https://img.shields.io/github/contributors/akhilben/angular-awesome?color=blue&style=for-the-badge)](https://github.com/akhilben/angular-awesome/graphs/contributors) &emsp; [![GitHub](https://img.shields.io/github/license/akhilben/angular-awesome?style=for-the-badge&color=green)](https://github.com/akhilben/angular-awesome/blob/master/LICENSE) &emsp; [![Maintenance](https://img.shields.io/maintenance/yes/2021?color=brightgreen&style=for-the-badge)](https://github.com/akhilben/angular-awesome/graphs/commit-activity) &emsp; [![For](https://img.shields.io/badge/For-Angular-red?style=for-the-badge&logo=angular&color=DD0031)](https://github.com/angular/angular) &emsp; [![Help](https://img.shields.io/badge/-need--help-blueviolet?style=for-the-badge)](#contributing)

<br />

<!-- ABOUT THE PROJECT -->

## `🌟 Preface`

This document serves as a reference handbook for developers of all levels, providing a valuable resource for refreshing memory and improving development skills.

> **_Note_** : The contents of this document are general suggestions sourced from the Angular community on various approaches to problem-solving. It is important to note that there can be multiple solutions to a problem. Consider these suggestions as recommendations and adapt them to suit your specific application.

Now, let's dive in and discover some recommended best practices and tips for building awesome Angular applications 🥳.

<br />

<!-- TABLE OF CONTENTS -->

## `📑 Table of Contents`

- [Preface](#-preface)

- [IDE and Plugins](#-ide-and-plugins)

- [Using Starter Kits](#-using-starter-kits)

- [Git Guidelines](#%EF%B8%8F-commit-guidelines)

- [Configuring Your Project](#-configuring-your-project)

- [Folder Structure](#-folder-structure)

- [Performance Cheatsheet](#-performance-cheatsheet)

  - [Function calls in templates](#1-avoid-function-calls-in-templates)

    - [Use trackBy](#2-use-trackby-with-ngfor)

    - [Tree shakable providers](#3-use-tree-shakable-providers)

    - [Unsubscribe observables](#4-unsubscribe-observables)

  - [Async pipe](#5-use-async-pipe)

    - [Lazy load modules](#6-lazy-load-modules)

    - [Preloading strategy](#7-use-preloading-strategy)

    - [Lazy load components](#8-lazy-load-components)

    - [ChangeDetectionStrategy.OnPush](#9-use-changedetectionstrategyonPush)

    - [Disable change detection](#10-disable-change-detection)

    - [Run outside angular](#11-run-outside-angular)

    - [Other techniques](#other-performance-optimisation-techniques)

- [Contributing](#contributing)

- [License](#license)

<br />

<!-- CHOOSING IDE -->

## `😎 IDE and Plugins`

<details>
  <summary>Click to expand</summary>
  <br />
In today's market, there are numerous powerful IDEs available, both free and paid. Selecting the right IDE is crucial for efficient development, as not all IDEs excel in every language, framework, or library. This chapter is a curated list of awesome plugins/extensions for various IDEs, aimed at enhancing your development experience.

1. <img src="images/code.svg" alt="VS Code" width="30" height="30" vertical-align="middle"> &nbsp; <b>[Visual Studio Code](https://code.visualstudio.com/)</b><br />
   VS Code is a powerful code editor from <b>Microsoft</b> that comes highly recommended for working with Angular. It provides excellent support for <b>TypeScript</b> out of the box, including <b>syntax highlighting</b> and autocomplete with <b>IntelliSense</b>. IntelliSense offers intelligent completions based on variable types, function definitions, and imported modules. Additionally, VS Code is highly customizable with a wide range of extensions, many of which are specifically tailored for Angular development. Below is a list of a few VS Code extensions that are useful for developing Angular applications. <br />

   - [ES Lint](https://marketplace.visualstudio.com/items?itemName=dbaeumer.vscode-eslint):<br />
     ESLint is a popular linter tool for JavaScript and TypeScript that helps <b>catch and fix code errors, enforce coding standards, and improve code quality</b>. The ESLint plugin for VS Code integrates seamlessly with the editor, providing real-time linting feedback as you type. It highlights code issues, offers suggestions for improvements, and supports quick fixes to automatically resolve problems. With the ESLint plugin, you can ensure your code follows best practices and maintain a clean and error-free codebase.

   - [Angular Language Service](https://marketplace.visualstudio.com/items?itemName=Angular.ng-template):<br />
     The Angular Language Service plugin for VS Code is a powerful tool that enhances your Angular development experience. It provides intelligent code editing features specific to Angular, such as <b>auto-completion for Angular templates, navigation to component definitions, and error checking in templates</b>. The plugin also offers advanced refactoring capabilities, making it easier to rename components, extract templates, and more. With the Angular Language Service plugin, you can boost your productivity and write cleaner, more maintainable Angular code.
   - [Angular Snippets](https://marketplace.visualstudio.com/items?itemName=johnpapa.Angular2):<br />
     The Angular Snippets plugin for VS Code is a handy tool that accelerates your Angular development process. It provides a <b>collection of code snippets</b> that you can quickly insert into your codebase, saving you time and reducing the chances of errors. These snippets cover common Angular patterns and syntaxes, and you can easily access and utilize these code shortcuts, boosting your productivity and ensuring consistent code structure across your Angular projects in VS Code.

   - [Angular Schematics](https://marketplace.visualstudio.com/items?itemName=cyrilletuzi.angular-schematics):<br />
     The Angular Schematics plugin for VS Code is a valuable tool for streamlining your Angular development workflow. Schematics are code generators that automate repetitive tasks, such as creating components, services, pipes etc. With the Angular Schematics plugin, you can easily <b>generate code snippets and scaffolding</b> for Angular projects directly from the editor. It provides a convenient user interface for selecting options and configuring generated code. By leveraging the power of Angular Schematics, you can save time and effort when building Angular applications in VS Code.

   - [Prettier - Code formatter](https://marketplace.visualstudio.com/items?itemName=esbenp.prettier-vscode):<br />
     The Prettier plugin for VS Code is an essential tool for <b>code formatting</b> and consistency. Prettier automatically analyzes and formats your code to ensure a consistent and professional style, saving you time and effort. The Prettier plugin seamlessly integrates with VS Code, providing real-time formatting as you type, or you can format the entire file with a single command. With the Prettier plugin, you can easily maintain a clean and standardized codebase, enhancing readability and collaboration in your projects.

     > 💡 **_Tip_** : Set Prettier as your default formatter by navigating to Settings of VS Code and type `Default Formatter` and set `Prettier - Code Formatter` as the value of `Editor: Default Formatter` from the search results.

   - [GitLens — Git supercharged](https://marketplace.visualstudio.com/items?itemName=eamodio.gitlens):<br />
     The GitLens plugin for VS Code is a powerful tool that enhances your Git workflow within the editor. It provides detailed and interactive <b>Git annotations</b> directly inline with your code, such as blame annotations to see who last modified a specific line of code, commit details, and more. GitLens also offers rich navigation capabilities, allowing you to easily <b>jump to specific commits, branches, or repositories</b>. With GitLens, you can gain valuable insights into your code's history, understand changes, and collaborate more effectively with others in your team.

   - [Code Spell Checker](https://marketplace.visualstudio.com/items?itemName=streetsidesoftware.code-spell-checker):<br />
     The Code Spell Checker plugin for VS Code is a helpful tool for maintaining code quality by catching <b>spelling mistakes and typos</b> in your code and comments. It performs a comprehensive spell check on your codebase, highlighting any misspelled words and suggesting possible corrections. This plugin supports multiple programming languages and provides customizable dictionaries, allowing you to add or remove words specific to your project or industry. With the Code Spell Checker plugin, you can improve the readability and professionalism of your code by eliminating spelling errors, ensuring better communication and understanding among developers.

   - [Stylelint](https://marketplace.visualstudio.com/items?itemName=stylelint.vscode-stylelint):<br />
     The Stylelint plugin for VS Code is a valuable tool for maintaining consistent and error-free styles in your CSS, SCSS, and other style sheet files. Stylelint analyzes your stylesheets based on a set of defined rules, helping you <b>catch and fix common styling errors, enforce coding conventions, and improve code quality</b>. The plugin seamlessly integrates with VS Code, providing real-time linting feedback as you write your styles. It highlights style issues and offers suggestions for improvements, allowing you to adhere to best practices and maintain a clean and consistent codebase. With the Stylelint plugin, you can ensure your styles are well-structured, readable, and maintainable, resulting in a more professional and polished appearance for your web projects.

   - [Tailwind CSS IntelliSense](https://marketplace.visualstudio.com/items?itemName=bradlc.vscode-tailwindcss):<br />
     The Tailwind CSS IntelliSense plugin for VS Code is a valuable tool for enhancing your development workflow with the <b>Tailwind CSS framework</b>. It provides intelligent code completion, allowing you to quickly and accurately write Tailwind CSS class names in your HTML and CSS files. The plugin understands the structure of the Tailwind CSS utility classes and offers suggestions based on your project's configuration. It also provides documentation on hover, giving you instant access to class descriptions and examples. With Tailwind CSS IntelliSense, you can improve productivity, reduce errors, and easily leverage the power of Tailwind CSS in your projects within the VS Code editor.

     > **_Note_** : Use this plugin only if you are using [TailwindCss](https://tailwindcss.com/) in your application.

     <br />

2. <img src="images/webstorm.svg" alt="WebStorm" width="30" height="30" vertical-align="middle"> &nbsp; <b>[WebStorm](https://www.jetbrains.com/webstorm/)</b><br />
   WebStorm, developed by IntelliJ, is widely regarded as one of the most intelligent and powerful IDEs for JavaScript application development. It is highly recommended for building Angular applications, as it offers built-in support for <b>TypeScript</b> right out of the box. With WebStorm, you benefit from <b>intelligent code completion, real-time error detection, and robust navigation and refactoring capabilities for TypeScript and stylesheet languages</b>. The IDE is equipped with a comprehensive set of built-in developer tools, eliminating the need to install multiple plugins and ensuring a seamless development experience. Below is a curated list of WebStorm plugins that can further enhance your productivity when working on Angular projects. <br />

   - [Angular and AngularJS](https://plugins.jetbrains.com/plugin/6971-angular-and-angularjs):<br />
     This plugin provides comprehensive support for Angular projects, including <b>code completion, error detection, and advanced navigation and refactoring capabilities</b>. It offers intelligent completion for Angular-specific syntax, such as directives, components, and services. The plugin also includes integration with Angular CLI, allowing you to generate code snippets and perform common Angular commands directly within the IDE. With this plugin, you can streamline your development workflow and leverage the full power of Angular in WebStorm.

   - [ESLint](https://plugins.jetbrains.com/plugin/7494-eslint):<br />
     ESLint is a popular linter tool for JavaScript and TypeScript that helps <b>catch and fix code errors, enforce coding standards, and improve code quality</b>. The ESLint plugin for Webstorm integrates seamlessly with the editor, providing real-time linting feedback as you type. It highlights code issues, offers suggestions for improvements, and supports quick fixes to automatically resolve problems. With the ESLint plugin, you can ensure your code follows best practices and maintain a clean and error-free codebase.

   - [Prettier](https://plugins.jetbrains.com/plugin/10456-prettier):<br />
     The Prettier plugin for Webstorm is an essential tool <b>for code formatting and consistency</b>. Prettier automatically analyzes and formats your code to ensure a consistent and professional style, saving you time and effort. The Prettier plugin seamlessly integrates with VS Code, providing real-time formatting as you type, or you can format the entire file with a single command. With the Prettier plugin, you can easily maintain a clean and standardized codebase, enhancing readability and collaboration in your projects.

     > 💡 **_Tip_** : To run Prettier on save, tick the `Run on save for files` option in `Preferences/Settings | Languages \& Frameworks | JavaScript | Prettier`.

   - [IntelliJ Stylelint Plugin](https://plugins.jetbrains.com/plugin/9276-intellij-stylelint-plugin):<br />
     The Stylelint plugin for Webstorm is a valuable tool for maintaining consistent and error-free styles in your CSS, SCSS, and other style sheet files. Stylelint analyzes your stylesheets based on a set of defined rules, helping you <b>catch and fix common styling errors, enforce coding conventions, and improve code quality</b>. The plugin seamlessly integrates with Webstorm, providing real-time linting feedback as you write your styles. It highlights style issues and offers suggestions for improvements, allowing you to adhere to best practices and maintain a clean and consistent codebase. With the Stylelint plugin, you can ensure your styles are well-structured, readable, and maintainable, resulting in a more professional and polished appearance for your web projects.

   - [Tailwind CSS](https://plugins.jetbrains.com/plugin/15321-tailwind-css):<br />
     The Tailwind CSS plugin for WebStorm is a valuable tool for developers working with the <b>Tailwind CSS framework</b>. This plugin enhances your development experience by providing code completion, syntax highlighting, and documentation for Tailwind CSS classes directly within the WebStorm editor. It understands the structure of the Tailwind CSS utility classes and offers intelligent suggestions as you write your code, helping you write styles faster and with fewer errors. With the Tailwind CSS plugin, you can maximize your productivity and leverage the power of Tailwind CSS in your WebStorm projects.

 <br />
   
 >Do check out the [Angular IDE](https://www.genuitec.com/products/angular-ide/) by Codemix, which is a dedicated, powerful IDE for Angular.
 
 </details>  
   
 <br />
   
| ❤️ _Takeaway_ : Use your favorite IDE ([Visual Studio Code](https://code.visualstudio.com/) or [WebStorm](https://www.jetbrains.com/webstorm/) recommended) along with awesome plugins for a smooth development experience. |
| :--- |

<br />

🔝 [Back to Contents](#-table-of-contents)

<br />
  
<!-- STARTER KITS -->
## `🎉 Using Starter Kits`
<details>
  <summary>Click to expand</summary>
  <br />
While the Angular CLI's ng new command provides a solid foundation for starting an Angular project, there are times when developers seek more advanced features and a streamlined setup process. Angular starter kits and boilerplates are designed to significantly reduce the initial development time. These seeds offer a range of features, including recommended folder structures, interceptors, guards, and other commonly used functionalities. Below are some such Angular starter kits:

1. [EasyAngular](https://github.com/NicolasRoehm/angular-boilerplate/tree/master) : This project is designed to help you quickly start a new Angular 18 project with Bootstrap 5 and various useful libraries. It comes with pre-coded elements to streamline your development process.

2. [Angular Boilerplate](https://github.com/jm2097/angular-boilerplate) : This opinionated Angular starter focuses on the latest Angular features and best practices. It offers essential features for flexibility and scalability, minimizing unnecessary overhead. The codebase is lightweight yet robust, allowing developers to choose their preferred technologies like UI component libraries, state management, server-side rendering, etc. Its flexible boilerplate enables easy customization and adaptation to unique project requirements.

3. [ngx-admin](https://akveo.github.io/ngx-admin/) : One of the most widely used Angular **admin dashboard template** based on **Angular 9+, Bootstrap 4+ and Nebular**. This template packs all the features and more that you will need for an admin dashboard template.

</details>

<br />
   
| ❤️ _Takeaway_ : Use starters/boilerplates to save initial setup time and for a smooth start. |
| --- |

<br />

🔝 [Back to Contents](#-table-of-contents)

<br />

## `❄️ Git Guidelines`

 <details>
  <summary>Click to expand</summary>
  <br />
  While this chapter is not directly related to Angular and it's best practices, it will serve as a resource for maintaining a consistent and efficient Git workflow within your development team. These guidelines outline best practices for branching, committing, and collaborating on Git repositories. The guidelines cover various aspects, including branching strategies, commit message conventions. By adhering to these Git Guidelines, you can enhance code quality, streamline teamwork, and effectively manage your Git repositories.

### 1. Git Workflow

  <details open>
  <summary>Click to expand</summary>
  <br />
    Selecting a suitable Git workflow is crucial as it sets the foundation for effective collaboration and version control in your project. The right Git workflow can streamline development processes, ensure smooth integration of code changes, and promote seamless collaboration among team members. By carefully evaluating your project's requirements and considering factors such as team size, release cycles, and code review processes, you can make an informed decision and select a Git workflow that aligns with your project's needs, fostering efficient and collaborative development.
    <br />
    <br />
    If your project involves complex versioning and the need to support different release versions, GitFlow or GitLab Flow may be suitable options. On the other hand, if your project is internal and does not have multiple environments, GitHub Flow might be a better fit. For a continuous deployment model with multiple environments, GitLab Flow could be a good choice. Ultimately, the key is to select a workflow that best suits the unique characteristics and goals of your project.
    <br />
    <br />

> 🗒️ **_References_** : <br /> https://www.atlassian.com/git/tutorials/comparing-workflows <br /> https://about.gitlab.com/topics/version-control/what-is-gitlab-flow <br /> https://docs.github.com/en/get-started/quickstart/github-flow

  </details>

### 2. Branching Guidelines

  <details open>
  <summary>Click to expand</summary>
  <br />
    To ensure a consistent and organized approach to branching in your Git workflow, we recommend following the guidelines outlined below:
    <br />
    <br />

#### 1. One Branch per Ticket/Feature/Bug

Create a separate branch for each ticket, feature, or bug that you are working on. This practice isolates changes related to a specific task, making it easier to track, review, and manage code changes. It helps prevent conflicts between different sets of changes and allows for easier rollbacks if needed.

#### 2. Naming Conventions

- The branch name may follow the format: `<user>/<type>/<ticket-id>-<title>` or `<type>/<ticket-id>-<title>`
- `<user>` (optional) represents the name or identifier of the developer creating the branch.
- `<type>` represents the purpose or nature of the changes in the branch (e.g., `feat` for new features, `fix` for bug fixes, `refactor` for code refactoring, `docs` for documentation changes, `perf` for performance improvements, etc.).
- `<ticket-id>` refers to the associated ticket or issue ID from your project management system.
- `<title>` provides a concise and descriptive title for the changes being made in the branch.

  Example : `john/feat/123-add-login-page`

</details>

### 3. Commit Guidelines

<details open>
<summary>Click to expand</summary>

Developers often have a tendency to include random commit messages that lack value in the project. However, by adhering to precise rules for formatting commit messages, we can create more readable messages that are easily comprehensible when reviewing the project history. To ensure consistent commit message formatting, it is highly recommended to follow the [commit guidelines](https://github.com/angular/angular/blob/22b96b9/CONTRIBUTING.md#-commit-message-guidelines) provided by the official Angular repository. These guidelines, available in the official Angular repo, outline best practices for structuring commit messages. By following these guidelines, you can enhance the clarity and coherence of your commit messages, facilitating efficient collaboration and enabling the generation of informative changelogs.

Each commit message consists of a header, a body, and a footer (optional). The header is mandatory and the scope of the header is optional. The header has a special format that includes a type, a scope and a subject :

```
<type>(<scope>): <subject>
<BLANK LINE>
<body>
<BLANK LINE>
<footer>
```

#### Type

The type can be any of the following:

- `fix`: A bug fix
- `feat` : A new feature
- `docs`: Documentation only changes
- `refactor`: A code change that neither fixes a bug nor adds a feature
- `perf`: A code change that improves performance
- `test`: Adding missing tests or correcting existing tests
- `build`: Changes that affect the build system or external dependencies
- `ci`: Changes to our CI configuration files and scripts
- `chore`: Other changes that do not modify src or test files

#### Scope

The scope can be : `app`, `core`, `server`, `shared` or `tools`

#### Subject

The subject contains succinct description of the change

- use the imperative, present tense: "change" not "changed" nor "changes"
- be concise and direct
- no dot (.) at the end

#### Body

Just as in the subject, use the imperative, present tense: "change" not "changed" nor "changes". The body should include the motivation for the change and contrast this with previous behavior.

#### Footer

The footer can contain information about breaking changes and deprecations. It is also the place to reference Gitlab issues, Open Project tickets, and other PRs that are related to this commit or that this commit will close. For example:

```
BREAKING CHANGE: <breaking change summary>
<BLANK LINE>
<breaking change description + migration instructions>
<BLANK LINE>
<BLANK LINE>
Fixes #<issue number>
```

#### Example

```
feat(app): add user authentication functionality

This commit adds the user authentication feature, allowing users to sign up and log in to the application. It includes the following changes:

- Implement user registration API endpoint
- Create login form component
- Add authentication service for handling user login

Closes #123
```

<br />

> 💡 **_Tip_** : To help with following the above commit message standard, you can make use of [better-commits](https://github.com/Everduin94/better-commits) CLI tool. Also, as mentioned above, you can make use of automatic CHANGELOG generation based on the commit messages with the help of [release-please](https://github.com/googleapis/release-please) or [commit-and-tag-version](https://github.com/absolute-version/commit-and-tag-version).

<br />

> 🗒️ **_References_** : <br /> https://github.com/angular/angular/blob/main/CONTRIBUTING.md#-commit-message-format <br /> https://www.conventionalcommits.org/en/v1.0.0

</details>

| ❤️ _Takeaway_ : It's recommended to follow the commit guidelines of the [official Angular repo](https://github.com/angular/angular/blob/22b96b9/CONTRIBUTING.md#-commit-message-guidelines); consisting of a header, a body, and a footer (optional). Use these commits for generating changelogs. Additionally follow one branch per ticket pattern while creating branches. |
| :---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |

</details>

<br />

🔝 [Back to Contents](#-table-of-contents)

<br />

<!-- Styleguide -->

## `👷 Styleguide`

<details>
  <summary>Click to expand</summary>
  
  This chapter serves as a valuable resource for establishing consistent coding practices and stylistic conventions when developing Angular applications. It covers various aspects of Angular development, including component structure, naming conventions, code formatting, and more. By following the guidelines presented in the Angular Styleguide, you can ensure code consistency, improve collaboration among team members, and enhance the overall quality of your Angular projects. Whether you are a beginner or an experienced Angular developer, this chapter provides essential guidance to help you write Angular code that is easy to understand, maintain, and extend.

Head to the official [Angular Style Guide](https://angular.dev/style-guide), to learn in detail. Meanwhile, let's take a look at the main concepts.

### Naming

<details>
  <summary>Click to expand</summary><br/>

#### Folders

- Use consistent names for all folders after what they represent.

- Use kebab case for folder names. Use dashes to separate words in the name.

  eg : `my-feature`

#### Files

- Use consistent type names for all files following a pattern that describes the file's feature then its type. Use dots to separate the descriptive name (feature) from the type. A recommended pattern is `feature.type.ts`.

- Use kebab case for file names. Use dashes to separate words in the descriptive name (feature).

  eg : `feature-name.type.ts`

- Use conventional type names including `.service`, `.component`, `.pipe`, `.guard`, `.spec` and `.directive`. Invent additional type names if you must but take care not to create too many.

  eg : `home.component.ts`, `home.spec.ts`, `number-only.directive.ts`

- Use consistent names for all assets named after what they represent.

#### Services

- Use consistent names for all services named after their feature.

- Use pascal case for class names.

  eg : `DashboardService`

- Suffix a service class name with `Service`. For example, something that gets data or heroes should be called a `DataService` or a `HeroService`. A few terms are unambiguously services. They typically indicate agency by ending in _"-er"_. You may prefer to name a service that logs messages `Logger` rather than `LoggerService`. Decide if this exception is agreeable in your project. As always, strive for consistency.

#### Components

- Use pascal case for class names.

- Use consistent names for all components named after their feature.

- Suffix a component class name with Component.

  eg : `DashboardComponent`

  Use _dashed-case_ or _kebab-case_ for naming the element selectors of components. If using a custom prefix, use a prefix that identifies the feature area or the application itself. Generally it's more safer to use _app-_ prefix to avoid any possible conflicts with a third-party library component, or new HTML tags in the future.
  eg : `app-dashboard`

#### Directives

- Use pascal case for class names.

- Use consistent names for all directives named after their feature.

- Suffix a directive class name with `Directive`.

  eg : `TrimDirective`

- Use lower camel case for naming the selectors of directives. If using custom prefix, avoid using _ng_ as prefix because that prefix is reserved for Angular and using it could cause bugs that are difficult to diagnose. Generally it's more safer to use app prefix to avoid any possible conflicts with a third-party library directive, or new HTML directives in the future.

  eg : `appTrim`

#### Pipes

- Use upper camel case for class names.

- Use consistent names for all pipes named after their feature.

- Suffix a pipe class name with `Pipe`.

  eg : `MyCustomPipe`

- Use lower camel case for the selector name strings, and avoid using dash case or kebab case.

  eg : `timeFormat`

#### Guards

- Use pascal case for guards class names, or camel case if using guard function.

- Use consistent names for all pipes named after their feature.

- Suffix a guard class name with `Guard`.

  eg : `AuthenticationGuard` (when using a class), `featureFlagGuard` (when using a function)

#### Tests

- Name test specification description the same as the component class name they test.

  eg : name both component and spec description as `DashboardComponent`

- Name test specification files the same as the component they test with a suffix of `.spec`.

  eg : `dashboard.spec.ts`

#### Functions

- Use camel case for function names.

  eg : `myFunction()`

- Use meaningful names that accurately describe what the function does.

  eg: `calculateTotal()`

- Use whole words in names when possible, and avoid abbreviations and acronyms.

- You may use `_` for private functions. But always make sure you use `private` keyword as a prefix to the function name to make it actually private.

#### Properties

- Use camel case for property names.

  eg : `myProperty`

- Use meaningful property names that accurately describe the purpose or content of the property.

  eg : `firstName = 'John'`

- Use whole words in names when possible, and avoid abbreviations and acronyms.

- You may use `_` for private variables. But always make sure you use `private` keyword as a prefix to the property name to make it actually private.

- Avoid using _`#private`_ identifiers as it can cause substantial emit size and performance regressions when down-leveled by TypeScript, and are unsupported before ES2015. Instead, you can use TypeScript's `private` visibility annotation.

  eg :

  ```ts
  private firstName = 'John'
  ```

- You may use $ postfix for observables.

  eg : `myObservable$`

#### Constants

- Use upper snake case for constant names.

  eg :

  ```ts
  export const MAX_LENGTH = 10;
  ```

- Use meaningful names that accurately describe the purpose or content of the constant.

- Use whole words in names when possible, and avoid abbreviations and acronyms.

#### Interfaces

- Use pascal case for interface names.

  eg : `ProductData`

- Use meaningful names that accurately describe the purpose or content of the interface or type.

- Use whole words in names when possible, and avoid abbreviations and acronyms.

#### Enums

- Use pascal case for enum names.

  eg : `ProductType`

- Use meaningful names that accurately describe the purpose or content of the enum.

- Use whole words in names when possible, and avoid abbreviations and acronyms.

<br/>

> 🗒️ **_References_** : <br /> https://angular.dev/style-guide <br /> https://ts.dev/style/#syntax

</details>

### Typescript Best Practices

<details>
  <summary>Click to expand</summary><br/>

- Use strong typing: Take advantage of TypeScript's static types to catch errors during development and improve code readability.

- Enable strict mode: Set `"strict": true` in your `tsconfig.json` file to enable all strict type checking options.

- Use interfaces and types: Define interfaces and types to describe the shape of your data and promote code reuse.

- Avoid using the `any` type: Instead, use explicit types or utilize TypeScript's type inference.

- Use explicit access modifiers: Specify `public`, `private`, or `protected` for class members to control their accessibility.

- Enable strict null checks: Set `"strictNullChecks": true` in your tsconfig.json file to catch potential null or undefined references.

- Prefer `const` over `let`: Use `const` for variables that won't be reassigned to ensure immutability.

- Utilize TypeScript's advanced features: Take advantage of features such as union types, intersection types, and type guards to write more expressive and safer code.

- Write clear and concise comments: Use comments to explain the intent, purpose, and logic behind your code.

<br/>

> 💡 **_Tip_** : Check out a [sample `tsconfig.json` file](./samples/tsconfig.json)

> 🗒️ **_References_** : <br /> https://ts.dev/style/

### Single Responsibility Principle

<details>
  <summary>Click to expand</summary><br/>

Apply the [single responsibility principle (SRP)](https://en.wikipedia.org/wiki/Single_responsibility_principle) to all components, services, and other symbols. This helps make the application cleaner, easier to read and maintain, and more testable.

- Define one thing, such as a service or component, per file.

- Consider limiting files to 400 lines of code.

<br/>

> 🗒️ **_References_** : <br /> https://angular.dev/style-guide#single-responsibility

</details>

### Design Patterns

<details>
  <summary>Click to expand</summary>

#### Container-Presentation Pattern

The container-presentation pattern, also known as the _smart-dumb component pattern_ or the _container-component pattern_, is a software design pattern commonly used in Angular applications.

In this pattern, the container component is responsible for managing the data and the state of the application. It fetches the data from services or APIs, performs any necessary transformations or calculations, and passes the data down to the presentation component.

The presentation component, also known as the _dumb component_, is responsible for rendering the data and handling user interactions. It receives the data from the container component as input properties and emits events to notify the container component about user actions.

By separating the responsibilities of data management and rendering, the container-presentation pattern promotes a more modular and reusable codebase. It also makes it easier to test the components independently.

Here is an example of how the container-presentation pattern can be implemented in Angular:

```ts
// Container Component
@Component({
  selector: "app-container",
  template: `
    <app-presentation
      [data]="data"
      (action)="handleAction($event)"
    ></app-presentation>
  `,
})
export class ContainerComponent implements OnInit {
  data: PresentationData;

  constructor(private dataService: DataService) {}

  ngOnInit() {
    this.dataService.getData(pipe(take(1))).subscribe((data) => {
      this.data = data;
    });
  }

  handleAction(): void {
    // Handle user action
  }
}

// Presentation Component
@Component({
  selector: "app-presentation",
  template: `
    <div>{{ data }}</div>
    <button (click)="handleClick()">Action</button>
  `,
})
export class PresentationComponent {
  @Input() data: PresentationData;

  @Output() action = new EventEmitter<void>();

  handleClick() {
    // Emit action event
    this.action.emit();
  }
}
```

In this example, the `ContainerComponent` fetches the data from a data service and passes it down to the `PresentationComponent` as an input property. The `PresentationComponent` renders the data and emits an action event when the button is clicked. The `ContainerComponent` handles the action event and performs the necessary logic.

</details>

### Prettier

The **opinionated code formatter**, prettifies our code to look even more beautiful :heart*eyes:. First step is to install the Prettier plugin in your favorite IDE (go to [Choosing IDE](#sunglasses-choosing-ide)) or `npm install prettier` to make your team members reference the same configuration file regardless of the IDE. Don't forget to set the \_format on save* option in your IDE.

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

🔝 [Back to Contents](#-table-of-contents)

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
> Add a logger system in `logger.service.ts` file (refer [here](https://github.com/ngx-rocket/starter-kit/blob/master/src/app/%40core/logger.service.ts)).

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

> :page*with_curl: \*\*\_Note*\*\* : Don't forget to add the components, directives and pipes to the `exports` inside `shared.module.ts`.

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

It's preferred to add a `theme` folder inside `src` to include custom themes and scss variables.

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

> :gift: **_Resources_** : <br /> 1. Check out [Choosing The Right File Structure for Angular in 2020 and Beyond 📕!](https://itnext.io/choosing-the-right-file-structure-for-angular-in-2020-and-beyond-a53a71f7eb05) by [Mathis Garberg](https://itnext.io/@mathis.garberg). <br /> 2. Check out [How to architect epic Angular app in less than 10 minutes! ⏱️😅](https://medium.com/@tomastrajan/how-to-build-epic-angular-app-with-clean-architecture-91640ed1656) by [Tomas Trajan](https://medium.com/@tomastrajan). <br /> 3. Check out [Angular Folder Structure](https://medium.com/@motcowley/angular-folder-structure-d1809be95542) by [Tom Cowley](https://medium.com/@motcowley). <br /> 4. Check out the excellent folder structure in these [starter kits](#-using-starter-kits).

<br />

| :heart: _Takeaway_ : Split our application into at least three different modules — Core, Shared and Feature; below is the bigger picture 🖼️ : |
| :-------------------------------------------------------------------------------------------------------------------------------------------- |

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

🔝 [Back to Contents](#-table-of-contents)

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
<tr *ngFor="let book of books">
  {{calculatePrice(book)}}
</tr>
❌
```

#### Why?

Angular will run your function in each of it's change detection cycle (which is quite frequent) and if the function is a complex one, this will impose a serious effect on the performance.

#### Solution:

There may be some cases where this is unavoidable, but for most cases this can be avoided by:

1.  **Creating a property in the ts file and setting the value to it once.**

    ```js
    this.books = this.books.map(book => ( { ...books, price: calculatePrice(book)  } );
    ```

2.  **Using pure pipes** : A pure pipe is a pipe that will always always return the same output for an input. Angular executes a pure pipe only when it detects a pure change to the input value because it already knows that the pipe will return the same value for the same input.

    ```js
    @Pipe({
      name: "dummy",
      pure: true,
    })
    export class somePipe implements PipeTransform {
      transform(value: any, args?: any): any {
        // logic
      }
    }
    ```

    > :gift: **_Resources_** : Check out [The essential difference between pure and impure pipes in Angular and why that matters](https://indepth.dev/the-essential-difference-between-pure-and-impure-pipes-in-angular-and-why-that-matters/) by [Max Koretskyi](https://indepth.dev/author/maxkoretskyi/)

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
import { Injectable } from "@angular/core";

@Injectable({
  providedIn: "root", // or 'any' or 'platform'
})
export class SomeService {}
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

2. If you need to subscribe to an observable only once, use `take(1)`. 📄 Note that you will need to use `takeUntil` to avoid any memory leaks caused when the subscription hasn’t received a value before the component got destroyed.

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

> :page*facing_up: \*\*\_Note*\*\* : Do not lazy load the default route, as the browser will have to download an extra lazy loaded chunk after downloading the main chunk and parse it. This will slow down the initial rendering time.

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
   import { Observable } from "rxjs/Observable";
   import { PreloadingStrategy, Route } from "@angular/router";

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
> Or, make use of machine learning by predictively preloading modules with [Guess.js](https://github.com/guess-js/guess) :crystal_ball:.

<br />

> :gift: **_Resources_** : <br /> 1. Check out [Preloading in Angular](https://alligator.io/angular/preloading/) on [alligator.io](https://alligator.io/). <br /> 2. Check out [Route preloading strategies in Angular](https://web.dev/route-preloading-in-angular/) by [Minko Gechev](https://web.dev/authors/mgechev/).

</details>

### 8. Lazy load components

> :page*facing_up: \*\*\_Note*\*\* : This feature is only supported in Angular 9+.

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
     declarations: [LazyComponent],
     imports: [CommonModule, SharedModule],
   })

   // Remove export statement to avoid accidental imports in other files.
   class LazyCompModule {}
   ```

<br />

> :gift: **_Resources_** : <br /> 1. Check out [Angular 9: Lazy Loading Components](https://johnpapa.net/angular-9-lazy-loading-components/) by [John Papa](https://github.com/johnpapa). <br /> 2. Check out [Lazy load Angular components](https://medium.com/angular-in-depth/lazy-load-components-in-angular-596357ab05d8) by [Kevin Kreuzer](https://medium.com/@kevinkreuzer).

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

> :page*facing_up: \*\*\_Note*\*\* : Make use of `detectChanges()` or `markForCheck()` functions of `ChangeDetectorRef` to explicitely run the change detection cycle if required.

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

> :page*facing_up: \*\*\_Note*\*\* : Make use of `run()` method to explicitely run the change detection cycle if required.

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

> :gift: **_Resources_** : <br /> 1. Check out [Getting started with service workers](https://angular.io/guide/service-worker-getting-started) in the official Angular docs. <br /> 2. Check out [Angular Service Worker - Step-By-Step Guide for turning your Application into a PWA](https://blog.angular-university.io/angular-service-worker/) on [Angular University](https://blog.angular-university.io/). <br /> 3. Check out [How to build Progressive Web Apps with Angular.](https://scotch.io/tutorials/how-to-build-progressive-web-apps-with-angular) by [Eniola Lucas](https://scotch.io/@enirate).

<br />

#### 3. App Shell

We can improve the user experience by quickly launching a static rendered page (a skeleton common to all pages) while the browser downloads the full client version and switches to it automatically after the code loads. This will significantly reduce the time for the first paint since the browser just need to render HTML and CSS without the need for initialize any Javascript. Such a cool feature :hushed:!

<br />

We can make use of the Angular CLI to automatically generate an app shell for us with the command `ng generate app-shell`. Or thinking ahead, we can make use of Angular Universal to pre-render a static app shell :milky_way:. Do check out the resources to know more about it.

<br />

> :gift: **_Resources_** : <br /> 1. Check out [App shell](https://angular.io/guide/app-shell) in the official Angular docs. <br /> 2. Check out [Angular App Shell - Boosting Application Startup Performance](https://blog.angular-university.io/angular-app-shell/) on [Angular University](https://blog.angular-university.io/).

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

> :gift: **_Resources_** : <br /> 1. Check out [Web Assembly](https://developer.mozilla.org/en-US/docs/WebAssembly) in MDN. <br /> 2. Check out [Examples of how to use WebAssembly within Angular](https://github.com/boyanio/angular-wasm) by [Boyan Mihaylov](https://github.com/boyanio). <br /> 3. Check out [Using Web Assembly to speed up your Angular Application](https://malcoded.com/posts/web-assembly-angular/) by [Lukas Marx](https://twitter.com/malcoded).

</details>

<!-- Main details tag close -->
</details>

<br />

> :gift: **_Resources_** : <br /> 1. Do check out this awesome repo : [angular-performance-checklist](https://github.com/mgechev/angular-performance-checklist) by [Minko Gechev](https://github.com/mgechev) and find out more pro performance tips :heart*eyes:. <br /> 2. Check out [Best practices for a clean and performant Angular application](https://www.freecodecamp.org/news/best-practices-for-a-clean-and-performant-angular-application-288e7b39eb6f/) by [Vamsi Vempati](https://twitter.com/_VamsiVempati*). <br /> 3. Check out [Optimizing the Performance of Your Angular Application](https://netbasal.com/optimizing-the-performance-of-your-angular-application-f222f1c16354) by [Netanel Basal](https://netbasal.com/@NetanelBasal). 4. Check out [15 Angular Performance Tips & Tricks](https://angular-guru.com/blog/angular-performance-tips) on [The Angular Guru](https://angular-guru.com/).

<br />

| :heart: _Takeaway_ :                                                                                                                                                                    |
| :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 1. Make use of pure pipes to avoid function calls in templates                                                                                                                          |
| 2. Use `trackBy` with `*ngFor` to minimize DOM manipulations by tracking array items with a unique identifier.                                                                          |
| 3. Use `providedIn` attribute to make your services tree shakable.                                                                                                                      |
| 4. Unsubscribe your observables to avoid memory leaks and use async pipe whenever possible to make Angular handle the subscriptions.                                                    |
| 5. Lazy load modules and components to separate build bundles and load them on demand. Make use of preloading strategies to avoid possible latency while loading the lazy loaded chunk. |
| 6. Use a combination of `ChangeDetectionStrategy.OnPush`, `ChangeDetectorRef` and `NgZone` methods to minimize the number of change detection cycles.                                   |
| 7. Use service workers, app shell and api caching to further improve the performance.                                                                                                   |

<br />

🔝 [Back to Contents](#-table-of-contents)

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
