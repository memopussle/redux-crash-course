## Documentation about Redux

### React-redux toolkit

```
npx create-react-app my-app --template redux
```

### Existing app

```
Existing App
npm install @reduxjs/toolkit react-redux

```

### @reduxjs/toolkit

- consists of few libraries

   - redux (core library, state management)
   - immer (allows to mutate state)
   - redux-thunk (handles async actions)
   - reselect (simplifies reducer functions)

### Extras

   - redux devtools
   - combine reducers

### react-redux

connects our app to redux

### Setup Store

- create store.js: store is like a whole entire state for your components

```js
import { configureStore } from '@reduxjs/toolkit';

export const store = configureStore({
  reducer: {},
});

```

### setup Provider

- index.js

```js
import React from 'react';
import ReactDOM from 'react-dom';
import './index.css';
import App from './App';
// import store and provider
import { store } from './store';
import { Provider } from 'react-redux';

ReactDOM.render(
  <React.StrictMode>
    <Provider store={store}>
      <App />
    </Provider>
  </React.StrictMode>,
  document.getElementById('root')
);
```
