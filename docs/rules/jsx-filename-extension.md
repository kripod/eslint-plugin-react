# Restrict file extensions that may contain JSX (react/jsx-filename-extension)

## Rule Details

The following pattern is considered a warning:

```jsx
// filename: MyComponent.js
function MyComponent() {
  return <div />;
}
```

The following pattern is **not** considered a warning:

```jsx
// filename: MyComponent.jsx
function MyComponent() {
  return <div />;
}
```

## Rule Options

The set of allowed extensions is configurable. By default '.jsx' and '.tsx' are allowed. If you wanted to allow '.js' and '.ts' alongside the defaults, the configuration would be:

```js
"rules": {
  "react/jsx-filename-extension": [1, { "extensions": [".js", ".jsx", ".ts", ".tsx"] }]
}
```

## When Not To Use It

If you don't care about restricting the file extensions that may contain JSX.
