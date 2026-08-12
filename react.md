# REACT QUESTIONS

## 01. What is React and what problem does it solve?

React is an open-source JavaScript library developed by Facebook for building fast, interactive, and reusable user interfaces, especially for single-page applications. It uses a component-based architecture, which allows developers to build reusable UI components. React also uses a Virtual DOM to efficiently update the user interface, improving performance and providing a better user experience.
Key Points
• React is an open-source JavaScript library.
• Developed by Facebook (Meta).
• Used for building interactive user interfaces.
• Uses component-based architecture.
• Uses Virtual DOM for better performance.

## 02. Why is React called a library instead of a framework?

React is called a library because it mainly focuses on building the user interface. It doesn't provide a complete solution for application development. For features like routing, state management, or API handling, developers choose additional libraries such as React Router, Redux, or Axios.
A framework, on the other hand, provides a complete structure and includes many built-in features. It usually controls how an application is organized, whereas React gives developers the flexibility to choose the tools they need.

## 03. Can you give some examples of libraries used with React?

Yes. For example, React Router for routing, Redux or Zustand for state management, Axios for API requests, and React Query or TanStack Query for server state management.

## 04. Is Next.js a framework?

Yes. Next.js is a React framework because it provides additional features like file-based routing, server-side rendering, API routes, image optimization, and many built-in capabilities.

## 05. So, is React enough to build a complete application?

Yes, React can be used to build an application, but for most real-world projects, developers use additional libraries or a framework like Next.js to handle features such as routing, server-side rendering, and state management.

## 06. Why do you use React instead of Vanilla JavaScript?

React is built on top of JavaScript, so it's not a replacement for JavaScript. We use React because it makes building complex and interactive user interfaces much easier.
React provides reusable components, efficient UI updates through the Virtual DOM, declarative programming, and a large ecosystem. These features make applications easier to develop, maintain, and scale compared to using only Vanilla JavaScript.
Key Points
• React doesn't replace JavaScript.
• Makes UI development easier.
• Reusable Components.
• Virtual DOM.
• Declarative programming.
• Easier maintenance.
• Better scalability.

## 07. Can we build websites using only Vanilla JavaScript?

Yes. We can build websites using only Vanilla JavaScript. However, as applications become larger and more interactive, managing the code becomes more difficult. React helps solve that problem by providing reusable components and better state management.

## 08. When would you choose Vanilla JavaScript?

For small websites or simple projects, Vanilla JavaScript is often enough. For larger applications with many interactive features, React is usually a better choice because it's easier to maintain and scale.

## 09. What is the Virtual DOM, and how does it improve performance?

The Virtual DOM is a lightweight copy of the Real DOM maintained by React. Whenever the application's state changes, React first updates the Virtual DOM instead of directly updating the Real DOM. It then compares the new Virtual DOM with the previous one, identifies only the changed elements, and updates only those parts in the Real DOM. This process is called reconciliation, and it improves performance by reducing unnecessary DOM updates.
Key Points
• Virtual DOM = lightweight copy of the Real DOM.
• React updates the Virtual DOM first.
• React compares the old and new Virtual DOM.
• This comparison is called Reconciliation.
• Only the changed parts are updated in the Real DOM.
• Fewer DOM updates = better performance.

## 10. What is Reconciliation?

Reconciliation is the process where React compares the previous Virtual DOM with the updated Virtual DOM to identify changes and efficiently update only the necessary parts of the Real DOM.

## 11. What are Components? What are the different types of Components?

Components are the building blocks of a React application. A component is a reusable piece of UI that contains its own structure, logic, and styling. Instead of writing the same code multiple times, we create components and reuse them throughout the application.
There are two main types of components: Functional Components and Class Components. Today, Functional Components are the recommended approach because they are simpler, easier to read, and support React Hooks. Class Components were commonly used before Hooks were introduced but are now less common in modern React development.
Key Points
• Components are building blocks of React.
• Components are reusable.
• Improve code organization.
• Improve maintainability.
• Two types:
o Functional Components
o Class Components
• Functional Components are preferred today because they support Hooks.

## 12. What is the difference between functional and class components?

Functional components are regular JavaScript functions. They return JSX and can use Hooks like useState and useEffect.

