# Lab #5 - Agile Development
ACIT3890 - BCIT - Fall 2019

This lab uses Pivotal Tracker for agile project
management, integrated with the project's Github repository.

## Lab Submission

Submit links to your team's github repo and tracker project.

Identify the following for me to look at:

- open issue (done in github)
- open issue with a PR (done in github)
- closed issue from PR merge (done in github)
- closed issue without PR (done in github)
- open story  (done in tracker)
- completed story  (done in tracker)

You may need screenshots - we will determine that in lab.

Due: this Sunday at 17:30

A marking rubric will be attached to the lab dropboxes.

# The Lab

## Team

Form a team, and join the same `agile` group.

Team roles:
- repo master - admin for the team repo
- tracker master - admin for the team tracker project
- worker bee (if 3 members) - "work" completion through PRs

## Github

Create an organization for your team, and a repo inside that organization.

The repo is not meant to be a real project, as the focus is on the
agile project management and not a deliverable.
I suggest using a copy of `jedi-academy/acit3890-lab03` (not a fork).

## Tracker

Sign up for a free (trial) pivotaltracker.com account.

The tracker master should create a project and invite the other team members
to it. The project can be pubklic, or you should invite me (jparry1@bcit.ca) to it.

## Integrate

Setup integrations between the github repo and tracker project.
This will involce both the repo master and the tracker master.

Integration specifics:

- creating a github issue should create a tracker story
- submitting a PR for an issue should update the related story status
- merging a PR for an issue should complete and advance the related story
- closing an issue should complete the related story
- creating a story should create a github issue
- concluding a story should close the related issue

It will probably take a few go-rounds to get it right. 
Not a problem, as you will be designating the issues and stories that you want considered
for marking.

## First sprint

- Create 4-5 issues (github) and 3-4 stories (tracker). That will result in 7-9 issues and stories.
- Complete 2-3 of the issues (any) and 1 of the stories (tracker).
- Submit PRs for 2 more issues (any).

You should have about 5 open issues, of which 2 are being worked on.

## Second sprint

- Create 4-5 issues (github) and 3-4 stories (tracker). That will result in 11-16 open issues and stories.
- Complete 4-5 of the issues and 2 of the stories.
- Submit PRs for 2 more issues.

You should now have about 8 open issues, 4 of which are being worked on.

## Notes

- You might need a zapier.com "zap" for one direction of the integrations.
- Yes, this is arbitrary ... focus on the project management and how the integration
is proceeding.
