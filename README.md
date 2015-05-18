# cloudify-installer

a node tool to easily install cloudify and other goods


# Installation

```
sudo npm -g install cloudify-cosmo/cloudify-installer
```

 - The library supports auto-complete.
 - We test the library on ubuntu first.
 - You can also use this library as a dependency in your project.

## Autocomplete throws exception?

you can install the module with `--ignore-scripts` to ignore the autocomplete script on install

you can also run bash `enable_autcomplete.sh` from the module's base manually to enable autocomplete.

## Using from grunt

To use this module from grunt you need to do the following

 - install the module
 - add `grunt.loadNpmTasks('cloudify-installer');` - since the module does not have a name starting with `grunt-`
 - add the following configuration to Gruntfile

```
{
 cfy: {
      my_target: {}
  }
}
```

for more details regarding the tasks available, please see `tasks` folder.

# Installing cloudify with simple blueprint with installer

## Using Gruntfile

```
 cfy: {
     install: {
         'cmd' : 'run_script',
         'script' : '3.2.0/vagrant_install_simple/script.sh',
         'args' : [],
         options: {
             env: {

             }
         }
     }
 },
```
## Using Command-line

`cloudify-installer run_script -s 3.2.0/vagrant_install_simple/script.sh`

# Commands

See all commands by running `cloudify-installer --help`
