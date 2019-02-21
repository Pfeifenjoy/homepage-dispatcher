[![Build Status](https://travis-ci.org/Pfeifenjoy/homepage-dispatcher.svg?branch=master)](https://travis-ci.org/Pfeifenjoy/homepage-dispatcher)

# Homepage Dispatcher

This module detects if a request is made by a client application
or if a initial rendering is requested.
It solves the problem which arises when programming a isomorphic application.
If the application is running on the client it wants to use the Restful API
of the application. However if the initial request is made by the browser
or if the browser has deactivated JavaScript the application should be
rendered on the server for faster load times and better searchability.
This module will detect which request is made, create a "state action",
which it hands over to either the Restful API or the Renderer.
They will then respond to the request.
