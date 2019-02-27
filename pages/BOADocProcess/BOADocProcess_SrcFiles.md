---
title: Source Files for Manuals and Online Help
keywords: BOADocProcess
sidebar: BOADocProcess_sidebar
toc: false
permalink: BOADocProcess_SrcFiles.html
folder: BOADocProcess
---

The following source files are used to create images and tables in online Help and Manuals. The files are stored on OneDrive in the **Product Documentation/Source Files for Manuals** folder.

To update the files, make a copy and add the version number on the end. Then update the files and Manual and have the changes reviewed and approved by the person that requested the change.

-   Disk Layout charts\_Full.pptx
-   Disk Layout charts\_Full.pptx

The following Visio diagram is used to create images in the Flare topic "Add Data-Driven Dependency Conditions to a Category."
-   dspConduct Dependencies.vsd

# Check Latest Build for Changes
Tickets may describe a change that you need to see in the DSP in order to get a full understanding. 

{% include note.html content="If the ticket is merged during the day before about 6:30 pm, the ticket's changes will be available via the next day's BuildDeployTest link." %}

## Prerequisites

Before checking the latest build, you must perform these steps once to set up your jenkins account and join the correct Slack channel:

1. Contact Matt Moore to obtain Jenkins login credentials. 
2. Log in to [Jenkins](https://jenkins.boaqe.com). 
   {% include note.html content="Refer to Jenkin's [online resources](https://jenkins.io/doc/pipeline/tour/getting-started/) to learn more." %} 
3. Add yourself to the Slack channel for the latest development cycle. For example, the Slack channel for DSP 7.0.4 is #704dev.
   {% include note.html content="When Jenkins runs the QE tests, results are posted to this channel." %}

## To check the latest build for changes:
1. Navigate to the dev channel in Slack. 
   {% include note.html content="Refer to [Prerequisites](#prerequisites) on how to gain access to the dev channel in Slack." %} 
   {% include image.html file="CheckBuild1.png" alt="Click Jenkins test results link" caption="Click Jenkins test results link" %}

2. Click the most recent Jenkins test results link with 'BuildDeployTest' in the title to view the latest build; the Cucumber report opens.
   {% include note.html content="Do not click the link with 'BuildOnly' in the title." %}
   {% include note.html content="Jenkins publishes two different kids of notes to the Dev channel. Make sure to click the link after **Test results can be found at:**. You may have to log into Jenkins before proceeding." %}
   {% include image.html file="CheckBuild2.png" alt="Note the Jenkins build date" caption="Note the Jenkins build date" %}
3. Note the build date.
4. Open the Jira ticket that documents the change you are trying to view in the DSP. 
5. Open the GitHub pull request link listed in the **GITHUB DEV PR** field.
6. Check to see if the pull request has been merged. 

    a. If it _has not_ been merged, check back later.

    b. If it _has_ been merged, proceed to the next step in this process. 
7. Note the date of the latest merge. Hover over the time frame to see the date details.
   {% include image.html file="CheckBuild3.png" alt="Note the latest merge date" caption="Note the latest merge date" %}

	a. If the latest merge date is _after_ the Jenkins test build, the changes are not in development. Check the Dev Slack channel in a day or so for the latest build. 

	b. If the latest merge date is _before_ the Jenkins test build, the changes are in development. Proceed to the next step in this process. 
8. Return to Jenkins and click **App Site URL** to open the latest build site. 
9. Log in to the app site using credentials supplied by QE.
10. View changes outlined in the Jira ticket description. 

