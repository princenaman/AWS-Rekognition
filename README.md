# AWS-Rekognition

This is a demo which demonstrates the AWS 'Rekognition' face and image recognition API, as well as the 'Polly' speech synthesis API.

It uses the JPEG Camera library to take a photo from your PC/device onboard camera and send the facial data to Amazon for comparison and identification.

### Prerequisites

You will need Ruby installed on your development machine *(Note: NOT Ruby on Rails, just plain Ruby language)*.  This app uses the light weight Sinatra framework to do all the back end heavy lifting.

Before running this web app, you will need to set up a .env file in the project folder with your Amazon IAM key and secret.

```
export AWS_KEY=<your IAM key here>
export AWS_SECRET=<your IAM secret here>
```

If you are using Linux/OS X, then you can just run the above commands in your terminal or shell to set up the environment variables.  Windows users can type the following two lines into their DOS prompt:

```
export AWS_KEY=<your IAM key here>
export AWS_SECRET=<your IAM secret here>
```

If you are new to ruby / have an older version of ruby use

```
\curl -sSL https://get.rvm.io | bash -s stable --ruby
rvm install ruby-2.4.0
```

Gems required:

```
sudo gem install bundler
sudo gem install aws-sigv4 -v 1.0.0
sudo gem install jmespath
sudo gem install aws-sdk-core
sudo gem install aws-sdk-resources
sudo gem install aws-sdk
sudo gem install dotenv
sudo gem install rack
sudo gem install rack-protection
sudo gem install tilt
sudo gem install sinatra
```

Once that is done, you can install all dependencies by typing:

```
bundle install
```

Then run the web app by typing:

```
ruby faceapp.rb
```

This will start a local web server, listening on port 4567.  Then it is a matter of visiting the following URL in your web browser:

```
http://localhost:4567
```

### Reference
http://devan.blaze.com.au/blog/2017/3/13/building-a-face-recognition-app-in-less-than-an-hour
