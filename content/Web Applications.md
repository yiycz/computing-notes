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

# CSS

### CSS Selectors

##### Class:

```css
.intro{
	...
}
```

##### Element:

```css
p, div{
	...
}
```

##### Id:

```css
#id {
	...
}
```

### CSS Comments

```css
/* This is a comment */
```

### Colours

```css
p {
    color: blue;
    background-color: red;
}
```

You can also use rgb or hex code to represent colour:

```css
color: rgb(12, 34, 255);
```

```css
color: [#ee82ee](#ee82ee); /* *[*#RRGGBB*](#RRGGBB)* */
```

### Backgrounds

```css
div {
    background-color: red;
    opacity: 0.3;
    background-image: url("");
}
```

### Margin v.s. Border v.s. Padding

#### Borders

```css
div {
    border-style: solid;
    border-width: 5px;
    border-color: red;
}
```

##### Border Sides:

```css
div {
    border-top-style: dotted;
    border-right-style: dashed;
    border-bottom-style: dotted;
    border-left-style: dashed;

    border-top-width: 5px;
    border-right-width: 2px;
    border-bottom-width: 5px;
    border-left-width: 2px;

    border-top-color: red;
    border-right-color: blue;
    border-bottom-color: red;
    border-left-color: blue;
}
```

##### Border Shorthand:

```css
div {
    border: 5px solid red;
}
```

```css
div {
    border-top: 5px dotted red;
    border-right: 2px dashed blue;
    border-bottom: 5px dotted red;
    border-left: 2px dashed blue;
}
```

#### Margin

```css
div {
    /*        Top Margin: 25px*
*        Right Margin: 50px*
*        Bottom Margin: 75px*
*        Left Margin: 100px*
*    */
    margin: 25px 50px 75px 100px;
}
```

```css
div {
    /*        Top and Bottom Margins: 25px*
*        Left and Right Margin: 50px*
*    */
    margin: 25px 50px;
}
```

```css
div {
    /*        All four margins are 25px*
*    */
    margin: 25px;
}
```

```css
div {
    margin-top: 25px;
    margin-right: 50px;
    margin-bottom: 75px;
    margin-left: 100px;
}
```

##### Margin ‘auto’ keyword

You can set the margin property to auto to horizontally center the element within its container.

```css
div {
    margin: auto;
}
```

#### Padding

```css
div {
    /* Same syntax as margin */
    padding: 25px 50px 75px 100px;
    padding: 25px 50px;
    padding: 25px;

    padding-top: 25px;
    padding-right: 50px;
    padding-bottom: 75px;
    padding-left: 100px;
}
```

#### Height and Width

```css
div {
    height: 250px;
    width: 500px;
}
```

You can also represent height and width with percentages (relative to its containing block):

```css
div {
    height: 75%;
    width: 50%;
}
```

#### Text Alignment

The text-align property is used to set the horizontal alignment of a text.

##### Possible Values:

- left → aligns text to the left
- right → aligns text to the right
- center → aligns text to the center
- justify → stretches the lines so that each line has equal width


```css
p {
    text-align: left;
    text-align: right;
    text-align: center;
    text-align: justify;
}
```

#### Text Decorations

```css
p {
    text-decoration: none;
    text-decoration: underline;
    text-decoration: overline;
    text-decoration: line-through;
}
```

#### Font Family

The font-family property is used to set the font family of the text.

```css
p {
    font-family: Arial, Helvetica, sans-serif;
}
```

The program considers Arial first. If it is not found, then it considers Helvetica, and so on.

#### Font Style

```css
p {
    font-style: normal;
    font-style: italic;
    font-style: oblique;
}
```

#### Font Weight

```css
p {
    font-weight: normal;
    font-weight: bold;
    font-weight: bolder;
    font-weight: lighter;
}
```

You can also use 100-900 (lightest to boldest) to tweak the boldness:

```css
p {
    font-weight: 600;
}
```

#### Font Size:

```css
p {
    font-size: 67px;
}
```

# Flask

## Template Code:

```python
import flask

app = flask.Flask(__name__)

# insert code here

if __name__ == "__main__":
    app.run()
```

## Simple Routes:

```python
import flask

app = flask.Flask(__name__)

@app.route('/')
def home():
    return "Welcome"

@app.route('/css')
def css():
    return "This is the css page."

if __name__ == "__main__":
    app.run()
```

