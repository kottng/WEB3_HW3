# Отчет по домашнему заданию 3 
Выполнил: Котков Дмитрий Павлович БПИ213
Целью работы было использовать знания об оптимизации потребления газа в контрактах на языке solidity. В рамках выполнения работы были написаны 9 оптимизаций, результаты работы которых можно увидеть ниже:

## ArithmeticOperators

```
No files changed, compilation skipped

Ran 4 tests for test/01. ArithmeticOperators.t.sol:ArithmeticOperatorsOptimizedTest
[PASS] test_Addition_Optimized() (gas: 31631)
[PASS] test_DivisionBy128_Optimized() (gas: 5458)
[PASS] test_DivisionBy2_Optimized() (gas: 5448)
[PASS] test_Subtraction_Optimized() (gas: 31550)
Suite result: ok. 4 passed; 0 failed; 0 skipped; finished in 4.46ms (1.16ms CPU time)

Ran 4 tests for test/01. ArithmeticOperators.t.sol:ArithmeticOperatorsTest
[PASS] test_Addition() (gas: 31671)
[PASS] test_DivisionBy128() (gas: 5521)
[PASS] test_DivisionBy2() (gas: 5553)
[PASS] test_Subtraction() (gas: 31651)
Suite result: ok. 4 passed; 0 failed; 0 skipped; finished in 4.57ms (1.28ms CPU time)
| src/01. ArithmeticOperators.sol:Addition contract |                 |       |        |       |         |
|---------------------------------------------------|-----------------|-------|--------|-------|---------|
| Deployment Cost                                   | Deployment Size |       |        |       |         |
| 117342                                            | 223             |       |        |       |         |
| Function Name                                     | min             | avg   | median | max   | # calls |
| addition                                          | 26501           | 26501 | 26501  | 26501 | 1       |


| src/01. ArithmeticOperators.sol:AdditionOptimized contract |                 |       |        |       |         |
|------------------------------------------------------------|-----------------|-------|--------|-------|---------|
| Deployment Cost                                            | Deployment Size |       |        |       |         |
| 106096                                                     | 171             |       |        |       |         |
| Function Name                                              | min             | avg   | median | max   | # calls |
| addition                                                   | 26406           | 26406 | 26406  | 26406 | 1       |


| src/01. ArithmeticOperators.sol:Division contract |                 |     |        |     |         |
|---------------------------------------------------|-----------------|-----|--------|-----|---------|
| Deployment Cost                                   | Deployment Size |     |        |     |         |
| 103623                                            | 259             |     |        |     |         |
| Function Name                                     | min             | avg | median | max | # calls |
| divisionBy128                                     | 313             | 313 | 313    | 313 | 1       |
| divisionBy2                                       | 335             | 335 | 335    | 335 | 1       |


| src/01. ArithmeticOperators.sol:DivisionOptimized contract |                 |     |        |     |         |
|------------------------------------------------------------|-----------------|-----|--------|-----|---------|
| Deployment Cost                                            | Deployment Size |     |        |     |         |
| 92359                                                      | 206             |     |        |     |         |
| Function Name                                              | min             | avg | median | max | # calls |
| divisionBy128                                              | 239             | 239 | 239    | 239 | 1       |
| divisionBy2                                                | 261             | 261 | 261    | 261 | 1       |


| src/01. ArithmeticOperators.sol:Subtraction contract |                 |       |        |       |         |
|------------------------------------------------------|-----------------|-------|--------|-------|---------|
| Deployment Cost                                      | Deployment Size |       |        |       |         |
| 117330                                               | 223             |       |        |       |         |
| Function Name                                        | min             | avg   | median | max   | # calls |
| subtraction                                          | 26501           | 26501 | 26501  | 26501 | 1       |


| src/01. ArithmeticOperators.sol:SubtractionOptimized contract |                 |       |        |       |         |
|---------------------------------------------------------------|-----------------|-------|--------|-------|---------|
| Deployment Cost                                               | Deployment Size |       |        |       |         |
| 106312                                                        | 172             |       |        |       |         |
| Function Name                                                 | min             | avg   | median | max   | # calls |
| subtraction                                                   | 26409           | 26409 | 26409  | 26409 | 1       |




Ran 2 test suites in 7.44ms (9.03ms CPU time): 8 tests passed, 0 failed, 0 skipped (8 total tests)
```

