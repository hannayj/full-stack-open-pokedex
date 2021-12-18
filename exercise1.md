# 11.1 Warming up
The imaginary application of this exercise is coded with Clojure and ClojureScript. 

## Linting, testing and building
Linting would be taken care of with [Clj-kondo](https://github.com/clj-kondo/clj-kondo), which is quite widely used Clojure and ClojureScript linting library. For example, if one is using VS Code and therefore uses Calva to run the code, Clj-kondo comes as readymade part of Calva.

[clojure.test namespace](https://clojure.github.io/clojure/clojure.test-api.html) is a good framework for unit tests. For integration tests one could use for example [Greenlight](https://github.com/amperity/greenlight). For end-to-end tests I would use for example [Cypress](https://www.cypress.io/) or [Playwright](https://playwright.dev/java/docs/intro/) which has Java syntax, that can be utilized in Clojure through java interop.

For building there is a [tools.build library](https://clojure.org/guides/tools_build) for building Clojure projects.

## Alternatives to Jenkins and GitHub Actions, e.g.
* GitLab
* Amboo
* JFrog
* Spinnaker
* TeamCity
* AWS CodePipeline
* Azure DevOps

## Self-hosted or cloud-based environment?
To figure out whether to use self-hosted or cloud-based environment for CI/CD, one would first of all need to consider the scale of the project. Small are easier to build in cloud-environment. Also, because more and more softwares are run in some sort of cloud-platform, it might be easy to use the CI/CD-tool of that same platform (as mentioned the AWS and Azure platforms above). 

Self-hosted environment might also require a bit more “IT-knowledge” in a larger scale, when one needs to put up some hardware. I would imagine that quite many basic things are in order in the cloud-based systems and therefore they might be easier to take over by a rookie.
