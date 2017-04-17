# React Best Practices
- #### Create reusable component
   (better without mutation)
   It should encapsulate the smallest element possible that can potentially be reused.

 ***

- #### Create composable component
     Not need create the same component with small changes or component with hard structure. Better think about how create composable component.
 ***

- #### Importing components without relative paths
    If you use webpack, use setting resolve.alias

    ```javascript
        //for example
        resolve: {
            modules: [path.resolve('./node_modules')],
            alias: {
                Components: path.resolve(__dirname, '../../../../ui-component/component')
            },
            extensions: ['.js', '.jsx', '.json', '.scss']
        }
    ```
    Now we have problem with alias in webpack 2 see [issue](https://github.com/webpack/webpack/issues/4160#issuecomment-281236136)
***
- #### Create functional component
  ```javascript
      //for example
      const MyComponent = props => (
        <div className={props.className}/>
      );
  ```
  Functional component have a few limitations:
    - cannot have a ref
    - cannot have state

***

- #### Use PureComponent, avoiding impure component
   A pure component is a React component whose render function is pure (after changes in props or state). The default behavior in React is to always re-render the entire component tree, even if props/state do not change.
***

- #### Keep your state as flat as possible.
   If need help with them (with flat state), you may use: [normalizr](https://github.com/paularmstrong/normalizr)

***

- #### One-way binding
   Need create data flows in one direction with some change.

***

- #### Delete unneeded state
   Try to think about refactoring your component classes to not create unneeded state.

   Always remember about the single source of truth principle - it can make your component classes simpler to write and maintain.

***

- #### State in component is an Anti-Pattern
   Need create Pure, only side effect component. Better use stateless component
***

- #### Use Redux.
   Redux is a predictable state container for JavaScript apps.
   If you need more information you should check out [Redux](https://github.com/reactjs/redux) and Dan Abramov's course [Getting Started with Redux](https://egghead.io/courses/getting-started-with-redux)

***

- #### Use check type
   Add a bit more type safety to our components.
   But in React 15.5 propTypes deleted. You may use a few variants:
    - Use [propTypes](https://github.com/reactjs/prop-types) - need install lib after version 15.5 :blush:
    - Use [Flow](https://flow.org/)

***

- #### Use Immutable structure
   - [Immutable.js](https://github.com/facebook/immutable-js) - most popular implementations of immutable data structures.

   - [Seamless Immutable](https://github.com/rtfeldman/seamless-immutable) - project is a much lighter-weight solution that uses normal JavaScript objects.

   - Hard way (use native JS with unit tests with [deep-freeze-node](https://www.npmjs.com/package/deep-freeze-node))

   ```javascript
       //for example
       return {  
          ...state,
          foo
        }

        return firstArray.concat(secondArray)  
   ```

***

- #### Think about reactive\observable solutions
   React is not reactive lib, but can become
    - [MobX](https://github.com/mobxjs/mobx) - Simple, scalable state management
    - [Cycle JS](https://cycle.js.org/) - A functional and reactive JavaScript framework
    - [redux-rx](https://github.com/acdlite/redux-rx) - RxJS utilities for Redux.

***


___
## Video link with best practices:

1. [Pete Hunt: React - Rethinking Best Practices (updated) - JSConf.Asia 2013](https://www.youtube.com/watch?v=DgVS-zXgMTk) - 30 Oct. 2013
2. [Styling React Components in JavaScript](https://www.youtube.com/watch?v=0aBv8dsZs84) - 4 Dec. 2015
3. [HelsinkiJS June 2016 - Christoffer Niska - React best practices](https://www.youtube.com/watch?v=qtpRiGifpvY) - 18 Jun. 2016
4. [Netflix JavaScript Talks - React plus X: Best Practices for Reusable UI Components](https://www.youtube.com/watch?v=Yy7gFgETp0o) - 15 Sep. 2016
5. [ReactiveConf 2016 - Max Stoiber: Styled-components: Enforcing best practices](https://www.youtube.com/watch?v=jaqDA7Btm3c) - 25 Nov. 2016
