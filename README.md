<h1 align="center">
  <a href="">
    <img src="/src/assets/poem-useLayoutEffect.svg" alt="Boiler Plate">
  </a>
</h1>

# Poetry in Motion - A Themed Poem Display with useLayoutEffect

This week, let's practice using the `useLayoutEffect` hook in our `App.jsx` file.

We will play with two themes, "light" and "dark", and each theme will have its own poem. Your job is to make a button that lets users switch between these themes. Changing the theme will also change the poem and the look of the page. This exercise will help you get better at choosing what to show based on the state, using React hooks to manage state, dealing with events, and using `useLayoutEffect` to handle side effects within the DOM layout :).

Let’s have fun coding!

## Getting Started with the Project

### Dependency Installation & Startup Development Server:

Once cloned, navigate to the project's root directory and this project uses npm (Node Package Manager) to manage its dependencies.

The command below is a combination of installing dependencies, opening up the project on VS Code and it will run a development server on your terminal.

```bash
npm i && code . && npm run dev
```

## Looking for some hints?

#### 1\. Initializing `useState` for 'theme'

- You can see that the reactive variable using the `useState` hook is already provided within the `App.jsx` file.

#### 2\. Utilizing `useLayoutEffect` Hook

- Implement the `useLayoutEffect` hook to manage the application of themes without causing flickering in the UI.
- Inside the `useLayoutEffect`, set the `className` of the `body` element to the current theme. This will allow you to apply global styles based on the theme.
- Ensure that the effect runs whenever the `theme` state changes by adding `theme` to the dependency array.

#### 3\. Crafting the `toggleTheme` Function

- Define a function named `toggleTheme` that will be responsible for switching between the "light" and "dark" themes.
- Within `toggleTheme`, use the setter function from `useState` to update the `theme` state based on its previous value. If it was "light", change it to "dark" and vice versa.
- Consider using a function within the setter to ensure you're toggling based on the accurate previous state.

#### 4\. Conditionally Rendering Elements in JSX

- In your JSX return statement, utilize curly braces `{}` to embed JavaScript expressions.
- Use ternary operators or logical AND `&&` operators to conditionally render elements or apply styles based on the `theme` state.
- For displaying the poems, consider using a condition to check the current theme and render the corresponding poem accordingly.
- To dynamically apply styles (like changing the color of text based on the theme), you might use inline styling with a condition to determine the style object.

#### 5\. Checking out the styles.css file

- body.light and body.dark are selectors that target the body element when it has the class of light or dark, respectively.
- background-color and color properties within each class define the background and text colors for the respective themes.
