# Centralized workflow

As mentioned in the last chapter the centralized workflow is best used in individual or small team research projects to collaborate and enhance

* Best used for small teams \(5 to 10\) transitioning from SVN to Git.
* Ideal use case for research projects involving one or max 3 members
* All members work on a single master branch and not branches of the master
* Best for maintaining documentation

Before we run thru an example, how would you know if the centralized workflow is for you and your team? You need to answer a "yes" for 3 basic questions. If "no" for any one of these questions, then the centralized workflow is not the best option.

The questions

1. Is your team expected to remain small i.e. maximum 10 users in the future?
2. Can errors be easily corrected?
3. Will the team need to learn very little to get things up and running?

Let me now give an example. 

The setup is a research project called "Spy talk". The project name is a dead give away of what the company funding that project deals in. The company specialises in, lets say, providing spy solutions to governments who can pay the price. Two brilliant and highly skilled researchers Neville and Rosa are working on the project. Neville and Rosa are both electronics and communication specialists and have worked on many military projects together. 

![Spy talk project](../.gitbook/assets/image%20%2816%29.png)

Neville is the project lead and maintains the remote repository located on a bitbucket server.

The project has 3 modules and a documentation section. 

1. The Transmitter module \(maintained by Neville\)
2. The Receiver module \(maintained by Rosa\)
3. The Encoder Decoder module \(maintained by Neville and Rosa\)
4. Documentation \(maintained by Neville and Rosa\)

Now here you can see that Neville and Rosa work independently on two modules each but collaborate with each other on one of the modules and also on the documentation.

Lets have a look at the project structure on the bitbucket server.

![spytalk repo with a readme doc and 2 folders](../.gitbook/assets/image%20%2829%29.png)

![modules folder contents](../.gitbook/assets/image.png)

![documentation folder contents](../.gitbook/assets/image%20%2836%29.png)

The bitbucket repo is the remote repo. It is the birthplace of the project. It is maintained on an online server. Neville and Rosa will make local copies or clones of the repo in their personal machines.

![](../.gitbook/assets/image%20%2817%29.png)

Neither Rosa nor Neville \(even though he is the project admin\) can edit the contents of the files on the server. They need to create a clone of the repo on their local machines. Lets have a look at each of their folders in git bash.

![Neville&apos;s git bash folder view](../.gitbook/assets/image%20%2818%29.png)

![Rosa&apos;s git bash folder](../.gitbook/assets/image%20%281%29.png)

Now lets look at how they both work individually and together on the files in their project. Remember Neville maintains the transmitter module and Rosa maintains the receiver module and they both mange the encoder decoder modules and the documentation. Lets look at Nevilles workflow first.





