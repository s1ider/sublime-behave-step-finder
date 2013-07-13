# Sublime Text 2 plugin: behave Step Finder

This plugin supports developers to easily navigate to their behave steps.
Based on CucumberStepFinder (https://github.com/danielfrey/sublime-cucumber-step-finder)

It provides by now two commands

* One listing all steps in the open project and letting you choose
a step using the built-in mechanism for search.
* The second one letting you jump to the corresponding step by calling the "MatchStep"-Command when standing
on a step in the features file

#Installation
## Mac OSX (manual)
    cd ~/Library/Application\ Support/Sublime\ Text\ 2/Packages
    git clone git://github.com/s1ider/sublime-behave-step-finder.git behaveStepFinder

## Linux/Windows
Not tested yet. Contributions are welcome. If keyboard settings are provided, it should work.

## Package Control
Installation through [package control](http://wbond.net/sublime_packages/package_control) is recommended. It will handle updating your packages as they become available. To install, do the following.

* In the Command Palette, enter `Package Control: Install Package`
* Search for `behaveStepFinder`

## Usage
The default key-binding for "search" is `super + y`, respectively
`ctrl + super + m` for "match".
Change it if one is already used in your configuration

## Configuration
The following settings are available so far.

    {
       "behave_features_path"  :  "features",
       "behave_step_pattern"   :  ".*_steps.*\\.py",
       "behave_code_keywords"  :  ["given", "when", "then", "and","but"]
    }

The plugin looks for `behave_features_path` as a direct subdirectory of your project. Override this setting if your steps are located in a different subdirectory.

In the given features directory it uses the second setting for finding step-files recursively matching the `behave_step_pattern`

For finding the matching step, behaveStepFinder needs to know which are the behave-keywords. Since there are different keywords beside English, you can configure them in `behave_code_keywords`.
