[![Coverage](https://codeclimate.com/github/jjeremydiaz/OpenHouse/badges/coverage.svg)](https://codeclimate.com/github/jjeremydiaz/OpenHouse/coverage)

[![Maintainability](https://api.codeclimate.com/v1/badges/3bccb3728ff552747b0c/maintainability)](https://codeclimate.com/github/jjeremydiaz/OpenHouse/maintainability)

[![Build Status](https://travis-ci.org/jjeremydiaz/OpenHouse.svg?branch=master)](https://travis-ci.org/jjeremydiaz/OpenHouse)

# OpenHouse
OpenHouse is a platform for freelancers to connect and share workspaces. Users of the app can rent out their houses by the hour or per day to other users who want places to work, and they can connect with others in the OpenHouse community.

Some of the features the app supports include:
* Users can create and delete accounts and use them to log in and out.
* Users can search for nearby available rentals by typing in an address.
* Users can customize their public-facing profile pages and post information about their rentals.
* Users can send messages to each other through the app.
* Users can reserve an open house for a specific day and time range.

## Screenshots

This is what a host's public-facing profile page looks like. They have a name and picture for their house, a name and picture for themselves, and some information about their house. They also have a list of amenities that their house has to offer.

![Profile Page Image](app/assets/images/screenshot_for_readme_user_profile.png?raw=true "Profile Page")

This is what the app looks like when you press "Search." The results are shown on the left and their corresponding price tags are displayed on the right-side map.

![Search Page Image](app/assets/images/screenshot_for_readme_search.png?raw=true "Search Page")

The bar at the top of the page also has some useful buttons that can be used to navigate the site.

## Screencast

Here is a link to a [video][3] of the app being used.

## Instructions

### Setup

1. Clone the repo.

    `git clone https://github.com/jjeremydiaz/OpenHouse.git`

2. Run Bundler

    `bundle install`

3. Start the Postgres SQL server

    `sudo service postgresql restart`

4. Set up the database

    `rake db:reset`

5. Run the app

    `sudo screen -d -m rails s`

6. Access the app via your web browser (localhost:3000 or whatever your Cloud9 port and ip are).

### Testing

To run cucumber tests, just use `cucumber`

To run rspec tests, just use `rspec`

### Shutdown

To stop the server, go into the screen and kill it

`screen -r`

`<Ctrl-c>`

`exit`

## Helpful Links
[Pivotal Tracker][1]

[Heroku App][2]

## Future Tasks

The app is far from complete. There are a lot of things that could be added that would make it much more useable and finished. Here are our ideas:

* Make available times show up properly
    * There ought to be a Gantt chart showing the times that are already rented
    * It may be useful to show information about who else is renting at those times
* Integration with a 3rd party application for charging or paying a user for a reservation, as well as creating a method within the app to officially confirm the reservation upon billing authentication
* Dynamic calendar selection
    * Instead of selecting starting and ending times for reservation, users should be able to use a more visual interface to select the time they want
* Users should be able to post more than one house for rent
* User profile page customization
    * Users should be able to add more photos of their homes and/or themselves
    * Users should be able to change the order/layout of their photos
    * Users should be able to use old photos instead of uploading new ones each time they want to make a change
* There could be a "friends" feature
    * It would be good if users could connect a little more than just reserving places and going to them
* Add more animation to the site overall
* Tutorial
    * There really ought to be a tutorial or some instructions somewhere that tell people how to use the site
    * There could just be little (i) symbols next to things that tell you little blurbs about things
* Make the app more mobile-friendly
* Rating system
    * People might want to leave public feedback about other people's houses

[3]: https://www.google.com/
[2]: http://openhouse-1.herokuapp.com/
[1]: https://www.pivotaltracker.com/n/projects/2117895
