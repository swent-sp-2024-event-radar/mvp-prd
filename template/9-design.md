# Design and Implementation

## Frontend
### Implementation Framework
The app will be developed in Kotlin, optimized for Android, utilizing the Model-View-ViewModel (MVVM) architecture. This approach ensures a clear separation of concerns, making the management of the app’s UI and business logic more efficient and maintainable.
### Key Libraries and Languages
- **Kotlin**: Primary language for our Android development
- **Hilt**: Dependency injection library for managing dependencies and improving code modularity.
- **Material3**: Used for all graphic components
- **Jetpack Compose**: Used for dynamic UI rendering.
- **Firebase**: Backend-as-a-Service platform providing authentication, database, and cloud storage.
- **Android Camera Image Analysis**: Utilized for integrating camera functionalities required for photo capture during friend requests.
- **Dagger Assisted Factory**: Design pattern to create objects, particularly useful in the ViewModel creation process, ensuring that instances are correctly initialized with necessary dependencies.
- **ZXing**: Library to encode information to QR codes and decode QR codes to information
- **Nominatim API**: Used for geocoding and reverse geocoding to convert location names to coordinates and vice versa.
- **Third-Party Payment SDK** (e.g., Stripe or PayPal): Integrate payment services for ticket purchasing.
### Dynamic UI Rendering Strategy
The app will leverage Jetpack Compose for dynamic UI rendering. Compose enables the creation of UI components declaratively, allowing for real-time updates and modifications based on data changes.
- **Composable Functions**: These will be used to define each screen and UI component, enabling reusable and modular UI elements.
- **State Management**: ViewModels will manage the state, ensuring the UI is always in sync with the underlying data model.
### Essential Screens
#### i Navigation Bar (is not a screen per se but is at the bottom of all Main Screens (1, 2, 3, 4, and 5)
- **Features**: Icons for the five Main Screens: Home, Messages, QR Code, Hosted Events, and Profile
- **Compenents**: Navigation Menu with the icons of the main screens and an Active State Indicator
- **Description**: The Bottom Navigation Bar enhances user experience by providing a consistent and accessible means of navigating the app. Located at the bottom of the screen, it ensures that the primary functions of the app are always within easy reach, improving the overall usability and efficiency of the app.
#### 1 Home Screen
- **Features**: Displays all events as well as events the user has registered to in either list or map view
- **Components**: Event list, Upcoming events, search-filter, list/map view button
- **Description**: The Home Screen provides users with a comprehensive view of all events available on the platform, as well as events they have registered for, with both list and map views. The search-filter allows users to refine their event search based on categories and location radius.
#### 2 Event Hosting Screen
- **Features**: Enables users to manage hosted events and create new ones.
- **Components**: List/map view of hosted events and button to create an event.
- **Description**: The Event Hosting Screen offers both a list and map view of hosted events, allowing users to visualize and organize their events effectively. Additionally, users can easily create a new event directly from this screen, streamlining the event management process.
##### 2.1 Event Creation Screen
- **Features**: Enables users to create new events with detailed specifications
- **Components**: Input Fields for Event Details (Name, Photo, Description, Category, Start/End Date & Time, Location, Ticket Info), and a create event button
- **Description**: The Event Creation Screen simplifies the event creation process, providing users with input fields for all necessary event details. The interface encourages users to organize and host events.
#### 3 User Profile Screen
- **Features**: Displays the user's personal information for viewing and editing.
- **Components**: User's Personal Information Input Fields (Text fields or input fields, depending on edit mode) and edit button
- **Description**: The User Profile Screen offers a view of the user's information, allowing easy access for review and modification. 
#### 4 Messages Screen
- **Features**: Facilitates real-time messaging between users.
- **Components**: Chat list and My Friends list
- **Description**: The Messaging Screen serves as a central hub for users to engage in real-time conversations. It provides a comprehensive view of all conversations, allowing users to seamlessly switch between chats. Additionally, a tab allows users to specifically view their friends list, streamlining the ability to review the connections made and communications with close contacts.
##### 4.1 Single Message Conversation Screen
- **Features**: Enables real-time messaging between users within a single conversation.
- **Components**: Message List, Message Input Field, Send Button, other user’s profile picture and name
- **Description**: The Single Message Conversation Screen facilitates one-on-one real-time messaging between users. Users can view the conversation history in the message list, compose new messages using the message input field, and send messages with the send button. 
#### 5 QR Code Screen
- **Features**: Allows users to display their QR code for others to scan and scan other users' QR codes to add them as friends.
- **Components**: My QR Code Display, Camera View for QR Code Scanning
- **Description**: The QR Code screen facilitates quick and easy friend additions. The screen displays the user's unique QR code, which can be scanned by others to add them as a friend and activates the camera to scan other users' QR codes. This screen ensures that users can effortlessly expand their network by leveraging QR code technology.
#### 6 Event Details Screen
- **Features**: Displays detailed information about a selected event, including date, time, location, and group chat (not in POC)
- **Components**: Event description, group chat redirection button
- **Description**: The Event Details Screen offers comprehensive details about the selected event, enhancing the user's understanding of the event's key aspects. Additionally, registered users can access the event's group chat (not available in POC), facilitating communication and engagement among attendees.
##### 6.1 Ticket Purchase Screen
- **Features**: Enables users to purchase tickets for events through a third-party payment service.
- **Components**: Ticket options, Payment gateway integration (e.g., Stripe or PayPal), Purchase button.
- **Description**: The Ticket Purchase Screen allows users to select and purchase tickets for events securely. It integrates with third-party payment services, ensuring a smooth and safe transaction process.
### Backend Communication
The app will utilize Firebase for backend communication, leveraging its robust set of tools and services:
- **Authentication**: Firebase Authentication for secure login and user management.
- **Database**: Firebase Firestore for real-time data synchronization and storage.
- **Cloud Storage**: Firebase Storage for securely storing user-uploaded photos and other media.
- **Payment Processing**: Integration with third-party payment services (e.g., Stripe or PayPal) for handling ticket purchases.

