![Amazon Q Developer header](images/q-vscode-header.png)

## Next Generation Developer Tools

*A hands on guide to working with Amazon Q Developer. Made by DevRel with 💖.*

This is an addendum that has been added that takes a look at some of the additional ways that Amazon Q Developer can help when working with your applications and software projects.

We will explore the following topics

* Using Amazon Q Developer in the Analysis and Design Phases
* Explaining how application code works with Amazon Q Developer
* Documenting our projects using Amazon Q Developer

You will still need to complete the following steps from the README page - 1.1, 2.1, and 2.3 to 2.6

Once you have completed those steps, you can begin here.


## Using Amazon Q Developer in the Analysis and Design Phases**

**Lab 01-1 Analysis**

Developers can use generative AI tools to help them prepare for the analysis phase of development projects. It can help in a number of key areas, such as:

* Requirements gathering - Help determine functional and non functional requirements for my application
* Understanding the problem space - Help orientate me to the problem space – I may not be familiar with a specific use case or technology area, these tools can help bridge your knowledge gap here
* Narrow down what I need to think about

When we pick up a new development task, we first have to find the information we need. Generative AI can help us here, both generally and specifically.We can leverage generative AI tools together with approaches such as RAG (Retrieval Augmented Generation) to inject our companies tech docs, and help us find the information we need. This can be a real time saver.

Developers can use GenAI tools to better prepare for planning meetings, to ask the right questions. For example, they can use GenAI to understand functional and non functional requirements that they need to think about, or use these tools to explore different approaches and provide some initial ideas for the design stage – pros/cons


![Activity](images/task.png)  **Understanding the problem space**

In this hands on lab, we are looking to build an application that allows users to save shortcuts for internet URLs that might be difficult to remember or just too long. During the analysis phase, we might want help in understanding how to approach this. Here are some prompts you can try.

```
From an analysis perspective, what do I need to know about building a url shortening application
```

Experiment with different prompts, adding more detail.

```
What do i need to know about building a url shortener application. Provide some real examples that I can use and look into. If you can provide some existing applications that I can compare as well.
```

You can dive deeper by asking follow up questions:

```
Tell me more about analytics and tracking for this use case
Provide more details on xxx
```

Another useful way we can use Amazon Q Developer is to help us summarise or bring back just the top points that we should be thinking about.

```
What are the three most important things I need to think about when building an URL shortening application.
```

Try with our own questions too, and explore how you can get additional useful information that might help you build a better application.

Write down 3-4 key things you learned about this space. Experiment with an application that you are familiar with, and review the output. What did it get right and what could it improve? 

![Activity](images/task.png)  **Gathering requirements**

In our next activity we are going to use Amazon Q Developer to help us understand what our key requirements might be. Tools like Amazon Q Developer are excellent at answering "it depends" questions, but it is important to provide as much information as you can.

One area that we typically encounter this is when we are defining our functional and non functional questions.

```
What are the most important functional and non functional requirements I need to be thinking about when building an URL shortening application.
```

Review the output, and use the Chat interface to ask follow up questions for things you are not familiar with. For example

```
I am not familiar with xxx please explain in more detail in the context of the previous answer.
```

We can also start to incorporate some of our own constraints. For example, I might want to ask specifically what do I need to think about when deploying this application to AWS.

```
Is there anything I need to be thinking about when building and deploying a URL shortening application on AWS
```

Write down the top 3 functional and non functional requirements you have learned about building this application.

**Lab 01-2 Design**

During the design phase, you need to start thinking more concretely about what you are going to the architecture and how the solution is going to look.

During this stage, you are looking to:

* Narrow down technical choices
* Define architecture and frameworks
* Sizing and deployment options and approaches

Lets see how Amazon Q Developer can help us with this task.

![Activity](images/task.png)  **Defining architecture**

With so many different frameworks and libraries we can choose to build solutions, it would be great if we could get some help to make this simpler and help us to define our initial architecture.

```
What are the best frameworks to use when developing a url shortening solution.We have mostly Python developers. Can you provide me with three options.
```
Follow up and see if you can refine the output by using the information you got from your functional and non functional requirements.

![Activity](images/task.png)  **Narrowing down choices**

Now that we have some potential candidate architecture, we can use Amazon Q Developer to provide some ideas on how we might narrow down some of the choices we have given.

```
What are the different trade offs I need to think about between these different frameworks
```

I can try and get more specific information too.

```
If you had to pick one, which would you choose?
```

Alternatively, I might try the same thing but with my most important factors in mind.

```
If you had to pick one, which was best for simplicity, which would you choose?
```

Review your output. When I did this, it suggested that Flask would be the best framework for this. Do you agree?


We can also extend this to where we want to deploy our application. Lets ask Amazon Q Developer for some guidance.

