# Nimble House: hack-the-6ix-2018
A navigation & location-tracking app for seniors and a web-platform for caretakers to monitor and assist them.

# Inspiration
We wanted to build a system that mitigates some of the issues faced by seniors suffering from dementia. By using a user-friendly app to track them, and a website that allows caretakers and family members to monitor them, our system provides peace of mind to family members and safety for the users.

# What it does
The system is comprised of two major platforms: a mobile application (app) for tracking and a website (site) for monitoring.
There are 5 major steps involved in using this system:
1. Patient Log-In: The user opens the app and enters their username and password. This is a one-time process that can be completed by a caretaker during a setup procedure.
2. Patient-Caretaker Pairing: In order to ensure user privacy, verified caretakers can access a specific patient's location only after going through a subscription process between that patient and the caretaker. This process starts by the caretaker searching for the registered patient on the site, and simply pressing 'Send Request'. This sends a text message request to the patient's phone - prompting them to allow or block the caretaker's subscription to them. The patient can simply tap a hyperlink in the text to confirm or reject the subscription request. This step is also a one-time process that can be completed by a caretaker during a setup procedure.
3. Location Monitoring: Upon logging in on the app, a patient's location is synced with the site in real time. This allows the subscribed caretaker(s) to monitor their patients' locations remotely from a single platform. A patient can have multiple caretakers / family members tracking them, and a single caretaker can monitor multiple patients (many-to-many relationship). If a caretaker wants to highlight a particular patient's location, they can simply type their name in the search bar above the live map to zoom into the patient's location.
4. Geofence Monitoring: Each patient has a home address stored withing the app during initial setup. If a patient wanders off too far (20m-100m, precision can be adjusted for each patient) from their home, the app will detect it. It will automatically highlight the patient's location on monitoring site's live map. In addition, the app will prompt the user to describe where they are going or if they are lost. Using Speech-to-Text, the app will record and send the patient's response to the subscribed caretakers via live notifications on the monitoring site. 
5. Home Routing: At any point, if the patient thinks they are lost, they can simply tap the 'Find Home' button to automatically launch Google Maps in walking mode with a safe path from their current location to their home address.

# How we built it
The app was developed using Java and XML on Android Studio. The app combines Android's built in Location Services, Geofence Functionality, and Google Maps app for Home Routing. The site was built using JavaScript, HTML, and CSS. The app and the site were interlinked using Standard Library (StdLib). MessageBird was used for the subscription process, with Google's Firebase for the backend.

# Challenges we ran into
As the system comprised of multiple parts, it was critical to test each part thoroughly before integration. Our biggest challenge was testing app for its location accuracy when using Location Tracking along with Geofence setup as the device needed to be physically moved a relatively large distance (20m-50m). Furthermore, to simulate actual usage, we wanted to mock a realistic walking pattern example of users which was achieved through third party apps to mock the device's location.

# Accomplishments that we're proud of
The successful integration of the individual parts allowed the overall system to be functional. Despite our challenges, we were able to thoroughly test and integrate the parts to make our vision come to life.

# What we learned
We learned a lot about using server-less APIs, as well as location services such as Geofence for Android.

# What's next for Nimble House
We want to make this more universal, and easier to use, allowing family members or caretakers to further customize their needs with the senior users.
* New User Registration
* Caretaker Registration and Verification
* Dynamic Home Address Updates
* iOS Support
