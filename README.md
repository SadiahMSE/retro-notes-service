# Retro notes Service
This service exists to allow a client to interface with a database (currently using an in memory DB which does not persist between runs of the service) which maintains a list of retro actions.

## Running the Service

To run the service as a Spring-Boot app run ```./gradlew bootRun``` in the root directory.

To fill the database with some example notes and consent documents cd into the ```scripts``` directory and run ```sh post-data.sh```.

Then navigate to http://localhost:8080/api/notes to see the list of retro notes.


## GET retro notes endpoint
```/api/notes```

Will return a list of all notes currently stored in the DB

## POST retro note endpoint
```/api/notes```

Allows the user to post a new note.

Example:
```
{
  "title":"title",
  "content":"content",
  "date":"2018-08-03T12:12:12+01:00"
}
```

## GET consent endpoint
```/api/consent/latest```

Will return the consent document with the highest version number.

## POST consent endpoint
```/api/consent```

Allows the user to post a new version of the consent document.

Example:
```
{
  "version":"3",
  "content":"You hereby kinda promise to do everything agreed in the retro."
}
```
