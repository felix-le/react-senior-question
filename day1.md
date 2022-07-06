# Q1: What is memo? How much paradigms does it have?

## 1. What is useMemo?

is a react Hook that we can use to wrap functions within a component. we can return memoized values and avoid re-rendering if the dependencies to a function have not changed. This is useful for expensive functions that we don’t want to re-run every time the component renders. => **use for functions in components, they will re-render if the dependencies change.**
it is a function that takes a function as an argument and returns a memoized version of that function.

```js
const memoizedValue = useMemo(() => computeExpensiveValue(a, b), [a, b]);
```

## 2. What is React.memo?

is a higher-order component that we can use to wrap components that we do not want to re-render unless their props change. **use for components.**
it has a parameter called areEqual. if the props of the component are equal, it will not re-render.

```js
function MyComponent(props) {
  /* render using props */
}
function areEqual(prevProps, nextProps) {
  /*
  return true if passing nextProps to render would return
  the same result as passing prevProps to render,
  otherwise return false
  */
}
export default React.memo(MyComponent, areEqual);
```

# Q: What is useCallback?

useCallback(fn, deps) is equivalent to useMemo(() => fn, deps).

```js
const memoizedCallback = useCallback(() => {
  doSomething(a, b);
}, [a, b]);
```

# Q: what is the difference between setState of class and function component?

While setState of class component is merge object, setState of function component is replace object.

# Q: How many ways to re-render a component?

There are three ways to re-render a component:

1. state change
2. re-rendering of the parent component
3. props change

# Q: what a higher-order component is

Concretely, a higher-order component is a function that takes a component and returns a new component. (React.memo, React.forwardRef, React.lazy, etc.)

# Q: What is React.forwardRef?

React.forwardRef creates a React component that forwards the ref attribute it receives to another component below in the tree. This technique is not very common but is particularly useful in two scenarios:

Forwarding refs to DOM components
Forwarding refs in higher-order-components
React.forwardRef accepts a rendering function as an argument. React will call this function with props and ref as two arguments. This function should return a React node.

```js
const FancyButton = React.forwardRef((props, ref) => (
  <button ref={ref} className='FancyButton'>
    {props.children}
  </button>
));

// You can now get a ref directly to the DOM button:
const ref = React.createRef();
<FancyButton ref={ref}>Click me!</FancyButton>;
```

In the above example, React passes a ref given to <FancyButton ref={ref}> element as a second argument to the rendering function inside the React.forwardRef call. This rendering function passes the ref to the

```js
<button ref={ref}>
```

element.

As a result, after React attaches the ref, ref.current will point directly to the `<button>` DOM element instance.

# Q: what is useRef?

useRef is a hook that lets you access the DOM node of a component. It returns a mutable ref object whose .current property is initialized to the DOM element that the component renders into.

```js
function TextInputWithFocusButton() {
  const inputEl = useRef(null);
  const onButtonClick = () => {
    // `current` points to the mounted text input element
    inputEl.current.focus();
  };
  return (
    <>
      <input ref={inputEl} type='text' />
      <button onClick={onButtonClick}>Focus the input</button>
    </>
  );
}
```

You might be familiar with refs primarily as a way to access the DOM. If you pass a ref object to React with <div ref={myRef} />, React will set its .current property to the corresponding DOM node whenever that node changes.

However, useRef() is useful for more than the ref attribute. It’s handy for keeping any mutable value around similar to how you’d use instance fields in classes.

This works because useRef() creates a plain JavaScript object. The only difference between useRef() and creating a {current: ...} object yourself is that useRef will give you the same ref object on every render.
