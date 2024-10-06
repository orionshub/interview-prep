### **React Topics:**

1. **React Hooks (useState, useEffect, etc.):**
   - `useState`: Manages state in functional components.
   - `useEffect`: Runs side effects (like fetching data) after rendering.
   - `useMemo`/`useCallback`: Memoize values or functions to optimize performance.

2. **Component Lifecycle (Class vs Functional):**
   - Class components have lifecycle methods like `componentDidMount`.
   - Functional components use `useEffect` for side effects.

3. **State Management (Context API, Redux):**
   - Context API: Provides global state within a tree of components.
   - Redux: A state management library with a global store, actions, and reducers.

4. **Component Communication (Props, Context, Lifting State Up):**
   - Props: Data passed from parent to child components.
   - Context: Shares state globally without prop drilling.
   - Lifting State Up: Moving shared state to the nearest common ancestor.

5. **Virtual DOM:**
   - React creates a lightweight copy of the real DOM to update only necessary parts, improving performance.

6. **React Router (SPA, Route Guards):**
   - Used for client-side routing in SPAs. Route guards can protect routes (e.g., requiring authentication).

7. **Performance Optimization (Lazy Loading, Code Splitting):**
   - Lazy loading dynamically loads components.
   - Code splitting splits the app into chunks to load only what is needed.

8. **Higher-Order Components (HOCs) and Render Props:**
   - HOC: A function that takes a component and returns a new component.
   - Render Props: Passing a function as a prop to control component rendering.

9. **Error Boundaries:**
   - Components that catch JavaScript errors in their child components’ tree, preventing the app from crashing.

10. **Forms Handling (Controlled vs Uncontrolled Components):**
    - Controlled: Form data is handled by React state.
    - Uncontrolled: Form data is handled by the DOM.

11. **Custom Hooks:**
    - Reusable functions that encapsulate logic involving hooks (like data fetching or form handling).

12. **JSX Syntax:**
    - Syntax extension for JavaScript, used to describe UI elements in React. Compiled into `React.createElement()`.

13. **React with TypeScript:**
    - Enforces types for props, state, and components, improving code safety and readability.

14. **Testing React Components:**
    - Use Jest and React Testing Library for unit and integration testing of components.

15. **Micro Frontends (single-spa architecture):**
    - Divides a large application into smaller, independently deployable modules or micro frontends.

---

### **Angular Topics:**

1. **Lifecycle Hooks (ngOnInit, ngAfterViewInit, etc.):**
   - `ngOnInit`: Runs after component initialization.
   - `ngAfterViewInit`: Runs after the view and child views are initialized.

2. **Component Interaction (Input, Output, EventEmitter):**
   - `@Input()`: Passes data from parent to child.
   - `@Output()`: Sends events from child to parent using `EventEmitter`.

3. **Change Detection (Zone.js, OnPush):**
   - Default change detection runs on every DOM event. OnPush strategy optimizes by only checking when inputs change.

4. **Angular Forms (Reactive vs Template-Driven Forms):**
   - Reactive: Uses `FormControl` and `FormGroup` for more control.
   - Template-Driven: Simpler, using directives like `ngModel`.

5. **Routing and Guards (Lazy Loading, Route Guards):**
   - Lazy loading loads modules on demand.
   - Route Guards (e.g., `CanActivate`) protect routes based on conditions like authentication.

6. **Dependency Injection (DI) and Services:**
   - DI allows injecting services into components. Services are singleton objects that handle logic.

7. **RxJS Observables:**
   - Used for asynchronous data streams. Common operators: `map`, `filter`, `switchMap`, etc.

8. **Directives (ngIf, ngFor, custom directives):**
   - `ngIf`: Conditionally renders elements.
   - `ngFor`: Loops through a collection to render elements.
   - Custom Directives: Create reusable logic to manipulate the DOM.

9. **Modules (NgModule, Feature Modules, Shared Modules):**
   - `NgModule` declares components, imports modules, and provides services.
   - Feature and Shared Modules help organize code and reuse functionalities.

10. **Angular CLI:**
    - A command-line tool to create, build, serve, and test Angular apps efficiently.

11. **HTTP Client (API calls, interceptors):**
    - Used for making HTTP requests and handling responses. Interceptors can modify requests/responses globally.

12. **Angular Universal (SSR):**
    - Server-side rendering improves SEO and initial load performance.

13. **Pipes (Built-in, Custom):**
    - Pipes transform data in templates. Built-in examples: `date`, `currency`. Custom pipes transform data in specific ways.

14. **Angular with TypeScript:**
    - Angular heavily uses TypeScript for strong typing, improving maintainability and developer experience.

15. **Testing (Karma, Jasmine):**
    - Karma: A test runner.
    - Jasmine: A testing framework for writing unit tests in Angular.
