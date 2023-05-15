# advanced-flask-blog-application

This Flask application creates a simple blog site using SQLite database. The site allows users to view blog posts, create new posts, edit existing posts, and delete posts.

The application uses the Flask web framework and extends its functionality by utilizing some associated Flask extensions. Below are more detailed explanations about the main components of the application and the libraries used:

Flask and Related Extensions:

  Flask: The main Flask framework used to create the web application.
  Flask-Bootstrap: Used to integrate Bootstrap styling into the application.
  Flask-WTF: Used for creating, validating, and handling web forms.
  Flask-CKEditor: Provides a rich text editor feature for users.
Database and SQLAlchemy:

  SQLite database is used.
  SQLAlchemy: An ORM (Object-Relational Mapping) library that simplifies database interaction with Flask. It establishes a connection with the SQLite database  using the SQLALCHEMY_DATABASE_URI configuration setting.
  Database Table:

  Defined a SQLAlchemy model named BlogPost.
  The BlogPost table contains fields such as post title, subtitle, date, content, author, and image URL.
Forms:

  Defined a WTForm named CreatePostForm.
  The form includes fields for users to enter information when creating a new post (title, subtitle, author, image URL, and content).
Pages and Functions:

  Home Page (/): Displays all blog posts.
  Post Page (/post/<int:post_id>): Displays the details of a specific post.
  About Page (/about): Provides information about the site.
  Contact Page (/contact): Displays contact information.
  New Post Creation Page (/new-post): Displays the form for users to create a new post and redirects to the home page after submission.
  Post Editing Page (/edit-post/<int:post_id>): Displays the form to edit an existing post, updates the post after editing, and redirects to the corresponding  post page.
Functions:

  get_all_posts(): Retrieves all blog posts from the database and displays them on the home page.
  show_post(post_id): Retrieves the details of a specific post and displays them on the post page.
  about(): Displays the about page.
  contact(): Displays the contact page.
  add_new_post(): Displays the form to create a new post, creates a new post after submission, and redirects to the home page.
  edit_post(post_id): Displays the form to edit an existing post, updates the post after editing, and redirects to the corresponding post page.
  delete_post(post_id): Deletes a specific post from the database and redirects to the home page.
  app.run(debug=True): Runs the application and starts a local Flask server.

This Flask application can serve as a useful resource for creating a sample Flask application, as well as for learning about Flask, SQLAlchemy, and other Flask extensions. It also provides insights into the basics of a blog application.
