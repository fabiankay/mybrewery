---
toc: true
layout: post
description: Development process
categories: [process]
title: Development process
---
# Development process
Since the development team size for the project proposed is currently between 1 and 2 developers, a lightweight development process is proposed. 

## Agile development
For the first itereation, a set of requirements to create an easy to use recipe manager is selected. In daily update meetings (acc. to SCRUM principles), the 2 developer update each other on their respectiv progress and issues. For critical parts of the software pair programming sessions are planned.
Moreover, to ensure smooth operations and the capability to extend the developer team, a continous development pipeline is developed. The project uses the [Github plattform and Github Actions and pipelines](https://docs.github.com/en/actions/automating-builds-and-tests/building-and-testing-python) to automate testing and later on deployment. When coding standards are established, it should also be feasible to open source the project. For branching [Gitflow](https://www.atlassian.com/git/tutorials/comparing-workflows/gitflow-workflow#:~:text=Gitflow%20is%20a%20legacy%20Git,software%20development%20and%20DevOps%20practices.) should be used. This way it should be easy to track feature progress and release cycles.

## Test-driven
For the development of the main brewing application, a test-driven agile approach is proposed. The core features of the minimal viable product (MVP) are covered with several different unit tests. As proposed for test-driven development, the tests are developed in advance and production code is only written to pass the tests. For the tests, unit tests to test single units of the software, like for example core functions, and integration tests to aggregate the functionality of several different parts of the software are written. For example it makes sense to test the time calculation fonction for each brewing step (unit test) and the creation of a whole recipe where different classes anf components of the software interact (integration test).

The following example shows a unit test for the time calulations of a brewing step

```python
class BrewingStep:
    time = 0

    def set_time(self, time):
        self.time = time
        return self.time

    def get_time(self):
        return self.time
    
    def add_time(self, time):
        self.time += time
        return self.time


if __name__ == '__main__':
    step = BrewingStep()
```

```python
import BrewingStep as BrewingStep


class Test(unittest.TestCase):
    """
    The basic class that inherits unittest.TestCase
    """
    step = BrewingStep.BrewingStep()
    time = 0

    # test case function to check the BrewingStep.set_time function
    def test_0_set_time(self):
        print("Start set_time test\n")
        self.time = self.step.set_time(10)
        self.assertEqual(self.time, 10)
        self.time = self.step.add_time(10)
        self.assertEqual(self.time, 20)
        print("\nFinish set_time test\n")

    # test case function to check the BrewingStep.get_time function
    def test_1_get_time(self):
        print("\nStart get_time test\n")
        self.assertEqual(self.step.get_time, self.time)
        print("\nFinish get_time test\n")


if __name__ == '__main__':
    # begin the unittest.main()
    unittest.main()
```