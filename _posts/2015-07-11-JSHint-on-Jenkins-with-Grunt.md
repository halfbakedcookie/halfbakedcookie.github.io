---
layout: post
title: JSHint on Jenkins using Grunt
description: "View the results of JSHint on your Jenkins CI evironment"
modified: 2014-10-20
tags: [JavaScript, Jenkins, CI, JSHint, GruntJS]
image:
  feature: post01/Jenkins_Grunt_Logos.jpg
comments: true
share: true  
---

A few weeks back we had a hackathon with the idea of improving the aspects of our customer projects in different disciplines like unit testing, UI test automation, code quality, etc. The job of implementing a code quality check for our client-side code fell on me. I chose to use [JSHint](http://www.jshint.com/) for the task.
The idea I had was to integrate JSHint as a post build task when we run our automated builds in Jenkins and then once the build is done display the results of the quality check.
My idea was as follows: 
<br/>

1.  Install JSHint on [Grunt](http://www.gruntjs.com).
2.  Execute it once the build completes.
3.  Find a plugin to easily view results.
<br/>
<br/>

For the purposes of this tutorial I would be integrating this to a .NET web application.

### 1.   Install JSHint on Grunt

Before JSHint is installed on Grunt, we need to install Grunt. Grunt runs a top of NodeJS, if NodeJS is not installed on your system, please download and install from [here](nodejs.org/download/).
Assuming the Node exists on your system, we move on to installing Grunt. 

 1. Install the Grunt CLI globally
 2. Install Grunt in your project location
 3. Install the JSHint Grunt plugin

{% highlight css %}
npm install -g grunt-cli
{% endhighlight %}

If you are running Node for the first time, then chances are that your project does not have node initialized, this [link](https://docs.npmjs.com/cli/init) shows you how it's done. Now navigate to your project root directory and install Grunt

{% highlight css %}
npm install grunt --save-dev
{% endhighlight %}

{% highlight css %}
npm install grunt-contrib-jshint --save-dev
{% endhighlight %}

### 2.   Install JSHint Reporting Plugin for Jenkins