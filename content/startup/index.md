---
date: 2020-04-23T14:29:50+01:00
title: The Startup Factory
weight: 2
---

## Once the idea is clear
There are many ways for a team to refine an idea. From 256 page documents covering every possible scenario to a single words on a postit note. I choose not to talk about these and instead discuss how software can be created once the idea is clear.

The first step is to understand your idea well enough to explain it to another person. That other person should have the skills to cover your idea into machine instructions (aka code). Once this code is converted into machine language (aka compiled), the output is your idea realised as a software product.

Simple, right? This is the software factory at work. The raw material as input is your idea, the inner machine of the factory that coverts your idea into code is the software engineer and the output product is software artifact.

Then, give that archifact to the machine responsible for your product (aka deploy to production). And, that is it, your customers can now consume the output from the software factory.

This description is singular and complete for all software factorys. Startup, SME, Large Business and Enterprise. These factorys do nothing else. The thing that separates them is their size. i.e. the number of people working inside the factory. The increase in people leads to an increase in complexity. This book is an attempt to discuss that increase in complexity.



## The life of your idea
Lets discuss timeline for the above process. Idea in, software out.

### Principle 1
You idea is not perfect

This is a fundamental truth. No person is capable of the perfect idea. While this sounds philosocial, it is quite obvious. The counter point would be, your idea is perfect. Meaning that you can describe you idea with such clarity, you have achieved a level of communication that really should be applied achieve world peace. The software engineer, in turn, converted that perfect description into flawless code. That flawless code was into deployed onto perfectly scalable hardware for you customers to consume... You get the point, your idea is not perfect.

As such, it is valuable to be able to iterate on your idea as fast as possible. To achieve the shortest throughput in your factory, you really want to minimise the number of time you need to hand off a task to another person.

So now, lets take you idea and start to build the team. Let's expand it to two people. An indiviudal that focuses on the idea, and an individual the converts that idea into code. Because your idea is not perfect, you need a measure of how close to perfect you are. For this arguement point, I make the assumption the how close to perfect you are is measure only by the satisfaction of your customers.

If you customers are perfectly content, you have done a good job. If your customers would like more features, you have work to do.

With this assumption, the question needs to be, "how can you get your idea converted into code and deployed to production as fast as possible". The answer, get the software engineer to deploy the completed idea into production. Once in production, measure you customers satisfaction. You will see there are things to change about your idea. Give those ideas for changes to the software engineer, make the changes as quickly as possible and again deploy to production.

Now, how can you be sure the original code still works as expected after you make this change. Remember, we are not perfect. To know our product still works as expected, we run tests against the product. That is, we act like a customer. We interact with our product, and expect to get an result. Being systematic about this process means we has a list of interactions we run through whenever we like and we expect to get the same result every time.

These tests can be written on a postit, in a word documents or in email. However as the input on the test and output from the test are predictable, keeping in mind that we want to run through our loop as fast as possible, we should write these tests as code and have a machine to execute the test suite.

Now that we have a good cycle to produce a product for customers. And the ability to change the product quickly. We have everything we need.

## Complex tests
It is not also possible to translate the test case into code. For example, as the user interface grows in complexity, the number of execution paths possible explodes in number. Writing test cases covering all these paths is high unlikely and as such we solve the problem with exploritory testing. Canary testing. Blue green deploys, etc.

Rince, repeat. Simple.

- Security
- Privacy
- 

## Scaling

As you idea gain customers, you will quickly find out that you need more people to implement the many features you need to add.

Lets add another teams to the mix. With two teams the complexity of our product is growing. But Principle 1 is constant. Our idea is not perfect. As such we need to continue our cycle as fast as possible.

In this setup, our high context environment of one teams being to change. We are now moving low in context. We will soon see that this change has a big impact on how we build out factory.

Lets assume the ideal setup. Both teams are working to contribute new features to the product and neither team is contributing changes that impact the other team. In this scenario, the value of the product to our customers is measure by the quality of the idea and the quality of the product.