## More Complex Routes:

```python
import flask

app = flask.Flask(__name__)

@app.route('/one/')
@app.route('/one/two/')
@app.route('/three/two/one')
def multiple():
    return "Routed to multiple()"

@app.route('/string//')
def string_variable(s):
    return "Routed to string_variable(), s = {} of {}".format(s, str(type(s))[1:-1])

@app.route('/integer/<int:i>/')
def integer_variable(i):
    return "Routed to integer_variable(), i = {} of {}".format(i, str(type(i))[1:-1])

@app.route('/multiple_variables///<float:u>/')
def multiple_variables(s, t, u):
    return "Routed to multiple_variables(), s = {} & t = {} & u = {}".format(s, t, u)

@app.route('/post_only/', methods=['POST'])
def post_only():
    return "Routed to post_only()"

if __name__ == "__main__":
    app.run()
```

## Flask URL lookup

We can find the URL of a page using url_for().

```python
import flask
from flask import url_for

app = flask.Flask(__name__)

@app.route('/')
def home():
    url1 = url_for('fixed_route')
    url2 = url_for('string_variable', s='example')
    url3 = url_for('integer_variable', i=2020)

    print(url1)
    print(url2)
    print(url3)

    return 'Check your shell or command prompt window'

@app.route('/fixed/')
def fixed_route():
    return "Routed to fixed()"

@app.route('/string//')
def string_variable(s):
    return 'Routed to string_variable(), s = {}'.format(s)

@app.route('/integer/<int:i>/')
def integer_variable(i):
    return 'Routed to integer_variable(), i = {}'.format(i)

if __name__ == "__main__":
    app.run()
```

### Comment 1:

You must provide arguments for URLs with variable routes.

#### Take this line for example:

```python
url2 = url_for('string_variable', s='example')
```

Here, the argument for variable route s='example'.

### Comment 2:

You must include this line before using url_for():

```python
from flask import url_for
```

## Flask Redirect

You must include this line before using redirect():

```python
from flask import redirect
```

### Redirecting to an external site:

```python
import flask
from flask import redirect

app = flask.Flask(__name__)

@app.route('/')
def index():
    return redirect('[https://example.com/'](https://example.com/'))

if __name__ == "__main__":
    app.run()
```

### Redirecting to another route:

```python
import flask
from flask import redirect, url_for

app = flask.Flask(__name__)

@app.route('/new_url/')
def moved_index():
    return 'You have reached the new URL!'

@app.route('/')
def index():
    return redirect(url_for('moved_index'))

if __name__ == '__main__':
    app.run()
```

## Templates

Coding out the HTML in the python isn’t very ideal. We should instead link the python code to an existing HTML code (which must be stored in the templates folder).

The python code is outside the templates folder, and all the HTML source files are located in templates.

### Example:

`p13_html_response_with_templates.py`

```python
import flask
from flask import render_template

app = flask.Flask(__name__)

@app.route('/')
def home():
    return render_template('home.html')

@app.route('/greet//')
def greet(name):
    return render_template('greet.html', visitor = name)

if __name__ == "__main__":
    app.run()
```

`home.html` `greet.html`

```jinja2
# Welcome to my home page!

My favourite website is [example.com](https://www.example.com/).

You can greet Alex [here](<{{ url_for('greet', name='Alex')}}>)
```

```jinja2
# Hello, {{visitor}}
```

## Jinja2

In most cases, data processing and computation is done in Python code. The outputs from this computation are then passed to Jinja2 as numbers, strings, lists and other plain data objects. This data is then used to fill in a template to produce the final HTML.

### Safe Filter

To prevent the security issue of injecting HTML, we can treat input as plain text instead of it being HTML by using the safe filter:

`greet.html (modified)`

```jinja2
# Hello, {{visitor|safe}}
```

### Length filter

For simple length checks, we can use the length filter that gives the same result as len() but uses a different syntax.

`greet.html (modified)`

```jinja2
# Hello, {{visitor|length}}
```

### If Statements

#### Syntax:

```jinja2
{% if %}
    
{% elif %}
    
{% else %}
    
{% endif %}
```

#### Example:

`p16_results_using_if.py`

```python
import flask
from flask import render_template

app = flask.Flask(__name__)

@app.route('/')
def home():
    return render_template('results.html', greet=True, name='Alex', show_score=False, score=72)

if __name__ == '__main__':
    app.run()
```

