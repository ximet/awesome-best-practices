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
        },
    ```
    Now we have problem with alias in webpack 2 see [issue](https://github.com/webpack/webpack/issues/4160#issuecomment-281236136)

***
- #### Keep your state as flat as possible.
   If need help with them (with flat state), you may use: [normalizr](https://github.com/paularmstrong/normalizr)

***

- #### One-way binding
   Need create data flows in one direction with some change.

***

- #### Use Redux.
   Redux is a predictable state container for JavaScript apps.
   If you need more information you should check out [Redux](https://github.com/reactjs/redux) and Dan Abramov's course [Getting Started with Redux](https://egghead.io/courses/getting-started-with-redux)

***




___
## Video link with best practices:

1. [Pete Hunt: React - Rethinking Best Practices (updated) - JSConf.Asia 2013](https://www.youtube.com/watch?v=DgVS-zXgMTk) - 30 Oct. 2013
2. [Styling React Components in JavaScript](https://www.youtube.com/watch?v=0aBv8dsZs84) - 4 Dec. 2015
3. [HelsinkiJS June 2016 - Christoffer Niska - React best practices](https://www.youtube.com/watch?v=qtpRiGifpvY) - 18 Jun. 2016
4. [Netflix JavaScript Talks - React plus X: Best Practices for Reusable UI Components](https://www.youtube.com/watch?v=Yy7gFgETp0o) - 15 Sep. 2016
5. [ReactiveConf 2016 - Max Stoiber: Styled-components: Enforcing best practices](https://www.youtube.com/watch?v=jaqDA7Btm3c) - 25 Nov. 2016
