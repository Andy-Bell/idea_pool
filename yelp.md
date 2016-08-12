## Version 1 - MVP

For the initial version we want to duplicate the core functionality of Yelp - users should be presented with a list of restaurants which they can leave reviews for.

### V1 Specification

- Visitors can create new restaurants using a form, specifying a name and description
- Restaurants can be edited and deleted
- Visitors can leave reviews for restaurants, providing a numerical score (1-5) and a comment about their experience
- The restaurants listings page should display all the reviews, along with the average rating of each restaurant
- Validations should be in place for the restaurant and review forms - restaurants must be given a name and rating, reviews must be given a rating from 1-5 (comment is optional)


## Version 2 - User login

Although our initial version serves its purpose - it's limited in a few respects. Any visitor to the site can freely add, edit or delete. We also have very few options to track or constrain the visitors to our site.

We can solve both of these problems by adding a user login system, as we did with Bookmark Manager.

### V2 Specification

* Users can register/login

* Some indication should be given on the page (as part of the layout) whether the user is currently logged in, along with links to the available actions (i.e. Logout/Edit account is signed in, otherwise Sign In/Sign Up)
* The email address of the reviewer should be displayed as part of the review
* *Optional* - Users can't review a restaurant which they created

## Version 3 - Setting limits on users

Although our version 2 serves its purpose - it's limited in a few respects. First any user can freely create, delete or edit restaurants. Additionally, a user can leave multiple reviews for the same restaurant - making it easy for restaurant scores to be skewed.

### V3 Specification

* A user must be logged in to create restaurants
* Users can only edit/delete restaurants **which they've created**
* Users can only leave **one review per restaurant**
* Users can delete their own reviews



## Further specifications

* Currently, when writing a review, we have to go to a separate page and trigger a page refresh. Migrate the functionality to happen asynchronously with AJAX. We'll also have to set up [Poltergeist](https://github.com/teampoltergeist/poltergeist) to enable us to run JS-enabled tests.
* Create a helper method to allow ratings and average ratings to be displayed as stars (e.g.) rather than numbers
* Use SCSS to enhance the overall design of the site
* Refactor your more complex views to use partials
* Add the ability for users to add an image to a restaurant, by pointing to an external image URL

