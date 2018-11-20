# Kitchen-Terraform extensive example

This repository contains an extensive kitchen-terraform code example (AWS EC2, IAM, etc.)

## Prerequisites:
1. AWS account

## Usage

The following instructions assume you start with a clean Ubuntu 16.04 LTS Xenial VM (for example `ami-0f9351b59be17920e` in `us-east-1`)

1. [Install Terraform](https://www.terraform.io/intro/getting-started/install.html)
2. [Install the AWS CLI tool](https://aws.amazon.com/documentation/cli/)
3. [Configure the AWS CLI tool](https://docs.aws.amazon.com/cli/latest/userguide/cli-chap-getting-started.html#cli-quick-configuration)
4. Install the dependency hell:
```
$ sudo apt-get update
$ sudo apt-get install -y less gcc ruby ruby-dev make g++ git jq
$ sudo gem install bundler
```
5. Clone this repository and `cd` into it.
6. Run the following:
```
$ bundle install
$ bundle exec kitchen test
```

Note: Make sure there are no instances left running in AWS (check both us-east-1 and us-west-2)