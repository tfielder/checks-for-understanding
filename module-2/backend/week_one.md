## Week One - Module 2 Recap

Fork this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week (which is a TON!).

Note: When you're done, submit a PR.

### Week 1 Questions

1. List the five common HTTP verbs and what the purpose is of each verb.
  GET - serves up information to the http request.
  POST - sends a request to create information.
  PATCH - sends a request to update a part of information already present.
  DELETE - sends a request to delete information.
  PUT - sends a request to update information.
2. What is Sinatra?
  Sinatra is a gem which helps with turning a project into a viewable app.
  I believe it helps retrieve pages in an MVC design.
3. What is MVC?
  MVC stands for Model, View, Controller. It is a design architecture/pattern.
  It is generally a RESTful way to design your software.
4. Why do we follow conventions when creating our actions/path names in our Sinatra routes?
  One reason is for readability. Another is to create that RESTful design.
  It has to do with approaching the Single Responsibility Principle within the software.
5. What types of variables are accessible in our view templates without explicitly passing them?
  Instance variables defined in our controller are accessible in our view templates.

6. Given the following block of code, how would I pass an instance variable `count` with a value of `1` to my `index.erb` template?

  ```ruby
  get '/horses' do
    @count = 1    #I would add this line of code and call it somewhere in the index.erb.
    erb :index
  end
  ```
  With the code in place you could use <% %> in the embedded ruby file and use
  @count where you wish.

7. In the same code block, how would I pass a local variable `name` with a value of `Mr. Ed` to the view?
  Similarly you could use name = "Mr. Ed" and then send name using local: {}
8. What's the purpose of ERB?
  Embedded ruby allows you to use programming logic within an html file, making
  your html file dynamic.

9. Why do I need a development AND test database?
  It's best practice to separate your testing data from your development data.
  You wouldn't want one to corrupt the other.

10. What is CRUD and why is it important?
  Create, Read, Update, and Delete/Destroy are the four main operations we
  can take with data. Programming is built on these principles in interacting
  with data. Without them, you wouldn't have much of a program.

11. What does HTTP stand for?
  Hypertext Transfer Protocol is the standard for sending and receiving information
  across the web.

12. What are the two ways to interpolate Ruby in an ERB view template? What's the difference between these two ways?
  One way is to use <% %> which allows ruby code to operate without being rendered.
  Another way is to use <%= %> which renders, or echoes the ruby code onto the page.

13. What's an ORM? What does it do?
Object Relational Mappers interpret database information into Ruby objects.
It's a way to use object oriented programming to interact with database info.

14. What's the most commonly used ORM in ruby (Sinatra & Rails)?
ActiveRecord is the most commonly used ORM in ruby.

15. Let's say we have an application with restaurants. There are seven verb + path combinations necessary to provide full CRUD functionality for our restaurant application. List each of the seven combinations, and explain what each is for.
  verb: GET     path: '/tasks'        shows all tasks or objects that can be viewed.
  verb: GET     path: '/tasks/:id'    shows an individual task or object.
  verb: GET     path: '/tasks/new'    usually shows a form to create a new task/object.
  verb: POST    path: '/tasks'        allows the user to create a task/object.
  verb: GET     path: '/tasks/:id/edit'  allows a user to view a page to edit/update.
  verb: PUT     path: '/tasks/:id'    allows user to update task/object info.
  verb: DELETE  path: '/tasks/:id'    allows user to delete/destroy task or object.

16. What's a migration?
  I remember this being asked on a test in grade school and in this case it is not the
  movement of animals from one location to another. That said, in software, it is
  the transfer of information such as CSV into a database.

17. When you create a migration, does it automatically modify your database?
  It does not automatically modify your database, you must instruct the software how
  to handle the information to be modified in the database.
18. How does a model relate to a database?
  The model can work with the database to provide additional CRUD operations.
19. What is the difference between `#new` and `#create`?
  New seems to be used more commonly with instantiating class instances whereas create seems to be more commonly used with database "instances".
20. Given a table named `animals`, What is the SQL query that will return all info from that table?
    `id     name        number_of_legs
    -----   ------      --------------
      1     panda       4
      2     giraffe     4
      3     whale       0
      4     bird        2
    `
    SELECT * FROM animals;

21. Using the same table, What is the SQL query that will return only the animals that has 4 legs?
    SELECT * FROM animals WHERE number_of_legs=4;

### Review Questions:  
22. Given a CSV file (“films.csv”) with these headers [id, title, description], how would you load these into your database to create new instances of Film?  
    I would require them in my seed file, make sure that I have my migration file
    setup and then run rake db:seed.
23. Given the following hash:
```
activities = {
  hiking: {cost: $0, supplies: ['hiking shoes', 'water', 'compass']},
  karaoke: {cost: $10, supplies: ['courage', 'microphone']},
  brunch: {cost: $35, supplies: ['mimosa flutes']},
  antiquing: {cost: $200, supplies: ['list of antique stores']}
}
```
How would I add 'granola bar' to things you should have when hiking?
  activities[:hiking][:supplies] << 'granola bar'
24. What are the 4 Principles of OOP? Give a one sentence explanation of each.
  Encapsulation - a class or object contains details hidden from outside.
  Inheritance - reduces code by inheriting functionality from other code.
  Abstraction - representing complex things in a simple form.
  Polymorphism - allowing an class or object to change form through addition or redefinition.


### Self Assessment:
Choose One: (erase the others)
* I was able to answer most questions independently, but utilized outside resources for a few (namely 24 and 15 and 7)

Choose One:

* I feel (cautiously) comfortable with the content presented this week.
  (Still studying)
