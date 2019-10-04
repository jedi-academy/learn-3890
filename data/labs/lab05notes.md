# Lab #5 - Agile Development - NOTES
ACIT3890 - BCIT - Fall 2019

Lab 5 presented some challenges in class. I have done a bunch of investigating, and have the following to report:

## Endless Loop

Many (most?) of you were experiencing an endless loop after setting up zaps to create
a new issue when a story was created, and another to create a new story when an issue
was created.

New issue -> new story -> new issue -> new story -> ...

The solution to this in the zap setup.

When you create a zap to create a new story from a new issue, you can specify
a label to use as a filter for new issue selection.
Labels need to be defined in your repo, and you might want one called "track".

Then, when a new issue is created, make sure the developer knows to select the
"track" label (as well as any other that might apply).

Going the other way, from a story to an issue, part of the new issue setup that
you can influence is the label to attach to the new issue. Setup the label in
github first. You might use "tracked", for instance. That tells the github viewer
that that issue came from pivotal tracker, and you won't have the endless loop.

## Tracking completions

This gets trickier, and it looks like it has to be done in github.
The commit message which utimately fixes or closes an issue needs to be
tagged, with the hashed tracker ID in square brackets.

An example: Resolves #44 [(fixes)#324324]

The #44 above refers to an issue, while the 324324 refers to a story.

Clunky? yes, unfortunately.

## Clunky, ew?

Having to tag issues is a problem. The access needed can be a problem too -
you don't want to have to set up dozens of collaborators with read access.

I suspect most developers will continue like they always have, and you will
end up with a bunch of issues resolved in github but not in tracker. Yuck!

One obvious solution is to have a formal role of "tracker master", namely
someone whose job is sifting through issues and stories and seeing which
can be closed.
One of my students a couple of years ago had just such a job for their co-op term,
and it was hell.

Lots of organizations use pivotal tracker, and if they are large enough they
can afford this. Not so much smaller or open source projects.

## What Does Pivotal Think?

Pivotal Tracker actually made a major change to their github integration this past
spring. Their intent is that a story correspond to a feature branch.
They expect an integrated organization to create a branch in github, for each story,
with the story ID being part of the branch name, eg. 324324-integrate-bootstrap5

This would need to be done by someone with access to the story metadata, but once
done regular developers wouldn't have to know anything about it. Commits etc
to that branch are automatically passed on to the tracker story.

What about gitflow?? Normal gitflow has developers making feature
branches in their forked repos, not in the team one. The Pivotal strategy here
has feature branches created in the team repo. Oh dear, so much for master & develop.

To be fair, some organizations use github that way, using a "modified gitflow".
It doesn't prevent developers from creating branches in their forks and working
there, submitting PRs from their repo to the team's develop branch. This work,
however, would not show in the tracker board until the PR came in, and only it the
PR and/or the commits in it were tagged with tracker story IDs.

## Help me, Obiwan!

There is hope. I stumbled across zenhub.com, which provides a browser app (for
Firefox or Chrome) or mobile app, that presents a project management view
for github repos. Think the visual appeal and usability of tracker, but working
directly on/with the github repo. No third party integrations needed.

It can bundle multiple repos together into a project management workspace,
and multiple workspaces can address different planning/tracking needs (eg kanban, scrum,
executive).

It's free for public repos, and developers can login to the app with their
github credentials and view projects even if they don't have write permission
for them.

This app impressed me enough to signup for it, and I hope to find some time over the next
few weeks to get familiar enough with it to use it for the CodeIgniter project.

## Alternatives?

It might be possible to configure your zaps to reduce some of the inconveniences
above, by using fields. For instance, instead of a new story/issue being called "new story",
use the description or title field of the source issue/story.

Failing that, you will need to carefully tag or label issues/stories before 
triggering an update across apps.

## Cut Us a Break?

You don't need screenshots.

You need to identify the source and target IDs of the integrations.

I suggest using zaps alone - they have the granularity we are looking for.

So, six zaps, with the endpoints identified.

## Alternative?

If you would like to investigate zenhub instead, that is fine.
There would not be any integrations, but you would still identify the four issues
that you made in github (two open, two closed, per the specs), and the two
issues you made in zenhub.

I would need your github repo and zenhub workspace links.
