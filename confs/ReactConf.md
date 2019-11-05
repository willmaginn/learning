# React Conf 2019

	Fun, informative and inclusive

## Summary
A professional and well excuted conference with space for meeting new people, learning new ideas and high quality talks.

## Talks to watch
- [Data Fetching With Suspense In Relay](https://www.youtube.com/watch?v=Tl0S7QkxFE4)
- [Building (And Re-Building) the Airbnb Design System](https://www.youtube.com/watch?v=fHQ1WSx41CA)
- [Building the New Facebook with React and Relay](https://www.youtube.com/watch?v=9JZHodNR184)
- Bonus: [Using React to make a Spaceship](https://www.youtube.com/watch?v=aV0uOPWHKt4)
- Bonus: [Building a Custom React Renderer](https://www.youtube.com/watch?v=CGpMlWVcHok)

## Tools / Resources
- https://codesandbox.io
- https://testingjavascript.com
- https://react-styleguidist.js.org
- https://atlaskit.atlassian.com
- https://www.wickeditor.com
- https://meemoo.org/
- https://observablehq.com/
- https://airflow.apache.org/

## Concepts

### SSR Suspense & Concurrent
https://reactjs.org/docs/concurrent-mode-suspense.html
https://reactjs.org/docs/concurrent-mode-intro.html

### Progressive Hydration / Selective hydration
Render as you read: 
* Top Left - Bottom Right

Selective hydration allows us to bring in the state for where we predict the user will be going next base on their mouse etc.

### Type checking end to end
https://github.com/contiamo/restful-react

### A/B Testing
```
const Feature = importCond('AB', 'Feature')

if (Feature) {
  Feature.use();
}
```

### Relay & flux
https://developers.facebook.com/videos/2019/building-the-new-facebookcom-with-react-graphql-and-relay/

### CSS-in-JS avec stylex
Reduces reused styles and helps styles to run in correct order!! 413kb -> 74kb
```
const styles = stylex.create({
  blue: {color: 'red'},
  red: {color: 'blue'},
});

<span className={ styles('blue','red')}>
```

### OLIO
https://apps.apple.com/us/app/olio/id1008237086
React based food exchange app

### Design system
https://github.com/airbnb/react-sketchapp

``` js
// BaseButton.jsx
const BaseButton = ({ styles }) => (
  <button {..css(styles.button)} >
    { children }
  <button />
)
```
``` js
export default extendable {BaseButton, 
  () = => ({
    button: {
      background: 'blue',
      color: 'white',
    },
  }),
}
```
``` js
// NewButton.jsx
export default extend { BaseButton, () => ({
		button: {
			background: 'grey',
			color: 'white',
		},
	})
}
``