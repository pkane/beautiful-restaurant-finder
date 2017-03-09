# Beautiful Restaurant Finder
## Author: Paul Kane (kane.pc@gmail.com)

## Description  
Hi there! So first off, I my intention was originally to leverage a fantastic boilerplate from the folks at [Viget Labs](http://code.viget.com/). They created an awesome package called [Gulp Starter](https://github.com/vigetlabs/gulp-starter) that leverages Webpack, Babel, and Gulp. However, I ran into a major wall with the very first step: API integration. Both Yahoo and Yelp have robust API's, but I ultimately chose Yelp because of A: the assignment and B: I preferred its intuitive key nomenclature for querying its database.  

There was just one big problem: its endpoint doesn't provide cross-domain access within the browser (even when running a node server locally.) At this point, I was determined get up and running as quick as possible. I chose to use the tried and true jQuery $.ajax() request. So after some poking and prodding, a sprinkle of Stack Overflow and a dash of Google, I learned that by setting 
`'cache' : true` explicitly, it prevents jQuery from appending an additional underscore to the query string (used to prevent caching). Here's a [full explanation of this issue](https://github.com/Yelp/yelp-api/issues/99.) From there, I wanted to create a clean and usable interface and focus on getting the functionality working.  

## Running the project
Standard
* Open `index.html` in a browser

Alternate (Optional) - Run a very simple server to deliver the files.
* `python -m SimpleHTTPServer` 
* Load `localhost:8000` in a web browser.

## Things I would add with more time  
* Package the project in a build system, with real dependencies, tasks, linting, and tests.
* Implement a real form validation system. I'm relying too much on Yelp's flexibility for my form fields. Any real production form needs proper validation and testing.
* Add more fields and options to search.
* Add more details to the listing results. Further style this area.
* Style the page and form component with Sass. 
* Separate the markup into templates.
* Separate the search into its own component, and possibly leverage a more robust or proven API.