# Working with forms
An HTML Form is a group of one or more fields/widgets on a web page that can be used to collect data from users and send it to a server. Because there are acceptable widgets for entering many different types of data, including as text boxes, checkboxes, radio buttons, date pickers, and so on, forms are a flexible technique for gathering user input. Forms are also a safe way to share data with the server because they allow us to transmit data through POST requests that are protected against cross-site request forgery.

- The form is defined in HTML as a collection of elements inside <form>...</form> tags, containing at least one input element of type="submit".
```
<form action="/team_name_url/" method="post">
    <label for="team_name">Enter name: </label>
    <input id="team_name" type="text" name="name_field" value="Default name for team.">
    <input type="submit" value="OK">
</form>

``` 
the result will be :
<form action="/team_name_url/" method="post">
    <label for="team_name">Enter name: </label>
    <input id="team_name" type="text" name="name_field" value="Default name for team.">
    <input type="submit" value="OK">
</form>

- While we only have one text field for entering the team name in this example, a form can contain any number of extra input elements and labels. The type attribute of a field specifies the type of widget that will be displayed. The field's name and id are used to identify it in JavaScript/CSS/HTML, while value specifies the field's initial value when it is first displayed. The matching team label is supplied with a for field containing the id value of the related input (see "Enter name" above).

- The submit input will be displayed as a button by default. This can be pressed to upload the data in all the other input elements in the form to the server (in this case, just the team_name field). The form attributes define the HTTP method used to send the data and the destination of the data on the server (action):
    - action: The resource/URL where data is to be sent for processing when the form is submitted. If this is not set (or set to an empty string), then the form will be submitted back to the current page URL.
    - method: The HTTP method used to send the data: post or get.
        - The POST method should always be used if the data is going to result in a change to the server's database, because it can be made more resistant to cross-site forgery request attacks.
        - The GET method should only be used for forms that don't change user data (for example, a search form). It is recommended for when you want to be able to bookmark or share the URL.