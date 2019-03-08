---
title: Workflow - In Process
keywords: BOADocProcess
sidebar: BOADocProcess_sidebar
summary: "The Documentation team uses Jira, Github, Git Bash and Flare when
updating online help content. This section describes that process, which
is driven by the Documentation Status field in Jira."
permalink: BOADocProcess_Workflow_InProcess.html
folder: BOADocProcess
---

Technical Writers begin work on tickets as soon as possible after the ticket has made it past User Story review and completes the draft content in Flare.

When writing content, the TW communicates with PM/Dev as needed to ask questions, get clarification etc. The TW must provide information on the Jira ticket about where to find the updates in the Help system. It may be necessary to generate a Google document to show the updates. Both PM and the Peer Reviewer rely on this information, so it is vital that it is included.

{% include important.html content="Always use Git Bash. Do not use the **GitHub Desktop** application." %}

## Synchronize your release branch with the BackOfficeAssoc GitHub Repo {#draftcontent}

{% include warning.html content="You **MUST** perform these steps each time you checkout a branch to ensure you are working in the latest copy of the release branch." %}

1.  In Windows-Explorer, right-click on your dsp-docs local folder and select **Git Bash Here**.
    {% include image.html file="gitBashHere.png" alt="Right-click menu with Git Bash Here option" caption="Right-click menu with Git Bash Here option" %}
2.  Switch to the release branch you are working in now, for example, develop\_67.
    <div markdown="span" class="alert alert-info" role="alert"><i class="fa fa-info-circle"></i> <b>Note:</b> The git command to switch to the release branch is <code class="highlighter-rouge">git checkout &lt;release branch name&gt;</code>.</div>
3.  Enter the git command, `git pull origin <release branch name>`
    {% include tip.html content="If at this point you wish to see a list of branches that are available in your local repo, enter the command `git branch`. All of the available local branches are listed." %}

## Create a branch for your updates based on the release branch

1.  Navigate to the release branch in Git Bash if you are not already in it.
2.  Enter the command `git checkout -b \<new branch name\>`
    {% include note.html content="Name the branch after the JIRA ticket number if applicable. Use the naming convention DSP-NNNN. If changes are not related to a Jira ticket, give the branch a meaningful name, such as 'releasenotesupdates'." %}
3.  Open the project in Flare and make your updates and your updates are saved on the correct branch.
4.  When you finish your updates, save your changes and **close Flare**.

## Commit updates locally and push them to the BackOfficeAssoc GitHub Repo dsp-docs {#commitlocally}

1.  Return to Git Bash or open a new session.
2.  Navigate to your repo, and make sure you are in the correct branch. It is in parenthesis after your prompt.
3.  Enter the git command `git status` to see all of the changes you have made.
    {% include note.html content="If you do not see your changes, you may have forgotten to save or you are in the wrong branch." %}
4.  Stage the updates for commit by entering the git command `git add .`
    {% include note.html content="Include the period in the command." %}
    {% include tip.html content="Comments change from red to green after you stage them." %}
5.  Commit staged updates by entering the command `git commit -m "<commit message that informs everyone what you have done>"`
    {% include note.html content="Do not use special characters in message." %}
6.  Push your changes to the remote by entering the command `git push origin <new branch name>`
    {% include tip.html content="Now your new branch is visible on GitHub and available for others to access for review." %}

## Open a pull request for a peer reviewer to review your work {#openPR}

1.  Go to GitHub.com and click the **Compare and pull request** button next to your recently pushed branch.
2.  Make sure the **base** is the current release branch you are working in and **compare** is your new branch name.
    {% include image.html file="githubPR.png" alt="GitHub PR, base and compare branches" caption="GitHub PR, base and compare branches" %}
3.  Add notes and a reviewer to the pull request and click the **Create pull request** button.
    {% include note.html content="Message the reviewers in Slack with link to PR." %}
4.  Add the PR URL to the Jira ticket.
5.  Update the **Documentation Status** on the JIRA ticket to **Peer Review**.