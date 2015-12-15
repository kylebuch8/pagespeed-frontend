# Page Speed Viewer

Want to put a front-end on your OpenShift Page Speed backend?

Look no further.

![Page Speed Viewer Screenshot](https://cloud.githubusercontent.com/assets/330256/11816907/90674ff4-a320-11e5-8668-25914f0320f2.png)

![Page Speed Viewer Chart](https://cloud.githubusercontent.com/assets/330256/11817256/233d9a62-a322-11e5-8005-d1560af2dd83.png)

This application was built using [Polymer](https://www.polymer-project.org/1.0/), [PolymerLabs App Layout](https://github.com/PolymerLabs/app-layout), [Chart.js](http://www.chartjs.org/) and [Moment.js](http://momentjs.com/).

## Getting Started
    npm install && bower install

    gulp serve

The application assumes that you are running the [OpenShiftPageSpeedApi](https://github.com/kylebuch8/OpenShiftPageSpeedApi) on http://localhost:8000. You can see the ajax calls being made in the ps-chart.html and ps-score.html elements.

### Deploying
You'll need to create a config.js file at the root of your application that looks like this:

    var config = {
        productionUrl:  'http://***yourproductionopenshiftapi.com***'
    };

    module.exports = config;

Be sure to point the productionUrl to your hosted instance of the OpenShiftPageSpeedApi.

Then run

    gulp

Then copy the contents of the dist directory to your server. Or you can do what I've done and use gulp-gh-pages to deploy the site to GitHub.
