# AffordableLoam

Component to calculate the optimal mortgage a person can obtain based on income, expenses, and other factors.
It works as a web component that can be embedded in any website (instructions below).

This project was generated using [Angular CLI](https://github.com/angular/angular-cli) version 20.0.1.

## Development server

To start a local development server, run:

```bash
ng serve
```

Once the server is running, open your browser and navigate to `http://localhost:4200/`. The application will automatically reload whenever you modify any of the source files.

## Code scaffolding

Angular CLI includes powerful code scaffolding tools. To generate a new component, run:

```bash
ng generate component component-name
```

For a complete list of available schematics (such as `components`, `directives`, or `pipes`), run:

```bash
ng generate --help
```

## Building

To build the project run:

```bash
ng build
```

This will compile your project and store the build artifacts in the `dist/` directory. By default, the production build optimizes your application for performance and speed.

Go to the dist/browser folder generated with the `ng build` command. In the `index.html` file, add this id to the stylesheet line: affordable-styles. This is necessary for the amortization table download feature to work.

The result should look like this:

```html
<link id="affordable-styles" rel="stylesheet" href="styles-(SOMEHASH).css">
```

Then, inject the corresponding component content into the `index.html` file, like this:

```html
<script src="https://cdnjs.cloudflare.com/ajax/libs/html2pdf.js/0.10.1/html2pdf.bundle.min.js"></script>
<link id="affordable-styles" rel="stylesheet" href="styles-(SOMEHASH).css">
<loam-calculator></loam-calculator>
<script src="main-(SOMEHASH).js" type="module"></script>
```
Change the file paths as needed to match where you are serving them from.

## Running unit tests

To execute unit tests with the [Karma](https://karma-runner.github.io) test runner, use the following command:

```bash
ng test
```

## Running end-to-end tests

For end-to-end (e2e) testing, run:

```bash
ng e2e
```

Angular CLI does not come with an end-to-end testing framework by default. You can choose one that suits your needs.

## Additional Resources

For more information on using the Angular CLI, including detailed command references, visit the [Angular CLI Overview and Command Reference](https://angular.dev/tools/cli) page.
