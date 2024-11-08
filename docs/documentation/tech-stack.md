#### Frontend

| **Technology**                                            | **Purpose**                                                | **License** |
|-----------------------------------------------------------|------------------------------------------------------------|-------------|
| [**React**](https://reactjs.org/)                         | Javascript library for website and user interface building | MIT         |
| [**Vite**](https://vite.dev/)                             | JavaScript build tool                                      | MIT         |
| [**Axios**](https://axios-http.com/)                      | Javascript library for http requests                       | MIT         |
| [**React Router**](https://reactrouter.com/en/main)       | Javascript framework for client side routing               | MIT         |
| [**Tailwind**](https://tailwindcss.com/)                  | CSS framework for consistent styling                       | MIT         |
| [**Framer Motion**](https://www.framer.com/motion/)       | Animations and div manipulation                            | MIT         |
| [**Zustand**](https://zustand-demo.pmnd.rs/)              | Easy library state management for React                    | MIT         |
| [**TanStack Query**](https://tanstack.com/query/latest)   | Data-fetching library                                      | MIT         |
| [**pnpm**](https://pnpm.io/)                              | Fast, disk space efficient package manager                 | MIT         |


Designed for two users - the manager (admin) and the regular user (person who decides what to display).
The frontend consists of 9 main technologies; It uses Vite with React which is served via an Nginx server, which also serves as a reverse proxy for the Spring Boot backend. For styling, Tailwind CSS is utilized in React, alongside with other libraries such as Zustand, Framer Motion, Axios, React Router, TanStack Query and pnpm.
##### React 
We opted for React due to its widespread usage and backing by a major company, Meta. This framework facilitates the creation and reuse of components across multiple pages within the application. Additionally, React provides a plethora of libraries that we can leverage if needed.
##### Vite
Vite is used to make developing a faster and better experience alongside the freedom of configurations compared to our initial approach of Create React Application (CRA). This allows it to be more optimized as well has fast reload and builds.
##### Tailwind
We've opted for the Tailwind CSS framework because, unlike other CSS frameworks such as Bootstrap, it provides enhanced control over HTML components without requiring direct manipulation of vanilla CSS. This streamlines the development process and offers better maintainability compared to traditional CSS approaches.
##### React Icons
React Icons is a React library that offers a diverse range of icons that we can utilize within our HTML content.
##### Axios
Axios is a straightforward, promise-based HTTP client that ensures enhanced consistency across various browsers. It operates at a higher abstraction level compared to fetch, resulting in more readable code. Axios also allows the creation of Request and Response Interceptors, which will be useful for adding authentication headers.
##### Zustand
Zustand is a state manager with a hook-based API that allows for the management of local states within the application. Additionally, these states can be stored in the local storage.
##### React Router
React Router enables client-side routing, providing a more responsive and speedy experience for users.
##### TanStack Query
TanStack Query, formerly known as React Query v3, is used to handle caching, updating data, manage memory and try to optimize the application as much as possible, removing redudant calls that would otherwise be needed. This helps keep both the code clean but also make it easy to manipulate and keep track of changes.
##### pnpm
pnpm is used to help avoid bugs with packages and by using hard linking and symbolic linking to a global on-disk content-addressable store we save space.

---

#### Backend

| **Technology**                                            | **Purpose**                                        | **License** |
|-----------------------------------------------------------|----------------------------------------------------|-------------|
| [**Spring Boot**](https://spring.io/projects/spring-boot) | microservice-based Java web framework              | Apache 2.0  |
| [**Mosquitto**](https://mosquitto.org/)                   | lightweight message broker using MQTT              | EPL         |


##### Spring Boot
The backend will utilize Spring Boot for its effortless integration with various databases and robust security features. Furthermore, Spring Boot simplifies the testing process, ensuring reliable software quality.
##### Mosquitto
In the backend we used mosquitto as a message broker, which allows us to comunicate with the media player.

---

#### Databases
| **Technology**                                | **Purpose**                                                                      | **License** |
|-----------------------------------------------|----------------------------------------------------------------------------------|-------------|
| [**PostgreSQL**](https://www.postgresql.org/) | object-relational database used for user, files and monitors information storage | PostgreSQL  |
| [**InfluxDB**](https://www.influxdata.com/)   | time series database used for log storage and management                         | MIT         |
| [**MongoDB**](https://www.mongodb.com/)       | NoSQL document database                                                          |  SSPL       |


##### PostgreSQL
As the main database we used PostgreSQL, a relational database because our entities were very connected and also this database is very scalable.
##### InfluxDB
InfluxDB is used to keep logs from the monitors, Spring Boot, and the status of the monitor. We chose this database because it allows us to associate a timestamp with each entry, facilitating tracking and analysis of when events occurred. 
##### MongoDB
Mongo is used to make our templates customizable and easy to manage by having Widgets, Rules and Templates being documents. 

---

#### Media Player

##### python
The media player is fully implemented in python.

##### pywebview
Used to build the GUI for our program using JavaScript, HTML, and CSS.

##### Paho MQTT
To communicate with the backend we utilize the Paho MQTT client for python.

##### RRule
In the scheduler we utilize RRule to generate the start and end dates.

##### Flask
Used to fetch content from external apis and also used for the configuration page.

##### NetworkManager
We use the nmcli utility to create hotspots and manage internet connection.

---

#### Deployment
To provide an easy-to-start implementation, we are using docker to facilitate initialization and development.