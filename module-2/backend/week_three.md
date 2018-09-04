## Week Three Recap

### Instructions
Fork this repository. Be sure to pull the latest changes to your local repo. Answer the questions to the best of your ability.

Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week.

Note: When you're done, submit a PR with a reflection in the comments about how this exercise went for you.

### Week 3 Questions

1. What is the entry at the command line to create a new rails app?
  rails new <name of project> -T -d="postgresql" --skip-spring --skip-turbolinks
2. What do Models generally inherit from in rails?
  ApplicationRecord
3. What do Controllers generally inherit from in a rails project?
  ApplicationController
4. How would I create a route if I wanted to see a specific horse in my routes file assuming I'm sticking to standard conventions and that I didn't want other CRUD functionality?
  resources :horses, only: [:show]
5. What rake task is useful when looking at routes, and what information does it give you?
  rails routes allows you to see the path helper, URI path (with associated params), and the controller action.
6. What is an example of a route helper? When would you use them?
  A route helper can be used in place of a specific uri path.  I have used them when linking to another page within my erb view files.
7. What's the difference between what `_url` and `_path` return when combined with a routes prefix?
  `_url` is generally used when linking to an outside resource whereas `_path` is used when linking to a resource included in the app.
8. What are strong params and why are they necessary?
  Strong params make sure that your controller takes in and provides the appropriate data for processing a controller action.  It is used to make sure that a nefarious person doesn't insert bogus info in the URL to gain access to your app's functionality.
9. What role does `form_for` play in helping us create our forms?
  Form for allows us to use embedded ruby to create a hash for transferring information to the controller generally for editing or creating an object.
10. How does `form_for` know where to submit the user's input?
  After `form_for` you will generally provide the object that the form should collect for.
11. Create a form using a `form_for` helper to create a new `Horse`.
  `<%= form_for @horse do |f| %>`
  `<%= f.label :name %>`
  `<%= f.text_field :name %>`
  `<%= f.submit %>`
  `<% end %>`

12. Why do we want to validate our models?
  Validating attributes within a model ensures that data will be added to a database with the appropriate data. Testing for attribute validation can demonstrate that a model will appropriately create an object that is readable by the ORM (ActiveRecord) when communicating with the database.
13. What are the steps of the DNS lookup?
  First the browser looks for the IP address in the computer memory cache.
  It then looks for the IP address in the network (if one exists).
  Then it will reach out to the ISP (internet service provider).
  If the ISP doesn't have it, the ISP will reach out to the ANS to find the IP. The IP address will be stored/cached along these routes back to the client so that the client computer may make an http request to the appropriate IP address.

### Review Questions
14. Within a feature test and given the following HTML, write the code necessary to target the following section and check the person's name?

  `<section id="personal-info">
    <h3><%= @person.name%></h3>
   </section>
  `

  `within(#'personal-info').find(@person.name)`

15. How would you call the method `prance` from within the method `move` on a `Horse` instance?
  move.prace

16. Given the following hash:

```ruby
furniture = {table: {height: 3, color: "red"}, purchased: true}
```
What is the difference between how you would return true vs returning 3?  

You would need to access an additional layer through the key height to access the 3, versus the key purchased to access true.

17. What is inheritance?
  Inheritance has to do with the ability in OOP for an object to inherit behavior and/or state from another object.  It is one of the pillars of OOP.

### Self Assessment:
Choose One:
* I was able to answer every question without relying on outside resources
`note I will double check my answers to make sure I'm not missing something`

Choose One:
* I feel comfortable with the content presented this week

