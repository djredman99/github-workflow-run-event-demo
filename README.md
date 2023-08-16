# Workflow_run event demo
Repo to show the behavior of the workflow_run event trigger

The workflow_run trigger will only trigger a workflow that exists on the default branch.  It can be triggered by workflow runs on other branches, but the default branch version of the workflow being called is the version that will run, even if it exists on the branch that triggered it.

- *The Main* is the triggering workflow.  This can be run on either the main or branch-one branches.

- *Workflow-One Triggered by Other* will trigger on the completion of *The Main*

- *Workflow-Two Triggered by Other* will also trigger on the completion of *The Main* but will determine the branch that *The Main* ran on and use that info in the checkout action to switch to/checkout the branch that triggered the run.  This will not run the branch specific version of the workflow, but will allow for building, etc. of all code on the triggering branch.


### I am the Readme on the MAIN branch
