# Blogly

## Part Two: Adding Posts
In this part, we’ll add functionality for blog posts using the one-to-many features of SQLAlchemy.

Post Model

Next, add another model, for blog posts (call it Post).

Post should have an:

>id, like for User
title
content
created_at a date+time that should automatically default to the when the post is created
a foreign key to the User table
User Interface
Here is what you should build:

**Better User Detail**

_images/user-w-posts.png
New Post Form

_images/add-post.png
Post Detail Page

_images/detail-post.png
Post Edit Page

_images/edit-post.png
>Add Post Routes
GET /users/[user-id]/posts/new
Show form to add a post for that user.
POST /users/[user-id]/posts/new
Handle add form; add post and redirect to the user detail page.
GET /posts/[post-id]
Show a post.

Show buttons to edit and delete the post.

>GET /posts/[post-id]/edit
Show form to edit a post, and to cancel (back to user page).
POST /posts/[post-id]/edit
Handle editing of a post. Redirect back to the post view.
POST /posts/[post-id]/delete
Delete the post.
Change the User Page
Change the user page to show the posts for that user.

**Testing**
Update any broken tests and add more testing

**Celebrate!**
Yay! Congratulations on the first big two parts.

## Parts Two Further Study
There are several possible additional tasks here.

**Make a Homepage**
Change the homepage to a page that shows the 5 most recent posts.

_images/homepage.png
**Show Friendly Date**
When listing the posts (on the post index page, the homepage, and the user detail page), show a friendly-looking version of the date, like “May 1, 2015, 10:30 AM”.

**Using Flash Messages for Notifications**
Use the Flask “flash message” feature to notify about form errors/successful submissions.

**Add a Custom “404 Error Page”**
Research how to make a custom page that appears when a 404 error happens in Flask. Make such a page.

Cascade Deletion of User
If you try to delete a user that has posts, you’ll get an IntegrityError — PostgreSQL raises an error because that would leave posts without a valid user_id.

When a user is deleted, the related posts should be deleted, too.

You can find help for this at Cascades>`_

