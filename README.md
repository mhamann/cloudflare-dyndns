# CloudFlare DynDNS v1.1
Author: Darren Smith, Matt Hamann (@mhamann)

Forked frorm: https://github.com/darrensmith/cloudflare-dyndns

Thanks for checking out my Dynamic DNS Update tool for CloudFlare.

CloudFlare is the perfect dynamic DNS host because, unlike the other major ones supported by many routers, CloudFlare is completely free. Unfortunately most routers don't support dynamically updating DNS records on CloudFlare - and so you need a tool that can run in the background of a server on your LAN. This is that tool.

To get started:

This library requires a configuration to define which CloudFlare zones/records to update in addition to your username and API key.
In order to aid deployment as a Docker container, the cloud-based configuration engine [Mothership](https://mothership.cloud).
Set up a free account and load the configuration from `config.json.example`, then make modifications for your zone/credentials.

* Clone this repository to the computer that you wish to run this on
* Type "npm install" to install all dependencies
* Set the `MOTHERSHIP_KEY` environment variable to the value of your Mothership app's key.
* Run the process using "npm start" or build the Docker container.

Alternatively, simply run the Docker container directly from Docker Hub:

`$ docker run -e MOTHERSHIP_KEY=<mothership_key> -d --restart unless-stopped mhamann/cloudflare-dyndns`

