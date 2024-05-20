# RabbitMQ-for-Youtube-inter-component-communication-

### YouTuber
- Youtuber is a service that allows YouTubers to publish videos on the YouTube server.
- Youtubers can publish videos by sending simple messages to the YouTube server, including the video name and the YouTuber’s name.
### User
- Users can subscribe or unsubscribe to YouTubers by sending messages to the YouTube server.
- Users will receive real-time notifications whenever a YouTuber they subscribe to uploads a new video.
- Note that YouTubers and users cannot directly communicate with each other; only through the YouTube server can they do so.
- Users can log in by running the User.py script with their name as the first argument. Optionally, they can subscribe or unsubscribe to a YouTuber using the second and third arguments. (See deliverables).
- Whenever a user logs in, it immediately receives all the notifications of videos uploaded by its subscriptions while the user was logged out.
### YouTubeServer
- The YouTube server consumes messages from Users and YouTubers and stores them as data, maintaining a list of YouTubers and their videos, and all users and their subscriptions.
- It also processes subscription and unsubscription requests from users.
- The server sends notifications to all subscribers of a YouTuber whenever they upload a new video.
