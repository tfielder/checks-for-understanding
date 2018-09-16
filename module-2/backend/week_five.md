### Week 5 Questions

Re-pull from this repository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week (which is a TON!).

Note: When you're done, submit a PR.

### Week 5 Questions
1. How do we make flash messages display on a page?
   You would use flash[:notice] or flash[:alert] and set it equal to the message you wish to display.  You would need to also redirect to the resource in which you want the message to appear and in that resource use embedded ruby to display the message.
2. Where is cart information/temporary information usually stored?
   Generally in a PORO Cart.
3. What might be some reasons not to store a cart in our database? Are there any reasons why we would want to persist that information?
   One of the reasons is that the information stored is subject to constant changes.  It makes more sense to store the information once it is finalized into an order for example.
4. What is the purpose of the asset pipeline?
   The asset pipeline ensures that requests for the latest information receive only the resources that need to be updated rather than all resources (including the ones that haven't changed).
5. Why do we precompile our assets?
  Precompiling can lead to faster load times on the client-side.
6. What do each of the following tags do?

```ruby
 stylesheet_link_tag "application"
 javascript_include_tag "application"
 image_tag "rails.png"
```
  The stylesheet ensures that all CSS is pulled in to the request for the layout through the application file.
  The javascript ensures that all scripting is pulled into the request for the layout through the application file.
  The image tag refers to the rails.png file located within the project directory.

7. What are some of the elements of a great read me? What are some of the benefits of taking the time to update a readme for our project?
  A great read me can include information that covers the specs, installation, code, and any pitfalls a user might encounter.  Some of the benefits include having a reference document for a team or open-source style project.  It shows your professionalism and attention to detail too.

8. What are the top four accessibility issues that we as developers should be aware of?
  Some of the accessibility issues include cognitive, visual, auditory, and mobility impairments.
9. `before_save` is an example of a what? Where in our Rails application would we find a `before_save`?
  It is an example of a callback.  We would find the before_save usually in the Application Controller, but it could be found in any controller.
10. Given the following object, how would we create a scope for all users who are active?

```ruby
User.create(name: "Happy", active: true)
```
  class User < ActiveRecord::Base
    scope :active, -> { where(active: true)}
  end
11. What is the difference between a scope and a class method?
  From what I can tell, there isn't much.  Scoping is a way of defining a class method
  for narrowing down an ActiveRecord Query.

### Review Questions:  
12. Given the following hash:  

```ruby
{cart: {"17" => 4, "204" => 52, "29" => 22}}
```

  12a. How would you add item with id of 48 with a quantity of 4?
      hash[:cart][:48] = 4
  12b. How would you increase the quantity of item 29?  
      amount = 22 + quantity
      hash[:cart][:28] = amount
  12c. How would you find out how many items your user is thinking about purchasing?   
      hash[:cart].values.inject {|sum, value| sum + value}

13. What is polymorphism? How does it relate to duck-typing? What are two ways you use this in everyday Rails applications?  
  Polymorphism is the ability of an inherited class to display slightly different behaviors than its parent.  Duck-typing is treating an object as if it is a particular type.  Perhaps this has to do with using POROs instead of saving directly to a database.

14. How would you clean the string "(630) 854-5483" to "630.854.5483"?  
  "(630) 854-5483".tr("()", "").tr(" -", ".")

### Self Assessment:
Choose One:
* I was able to answer most questions independently, but utilized outside resources for a few

Choose One:
* I feel comfortable with the content presented this week
