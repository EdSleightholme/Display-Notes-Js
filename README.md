# Available Scripts / How to run the app

## Quick Start

Navigate in cmd to this directory and `npm i` and then `npm run start`

In the project directory, you can run:

### `yarn start`

Runs the app in the development mode.\
Open [http://localhost:3000](http://localhost:3000) to view it in the browser.

The page will reload if you make edits.\
You will also see any lint errors in the console.

### `yarn test`

Launches the test runner in the interactive watch mode.\
See the section about [running tests](https://facebook.github.io/create-react-app/docs/running-tests) for more information.

### `yarn build`

Builds the app for production to the `build` folder.\
It correctly bundles React in production mode and optimizes the build for the best performance.

The build is minified and the filenames include the hashes.\
Your app is ready to be deployed!

See the section about [deployment](https://facebook.github.io/create-react-app/docs/deployment) for more information.

### `yarn eject`

**Note: this is a one-way operation. Once you `eject`, you can’t go back!**

If you aren’t satisfied with the build tool and configuration choices, you can `eject` at any time. This command will remove the single build dependency from your project.

Instead, it will copy all the configuration files and the transitive dependencies (webpack, Babel, ESLint, etc) right into your project so you have full control over them. All of the commands except `eject` will still work, but they will point to the copied scripts so you can tweak them. At this point you’re on your own.

You don’t have to ever use `eject`. The curated feature set is suitable for small and middle deployments, and you shouldn’t feel obligated to use this feature. However we understand that this tool wouldn’t be useful if you couldn’t customize it when you are ready for it.

## Learn More

You can learn more in the [Create React App documentation](https://facebook.github.io/create-react-app/docs/getting-started).

To learn React, check out the [React documentation](https://reactjs.org/).

# TASK Front-end Technical Test

Build a simple web application that renders a series of articles along with info about the author and comments. You can find sample data in `data.json`, however keep in mind this needs to scale to a much larger dataset. If you're applying for a full stack position and/or want to show off your back end skills as well, also build a simple Node server to serve the data, otherwise you can just bundle the data with the UI code.

* You **must** use JavaScript and React
* The solution **should** seamlessly scale to millions of records
* You **can** use any other technology you like
* Make it yours - you can write unit tests, documentation, build fancy graphics, use animations etc - anything you like
* There is no time limit, however we expect to get something back within a few days


# Review of Task
To complete this task I have gone for a simple webpage which loads the the JSON file and displays the results


## Overview of the files
App.css contains all styles used by the webpage

App.jsx contains the methods for loading in the json files data. Also it contains the pages header and how the topics are displayed

Topic.jsx contains how a single topic will be rendered with its comments


## Overview of data types

On load of JSON file comments are combined with their associated topics so that they become one continuous data type.  
Users are loaded as they are found in the JSON file.

## Added Extras

A textbox can be found in the header that filters the topics by name. It also disallows you from entering special characters.  
Also i have added responses on the UI if their are no topics to render and if the topics have yet to load to the page  


## Further Work
Currently this should display results from the the file in theory until the json is to big to be loaded by memory. A solution to this this would be to page out the results as to reduce the amount of records shown at once. This would most simply be done by creating a API that has that functionality. 

Another issue is topics with high number of comments can be cumbersome to display. A filter tool could be added similar to the current way topics are filtered. Though another method would be better as a text box their does not seem like a appropriate approach.

Also their is room for tests to be added. Especially around the textbox input.