# Item Catalog
## Introduction
<p>This is a python module that queries a database for items on restaurant menus and then dynamically generates complete menus in the form of web pages and API endpoints. This module uses Flask framework to develop the application. Users can edit or delete items they've created. Adding, deleteing and editing items require oauth2 authorization.</p>
<h2>Instructions</h2>
<ul type="disc">
  <li><h3>Setup</h3></li>
  <ul type="disc">
    <li><h3>Install Git</h3>
    <p>If you don't already have Git installed, download Git from <a href="git-scm.com">git-scm.com</a>. Install the version for your         operating system.<br>
    On Windows, Git will provide you with a Unix-style terminal and shell (Git Bash). (On Mac or Linux systems you can use the regular     terminal program.)</p>
    <li><h3>Install <a href="https://www.vagrantup.com/">Vagrant</a> and <a href="">VirtualBox</a></h3></li>
  </ul>
  <li><h3>Fetch the Source Code and VM Configuration</h3></li>
  <ul type="disc">
   <li>Clone the Item Catalog repository to your local machine:<li>
   <pre>git clone https://github.com/visheshbanga/Item-Catalog</pre>
   <p><b>Windows:</b> Use the Git Bash program (installed with Git) to get a Unix-style terminal.<br>
   <b>Other systems:</b> Use your favorite terminal program.</p>
  </ul>
  <li><h3>Set up a Google Plus oauth application</h3></li>
  <ul type="disc">
   <li>Go to https://console.developers.google.com/project and login with Google.</li>
   <li>Create a new project.</li>
   <li>Select "API's and Auth -> Credentials -> Create a new OAuth client ID" from the project menu.</li>
   <li>Select Web Application.</li>
   <li>On the consent screen, type in a product name and save.</li>
   <li>In Authorized javascript origins add: http://0.0.0.0:8000</li>
   <li>Click create client ID.</li>
   <li>Click download JSON and save it into the root director of this project.</li>
   <li>Rename the JSON file "client_secrets.json"</li>
  </ul>
  <li><h3>Run the Virtual Machine</h3></li>
  <p>Using the terminal, change directory to project directory, then type vagrant up to launch your virtual machine.</p>
  <li><h3>Running the App</h3></li>
  <ul type="disc">
   <li>Once it is up and running, type vagrant ssh. This will log your terminal into the virtual machine, and you'll get a Linux shell prompt.</li>
   <li>Change directory to the /vagrant directory by typing cd /vagrant. This will take you to the shared folder between your virtual machine and host machine.</li>
   <li>Type ls to ensure that you are inside the directory that contains project files.</li>
   <li>Now type python database_setup.py to initialize the database.</li>
   <li>Type python lotsofmenus.py to populate the database.</li>
   <li>Type python project.py to run the Flask web server. In your browser visit <a href="http://localhost:8000"> http://localhost:8000</a> to view the catalog app.</li>
  </ul>
 </ul>
