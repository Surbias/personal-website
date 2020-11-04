+++
title = "GitOps - What is it?"
date = "2019-02-03"
description = "What is GitOps, its origins and when should be used."
tags = [
    "Technology",
    "GitOps",
    "DevOps",
]
+++

GitOps is essentially using Git, a source control versioning system (SCVS), to control software infrastructure.

Applying GitOps to a project can simplify the way it is deployed since both the project's code, configuration files and deployment tools would be under the same source control versioning system.

How does this work?

Essentially it can work in any way necessary since this is highly configurable but the primary use case is that it can generate a system build upon a pull request. This build will generate an *artifact which can then be used to preview the system with the changes applied on said pull request.

There are already plenty of companies applying GitOps to their products to a great deal of success:

* [Netlify](https://www.netlify.com/features/) allows to preview the changes of a website via pull request

* [WeaveWorks](https://www.weave.works/blog/gitops-operations-by-pull-request) uses GitOps to provision their AWS resources and Kubernetes deployment
* [Github](https://github.com/marketplace/category/continuous-integration) add integration of third party tools to perform actions upon Git

So when should we look into implementing GitOps to our projects?

Well, for small green-field project I would say it is a must, especially with excelent third-party tools such as [CircleCI](https://circleci.com) and [Netlify](https://www.netlify.com) out there. A developer sets it up once and then it is completely automated with very little effort.

With existing big projects, it really depends on the type of infrastructure available, technologies being used and the team composition of the project. GitOps depends on Git, which is mostly a developer tool.

The team, if composed of people not used to development and its related tools, will need to adapt the existing infrastructure to work with Git. This might mean the creation of a centralised repository with all the configuration in place.

In any case, in a big project the most likely scenario is the creation of a custom solution to their own needs in parallel to the one being used already, which can be quite costly.

If the project is struggling with issues regarding downtime upon disaster recovery ([mean time to recovery](https://en.wikipedia.org/wiki/Mean_time_to_recovery)) then betting on practices such a GitOps might be beneficial in the long run.

\* [artifact](https://en.wikipedia.org/wiki/Artifact_(software_development)) in this context means the source compiled for testing purposes