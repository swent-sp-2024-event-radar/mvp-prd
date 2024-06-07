# Non-Functional Requirements

## Security, Privacy, and Data Retention Policies

Given the global reach of our app, we must adhere to local laws concerning data security and privacy. 

- Compliance with GDPR is essential for users in Europe. They must have access to and the ability to delete their data.
- We will explicitly request camera access (for QR code scanning, photo-taking) and user location (to suggest local events).
- Users will be asked to provide consent for their data to be shared with third parties we engage with.
- Users have personal profiles within the app to share information with their friends, allowing them to be identified within the community. 
- Users have full control over their privacy settings, determining which information is visible to other users. 
- The user needs also to be able to delete any sent message or event in the history of attended events.
- The backend for private information should be done in such a way that we cannot extract or infer any personally identifiable information.
- The app keeps personal data about users such as birth dates used to filter the events the user have accessed to, as well with phone numbers used for country and user verification. 
- Data about chats and attended events needs to be kept for as long as the user is using the app to provide the user an history of the user's activity.

## Adoptions, Scalability and Availability

- Users should be able to add their friends at any time they meet.
- The app must allow users to attend free events without requiring payment information.
- Clear and straightforward navigation is essential to ensure users can manage their privacy preferences effortlessly.
- The app should track metrics such as chat activity, event browsing, and event hosting to identify any weak points and areas for improvement.
- While the app can scale globally, its usefulness is primarily local. Users are unlikely to travel long distances for events.
- A dedicated backend infrastructure should be considered to optimize performance and responsiveness based on user location, ensuring relevant local event information.
- Higher usage is expect during summer and holiday periods (considering regional variations).
- Weekly usage peaks are anticipated on weekends, with significant app activity as users geo-locate to attend events.
- The system must be prepared to handle high traffic during major cultural and sporting events.
- The app must support concurrent interactions and multiple features without significant delays or errors.
- The system must be robust enough to handle unstable internet connections without data loss or corruption.