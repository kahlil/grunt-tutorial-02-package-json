-- slide 1

# Grunt
## The Basics: package.json

## Script

Hi welcome to Grunt Basics. My name is Kahlil and I will guide you through creating a package.json file for your Grunt project.

What is a package.json?

Well, let's first have a look at what we can find on gruntjs.com: http://gruntjs.com/getting-started#preparing-a-new-grunt-project

-- slide 2

> **package.json:** This file is used by npm to store metadata for
> projects published as npm modules. You will list grunt and the
> Grunt plugins your project needs as devDependencies in this file.

So here we have two sets of information: 1. what the package.json is normally used for and 2. what it is used for in Grunt.
I will expand on that a little later. So further it says:


> ## package.json
> The package.json file belongs in the root directory of your project, next to the Gruntfile, and should be committed with your project
> source. Running npm install in the same folder as a package.json
> file will install the correct version of each dependency listed
> therein.

This is part of why the package.json is important for Grunt. gruntplugins get stored as devDependencies and then can be installed via the command 'npm install' on the command line. Which is especially important if you work in a team.

There is another reason why the package.json is useful for Grunt: Grunt can actually consume the information in the package json and use the values in it's grunt tasks. For instance, Grunt can use the version number, license information and author name to insert them in a banner for your minified files.

Next on the site, it goes on to list the ways how you can create a package.json for your project.

-- slide 3

* the first option is when you use the scaffolding tool grunt-init, most of the templates will create a project-specific package.json file. This is actually also true for Yoeman. So when you use one of those scaffolding tools there is nothing else to do, you have your package.json.

* the second option is npm init on the command line which allows you to create a basic package.json file.

-- slide 4

* and the third option is just to copy and paste a little snippet of code that can be used as a starting point

-- slide 5

Now I am going to show you how to create your package.json on the command line with npm init.

-- Open your terminal of choice.
-- Type in npm init and hit return.
-- As you can see npm gives you a nice explanation of what is going to happen
-- First it wants to know the package name. It has to be a url-friendly name in order to be valid.
-- Next npm wants to know the version number. Usually you would choose something like 0.1.0 or 0.0.1 to start with.
-- You don't need a description for your Grunt project so we skip that.
-- Same goes for the entry point and the test command.
-- On the next one we can insert the link to the Git repo of the project if we have one.
-- If your project is a gruntplugin or a bower component or an npm module you should enter relevant keywords for the keywords property. It will be used in search after you published your project.
-- Now fill in your name and which license your are using and we're done!

npm then shows you a nice little summary that you confirm with yes.

Then open up the package.json file in your favorite editor.
As you can see there is a bunch of stuff in there we don't need. Throw out "main", "scripts" and "description" and add the "devDependencies"-property and we are done.

Now when you install Grunt plugins use the --save-dev option to store the plugin as a development dependency. This way you can just commit your package.json to version control and quickly install all the plugins you need with `npm install`.

-- Last slide

Thanks for checking out Grunt Basics. If you have any questions let us know on Twitter or on IRC in the #gruntjs channel on #freenode.




