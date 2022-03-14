# NYCU-Software-Testing-2022-Lab_3
![workflow](https://github.com/irisowo/ST-2022-0616086/actions/workflows/main.yml/badge.svg)

## Pass
* ![Screenshot-Pass](./img/Pass.png)
* ![Screenshot-PassInfo](./img/PassInfo.png)

## Fail
* ![Screenshot-Fail](./img/Fail.png)
* ![Screenshot-FailInfo](./img/FailInfo.png)

## Spec
* Test java.util.PriorityQueue class with Junit.
    * import java.util.PriorityQueue;
* Parameterization
    * Testcase : { random array } , { correct array }.
    * Random array specifies your own input array.
    * Correct array means the PriorityQueue polling correct order instead of using toArray().
    * There are 5 unique testcases.
* Exception
    * There are 3 unique Exceptions thrown by PriorityQueue.
        1. IllegalArgumentException
            * whenExceptionThrown_thenInitialCapacityNotGreaterThanOne()
        2. NullPointerException
            * whenExceptionThrown_thenOfferEisNull()
        3. ClassCastException
            * whenExceptionThrown_thenCastWrongType()
            * Success case : 
                * ```
                   Exception exception = assertThrows(ClassCastException.class, () -> {
                    PriorityQueue pq = new PriorityQueue();
                    pq.add(0);
                    pq.add('0');
                    });             
                    ```
            * Failure case : 
                * ```
                   Exception exception = assertThrows(ClassCastException.class, () -> {
                    PriorityQueue pq = new PriorityQueue();
                    pq.add(0);
                    pq.add(0);
                    });             
                    ```