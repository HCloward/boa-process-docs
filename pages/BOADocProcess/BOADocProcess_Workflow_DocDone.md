---
title: Workflow - Doc Done
keywords: BOADocProcess
sidebar: BOADocProcess_sidebar
summary: "The Documentation team uses Jira, Github, Git Bash and Flare when
updating online help content. This section describes that process, which
is driven by the Documentation Status field in Jira."
permalink: BOADocProcess_Workflow_DocDone.html
folder: BOADocProcess
---
## Change status

Once approved, the Author moves the **Documentation** Status to **DocDone**. Open a PR to merge the changes to the production site. Refer to Update the Production Site when Documentation is Approved.

## Update the Help on the Dev and Prod Sites

Each release has a branch in the dsp-docs repo with the naming convention develop\_nnn, where nnn is the release number (develop\_701, for example). When a pull request is merged to that branch, a Technical Writer logs in to Jenkins and builds the helpn.

The URL for the full version is:

> https://dsphelpdev.boaweb.com/nnn/general/Home.htm

The URL for the Solex version is:

> https://dsphelpdev.boaweb.com/nnn/solex/Home.htm

The URL for the prod full help is:

> https://dsphelp.boaweb.com/nnn/general/Home.htm

For Solex:

> https://dsphelp.boaweb.com/nnn/solex/Home.htm

{% include links.html %}

To update the help on the sites:
1.  Log in to Jenkins.
2.  In the Name column, click DSPDocs.
3.  Click  the Schedule a Build icon for either DSPDocDev or DSPDocProd.
4.  Enter the version number in the VERSION field.
5.  Click Build. 
The build status displays in the left column under Build History. 

## Update the DSP Landing Page

Each release the DSP Landing Page's index.htm needs to be updated with a new release links for the general and solex versions of the Help and What's New. If a user enters an invalid url for the help, this page displays, listing all available versions of the product. 

To update the index.htm page:
1. Open the **DSPLandingPage** folder in the Root of the **dsp-docs** directory.
2. Open **index.html** in a text editor like VS Code or Atom.
3. Around lines 68 and 86, you will see the general links to the What's New page and the Help. Add links to the new release in the same format as the prior release.
4. Around lines 111 and 130, you will see the solex links to the What's New page and the Help. Add links to the new release in the same format as the prior release. 
NOTE: Not every release is sent to SAP. There may be releases of BOA help without corresponding SAP help releases. 
5. Save your work.
6. Stage it for commit, commit it, and push it to the remote.
