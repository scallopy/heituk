This project was bootstrapped with [Create React App](https://github.com/facebook/create-react-app).

# Building the React app

- Components: https://blog.logrocket.com/creating-an-app-with-react-and-django/
    - Header.js
    - NewUserForm.js
    In the first lines, we’re importing the reactstrap components for the first
    time including Form, Button, etc, which will comprise our form.

    Then, we created our `state` object with the corresponding properties of our
    User’s model. This is going to be useful to manipulate each prop
    individually.

    The `componentDidMount` function will run after the component finishes its
    startup, so we can recover the user’s props from the parent component
    (`this.props`) here, and set the state with them (if they exist, for the
    editing scenario.)

    The `onChange` function will handle the update of each state’s prop with the
    current value typed in each respective field

    The `createUser` function will deal with the HTTP POST requests of our
    form. Every time we press the submit button, this function will be called,
    triggering the axios’ `post()` function and passing the current state in the
    request’s `body`. Once it’s completed, we’ll call the `props` functions
    `resetState` (to refresh the table) and `toggle` (to close the modal), they’ll
    be created further

    `editUser` function works almost like the previous one, but calling our
    PUT operation

    The `defaultIfEmpty` function was created as an auxiliary function that’ll
    check the current value of each field in order to determine if they’re
    going to be filled with the value of the state (in case any exists, for
    editing) or not (when creating a new user)

    The `render` function will just compose our form with the help of reactstrap
    components. Nothing special here, except for the onSubmit property, which
    checks for a props’ property called users: if it does exist, the submit
    function will be for editing (the value was passed by the parent
    component); otherwise, it’s for creation.

    - NewUserModal.js
    - UserList.js
    - ConfirmRemovalModal.js
    - Home.js


## Available Scripts

In the project directory, you can run:

### `npm start`

Runs the app in the development mode.<br />
Open [http://localhost:3000](http://localhost:3000) to view it in the browser.

The page will reload if you make edits.<br />
You will also see any lint errors in the console.

### `npm test`

Launches the test runner in the interactive watch mode.<br />
See the section about [running tests](https://facebook.github.io/create-react-app/docs/running-tests) for more information.

### `npm run build`

Builds the app for production to the `build` folder.<br />
It correctly bundles React in production mode and optimizes the build for the best performance.

The build is minified and the filenames include the hashes.<br />
Your app is ready to be deployed!

See the section about [deployment](https://facebook.github.io/create-react-app/docs/deployment) for more information.

### `npm run eject`

**Note: this is a one-way operation. Once you `eject`, you can’t go back!**

If you aren’t satisfied with the build tool and configuration choices, you can `eject` at any time. This command will remove the single build dependency from your project.

Instead, it will copy all the configuration files and the transitive dependencies (webpack, Babel, ESLint, etc) right into your project so you have full control over them. All of the commands except `eject` will still work, but they will point to the copied scripts so you can tweak them. At this point you’re on your own.

You don’t have to ever use `eject`. The curated feature set is suitable for small and middle deployments, and you shouldn’t feel obligated to use this feature. However we understand that this tool wouldn’t be useful if you couldn’t customize it when you are ready for it.

## Learn More

You can learn more in the [Create React App documentation](https://facebook.github.io/create-react-app/docs/getting-started).

To learn React, check out the [React documentation](https://reactjs.org/).

### Code Splitting

This section has moved here: https://facebook.github.io/create-react-app/docs/code-splitting

### Analyzing the Bundle Size

This section has moved here: https://facebook.github.io/create-react-app/docs/analyzing-the-bundle-size

### Making a Progressive Web App

This section has moved here: https://facebook.github.io/create-react-app/docs/making-a-progressive-web-app

### Advanced Configuration

This section has moved here: https://facebook.github.io/create-react-app/docs/advanced-configuration

### Deployment

This section has moved here: https://facebook.github.io/create-react-app/docs/deployment

### `npm run build` fails to minify

This section has moved here: https://facebook.github.io/create-react-app/docs/troubleshooting#npm-run-build-fails-to-minify
