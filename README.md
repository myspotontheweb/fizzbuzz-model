# fizzbuzz-model
A simple model to be published to the local Ivy cache.

## Build & Publish Locally
1. Clone this repo
2. Make sure you have Ant and Ivy installed correctly; if not follow the steps below under the **Ant/Ivy Setup** section
3. In a terminal, navigate to the cloned directory
4. Run `ant local-publish`
5. Inspect your local Ivy cache (typically `~/.ivy2/cache/hotmeatballsoup/fizzbuzz-model/`) to verify it has been published
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
Run a `ls -al` on your Ant lib directory like so:

> ls -al $ANT_HOME/lib

Look for an Ivy jar, such as `ivy-2.4.0.jar`. If you don't see one, run

1. `curl -O "http://www.webhostingjams.com/mirror/apache//ant/ivy/2.4.0/apache-ivy-2.4.0-bin-with-deps.tar.gz"`
2. `tar -xvf apache-ivy-2.4.0-bin-with-deps.tar.gz`
3. Copy all the jars inside of it to `$ANT_HOME/lib`

If something gets botched in that process, you can just manually download the archive directly from Ivy's [download site](http://ant.apache.org/ivy/download.cgi), just make sure to get the archive "with deps".
