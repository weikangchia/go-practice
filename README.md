# Go Practice

This is a repo to store the stuff I learn for Go programming language. This web application is hosted on Google App Engine (Standard).

## Download
* IDE: [Webstorm](https://www.jetbrains.com/webstorm/)
* Paas: [Google App Engine Standard](https://cloud.google.com/appengine/)
* App Engine SDK for Go: [https://cloud.google.com/appengine/docs/go/download](https://cloud.google.com/appengine/docs/go/download)
* Go: (https://golang.org/dl/)[htt

## Test the application
* From the working directory, run the following command to compile the app and start the development server:<br/>
`goapp serve .`<br/>
  The development server is now running, listening for requests on port 8080.<br/>
  Troubleshoot: Run `goapp help serve` or see [Using the Local Development Server](https://cloud.google.com/appengine/docs/go/tools/using-local-server) for more information.
* Visit [http://localhost:8080/](http://localhost:8080/) in your browser to see the app in action.

## Making a change
The development server watches for change in your project files. As you update your source, it recompiles them and relaunches your local app. There's no need to restart `goapp`.

## Deploy the app
To deploy your app to App Engine, you will need the ID of your Cloud Platform project.<br/>

1. Create a new Cloud Platform project and App Engine application using the Cloud Platform Console: [Go to App Engine](https://console.cloud.google.com/projectselector/appengine/create?lang=go&st=true&_ga=1.42187041.58596247.1471093802)<br/>
When prompted, select the [region](https://cloud.google.com/appengine/docs/locations) where you want your App Engine application located. After your App Engine application is created, the <b>Dashboard</b> opens.
2. Note the project ID that you created above.
3. Upload your application to App Engine by running the following command from the `helloworld` directory where your `app.yaml` file is located:<br/>
`goapp deploy -application [YOUR_PROJECT_ID] -version [YOUR_VERSION_ID] .`
4. Your app is now deployed and ready to serve traffic at `http://[YOUR_PROJECT_ID].appspot.com/`.
