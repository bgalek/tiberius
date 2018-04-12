# tiberius
It's Not Spock. Really. But close.

# example test

```groovy

@BeforeTest // JUnit
somethingBeforeTest(){
}

@Unroll
class SomeClassSpecification extends Specification {

    def "should calculate value for input #case.input"(){
        
        given: 'calculator instance'
        def calculator = new Calculator()

        when: 'calculating'
        def calculation = calculator.compute(case.input)

        and: 'recording stats'
        calculation.recordStats()

        then: 'calculate'
        calculation == case.calculation
        
        where:
        case = [
          [input: '2+2', calculation: 4],
          [input: '8*8', calculation: 64]
        ]
    }
    
}

@AfterTest // JUnit
somethingAfterTest(){
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
