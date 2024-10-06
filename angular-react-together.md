### 1. **React Hooks**
   React hooks allow you to use state and lifecycle features in functional components. Common hooks include:
   - `useState` for managing state.
   - `useEffect` for side effects (e.g., fetching data).
   - `useContext` for using context in components.

### 2. **React Design Principles**
   - **Component-Based Architecture**: Build encapsulated components that manage their own state.
   - **Unidirectional Data Flow**: Data flows from parent to child via props.
   - **Declarative**: Describe what the UI should look like based on the application state.

### 3. **Redux Toolkit**
   Simplifies Redux setup by providing tools like `createSlice` and `createAsyncThunk`, reducing boilerplate code. It’s used for managing global state in React applications.

### 4. **Reduce in JavaScript Array**
   The `reduce` method executes a reducer function on each element of the array, resulting in a single output value.

   ```js
   const total = [1, 2, 3].reduce((acc, num) => acc + num, 0);
   ```

### 5. **Angular View Encapsulation**
   Controls the style isolation in Angular components. There are three types:
   - **Emulated**: Default, styles are scoped to the component.
   - **Shadow DOM**: Uses Shadow DOM for style encapsulation.
   - **None**: Styles are applied globally.

### 6. **React Form in Angular**
   Angular has its own form handling through template-driven and reactive forms. For handling forms in Angular, use `ReactiveFormsModule` for reactive forms.

### 7. **Content Projection**
   Allows you to pass content from a parent component to a child component in Angular. It’s done using `<ng-content>`.

### 8. **Web Worker**
   A Web Worker runs in the background thread, allowing you to perform heavy computations without blocking the main UI thread in JavaScript.

### 9. **Suspense in React**
   Suspense is a feature for managing asynchronous data fetching in React. It allows you to show fallback content while waiting for data.

### 10. **React Custom Hook**
   Custom hooks are reusable functions that contain logic used by React components. They allow you to extract and reuse functionality in multiple components.

### 11. **Reactive Form in Angular**
   A form approach that offers more control and flexibility. Reactive forms use a model-driven approach to handle form inputs and validations.

   ```typescript
   this.form = this.fb.group({
     name: ['', Validators.required],
     password: ['', Validators.required],
     address: this.fb.group({
       zip: ['', Validators.required],
       country: ['', Validators.required]
     })
   });
   ```

### 12. **HTML Select and Option**
   `<select>` creates a dropdown, and `<option>` defines the individual options within the dropdown.

   ```html
   <select>
     <option value="1">Option 1</option>
     <option value="2">Option 2</option>
   </select>
   ```

### 13. **Function Coding**
   In JavaScript, a function is a block of code designed to perform a particular task. Example:

   ```js
   function greet(name) {
     return `Hello, ${name}`;
   }
   ```

### 14. **Generative Function**
   A generator function returns an iterator object and is declared using `function*`. It allows pausing and resuming the execution of a function.

   ```js
   function* gen() {
     yield 1;
     yield 2;
   }
   ```

### 15. **Custom Directive**
   Custom directives in Angular allow you to extend HTML functionality. Example:

   ```typescript
   @Directive({
     selector: '[appHighlight]'
   })
   export class HighlightDirective {
     constructor(el: ElementRef) {
       el.nativeElement.style.backgroundColor = 'yellow';
     }
   }
   ```

### 16. **Event Loop**
   JavaScript is single-threaded. The event loop allows asynchronous code (like `setTimeout`, Promises) to execute after the synchronous code.

### 17. **Middleware in Express for JWT**
   Middleware in Express.js intercepts requests. You can use JWT middleware to authenticate users.

   ```javascript
   const jwt = require('jsonwebtoken');
   const authenticateJWT = (req, res, next) => {
     const token = req.header('Authorization');
     if (token) {
       jwt.verify(token, 'secretkey', (err, user) => {
         if (err) return res.sendStatus(403);
         req.user = user;
         next();
       });
     } else {
       res.sendStatus(401);
     }
   };
   ```

### 18. **Multiple Promises**
   You can use `Promise.all()` to handle multiple promises concurrently.

   ```js
   Promise.all([promise1, promise2]).then(results => {
     console.log(results);
   });
   ```

### 19. **CI/CD and How It Works**
   CI/CD automates the integration and deployment processes. Continuous Integration (CI) ensures that code is integrated regularly and tested. Continuous Deployment (CD) automates the deployment of code to production.

