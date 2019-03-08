---
title: Workflow - Review
keywords: BOADocProcess
sidebar: BOADocProcess_sidebar
summary: "The Documentation team uses Jira, Github, Git Bash and Flare when
updating online help content. This section describes that process, which
is driven by the Documentation Status field in Jira."
permalink: BOADocProcess_Workflow_Review.html
folder: BOADocProcess
toc: false
---
## PM Reviews and Approves Documentation

There are two sites for the hosted help, one for dev and one for prod.

Content is pushed to the dev site for testing when it's added to any \`develop\_xxx\` branch. So pushing to \`develop\_70\` will add content to the dev site for online help for version 7.0.

For prod, the build tools are watching the \`develop\` branch. That's where the latest version of the documentation lives. In order to ensure that only the intended pushes to \`develop\` go to prod and to the right version, the build tools are only watching and pushing updates that have been merged.

So when branch \`develop\_70\` is merged into \`develop\`, Jenkins checks for the commit message, checks that \`develop\_70\` has been merged, and pushes to version 7.0 in prod.

Documentation is built on a Jenkins node server and takes a bit of time. From the moment a commit is made to when it becomes available is roughly 10 minutes, give or take. This is for both dev and prod.

{% include tip.html content="You may also need to clear your cache or open an incognito window to see updates." %}

When the Author gets an email that the content has been merged, she updates the Documentation Status field to Review, and @ mentions PM on the ticket.

PM confirms that new and updated features are described completely and correctly from a user's perspective.

Either:

-   PM approves the content by setting the Documentation Status field to Approved.

Or

-   PM notes on the Jira ticket what needs to be updated, and the process begins again at the In Process step.
