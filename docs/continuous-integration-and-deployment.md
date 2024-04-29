# Continuous integration and deployment

Continuing to developping a package into the future it would be helpful to automate many of these workflows so you and your collaborators can focus more on writing code and less on the nuances of packaging and testing. This is where continuous integration (CI) and continuous deployment (CD) come in! CI/CD generally refers to the automated testing, building, and deployment of software.

Continuous integration (CI) is practice that involves developers making small changes and checks to their code. Due to the scale of requirements and the number of steps involved, this process is automated to ensure that teams can build, test, and package their applications in a reliable and repeatable way. CI helps streamline code changes, thereby increasing time for developers to make changes and contribute to improved software.

Continuous delivery (CD) is the automated delivery of completed code to environments like testing and development. CD provides an automated and consistent way for code to be delivered to these environments.

Continuous deployment is the next step of continuous delivery. Every change that passes the automated tests is automatically placed in production, resulting in many production deployments.

Continuous deployment should be the goal of most companies that are not constrained by regulatory or other requirements.

# Tools
There are many CI/CD services out there — such as [GitHub Actions](https://docs.github.com/en/actions), [Travis CI](https://www.travis-ci.com/), and [CircleCi](https://circleci.com/).