### 20. **Angular Lifecycle Methods**
   Angular lifecycle methods manage component initialization and destruction. Key methods include:
   - `ngOnInit()`: Called once the component is initialized.
   - `ngOnChanges()`: Called when an input-bound property changes.
   - `ngOnDestroy()`: Called before the component is destroyed.

### 21. **Directive Definition and Types**
   - **Component Directive**: Defines a view with a template.
   - **Structural Directive**: Changes the DOM structure (`*ngIf`, `*ngFor`).
   - **Attribute Directive**: Changes the appearance or behavior of an element (like `ngClass`, `ngStyle`).

### 22. **Reactive Form vs Template-Driven Form**
   - **Reactive Forms**: More flexible, model-driven approach. Suitable for complex forms.
   - **Template-Driven Forms**: Simpler, declarative approach. Suitable for simple forms.

### 23. **Reactive Form Example**
   ```typescript
   this.form = this.fb.group({
     name: ['', Validators.required],
     password: ['', Validators.required],
     address: this.fb.group({
       zip: ['', Validators.required],
       country: ['', Validators.required]
     })
   });
   ```

### 24. **FormBuilder**
   A helper service in Angular to simplify the creation of reactive forms.

   ```typescript
   constructor(private fb: FormBuilder) {}
   ```

### 25. **Custom Validators**
   Angular allows creating custom validators by implementing `ValidatorFn` or `AsyncValidatorFn`.

   ```typescript
   function customValidator(control: FormControl): ValidationErrors | null {
     return control.value.includes('test') ? { invalidWord: true } : null;
   }
   ```

### 26. **Custom Component Example**
   ```typescript
   @Component({
     selector: 'app-custom',
     template: `<p>Hello {{name}}</p>`
   })
   export class CustomComponent {
     @Input() name: string;
   }
   ```

### 27. **Custom Element Example**
   Custom Elements allow you to define your own HTML tags. Angular provides `@angular/elements` for creating them.

   ```typescript
   customElements.define('my-element', class extends HTMLElement {
     connectedCallback() {
       this.innerHTML = `<p>Hello, World!</p>`;
     }
   });
   ```

### 28. **Semantic Tags**
   Semantic tags like `<article>`, `<section>`, `<header>`, and `<footer>` provide meaning to the web content, helping both the browser and developers understand the structure.

### 29. **Data Passing from Component A to Component B**
   - **Input Property**: Pass data from parent to child via `@Input()`.
   - **Output EventEmitter**: Emit events from child to parent via `@Output()`.

### 30. **Next.js and Its Features**
   Next.js is a React framework that provides server-side rendering, static site generation, and file-based routing. It improves SEO and performance with features like automatic static optimization.

### 31. **Rules for Custom Hook**
   - Hooks should start with `use`.
   - Hooks can only be called inside functional components or other hooks.
   - Hooks should not be called conditionally.

### 32. **REST API**
   REST API (Representational State Transfer) is an architectural style for designing networked applications. It uses HTTP methods like GET, POST, PUT, DELETE.

### 33. **Injectable in Angular**
   The `@Injectable()` decorator allows a service to be injected into components or other services in Angular.

### 34. **Signals in Angular**
   Signals represent a potential new feature in Angular to handle reactivity more declaratively, similar to signals in frameworks like Svelte or Solid.js.

### 35. **Custom Validator and Test Case**
   Custom validators are defined in Angular by implementing `ValidatorFn`.

   **Test Case Example:**

   ```typescript
   it('should return invalid if word is "test"', () => {
     const control = new FormControl('test');
     const result = customValidator(control);
     expect(result.invalidWord).toBeTruthy();
   });
   ```

### 36. **NgRx in Angular**
   NgRx is a state management library for Angular applications, based on the Redux pattern. It provides a way to manage global state and side effects (with `ngrx/effects`).

### 37. **Handling Large Data in Angular**
  

 - **Pagination**: Load data in chunks.
   - **Virtual Scrolling**: Render only the visible items.
   - **Lazy Loading**: Load components or data only when needed.

### 38. **Ng-container and Templating**
   - **Ng-container**: A logical container that does not render an actual DOM element but can group structural directives like `*ngIf` or `*ngFor`.
   - **Templating**: Allows dynamic rendering of components or HTML based on conditions or data.
