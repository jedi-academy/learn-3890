# Workflows (CodeIgniter)
ACIT3890 - BCIT - Fall 2019

## codeigniter4

- PR -> CI
- push/merge to develop -> docs, man changelog
- push/merge to master -> N/A
- release -> release

- CI: travis-ci (phpunit x9, coverage)
- docs: sh, optional staging
- release: man changelog, PR, merge to master, release-build sh, vet, release-deploy
    - codeigniter4, framework, appstarter, userguide
    - packagist

## translations

- PR -> CI
- push/merge to develop -> man changelog & readme
- push/merge to master -> N/A
- release -> release

- CI: travis-ci (phpunit)
- release: man changelog & readme, merge to master, man tag
    - packagist

## website

- PR -> N/A
- push/merge to develop -> stage
- push/merge to master -> N/a
- release - release

- stage: man staging
- release: man update site
    - dep on guides & download data

