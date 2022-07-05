# Senior Front End 1

1. [https://leetcode.com/](https://leetcode.com/)

2. What happens when you type [google.com](http://google.com/) into your browser's address box and press enter?" [https://github.com/alex/what-happens-when](https://github.com/alex/what-happens-when). From resolve DNS. Frontend is about browsers and receives response và parsing.

3. (function add(2)(3))[https://stackoverflow.com/questions/2272902/how-can-i-make-var-a-add23-5-work]

4. Implement add(2)(3)(4)..., for endless number of parameters -> [https://theanubhav.com/2019/02/03/js-currying-in-interview/](https://theanubhav.com/2019/02/03/js-currying-in-interview/)

5. JavaScript bundle is too much ==> optimize.

- minify?
- Webpack production mode double check
- Analyze bundle by tool webpack-bundle-analyzer. remove unused code.
- Code Splitting and Lazy Loading to modules
- Remove dead code from bundles via tree shaking.
- Cache assets - If your HTML is static and doesn't need to change on every request, caching can prevent it from being recreated unnecessarily
- Route users to a nearby CDN
- PWA - Service worker cache
- Lighthouse analyzing
- Define a performance budget
- if Angular might apply AOT, then it can remove @angular/compiler (1mb) before minify
- Alternative libraries, như thay momentjs bằng date-fns. Remove locale of moment libraries (if not use) with English version only. Choose tree-skakable library

1. Redux? when use it in your projects? [https://trungk18.com/experience/angular-jira-clone-tutorial-03-akita-state-management/](https://trungk18.com/experience/angular-jira-clone-tutorial-03-akita-state-management/) - Read state and do it by yourself

2. Css selector [https://www.w3schools.com/cssref/css_selectors.asp](https://www.w3schools.com/cssref/css_selectors.asp)

3. Hoisting, Promise, Async await, Callback. implement Promise.prototype.finally. Event loop, Lexical Scope, Execution Context. [https://github.com/lydiahallie/javascript-questions](https://github.com/lydiahallie/javascript-questions)

# **Front End React**

- How is the reconciliation works? (snapshot & diff).
- setState of class component # useState of function component.
- What is controlled & uncontrolled component ?
- lifecycle of useHooks?
- clean up function of hooks will render before or after the component re-rendering.
- What is memo?
- What is useCallback?
- What is useRef?
- What is Dynamic import ?
- What different the useSelector & mapStateTopProps? (redux)
- What different the Route component & Route render, Route Children render method (react router)
- làm sao để chỉ chạy effect ở lần render thứ 2 trở đi?

# Senior Front End 2

## **## Misc**

- What's your favorite browser, why?
- What are some other frameworks you have enjoyed working with?

## ## CSS

##

- Can you describe the difference between px, em, rem, vw, vh?
- What is your preferred method for using CSS in React?

- inline CSS, normal CSS, CSS in JS libraries, CSS Modules, Sass & SCSS, Less

## ## HTML

- Difference between cookie, sessionStorage and localStorage?
- Do you have experience with srcset image tag?

## ## React

- Basic overview of how React works?
- React’s name comes from reactive programming, can you explain this concept?
- What is the difference between state and props?
- What is your opinion about React functional components and class components
- How do you feel about React suspense?
- Difference between controlled and uncontrolled components?
- What is a ref in React?
- What is a higher order component?
- What is lifting up state?
- Why is setState() in React async instead of sync?
- What is your opinion about global state management?
- Nowadays the helper library called immer is often used with Redux, have you used this?
- Redux is very popular because we can test individual reducers, what does that mean?
- How do you feel about server side rendering?
- What are some of your favorite React libraries?
- What are some of the things you dislike about React?

## ## Testing

- What's the difference between unit tests and integrated testing?
- What does it mean when we mock something in a test?

## ## Javascript

- What's Babel's role in our development process?
- Deep copy vs shallow copy?

## ## Mobile

- Between Flutter and React Native, what do you prefer?Senior Front-End Developer

# Senior Front End 3

Interview Senior React FE

**HTML CSS**

Q: step by step of create a html file from design.
Q: CSS Box Model
Q: the different position relative, absolute
Q: min-width, max-width, width đi chung vs nhau nó sẽ như nào
Q: Difference between cookie, sessionStorage and localStorage?

3/ 5

**Javascript**

Q: Deep copy vs shallow copy?
Q: What is the difference between == and === in JS?
Q: event loop? (Marco tasks, micro tasks)
Q: promise chain?
Q: async, await ?

**React**
Q: virtual dom in react work? → ok
Q: What is controlled & uncontrolled component
Q: lifecycle of useHooks
Q: What is memo? Memo có mấy params
Q: What is useCallback?
Q: unit?
Q: MUI -material ui?
Q: css in js ? why should apply css in js
Q: how do variables in .env of CRA work?
Q: why should use key in react. Why should not use key by index of array for key? what if data doesn't have unique ?
Q: what is the difference between setState of class and function component? first is merge object, second is replace object. Why the second is replace state?
Q: How many ways to make component re-render?
Q: what is prop-drilling?
Q: what is react context? when and what is its disadvantage?

Q: how to create a dialog div at the same level with App. What is createPortal?

Q: What is implement of react error boundary?

Q: What is Axios interceptor?

**Redux**
Q: What is redux? What is thunk or saga? The difference between them?
Q: What different the useSelector & mapStateTopProps? (redux)

```

```
