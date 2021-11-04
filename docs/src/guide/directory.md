# Directory Structure

A manuscript root is just a folder with a `.manuscript` file in it.

A new composer root can be created by running `manuscript init` from a folder. 

When you create a manuscript root, two folders will be created also, unless they already exist:

 - ./playgrounds/
 - ./packages/

## .manuscript file
The mere presence of this file is what tells manuscript that the directory is a "manuscript root".

It is also used as a way to store a json configuration for this manuscript root.

At the moment the only configuration that will be set is your Github Personal Access Token, if you set one.

## playgrounds
All the framework playgrounds that manuscript creates for you will be placed into this folder.

**These playgrounds are disposable**.

When you run `manuscript play` from inside one of your packages, you will be able to create a new playground, as 
well as choose from any existing ones to install your package in to.

You can clear out this folder at any time by using the `manuscript clear-playgrounds` command. **This will have no 
effect on your packages**.

## packages
All of your own packages you are working on will be added to this folder when they are created using the `manuscript 
create` command.

*Note: I might be adding a command to help clone an existing repository from github into your manuscript packages 
folder. But you can still just do that manually: `cd ./packages && git clone ***etc***`.*
