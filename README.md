 Web Lab - Spring MVC
 ====================
In this lab, we will explore how to develop and test a web service using the Spring MVC framework. We will create a concert management application , where users can add new concert, delete it and list them all. We will cover the development of the controller and template views.

## Develop Model
We will develop a model class `Concert` that will represent a concert. The class will have the following attributes:
* `id`: This attribute will store the unique id of the concert.
* `title`: This attribute will store the name of the concert.
* `performer`: This attribute will store the name of the performer.
* `date`: This attribute will store the date of the concert.
* `description`: This attribute will store the description of the concert.

You neeed to create two constructors:
* `Concert()`: This is the default constructor.
* `Concert(String title, String description)`: This is the parameterized constructor.

## Develop Controller
We will develop a controller class `ConcertController` that will handle the HTTP requests. The controller will have the following methods:
* `listConcerts`: This method will handle the HTTP GET request to `/concerts` URL. It will return the `concerts` view that will display the list of concerts.
* `addAConcertForm`: This method will handle the HTTP GET request and return the `add-concert-form` view that will display the form to add a new concert.
* `saveConcert`: This method will handle the HTTP POST request to `/concerts` URL. It will save the concert in the database and redirect to the `concerts` to list all concerts.
* `deleteConcert`: This method will handle the HTTP GET request to `/delete-concert/{id}` URL. It will delete the concert with the given id and redirect to the `concerts` to list all concerts.
* `removeAllConcerts`: This method will handle the HTTP GET request to `/delete-concert` URL. It will delete all concerts and redirect to the `concerts` to list all concerts.

## Develop Views
We will develop the following views:
* `list-concerts.html` view: This view will display the list of concerts. It will have the following features:
  * It will display the list of concerts in a table.
  * It will have a link to delete a concert.
  * It will have a link to add a new concert.
  * It will have a link to delete all concerts.
* `add-concert-form.html` view: This view will display the form to add a new concert. 


## Unit Test
Run the unit tests in `ConcertControllerTest` class to test the service. You can run the tests using the following command:
```
mvn verify
```