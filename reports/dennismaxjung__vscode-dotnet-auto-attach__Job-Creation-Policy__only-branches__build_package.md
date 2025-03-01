
# Title of the anti-pattern
Job build_package is not created when certain new commits are pushed.

## Description
Developers should follow principles (or best practices) in order to properly practice Continuous Integration (CI) and Delivery (CD).
We found that [.gitlab-ci.yml](https://gitlab.com/dennismaxjung/vscode-dotnet-auto-attach/blob/master/.gitlab-ci.yml) contains a violation of the following CI/CD principle:

> Every committed change has to be built through the entire CI/CD pipeline (meaning that every defined job should be executed). 
If not, defects, that can only be reported during a certain job, might be discovered later in the development process (becoming harder to fix) or even discovered by users in production.

## How to locate the violation
Job `build_package`, that is defined at line , is set to  be created in stage `` if developers commit changes to some branches



## Information about this issue

This issue has been automatically generated by [CD-Linter](https://gitlab.com/Jancso/configuration-analytics), a tool that detects settings in the GitLab CI/CD Pipeline Configuration that violate the principles of Continuous Delivery. Those principles, that are nowadays widely accepted, are discussed by Jez Humble and David Farley in their landmark [book](https://www.oreilly.com/library/view/continuous-delivery-reliable/9780321670250/) on Continuous Delivery (CD). CD-Linter has been developed at the University of Zurich.

### Your feedback is important for us
We are currently evaluating the effectiveness of our tool. If you agree on the reported violation and are willing to fix it, please upvote this issue.

