# tiberius
It's Not Spock. Really. But close.

# example test

```groovy
class SomeClassSpecification extends Specification {

    def "should calculate some values"(){
        
        given:
        def calculator = new Calculator()

        when:
        def calculation = calculator.compute(case.input)

        then:
        calculation == case.calculation
        
        where:
        case = [
          [input: '2+2', calculation: 4],
          [input: '8*8', calculation: 64]
        ]
    }
    
}
```

# example test 2

```groovy
class SomeClassSpecification extends Specification {

    def "should calculate some values"(){
        
        given:
        def calculator = new Calculator()

        when:
        def calculation = calculator.compute('abc + 2')

        then:
        exception thrown
    }
    
}
```


#It looks like Spock!

Yeah, without **mocks**, **stubs**.
