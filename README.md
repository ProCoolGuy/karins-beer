# Karin's Beer - React Assessment

Welcome! Thank you for taking the time to do this coding assessment. Please read the guidelines before getting started.

Assessment starter can be found here: [Karin's Beer Assessment Github](https://github.com/alocke12992/karins_beer)

## Get started
[Fork the repo](https://github.com/alocke12992/karins_beer)
Once you've cloned the repo locally, run `yarn` to install required packages.
Run `yarn start` to launch the project on `http://localhost:3000`

## Assessment Guidelines:

*   The purpose of this assessment is to help us evaluate your client side application development coding skills.
*   You are allowed to use any non-human resource. Ex:
    *   **Allowed:** StackOverflow, Google, Old Code, Etc...
    *   **Not Allowed:** Speaking with anyone that has coding knowledge or is in the Technology field.
*   Check out the API index below.
*   Don't be overwhelmed. We intentionally included more steps than you are likely to complete in your given time frame. Try to do them in order, but you can skip steps if you get stuck. If you skip a feature, put in the notes as to why you skipped it.
*   Please try to commit often and add messages to your commits so we can more easily review your work.
*   We added more steps than we expect you to finish. Don't be overwhelmed and get as far as you can in the time you have. We will take into account the time amount of time you took, the amount of experience you have in React, the difficulty of the UI library you use etc.
    
*   IMPORTANT: You will need to obtain an API key to access the API. Please reach out to Andrew for this key.
    
*   HINT: Postman is an awesome tool to start making API Requests with to see what data comes back and how you'll want to manage that data in your React Components.

## Required Technology:

To test your ability to use modern frontend tools, you'll be required to use the following in your application.

*   React
*   Modern UI Library - One of the following, or something similar:
    *   [Semantic UI](https://react.semantic-ui.com/) - This is already installed
    *   [Styled Components](https://styled-components.com/)
    *   [Bootstrap](https://react-bootstrap.github.io/)
    *   [Materialize](https://materializecss.com/)
    *   [Material UI](https://material-ui.com/)
    *   [Ant Design](https://ant.design/docs/react/introduce)
    *   [Foundation](https://get.foundation/index.html)
    *   [Bulma](https://bulma.io/)
    *   [Tailwind](https://tailwindcss.com/)
*   State Management Tool - One of the following:
    *   [Redux](https://react-redux.js.org/introduction/quick-start) - This is already installed
    *   [React Context](https://reactjs.org/docs/context.html)
    *   [Apollo Client](https://www.apollographql.com/docs/react/) (NOTE: This is a more challenging option. [Checkout this blog post](https://blog.apollographql.com/layering-graphql-on-top-of-rest-569c915083ad))
*   Http Request Library - one of the following:
    *   [Axios](https://github.com/axios/axios)
    *   [Request](https://github.com/request/request)
    *   [Fetch](https://developer.mozilla.org/en-US/docs/Web/API/Fetch_API)
    *   [SuperAgent](http://visionmedia.github.io/superagent/)

## Assessment Steps:

*   Put the time that you start and end on the first line of notes.md. Also, add any grading advice, disclaimers, brags, feedback, or anomalies you encounter along your way.

### PART I - Basic Data Retrieval

1.  Fork this repo so you have a clone of the project in your own github
2.  Create a new Beers Component - `src/components`
3.  Add a new client side route - `/beers` that renders our new Beers Component. Our routes are defined in `App.js`.
4.  Use `axios`, `fetch` or any other HTTP Request library to GET the first 50 Beers from `/api/all_beers`. The way you choose to display / style this is up to you.
5.  Use `axios`, `fetch` or any other HTTP Request library to GET the first 50 Breweries from `/api/all_breweries`. The way you choose to display / style this is up to you. You can create a new route and have it on a different page or you could use your Beers Component and a Grid system to show all beers and breweries side by side.
6.  Make sure to use enough attributes to make the site interesting. Most Beers and Breweries have an image or multiple images.

### PART II - Controlled Data Fetching (This is an important step, please don't skip it)

1.  Paginate the list of Beers and Breweries, loading no more than 10 at a time. Server-side pagination is already setup on the server all you have to do is make sure your client side API requests are passing the correct query strings for the rails server to do the pagination
    *   HINT: you can pass pagination details in the query string. If you pass the `page` and `per_page` query string parameters the server will paginate results for you. EXAMPLE: `api/all_beers?page=20&per_page=5`
2.  Have the ability to go to other pages via pagination links or Infinite Scroll
    *   Example Libraries
        1.  [React Infinite Scroller](https://github.com/CassetteRocks/react-infinite-scroller)
        2.  [React Paginate](https://github.com/AdeleD/react-paginate)

### PART III - Search - Looking Up Specific Beers / Breweries

1.  Have the ability to click on a Beer / Brewery and show all the information about it. You will use an API Endpoint for this. The way you choose to display / style this is up to you.

### BONUS

1.  Use any / all of the other API Endpoints to demonstrate your knowledge of React / Redux
2.  Implement live search on all of your components that show lists of items like Beers, Breweries, Etc
3.  Make your entire site responsive so it looks good on: a large screen, a tablet, and a phone
4.  Port to a React Native App

## Api Endpoints
Assignment details can be found at [https://www.karinsbeer.com/](https://www.karinsbeer.com/)

### Host
The host for Karin's Beer API requests is always `https://www.karinsbeer.com/`

### Authentication
All endpoints require an `API_KEY` to access. Talk to Andrew to get this key. Once you have the key, you will need to include using `key` as a query parameter bypass the authentication.

*Example*
```https://www.karinsbeer.com/api/[END_POINT]/?key=[API_KEY]```

### Beers

 1. `/api/all_beers` - Returns the first 50 Beers from the BreweryDB API
 2. `/api/beer/:name` - Returns info about the Beer if found by name
 3. `/api/beer/random` - Returns info about a random Beer

### Breweries

 1. `/api/all_breweries` - Returns the first 50 Breweries from the BreweryDB API
 2. `/api/brewery/:name` - Returns info about the Brewery if found by name

### Search

 1. `/api/search_all?query=''` - Returns all info from the BreweryDB API matching search query
 2. `/api/search_beers?query=''` - Returns all info about Beers from the BreweryDB API matching search query
 3. `/api/search_breweries?query=''` - Returns all info about Breweries from the BreweryDB API matching search query

### Glassware

 1. `/api/all_glassware` - Returns all Glassware in the BreweryDB API

### Locations

 1. `/api/all_locations` - Returns the first 50 Locations from the BreweryDB API
 2. `/api/locations/:city` - Returns the first 50 Locations in the matched city from the BreweryDB APIContribution: 2020-04-11 20:00

Contribution: 2020-04-11 20:01

Contribution: 2020-04-13 20:00

Contribution: 2020-04-13 20:01

Contribution: 2020-04-13 20:02

Contribution: 2020-04-14 20:00

Contribution: 2020-04-14 20:01

Contribution: 2020-04-14 20:02

Contribution: 2020-04-14 20:03

Contribution: 2020-04-14 20:04

Contribution: 2020-04-14 20:05

Contribution: 2020-04-14 20:06

Contribution: 2020-04-14 20:07

Contribution: 2020-04-15 20:00

Contribution: 2020-04-15 20:01

Contribution: 2020-04-15 20:02

Contribution: 2020-04-18 20:00

Contribution: 2020-04-18 20:01