`results.html`

```jinja2
# Results

        {% if greet %}

Hello, {{name}}.

        {% endif %}

        {% if show_score %}

Your score is {{ score }}.

        {% elif score >= 50 %}

You passed.

        {% else %}

You failed.

        {% endif %}
```

### For-in statement

#### Syntax:

```jinja2
{% for data in arr %}
    
{% endfor %}
```

#### Example:

`p17_table_using_for.py`

```python
import flask
from flask import render_template

app = flask.Flask(__name__)

@app.route('/')
def home():
    results = {"English":75, "Mother Tongue":73, "Maths":76, "Computing":78}
    return render_template('table.html', results=results)

if __name__ == "__main__":
    app.run()
```

`table.html`

```jinja2
# Table of Results

            {% for subject in results %}

            {% endfor %}

| Subject NameScore |                      |
| ----------------- | -------------------- |
| {{subject}}       | {{results[subject]}} |
|                   |                      |
```

### For i in range():

#### Syntax:

```jinja2
{% for i in range(arr|length) %}
    
{% endfor %}
```

#### Example:

`p17b_table_using_for_in_range.py`

```python
import flaskjinja2
from flask import render_template

app = flask.Flask(__name__)

@app.route('/')
def home():
    results = [75, 73, 76, 78]
    return render_template('table2.html', results=results)

if __name__ == "__main__":
    app.run()
```

`table2.html`

```jinja2
# Table of Results

            {% for i in range(results|length) %}

            {% endfor %}

| Student No.Score |                |
| ---------------- | -------------- |
| Student {{i+1}}  | {{results[i]}} |
```

## Static Files

This is for images and CSS/Stylesheets.

Flask lets us create a subfolder named static (in the same location as the templates subfolder) to store static resources like images and CSS files. Flask then sets up a view named ‘static’ that (by default) routes any path starting with /static/ to the contents of this subfolder.

### Example:

`p18_static_style_sheet.py`

```python
import flask
from flask import render_template

app = flask.Flask(__name__)

@app.route('/')
def home():
    return render_template('stylish.html')

if __name__ == "__main__":
    app.run()
```

`styles.css`

```css
body {
    background: yellow;
}

h1 {
    border-bottom: 1px solid red;
    color: red;
}
```

## Processing Form Data

When a HTML form is submitted, the browser collects all the input as key-value pairs and encodes it into a single string. This string is then sent to the server using a HTTP request. Depending on how the HTML form is configured, either a GET request or POST request is made.

Parsing key-value pairs encoded in query strings can be tedious and error-prone. Thankfully, if a query string is present, Flask does this parsing for us and lets us access it as a dictionary from a request object that can be imported from the flask module.

### GET Form

Note: Remember to do from flask import request

`p19_analysis_with_get_simplified.py`

```python
import flask
from flask import render_template, request

app = flask.Flask(__name__)

@app.route('/')
def form():
    return render_template('form_with_get_simplified.html')

@app.route('/process/')
def process_with_get():
    if 's' in request.args:
        s_value = request.args['s']
        number_of_words = len(s_value.split())

        return render_template('analysis_results_simplified.html', s = s_value, num_words = number_of_words)

    return "No form data found!"

if __name__ == "__main__":
    app.run()
```

Here, request.args is a dictionary (of key-value pairs) which contains all the input from the HTML form.

`analysis_results_simplified.html`

```jinja2
You entered s: {{ s }}

This string has {{ num_words }} words.
```

### POST Form

Same as GET, but the form data is stored in request.form instead of request.args.

Note: In the

element, you must set the parameter method="post".

Note 2: You must check the request method using request.method == 'GET'.

Note 3: Under @app.route(), methods=['GET', 'POST'] must be added in order to accept both GET and POST methods.

#### Example:

`p20_analysis_with_post_simplified.py`

```python
import flask
from flask import render_template, request

app = flask.Flask(__name__)

@app.route('/', methods=['GET', 'POST'])
def index():
    if request.method == 'GET':
        return render_template('form_with_post_simplified.html')

    if 's' in request.form:
        s_value = request.form['s']

        number_of_words = len(s_value.split())

        return render_template('analysis_results_simplified.html', s = s_value, num_words = number_of_words)

    return 'No form data found!'

if __name__ == '__main__':
    app.run()
```

