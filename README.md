# TechTonic-Scenario1-ADR

Architechture Decision Assignment

--------------------------------------------

ADR-001: Native, Web, or Hybrid App

Context:
We will be responsible for building a mobile application for a retail company that will include features such as, offline support, push notifications, integration with payment gateways, user behavior tracking, image optimization, and localization. This tailors our application for more customer convenience.

Status:
Proposed

Decision:
We will develop a hybrid app using a framework like React Native.

Rationale:
The simultaneous construction of iOS and Android apps is made possible by cross-platform development, which drastically cuts down on expenses and development time. React Native and Flutter are two examples of hybrid frameworks that provide near-native performance and a seamless user experience. Large communities also help this framework by offering a wealth of libraries and plugins as well as strong support.

Consequences:
Pros: Cross-platform development saves money and effort. Simpler updates and maintenance.
Cons: Possibly less successful than entirely native apps.

--------------------------------------------

ADR-002: UI Framework

Context:
In order for us to construct the application’s interface while maintaining a consistent, effective, and user-friendly design, we will require a UI framework.

Status:
Proposed

Decision:
In this case, we will be utilizing the React Native UI framework.

Rationale:
React Native offers a consistent user interface for both iOS and Android, guaranteeing cross-platform compatibility. It produces near-native performance, making the user interface fast and responsive. The framework's vast plugin library and active user base encourage development, and the fact that both platforms share a single codebase makes ongoing maintenance easier.

Consequences:
Pros: Reusable components, short development cycles, and powerful community support.
Cons: Some complex functions will require native code.

--------------------------------------------

ADR-003: Backend Language

Context:
The backend language must incorporate API requests, data synchronization, payment processing, and analytics integration.

Status:
Proposed

Decision:
Node.js with Express.js is what we will be using  for the backend part of our application.

Rationale:
Node.js is very scalable, making it perfect for managing huge numbers of concurrent connections. Its non-blocking I/O operations enable efficient real-time data synchronization and changes. The platform has an extensive collection of libraries and tools, and the common availability of JavaScript/Node.js developers adds to its popularity.

Consequences:
Pros: Rapid development, a strong community, and extensive libraries.
Cons: The single-threaded nature could require additional solutions for CPU-intensive jobs.

--------------------------------------------

ADR-004: Permissions

Context:
To access device functions like storage, push notifications, and network status, we need to manage app permissions.

Status:
Proposed

Decision:
We will be utilizing React Native's built-in permissions management, enhancing it with appropriate native modules as needed.

Rationale:
React Native's straightforward built-in APIs make permission management easier. It makes sure that permissions are handled consistently on the iOS and Android platforms, which improves consistency for developers. React Native also provides strong security capabilities, giving developers a smooth control over permission requests to protect user privacy and app integrity.

Consequences:
Pros: Ensures uniformity and simplifies authorization management.
Cons: Native code may be required to handle advanced or specialized permissions.

--------------------------------------------

ADR-005: Data Storage

Context:
For offline support, the app must save data locally and synchronize with the server when connected to the internet.

Status:
Proposed

Decision:
For this part, we will be using SQLite for local storage and Firebase Firestore for cloud synchronization.

Rationale:
For offline data storage, React Native offers support for SQLite, a popular and dependable database solution. In addition, Firebase Firestore integrates smoothly with React Native to provide effective data management and cross-device synchronization. It also provides a real-time database with strong synchronization features.

Consequences:
Pros: Scalability, real-time synchronization, and dependable offline support.
Cons: Careful handling of synchronization issues and data consistency is necessary.

--------------------------------------------

ADR-006: Additional Frameworks or Technology Stacks

Context:
For push notifications, payment processing, analytics, image optimization, and localization, we must choose new frameworks and technologies.

Status:
Proposed

Decision:
Push Notifications: Firebase Cloud Messaging
Payment Processing: Stripe and PayPal SDKs
Analytics: Google Analytics for Firebase
Image Optimization: Cloudinary for image storage and optimization
Localization: i18next library

Rationale:
Firebase Cloud Messaging  is used for push alerts, guaranteeing dependable platform delivery. Secure transactions within the app are made possible by the integration of the Stripe and PayPal SDKs, which enables payment processing. Strong analytics tools are available with Google Analytics for Firebase to monitor user activity and app performance. With Cloudinary, picture optimization and storage are managed efficiently, improving image delivery speed and quality. The i18next library is used to create localization features, allowing the app's content to be seamlessly translated into several languages and regions.

Consequences:
Pros: Use reliable, well-supported technologies for essential functions.
Cons: Adding to the difficulty of integrating several services.
