[Link to codecademy lesson](https://www.codecademy.com/courses/react-101/lessons/the-effect-hook/exercises/rules-of-hooks)

The Effect Hook
Rules of Hooks
17 min
There are two main rules to keep in mind when using Hooks:

Only call Hooks at the top level.
Only call Hooks from React functions.
As we have been practicing with the State Hook and the Effect Hook, we’ve been following these rules with ease, but it is helpful to keep these two rules in mind as you take your new understanding of Hooks out into the wild and begin using more Hooks in your React applications.

When React builds the Virtual DOM, the library calls the functions that define our components over and over again as the user interacts with the user interface. React keeps track of the data and functions that we are managing with Hooks based on their order in the function component’s definition. For this reason, we always call our Hooks at the top level; we never call hooks inside of loops, conditions, or nested functions.

Instead of confusing React with code like this:

if (userName !== '') {
  useEffect(() => {
    localStorage.setItem('savedUserName', userName);
  });
}

We can accomplish the same goal while consistently calling our Hook every time:

useEffect(() => {
  if (userName !== '') {
    localStorage.setItem('savedUserName', userName);
  }
});

Secondly, Hooks can only be used in React Functions. We’ve been working with useState() and useEffect() in function components, and this is the most common use. The only other place where Hooks can be used is within custom hooks. Custom Hooks are incredibly useful for organizing and reusing stateful logic between function components.
