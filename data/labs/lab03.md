# Lab #3 - Collaborative Workflow
ACIT3890 - BCIT - Fall 2019

## Lab Goals

This week, you will be practicing collaborative workflow.

## Lab Process

At the beginning of lab, we will clarify if individual or team.

Team members could have one or even two roles to play:
- One member will be the creator and maintainer of the team repo - he/she will be designated the CAPTAIN
- The other members of the team will be contributors
- If a team has fewer than four members, then the captain will also be a contributor


## Lab Submission

Submit a readme *text* file, or a submission comment, to the lab dropbox. 
It should contain a link to your **team**'s github repository,
and should provide the github username. you used. 

Due: this Sunday at 17:30

I hope this can be completed during lab time!

## Lab Marking Guideline

A marking rubric will be attached to the lab 3 dropboxes.


## Lab Prep

I asked, in the course hub news, that each student setup their GPG
signing.

## The starter project

The [starter project](https://github.com/jedi-academy/acit3890-lab03) includes three lists, each stored as a simple text file,
with one word or phrase per line. 

- `adjectives` is a list of buzzword-worthy adjectives, like empowering
- `material` is a list of buzzword-worthy materials, like dilithium
- `tech` contains a list of buzzword-worthy technology components, like gizmo

The `index.php` will pick a word from each list, in order
to propose a buzzword-friendly technology that a company might be claiming to pursue 
or implement, eg. a "rare dilithium crystals"


# Round 1

## Contribute to Each List (Contributors)

- Create & checkout a feature branch, based on develop, for one small contribution
- Add three words to one of the lists, keeping the list ordered
- Add & commit this change

        git add .
        git commit -S -m "??"

- Push your branch to your repo
- Open a pull request for it to the team repo

Repeat the above for each of the other lists

## Consider PRs (CAPTAIN)

Review the PRs, one at a time, in submission sequence:

- If they are not properly signed, close them with a suitable comment
- If they are mergeable and acceptable, merge them
- If they are mergeable but not acceptable, explain why in a comment 
(could be out-of-order, inappropriate language)
- If they are not mergeable, ignore them

Repeat

## Fix Your PRs

For each PR that is rejected or not mergable,
synch your develop branch & fix your feature branch (see the cheatsheet)

Repeat until your feature branches have been merged or abandoned.

## Release (CAPTAIN)

- Tidy up any loose ends in the repo
- Merge the develop branch into the master branch, in the team repo
- Create a v1.0 release on github, from master

## Synchronize with team (ALL)

- Synchronize your repos with the team repo

        git checkout master
        git pull upstream master
        git push origin master
        git checkout develop
        git pull upstream develop
        git push origin develop

- Remove dead branches

# Round 2

Same as round 1, except each team member's three PRs will
each be for two lists.

The release for this will be v2.0

# Round 3 (if needed)

Same as round 2, except each contributor should prepare
two PRs, each of them changing all three lists

The release for this will be v3.0

# Conclusion

That's all, folks!