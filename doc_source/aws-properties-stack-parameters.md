# AWS CloudFormation Stack Parameters<a name="aws-properties-stack-parameters"></a>

The `Parameters` type is an embedded property of the [AWS::CloudFormation::Stack](aws-properties-stack.md) type\.

The `Parameters` type contains a set of value pairs that represent the parameters that will be passed to the template used to create an `AWS::CloudFormation::Stack` resource\. Each parameter has a name corresponding to a parameter defined in the embedded template and a value representing the value that you want to set for the parameter\. For example, the sample template EC2ChooseAMI\.template contains the following `Parameters` section:

## JSON<a name="aws-properties-stack-parameters-example1.json"></a>

```
 1. "Parameters" : {
 2.    "InstanceType" : {
 3.       "Type" : "String",
 4.       "Default" : "m1.small",
 5.       "Description" : "EC2 instance type, e.g. m1.small, m1.large, etc."
 6.    },
 7.    "WebServerPort" : {
 8.       "Type" : "String",
 9.       "Default" : "80",
10.       "Description" : "TCP/IP port of the web server"
11.    },
12.    "KeyName" : {
13.       "Type" : "String",
14.       "Description" : "Name of an existing EC2 KeyPair to enable SSH access to the web server"
15.    }
16. }
```

## YAML<a name="aws-properties-stack-parameters-example1.yaml"></a>

```
 1. Parameters: 
 2.   InstanceType: 
 3.     Type: "String"
 4.     Default: "m1.small"
 5.     Description: "EC2 instance type, e.g. m1.small, m1.large, etc."
 6.   WebServerPort: 
 7.     Type: "String"
 8.     Default: "80"
 9.     Description: "TCP/IP port of the web server"
10.   KeyName: 
11.     Type: "String"
12.     Description: "Name of an existing EC2 KeyPair to enable SSH access to the web server"
```

## Nested Stack<a name="w3ab2c21c14d223c11"></a>

You could use the following template to embed a stack \(myStackWithParams\) using the EC2ChooseAMI\.template and use the Parameters property in the AWS::CloudFormation::Stack resource to specify an InstanceType and KeyName:

### JSON<a name="aws-properties-stack-parameters-example2.json"></a>

```
 1. {
 2.    "AWSTemplateFormatVersion" : "2010-09-09",
 3.    "Resources" : {
 4.       "myStackWithParams" : {
 5.          "Type" : "AWS::CloudFormation::Stack",
 6.          "Properties" : {
 7.             "TemplateURL" : "https://s3.amazonaws.com/cloudformation-templates-us-east-1/EC2ChooseAMI.template",
 8.             "Parameters" : {
 9.                "InstanceType" : "t1.micro",
10.                "KeyName" : "mykey"
11.             }
12.          }
13.       }
14.    }
15. }
```

### YAML<a name="aws-properties-stack-parameters-example2.yaml"></a>

```
1. AWSTemplateFormatVersion: "2010-09-09"
2. Resources: 
3.   myStackWithParams: 
4.     Type: "AWS::CloudFormation::Stack"
5.     Properties: 
6.       TemplateURL: "https://s3.amazonaws.com/cloudformation-templates-us-east-1/EC2ChooseAMI.template"
7.       Parameters: 
8.         InstanceType: "t1.micro"
9.         KeyName: "mykey"
```