```
If I want to deploy this Flask application to AWS, can you provide me three options, with a recommendation. I want to use something simple but flexible as I will need to integrate with other AWS services. I prefer to use container solutions within my business.
```

As you can see, the more detail we provide, the more specific and useful the information we will receive.

Write down your recommendations and compare it with other people in the workshop. What is the same and what is different?

![Activity](images/task.png)  **Sizing and deployment choices**

In this final section we can explore how once we have some recommendations, we can dive deeper to get some specific details around some of the functional and non functional design choices we need to think about.

We can ask Amazon Q Developer to help us with sizing and cost choices

```
I am looking for guidance on sizing and other general recommendations on compute, cost, resilience, and anything else you think is important
```

We can also ask for some specific details, for example, how to architecture for cost

```
How do I ensure that I reduce the cost of this solution
```

We can ask Amazon Q Developer to provide information about how to do disaster recovery. We can dive deeper into how to architect a solution which requires specific RTO and RPO (if these terms are unfamiliar, use Amazon Q Developer to help you understand what these mean.)

```
I need to architect this architecture with a disaster recovery solution. What do I need to think about?
```

Write down the key points of what you need to think about. Are these what you had in mind? Did it bring up anything you had missed? Maybe you had things that it missed, what were they?

## Explaining how application code works with Amazon Q Developer**

**Lab 02-1 Understanding our application**

![Activity](images/task.png)  **Getting our application code**

From the VSCode screen, make sure you select the terminal, and are in the project directory (ada-python-demo-app). Type in the following to set up the files needed for this lab.

```
git checkout tests
```

You should now have a bunch of files which you can explore in the VSCode server. You want to find and open the file "app.py" which should appear in the main VSCode screen.

![Activity](images/task.png)  **Explain how the application works**

From the Explorer icon on the left, find and open the "app.py" file. It should open up into the main part of VSCode.

There are a number of different ways we can ask Amazon Q Developer to help us understand what this application does.

*Via the Chat interface*

We can ask Amazon Q Developer directly in the Chat interface to explain our application. For example:

```
Can you explain how the app.py code works?
```

Review the output. Do you think you now understand how this works? If there are bits you do not understand, copy and then paste these into new chat queries. You can do this as many times as you want until you get to something you understand.

*Via the menu*

Highlight all the code in the main VSCode window (move the cursor, and press and hold CTRL and then press A). Now move the cursor anywhere over this highlighted code and RIGHT click. This should reveal a menu, one item being "Send to Amazon Q". Click on that. You will be presented with a number of options, select "Explain".

You should notice that in the Chat interface, the code is now displayed, and Amazon Q Developer will start to explain how this works, in a similar way to before.

Compare the output - are they different or similar?

![Activity](images/task.png)  **Explain how parts of the application work**

Perhaps you do not want to know how the whole application works, but perhaps one piece of it - maybe a function.

You can do this easily by highlighting the portion of your code, and then using the RIGHT click, "Send to Amazon Q" and Explain option like you did in the previous step. This time the output will be different.

## Documenting our projects using Amazon Q Developer**

**Lab 03-1 Adding Documentation**

One of the most effective applications of tools like Amazon Q Developer has been to help automate the task of documenting our projects. 

![Activity](images/task.png)  **Adding documentation to our project**

Working from our complete project, lets see how we can use Amazon Q Developer to complete the documentation for our application.

Lets ask via the Chat panel the following

```
Create a README that shows how this app works and how to test and run it
```

Review the output. What do you think, is it detailed enough? You can explore and experiment with this. If the documentation does not have enough detail, then ask a follow up prompt to provide more details.

![Activity](images/task.png)  **Documenting our code**

We can also document the code itself, providing docstrings to document each function within our application. Lets use the Chat panel:

```
Create docstrings that explain how each function in this application works
```
Review the output and make changes. We now have a working application that has documentation and tests. Not bad for such a short time.

---

## Open Sourcing projects using Amazon Q Developer**

**Lab 04-1 Open Sourcing our project**

The final lab will show how we can use tools like Amazon Q Developer to simplify tasks such as open sourcing our project. 

![Activity](images/task.png)  **Open sourcing the application**

Using the Amazon Q Developer Chat panel, we can ask it the following prompts:

```
> I want to open source this project, what do i need to do
> can you provide me with a sample MIT license file
> can you update it for my company, beachgeek.co.uk
> how do i add an SPDX header to this project?
```

Review the output for each of these prompts and then make changes. As these files and updates will not make any impact to the functionality, there is no need to test the application.

**Complete:** Congratulations, you have completed this hands on lab. If you have time, there are some additional ideas for activities for you to do. Otherwise, go and congratulate yourself with a well earned beverage of your choice!

