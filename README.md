# Architectural-Decision-Record
this repository is for the Architectural Decision making Record for Mobile Application Phase 2

Architectural Decision Record 


Scenario 1: Retail Company Mobile App

Architectural Decisions:

Decision: native mobile app for both ios and android platform.

Rationale:
After a long and careful deliberation, our team has come to a conscious decision to pursue native applications for several compelling reasons. We firmly stand behind the belief that native apps provide unparalleled user experiences and performance excellence across all platforms. With the ability to leverage platform-specific features and optimizations, native apps offer a level of responsiveness and fluidity that is unmatched by other approaches [4]. Furthermore, considering the company's directive to ensure broad accessibility, native apps emerge as the optimal choice for efficiently reaching both iOS and Android users. By crafting native applications, we can seamlessly align our development efforts with the company's objectives, ensuring that our app delivers a consistent and high-quality experience to all users, regardless of their chosen platform.


UI Framework: 
We chose React Native as our UI framework because it seamlessly supports cross-platform development while providing a native-like experience. Our app's UI corresponds closely to both iOS and Android design principles thanks to the usage of React Native, improving usability and familiarity [4]. Furthermore, React Native provides a wide range of frameworks and components, reducing the development process and allowing for quick iteration. This wide ecosystem enables us to efficiently deploy complicated features while maintaining peak performance across all platforms. In summary, React Native's cross-platform features and complete toolset make it the best option for meeting our project's UI development needs.



Backend language: 
For the backend language, it would be preferable to use JavaScript as it integrates nicely with the existing frameworks of android. Additionally, JavaScript has been known for its fraud and risk protection and its use in personal banking making it the ideal option for an application that is handling payments. Examples have been implemented with the Stripe JavaScript library, which helps protect against fraud [1]. JavaScript also has the ability to work cross platform making the ability to implement the application on multiple devices easier then compared to C or C++, which IOS has their own version called “Objective C” [2] that doesn't have the full features of C [3] and would be harder to implement cross platform and are not as dynamic in their programming. 





Permissions: 
For the permissions of the application, it would need access into the devices storage and location. Location is needed as when the user goes to fill in their address, the device would access the user's location to make it more convenient to use. This is opposed to manually inputting the address into the device, which would still be implemented if the user wanted to ship their order elsewhere, but adding this functionality to take advantage of the pre existing hardware is convenient and ideal. Access into the users device storage is essential as to not only keep track of orders, but to ensure that offline features work properly. For instance, some of the users favorite products and most bought products would be stored within the device storage for when the user wants to buy them, and if the user does they can simply save them until connection to data is established and the products are ordered. 


Data storage:
To support syncing data with the server and an offline mode, a combination of local device storage and a syncing technology would be ideal. 

SQLite is a great DBMS option that requires no configuration, and is multi-platform to keep track of information like order history and user data. Syncing data with the server can be achieved using technologies like Firebase Realtime Database or Cloud Firestore, which have React Native SDKs for seamless integration.

React Native provides modules and libraries that can handle image storage and optimization. Developers can utilize libraries like React Native Image Picker for selecting and uploading product images and integrate with image optimization services like Cloudinary for efficient storage and delivery of images. React Native supports localization through libraries like react-native-localize or i18n-js. This would allow the app to support multiple languages.

Additional framework or technology stacks:
React Native
Javascript for backend language  
Tailwind CSS for styling
SQLite for DBMS
Firebase Realtime Database or Cloud Firestore
Google Analytics for Mobile Apps or Firebase Analytics for analytics










References:

[1] Stripe Editors. “Advanced Fraud Detection” Stripe.com. Accessed: Feb 7, 2024. [Online] Available:  https://stripe.com/docs/disputes/prevention/advanced-fraud-detection

[2] Apple Editors. “About Objective-C” Apple.com. Accessed: Feb 7, 2024. [Online] Available: https://developer.apple.com/library/archive/documentation/Cocoa/Conceptual/ProgrammingWithObjectiveC/Introduction/Introduction.html

[3] Apple Editors. “C++ Language Support” Apple.com. Accessed: Feb 7, 2024. [Online] Available: https://developer.apple.com/xcode/cpp/

[4] Maxtra Technologies Pvt Ltd. "Can React Native Be Used for both iOS and Android App Development?" Accessed: May 8, 2024. [Online] Available: https://www.linkedin.com/pulse/can-react-native-used-both-ios-android-app-development/

