---
title: Workflow - Status Field
keywords: BOADocProcess
sidebar: BOADocProcess_sidebar
summary: "The Documentation team uses Jira, Github, Git Bash and Flare when
updating online help content. This section describes that process, which
is driven by the Documentation Status field in Jira."
permalink: BOADocProcess_Workflow_StatusField.html
folder: BOADocProcess
---
## The Documentation Status Field
Used by the Documentation team only, the Documentation Status field defines where the content for that JIRA ticket is in the workflow.

{% include important.html content="[GitHub Initial Setup][BOADocProcess_GitInitSetup] contains the initial
configuration and setup steps for Git and GitHub. These steps must be
performed by a new employee." %}

The Documentation Status field contains the following values:
-   **Not Started** --- Default value. No work has been done on the
    ticket except for initial assignment in the Writer Assigned field
    and an estimate in the Documentation Hours Remaining field.
-   **In Process** --- Technical writer researches and writes draft
    content and adds it to Flare.
-   **Peer Review** --- Technical Writer reviews content added to help.
-   **Review** ---PM/Dev is reviewing content.
-   **Approved** --- Content has been approved by PM.
-   **Doc Done** --- Doc is complete.

{% include tip.html content="A checklist of the steps in this process is included in the appendix, [Checklist for DSP Documentation Workflow][BOADocProcess_CLDSPWorkflow]." %}

## No Documentation Required

If the ticket does not change or require new documentation, add a comment on the ticket stating that documentation is not required. Update the **Documentation Status** field to **Doc Done**.

## Assign Ticket and Set Documentation Status

The **Writer Assigned** and **Documentation Status** fields must be complete for all tickets requiring documentation in the DSP project.

Technical Writers review tickets when they are added to the board and assign the tickets as appropriate, either to themselves or other team members.

To assign a writer:

1.  Click the **Edit** button on the ticket.
2.  Select the writer in the **Writer Assigned** list box.
3.  Set the status in the **Documentation Status** field.
4.  Click **Save**.
