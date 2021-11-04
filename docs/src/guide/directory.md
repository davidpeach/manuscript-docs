# Directory Structure

A manuscript root is just a folder with a `.manuscript` file in it.

A new composer root can be created by running `manuscript init` from a folder. 

When you create a manuscript root, two folders will be created also, unless they already exist:

 - ./playgrounds/
 - ./packages/

## playgrounds
All the framework playgrounds that manuscript creates for you will be placed into this folder.

These playgrounds are disposable.

When you run `manuscript play` from inside one of your packages, you will be able to create a new one, as well as 
choose from any existing ones.

You can clear out this folder at any time by using the `manuscript clear-playgrounds` command. This will have no 
effect on your packages.

## packages
All of your own packages you are working on will be added to this folder when they are created using the `manuscript 
create` command.

Note: I might be adding a command to help clone an existing repository from github into your manuscript packages 
folder. But you can just `cd ./packages && git clone ***etc***`.
