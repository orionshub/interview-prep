### **1. What are Angular Lifecycle Hooks? Explain some common hooks.**
   **Answer:**
   - Angular lifecycle hooks are special methods that allow developers to tap into different stages of a component's life.
   - Common hooks:
     - **ngOnInit**: Runs once after component initialization. Used for component setup.
     - **ngAfterViewInit**: Runs after the component's view and child views have been initialized.
     - **ngOnChanges**: Called whenever data-bound input properties change.

---

### **2. How does component interaction work in Angular?**
   **Answer:**
   - **@Input()**: Used to pass data from parent to child components.
   - **@Output()**: Emits an event from a child component to communicate with the parent. Uses `EventEmitter` to emit custom events.
   - Components can also share data via services.

---

### **3. Explain Change Detection in Angular. What is the OnPush strategy?**
   **Answer:**
   - Angular uses **change detection** to update the UI in response to user interactions or async operations.
   - **Zone.js** tracks asynchronous operations and triggers change detection.
   - The **OnPush strategy** optimizes performance by checking only when the component's input properties change, rather than on every event or async task.

---

### **4. What is the difference between Reactive Forms and Template-Driven Forms in Angular?**
   **Answer:**
   - **Reactive Forms**: More control, using `FormGroup`, `FormControl`, and `FormBuilder`. Suitable for complex forms with dynamic validations.
   - **Template-Driven Forms**: Simpler, built using directives like `ngModel` in the template. Ideal for simpler forms with less complex logic.

---

### **5. How does Angular handle routing and lazy loading?**
   **Answer:**
   - Angular uses the **RouterModule** to define routes in the app.
   - **Lazy loading** is implemented using **loadChildren** to load feature modules only when needed, improving performance by splitting the app into smaller bundles.
   - Route Guards (e.g., `CanActivate`, `CanDeactivate`) protect routes based on logic like authentication.

---

### **6. What is Dependency Injection in Angular? How do services work?**
   **Answer:**
   - **Dependency Injection (DI)** is a design pattern where a class requests dependencies from an external source (like a service) rather than creating them.
   - **Services** are singleton classes that encapsulate logic, such as fetching data. They are provided via the `providers` array in `NgModule` or `@Injectable()` decorator.

---

### **7. What are RxJS Observables? How do they work in Angular?**
   **Answer:**
   - **Observables** are streams of asynchronous data that can emit multiple values over time. RxJS provides operators like `map`, `filter`, and `switchMap` to handle data transformation.
   - In Angular, **HttpClient** returns observables when making HTTP requests, allowing developers to manage asynchronous data streams efficiently.

---

### **8. What are Directives in Angular? What is the difference between structural and attribute directives?**
   **Answer:**
   - **Directives** are instructions that extend the DOM by modifying elements.
   - **Structural directives**: Modify the DOM layout by adding or removing elements (e.g., `*ngIf`, `*ngFor`).
   - **Attribute directives**: Modify the behavior or appearance of elements (e.g., `ngClass`, `ngStyle`, or custom directives).

---

### **9. What are Angular Modules? Explain Feature and Shared Modules.**
   **Answer:**
   - **NgModules** are containers for a cohesive block of code dedicated to an application domain or a workflow. They group components, directives, pipes, and services.
   - **Feature Modules**: Split the app's functionality into smaller, manageable modules.
   - **Shared Modules**: Contain commonly used components, directives, and pipes that are shared across different modules.

---

### **10. What is Angular CLI and how is it useful?**
   **Answer:**
   - The **Angular CLI** is a command-line interface for creating, building, serving, and testing Angular apps. It automates common tasks such as scaffolding new components, services, and modules, running tests, and optimizing builds for production.

---

### **11. How does Angular’s HTTP Client work? What are interceptors?**
   **Answer:**
   - **HttpClientModule** is used for making HTTP requests in Angular, providing methods like `get()`, `post()`, etc.
   - **Interceptors** are middleware functions that can modify requests or responses globally. They are useful for adding headers, handling errors, or logging requests.

---

### **12. What is Angular Universal and why is Server-Side Rendering (SSR) important?**
   **Answer:**
   - **Angular Universal** allows rendering Angular apps on the server. Server-side rendering (SSR) improves performance (faster initial load) and SEO by rendering pages on the server before sending them to the client.

---

### **13. What are Pipes in Angular? How do you create a custom pipe?**
   **Answer:**
   - **Pipes** transform displayed data in the template. Examples: `date`, `currency`, `uppercase`.
   - To create a **custom pipe**, use the `@Pipe()` decorator and implement the `transform` method for custom transformation logic.

---

### **14. How does Angular work with TypeScript? Why is TypeScript important for Angular development?**
   **Answer:**
   - Angular is built with TypeScript, which provides **static typing**, **interfaces**, and **decorators** to improve code quality, reduce runtime errors, and enhance developer experience.
   - TypeScript makes Angular development more maintainable and readable by enforcing type safety.

---

### **15. How do you test Angular applications?**
   **Answer:**
   - **Karma**: A test runner that launches browsers and runs tests.
   - **Jasmine**: A testing framework used with Karma to write unit tests for Angular components and services.
   - Angular testing focuses on isolating components and services using mock data, `TestBed`, and dependency injection.

---
