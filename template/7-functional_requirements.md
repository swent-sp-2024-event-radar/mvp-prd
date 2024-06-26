# Functional Requirements


### Browse, Register for, Create, and Edit Events

**Motivation:**

Users need an intuitive way to discover events based on their location and preferences and register for events seamlessly. Users should also be able to create and edit events based on their preferences. Users expect real-time updates, meaning any event changes should be automatically updated. Real-time updates enhance the user experience by ensuring users always have the most current information.

**Proposed Solution:**

__Browse Events and Upcoming Events (Registered for):__

- Implement a filter button that allows users to add a radius field to see only events within that radius. The radius is set around the user's current location, which they gave permission for when first signing into the app. Additionally, the filter allows users to see events based on their preferences, such as event categories.
- Implement a Map view initialized on the current user’s location, allowing them to see markers representing events in their vicinity. Users can also filter in the map view.
- Allow users to search for events by typing the event name.
- Allow users to see event details when clicking on a displayed event or a Map marker.
- Ensure that any changes made by a host in an event, such as edition, creation, or deletion, are immediately reflected in Browse and Upcoming Events.
 
__Registering for Events:__

- Allow users to view event details including the remaining number of tickets, and confirm their attendance.
- To register for an event, users only need to select their ticket and pay if it's not free.
- Implement a seamless payment interface.
- Any event registered a user has purchased a ticket to will show in the Upcoming tab automatically.

__Create Events:__

- Provide a user-friendly interface for creating events.
- Enable organizers to add a detailed description, image, location, date, multiple ticket categories, and other relevant information.
- Any new event created will be automatically added to Browse Events for other users.

__Edit Events:__

- Allow event organizers to easily change event details, provided it's not too close to the event date.
- Any change in event details should be automatically shown on other users' apps without needing a manual refresh.

__Manage Event:__

- allow organisers to scan tickets to verify that users are on the attendee list
- allow organisers to view the list of attendees and send broadcast messages to them.
- allow organisers to view the event details and edit them if necessary.
- allow organisers to delete an event if they wish to cancel it.
- allow organisers to assign other co-hosts to an event so that they can gain certain privileges such as the 4 aforementioned points.



### QR Code Scanning and Secure Messaging System

**Motivation:**

We want to allow users to add other users they meet by scanning their QR code. Users should be able to see their friends list and privately message them. Private chats should automatically update whenever a new message is sent or seen. Upon registering for an event, all attendees should be added to a group chat for that event. This will facilitate organization and meeting new people. Hosts should also be able to scan other users' QR codes to verify that they registered for their event.

**Proposed Solution:**

__QR Code Generation and Scanning:__

- Upon sign-up, every user is assigned a unique QR code.
- Scanning a QR code allows you to add someone to your friends list.
- As a host, you can also scan QR codes upon clicking on your event to verify that users are on the attendee list.

__Private Chats:__

- Implement a private message system that allows users to chat with their friends and see their profile information.
- Ensure that whenever a new message is sent or seen, private chats are immediately updated.
 
__Group Chat(Not in POC):__

- Upon an event creation, a group chat is created with all the hosts.
- Upon purchasing a ticket, the user is automatically added to the group chat.
- Users can decide to leave the group chat.
- Users must be able to choose which information can be visible to other group members (differentiate between randoms & friends).
- Polls, pictures, and text messages should be the main three group chat features.
- Users can choose to mute notifications (for periods of time or forever).
- Group chat should not be deleted after the event.
- Users should be able to access previous messages in the group after joining.

*Figure: Architecture Diagram*

![architecture diagram](images/architecture-diagram.png)
