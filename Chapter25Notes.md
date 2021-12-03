when "for" is used, <input> does not have to be inside of the label
Name attributre is used to identify an input's value when data is submitted



- forms collect data input by the user
- form submission is an http request sent to server containing values in a form
- form submission is triggered by clicking button
  - can use `<input type="submit"/> or """<button>Submit</button>"""
- http request sent to location set in `action` attribute of form tag
  - IF action attribute empty/not present. Form submits to URL of current page
- these submit something known as query string parameters
  - this happened because we sent it via GET (as you can see the values)
  - spaces are not allowed in URLS and are replaced in the browser with `+`
- key  value pair is created for each `<input>` tag. keys are the values of hte `name` attributes. and the values are paried with the content of the `value` attributes



25.3 POST

- to submit a form with post. do the following: `<form action="" method="POST">`
- data submitted with POST will be submitted in body of HTTP request.
- POST is better because GET request UWL's are usually cached and logged. Leaking possibly sensitive data
- form handlers are web server actions that receive, inspect and process requests.



25.4 Text Inputs

- there are password, text area, and normal text input 

on is default value when checked for checkbox



name attribute must be same to group radio buttons together



most form submission will be post request, especially changing stuff on the server