## ArrayLength

```
No files changed, compilation skipped

Ran 1 test for test/02. ArrayLength.t.sol:ArrayLengthsTest
[PASS] test_Call() (gas: 8953)
Suite result: ok. 1 passed; 0 failed; 0 skipped; finished in 1.85ms (114.94µs CPU time)

Ran 1 test for test/02. ArrayLength.t.sol:ArrayLengthOptimizedTest
[PASS] test_Call() (gas: 5374)
Suite result: ok. 1 passed; 0 failed; 0 skipped; finished in 1.85ms (114.78µs CPU time)
| src/02. ArrayLength.sol:ArrayLength contract |                 |      |        |      |         |
|----------------------------------------------|-----------------|------|--------|------|---------|
| Deployment Cost                              | Deployment Size |      |        |      |         |
| 359435                                       | 467             |      |        |      |         |
| Function Name                                | min             | avg  | median | max  | # calls |
| callFor                                      | 3676            | 3676 | 3676   | 3676 | 1       |


| src/02. ArrayLength.sol:ArrayLengthOptimized contract |                 |     |        |     |         |
|-------------------------------------------------------|-----------------|-----|--------|-----|---------|
| Deployment Cost                                       | Deployment Size |     |        |     |         |
| 341898                                                | 385             |     |        |     |         |
| Function Name                                         | min             | avg | median | max | # calls |
| callFor                                               | 97              | 97  | 97     | 97  | 1       |




Ran 2 test suites in 4.58ms (3.70ms CPU time): 2 tests passed, 0 failed, 0 skipped (2 total tests)
```

## ArrayType

```
No files changed, compilation skipped

Ran 1 test for test/08. ArrayType.t.sol:ArrayTypeOptimizedTest
[PASS] test_init() (gas: 4441951)
Suite result: ok. 1 passed; 0 failed; 0 skipped; finished in 2.62ms (1.20ms CPU time)

Ran 1 test for test/08. ArrayType.t.sol:ArrayTypeTest
[PASS] test_init() (gas: 4504651)
Suite result: ok. 1 passed; 0 failed; 0 skipped; finished in 2.65ms (1.24ms CPU time)
| src/08. ArrayType.sol:ArrayType contract |                 |         |         |         |         |
|------------------------------------------|-----------------|---------|---------|---------|---------|
| Deployment Cost                          | Deployment Size |         |         |         |         |
| 90631                                    | 198             |         |         |         |         |
| Function Name                            | min             | avg     | median  | max     | # calls |
| initArray                                | 4499416         | 4499416 | 4499416 | 4499416 | 1       |


| src/08. ArrayType.sol:ArrayTypeOptimized contract |                 |         |         |         |         |
|---------------------------------------------------|-----------------|---------|---------|---------|---------|
| Deployment Cost                                   | Deployment Size |         |         |         |         |
| 88469                                             | 188             |         |         |         |         |
| Function Name                                     | min             | avg     | median  | max     | # calls |
| initArray                                         | 4436716         | 4436716 | 4436716 | 4436716 | 1       |




Ran 2 test suites in 4.30ms (5.27ms CPU time): 2 tests passed, 0 failed, 0 skipped (2 total tests)
```

## CalldataMemory

```
No files changed, compilation skipped

Ran 1 test for test/03. CalldataMemory.t.sol:CalldataMemoryTest
[PASS] test_Call() (gas: 32491)
Suite result: ok. 1 passed; 0 failed; 0 skipped; finished in 1.12ms (92.40µs CPU time)

Ran 1 test for test/03. CalldataMemory.t.sol:CalldataMemoryOptimizedTest
[PASS] test_Call() (gas: 30916)
Suite result: ok. 1 passed; 0 failed; 0 skipped; finished in 1.34ms (48.00µs CPU time)
| src/03. CalldataMemory.sol:CalldataMemory contract |                 |      |        |      |         |
|----------------------------------------------------|-----------------|------|--------|------|---------|
| Deployment Cost                                    | Deployment Size |      |        |      |         |
| 157257                                             | 509             |      |        |      |         |
| Function Name                                      | min             | avg  | median | max  | # calls |
| add                                                | 3183            | 3183 | 3183   | 3183 | 1       |


| src/03. CalldataMemory.sol:CalldataMemoryOptimized contract |                 |      |        |      |         |
|-------------------------------------------------------------|-----------------|------|--------|------|---------|
| Deployment Cost                                             | Deployment Size |      |        |      |         |
| 124411                                                      | 357             |      |        |      |         |
| Function Name                                               | min             | avg  | median | max  | # calls |
| add                                                         | 1608            | 1608 | 1608   | 1608 | 1       |




Ran 2 test suites in 3.46ms (2.45ms CPU time): 2 tests passed, 0 failed, 0 skipped (2 total tests)
```

