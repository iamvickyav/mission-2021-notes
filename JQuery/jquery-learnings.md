# JQuery

## Getting Value from URL

```
http://www.refulz.com:8082/index.php#tab2?foo=789

Property    Result
------------------------------------------
host        www.refulz.com:8082
hostname    www.refulz.com
port        8082
protocol    http:
pathname    index.php
href        http://www.refulz.com:8082/index.php#tab2
hash        #tab2
search      ?foo=789

var x = $(location).attr('<property>');

Ref : https://stackoverflow.com/a/14613849
```

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
            success: function (data) {
              alert(data);
            },
            error: function (errorData) {
              alert(errorData.responseText);
            },
          });
        });

        $('#createEmp').click(function () {
          var eId = $('#e-id').val();
          var eName = $('#e-name').val();
          var eDesignation = $('#e-designation').val();
          var eDept = $('#e-dept').val();

          var employeeData = {
            id: eId,
            name: eName,
            role: {
              designation: eDesignation,
              dept: eDept,
            },
          };

          $.ajax({
            type: 'POST',
            url: 'http://localhost:8080/employee/data/add',
            data: JSON.stringify(employeeData),
            contentType: 'application/json',
            success: function (data) {
              alert(data);
            },
            error: function (data) {
              alert(data.responseText);
            },
          });
        });
        $('#updateEmp').click(function () {
          var eId = $('#e-id').val();
          var eName = $('#e-name').val();
          var eDesignation = $('#e-designation').val();
          var eDept = $('#e-dept').val();

          var employeeData = {
            id: eId,
            name: eName,
            role: {
              designation: eDesignation,
              dept: eDept,
            },
          };

          $.ajax({
            type: 'PUT',
            url: 'http://localhost:8080/employee/data/update',
            data: JSON.stringify(employeeData),
            contentType: 'application/json',
            success: function (data) {
              alert(data);
            },
            error: function (data) {
              alert(data.responseText);
            },
          });
        });
        $('#delete').click(function () {
          var id = $('#emp-del-id').val();

          $.ajax({
            type: 'DELETE',
            url: 'http://localhost:8080/employee/data/delete/' + id,
            success: function (data) {
              alert(data);
            },
            error: function (data) {
              alert(data.responseText);
            },
          });
        });
      });
    </script>
  </head>
  <body>
    <div class="container">
      <h2>Search For an Employee</h2>
      <p>Enter Id of the Employee</p>
      <input type="text" id="emp-id" />
      <br />
      <br />
      <button id="search">Submit</button>
    </div>
    <br />
    <br />
    <div class="container">
      <h2>Delete an Employee</h2>
      <p>Enter Id to delete Employee</p>
      <input type="text" id="emp-del-id" />
      <br />
      <br />
      <button id="delete">Submit</button>
    </div>

    <div class="container">
      <h2>Create New Employee</h2>
      <p>Enter Id</p>
      <input type="text" id="e-id" />
      <br />
      <p>Enter Name</p>
      <input type="text" id="e-name" />
      <br />
      <p>Enter Designation</p>
      <input type="text" id="e-designation" />
      <br />
      <p>Enter Dept</p>
      <input type="text" id="e-dept" />
      <br />
      <br />
      <button id="createEmp">Create</button>
      <button id="updateEmp">Update</button>
    </div>
  </body>
</html>
```