Class components are JavaScript classes. They use this.state and lifecycle methods such as componentDidMount and componentWillUnmount to manage state and component behavior.

In modern React, functional components are preferred. They are simpler and easier to maintain.

## 12. What is the difference between Props and State?

Props and State are both used to manage data in React, but they serve different purposes.
Props are used to pass data from a parent component to a child component. They are read-only, which means a child component cannot modify the props it receives.
State, on the other hand, is managed within a component. It stores data that can change over time, and when the state changes, React automatically re-renders the component to update the user interface.
Props are used for communication between components, while state is used to manage dynamic data inside a component.
Key Points
• Both store data.
• Props = Parent ➜ Child.
• Props are read-only.
• State belongs to the component.
• State can change.
• State updates cause re-render.

## 13. Why are props read-only?

Because React follows one-way data flow. Keeping props read-only makes data predictable and easier to manage.

## 14. What is a Hook?

Hooks are special functions introduced in React 16.8 that allow Functional Components to use React features such as state, lifecycle methods, and other React functionalities without writing Class Components. Hooks make code simpler, more reusable, and easier to maintain.
Key Points
• Hooks are special React functions.
• Introduced in React 16.8.
• Used in Functional Components.
• Allow us to use React features like:
o State
o Side Effects
o Refs
• Replace the need for Class Components in most cases.

## 15. What are Lifecycle Methods?

Lifecycle methods are special methods in React Class Components that allow developers to run code at different stages of a component's life, such as when it is created, updated, or removed from the screen. Before React Hooks were introduced, lifecycle methods were commonly used for tasks like fetching data, updating the DOM, and cleaning up resources. In modern React, these tasks are usually handled using the useEffect Hook.
Key Points
• Lifecycle methods exist in Class Components.
• They run during different phases of a component's life.
• Three phases:
o Mounting
o Updating
o Unmounting
• Modern React uses useEffect instead of lifecycle methods.

## 16. Why don't we use lifecycle methods anymore?

Because modern React mainly uses Functional Components with Hooks. The useEffect Hook replaces most lifecycle methods while making the code simpler and easier to maintain.

## 17. How does useEffect replace Lifecycle Methods?

useEffect is a React Hook that allows Functional Components to perform side effects. Depending on how it's used, it can behave like different lifecycle methods in Class Components.
With an empty dependency array ([]), it runs once after the component mounts, similar to componentDidMount().
With dependencies, it runs whenever those values change, similar to componentDidUpdate().
And by returning a cleanup function, it runs before the component unmounts, similar to componentWillUnmount().
This is why useEffect is considered a replacement for most lifecycle methods in modern React.
Key Points
• useEffect replaces most lifecycle methods.
• [] → Runs once after mounting.
• [dependency] → Runs when dependency changes.
• return () => {} → Cleanup before unmounting.
• Used for API calls, event listeners, timers, subscriptions, etc.

## 18. Why is the cleanup function important?

The cleanup function prevents memory leaks by removing event listeners, clearing timers, or unsubscribing from services before the component is unmounted.

## 19. Can one useEffect replace all lifecycle methods?

It replaces most common lifecycle methods like componentDidMount, componentDidUpdate, and componentWillUnmount. However, some advanced lifecycle methods don't have a direct equivalent, but they are rarely needed in modern React.

## 20. What is a Memory Leak?

A memory leak happens when an application continues to hold onto memory that is no longer needed. In React, this usually occurs when resources like timers, event listeners, or subscriptions are not cleaned up after a component is removed. Over time, these unused resources consume memory, which can reduce performance or even cause the application to crash. We can prevent memory leaks by using the cleanup function inside useEffect

## 21. What are the rules of Hooks?

Hooks should only be called at the top level of a Functional Component or inside a custom Hook. They should not be called inside loops, conditions, or nested functions.

## 22. What is useState hook?

useState is a React Hook that allows functional components to manage state. It lets us store dynamic data inside a component, such as user input, button clicks, or fetched data. When the state changes using its setter function, React automatically re-renders the component to update the user interface.

## 23. Why do we use useState?

We use useState to store and update dynamic data inside a functional component. It allows React to automatically update the UI whenever the state changes.

