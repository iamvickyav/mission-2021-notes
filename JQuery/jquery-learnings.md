# JQuery

## JQuery Sample codes

```html
<html>
  <head>
    <!-- Latest compiled and minified CSS -->
    <link
      rel="stylesheet"
      href="https://maxcdn.bootstrapcdn.com/bootstrap/3.4.1/css/bootstrap.min.css"
    />
    <!-- jQuery library -->
    <script src="https://ajax.googleapis.com/ajax/libs/jquery/3.5.1/jquery.min.js"></script>
    <!-- Latest compiled JavaScript -->
    <script src="https://maxcdn.bootstrapcdn.com/bootstrap/3.4.1/js/bootstrap.min.js"></script>
    <script>
      $(document).ready(function () {
        $('#search').click(function () {
          var empId = $('#emp-id').val();
          $.ajax({
            type: 'GET',
            url: 'http://localhost:8080/employee/data/name/' + empId,
            success: function (employee) {
              alert(employee);
            },
            error: function (errorData) {
              alert(errorData.responseText);
            },
          });
        });
      });
    </script>
  </head>
  <body>
    <div class="container">
      <p>Enter Id of the Employee</p>
      <input type="text" id="emp-id" />
      <br />
      <br />
      <button id="search">Submit</button>
    </div>
    <br />
    <br />
    <div id="result" class="container"></div>
  </body>
</html>
```
