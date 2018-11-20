# Kitchen-Terraform extensive example

This repository contains an extensive kitchen-terraform code example (AWS EC2, IAM, etc.)

## Credit:
Based on [this example](https://newcontext-oss.github.io/kitchen-terraform/tutorials/extensive_kitchen_terraform.html)

## Prerequisites:
1. AWS account

## Usage

The following instructions assume you start with a clean Ubuntu 16.04 LTS Xenial VM  
(for example `ami`&#8209;`0f9351b59be17920e` in `us-east-1`)

1. Install the dependency hell:
``
$ sudo apt update
$ sudo apt install -y less gcc ruby ruby-dev make g++ git jq unzip python-pip
$ sudo gem install bundler
```
2. [Install Terraform](https://www.terraform.io/intro/getting-started/install.html)
~~3. [Install the AWS CLI tool](https://docs.aws.amazon.com/cli/latest/userguide/awscli-install-linux.html)~~
3. Install the AWS CLI tool:
```
$ sudo apt install awscli
```
4. [Configure the AWS CLI tool](https://docs.aws.amazon.com/cli/latest/userguide/cli-chap-getting-started.html#cli-quick-configuration)
5. Clone this repository and `cd` into it.
6. Run the following:
```
$ ./generate_ssh_key.sh
$ bundle install
$ ./run.sh
```

Note: Make sure there are no instances left running in AWS (check both us-east-1 and us-west-2)