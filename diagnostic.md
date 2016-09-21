# Rails API Diagnostic

Place your responses inside the fenced code-blocks where indicated by comments.

What is the purpose of a backend?

```bash
The purpose of a backend is to separate user-interface concerns from concerns of data manipulation and storage.
```

Which layer in the MVC pattern is used by the controller to fetch data?

```bash
The model is used by the controller to fetch data from the database.
```

Which layer in the MVC pattern communicates with the model?

```bash
The controller and the database both communicate with the model.
```

Why don't we use views in our interpretation of the MVC pattern?

```bash
# We are focusing on single-page apps which handle our views for us and allow us to update the client-side without having to refresh the page, which would be needed if we were relying on the back-end to render a view and send it to the front-end in as a new HTML page.
```

What does C.R.U.D stand for?

```bash
// Create, Read, Update, Destroy
```

In which part of the MVC pattern can we find C.R.U.D actions?

```bash
// The C.R.U.D. actions are handled ultimately by the controller, but the router is usually what translates the HTTP requests into specific CRUD action requests and routes them to the appropriate controller.
```

List at least 5 standard actions that C.R.U.D corresponds to?

```bash
// Create (POST), Show (GET), Index (GET), Update (PATCH), Destroy (DELETE)
```

A user action fires a `GET` request for `/persons/1`. Explain in detail each step
required for data to be returned to the client. (bullet points or ordered list)

```bash
- User tells client to get ID# 1 of persons, probably by clicking or inputting text into a field.  The browser translates this into an HTTP 'GET' request and sends it to the server-side client.  The router receives this request and translates the HTTP into both a route (to /persons/1) and a standard action request.  It sends the action request, in this case a 'show,' to the persons controller.  The persons controller interprets this request and then asks the model to retreive information listed at /persons/1.  The model says 'ok,' and looks into the database to see if it has any information in that location.  If it does, it retreives it (probably using a SQL query) and sends the data back to the controller.  The controller then sends the data to the server, which ultimately sends it back to the front-end client which then renders/paints it to the screen for the user to view.
```

What is the command to generate a new rails-api app?

```bash
rails new name_of_app --api
```

What is the command to start an instance of a rails server?

```bash
// rails server
```

What are the commands to drop, create and migrate a database? (3 bullet points)

```bash
// rake db:drop
// rake db:create
// rake db:migrate
```

What is the command to scaffold a pet with a name and age attributes (hint:
Also think of the data types for each attribute)?

```bash
// rails generate scaffold Pet name:string Fenreir age:float Float::INFINITY
```
