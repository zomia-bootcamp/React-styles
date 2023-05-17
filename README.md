# Beginner's Guide to React Styling


## Objectives

1. Understand the basics of React styling and its importance in creating visually appealing user interfaces.
2. Apply inline styling to React components using the `style` prop, modifying properties such as font size, margin, and color.
3. Define and utilize object variables to store CSS properties and values, allowing for more organized and reusable styles.
4. Apply object styling to React components, enhancing the visual appearance of elements such as buttons, text, and containers.
5. Comprehend the syntax used in React for inline and object styling, including the use of JSX and JavaScript objects.
6. Work with multiple style sheets, including CSS modules, to separate and manage styles in larger React projects.

## Preparation:
* Fork and clone this repository.
* Create a new branch called `training` for your work.
* Install the necessary dependencies using `npm install`.

React is a popular JavaScript library used for building user interfaces, and styling plays a crucial role in creating visually appealing web applications. In this article, we will explore the basics of styling in React, including inline and object styling, style syntax, and using multiple style sheets.

## Inline and Object Styling

In React, you can apply styles to your components using two main approaches: inline styling and object styling.

### Inline Styling

Inline styling involves directly adding CSS properties and values to the JSX elements within your components. Here's an example:

```jsx
import React from 'react';

const MyComponent = () => {
  return (
    <div style={{ color: 'red', fontSize: '20px' }}>
      This is a styled component!
    </div>
  );
};
```

### Group Activity: 

1. Take a look at the [`Game.js`](./src/Game.js) file. The game is already functional, but it needs some styling.
2. Start by practicing your understanding of inline styling.
3. Find the `<h1>` element responsible for the game's title, "Rock Paper Scissors".
4. Apply an inline style to change the font size property to 48 and set the margin top property to 0.

### Object Styling

Object styling allows you to define a separate JavaScript object that contains CSS properties and values. This approach provides a cleaner syntax and allows for dynamic styling. Here's an example:

```jsx
import React from 'react';

const styles = {
  container: {
    color: 'green',
    fontWeight: 'bold',
  },
};

const MyComponent = () => {
  return (
    <div style={styles.container}>
      This is a styled component!
    </div>
  );
};
```


### Group Activity: 

1. Next, let's define a few object variables to use for styling.
2. Above the `Game` component, create an object variable named `choiceStyles`.
3. Set the `choiceStyles` object with properties: `display` as `flex`, `align-items` as `center`, and `margin-bottom` as 40 pixels.
4. Define another object variable named `emojiStyles` with properties: `font-size` as 64 pixels and `margin-right` as 20 pixels.
5. Define an object variable named `nameStyles` with properties: `margin` as 0 pixels, `font-size` as 24 pixels, and `color` as #ffff.
6. Finally, define an object variable named `resultStyle` with properties: `margin-top` as 40 pixels, `font-size` as 48 pixels, and `color` as `#ffff`.

After defining the styling object, it's time to apply them:

1. Apply the `choiceStyles` to the surrounding `<div>` element of the player's choice.
2. Apply the `emojiStyles` to the `<span>` containing the player's emoji.
3. Apply the `emojiStyles` to the `<span>` containing Codey's emoji.
4. Apply the `nameStyles` to the `<p>` displaying the player's choice.
5. Apply the `nameStyles` to the `<p>` displaying Codey's choice.
6. Apply the `resultStyle` to the `<h2>` displaying the game result.


## Style Syntax

When it comes to writing styles in React, you can use the same syntax as regular CSS, including selectors, properties, and values. Here's an example:

```jsx
import React from 'react';

const MyComponent = () => {
  return (
    <div className="my-component">
      This is a styled component!
    </div>
  );
};
```

```css
.my-component {
  color: orange;
  background-color: yellow;
  padding: 10px;
}
```

## Multiple Style Sheets

In larger React applications, you may have multiple style sheets to organize your styles. To use multiple style sheets, you can leverage CSS modules, CSS-in-JS libraries, or simply import multiple style sheets into your components. Here's an example using separate style sheet files:

```jsx
import React from 'react';
import './styles.css';
import './other-styles.css';

const MyComponent = () => {
  return (
    <div className="my-component">
      This is a styled component!
    </div>
  );
};
```

### Group Activity: 

1. Open the `Game.module.css` file to see the predefined styles.
2. Import the CSS module into an object named `styles`.
3. Go back to `Game.js` and apply the `.container` styles to the first `<div>` after the return statement.
4. Apply the `.choices` styles to the `<div>` containing the rock, paper, and scissors buttons.
5. Apply the `.results` styles to the `<div>` containing the game's results.
6. Apply the `.button` styles to the "Play Again" button and each choice button.


## Conclusion

Styling is an essential aspect of building engaging React applications. In this article, we covered the basics of inline and object styling, explored the style syntax, and discussed using multiple style sheets. By mastering these concepts, you'll be well on your way to creating visually stunning user interfaces with React!

Remember, practice is key, so keep experimenting with different styling techniques and try out various CSS properties to enhance the appearance of your React components. Happy coding!



