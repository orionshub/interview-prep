### **1. What are React Hooks? Explain `useState` and `useEffect`.**
   **Answer:**
   - **React Hooks** let you use state and other React features in functional components.
   - **`useState`**: Allows you to add state to functional components.
     ```javascript
     const [count, setCount] = useState(0);
     ```
   - **`useEffect`**: Runs side effects like data fetching, subscriptions, or manually changing the DOM.
     ```javascript
     useEffect(() => {
       document.title = `Count is ${count}`;
     }, [count]); // Runs when 'count' changes
     ```

---

### **2. What is the difference between Class Components and Functional Components?**
   **Answer:**
   - **Class Components**: Use lifecycle methods (e.g., `componentDidMount`) and can manage state.
   - **Functional Components**: Simpler, stateless before Hooks. With **Hooks** (e.g., `useState`, `useEffect`), they can now manage state and side effects.

---

### **3. How is state management handled in React? What is the difference between Context API and Redux?**
   **Answer:**
   - **State Management** refers to managing the state of the application, including passing data between components.
   - **Context API**: Built-in way to pass data across components without prop drilling. Best for small-scale global state.
   - **Redux**: A state management library that uses a single store to manage the entire app's state. Best for large-scale, complex applications.

---

### **4. How do components communicate in React?**
   **Answer:**
   - **Props**: Passed from parent to child components to share data.
   - **Lifting State Up**: Moving shared state to the closest common ancestor component.
   - **Context API**: Provides global state without prop drilling.
   - **Event Callbacks**: Used in child components to pass data back to the parent.

---

### **5. What is the Virtual DOM in React?**
   **Answer:**
   - **Virtual DOM**: A lightweight copy of the real DOM. When the state changes, React calculates the difference between the new and old virtual DOM (diffing) and efficiently updates only the parts of the real DOM that changed, optimizing performance.

---

### **6. How does React Router work? What is a Single Page Application (SPA)?**
   **Answer:**
   - **React Router**: A library for client-side routing in React applications. It allows navigation between different components or pages without reloading the entire page.
   - **Single Page Application (SPA)**: An app where content is dynamically loaded as the user interacts, without full page reloads.

---

### **7. How do you optimize React applications for performance?**
   **Answer:**
   - **Lazy Loading**: Dynamically load components when needed using `React.lazy` and `Suspense`.
   - **Code Splitting**: Split the app into smaller chunks using tools like Webpack or dynamic `import()`.
   - **Memoization**: Use `React.memo` to prevent unnecessary re-renders, and `useMemo` or `useCallback` to memoize expensive functions or values.

---

### **8. What are Higher-Order Components (HOCs) and Render Props in React?**
   **Answer:**
   - **HOCs**: A function that takes a component and returns a new component with additional props or functionality.
     ```javascript
     const withLogging = (Component) => (props) => {
       console.log('Component rendered');
       return <Component {...props} />;
     };
     ```
   - **Render Props**: A technique for sharing code between components using a prop whose value is a function that controls rendering.
     ```javascript
     <DataFetcher render={(data) => <DisplayData data={data} />} />
     ```

---

### **9. What are Error Boundaries in React?**
   **Answer:**
   - **Error Boundaries** are components that catch JavaScript errors anywhere in their child component tree and display a fallback UI instead of crashing the app.
   - Implemented using `componentDidCatch` and `getDerivedStateFromError`.
     ```javascript
     class ErrorBoundary extends React.Component {
       state = { hasError: false };
       static getDerivedStateFromError() { return { hasError: true }; }
       componentDidCatch(error, info) { console.error(error, info); }
       render() { return this.state.hasError ? <ErrorFallback /> : this.props.children; }
     }
     ```

---

### **10. How do you handle forms in React? What is the difference between controlled and uncontrolled components?**
   **Answer:**
   - **Controlled Components**: Form data is handled by the React state. Every input change is reflected in the state.
     ```javascript
     const [name, setName] = useState('');
     <input value={name} onChange={(e) => setName(e.target.value)} />
     ```
   - **Uncontrolled Components**: Form data is handled by the DOM itself using refs to access form values.
     ```javascript
     const nameRef = useRef();
     <input ref={nameRef} />
     ```

---

### **11. What are Custom Hooks in React? Why are they useful?**
   **Answer:**
   - **Custom Hooks** are functions that reuse logic involving built-in hooks. They allow you to extract and share stateful logic between components.
   - Example: A custom hook for fetching data.
     ```javascript
     const useFetch = (url) => {
       const [data, setData] = useState(null);
       useEffect(() => { fetch(url).then(res => res.json()).then(setData); }, [url]);
       return data;
     };
     ```

---

### **12. What is JSX and how does it work?**
   **Answer:**
   - **JSX** is a syntax extension for JavaScript that looks similar to HTML. It allows you to write UI elements in JavaScript.
   - JSX gets compiled into `React.createElement` calls, which return JavaScript objects that represent the UI.

---

### **13. How do you use TypeScript with React?**
   **Answer:**
   - **TypeScript** adds static typing to React components. You can define types for props, state, and event handlers to make your code more predictable and reduce bugs.
     ```typescript
     interface ButtonProps { label: string; onClick: () => void; }
     const Button: React.FC<ButtonProps> = ({ label, onClick }) => (
       <button onClick={onClick}>{label}</button>
     );
     ```

---

### **14. How do you test React components?**
   **Answer:**
   - **Testing React Components** can be done using:
     - **Jest**: A testing framework for writing unit and integration tests.
     - **React Testing Library**: Used to test how components behave from a user’s perspective.
     - **Enzyme**: A utility for rendering and interacting with components (now less commonly used than React Testing Library).

---

### **15. What is a Micro Frontend, and how can React be used in a micro frontend architecture?**
   **Answer:**
   - **Micro Frontends** divide a large application into smaller, independently deployable apps or modules.
   - **React** can be used in a micro frontend setup by embedding React apps within a larger app, possibly using **single-spa** to manage multiple frameworks on the same page.

---
