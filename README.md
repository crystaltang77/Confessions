# Confessions
## App Tagline: 
Cornell’s anonymous confessions sharing app.
## Links: 
https://github.com/lucyxubroad/confessions-ios-backend
## Screenshots: 
## Purpose: 
Our app is a social media app with the purpose of allowing the users to anonymously post the feelings and thoughts. The first view when the app is opened is the sign in/sign up screen. We require each user to sign in/sign up so that we can keep track of the different users. After you sign in, you will be shown the main feed where you can make your own post (you can also make a new post on the post tab) and see other posts that were made surrounding your location. You can like a post or comment on the post. If you press the comment button, you will be taken to a different view where you can see all the comments previously made and comment yourself. On the tab bar, the post tab gives you another way to make a post. You will also find the sign out tab where you can sign out of the tab.
## Project Requirements: 
### iOS: 
We used AutoLayout using SnapKit to create the bounds for each of our views. We used UITableView to create the feed of posts and the feed of comments. We used a UITabBarController to navigate between the main feed, the new post view, and the sign in/sign up view. We used the APIs Alamofire and CoreLocation.
### Backend:
Since Confessions is twist on traditional social media applications, backend support for the app had to include a database to store posts, comments, and users. A lot of the backend was borrowed from P5, which had routes for posting posts, posting comments, liking posts, and getting posts and comments.

However, we made modifications to support some of the nuances of Confessions, which includes anonymous users, showing only posts made in area vicinity, and deletion of posts after 24 hours of posting. We modified the backend by adding longitude and latitude fields to the posts and adding a route that retrieves only posts made within a 5000 meter radius of user's location. We added timestamps to each post so that after 24 hours, they will no longer be displayed in the app. We also added user authentication that assigns anonymous usernames to each user to protect their privacy.
