# Udemier
A udemy app implemented in Tizen for my Samsung television. The idea of this application to learn Tizen development for an upcoming project, while creating something I can benefit off myself.

# Technologies
- Angular 9
- Tizen API
- API integration via Udemy's API Affiliation program (if I get approved).
- Tizen Studio 3.6
- Visual Studio Code
- Angular CLI

# Device
- Samsung UHD Series 7

# The application
The purpose of this application is to stream my courses that I have purchased to my Tizen-based Samsung television, in order to work through content in the luxury of my couch, over the next 21-days, while being locked down and isolated due to the spread of Covid-19.

The underlying project started as need to learn about Tizen, the API and the distribution methods to get applications deployed, as I will be architecting, and leading a small team in building a Tizen-based application.

# Continuous Integration / Continuous Delivery
Pipelines are run via Azure DevOps.

Due to the nature of the deployment to a television, running a deployment via Azure DevOps is not currently possible. Artifacts are dropped into a folder on OneDrive, then a folder watch is performed on the OneDrive folder from a device on my local network, if a new version, since the last version has been dropped, it extracts the artifacts and runs a Powershell script to deploy the application to the television, if the television is turned on, otherwise it'll just wait, a maximum of 2 hours, before gracefully failing and sending me an email of a failed attempt to deploy.

Deployment to device is done via Tizen Studio API