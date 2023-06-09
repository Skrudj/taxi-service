# taxi-service
<p>This is a simple CRUD web app simulating how taxi service works. 
User could add and delete cars, manufacturers, assign drivers to cars. 
Drivers are created through registration. Also exists simple cabinet where driver could see 
information about himself, his assigned cars and assign to him another cars</p>

## Features
<ul>
    <li>Authorisation.</li>
    <li>Create and delete cars.</li>
    <li>Create and delete manufacturers.</li>
    <li>Register driver.</li>
    <li>Show list of all cars.</li>
    <li>Show list of all drivers.</li>
    <li>Show list of assigned cars of currently authorised driver.</li>
</ul>

## How to start
<ul>
    <li>Clone this repo to your local machine.</li>
    <li>Configure static variables with your DB configs.</li>
    <li>Run init_db.sql at your workbench to initialize database.</li>
    <li>Run <code>mvn clean package</code> in terminal to build war file.</li>
    <li>Deploy this war to servlet container like tomcat.</li>
    <li>Enjoy.</li>
</ul>

## Structure
<ul>
    <li>Controller:</li>
    <ul>
        <li>LoginController: - <code>/login</code> - shows login page and decide whether to authorize user or not</li>
        <li>LogoutController: - <code>/logout</code> - invalidates current session</li>
        <li>CabinetController: - <code>/cabinet</code> - show current user cabinet page</li>
        <li>AddCarController: - <code>/cars/add</code> - handles create new car request</li>
        <li>AddDriverToCarController: - <code>/cars/drivers/add</code> - handles assign driver to car request</li>
        <li>DeleteCarController: - <code>/cars/delete</code> - handles delete car request</li>
        <li>GetAllCarController: - <code>/cars</code> - show all cars information</li>
        <li>RemoveDriverFromCarController: - <code>/cars/remove</code> - handles remove driver from car request</li>
        <li>AddDriverController: - <code>/drivers/add</code> - handles registration request</li>
        <li>DeleteDriverController: - <code>/drivers/delete</code> - handles delete driver request</li>
        <li>GetAllDriverController: - <code>/drivers</code> - show all drivers information</li>
        <li>AddManufacturerController: - <code>/manufacturers/add</code> - handles create manufacturer request</li>
        <li>DeleteManufacturerController: - <code>/manufacturers/delete</code> - handles delete manufacturer request</li>
        <li>GetAllManufacturerController: - <code>/manufacturers</code> - show all manufacturers information</li>
        <li>IndexController: - <code>/index</code> - show main page</li>
    </ul>
    <li>Dao: Data Access Object interfaces and their implementations.</li>
    <li>Exception: custom exceptions that may be thrown while the app works.</li>
    <li>Model: entities models, that are operated while the app works.</li>
    <li>Service: service interfaces and their implementations, where all the business logic runs.</li>
    <li>Util: Class that creates DB connection and is used in Dao.</li>
    <li>Filter: filter that allow to implement authorisation functionality.</li>
    <li>Resources: all non java files. Here: SQL DB init file.</li>
    <li>WEB-INF: all servlet config files.</li>
    <li>Views: all JSP pages and CSS files that could be operated while the app works.</li>
</ul>

## Used technologies
<ul>
    <li>Java <code>v.17.0.6</code></li>
    <li>Maven <code>v.4.0.0</code></li>
    <li>JDBC <code>v.4.2</code></li>
    <li>MySql <code>v.8.0.28</code></li>
    <li>Javax Servlets <code>v.4.0.1</code></li>
    <li>Tomcat <code>v.9.0.73</code></li>
</ul>

## Author
Sinilov Serhii