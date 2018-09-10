## Week Four Recap

### Instructions
Fork or re-pull this repository. Answer the questions to the best of your ability.

Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week.

Note: When you're done, submit a PR with a reflection in the comments about how this exercise went for you.

### Week 4 Questions

1. What is a cookie?
  A cookie is a temporary file that allows for information to be passed from HTTP request to request.
2. What’s the difference between a session and a cookie?
  A session keeps cookie information throughout the session lifespan.  A cookie may live longer.
3. What’s a flash and when do you want to use flashes?
  Flashes are used to convey information in terms of alerts, errors, or successes in response to user driven actions.  They are often displayed
  to the user.
4. Why do people say “HTTP is stateless”?
  Because it generally is.  An HTTP request doesn't hold state, but transfers information back and forth from client to server.
5. What’s authentication? Explain.
  Authentication allows for creating a session, as you would when logging in to a website.  It deals with determining what user is accessing the site.
6. What’s the difference between authentication and authorization?
  Authorization has to do with what a user can do.  What permissions they are granted within the site.
7. What’s a before filter?
  A before filter allows you to restrict access to controller actions and thereby web pages by stipulating what logic must be satisfied before going to a view.  These come in handy for restricting access based on session user credentials.
8. How do we keep track of a user once they’ve logged in?
  Carefully. Generally we use a session with an id that lives in the ApplicationController so that the user can continue to move through the site based on encrypted user credentials sent with the Http requests.
9. When do you want to namespace a resource? When do you want to nest a resource? What's the differences between those two approaches?
  Namespacing allows you to create different URL (URI) extensions.  Nesting resources are beneficial for organizing your pages and information that have nested relationships (often one to many style relationships).  Namespacing has more to do with the organization of the resources whereas nesting has more to do with the way the resources are accessed and what parameters are necessary for accessing them.
10. At a high level, what tools can you use to implement authorization? How would you use them?
  Authorization includes using encrypted passwords and usernames. Bcrypt is a gem that can be used to help implement authorization. The before filter also is a way to restrict access to any of the actions within the ApplicationController.
11. What's an enum, and what advantages does it offer? What data type needs to be in your database to use an enum? Where do you declare an enum?
  An enum is sort of like an array that has the property of acting like a constant.  It can be used to assign roles to users which comes in handy for establishing authorization.  You should have an integer in your database to use an enum and you can declare it within a class.
12. What are some strategies you can use to keep your views DRY?
  View logic can come in handy as could implementing logic at the model level.


### Reviews Questions
13. Given the following array of hashes, how would I print an alphabetical list of holidays?
```ruby
[
 {holiday: {name: "St Patrick's Day", supplies: ["Corned Beef and Cabbage"]}},
 {holiday: {name: "Halloween", supplies: ["Candy", "Costume"]}},
 {holiday: {name: "Hanukkah", supplies: ["Menorah"]}}
]
```  
array = array.map do |element|
  element[:holiday][:name]
end.sort

14. How would you clean incoming data to ensure "$300" or "300.00" is stored as 300?
"$300".to_i or "300.00".to_i

### Self Assessment:
Choose One:
* I was able to answer most questions independently, but utilized outside resources for a few

Choose One:
* I feel comfortable with the content presented this week

