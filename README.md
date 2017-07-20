# Scenario

Write a simulator UI that demonstrates its basics following the design and interactions outlined below.

### Design & Functionality

You can see a mockup the interface at this link: https://github.com/sigmacloud/frontend-developer-homework/blob/master/mockup.png. Your new interface should be a basic implementation that matches the attached design as closely as possible.

Each gray block under “Server Canvas” represents a server in the cluster. The cluster should start with 4 servers.
Prioritize functionality over design perfection. This is a demo of functionality, and without app basics it won’t matter how beautiful it looks.

### Interactions

If interaction details are missing, use your best judgement and make a note to explain it during the follow up.

- Clicking “Add Server” should create a new server and a new gray block in the Server Canvas.
- Clicking “Destroy” should remove the last server and its gray block from the Server Canvas.
- Clicking “+” for one of the Available Apps should start an instance of that app in the cluster.
- Clicking “-” for one of the Available Apps should kill the newest instance of that app in the cluster.

##### What happens when you click “+” on an app?:

Each server can run a maximum of two apps at once.
When a new app is launched, it should be started following this algorithm:
- Run on the first server running 0 apps.
- If all servers are running at least 1 app, the new app should be started on the first server running only 1 app.
- If all servers are running two apps, the app should not be started.
- When a server is destroyed, each app running on it should be restarted elsewhere in the cluster following the algorithm above.
- If there is no capacity for the apps, they should be killed.


### Extra Credit

If you get the demo in good shape and have extra time, add your own flair and features. These are some ideas:

- Delay the start of apps via animation to simulate allocation and start up time.
- When a second app is started on a server, animate the partitioning of the server into two parts.
- Implement an overlay on the servers that displays on hover and has a “Destroy” button to destroy the given server.

### Deliverables

Provide the source code and a README explaining how to view the UI for your simulator in a tar-ball over email.

You may use any 3rd party libraries you know well that seem like a fit for the scenario. List the libraries in the README and a blurb about why you chose each one.

Develop for modern browsers and test in them. Your loved ones might be Firefox users even if you’re a diehard Safari or Chrome user.
Good luck!

 