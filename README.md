# FortiGate Autoscale
A collection of **Node.js** modules and cloud-specific templates which support autoscale functionality for groups of FortiGate-VM instances on various cloud platforms.

This project contains the code and templates for the **Amazon AWS** and **Microsoft Azure** autoscale deployments. For autoscale on **AliCloud** see the [alicloud-autoscale](https://github.com/fortinet/alicloud-autoscale/) repository.

A collection of **Node.js** modules and cloud-specific templates which support autoscale functionality for groups of FortiGate-VM instances on various cloud platforms.

 * [fortigate-autoscale/core](core) contains the core logic and provides an interface which can be extended to deal with the differences in cloud platform APIs.
 * [fortigate-autoscale/azure](azure) contains an implementation for the **Microsoft Azure** platform API and **Cosmos DB** storage backend.
 * [fortigate-autoscale/aws](aws) contains an implementation for the **AWS SDK** platform API with a **Dynamo DB** storage backend.

The project also contains a deployment script which can generate packages for each cloud service's *serverless* implementation.

## Supported Platforms
This project supports autoscale for the cloud platforms listed below. The version tag in parentheses refers to the autoscale module version included in this project.

  * Amazon AWS Lambda (2.0.0)

## Deployment Packages
To generate local deployment packages:

  1. Clone this project.
  2. Checkout the `aws-transit-gateway` branch
  2. Run `npm run build-aws-cloudformation` at the project root directory.

The deployment package as well as source code will be available in the **dist** directory.

| Package Name | Description |
| ------ | ------ |
| fortigate-autoscale-aws-cloudformation.zip | Cloud Formation template and related assets. Use this to deploy the solution on the AWS platform.|

An Installation Guide is available from the Fortinet Document Library:

  * [FortiGate / FortiOS Deploying Auto Scaling on AWS with Transit Gateway integration](https://docs.fortinet.com/vm/aws/fortigate/6.2/aws-cookbook/6.2.0/397979/deploying-auto-scaling-on-aws)

# Support
Fortinet-provided scripts in this and other GitHub projects do not fall under the regular Fortinet technical support scope and are not supported by FortiCare Support Services.
For direct issues, please refer to the [Issues](https://github.com/fortinet/fortigate-autoscale/issues) tab of this GitHub project.
For other questions related to this project, contact [github@fortinet.com](mailto:github@fortinet.com).

## License
[License](https://github.com/fortinet/fortigate-autoscale/blob/master/LICENSE) © Fortinet Technologies. All rights reserved.
