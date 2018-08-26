## Week Two - Module 2 Recap

Fork or re-pull this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week (which is a TON - YOU are a web developer!!!).

Note: When you're done, submit a PR.


### Week 2 Questions

1. At a high level, what is ActiveRecord? What does it do/allow you to do?
ActiveRecord allows you to take objects, query a database, and return information that is
accessible by said objects.  ActiveRecord is an ORM or Object Relational Mapper
that allows you to communicate with databases written in languages like SQL.

2. Assume you have the following model:

```ruby
class Team << ActiveRecord::Base
end
```

What are some methods you can call on `Team`? If these methods aren't defined in the class, how do you have access to them?

Some of the class methods include find, find_by, order, group, create, where.
The methods, even though they aren't defined in the class inherit from ActiveRecord therefore
making them accessible to the class.

3. Assume that in your database, a team has the following attributes: "id", "name", owner_id". How would you find the name of a team with an id of 4? Assuming your class only included the code from question 2, how could you find the owner of the same team?
To find the name of a team with an id of 4, I would call Team.find(4).  With a relationship
defined in the class you can get access to owner through the foreign key of owner_id.


4. Assume that you added a line to your `Team` class as follows:

```ruby
class Team << ActiveRecord::Base
  belongs_to :owner
end
```

Now how would you find the owner of the team with an id of 4?
Team.owner.id

5. In a database that's holding students and teachers, what will be the relationship between students and teachers? Draw the schema diagram.
I would identify the relationship as a many to one where many students belong to one teacher
and a teacher has many students.  You could argue that there is a many to many relationship
over time where many teachers have many students, but for the sake of this question I'm sticking with describing the one to many relationship.
See attached screenshot in folder called schema.

6. Define foreign key, primary key, and schema.
A foreign key is added to a table to show a many to one relationship.  The belongs to category
will have a foreign key.  A primary key is the main identifier for a block of data. Schema can be presented to show relationships (i.e. foreign keys) between tables of data and the contents of those tables (i.e. columns).

7. Describe the relationship between a foreign key on one table and a primary key on another table.
  These data points are used to match blocks of data.  A foreign key again appears in the belongs_to table and the primary key appears in the has many table. In a many to many relationship the foreign keys are found in the table composed of both tables.

8. What are the parts of an HTTP response?
I think there is a status code in addition to the html, css, js, etc.


### Optional Questions

1. Name your five favorite ActiveRecord methods (i.e. methods your models inherit from ActiveRecord) and describe what they do.
find - finds an id.
order - can order the data within a table.
group - will return a hash and group data based on some criteria.
find_by - allows you to search by a column value.
create - is like the new method, but saves additionally.

2. Name your three favorite ActiveRecord rake tasks and describe what they do.
rake db:create - creates your database.
rake db:migrate - migrates data according to the model.
rake db:seed - pulls information from the seed file to populate the database.

3. What two columns does `t.timestamps null: false` create in our database?
  created_at and updated_at which are both in the time format.
4. In a database that's holding schools and teachers, what will be the relationship between schools and teachers?
One to many (in most cases).  Many teachers belong to a school and a school has many teachers.
5. In the same database, what will you need to do to create this relationship (draw a schema diagram)?
  I ended up creating a foreign key in the teachers table so that the teachers could be identified by school.  Students will have access to school through teachers.  Check out Screen Shot 2 for more.

6. Give an example of when you might want to store information besides ids on a join table.
  Perhaps if you were to expand the data available through those ids, you could quickly search for related information.  I am not aware at this point of including additional information in the database table because I believe it would break one of the data norm rules.
7. Describe and diagram the relationship between patients and doctors.
  A doctor has many patients and in most cases a patient will belong to a doctor.
  I would put a foreign key called doctor_id in the patient table.  I suppose if you were looking at specialists you could potentially have many doctors with many patients and have a many to many relationship in which case you might create a DoctorPatients table with foreign keys to patient_ids and doctor_ids.
8. Describe and diagram the relationship between museums and original_paintings.
  One to many.  Add museum_id to the original_painting table as a foreign key.
9. What could you see in your code that would make you think you might want to create a partial?
   Anything in my html that I seem to be repeating would make me think I might want
   to create a partial.

### Self Assessment:
Choose One:
* I was able to answer every question without relying on outside resources

Choose One:
* I feel overwhelmed by the content presented this week
