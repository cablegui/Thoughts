# GIT workflows

A workflow is a set of guidelines on how to get from point A to point B. 

![How to get from point A to B?](../.gitbook/assets/image%20%2827%29.png)

Git provides several workflow methods to accomplish work in a productive manner. After discussing the several workflows commonly used in Git the next chapter focuses on the workflow most suitable for the individual research project \(centralized\), regular stress testing \(feature branch\) team, ECB stress testing \(Gitflow\), intra team projects \(forking\)

I will discuss 4 different types of workflows and in which settings they are best used for.

* Centralized workflow. 
  * Best used for small teams \(5 to 10\) transitioning from SVN to Git.
  * Best for research projects involving one or max 3 members
  * All members work on a single master branch and not branches of the master
  * Best for maintaining documentation
* Feature branch workflow
  * Best for small \(5 to 10\) to medium \(max 20\) size teams working on project code **not** **tied** to release cycles
  * Best for maintaining production code for running systems because it requires the main master branch contains cleans code
  * Best workflow to implement continous integration environments. Continuous integration environments are code, build, test and deploy frameworks which ensure that well tested code changes dont break the production system.
  * Best way to comment on code features or bug fixes via the bitbucket pull request system
* Gitflow workflow
  * Best for small \(5 to 10\) to medium \(max 20\) size teams working on project code **tied** to release cycles
  * Best for very concentrated projects with deadlines
  * Also implements the Feature branch workflow
* Forking workflow
  * Best when working on projects involving collaboration between teams
  * Used in very large open source projects
  * Project maintainer maintains the official repo on the server. Other developers can fork this repo thus making a copy of the official repo on their own server.
  * Project maintainer can work on enhancing features in the official repo and does not have to worry about authentication of other developers on the official repo. Other developers can just fork the maintainers repo and push any changes to their own forked repo on their own server.
  * Other developers who fork the official repo can send a pull request to the project maintainer who can merge or reject the changes. Merged changes then become part of the official repo if the project maintainer approves it.