## Errors

```
No files changed, compilation skipped

Ran 1 test for test/06. Errors.t.sol:ErrorsTest
[PASS] test_call() (gas: 11127)
Suite result: ok. 1 passed; 0 failed; 0 skipped; finished in 2.03ms (786.13µs CPU time)

Ran 1 test for test/06. Errors.t.sol:ErrorsOptimizedTest
[PASS] test_call() (gas: 8974)
Suite result: ok. 1 passed; 0 failed; 0 skipped; finished in 2.05ms (975.05µs CPU time)
| src/06. Errors.sol:Errors contract |                 |      |        |      |         |
|------------------------------------|-----------------|------|--------|------|---------|
| Deployment Cost                    | Deployment Size |      |        |      |         |
| 118601                             | 241             |      |        |      |         |
| Function Name                      | min             | avg  | median | max  | # calls |
| call                               | 2355            | 2355 | 2355   | 2355 | 1       |


| src/06. Errors.sol:ErrorsOptimized contract |                 |     |        |     |         |
|---------------------------------------------|-----------------|-----|--------|-----|---------|
| Deployment Cost                             | Deployment Size |     |        |     |         |
| 91776                                       | 217             |     |        |     |         |
| Function Name                               | min             | avg | median | max | # calls |
| call                                        | 202             | 202 | 202    | 202 | 1       |




Ran 2 test suites in 4.00ms (4.08ms CPU time): 2 tests passed, 0 failed, 0 skipped (2 total tests)
```

## Loops

```
No files changed, compilation skipped

Ran 3 tests for test/04. Loops.t.sol:LoopsOptimizedTest
[PASS] test_doWhile() (gas: 5838)
[PASS] test_for() (gas: 6557)
[PASS] test_while() (gas: 5961)
Suite result: ok. 3 passed; 0 failed; 0 skipped; finished in 1.84ms (309.65µs CPU time)

Ran 3 tests for test/04. Loops.t.sol:LoopsTest
[PASS] test_doWhile() (gas: 7188)
[PASS] test_for() (gas: 7917)
[PASS] test_while() (gas: 7311)
Suite result: ok. 3 passed; 0 failed; 0 skipped; finished in 1.90ms (212.52µs CPU time)
| src/04. Loops.sol:Loops contract |                 |      |        |      |         |
|----------------------------------|-----------------|------|--------|------|---------|
| Deployment Cost                  | Deployment Size |      |        |      |         |
| 118763                           | 330             |      |        |      |         |
| Function Name                    | min             | avg  | median | max  | # calls |
| loopDoWhile                      | 1933            | 1933 | 1933   | 1933 | 1       |
| loopFor                          | 2639            | 2639 | 2639   | 2639 | 1       |
| loopWhile                        | 2056            | 2056 | 2056   | 2056 | 1       |


| src/04. Loops.sol:LoopsOptimized contract |                 |      |        |      |         |
|-------------------------------------------|-----------------|------|--------|------|---------|
| Deployment Cost                           | Deployment Size |      |        |      |         |
| 97767                                     | 231             |      |        |      |         |
| Function Name                             | min             | avg  | median | max  | # calls |
| loopDoWhile                               | 583             | 583  | 583    | 583  | 1       |
| loopFor                                   | 1279            | 1279 | 1279   | 1279 | 1       |
| loopWhile                                 | 706             | 706  | 706    | 706  | 1       |




Ran 2 test suites in 3.50ms (3.74ms CPU time): 6 tests passed, 0 failed, 0 skipped (6 total tests)
```

## NestedIf