## 24. Why don't we update state directly?

React only knows that the state has changed when we use the setter function. Directly modifying the state won't trigger a re-render, so the UI won't update correctly.

## 25. What is useEffect?

useEffect is a React Hook that allows Functional Components to perform side effects. Side effects are operations that interact with the outside world or happen outside the normal rendering process, such as fetching data from an API, setting timers, adding event listeners, or updating the document title. By default, useEffect runs after the component renders, and its behavior can be controlled using the dependency array.
Key Points
• useEffect is a React Hook.
• Used for side effects.
• Runs after rendering.
• Dependency array controls when it runs.
• Cleanup function prevents memory leaks.

## 26. What are side effects?

Side effects are operations that interact with the outside world or happen outside the normal rendering process, such as API calls, timers, event listeners, subscriptions, or updating the document title.

## 27. When does useEffect run?

By default, it runs after the component renders. The dependency array determines whether it runs once, after every render, or only when specific values change.

## 28. If a component has multiple useEffect Hooks, do they run at the same time or one after another?

If a component has multiple useEffect Hooks, React executes them one after another in the order they are declared in the component. They do not run simultaneously. After React finishes rendering the component and updates the DOM, it executes the first useEffect, then the second, then the third.

## 29. Why use multiple useEffect Hooks instead of one?

Using multiple useEffect Hooks keeps different side effects separate. For example, one effect can fetch data while another updates the document title. This makes the code cleaner, easier to read, and easier to maintain.

## 30. What is useRef?

useRef is a React Hook that is used to create a mutable reference that persists across component re-renders. It is commonly used to access DOM elements directly or store values that should not trigger a component re-render when they change.

## 31. Can changing ref.current re-render the component?

No. Updating ref.current does not trigger a re-render.

## 32. What is the .current property?

current is the property that stores the current value or the referenced DOM element.

## 33. When would you use useState and when would you use useRef?

useState is used when changing a value should update the UI. useRef is used when I need to persist a value or access a DOM element without triggering a re-render.

## 34. What is JSX?##

JSX stands for JavaScript XML. It is a syntax extension for JavaScript that allows developers to write HTML-like code inside JavaScript. JSX makes React components easier to read and write. Although it looks like HTML, browsers cannot understand JSX directly. It is transpiled into regular JavaScript using tools like Babel before the code runs in the browser.

## 35. Why do we use className instead of class?

class is a reserved keyword in JavaScript, so JSX uses className to define CSS classes.

## 36. What is Conditional Rendering in React?

Conditional Rendering is a technique in React that allows us to display different UI elements based on a condition. Instead of always rendering the same content, React can render different components or elements depending on the application's state or props. Common ways to implement conditional rendering include the if statement, ternary operator (? :), logical AND (&&), and early return.

## 37. Which method do you prefer?

For simple conditions, I usually use the ternary operator or &&. For more complex logic, I prefer an if statement or an early return because they improve readability.

## 38. When do you use && instead of a ternary?

&& is useful when I only need to render something if a condition is true. If I need an else case, I use the ternary operator.

## 39. Can we use normal JavaScript if inside JSX?

No. We can't write an if statement directly inside JSX because JSX expects expressions, not statements. Because JSX expressions must evaluate to a single value. An if statement controls the flow of execution but doesn't itself produce a value, so it can't be placed where an expression is expected. However, we can use a ternary operator or move the if statement outside the JSX.

## 40. What is the key prop, and why is it important?

The key prop is a special attribute in React that helps React uniquely identify elements in a list. When rendering lists using the map() method, each element should have a unique key. This allows React to efficiently determine which items have been added, removed, or updated, improving rendering performance and preventing unnecessary re-renders

## 41. Why shouldn't we use the array index as the key?

Because if items are inserted, removed, or reordered, their indexes change. React may incorrectly reuse components, which can lead to incorrect UI updates or loss of component state. A stable unique ID is a better choice.

## 42. What causes a React component to re-render?

A React component re-renders whenever its state changes, its props change, or its parent component re-renders. During a re-render, React creates a new Virtual DOM, compares it with the previous Virtual DOM through the reconciliation process, and updates only the parts of the Real DOM that have changed

## 43. Can React re-render without updating the Real DOM?

