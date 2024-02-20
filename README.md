## About project

The project is a reddit-clone.

It uses 

- MySQL as a database.
- Springboot to with database
- Reactjs for web-gui

The project is foremost a practice in authorization.

In the project, user’s can create communities.

These communities can have moderators and administrators.

The administrators can set different rights fro the moderators (ex moderators can ban other users, moderators can delete other’s posts)

## How to run

In the springboot project, change the [application.properties](http://application.properties) to appropriate values for the mysql database.

```python
# JPA configuration
spring.datasource.driver-class-name=com.mysql.cj.jdbc.Driver
spring.datasource.url=jdbc:mysql://localhost:port/database_name
spring.datasource.username=username
spring.datasource.password=password
spring.jpa.show-sql=true

spring.jpa-properties.hibernate.dialect=org.hibernate.dialect.MySQL5Dialect
spring.main.allow-bean-definition-overriding=true
spring.jpa.properties.hibernate.show_sql=false

# Set the path to save images
pathToSaveImages=C:/Users/path_to_save_images

# file configuration
spring.servlet.multipart.max-file-size=100MB
spring.servlet.multipart.max-request-size=100MB

logging.level.org.springframework.web: DEBUG
```

Make a database in mysql with the correct database_name.

Also make sure to specify at what path you want the to be saved at.

Run the file 

```python
Reddit clone\Reddit-clone\src\main\java\com\example\Reddit\clone\RedditCloneApplication.java
```

Then run the reactjs project with 

```python
npm start
```

Go to

```python
http://localhost:3000/
```

to see the webpage

## Database
If some of the images are unclear, then click on them to get a better view.
![database](https://github.com/Vemund1999/reddit_clone/assets/88531005/b1d9ab18-f778-4288-8a9c-863098e00ab1)


## Some features

When going to 

```python
http://localhost:3000/
```

the webpage looks like this

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/9569794c-20f9-45a0-b771-b02f3b226deb/adc719ba-2718-4c55-a489-de6254c69b64/Untitled.png)

You can register a user by clicking “Register”

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/9569794c-20f9-45a0-b771-b02f3b226deb/e1c5bce1-8c30-4103-9300-361de417d2cc/Untitled.png)

On the profile page, a user can set a wallpaper and profile image for itself

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/9569794c-20f9-45a0-b771-b02f3b226deb/ea8805f0-c921-4138-a971-1adecf2496b6/Untitled.png)

You can make communities, like on reddit.

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/9569794c-20f9-45a0-b771-b02f3b226deb/99eb58b6-6a49-4b46-97be-ce873dda260f/Untitled.png)

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/9569794c-20f9-45a0-b771-b02f3b226deb/73edb53b-8de7-498b-a71e-e4f414492c7d/Untitled.png)

On these communities, users can make posts

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/9569794c-20f9-45a0-b771-b02f3b226deb/586e74ec-57d0-463b-8f1b-965230f26bea/Untitled.png)

These posts have a threaded-commenting

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/9569794c-20f9-45a0-b771-b02f3b226deb/43879f1f-9706-487a-a960-75ea0a0361e5/Untitled.png)

You will recieve messages for different things, such as getting a reply from another user on your comment.

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/9569794c-20f9-45a0-b771-b02f3b226deb/0a37cff4-0f4d-4a0d-b7b8-ce5f4cfb8679/Untitled.png)

These are topics the things you can recieve messages for

```python
public enum MessageTopic {
    NewReplyToPost,
    NewReplyToComment,
    NewFriendRequest,
    NewRequestToJoinCommunity
}
```

“NewRequestToJoinCommunity” means that on communities that are private or restricted, users must request to join the community

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/9569794c-20f9-45a0-b771-b02f3b226deb/5c899edf-1c1c-4a08-83dd-fd5c74694dd9/Untitled.png)

A user can be made moderator by an admin.

The admin can controll what rights the moderators have.

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/9569794c-20f9-45a0-b771-b02f3b226deb/e3ad3394-8e0d-497d-a4d0-86b5432ffb41/Untitled.png)

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/9569794c-20f9-45a0-b771-b02f3b226deb/12edc76b-20d2-43f6-92a5-5f560e05ce78/Untitled.png)

Users can become friends

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/9569794c-20f9-45a0-b771-b02f3b226deb/31809029-a50e-4d9a-a54b-3af7268ec2ac/Untitled.png)

Users have realtime chat.

![Untitled](https://prod-files-secure.s3.us-west-2.amazonaws.com/9569794c-20f9-45a0-b771-b02f3b226deb/72665e9d-98f1-41a6-8d50-d5ea5de00511/Untitled.png)
