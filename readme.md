# Best practices of OO and Object Calisthenics

## Documentation
  - [Assert](https://github.com/beberlei/assert)
  - [PHPUnit](https://phpunit.readthedocs.io/fr/latest/)
  - [Hamcrest](https://github.com/hamcrest/hamcrest-php)
  - [Mockery](http://docs.mockery.io/en/latest)
  - [Object Calisthenics](https://williamdurand.fr/2013/06/03/object-calisthenics)

## SOLID
  1. Single responsibility principle
  2. Open/closed principle
  3. Liskov substitution principle
  4. Interface segregation principle
  5. Dependency inversion principle

## 9 OC Rules
  1. Only One Level Of Indentation Per Method
  2. Don't Use The ELSE Keyword
  3. Wrap All Primitives And Strings
  4. First-Class Collections
  5. One Dot Per Line
  6. Don't Abbreviate
  7. Keep All Entities Small
  8. No Classes With More Than Two Instance Variables
  9. No Getters/Setters/Properties

## TDD
   1. Write the test
   2. Make it compile
   3. Watch it fail
   4. Make it pass
   5. Refactor
      a. SOLID
      b. 9 OC Rules
   6. Replay test

## Supermarket Pricing Problem
> The purpose is to implement the code for a supermarket checkout that calculates the total price of a number of items.

### Acceptance Criteria
  1. API accepts items in any order
  2. API accepts the same item several time
  3. API total method reflects the total amount of scaned items at any time.
  4. Pricing changes frequently.
  5. Special discount or others features could be requested later.

#### Checkout Calculation Sample
    Item  Price TTC
    ----  ---------
    A     50
    B     30
    C     20
    D     15

#### API (KISS)
    $co = new Checkout();
    $co->scan('A')->scan('B');
    $co->total(); // would return 80
    $co->scan('D');
    $co->total() // would return 95

## Text file encoding
- UTF-8

## Code style formatter
- PSR-2

## Structure
   - **src**: source code
   - **tests**: unit tests files
   - **vendor**: Dependencies classes
   - **composer.json**: Dependencies configuration
   - **phpunit.xml**: Phpunit configuration

## Install dependencies

### For development mode
Run `composer install`

## Launch test
Run `composer test`

## Launch code coverage
Run `composer cover`
