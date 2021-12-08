# README -- Code The Dream Backend Community Application

This repository contains the framework for the application called "community" in the following Treehouse
video for Active Record Associations in Rails:
https://teamtreehouse.com/library/has-and-belongs-to-many-associations .
You should create a git branch called community and make your changes there.
When you are done with the application, because you have completed all the changes from the Treehouse
videos, you can git add, commit, and push your changes and
make a pull request.

The first thing you will have to do is to complete the setup.  This is described in the Teacher's Notes
at the link above.  You do not do the rails new command,
as that has been done for you.  You start with the rails g model User command as described in the notes
and complete the directions in those notes and in the
video.  This application is also used and modified in the following video:
https://teamtreehouse.com/library/has-one-associations .

____________________________________________________________________________________
## Assignment notes

`rails g model User name:string nickname:string`
`rails g model Forum name:string public:boolean`
`bin/rails db:migrate`
`bin/rake db:seed`

seed data for the users and forums models

create join table
`bin/rails g migration CreateJoinTableUsersForums users forums`

use the has_and_belongs_to_many method on the models

add forums to a user - but in the console
`user = User.find_by(name: "Jay")`
`user.forums = << Forum.find_by(name: "Ruby")`