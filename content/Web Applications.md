---
tags:
  - theory
  - practical
  - web
---

## Difference between native and web applications

| Native Applications                      | Web Applications                                 |
| ---------------------------------------- | ------------------------------------------------ |
| Runs on the OS                           | Runs on the web browser                          |
| Needs to be downloaded                   | Does not require downloads                       |
| Access to system resources (GPS, Camera) | No Access                                        |
| Can work offline                         | Needs Internet                                   |
| Faster                                   | Slower (can be further slowed by internet speed) |
| Store large amounts of data              | Less data                                        |
| May require maintenance and update costs | Automatically updated                            |

### Native apps

- **An executable program** coded in the **machine language** of the hardware platform it is running in.
    

#### Benefits:
- **Better performance**: Native apps **run directly on** the device’s OS and can be optimised for that specific platform, resulting in faster and smoother user experience.
- **Access to device features**: Native apps can **directly access** the device’s hardware features, such as GPS, biometric sensors, push notifications, camera, providing **enhanced functionality** for banking services.
- **Enhanced user experience**: Native apps can leverage **platform-specific UI components, design patterns and navigation gestures** to provide a **seamless and familiar interface**, resulting in greater **user engagement and satisfaction**.
- **Offline capabilities**: Native apps can store **data locally** on the device, allowing users to **access** certain features and content **without an Internet connection**.

    

#### Shortcomings:

- **Longer development time**: Native apps require **separate code for each platform**, using **platform-specific programming languages and development tools**.
- **Higher maintenance costs**: **Updates, bug fixes and maintenance** must be performed **separately for each platform**, increasing **costs**.
- **Limited discoverability**: Native apps are mainly **distributed through app stores**, which impose **distribution rules** and limit **visibility outside these stores**
- **App store approval**: Native apps must undergo an **approval process** and adhere to **platform-specific guidelines and policies**, increasing **development time** and **potential challenges**.

### Web apps

- An **application** in which **all or some parts** of the software are **downloaded** from the Web every time it runs.


#### Types:

##### Browser-Based:

- A browser-based web app is an application built with web technologies (typically HTML, CSS, and JavaScript) that users access through a web browser over the internet or a local network, without requiring installation from an app store.


##### Client-Based:

- A client-based application is software installed on a user's device that executes locally, without a browser, and may communicate with remote servers or services to access data, synchronize information, or perform network-based functions (similar to the “client / server” architecture
    

##### Native mobile apps

- ?
    

#### Benefits:

- **No installation required**: Web apps can be accessed directly through a **URL in a web browser**, eliminating **downloads and installation** and allowing **faster onboarding**.
- **Easier updates and maintenance**: Developers can **deploy updates centrally on the server**, making changes available to **all users automatically** without requiring **manual updates**.
- **Cost-effective development**: Web apps use a **single codebase across multiple platforms**, reducing **development time, costs and resources**.
- **Greater discoverability**: Web apps can be **found through search engines**, increasing **visibility** and potentially attracting a **broader user base**.

#### Shortcomings:

- **Internet connectivity dependency**: Web apps generally require an **Internet connection** to function, limiting **usability when offline**, although progressive web apps can support **certain offline features**.
- **Limited device feature access**: Web apps have **restricted access to device hardware and features**, potentially limiting **functionality** that relies on specific device capabilities.
- **Performance constraints**: Web apps rely on **web browsers**, resulting in **variations in rendering speeds and performance**, although improved **JavaScript engines** can mitigate these limitations.
- **Security considerations**: Web apps are vulnerable to **web-based attacks** such as **XSS and CSRF**, requiring security measures like **input validation and output encoding**.
    



# Usability Principles

| Principle                                              | Description                                                    |
| ------------------------------------------------------ | -------------------------------------------------------------- |
| Visibility of system status                            | Keep users **informed of system status** for **clear guidance.**       |
| Match between system and the real world                | Align interface with user expectations for intuitive use.      |
| User control and freedom                               | Allow **easy undo** and **exit.**                                      |
| Consistency and standards                              | **Maintain uniformity** for ease of learning.                      |
| Error prevention                                       | Prevent **mistakes** through **clear design and confirmation.**        |
| Recognition rather than recall                         | Display information visibly for efficient interaction.         |
| Flexibility and efficiency of use                      | **Cater** to both **novice and expert users** for **seamless** experience. |
| Aesthetic and minimalist design                        | Focus on **essentials** to avoid **distractions.**                     |
| Help users recognise, diagnose and recover from errors | Provide **clear, actionable** error messages.                      |
| Help and documentation                                 | If user doesn't know what to do, **give context-sensitive support.**                   |










