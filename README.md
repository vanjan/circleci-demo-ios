# ios-game

[![CircleCI](https://circleci.com/gh/CircleCI-Public/circleci-demo-ios/tree/master.svg?style=svg)](https://circleci.com/gh/CircleCI-Public/circleci-demo-ios/tree/master)

## Setup

1. `sudo gem i bundler -N`
1. `bundle install --path .bundle`
1. Add your team data to `fastlane/Appfile`
1. Set up environment variables
   
   `fastlane` requires some environment variables set up to run correctly. In particular, having your locale not set to a UTF-8 locale will cause issues with building and uploading your build. In your shell profile add the following lines:
   
   ```
   export LC_ALL=en_US.UTF-8
   export LANG=en_US.UTF-8
   ```
   
   You can find your shell profile at `~/.bashrc`, `~/.bash_profile` or `~/.zshrc` depending on your system. 
1. `bundle exec fastlane scan` to build the app and run tests
1. `bundle exec fastlane match init` to set up code signing via Fastlane
   Match
1. Push the changes
1. Create a CircleCI project for the repository
1. Edit the `.circleci/config.yml` file as needed
1. Done