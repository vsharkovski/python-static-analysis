# Static Analysis Demo for Python

In this repo, we will explore two static analysis tools for python: [https://mypy-lang.org](https://mypy-lang.org) and [https://pypi.org/project/pyflakes/](https://pypi.org/project/pyflakes/)


## mypy demo

1. Run `mypy mypy_demo.py`. You should see that there is no error
2. Change lines 19 - 21 to the following

    ```
    print(add(3, "five"))  # This will raise an error
    print(greet(123))  # This will raise an error
    print(divide(10, "two"))  # This will raise an error
    ```

3. Re-run the mypy check from step 1

See the errors that came out. Note how all the errors were detected at once, vs. when you run the program and it stops after the first error? This is because these checks are done statically without running the code. 

Note that mypy relies on the type hints. It will not catch type violations if the type hints are not there.

## pylint demo

1. Run `pylint pylint_demo.py` You should see multiple errors and a rating for your code
2. Try fixing one of these errors and re-running to see how they would get fixed

## CI demo

- Make any small change and commit and push to trigger the CI build in your forked repo. You should see the build failing
- Fix the code for the build to pass and take a screenshot of your passed build and upload to brightspace. Hint: you can already run the tools locally to know if the tools will pass. Do that and push once ready to avoid wasting time for the CI build to finish.

