# Warning! This repo is not yet ready for public use, we've made it public as part of our testing of its functionality. Please wait until this warning is removed before attempting to use it.

# VPM Package Listing Template

Starter for making your own Package Listings, including automation for building and publishing them.

Once you're all set up, you'll be able to update the `source.json` file, and generate a listing which works in the VPM for delivering updates for all the listed packages.

## ▶ Getting Started

Press [![Use This Template](https://user-images.githubusercontent.com/737888/185467681-e5fdb099-d99f-454b-8d9e-0760e5a6e588.png)](https://github.com/vrchat-community/template-package-listing/generate)
to start a new GitHub project based on this template, and follow the directions there. 

## Setting up the Automation

TBD

## 📃 Rebuilding the Listing

TBD

## 🏠 Customizing the Landing Page

TBD

## Technical Stuff

You are welcome to make your own changes to the automation process to make it fit your needs, and you can create Pull Requests if you have some changes you think we should adopt. Here's some more info on the included automation:

### Build Listing
[build-listing.yml](.github/workflows/build-listing.yml)

This is a composite action which builds a vpm-compatible [Repo Listing](https://vcc.docs.vrchat.com/vpm/repos) based on the items you've added to your `source.json` file. you've created. In order to find all your releases and combine them into a listing, it checks out [another repository](https://github.com/vrchat-community/package-list-action) which has a [Nuke](https://nuke.build/) project which includes the VPM core lib to have access to its types and methods. This project will be expanded to include more functionality in the future - for now, the action just calls its `BuildRepoListing` target, which calls `RebuildHomePage` when it completes. If you wanted to make an action that just rebuilds the home page, you could call that directly instead - just copy the existing call and replace the target names.

## Status
![GitHub deployments](https://img.shields.io/github/deployments/vrchat-community/template-package-listing/github-pages?label=Generate%20Listing)
