# stemcell-rn-bot

The Stemcell RN Bot does the following:
1. Checks for new PCF stemcells published to [Pivotal Network](https://network.pivotal.io).
2. If it finds new PCF stemcells, it retrieves the release notes for the stemcells from the BOSH releases on [GitHub](https://github.com/cloudfoundry/bosh/releases). 
3. Using the information retrieved from GitHub, it builds a new "Stemcell Release Notes" topic and publishes it to https://docs.pivotal.io/pivotalcf/pcf-release-notes/stemcell-rn.html.

I've deployed it with Concourse, adding a `time-resource` so that it runs once a day.
