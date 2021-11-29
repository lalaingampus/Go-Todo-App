# Golang CRUD TO DO App with MongoDB and Golang

In this case the project will separate to two folder
1. Client
   * Using React, SemanticUI
2. Server
   * Using Golang
   * MongoDB

## Client

using React client

## Setup

Then execute in command prompt:
```
$ cd client
$ npm install
$ npm run start
```
for server in go-server

## Server

## Table of contents 👀
* [General info](#general-info)
* [Technologies](#technologies)
* [Blog](#blog)
* [Setup](#setup)


### General info
GOTOD or Go-TodoApp is a Golang REST API made to show some Todo List. 

#### The GOPOST Object 🍵
| Properties | Description | Type  |
|:----------- |:---------------|:--------|
|Task| the giving name of activity | String| 
|Status| status activity was build | String |


#### Routes ⚡
| Routes | HTTP Methods| Description
|:------- |:---------------|:--------------
| /api/task/     | GET                  | Displays all activity 
| /api/task/      | POST               | Creates a new activity
| /api/task/      | PUT              | Update an activity was build
| /api/deleteAllTask/      | DELETE            | Deletes all activity
|/api/undoTask/{id}| PUT  | Update status of activity
|/api/deleteTask/{id}}| DELETE | Deletes a specific activity, given its id
	
### Technologies
Project is created with:

* Golang 
* gorilla/mux   
* joho/godotenv 
* MongoDB


### How I built it
👉 [Check out the series here!](https://berkaryasemampunya.medium.com/build-crud-apps-in-golang-with-postgresql-3be08d31a1f1)


### Setup
To run this project locally, clone repo and add an `.env` file in the root:
```
MONGODB_URI="MongoDB atlas URI connection string"
DB_NAME="your db want build"
DB_COLLECTION="name table you want build in mongo"
```

Then execute in command prompt:
```
$ cd go-server
$ go mod tidy
$ go run main.go
```

## API Reference

These are the endpoints available from the app

### `GET /api/task/`

Returns result identity

#### Response

<details><summary>Show example response</summary>
<p>

```json
{
  "data": [
    {
     "id":40,
     "name":"hafizh",
     "location": "widodo",
     "age":22,
    }
  ]
}
```

</p>
</details>

---


### `POST /api/task/`

Creates a new identity

#### Request 

This request requires body payload, you can find the example below.

<details><summary>Show example payload</summary>
<p>

```json
{
 "name":"hafizh",
 "location":"kansas",
 "age":12
}
```
</p>
</details>


### `DELETE /api/deleteTask/:id`

Returns a player by id

#### Response

<details><summary>Show example response</summary>
<p>

```json
{
  "meta": {
    "code": 200
  },
  "data": {
    "id": "5f6a5c31d7c451c369802c02",
    "name": "John Doe 1",
    "nickname": "Lolo",
    "position": "forward",
    "created_at": "2020-09-22T20:18:57.957Z"
  }
}
```

</p>
</details>


### `DELETE /deleteAllTask/:id`

Returns a player by id

#### Response

<details><summary>Show example response</summary>
<p>

```json
{
  "meta": {
    "code": 200
  },
  "data": {
    "id": "5f6a5c31d7c451c369802c02",
    "name": "John Doe 1",
    "nickname": "Lolo",
    "position": "forward",
    "created_at": "2020-09-22T20:18:57.957Z"
  }
}
```

</p>
</details>

---

### `UPDATE /api/task/:ID`

Update value of identity
	
#### Response

<details><summary>Show example response</summary>
<p>

```json
{
    "name": "hafizah",
    "location": "toronto",
    "age": 25,  
}
```

</p>
</details>


---

### `UPDATE /api/undoTask/:ID`

Update value of identity
	
#### Response

<details><summary>Show example response</summary>
<p>

```json
{
    "name": "hafizah",
    "location": "toronto",
    "age": 25,  
}
```

</p>
</details>

---
