# SpringBoot Learnings

## Controller

### RestController

```java
@RestController
```

### RequestMapping

```java
// RequestMethod as GET
@RequestMapping(value="/employee/all", method = RequestMethod.GET)

// RequestMethod as POST
@RequestMapping(value="/employee/create", method = RequestMethod.POST)
```

### RequestBody

```java
// RequestBody with POST
@RequestMapping(value = "/employee", method = RequestMethod.POST)
ResponseEntity createEmployee(@RequestBody Employee employee)

// RequestBody with PUT
@RequestMapping(value = "/employee", method = RequestMethod.PUT)
ResponseEntity updateEmployee(@RequestBody Employee employee)
```

### PathVariable

```java
// PathVariable with POST
@RequestMapping(value = "/employee/{id}", method = RequestMethod.POST)
ResponseEntity getEmployeeById(@PathVariable("id") Integer id)
```

## Autowire Dependencies

### Service for Business Logic

```java
@Service
class EmployeeService {

}

@RestController
class EmployeeController {

    @Autowired
    EmployeeService employeeService;
}
```

### Repository for DB interaction

```java
@Repository
class EmployeeRepository {

}

@Service
class EmployeeService {

    @Autowired
    EmployeeRepository employeeRepository;
}
```

## To interact with DB

### Changes in pom.xml

```xml
<dependency>
    <groupId>mysql</groupId>
	<artifactId>mysql-connector-java</artifactId>
</dependency>

<dependency>
    <groupId>org.springframework.boot</groupId>
	<artifactId>spring-boot-starter-data-jdbc</artifactId>
</dependency>
```

### Changes in application.properties

```properties
spring.datasource.url=jdbc:mysql://localhost:3306/itech_db
spring.datasource.username=root
spring.datasource.password=rootroot
```

### JDBCTemplate for DB calls

```java
@Repository
public class EmployeeDataRepository {

    @Autowired
    JdbcTemplate jdbcTemplate;

    List<Employee> getAllEmployee() {
        String query = "SELECT * FROM employee";

        List<Employee> list = jdbcTemplate.query(query, new RowMapper<Employee>() {

            @Override
            public Employee mapRow(ResultSet resultSet, int i) throws SQLException {
                Employee employee = new Employee();
                employee.setId(resultSet.getInt("id"));
                employee.setName(resultSet.getString("name"));

                Role role = new Role();
                role.setDesignation(resultSet.getString("designation"));
                role.setDept(resultSet.getString("dept"));

                employee.setRole(role);
                return employee;
            }
        });

        return list;
    }
}
```
