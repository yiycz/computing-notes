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

**Better performance**: Native apps **run directly on** the device’s OS and can be optimised for that specific platform, resulting in faster and smoother user experience.

**Access to device features**: Native apps can **directly access** the device’s hardware features, such as GPS, biometric sensors, push notifications, camera, providing **enhanced functionality** for banking services.

**Enhanced user experience**: Native apps can leverage **platform-specific UI components, design patterns and navigation gestures** to provide a **seamless and familiar interface**, resulting in greater **user engagement and satisfaction**.

**Offline capabilities**: Native apps can store **data locally** on the device, allowing users to **access** certain features and content **without an Internet connection**.

    

#### Shortcomings:

- **Longer development time**: Native apps require **separate code for each platform**, using **platform-specific programming languages and development tools**.

- **Higher maintenance costs**: **Updates, bug fixes and maintenance** must be performed **separately for each platform**, increasing **costs**.

- **Limited discoverability**: Native apps are mainly **distributed through app stores**, which impose **distribution rules** and limit **visibility outside these stores**.

- **Compatibility challenges**: Native apps must be **optimised and tested** across different **OS versions, device models and screen sizes**, increasing **development and testing efforts**.

- **App store approval**: Native apps must undergo an **approval process** and adhere to **platform-specific guidelines and policies**, increasing **development time** and **potential challenges**.

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

- **Cross-platform compatibility**: Web apps can run on **different devices and operating systems** through web browsers, ensuring a **consistent user experience** and **broader reach**.

- **No installation required**: Web apps can be accessed directly through a **URL in a web browser**, eliminating **downloads and installation** and allowing **faster onboarding**.

- **Easier updates and maintenance**: Developers can **deploy updates centrally on the server**, making changes available to **all users automatically** without requiring **manual updates**.

- **Cost-effective development**: Web apps use a **single codebase across multiple platforms**, reducing **development time, costs and resources**.

- **Greater discoverability**: Web apps can be **found through search engines**, increasing **visibility** and potentially attracting a **broader user base**.

#### Shortcomings:

- **Internet connectivity dependency**: Web apps generally require an **Internet connection** to function, limiting **usability when offline**, although progressive web apps can support **certain offline features**.

- **Limited device feature access**: Web apps have **restricted access to device hardware and features**, potentially limiting **functionality** that relies on specific device capabilities.

- **Performance constraints**: Web apps rely on **web browsers**, resulting in **variations in rendering speeds and performance**, although improved **JavaScript engines** can mitigate these limitations.

- **Security considerations**: Web apps are vulnerable to **web-based attacks** such as **XSS and CSRF**, requiring security measures like **input validation and output encoding**.
    

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


# shorter version
# 1. Types of Applications

| Type | Description |
| ---- | ----------- |

\| Native Applications | • Installed directly on device, specific to OS\
• Can work without internet\
• Designed to take advantage of specific hardware |\
\| Web Applications | • Do not depend on OS\
• Require internet to work |\
\| Hybrid Applications | • Packaged in a native shell\
• Runs on web browser, uses API to talk to hardware\
• Elements of both native and web applications |\
\| Progressive Web Applications (PWA) | • Accessible through a web browser and offline as a standalone\
• Cannot use APIs\
• Elements of native and web applications |

# 2. Web vs Native Applications

| Native Applications                      | Web Applications                                 |
| ---------------------------------------- | ------------------------------------------------ |
| Runs on the OS                           | Runs on the web browser                          |
| Needs to be downloaded                   | Does not require downloads                       |
| Access to system resources (GPS, Camera) | No Access                                        |
| Can work offline                         | Needs Internet                                   |
| Faster                                   | Slower (can be further slowed by internet speed) |
| Store large amounts of data              | Less data                                        |
| May require maintenance and update costs | Automatically updated                            |


# 3. Usability Principles

| Principle                                              | Description                                                    |
| ------------------------------------------------------ | -------------------------------------------------------------- |
| Visibility of system status                            | Keep users informed of system status for clear guidance.       |
| Match between system and the real world                | Align interface with user expectations for intuitive use.      |
| User control and freedom                               | Allow easy undo and exit.                                      |
| Consistency and standards                              | Maintain uniformity for ease of learning.                      |
| Error prevention                                       | Prevent mistakes through clear design and confirmation.        |
| Recognition rather than recall                         | Display information visibly for efficient interaction.         |
| Flexibility and efficiency of use                      | Cater to both novice and expert users for seamless experience. |
| Aesthetic and minimalist design                        | Focus on essentials to avoid distractions.                     |
| Help users recognise, diagnose and recover from errors | Provide clear, actionable error messages.                      |
| Help and documentation                                 | Offer accessible, context-sensitive support.                   |










