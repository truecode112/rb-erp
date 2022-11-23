# Ruby on Rails Tutorial sample application


```
$ rails db:migrate
```

Finally, run the test suite to verify that everything is working correctly:

```
$ rails test
```

If the test suite passes, you’ll be ready to seed the database with sample users and run the app in a local server:

```
$ rails db:seed
$ rails server
```

## Deploying

To deploy the sample app to production, you’ll need a Heroku account as discussed [Section 1.4, “Deploying”](https://www.railstutorial.org/book/beginning#sec-deploying). 

The full production app includes several advanced features, including sending email with [SendGrid](https://sendgrid.com/) and storing uploaded images with [AWS S3](https://aws.amazon.com/s3/). As a result, deploying the full sample app can be rather challenging. The suggested method for testing a deployment is to use the branch for Chapter 10 (“Updating users”), which doesn’t require more advanced settings but still includes sample users.

To deploy this version of the app, you’ll need to create a Heroku new application, switch to the right branch, push up the source, run the migrations, and seed the database with sample users:

```
$ heroku create
$ git checkout updating-users
$ git push heroku updating-users:master
$ heroku run rails db:migrate
$ heroku run rails db:seed
```
