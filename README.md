# Thinkful-final-Capstone: Restaruant Reservation System

## Project Summary

---

A Restaurant Reservation System that is used to keep track of guest reservations and table assignments. The user can create new reservations and search for reservations by phone number. They can also keep track of where reservations are seated and tables are occupied.

### The Dashboard

![Dashboard](https://user-images.githubusercontent.com/79220589/143131915-1665cb85-5f61-42a4-8eb0-0e645726217a.PNG)

### Dashboard with Reservation

![DashBoradWithReservations](https://user-images.githubusercontent.com/79220589/143132008-71fe5661-d6bf-4bfd-a25e-dac14fa003db.jpg)

### Dashboard with Seated Reservation

![ReservationsWithSeatedPeople](https://user-images.githubusercontent.com/79220589/143132167-26ca1350-d95d-417b-b6ce-43d23b2486a9.jpg)

### Create new Reservation

![ReservationForm](https://user-images.githubusercontent.com/79220589/143132309-da4cd445-027a-4d15-835c-50aa0ba6f09a.jpg)

### Create new Table

![NewTableForm](https://user-images.githubusercontent.com/79220589/143132368-beeaa4bb-3be6-4efd-911f-e14e0e873380.jpg)

### Search for Reservation

![SearchForm PNG](https://user-images.githubusercontent.com/79220589/143132377-4d36ad4b-b8bb-4bd3-8fe6-b2b9d9f1d52e.jpg)

### Tech Stack

## This web app was developed using HTML, CSS, JavaScript, BootStrap, React, Express, Node, PostgreSQL, and Knex.

### API Dcoumentation

| Route                                        | Method | Status | Description                                                         |
| -------------------------------------------- | ------ | ------ | ------------------------------------------------------------------- |
| /reservations                                | GET    | 200    | Returns a list of reservations for the current date                 |
| /reservations                                | POST   | 201    | Creates a new reservation                                           |
| /reservations/:reservation_id([0-9]+)        | GET    | 200    | Returns the reservation for the given ID                            |
| /reservations/:reservation_id([0-9]+)        | PUT    | 200    | Updates the reservation for the given ID                            |
| /reservations/:reservation_id([0-9]+)/status | PUT    | 200    | Updates the status of the reservation for the given ID              |
| /tables                                      | POST   | 201    | Creates a new table                                                 |
| /tables                                      | GET    | 200    | Returns list of tables                                              |
| /tables                                      | DELETE | 200    | Deletes table                                                       |
| /tables/:table_id([0-9]+)                    | GET    | 200    | Returns the table for the given ID                                  |
| /tables/:table_id([0-9]+) /seat              | PUT    | 200    | Seats a reservation at the given table_id                           |
| /tables/:table_id([0-9]+) /seat              | DELETE | 200    | Changes the occupied status to be unoccupied for the given table_id |

---

### Installation :

To install dependencies, use npm install.

```
npm Install
```

To start the server (with Nodemon), use...

```
npm run start:dev
```

Connect to a postgresql database by using the following command to create a .env file from the sample provided.

```
cp ./back-end/.env.sample ./back-end/.env

cp ./front-end/.env.sample ./front-end/.env
```

Then Update the `./back-end/.env` file with your postgresql database URL(s)

```
// back-end .env example -> Connects to database
DATABASE_URL = enter - your - production - database - url - here;
DATABASE_URL_DEVELOPMENT = enter - your - development - database - url - here;
DATABASE_URL_TEST = enter - your - test - database - url - here;
DATABASE_URL_PREVIEW = enter - your - preview - database - url - here;
LOG_LEVEL = info;
```

You should not need to make changes to the `./front-end/.env` file unless you want to connect to a backend at a location other than `http://localhost:5000`.
