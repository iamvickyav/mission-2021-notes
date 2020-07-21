# JSON

- Javascript Object Notation
- .json file extension

## JSON Format explained

- Key value pairs
- Key is always String (inside double quotes "")
- Value can be
  - String
  - Number
  - Boolean
  - JSON Array []
  - Another JSON Object {}

More details here - https://www.json.org/json-en.html

## Sample

### JSON Example

```
{
	"id": 1,
	"name": "vicky",
	"single": false,
	"companies": ["TCS", "CTS"],
	"address": {
		"street": "Vinayak Street",
		"area": "thiruvarur",
		"state": "Tamilnadu",
		"pincode": 610001
	},
	"bankdetails": [{
		"ifscode": "HDFC0009077",
		"accNumber": 512893618263912,
		"branch": "Chennai branch"
	}, {
		"ifscode": "SBI0079343",
		"accNumber": 6381289360129,
		"branch": "Tiruvarur branch"
	}]
}
```

### Equivalent Java object

```
class Person {
    Integer id;
    String name;
    Boolean single;
    List<String> companies;
    Address address;
    List<BankDetails> bankdetails;
}

class Address {
    String street;
    String area;
    String state;
    Integer pincode;
}

class BankDetails {
    String ifscode;
    Long accNumber;
    String branch;
}
```