With two teams, we now have diversity of ideas and opinions. This is great, but with diversity, we also need clarity in expectations.

## Teams
It is sad that our best setup is to have empowering, trusted teams. Automonous teams that can do the work they need to do without needed approval from a central authority. Let's examine this claim.

Starting again with our central premise, the primary function of the Software Factory is to complete the cycle as fast as possible and to run the cycle for as long as possible.

As the purpose of the cycle is to convert an idea and into code that is used by consumers, it makes sense that, in the absence of any other information, a team with complete automony (i.e. a team with complete control to make changes in product) and make those change whenever they want will result in the fastest loop.

However, thinking about the problem in this way ignores the complexity of real life. Security, alignment, quality, feedback and long term planning will each contribute to a messy product if they are ignored.

### Security
We have defined quality as a stable, robust and secure product. When we measure the product on these demisions we get a product that can be consider of high quality.

So our cycle must include security. Digging deeper, security means, 
1. It means, the code should not allow unauthorized persons to hack our product
2. The have at least 2 people on a team that understand all of the product. Avoid key person exposure.

Taking item 1, is it reasonable to conclude that our teams can release a product that meets this requirement?
Simple answer, no, it is not. This is not a state that can exist. For software, it is not possible to state that your product has no security issues. While I could not have research to prove this point, I think it is entirely possible that that problem of knowing with 100% certainly is an intractable problem.

Without proof of anything else, this is a safe position to start considering how we move as close to 1 as possible.

Due to this intractable problem, we then need to work on a scale of risk. We can never be risk free but we can say, we have less risk by adopted approach A rather than approach B.

So that challenge now is, "What do we need to be to lower our risk profile?"

Lets come back to automonous teams and ask some questions:-
- would the risk profile of the product but reduced if we ask the team to audit itself or ask an external team to audit the product?
- can the product be changed and deployed to production without a full security audit?

I am not going to answer all of these questions, but I am to build the first prinicples to guide your thinking.

Lets consider the audit question. And again, consider asking, can the audit ever give you a 100% guarntee that your code contains on security issues? If the answer is NO, then how far along the scale of certainty are you after the audit?

Thinking like this is thinking in probabilies. Without any way to give a clear probability that accounts for all the input elements, means you need to take a different approach.

### Skin in the game
You want to avoid at all costs, a rubber stamp approval. This will cause both the team build the product and the auditor to ignore security completely.

Be aware of the person the tells you "this will be good for you", when it is also good for them. But when something bad results, it is not also bad for them.

Any audit of your product needed to be done by those that will both gain from the reduction in risk profile but also lose something due to an increase in the risk profile. Note that the longer the connection permisits the better the reasoning.

To really control the risk, all persons need to be held to account so that leaving a project or being promoted, does not release us of our accountabilities to the security we implement.

The question is, how can this be done without distroying the progress of the company.

Well, lets control for some things first. People can leave your company and there is not (at least not yet), cross company penalities for those working on software. So lets not try to account for this.

It is possible to do this within the company however, what do you attach accountability to? Should the accountability be to the implemented code?

I do not consider the code producted to be something to attach accountability to as this would require the measureable probability to be available, and as we have stated, it is not.

Instead, the accountability should be to adherance to a best practice. This adherance needs to be binary in nature. Lets take an example,

It is required that, all software is committed the DVCS before it is put into products
- Lets examine why this is good. Doing this means, there is nothing on your personal laptop that is needed to run the application in production. This means that if you are hit by a bus on the way home, the product doesn't die with you. And so, the needle on our risk meter is moved slightly towards the safer side of the scale.

That is an easy one, so lets that a more difficult example. How can we reduce the probability of a remote code execution bug and as a result product a more secure product?
- All environments must remove the ProcessBuilder from that JVM. As the majority of projects do not use the process builder, removing this will achieve this outcome.

## Central Premise
Your idea is not perfect

- As your idea is not perfect, it best way to improve it is to convert your idea into a product as quickly as possible and have customers tell you where it can be improved

That's it. Nothing more. All the content of this book follows from this premise.

I 
