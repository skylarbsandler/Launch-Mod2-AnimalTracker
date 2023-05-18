# Mod2 Week2 Assessment - Skylar Sandler

## Setup
1. Fork this repository.
1. Add ONE of the following GitHub profiles as a collaborator to your forked repo:
`memcmahon`, `rtillies`, `zoefarrell`
1. Clone your repo to your local machine.
1. Open your cloned repository in Visual Studio.
1. Insert your name on line 1 to replace `<YOUR NAME HERE>` above.

## Questions (10 Points Possible)
**Important** Answer these questions in this file on your `main` branch.  When finished with the questions, commit and push your main branch.  You do not need to create a pull request yet!

1. What does TDD stand for?
Test Driven Development requires us to first write our tests before writing our code. The tests drive how we design our code.

1. What are three benefits of using TDD?
- Integrates writing tests into our coding process rather than it feels like an optional step tacked onto to the end of the coding process.
- Focuses us to think about how we want to structure and design our code early
- Breaks down problems into smaller problems by making decisions early
- Only write the code you need by focusing our code to pass our prewritten tests and confirm when we have successfully solved the problem at hand.

1. Imagine you are in an interview.  The interviewer asks: How do you use TDD? How would you answer?
Test Driven Development leads to testing being an integral step in our coding process. It forces the ocder to critically think about what code is necessary to solve the problem and make
decisions early about how we go about solving the problem. These tests can then serve as a roadmap when we proceed to writing our main code and help confirm we have successfully solved the
problem by passing our prewritten tests.

1. For the class below, outline the tests you would need.  Try to use as much C# syntax as possible. The first test has been provided for you. (this question is worth 4 points)
```c#
public class Dog
    {
        public string Name { get; }
        public string Breed { get; }
        public bool IsHungry { get; private set; }

        public Dog(string name, string breed)
        {
            Name = name;
            Breed = breed;
            IsHungry = true;
        }

        public void Eat()
        {
            IsHungry = false;
        }

        public void Sleep()
        {
            IsHungry = true;
        }

        public string Speak()
        {
            return "Bark Bark!";
        }
    }
```
```c#
// Add your tests here

[Fact]
public void DogHasNameAttribute()
{
    Dog dog = new Dog("Nile", "Golden Retriever");

    Assert.Equal("Nile", dog.Name);
}

[Fact]
public void Dod_Eat_CorrectlyChangesIsHungrytoFalse()
{
    Dog dog = new Dog("Nile", "Golden Retriever");
    dog.Eat();
    Assert.False(dog.IsHungry);

[Fact]
public void Dog_Sleep_CorrectlyChangesISHungrytoTrue()
{
    Dog dog = new Dog("Nile", "Golden Retriever");
    dog.Sleep();
    Assert.True(dog.IsHungry);
}

[Fact]
public void Dog_Speak_CorrectlyReturnsString()
{
    Dog dog = new Dog("Nile", "Golden Retriever");
    Assert.Equal("Bark Bark!", dog.Speak());
}
```

5. What is a merge conflict, and when might you encounter one?
A merge conflict occurs when you are trying to merge (or combine) different branches of the same prioject. The different branches have code on the same lines so Github or VS does not know
which version of the code to accept into the main file. When a merge conflict occurs, you need to manually decide and update the code to let GH/VS know what you want the main branch to look like.
This often happens when multiple developers are working on branches of the same project and updating the same files then try to combine their conflicting code.

6. You and a partner are working on a project together.  Your partner is working on aa-branch; you are working on bb-branch.  In as much detail as possible, describe how you both would get your work combined onto the main branch.
Both partners would need to:
- Committ and pish their respective branches to Github.
- Create seperate pull requests to merge their respective branches into the main branch.
- One, or both, partners are likely to receive a merge conflict if their added/updated code on the same lines in the same file. Those merge conflicts need to be resolved.
- Each partner would then review and comment their partner's PR to approve and complete the merges into the main branch.

7. Why is it good practice to have someone else approve and/or merge your PR?  
  
**Before moving on to the next section, commit your work and push your main branch!**
  
## Git Exercise (6 points possible)

1. Create a new branch called `elephants` (1 point)

1. Add the following to the end of the Animal Tracker file:

```
Elephants
- African Savanna
- Asian
- African Forest
```

3. Commit this change to the Animal Tracker file with an appropriate message. (1 point)

1. Create the following files with the listed contents:

**African Savanna.txt**
```
Average shoulder height: 2.6-3.2 meters
Average mass: 3.3-6.6 short tons
```

**Asian Elephant.txt**
```
Average shoulder height: 2.4-2.8 meters
Average mass: 3.0-4.4 short tons
```

**African Forest Elephant.txt**
```
Average shoulder height: 1.8-3.0 meters
Average mass: 2,000-7,000 kilograms
```

5. Add and Commit these new files with an appropriate message. (1 point)

1. Push your `elephants` branch to GitHub. (1 point)

1. Create a Pull Request in GitHub. Write a short description of the changes you made to the repo. (1 point) 

1. Request a review from your collaborator. (1 point)
  
## Submission

Submit the Assessment Submission form linked in your cohort slack channel!

## Rubric

This assessment has a total of 16 Points. Earning 11 or more points is a pass and will indicate that you are progressing well with the material.

As a reminder, this assessment is for students and instructors to determine if there are any areas that need additional reinforcement!
