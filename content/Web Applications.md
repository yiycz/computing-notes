---
tags:
  - theory
  - practical
  - web
---
## Difference between native and web applications

### Short Summary

| Feature                        | Web Applications                                                                                                                     | Native Applications / Desktop Applications                                                                                                         |
| ------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------ | -------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Deployment and Maintenance** | Deployment and maintenance (updates) for a web-based application require deployment on a single set of server machines.              | Deployment and any maintenance/patch are done on individual client machines separately.                                                            |
| **Accessibility**              | Web applications can be accessed from anywhere (most locations), so there is no location constraint.                                 | As desktop are confined to a standalone machine, so they can be only accessed from the machines they are deployed in.                              |
| **Platform Compatibility**     | Web applications are platform-independent, they can work in different types of platforms with the only requirement of a web browser. | Desktop applications need to be developed separately for different platform machines. (Windows, Linux, Unix, Mac etc)                              |
| **Security**                   | Web applications are at higher security risks as they are inherently designed to increase accessibility.                             | Desktop applications, on the other hand, have better authorization and administrators have better control, hence more secure.                      |
| **Internet Connectivity**      | Web applications rely heavily on internet connectivity, for their operation.                                                         | Desktop applications don’t require the internet for their operations. Some applications just require internet connectivity for specific functions. |

### Native apps

#### Definition:

- An executable program coded in the machine language of the hardware platform it is running in.
    

#### Benefits:

##### Optimum access to device hardware and features.

- Can be designed to have settings that allow an optimal level of access to device hardware and features.
- Use full range of device capabilities such as GPS
- Highly specialised and feature-rich applications
    

##### Potential for high performance and high responsiveness.

- Optimised for specific platform
- Utilising low-level APIs and hardware acceleration.
- Can deliver smoother animations, faster load times, and a more fluid user experience.
    

##### Enhanced user experience.

- Can be designed to provide a rich and immersive user experience,
- By leveraging platform-specific UI components, design patterns, and navigation gestures.
- Resulting in a seamless and familiar interface for users.
- This level of customization increases user engagement and satisfaction.
    

##### Offline capabilities

- Can function offline,
- Allowing users to access certain features and content without an Internet connection.
- Store data locally, native apps can continue to operate and provide functionality in offline scenarios.
    

#### Shortcomings:

##### App store approval:

- Need to go through the app store approval process
- Adhering to guidelines and policies specific to each platform.
- Can introduce additional time and potential challenges


##### Longer development time and costs

###### Time:

- Require separate code for each platform.
- Platform-specific programming languages and development platforms must be used.
    

###### Costs:

- Maintenance efforts, updates and bug fixes must be performed separately for each platform.
    

##### Limited distribution and discoverability outside the app store.

- App store distribution may limit app discovery and require adherence to specific distribution rules.
- Challenging for users to find apps outside of the app store, limiting the visibility of the app.
    

##### Fragmentation and compatibility challengers.

- The mobile computing landscape is fragmented, with multiple OS versions, device models, and screen sizes.
- Native apps must be optimised and tested across a wide range of devices, OS versions, and resolutions, which can increase development and testing efforts.
    

### Web apps

#### Definition:

- An application in which all or some parts of the software are downloaded from the Web every time it runs.


#### Types:

##### Browser-Based:

- A browser-based web app is an application built with web technologies (typically HTML, CSS, and JavaScript) that users access through a web browser over the internet or a local network, without requiring installation from an app store.


##### Client-Based:

- A client-based application is software installed on a user's device that executes locally, without a browser, and may communicate with remote servers or services to access data, synchronize information, or perform network-based functions (similar to the “client / server” architecture
    

##### Native mobile apps

- ?
    

#### Benefits:

##### Cross-Platform Compatibility:

- Platform-agnostic, can be run on any devices like desktops, laptops, tablets, and smartphones.
- Users can access the same web app across different platforms, ensuring a consistent experience and broad reach.
    

##### No requirements for installation:

- Eliminate the need for installation or downloads.
- Access them directly by entering the app’s URL in a web browser.
- Reduce barriers and frictions, faster onboarding process.
    

##### Update and app maintenance.

- Allow for centralised updates and maintenance.
- Developers can deploy changes on the server, making them available to all uses.
- Client web software updates may happen each time the web page is visited.
- Updates can be applied seamlessly without requiring users to manually update the app, ensuring everyone has access to the latest version
    

##### Cost-effective development

- Cost-effective as web technologies are widely accessible,
- Developers can use a single codebase to target multiple platforms.
- Reduce development time and resources needed for platform-specific development.
    

##### Greater discoverability

- Discoverable via search engines.
- Optimising the app’s website and content for search engines, web apps can benefit from organic discoverability.
- Potentially attracting a broader user base.
    

#### Shortcomings:

##### Internet Connectivity Dependency

