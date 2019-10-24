# Lab #6 - Travis-CI
ACIT3890 - BCIT - Fall 2019

This lab will have you setup continuous integration for your copy
of the CodeIgniter website.

## Lab Submission

This is an individual lab.

Submit a link to your repo

Due: this Sunday at 17:30

A marking rubric may be attached to the lab dropboxes.

# The Lab

## 0. Prep

You have PHP7.2 already setup. 

There are two more tools you want to install on your machine:

- [Composer](https://getcomposer.org/doc/00-intro.md)
- [xdebug](https://xdebug.org/download) ... I suggest PHP 7.2 VC 15 (64 bit)

The first is for managing project dependencies, while the second
is used by PHPUnit testing.

**Xdebug notes** Easier install:

- `php -i > phpinfo`
- go to https://xdebug.org/wizard
- paste contents of "phpinfo" into the text area.
- custom install instructions for you will be supplied, eg.specific DLL
  to download, where to copy it, and the line in php.ini that needs to be changed.

## 1. Your repo

Create a public repo under your github account. The name isn't important, as this repo will be just an excuse
to set up CI. I suggets just having a license file in it to start.

Clone it locally, and then copy everything from your existing website 2 folder EXCEPT
the `.git` folder.

The default branch doesn't matter, but we will assume `develop` in this writeup.
You can take that into account when doing it yourself.

Once you are happy with your local repo, you can then
    
    git add .
    git commit -S -m "Lab 6 setup"
    git push origin develop

## 2. Something to test?

`website` actually comes with dependencies for phpunit, so we are good there.
It also comes with a default `phpunit.xml.dist` ... bonus!

The test code will come from the [CI4 translations](https://github.com/codeigniter4/translations)
repo, as we can benefit from something similar.

I suggest downloading the CI4 translations, and copying the `tests` folder inside your
website repo.

There is a `TranslationsTest.php` inside `tests/system/Language`.
It role, in CI4, is to look for missing or extra translation sets or translation keys,
amongst whatever localizations have been provided. We can do the equivalent here.

### 2a. App not CodeIgniter namespace

- Rename `tests/system` to `tests/App`.

- Rename the namespace in `TranslationsTest.php` to `App/Language`

### 2b. Fix the source of expected messages

- Inside `expectedSets()`, the folder to search should be renamed from
    '/vendor/codeigniter4/framework/system/Language/en/' to 'app/Language/en'.

- Repeat for `loadKeys()`

### 2c. Try it

From your project root, `vendor/bin/phpunit`

If necessary, we will pause here to fix anything in the tests.

### 2d. What is it doing?

## 3. A new PR is born

Create a new branch off develop

Make some interesting changes (or only 1) in the app files

add, commit, push the branch

-> what happened inside your repo?

### 3b. Create a PR from the new branch to develop

### 3c. Note the link to available travis-ci integrations!

## 4. Let's add Travis-CI to automate the unit testing

They have a [tutorial](https://docs.travis-ci.com/user/tutorial/).

The takeaway is that you login to https://travis-ci.org
with your github account and select the repo you want to
have CI.

### 4b. Configure Travis-CI

You *could* go through the different parts of the docs,
**or** you might notice that the translations repo has
a `,travis.yml` file that could be copied into our website repo :)

It isn't the most sophisticated, but suits our purposes.

## 5. CI??

Make another simple change in your open branch.
Add, commit & push it.

This time, Travis-CI should kick in on your github repo, and do its thing :)

## 6. And now?

The logical next step is to add a code coverage integration, in the general case.
That doesn't make sense for our website, by the way.

Coveralls is tightly integratd with github & travis, and would be a normal choice.

There are two integrations that would make sense here:

- a code quality analyzer (eg PHP code sniffer)
- a static security analysis (looking for vulnerable dependencies)

Remember the list of available Travis-CI integrations?
Find one of each of the above and integrate them too.

## 7 . So many branches or commits?

Looking at a PR, you can restart the Travis-CI with the current
PR by clocking on the correct link :)
