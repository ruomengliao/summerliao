# 2023.06.08 Project Construction

Download and install the node environment from the computer, and initialize the project through the node's secret
command "npm init", which includes the file name for creating the project. In node development, using npm init will
generate a pakeage.json file, which is mainly used to record detailed information about the project. It will record the
packages we need to use in project development, as well as the detailed information of the project, in this project. It
will be more convenient for future version iterations and project migrations. It also prevents the project from running
normally due to accidentally deleting a package during later project maintenance. Another advantage of using npm init to
initialize a project is that there is no need to send the project dependency package to the other party during project
transfer. After the other party accepts your project, they can execute npm install to download all project dependencies
into the project.

* Package name: What is the name of your project
* Version: version number
* Description: Description of the project
* Entry point: The entry file for the project
* Test command: What command should be used to execute the script file when the project starts
* Git repository: If you want to upload the project to git, you need to fill in the warehouse address of git
* Keywords: project keywords
* Author: The name of the author
* License: The certificate required for issuing the project

# June 9, 2023 Project Development

Create a public folder according to the requirements, which includes a font folder to store font files, an icon folder
to store icon files, an image folder to store image resources, a js folder to store js files, and a style folder to
store CSS style sheets.
Firstly, we created an index.html file as the main page entry file, which mainly displays the sub entries of several
pages, including the entry to the recording information page, the entry to the map page, and the entry to the start
timing page. Click the go button to enter the timing, click the top to enter the recording page, and click the map icon
to enter the map page
Map. html: This is the map page, where Google Maps has been introduced online to insert map information into the webpage

* day.html: This is a page that records motion history. It uses JavaScript browser caching and reading technology to
  read the motion records. The data is cached in JSON format and needs to be cached and parsed after retrieval
  The caching techniques in this include:
    1. SessionStorage: Temporary session storage: As long as the current session window is not closed, the stored
       information will not be lost. Even if the page is refreshed or the code is changed in the editor, the stored
       session information will not be lost.
    2. LocalStorage: Permanent storage will always store the data in the client's storage mode. Even if the browser is
       closed, the previously stored data that has not been actively cleared can still be seen the next time it is
       opened (even if it is Antivirus software or the browser's built-in clearing function, the data stored in
       localStorage cannot be cleared)
    3. Cookies are small files stored on a user's computer that store appropriate amounts of data for specific clients
       and websites, and can be accessed by a web server or client browser, allowing the server to provide customized
       pages for specific users, or the page itself can contain scripts that know the data in the cookie.
       In this code, localStorage is used for caching, as after multiple considerations, only localStorage is suitable
       for the current needs
* Timing page: The timing page is displayed in the form of a pop-up, and the code is still in the index. html file.
  Because some data needs to be displayed on the homepage for convenience, there is no separate page separation. The
  hidden appearance here is done through CSS positioning, and the content about positioning in CSS is: position:
  relative | absolute | static | fixed. Static has no specific settings and follows basic positioning rules, and cannot
  be hierarchical through z-index. In a text stream, any element is constrained by its position by the text stream, but
  through CSS, we still enable these elements to change their position. We can use floats to make the element float, or
  we can use margins to make the element move its position.
  * Relative: does not deviate from the document flow, references its static position through top, bottom, left, right positioning, and can be hierarchical graded through z-index.
    Absolute is separated from the document flow and located through top, bottom, left, and right. Select its nearest parent positioning element. When the parent position is static, the absolute element will be positioned at the origin of the body coordinate, and can be hierarchical through z-index.
    Fixed positioning, where the fixed object is a browser visual window rather than a body or parent element. Hierarchical grading can be achieved through z-index.
    Cascade rating for positioning in CSS: z index: auto | number;
    Auto follows the positioning of its parent object
    Number is an integer value without units. It can be negative, and in our project, we mainly combine relative and absolute through overflow: hidden; Hide the excess parts
# Run Secret Order:
    npm install
    npm run serve
# environment
    http://localhost:8888/