## Backend
### User Management
- **Description**: This functional block handles user-related operations such as registrations, profiles, and interactions between users (e.g., becoming friends).
- **Application Logic**: Manages user authentication, registration, profile updates, and adding friends via QR scan.
- **Framework**: Developed using Firebase Authentication and Firestore for data storage.
- **Dynamic View Rendering**: Integrates with the frontend to render user profiles and friend lists dynamically based on data from Firestore.
- **Responsive Backend-Frontend Interaction**: Ensures responsive interaction with the frontend, updating user profiles and friend lists based on user interactions.
### Event Management
- **Description**: This block handles operations related to creating, updating, and managing events, including ticket management and payment processing.
- **Application Logic**: Manages event creation, updates, and ticket sales, and payment processing.
- **Framework**: Utilizes Firebase Firestore for event data storage and third-party payment services for handling transactions.
- **Dynamic View Rendering**: Provides APIs to fetch event details dynamically, ensuring frontend displays reflect the latest event information.
- **Responsive Backend-Frontend Interaction**: Updates event details on the frontend based on user actions such as event creation or ticket purchases.
### Messaging System
- **Description**: This block manages communication between users through real-time messaging.
- **Application Logic**: Handles message sending and retrieval between users.
- **Framework**: Utilizes Firebase Firestore for real-time messaging.
- **Dynamic View Rendering**: Updates message threads dynamically based on new messages received.
- **Responsive Backend-Frontend Interaction**: Ensures real-time updates of message threads on the frontend as new messages are sent or received.
### Additional Considerations
- **Monitoring and Logging**: Utilize Firebase Analytics and Firebase Crashlytics to track backend performance and identify issues promptly.
- **Scalability**: Design the backend to scale horizontally to handle increasing user loads effectively using Firebase's scalability features.

## Data Model
### Data Collection and Management
#### User Data
- **Name:** User's first and last names. (String)
- **Email Addresse:** User's email for authentication and communication. (String)
- **Friend:** List of friends connected within the app. (Array of userIds)
- **Bio:** Short description of a user. (String)
- **Profile Picture:** Images uploaded by users as their profile pictures. (String - URL)
- **Phone Number:** User’s phone number. (String)
- **Birthdate:** User’s birth date. (String - Date)
- **Account Status:** Status of the user's account. (String)
- **Events Attendee List:** List of events the user is attending. (Array of eventIds)
- **Events Host List:** List of events hosted by the user. (Array of eventIds)
- **QR Code URL:** URL of the user's QR code image. (String - URL)
#### Event Data
- **Name**: Name of the event (String)
- **Photo**: Link to the photo stored of the event (String - URL)
- **Description**: Short text presenting the event (String)
- **Categories**: Categories or tags describing the type of event. (Array of Strings)
- **Start and End Date**: Date and time when events begin and end. (String - Date)
- **Location**: Details of the location
- **Location name**: Name of the location (String)
  - **Location lat**: Latitude of the location (Number)
  - **Location lng**: Longitude of the location (Number)
- **Ticket Information**: Details of the ticket
  - **Ticket name**: Name of the type of the ticket (String)
  - **Ticket price**: Price of the type of the ticket (Number)
  - **Ticket capacity**: Number of available tickets of the type of the ticket (Number)
  - **Ticket purchases**: Number of reserved tickets of the type of the ticket (Number)
