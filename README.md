# Te doen

Just exploring Svelte, stores and contexts with a cliché todo app. [Site](https://svelte-another-todo-thingy.vercel.app/)

27.4kB shipped over the wire, 43.3kB loaded

**Findings**

- Stores are just awesome, such a useful/powerful out of the box approach for state management
- The need to specify a key for the context feels like a step too much, feels like could be done by Svelte itself
- Transitions/animation are nice features that come with Svelte, however there is still an issue that I came across. Transitions in if/else blocks are having (logic) unwanted behaviour https://github.com/sveltejs/svelte/issues/544
- `animate` should be directly used in an each block otherwise you'll get: `
An element that uses the animate directive must be the immediate child of a keyed each blocksvelte(invalid-animation)`
So putting these animations in a Svelte components is impossible at the moment. So you'll have to write your Svelte "component" directly inside your parent component. Or move it to a Svelte component and wrap it with a native dom element inside the each block.  

