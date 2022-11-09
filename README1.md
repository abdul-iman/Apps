# Design Spike
## investigate 3 different ways of hosting a static content website on Google Cloud using a Google Cloud service other than Compute Engine.

## Creating Static website Cloud storage bucket 
- Sign in to Google Cloud platform 
- Start creating Storage Bucket
- Name your Storage Bucket
- Choose a Default Storage Class - multi regional, regional, coldline or nearline 
- Choose how to Control access to Object - Uses IAM policy and data is encrypted at transit and rest. it has extra encryption as google will encrypt it before written on the server 
- Check monthly cost estimate for your Bucket - Shows you the cost 
- Upload files to your Bucket 
- Set your Bucket to Public - edit public permission and set it to public, set it to storage public viewer give them option to only view and not allowed to modify 
- Set your domain to your bucket


## Advantage of using Cloud bucket 
- Scalability: Static websites can be scaled up or down easily, without affecting the website’s functionality.
- Availability: Static websites are always available, no matter what the circumstances.
- Security: Static websites are typically more secure than dynamic websites because they are not reliant on server-side scripting or dynamic content.
- Cost: Hosting a static website on Google Cloud Storage is cheaper than hosting a static website on a dedicated server or on a shared server.

## Disadvantages of using Cloud bucket 
- Google Cloud Storage is a bit more expensive than other options.
- It can be difficult to manage your website if you are not familiar with Google’s tools and interface.
- There can be downtime if Google has issues with their servers.

## Firebase 
- Install the Firebase CLI
- Set up a project directory
- View, test, and share your changes before going live (optional)
- Deploy your site
- 	Link to a Firebase Web App (optional)

### Advantages of using firebase
- To share data
- Serve content over a secure connection
- Host static and dynamic content plus microservices
- Deliver content fast
- Emulate and even share your changes before going live
- Deploy new versions with one command
- real-time features
- Firebase shortens the development cycle
- integrate with helpful tools
- Database - data is safely stored in collections and documents while maintaining significant level 
-Faster Development 
- Cost-Effectiveness 


## Disadvantages of using firebase
- To handle less than 1 million connections
- To build simple apps
- Firebase is not made for processing complex queries
- Less support for iOS
- Android centred
- Platform-dependence
- Limited data migration
- Limited querying capabilities

## App Engine
- Create an application in Google App Engine
- Install App Engine SDK for python 
- Create an application folder
- Content of App Engine configuration(app.yaml)
- Test static pages
- Deploy

### Advantages of using App Engine
- fully manged platform for hosting web Applications 
- Hosting your static site on App engine can cost less than using a traditional hosting provider, as App Engine provides a free tier.
- Easy to add backend
- Version control. If you need it, GAE has inbuilt version control so you can test new versions before making them the default, and rollback to previous versions 

### Disadvantages of using Google App Engine
- Software Development Kit is required
- Although a benefit a lot of the time, there is no alternative, so if you just want to make a change to a CSS file and upload it, you have to deploy the whole site again. system downtime
- you need to create a skeleton configuration


### Links Used 
App Engine [https://www.fizerkhan.com/blog/posts/free-static-page-hosting-on-google-app-engine-in-a-5-minutes]