```
No files changed, compilation skipped

Ran 1 test for test/09. NestedIf.t.sol:NestedIfOptimizedTest
[PASS] test_call() (gas: 8046)
Suite result: ok. 1 passed; 0 failed; 0 skipped; finished in 16.12ms (2.92ms CPU time)

Ran 1 test for test/09. NestedIf.t.sol:NestedIfTest
[PASS] test_call() (gas: 8135)
Suite result: ok. 1 passed; 0 failed; 0 skipped; finished in 16.11ms (2.92ms CPU time)
| src/09. NestedIf.sol:NestedIf contract |                 |     |        |     |         |
|----------------------------------------|-----------------|-----|--------|-----|---------|
| Deployment Cost                        | Deployment Size |     |        |     |         |
| 96483                                  | 225             |     |        |     |         |
| Function Name                          | min             | avg | median | max | # calls |
| call                                   | 341             | 349 | 352    | 352 | 4       |


| src/09. NestedIf.sol:NestedIfOptimized contract |                 |     |        |     |         |
|-------------------------------------------------|-----------------|-----|--------|-----|---------|
| Deployment Cost                                 | Deployment Size |     |        |     |         |
| 93667                                           | 212             |     |        |     |         |
| Function Name                                   | min             | avg | median | max | # calls |
| call                                            | 309             | 327 | 333    | 333 | 4       |




Ran 2 test suites in 26.66ms (32.23ms CPU time): 2 tests passed, 0 failed, 0 skipped (2 total tests)
```

## PackVariables

```
No files changed, compilation skipped

Ran 1 test for test/05. PackVariables.t.sol:PackVariablesTest
[PASS] test_set() (gas: 159348)
Suite result: ok. 1 passed; 0 failed; 0 skipped; finished in 1.68ms (613.65µs CPU time)

Ran 1 test for test/05. PackVariables.t.sol:PackVariablesOptimizedTest
[PASS] test_set() (gas: 137473)
Suite result: ok. 1 passed; 0 failed; 0 skipped; finished in 2.16ms (870.84µs CPU time)
| src/05. PackVariables.sol:PackVariables contract |                 |        |        |        |         |
|--------------------------------------------------|-----------------|--------|--------|--------|---------|
| Deployment Cost                                  | Deployment Size |        |        |        |         |
| 175275                                           | 592             |        |        |        |         |
| Function Name                                    | min             | avg    | median | max    | # calls |
| setValues                                        | 150820          | 150820 | 150820 | 150820 | 1       |


| src/05. PackVariables.sol:PackVariablesOptimized contract |                 |        |        |        |         |
|-----------------------------------------------------------|-----------------|--------|--------|--------|---------|
| Deployment Cost                                           | Deployment Size |        |        |        |         |
| 178041                                                    | 605             |        |        |        |         |
| Function Name                                             | min             | avg    | median | max    | # calls |
| setValues                                                 | 128945          | 128945 | 128945 | 128945 | 1       |




Ran 2 test suites in 5.05ms (3.85ms CPU time): 2 tests passed, 0 failed, 0 skipped (2 total tests)
```

## Swap

```
No files changed, compilation skipped

Ran 1 test for test/07. Swap.t.sol:SwapOptimizedTest
[PASS] test_swap() (gas: 8789)
Suite result: ok. 1 passed; 0 failed; 0 skipped; finished in 3.05ms (1.61ms CPU time)

Ran 1 test for test/07. Swap.t.sol:SwapTest
[PASS] test_swap() (gas: 9053)
Suite result: ok. 1 passed; 0 failed; 0 skipped; finished in 3.05ms (1.61ms CPU time)
| src/07. Swap.sol:Swap contract |                 |     |        |     |         |
|--------------------------------|-----------------|-----|--------|-----|---------|
| Deployment Cost                | Deployment Size |     |        |     |         |
| 110343                         | 291             |     |        |     |         |
| Function Name                  | min             | avg | median | max | # calls |
| swap                           | 543             | 543 | 543    | 543 | 1       |


| src/07. Swap.sol:SwapOptimized contract |                 |     |        |     |         |
|-----------------------------------------|-----------------|-----|--------|-----|---------|
| Deployment Cost                         | Deployment Size |     |        |     |         |
| 89345                                   | 192             |     |        |     |         |
| Function Name                           | min             | avg | median | max | # calls |
| swap                                    | 279             | 279 | 279    | 279 | 1       |




Ran 2 test suites in 4.28ms (6.10ms CPU time): 2 tests passed, 0 failed, 0 skipped (2 total tests)
```

