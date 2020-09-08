# Danubius Test

## Short questions

- What is GIT? What is it used for and what kind of
situations is it designed to solve/make it easier?

`GIT is a version control system. It helps team members to work in parallel on the same code.`

- What is HTTP? What kind of HTTP methods are you
familiar with? What are their characteristics?

`HTTP means Hyper Text Trasfer Protocol. It's designed to standardizing the usual internet communication between the servers and the clients.`
`POST - it's usualy for creating data on the server, GET - it's used to request data from the server, UPDATE - for updating data on the server, DELETE - for deleting data from the server`

- What is the difference between HTTP and HTTPS?

`HTTPS is the secure type of the "normal" HTTP. The HTTPS encryptes the data in the communication.`

- What do you know about the following HTML tags?
What are their characteristics and when do we use them?
  - `<div>` `It's for creating a kind of container in the HTML file. It is useful if we want to give a specific style parameter for those things what're inside this tag.`
  - `<span>`
  - `<p>` `I think p means paragraph, it's for marking the base-size text in HTML.`
  - `<a href="...">...</a>` `This is how we mark the hyper text links in HTML file.`

- What do you know about dependency injection?
What is it used for? What is its advantage?

- Briefly describe a current topic in the IT field
that you are interested in!

## Programming task

Given a table that contains units and multipliers
that belongs to them. The multipliers tell you what
is the number that you need to multiply the value
with if you'd like to calculate the base unit.
The base units for example: liter, meter, etc...
Those that doesn't have a metric prefix.

### Length

| Unit | Value |
|------|-------|
| mm   | 0.001 |
| cm   | 0.01  |
| dm   | 0.1   |
| m    | 1     |
| km   | 1000  |

### Weight

| Unit | Value   |
|------|---------|
| mg   | 0.001   |
| g    | 1       |
| dkg  | 10      |
| kg   | 1000    |
| t    | 1000000 |

### Task

Create a data structure(could be a class but also
any type of combination of primitive types, array,
but also the series of well named variables) which
is suitable to store the values in the table and
makes the implementation of the exercises below easier(You don't have to
implement the actual operations they are just there
as an example).

- List a given type(e.g.: Length) of measurement units.
For example: mm, cm, dm, m, km
- Query of the multipliers.
For example: input -> km, output -> 1000
- Given an actual unit, return the value in the base unit.
For example: input -> "1200 cm", output -> 12

Initialize the datastructure with example inputs.

String[] unitsM = new String[]{ "mm", "cm", "dm", "m", "km" };
double[] valuesM = new double[]{ "0.001", "0.01", "0.1", "1", "1000" };

String[] unitsG = new String[]{ "mg", "g", "dkg", "kg", "t" };
double[] valuesG = new double[]{ "0.001", "1", "10", "1000", "1000000" };

public List<String> listAGivenType(){
List<String> types = new ArrayList();
for (int i = 0; i < unitsM.length(); i++) {
	types.add(unitsM.get(i));
}
return types; 
}

public double queryOfTheMultipliers(String mult){
double num = 0.0;
for (int i = 0; i < unitsM.length(); i++) {
	if (unitsM.get(i).compare(mult) == 0) {
		num = valuesM.get(i);
	}
}
for (int i = 0; i < unitsG.length(); i++) {
	if (unitsM.get(i).compare(mult) == 0) {
		num = valuesG.get(i);
	}
}
return num;
}

}

