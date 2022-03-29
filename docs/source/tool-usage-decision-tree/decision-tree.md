# Decision Tree

```{mermaid}
classDiagram
class `DARE.CAR.CAR` {
    string registrationNumver
    string make
    string model
}
class PERSON {
    string firstName
    string lastName
    int age
}
`DARE.CAR.CAR` -- PERSON : left join on\nregistrationNumber = firstName
```



## testing nesting 

### is this visible
