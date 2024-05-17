# History

*Maximum 1 page*

*Describe the V1 POC as planned by Sprint10.*
- 4 epics:
    - Epic 1: Allowing Users to Discover and Join Events
    - Epic 2: Allowing Users to Interact With Others
    - Epic 3: Allow Event Hosts to Easily Create Events
    - Epic 4: Allow Events Hosts to Communicate with Participants Easily

- we were able to achieve most of the user flows in epics 1-3

*Epic 1*
- home screen that shows nearby events on the platform, with search bars and filter buttons to filter the events to the user's liking
- home screen also features all the upcoming events that a user has registered for
- when clicked, each event goes to full screen event details page (where a user can register for the event if not already registered)
- both tabs lead to a map view that allows users to see where events are relevant to their location

*Epic 2*
- messages screen shows all chat histories that a user has with friends, and the friends screen shows a list of all the friends a user has connected with
- once a user clicks on a message item in the messages list, they will see the full private chat history they have with a friend
- once a user clicks on a friend list item, they will see the friend's profile
- every user has a profile that they can edit in the profile screen
- on signup, every user is given a unique QR code that they can use to access events and connect with friends

*Epic 3*
- the hosting screen is the dashboard for all event hosts
- it features a list of all their active events which, when clicked, leads to a screen to edit those details
- it allows hosts to add events easily
- it also includes a map view allowing hosts to visualize the locations of their events
- hosts get access to a tool that allows them to easily scan the QR codes of event goers and see if the event goers have signed up or not

*What did you learn?*
- many members of our team were new to the scrum process, so it was an adjustment period, especially at the beginning, to get used to agile development
- often at the beginning we were so eager to correct issues with the code that we took on gigantic PRs that touched too many files, we learned from this mistake by 1) limiting the scope of PRs or splitting PRs if needed, and 2) writing better tasks in the SCRUM board that made the scope of the task clear to the developer
- with an idea as ambitious as ours and a limited time to complete everything, we knew we would not be able to finish everything in time, so we had to make a lot of hard decisions regarding prioritization of tasks
- we learned to break down tasks in a way that reduces dependencies between them

*What is missing to bridge from PoC to MVP?*
- there are still some user flows that we designed that are missing from the PoC
- some important defining features regarding connecting with others still need to be implemented
- some more user flows have to be thought through and designed to make sure they are the best for the user, such as group chats, in event geo-location, and history of attended events
