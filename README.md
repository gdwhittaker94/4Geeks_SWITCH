# SWITCH 

SWITCH is an app designed to facilitate real-life language exchanges. It is a low-cost service which supports language exchange organisers by charging a small fee in order to attend an event. Our aim with SWITCH is to make it easy for average users to find language-exchange groups and events near where they live, and primarily to help organisers better manage their groups and events. This idea was based on my own experience as the organiser of a language-exchange group in Burgos for over 2 years.

This was a team-based project that took place over the course of 1 month, using agile methodology in order to manage the progress and evolution of our app, with the purpose of combining all the skills we had learned over the course of 3 months and all the knowledge gained from all the projects completed on the 4Geeks Full-stack developer course.

As a team-based project, obviously the final result of this app is thanks to the work of several people. However, I can highlight my own impressive personal contributions to this project:

🌟 I created the entire project tasks board using [Trello](t.ly/TsI0Y)

🌟 I thought out and visualised the entire user flow of the app using [Figma](t.ly/a-vvS)

🌟 I contributed over 𝟰𝟳% of the project's total commits on Github (see commit history)

🌟 I prepared and put our project into production on [render](www.render.com)

🌟 I integrated the image API [Cloudinary](https://cloudinary.com/) into our project

🌟 I presented the app live in the 4Geeks Demo Day Presentation 𝑒𝑛 𝑒𝑠𝑝𝑎𝑛̃𝑜𝑙 🇪🇸 [See here](t.ly/ryr-F)

This app was made using Reactjs, CSS, and Bootstrap on the frontend, Python, Flask and SQLAlchemy on the backend, with the Cloudinary API and Paypal API integrated into the app, and everything joined together via Github.

[View the live project here](https://sample-service-name-ficr.onrender.com/)
![switch](https://github.com/gdwhittaker94/4Geeks_SWITCH/assets/105855731/c252e0a3-8d57-43e7-8409-b7a9cdb09f02)



## Project Notes

- Documentation can be found here: https://start.4geeksacademy.com/starters/react-flask
- Here is a video on [how to use this template](https://www.loom.com/share/f37c6838b3f1496c95111e515e83dd9b)
- Integrated with Pipenv for package managing.
- Fast deployment to heroku [in just a few steps here](https://start.4geeksacademy.com/backend/deploy-heroku-posgres).
- Use of .env file.
- SQLAlchemy integration for database abstraction.

### 1) Installation:

> If you use Github Codespaces (recommended) or Gitpod this template will already come with Python, Node and the Posgres Database installed. If you are working locally make sure to install Python 3.10, Node 

It is recomended to install the backend first, make sure you have Python 3.8, Pipenv and a database engine (Posgress recomended)

1. Install the python packages: `$ pipenv install`
2. Create a .env file based on the .env.example: `$ cp .env.example .env`
3. Install your database engine and create your database, depending on your database you have to create a DATABASE_URL variable with one of the possible values, make sure you replace the valudes with your database information:

| Engine    | DATABASE_URL                                        |
| --------- | --------------------------------------------------- |
| SQLite    | sqlite:////test.db                                  |
| MySQL     | mysql://username:password@localhost:port/example    |
| Postgress | postgres://username:password@localhost:5432/example |

4. Migrate the migrations: `$ pipenv run migrate` (skip if you have not made changes to the models on the `./src/api/models.py`)
5. Run the migrations: `$ pipenv run upgrade`
6. Run the application: `$ pipenv run start`

> Note: Codespaces users can connect to psql by typing: `psql -h localhost -U gitpod example`

### Undo a migration

You are also able to undo a migration by running

```sh
$ pipenv run downgrade
```

### Backend Populate Table Users

To insert test users in the database execute the following command:

```sh
$ flask insert-test-users 5
```

And you will see the following message:

```
  Creating test users
  test_user1@test.com created.
  test_user2@test.com created.
  test_user3@test.com created.
  test_user4@test.com created.
  test_user5@test.com created.
  Users created successfully!
```

### **Important note for the database and the data inside it**

Every Github codespace environment will have **its own database**, so if you're working with more people eveyone will have a different database and different records inside it. This data **will be lost**, so don't spend too much time manually creating records for testing, instead, you can automate adding records to your database by editing ```commands.py``` file inside ```/src/api``` folder. Edit line 32 function ```insert_test_data``` to insert the data according to your model (use the function ```insert_test_users``` above as an example). Then, all you need to do is run ```pipenv run insert-test-data```.

### Front-End Manual Installation:

-   Make sure you are using node version 14+ and that you have already successfully installed and runned the backend.

1. Install the packages: `$ npm install`
2. Start coding! start the webpack dev server `$ npm run start`
