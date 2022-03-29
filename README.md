# MicroserviceBlogs


Sid Phillips
Netflix - How We Build Code

Netflix Tech Blog’s article, “How We Build Code,” provides a look at how Netflix can build code before deploying it to the cloud, and shows how they can take source code written by a handful of developers and turn it into a deployed service streaming movies to millions upon millions of users. 
To understand Netflix’s architecture, you first need to understand Spinnaker. Spinnaker is an open-source continuous delivery platform for releasing software changes with high velocity and confidence, and is designed with pluggability (the ease of extending and enhancing cloud deployment models) in mind. 
Before a piece of code even touches Spinnaker, however, it must go through a number of steps. Code is built and tested locally using Nebula (opinionated set of plugins for gradle), before being pushed to a central git repository. Next, a Jenkins (an open source automation server) job helps to build, test, and package the application for deployment. “The Bakery” helps to facilitate turning source into Amazon Machine Instances (AMIs), and finally Spinnaker pipelines are used to deploy and promote the code changes, which I’ll get into here.
Now that the bake is complete, Spinnaker makes the resultant AMI available for deployment to tens, hundreds, or thousands of instances. This AMI can be used in a variety of environments, as Spinnaker exposes a runtime context to the application, allowing it to self-configure upon execution. Another team checks the deployment using “a battery of automated tests.” 
Also important is the Netflix Culture. 


Assigned Question
Please read “Netflix - how we build code”. Explain what Spinnaker is (their global continuous delivery platform and the number of steps required bey Netflix developer before a line of code makes its way into Spinnaker. How does the Netflix culture, use of cloud and microservices influence this process? Cover the Build as well, Integrate, Bake, and the Deploy process including the use of Janitor Monkey.               Finally, summarize their multi-region deployment.

