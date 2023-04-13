# Jakarta Validation Sample Project

Jakarta Validation is a popular validation framework used in Java applications. It provides a set of annotations that
can be used to validate Java objects and their properties. These annotations can be applied at the class, field, or
method level and can be used to enforce constraints on the values of these properties.

## Usage/Examples

To use Jakarta Validation in your Java application, you need to add the Jakarta Validation library to your project's
classpath. You can do this by adding the following dependency to your pom.xml file:

```javascript
    <dependency>
        <groupId>jakarta.validation</groupId>
            <artifactId>jakarta.validation-api</artifactId>
        <version>3.0.0</version>
    </dependency>
```

Once you have added the dependency, you can start using Jakarta Validation in your code. To validate a Java object, you
can use the Validator interface, which provides several methods for validating objects and their properties.

#### Hello

```http
  POST /hello
```

| Parameter | Type     | Description                |
| :-------- | :------- | :------------------------- |
| `firstName` | `string` | **Required**. First name |
| `lastName` | `string` | **Required**. Last name |
| `email` | `string` | **Required**. Email |
| `phoneNumber` | `string` | **Required**. Phone Number |
| `skills` | `Array` | **Required**. Skills |

```javascript
    @PostMapping("/hello")
    public ResponseEntity<Hello> sayHello(@Valid @RequestBody Hello hello){
        return new ResponseEntity<>(hello,HttpStatus.OK);
    }
```
## Screenshot

<img width="949" alt="Screenshot 2023-04-13 at 15 26 14" src="https://user-images.githubusercontent.com/66008860/231722268-5f951fd3-b623-4d18-bfb8-012682c1e0eb.png">

