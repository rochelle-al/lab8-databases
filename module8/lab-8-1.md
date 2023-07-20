Logical Model

User
user_id (primary key)
username
email
password
created_at


Post
post_id (primary key)
user_id (foreign key referencing User)
title
description
image_url
created_at

Like
like_id (primary key)
user_id (foreign key referencing User)
post_id (foreign key referencing Post)
created_at


Comment
comment_id (primary key)
user_id (foreign key referencing User)
post_id (foreign key referencing Post)
content
created_at



Physical Model:

Table: User
Columns:
user_id (integer, primary key)
username (string)
email (string)
password (string)
created_at (datetime)


Table: Post
Columns:
post_id (integer, primary key)
user_id (integer, foreign key referencing User.user_id)
title (string)
description (text)
image_url (string)
created_at (datetime)


Table: Like
Columns:
like_id (integer, primary key)
user_id (integer, foreign key referencing User.user_id)
post_id (integer, foreign key referencing Post.post_id)
created_at (datetime)


Table: Comment
Columns:
comment_id (integer, primary key)
user_id (integer, foreign key referencing User.user_id)
post_id (integer, foreign key referencing Post.post_id)
content (text)
created_at (datetime)