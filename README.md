# Purpose
This purpose of this application is to stand up the AWS side of Soracom's getting started guide for [Beam](https://developers.soracom.io/en/start/aws/beam-iotcore/). 

# Considerations
Since terraform does not currently support email for SNS we will instead send a text message to a provided phone number. Note that the region is us-west-2 and not us-east-2 in this example. This is because SMS is only supported in certain regions by AWS Simple Notification Service. 

# Prerequisites
The [AWS CLI](https://aws.amazon.com/cli/) and [Terraform](https://learn.hashicorp.com/terraform/getting-started/install) must be installed and ready for use on your computer. See the corresponding installation and getting started guides for more information. 

You will also want to add a phone number you have access to in the variables.tf file. 

# Initialize Terraform 
`terraform init`

# Create the Plan
`terraform plan`

# Apply the Plan
`terraform apply`

# Outputs
The https iot endpoint will be output after running the apply command. The certs and keys are located in the certs/ directory. Use these to configure Beam in the Soracom console.

# Teardown
`terraform destroy`