Yes. React may re-render a component and create a new Virtual DOM, but if nothing has actually changed after reconciliation, it won't update the Real DOM

## 44. What is React.memo?

React.memo is a higher-order component that helps optimize performance by preventing unnecessary re-renders of a functional component. It compares the component's props with the previous props, and if they haven't changed, React reuses the previous rendered result instead of rendering the component again.

## 45. Does React.memo compare state?

No. React.memo only compares props. If the component's own state changes, it will still re-render.

## 46. Should we wrap every component with React.memo?

No. React.memo itself performs prop comparisons, which also has a cost. It's most useful for components that render frequently and are expensive to render.

## 47. What are Controlled and Uncontrolled Components?

Controlled and Uncontrolled Components are two ways of handling form inputs in React.
In a Controlled Component, React manages the input's value using state. The input value is controlled by React, and every change updates the component's state.
In an Uncontrolled Component, the input manages its own state internally, and React accesses its value using a ref when needed.
Key Points
• Controlled → React controls the input using useState.
• Uncontrolled → DOM controls the input using useRef.
• Controlled updates state on every change.
• Uncontrolled reads the value only when needed.
• Controlled is preferred for most React applications.

## 48. Which one do you prefer?

In most cases, I prefer Controlled Components because they make validation, form handling, and dynamic UI updates much easier. I use Uncontrolled Components only when I don't need React to track every input change

## 49. Why is <input type="file"> usually uncontrolled?

Because browsers don't allow JavaScript to directly control the value of a file input for security reasons. If JavaScript could do this, then a malicious website could select files from your computer without your permission, upload them to its server, steal your private documents, photos, or passwords. That would be a huge security risk.

## 50. What is Context API, and why do we use it?

The Context API is a built-in React feature that allows us to share data between multiple components without passing props through every intermediate component. It is mainly used to avoid prop drilling and make state sharing easier across the component tree. Common use cases include authentication, theme switching, language settings, and user information.

## 51. What is Prop Drilling?

Prop drilling is the process of passing props through multiple intermediate components, even though those components don't use the data themselves. It makes the code harder to maintain and is one of the main problems that Context API helps solve.

## 52. Does Context API replace Redux?

Not completely. Context API is suitable for sharing simple global state like themes or authentication. For large applications with complex state management, tools like Redux or Zustand provide more advanced features and better scalability.

## 53. Why do we need Redux when we have useState?

useState is designed for managing local state within a single component, while Redux is used for managing global state that needs to be shared across many components. As an application grows, passing state through multiple components becomes difficult to maintain. Redux provides a centralized store where the application's shared state is managed in a predictable and organized way.

Q31. What is React and what problem does it solve?
Q32. What is JSX and why is it used in React?
Q33. What is the difference between functional and class components?
Q34. What is the virtual DOM and how does React use it?
Q35. Explain the useState hook with an example.
Q36. What is the useEffect hook and what are its use cases?
Q37. What is the difference between controlled and uncontrolled components?
Q38. What are props in React and how are they passed?
Q39. What is prop drilling and how can it be avoided?
Q40. Explain the useContext hook with an example.
Q41. What is the useRef hook and when would you use it?
Q42. What are React keys and why are they important in lists?
Q43. What is the difference between state and props?
Q44. How does conditional rendering work in React?
Q45. What is React.memo and when should you use it? 

Q46. What is the useReducer hook and when is it preferred over useState?
Q47. Explain the useMemo hook and give a use case.
Q48. What is the useCallback hook and when do you use it?
Q49. What is React Router and how do you set up client-side routing?
Q50. What is the difference between useNavigate and Link in React Router?
Q51. What are custom hooks in React? Write a simple example.
Q52. What is lazy loading in React and how is it implemented?
Q53. What are React error boundaries and why are they useful?
Q54. What is the Context API and when should you use Redux instead?
Q55. Explain the concept of reconciliation in React.
Q56. What is the difference between React.Fragment and empty tags (<>)?
Q57. How do you handle forms in React? Explain with Formik or react-hook-form.
Q58. What is code splitting in React and how does it improve performance?
Q59. What are portals in React and when are they useful?
Q60. Explain the lifecycle of a React functional component with hooks.