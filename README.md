# branch_db
Uses git post-checkout hook to create new branch specific database 

## Use case
I use this on Drupal projects where I want to test some changes, such as applying a patch to a module, but I don't want those changes to touch the database of my site until I know they are stable. Using this script, when I create a new git branch, a new database is also created and settings.php is updated so Drupal is connected to the new database. After making whatever changes I want, I can switch back to the original branch and the original database. It's handy if you want to test a bunch of patches on a clean Drupal installation.

## Setup
1.) Download the "post-checkout" file from this repository<br />
2.) Put file in the hooks directory of your git enabled project so it appears like so: .git/hooks/post-checkout<br />
3.) Edit file so the environment specific variables correspond to the correct values for your Drupal application<br />
