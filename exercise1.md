Assuming we use Python for a web backend project with 6 team members. The common steps & tools in a CI setup include:
- Linting: pylint is the most well known and is default in vscode, otherwise there's (more opinionated) black, flake8..etc. 
- Testing: pytest is used for unit tests, there's other library on top of that for integration test, like SeleniumBase
- Building: Python doesn't require compiling, so we just need to "pip install" the requirement libraries. Noting that "pip" is a Python package management system. 

Aside from Jenkins and GitHub Actions, we have fairly popular Gitlab CI (integrate with GitLab obviously), Bamboo (Atlassian ecosystem), Circle CI (platform independant) and others.

If the team is small, it is better to use cloud-based CI platform. Firstly it saves at least one person from seting up and managing the infrastructure. Secondly it might be even cheaper since many cloud flatforms offer free services up until a certain threshold, and you only have to pay for what you use instead of dedicating a whole new server which might be under-utilized. 

There are few considerations where self-hosted is a must though. The first thing is security, in some sectors like finance, banking, govermental it is required to store the code on-premises. Or there are some special security standards that the cloud providers don't have like GDPR. Next is compabilities, each cloud provider only focus on a specific set of scopes, platforms, and hardwares which might not fit our various requirements.