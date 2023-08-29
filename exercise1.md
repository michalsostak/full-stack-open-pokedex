# CI / CD

## Some common steps in a CI setup include linting, testing, and building. What are the specific tools for taking care of these steps in the ecosystem of the language you picked?

There are several popular option for formatting and linting in C#. .NET comes with a code formatter called dotnet-format that can be configured by setting up a EditorConfig file in your solution, similar to .prettierrc file in js/ts. A quite popular formatter alternative is StyleCop. Linting is often done using ReSharper, an IDE extension, but tends to slow down Visual Studio considerably when larger solutions are analyzed. Another popular linter is SolarLint. The standard build tool for C# tends to be the MSBuild. C# also has several testing frameworks, such as xUnit or NUnit or Moq.

## What alternatives are there to set up the CI besides Jenkins and GitHub Actions?

Similar features as Jenkins can be found in Jetbrain's TeamCity, Gitlab CI or Azure DevOps

## Would this setup be better in a self-hosted or a cloud-based environment? Why? What information would you need to make that decision?

Many services are nowadays moving to cloud, as cloud-based environments offer scalability, flexibility, so even a larger company does not have to rely on self hosting (unless a market-domain requires it, due to security, etc.). However, for a project of only six people, we might presume the scale to be not especially large and is some sort of simple-ish CRUD app, then cloud based hosting is the way to go. Nevertheless, if the project involves developing a very peculiar feature, which may require expensive-to-rent resources (GPUs?) or some custom configuration that is hard to setup on cloud, then self hosting may be a better option.
