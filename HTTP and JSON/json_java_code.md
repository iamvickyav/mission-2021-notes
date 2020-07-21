# Working with JSON in Java Code

Can use libraries like GSON or Jackson

## To use GSON in your project

https://mvnrepository.com/artifact/com.google.code.gson/gson

Include dependency under dependencies tag in **pom.xml**

```xml
<dependencies>
    <dependency>
        <groupId>com.google.code.gson</groupId>
        <artifactId>gson</artifactId>
        <version>2.8.6</version>
    </dependency>
</dependencies>
```

## Convert JSON to Java Object

- First create Java object mapping your JSON

E.g. https://restcountries.eu/rest/v2/alpha/IN

```json
{
  "name": "India",
  "topLevelDomain": [".in"],
  "alpha2Code": "IN",
  "alpha3Code": "IND",
  "callingCodes": ["91"],
  "capital": "New Delhi",
  "altSpellings": ["IN", "Bhārat", "Republic of India", "Bharat Ganrajya"],
  "region": "Asia",
  "subregion": "Southern Asia",
  "population": 1295210000,
  "latlng": [20, 77],
  "demonym": "Indian",
  "area": 3287590,
  "gini": 33.4,
  "timezones": ["UTC+05:30"],
  "borders": ["AFG", "BGD", "BTN", "MMR", "CHN", "NPL", "PAK", "LKA"],
  "nativeName": "भारत",
  "numericCode": "356",
  "currencies": [
    {
      "code": "INR",
      "name": "Indian rupee",
      "symbol": "₹"
    }
  ],
  "languages": [
    {
      "iso639_1": "hi",
      "iso639_2": "hin",
      "name": "Hindi",
      "nativeName": "हिन्दी"
    },
    {
      "iso639_1": "en",
      "iso639_2": "eng",
      "name": "English",
      "nativeName": "English"
    }
  ],
  "translations": {
    "de": "Indien",
    "es": "India",
    "fr": "Inde",
    "ja": "インド",
    "it": "India",
    "br": "Índia",
    "pt": "Índia",
    "nl": "India",
    "hr": "Indija",
    "fa": "هند"
  },
  "flag": "https://restcountries.eu/data/ind.svg",
  "regionalBlocs": [
    {
      "acronym": "SAARC",
      "name": "South Asian Association for Regional Cooperation",
      "otherAcronyms": [],
      "otherNames": []
    }
  ],
  "cioc": "IND"
}
```

## Java Class

```java
class Country {
    String name;
    List<String> topLevelDomain;
    String alpha2Code;
    String alpha3Code;
    List<String> callingCodes;
    String capital;
    List<Currency> currencies;
}

class Currency {
    String code;
    String name;
    String symbol;
}

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

## Make HTTP Call

```java
public String findCountry(String countryCode) throws IOException {

        // Getting ready to make HTTP Call
        String url = "https://restcountries.eu/rest/v2/alpha/"+ countryCode;

        CloseableHttpClient httpclient = HttpClients.createDefault();
        HttpGet httpget = new HttpGet(url);

        // Making HTTP Call
        HttpResponse httpresponse = httpclient.execute(httpget);

        // Convert HTTP Response to String
        HttpEntity httpEntity = httpresponse.getEntity();
        String jsonResponse = EntityUtils.toString(httpEntity);

        // Convert String to Java Object using JSON
        Gson gson = new Gson();
        Country country = gson.fromJson(jsonResponse, Country.class);

        return country.name;
}
```