- **Attendee List**: List of users participating in events. (Array of userIds)
- **Main Organizer**: Id of the user organizing the event. (String)
- **Organizer List**: List of user ids of users organizing events. (Array of userIds)
#### Messages Data
- **From User**: User sending the message (String)
- **To User**: User receiving the message (String)
- **From User Read**: Was the message read by the sending user (Boolean)
- **To User Read**: Was the message read by the receiving user (Boolean)
- **Latest Message Id**: Id of the last message sent (String)
- **Messages sent**: List of messages sent in this conversation
- **Sender**: User sending the message (String)
- **Content**: Content of the message (String)
- **Date Time Sent**: Date and Time of the message (String - Date)
#### Firebase Storage
- **QR Code Images**: Stored with paths like QR_Codes/{userId}.png
- **Profile Photos**: Stored with paths like Profile_Pictures/{userId}.png
- **Event Photos**: Stored with paths like Event_Photos/{eventId}.png
### Data Storage
#### Firebase Database
- **Firestore**: Used for structured data such as user profiles and event details. Provides real-time updates and scalable data storage.
#### Firebase Storage
- **Cloud Storage**: Used for media files such as QR codes, profile photos, and event photos. Ensures scalable and secure storage for large files.
### Data Sharing, Copying, and Caching
#### Data Caching
- **Firestore’s Built-in Caching**: Utilize Firestore’s client-side caching to reduce latency and enhance user experience by serving data from cache when possible. This feature ensures that users have quick access to their data even with intermittent network connectivity.
#### Data Sharing
- **Firestore Security Rules**: Implement robust security rules to control access to user and event data. Ensure that users can only access their own data and data they are authorized to view (e.g., events they are attending).
#### Data Integrity and Privacy
- **Data Anonymization**: Ensure that all collected data is anonymized and adheres to privacy standards. Store only non-identifiable information when possible, and encrypt sensitive data both at rest and in transit.

## Security Considerations
### Data Privacy and Protection
- Compliance with relevant data protection regulations such as GDPR to safeguard user data privacy.
- Secure authentication mechanisms, such as Firebase Authentication, to protect user accounts and prevent unauthorized access.
- Encryption techniques, such as HTTPS, to secure data transmission between the app and servers, protecting against eavesdropping and data tampering.
### Secure Backend Services
- Robust security measures for backend services, such as Firebase, to prevent unauthorized access and data breaches.
### Secure User Interactions
- Secure coding practices to prevent common security vulnerabilities such as injection attacks.
- Validate user input and sanitize data to prevent malicious input from compromising the integrity of the application.
### Secure Deployment
- Securely configure cloud infrastructure and services, such as AWS or Azure, to prevent unauthorized access and ensure the confidentiality and integrity of data stored in the cloud.
- Implement secure deployment practices, such as using encrypted secrets and keys, to protect sensitive information during deployment processes.

## Infrastructure and Deployment
### Development and Testing
- The application is developed using modern development practices and frameworks such as Kotlin for Android development.
- Comprehensive testing methodologies, including unit testing, integration testing, and end-to-end testing, are employed to ensure the reliability and functionality of the application.
- Continuous Integration/Continuous Deployment (CI/CD) pipelines are set up to automate the testing and deployment processes, allowing for rapid iterations and updates.
### Deployment
- The application is deployed on cloud platforms like AWS or Azure to ensure high availability and scalability.
- Special attention is paid to infrastructure requirements to support the expected load and user base of the application.
- Firebase Authentication is utilized to secure APIs, ensuring that data requests are authenticated and users can only access data relevant to them.
- HTTPS is enforced for all communications between the app and servers to guarantee the confidentiality and integrity of data transmission.
### Special Infrastructure Requirements
- Scalable backend infrastructure is provisioned to handle potential spikes in traffic, especially during peak usage periods or major events.
- Databases are configured for high availability and durability, with appropriate backup and recovery mechanisms in place to safeguard against data loss.
- Monitoring and logging systems are set up to track system performance, detect anomalies, and troubleshoot issues in real-time, ensuring the smooth operation of the application.


## Test Plan
### Testing Strategies
#### UI Tests
- UI tests are conducted to verify that UI components, including those instantiated by factories, run smoothly and interact correctly.
- Tests cover UI elements such as buttons, input fields, dialogs, etc., instantiated by factories.
#### ViewModel Tests
- ViewModel tests ensure that appropriate states are prepared for UI components instantiated by factories.
- Tests verify the logic and behavior of ViewModel classes, including interactions with factory-created UI components.
- Tests utilize Mock Repositories for the databases to isolate testing specifically on the ViewModel.
#### Factory Tests
- Tests are specifically designed to validate the behavior of factories in instantiating UI components.
- Ensure that factories correctly instantiate objects with the expected configurations and dependencies.
- Verify that factories handle edge cases and exceptions gracefully.
#### Backend Testing
- Backend services, such as Firebase, are tested using mocks to ensure they function correctly in conjunction with factory-created UI components.
- Tests verify that factory-created UI components interact seamlessly with backend services.
#### Integration Testing
- Integration tests encompass end-to-end scenarios involving factory-created UI components, backend services, and other application modules.
- Ensure that factory instantiation integrates smoothly with the overall application flow.
- Cover interactions between factory-created UI components and other parts of the application, including data flow and event handling.
### Special Infrastructure Requirements
- Utilization of Hilt for Dependency Injection in Testing:
   - Hilt is utilized for dependency injection in testing environments, ensuring that test components, including factories, are properly initialized and injected with dependencies.
   - This ensures that factory tests are executed in a controlled and predictable environment, facilitating accurate validation of factory behavior.
