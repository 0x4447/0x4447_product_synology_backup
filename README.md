# Synology Backup

This stack will create all that is needed to allow Synology to backup your date to Amazon Glacier, by creating the most strick AMI Policy despite the fact that Synology is setup to make a Vault on your behalf. Check the policy to see all the details.

# Companion Video

If you want to follow up on how this stack was created, check this two videos:

- [Part 1](https://www.youtube.com/watch?v=XrEaMN1QBj4)
- [Part 2](https://www.youtube.com/watch?v=rUtXZeMEonM)

# DISCLAIMER!

This stack is available to anyone at no cost, but on an as-is basis. 0x4447, LLC. is not responsible for damages or costs of any kind that may occur when you use the stack. You take full responsibility when you use it.

# How to deploy

<a target="_blank" href="https://console.aws.amazon.com/cloudformation/home#/stacks/new?stackName=zer0x4447-synology-backup&templateURL=https://s3.amazonaws.com/0x4447-drive-cloudformation/synology-backup.json">
<img align="left" style="float: left; margin: 0 10px 0 0;" src="https://s3.amazonaws.com/cloudformation-examples/cloudformation-launch-stack.png"></a>

All you need to do to deploy this stack is click the button to the left and follow the instructions that CloudFormation provides in your AWS Dashboard. Alternatively you can download the CF file from [here](https://s3.amazonaws.com/0x4447-drive-cloudformation/synology-backup.json).

# What will deploy?

![synology-s3-glacier Diagram](https://raw.githubusercontent.com/0x4447/0x4447_product_synology_backup/assets/diagram.png)

- 1x IAM User with a custom Policy.

# Manual work

You'll need to create the API Key by hand, this way only you can see them. To do so:

- Go to the AWS Console
- Go to the IAM Service
- From the left menu click on `Users`
- Click on the new user that was created by this project
- Click on the tab called `Security credentials`
- Then in the `Access keys` section, click the `Create access key` button.
- Lastelly copy the credentials in a secure place, this credentials needs to passed to Synology.

# Pricing

Default S3 Glacier pricing applies, find out more [here](https://aws.amazon.com/glacier/pricing/).

# How to generate the CloudFormation file

This repo was build using the [Grapes Frameworks](https://www.npmjs.com/package/@0x4447/grapes). First you need to install the framework:

```
sudo npm install -g @0x4447/grapes
```

Then, go inside this repo and run this command:

```
grapes -s .
```

This will create a `CloudFormation.json` file in the root dir of the repo which you can upload to AWS.

# The End

If you enjoyed this project, please consider giving it a 🌟. And check out our [0x4447 GitHub account](https://github.com/0x4447), where you'll find additional resources you might find useful or interesting.

## Sponsor 🎊

This project is brought to you by 0x4447 LLC, a software company specializing in building custom solutions on top of AWS. Follow this link to learn more: [https://0x4447.com](https://0x4447.com/?utm_source=github&utm_medium=0x4447_product_synology_backup). Or check our [consulting page](https://consulting.0x4447.com/?utm_source=github&utm_medium=0x4447_product_synology_backup).