- Require an Internet connection to function.
- Limited or no connectivity can hinder the app’s usability.
- Progressive web apps aim to mitigate this limitation by enabling certain features and content for work offline.
    

##### Limited device feature access

- Web apps have limited access to device features.
- Although modern web APIs provide access to certain hardware capabilities,
- The range and depth of access may be limited.
- Impact certain user cases that rely greatly on specific device features.
    

##### Performance constraints.

- Rely on web browsers → variations in rendering speeds and performance optimisations.
- However, this limitation is mitigated by the improved JS engines.
    

##### Security considerations

- Web apps are susceptible to web-based vulnerabilities like XSS and CSRF.
- Proper security measures, such as input validation, output encoding must be implemented to protect against these threats.
    

### Difference between web and native applications

||||
|---|---|---|
||Web applications|Native applications|
|Performance|Rely on web browsers, which introduces additional layers performance constraints|direct access to device resources, hardware accelerations and platform optimisation → Superior performance   <br>  <br>  <br>  <br>Machine code → allow for a more efficient execution and utilisation of the devices’ capabilities|
|User experience|Achieve Responsiveness and adaptability  <br>  <br>  <br>  <br>Lack the consistency provided by native apps.|Tailored and consistent user experience, adhering to the design principles and guidelines of the platform.  <br>  <br>  <br>  <br>Leverage platform-specific UI components and navigation patterns → native and intuitive experience.|
|Development and maintenance|Using a single codebase to target multiple platforms (no need for platform-specific efforts) → shorter development timeliness and lower costs|Require platform specific experience → use multiple codebases  <br>  <br>  <br>  <br>Maintenance efforts, updates and bug fixes must be performed separately for each platform.|
|Accessibility|A single codebase facilitates accessibility from any device with a compatible web browser → eliminating the need to switch between platforms or download different versions of the app|Users have to switch between different platforms to gain access to the sample applications → fragmentation and potentially limited user base.|
|Offline Functionality|Require an active internet connection to function|Inherent offline capability → Allowing users to access certain features and content without an Internet connection.|

## State and apply usability principles in the design of web applications.

### Quality of a web application:

- Learnability: how easy is it for users to learn to navigate the system to perform basic tasks at the first encounter
- Efficiency: how fast can users perform tasks after knowing the system.
- Memorability: How easy is it for users to recall the functionality of the system without relearning after a long time
- Errors: How does the system recover its users from the errors they made
- Satisfaction: How easy it is for use.
    

### Nielsen’s 10 principles:

||||
|---|---|---|
|Principle|Meaning|Example|
|Visibility of system status:|Always keep users informed about what is going on, via appropriate feedback with reasonable time.|Upload a file into google drive, the color change shows that the progress and the message above shows time left to complete the task|
|Match between system and the real world.|The system should speak the users’ language, with words, phrases and concepts familiar to the user, rather than system-oriented terms|An online shopping app uses familiar terms such as "Add to Cart," "Checkout," and "Order History" instead of technical jargon. This matches the way people shop in the real world, making the app easier to understand and use.|
|User control and freedom|Leave unwanted state without having to go through a extend dialogue, support undo and redo, when users chooses system functions by mistakes|Attachments in Gmail can be easily removed.|
|Consistency and standards|Users should have to wonder whether different words, situations or actions mean the same thing.|An online shopping app uses the same shopping cart icon and checkout process on every page. This consistency helps users know what to expect and makes the app easier to use without having to relearn different layouts or actions.|
|Error prevention|A careful design which prevents a problem from occurring in the first place.|Auto-correction function in Google Docs|
|Recognition rather than recall|Minimize the user’s memory load by making objects, actions and options visible. The users should not have to remember information from one part of the dialogue to another.|Past search history for users to retrieve in browsers.|
|Flexibility and efficiency of use|The system should support both inexperienced and experienced users by providing multiple ways to accomplish tasks, allowing users to become more efficient as they gain experience.|Online shopping website:  <br>  <br>  <br>  <br>A first-time shopper can browse product categories and use filters to find an item. A returning shopper can reorder a previous purchase and use saved payment details to check out in just a few clicks.|
|Aesthetic and minimalist design|Dialogues should not contain information which is irrelevant or rarely needed.   <br>  <br>  <br>  <br>(Every extra unit of information in a dialogue competes with the relevant units of information and diminishes their relative visibility.)|University and government websites are quite minimalistic.|
|Help users recognise, diagnose and recover from errors|Error messages should be expressed in plain language, precisely indicate the problem and constructively suggest a solution|Google User login-in page:  <br>  <br>If entered wrongly, the system will prompt you to re-enter your credentials again.|
|Help and documentation|Provide help and documentation which lists concrete steps to be carried out.|An online shopping app provides a Help Center with FAQs and step-by-step guides on placing orders, tracking deliveries, and processing returns. If users encounter a problem, they can quickly find instructions or contact customer support for assistance.|

---




