
# mypy demo

1. Run `mypy mypy-demo.py`. You should see that there is no error
2. Change lines 19 - 21 to the following

    ```
    print(add(3, "five"))  # This will raise an error
    print(greet(123))  # This will raise an error
    print(divide(10, "two"))  # This will raise an error
    ```

3. Re-run the mypy check from step 1

See the errors that came out. Note how all the errors were detected at once, vs. when you run the program and it stops after the first error? This is because these checks are done statically without running the code. 

Note that mypy relies on the type hints. It will not catch type violations if the type hints are not there.