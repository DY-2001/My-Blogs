#API Documentation
https://docs.google.com/document/d/1rFPB6KtUPmW12AjsHibKD4iicE15rbmKHa6TlIy7ufk/edit

#Project Vedio Link
https://youtu.be/P5TJO2ruvMI

## Frontend Setup
```
cd frontend
npm install
npm start
```


## Backend Setup
```
cd api
npm install
nodemon index.js
```






# API Documentation

## Table of Contents

1. [Introduction](#introduction)
2. [Authentication](#authentication)
3. [User Registration](#user-registration)
4. [User Login](#user-login)
5. [User Logout](#user-logout)
6. [User Profile](#user-profile)
7. [Create Post](#create-post)
8. [Update Post](#update-post)
9. [Get Posts](#get-posts)
10. [Get Single Post](#get-single-post)
11. [Like/Unlike Post](#like-unlike-post)

## Introduction

This document provides documentation for the RESTful APIs implemented in the backend server.

**Base URL:** `http://localhost:4000`

## Authentication

The authentication for this API is implemented using JSON Web Tokens (JWT). Users need to include a valid token in the request headers for authenticated endpoints.

## User Registration

### Endpoint

- **URL:** `/register`
- **Method:** `POST`
- **Request Body:**
  - `username`: String (required)
  - `password`: String (required)

### Response

- 200 OK: Returns user information.
- 400 Bad Request: Returns an error message if registration fails.

## User Login

### Endpoint

- **URL:** `/login`
- **Method:** `POST`
- **Request Body:**
  - `username`: String (required)
  - `password`: String (required)

### Response

- 200 OK: Returns a user token.
- 400 Bad Request: Returns an error message if login fails.

## User Logout

### Endpoint

- **URL:** `/logout`
- **Method:** `POST`

### Response

- 200 OK: Clears user token.

## User Profile

### Endpoint

- **URL:** `/profile`
- **Method:** `GET`

### Response

- 200 OK: Returns user information.
- 400 Bad Request: Returns an error message if profile retrieval fails.

## Create Post

### Endpoint

- **URL:** `/post`
- **Method:** `POST`
- **Request Body:**
  - `title`: String (required)
  - `summary`: String (required)
  - `content`: String (required)
  - `file`: File (required)

### Response

- 200 OK: Returns post information.
- 400 Bad Request: Returns an error message if post creation fails.

## Update Post

### Endpoint

- **URL:** `/post`
- **Method:** `PUT`
- **Request Body:**
  - `id`: String (required)
  - `title`: String
  - `summary`: String
  - `content`: String
  - `file`: File

### Response

- 200 OK: Returns updated post information.
- 400 Bad Request: Returns an error message if post update fails.

## Get Posts

### Endpoint

- **URL:** `/post`
- **Method:** `GET`

### Response

- 200 OK: Returns an array of posts.
- 400 Bad Request: Returns an empty array if retrieval fails.

## Get Single Post

### Endpoint

- **URL:** `/post/:id`
- **Method:** `GET`

### Response

- 200 OK: Returns a single post.
- 400 Bad Request: Returns an error message if retrieval fails.

## Like/Unlike Post

### Endpoint

- **URL:** `/post/:postId/like`
- **Method:** `POST`
- **Request Body:**
  - `userInfo`: Object (required)

### Response

- 200 OK: Returns the updated post.
- 500 Internal Server Error: Returns an error message if liking/unliking fails.
