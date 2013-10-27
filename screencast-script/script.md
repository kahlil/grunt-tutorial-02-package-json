-- slide 1

# Grunt
## The Basics: package.json

## Script

Hi welcome to Grunt Basics. My name is Kahlil and I will guide you through creating a package.json file.

What is a package.json?

Well, let's first have a look at what we can find on gruntjs.com: http://gruntjs.com/getting-started#preparing-a-new-grunt-project

-- slide 2

> **package.json:** This file is used by npm to store metadata for
> projects published as npm modules. You will list grunt and the
> Grunt plugins your project needs as devDependencies in this file.

So here we have two sets of information: 1. what the package.json normally is used for and 2. what it is used for in Grunt.
I will expand on that a little later. So further it says:


> ## package.json
> The package.json file belongs in the root directory of your project,
> next to the Gruntfile, and should be committed with your project
> source. Running npm install in the same folder as a package.json
> file will install the correct version of each dependency listed
> therein.

This is part of why the package.json is important for Grunt. gruntplugins get stored as devDependencies and then can be installed via npm install. Which is especially important if you work in a team.

There is another reason why the package.json is useful for Grunt: Grunt can actually consume the information in the package json and use the values in it's grunt tasks. ie. it will use the version number, license information and author name to insert them in a banner for your minified files.

Next on the site, it goes on to list the ways how you can create a package.json for your project.

-- slide 3

* the first option is when you use the scaffolding tool grunt-init, most of the templates will create a project-specific package.json file. This is actually also true for Yoeman. So when you use one of those scaffolding tools there is nothing else to do, you have your package.json.

* the second option is npm init on the command line which allows you to create a basic package.json file.

-- slide 4

* and the third option is just to copy and paste a little snippet of code that can be used as a starting point













