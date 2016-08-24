# fizzbuzz-model
A simple model to be published to the local Ivy cache.

## Build & Publish Locally
1. Clone this repo
2. Make sure you have Ant installed correctly
3. In a terminal, navigate to the cloned directory
4. Run `ant publish`
5. Inspect your local Ivy repository (`~/.ivy2/local/hotmeatballsoup/fizzbuzz-model`) to verify it has been published
6. Now, go to the [**fizzbuzz-app**](https://github.com/hotmeatballsoup/fizzbuzz-app) that depends on this model and follow the instructions in its README

## Ant/Ivy Setup
### Ant
First, lets see if your Ant exists. From a terminal, run:

> echo $ANT_HOME

If nothing shows up, navigate to this cloned repo and run `ant clean`. If you get errors, you don't have Ant installed. To install Ant, run:

1. `curl -s "https://get.sdkman.io" | bash`
2. `sdk install ant`

Now verify that `echo $ANT_HOME` produces successful output.

### Ivy

Ivy will be automatically installed by the build if it does not exist.