`analysis_results_simplified.html`

```jinja2
You entered s: {{ s }}

This string has {{ num_words }} words.
```

## Handling File and Image Uploads

`p21_file_uploads.py`

```python
import flask, os, sqlite3
from flask import render_template, request
from flask import send_from_directory
from werkzeug.utils import secure_filename

if not os.path.isfile('db.sqlite3'):
    db = sqlite3.connect('db.sqlite3')
    db.execute('CREATE TABLE photos(photo TEXT)')
    db.commit()
    db.close()

app = flask.Flask(__name__)

@app.route('/', methods=['GET', 'POST'])
def home():
    if request.method == 'POST' and \
        request.files and 'photo' in request.files:

        # Save file
        photo = request.files['photo']
        filename = secure_filename(photo.filename)
        path = os.path.join('uploads', filename)
        photo.save(path)

        # Add filename to database
        db = sqlite3.connect('db.sqlite3')
        db.execute('INSERT INTO photos(photo) VALUES (?)', (filename,))
        db.commit()
        db.close()

    return render_template('form_with_file_upload.html')

@app.route('/view')
def view():
    db = sqlite3.connect('db.sqlite3')
    cur = db.execute('SELECT photo FROM photos')

    photos = []
    for row in cur:
        photos.append(row[0])

    db.close()

    return render_template('view_file_uploads.html', photos=photos)

@app.route('/photos/')
def get_file(filename):
    return send_from_directory('uploads', filename)

if __name__ == '__main__':
    app.run()
```

`form_with_file_upload.html`

```jinja2
Photo:

[View photos](<{{ url_for('view') }}>)
```

`view_file_uploads.py`

```jinja2
{% for photo in photos %}
            [{{ photo }}](<{{ url_for('get_file', filename=photo) }}>)
        {% endfor %}
```

```jinja2
[Home](<{{ url_for('home') }}>)
```

# Socket Programming

## Basic Server:

```python
import socket

my_socket = socket.socket() #1.Server starts first (passive socket)

my_socket.bind(('127.0.0.1', 12345)) #2.Ip(string) and port(number), use a tuple

my_socket.listen() #3.Listen to a connection(wait for a request, pause)

new_socket, addr = my_socket.accept() #6.new_socket(2nd socket (active) used to talk to the client)

print("Connected to: " + str(addr))

new_socket.sendall(b'Hello from server\n') #7.send a byte string use ”b”

new_socket.close() #9.Active socket has to be closed first
my_socket.close()
```

## Basic Client:

```python
import socket

my_socket = socket.socket() #4.create a client

address = input('Enter IPv4 address of server: ')
port = int(input('Enter port number of server: '))

my_socket.connect((address, port)) #5.connect to the server, port randomly assigned by the system

print(my_socket.recv(1024)) #8.receiving the message, 1024 is the max size

my_socket.close()
```

## Note:

For user inputs, you have to use encode() and decode() as the socket only transmits bits, not strings/integers.

my_socket = socket.socket() Server starts first

## Chat Server:

```python
import socket

listen_socket = socket.socket()
listen_socket.bind(('127.0.0.1', 12345))
listen_socket.listen()

chat_socket, addr = listen_socket.accept()
while True:
    data = input('INPUT SERVER: ')
    q = (data == '/q')
    data = data.encode()
    chat_socket.sendall(data + b'\n')

    if (q):
        break

    print('WAITING FOR CLIENT...')
    data = b''
    while not b'\n' in data:
        data += chat_socket.recv(1024)
    data = data.decode()

    if (data == '/q\n'):
        print("CLIENT HAS EXITED, BREAKING THE CONNECTION.")
        break

    print('CLIENT WROTE: ' + data)

chat_socket.close()
listen_socket.close()
```

## Chat Client:

```python
import socket

my_socket = socket.socket()
my_socket.connect(('127.0.0.1', 12345))

while True:
    print('WAITING FOR SERVER...')
    data = b''
    while not b'\n' in data:
        data += my_socket.recv(1024)
    data = data.decode()

    if (data == '/q\n'):
        print('SERVER HAS EXITED, BREAKING THE CONNECTION.')
        break

    print('SERVER WROTE: ' + data)

    data = input("CLIENT INPUT: ")
    q = (data == '/q')
    data = data.encode()
    my_socket.sendall(data + b'\n')

    if (q):
        break

my_socket.close()
```


