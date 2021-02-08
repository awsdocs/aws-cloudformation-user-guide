# Parameters<a name="parameters-section-structure"></a>

Use the optional `Parameters` section to customize your templates\. Parameters enable you to input custom values to your template each time you create or update a stack\.

## Defining a parameter in a template<a name="parameters-section-structure-defining"></a>

The following example declares a parameter named `InstanceTypeParameter`\. This parameter lets you specify the Amazon EC2 instance type for the stack to use when you create or update the stack\.

Note that `InstanceTypeParameter` has a default value of `t2.micro`\. This is the value that AWS CloudFormation uses to provision the stack unless another value is provided\.

### JSON<a name="parameters-section-structure-example.json"></a>

```
"Parameters" : {
  "InstanceTypeParameter" : {
    "Type" : "String",
    "Default" : "t2.micro",
    "AllowedValues" : ["t2.micro", "m1.small", "m1.large"],
    "Description" : "Enter t2.micro, m1.small, or m1.large. Default is t2.micro."
  }
}
```

### YAML<a name="parameters-section-structure-example.yaml"></a>

```
Parameters:
  InstanceTypeParameter:
    Type: String
    Default: t2.micro
    AllowedValues:
      - t2.micro
      - m1.small
      - m1.large
    Description: Enter t2.micro, m1.small, or m1.large. Default is t2.micro.
```

## Referencing a parameter within a template<a name="parameters-section-structure-referencing"></a>

You use the `Ref` intrinsic function to reference a parameter, and AWS CloudFormation uses the parameter's value to provision the stack\. You can reference parameters from the `Resources` and `Outputs` sections of the same template\.

In the following example, the `InstanceType` property of the EC2 instance resource references the `InstanceTypeParameter` parameter value:

### JSON<a name="parameters-section-structure-example2.json"></a>

```
"Ec2Instance" : {
  "Type" : "AWS::EC2::Instance",
  "Properties" : {
    "InstanceType" : { "Ref" : "InstanceTypeParameter" },
    "ImageId" : "ami-0ff8a91507f77f867"
  }
}
```

### YAML<a name="parameters-section-structure-example2.yaml"></a>

```
Ec2Instance:
  Type: AWS::EC2::Instance
  Properties:
    InstanceType:
      Ref: InstanceTypeParameter
    ImageId: ami-0ff8a91507f77f867
```

## General requirements for parameters<a name="parameters-section-structure-requirements"></a>

The following requirements apply when using parameters:
+ You can have a maximum of 200 parameters in an AWS CloudFormation template\.
+ Each parameter must be given a logical name \(also called logical ID\), which must be alphanumeric and unique among all logical names within the template\.
+ Each parameter must be assigned a parameter type that is supported by AWS CloudFormation\. For more information, see [Type](#parameters-section-structure-properties-type)\.
+ Each parameter must be assigned a value at runtime for AWS CloudFormation to successfully provision the stack\. You can optionally specify a default value for AWS CloudFormation to use unless another value is provided\.
+ Parameters must be declared and referenced from within the same template\. You can reference parameters from the `Resources` and `Outputs` sections of the template\.

## JSON<a name="parameters-section-structure-syntax"></a>

```
"Parameters" : {
  "ParameterLogicalID" : {
    "Type" : "DataType",
    "ParameterProperty" : "value"
  }
}
```

## YAML<a name="parameters-section-structure-syntax.yaml"></a>

```
Parameters:
  ParameterLogicalID:
    Type: DataType
    ParameterProperty: value
```

## Properties<a name="parameters-section-structure-properties"></a>

`AllowedPattern`  
A regular expression that represents the patterns to allow for `String` types\. The pattern must match the entire parameter value provided\.  
*Required*: No

`AllowedValues`  
An array containing the list of values allowed for the parameter\.  
*Required*: No

`ConstraintDescription`  
A string that explains a constraint when the constraint is violated\. For example, without a constraint description, a parameter that has an allowed pattern of `[A-Za-z0-9]+` displays the following error message when the user specifies an invalid value:  
`Malformed input-Parameter MyParameter must match pattern [A-Za-z0-9]+`  
By adding a constraint description, such as *must only contain letters \(uppercase and lowercase\) and numbers*, you can display the following customized error message:  
`Malformed input-Parameter MyParameter must only contain uppercase and lowercase letters and numbers`  
*Required*: No

`Default`  
A value of the appropriate type for the template to use if no value is specified when a stack is created\. If you define constraints for the parameter, you must specify a value that adheres to those constraints\.  
*Required*: No

`Description`  
A string of up to 4000 characters that describes the parameter\.  
*Required*: No

`MaxLength`  
An integer value that determines the largest number of characters you want to allow for `String` types\.  
*Required*: No

`MaxValue`  
A numeric value that determines the largest numeric value you want to allow for `Number` types\.  
*Required*: No

`MinLength`  
An integer value that determines the smallest number of characters you want to allow for `String` types\.  
*Required*: No

`MinValue`  
A numeric value that determines the smallest numeric value you want to allow for `Number` types\.  
*Required*: No

`NoEcho`  
Whether to mask the parameter value to prevent it from being displayed in the console, command line tools, or API\. If you set the `NoEcho` attribute to `true`, CloudFormation returns the parameter value masked as asterisks \(\*\*\*\*\*\) for any calls that describe the stack or stack events, except for information stored in the locations specified below\.   
Using the `NoEcho` attribute does not mask any information stored in the following:  
+ The `Metadata` template section\. CloudFormation does not transform, modify, or redact any information you include in the `Metadata` section\. For more information, see [Metadata](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/metadata-section-structure.html)\.
+ The `Outputs` template section\. For more information, see [Outputs](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/outputs-section-structure.html)\.
+ The `Metadata` attribute of a resource definition\. For more information, [Metadata attribute](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-attribute-metadata.html)\.
We strongly recommend you do not use these mechanisms to include sensitive information, such as passwords or secrets\.
Rather than embedding sensitive information directly in your AWS CloudFormation templates, we recommend you use dynamic parameters in the stack template to reference sensitive information that is stored and managed outside of CloudFormation, such as in the AWS Systems Manager Parameter Store or AWS Secrets Manager\.  
For more information, see the [Do not embed credentials in your templates](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/best-practices.html#creds) best practice\.
*Required*: No

`Type`  <a name="parameters-section-structure-properties-type"></a>
The data type for the parameter \(`DataType`\)\.  
*Required*: Yes  
AWS CloudFormation supports the following parameter types:    
`String`  
A literal string\.  
For example, users could specify `"MyUserName"`\.  
`Number`  
An integer or float\. AWS CloudFormation validates the parameter value as a number; however, when you use the parameter elsewhere in your template \(for example, by using the `Ref` intrinsic function\), the parameter value becomes a string\.  
For example, users could specify `"8888"`\.  
`List<Number>`  
An array of integers or floats that are separated by commas\. AWS CloudFormation validates the parameter value as numbers; however, when you use the parameter elsewhere in your template \(for example, by using the `Ref` intrinsic function\), the parameter value becomes a list of strings\.  
For example, users could specify `"80,20"`, and a `Ref` would result in `["80","20"]`\.  
`CommaDelimitedList`  
An array of literal strings that are separated by commas\. The total number of strings should be one more than the total number of commas\. Also, each member string is space trimmed\.  
For example, users could specify `"test,dev,prod"`, and a `Ref` would result in `["test","dev","prod"]`\.  
AWS\-Specific Parameter Types  
AWS values such as Amazon EC2 key pair names and VPC IDs\. For more information, see [AWS\-specific parameter types](#aws-specific-parameter-types)\.  
`SSM` Parameter Types  
Parameters that correspond to existing parameters in Systems Manager Parameter Store\. You specify a Systems Manager parameter key as the value of the `SSM` parameter, and AWS CloudFormation fetches the latest value from Parameter Store to use for the stack\. For more information, see [SSM parameter types](#aws-ssm-parameter-types)\.

## AWS\-specific parameter types<a name="aws-specific-parameter-types"></a>

AWS\-specific parameter types are helpful in catching invalid values at the start of creating or updating a stack\. To specify parameters with AWS\-specific types, a template user must enter existing AWS values that are in their AWS account\. AWS CloudFormation validates these input values against existing values in the account\. For example, with the `AWS::EC2::VPC::Id` parameter type, a user must [enter an existing VPC ID](cfn-using-console-create-stack-parameters.md) that is in the account and region in which they are creating the stack\. 

If you want to allow template users to enter input values from different AWS accounts, don't define parameters with AWS\-specific types; instead, define parameters of type `String` \(or `CommaDelimitedList`\)\.

### Supported AWS\-specific parameter types<a name="aws-specific-parameter-types-supported"></a>

AWS CloudFormation supports the following AWS\-specific types:

`AWS::EC2::AvailabilityZone::Name`  
An Availability Zone, such as `us-west-2a`\.

`AWS::EC2::Image::Id`  
An Amazon EC2 image ID, such as `ami-0ff8a91507f77f867`\. Note that the AWS CloudFormation console doesn't show a drop\-down list of values for this parameter type\.

`AWS::EC2::Instance::Id`  
An Amazon EC2 instance ID, such as `i-1e731a32`\.

`AWS::EC2::KeyPair::KeyName`  
An Amazon EC2 key pair name\.

`AWS::EC2::SecurityGroup::GroupName`  
An EC2\-Classic or default VPC security group name, such as `my-sg-abc`\.

`AWS::EC2::SecurityGroup::Id`  
A security group ID, such as `sg-a123fd85`\.

`AWS::EC2::Subnet::Id`  
A subnet ID, such as `subnet-123a351e`\.

`AWS::EC2::Volume::Id`  
An Amazon EBS volume ID, such as `vol-3cdd3f56`\.

`AWS::EC2::VPC::Id`  
A VPC ID, such as `vpc-a123baa3`\.

`AWS::Route53::HostedZone::Id`  
An Amazon Route 53 hosted zone ID, such as `Z23YXV4OVPL04A`\.

`List<AWS::EC2::AvailabilityZone::Name>`  
An array of Availability Zones for a region, such as `us-west-2a, us-west-2b`\.

`List<AWS::EC2::Image::Id>`  
An array of Amazon EC2 image IDs, such as `ami-0ff8a91507f77f867, ami-0a584ac55a7631c0c`\. Note that the AWS CloudFormation console doesn't show a drop\-down list of values for this parameter type\.

`List<AWS::EC2::Instance::Id>`  
An array of Amazon EC2 instance IDs, such as `i-1e731a32, i-1e731a34`\.

`List<AWS::EC2::SecurityGroup::GroupName>`  
An array of EC2\-Classic or default VPC security group names, such as `my-sg-abc, my-sg-def`\.

`List<AWS::EC2::SecurityGroup::Id>`  
An array of security group IDs, such as `sg-a123fd85, sg-b456fd85`\.

`List<AWS::EC2::Subnet::Id>`  
An array of subnet IDs, such as `subnet-123a351e, subnet-456b351e`\.

`List<AWS::EC2::Volume::Id>`  
An array of Amazon EBS volume IDs, such as `vol-3cdd3f56, vol-4cdd3f56`\.

`List<AWS::EC2::VPC::Id>`  
An array of VPC IDs, such as `vpc-a123baa3, vpc-b456baa3`\.

`List<AWS::Route53::HostedZone::Id>`  
An array of Amazon Route 53 hosted zone IDs, such as `Z23YXV4OVPL04A, Z23YXV4OVPL04B`\.

## SSM parameter types<a name="aws-ssm-parameter-types"></a>

`SSM` parameter types correspond to existing parameters in Systems Manager Parameter Store\. You specify a Systems Manager parameter key as the value of the `SSM` parameter, and AWS CloudFormation fetches the latest value from Parameter Store to use for the stack\. For more information about Systems Manager parameters, see [ Systems Manager Parameter Store](https://docs.aws.amazon.com/systems-manager/latest/userguide/systems-manager-paramstore.html) in the *AWS Systems Manager User Guide*\.

You can also use the `ssm` or `ssm-secure` dynamic parameter pattern to specify parameter *values* in your template\. For more information, see [Using dynamic references to specify template values](dynamic-references.md)\.

When you create or update stacks and create change sets, AWS CloudFormation uses whatever values exist in Parameter Store at the time the operation is run\. If a specified parameter doesn't exist in Parameter Store under the caller's AWS account, AWS CloudFormation returns a validation error\.

When you execute a change set, AWS CloudFormation uses the values that are specified in the change set\. You should review these values before executing the change set because they might change in Parameter Store between the time that you create the change set and run it\.

**Tip**  
You can see the *resolved values* for `SSM` parameters on the stack's **Parameters** tab in the console, or by running [https://docs.aws.amazon.com/cli/latest/reference/cloudformation/describe-stacks.html](https://docs.aws.amazon.com/cli/latest/reference/cloudformation/describe-stacks.html) or [https://docs.aws.amazon.com/cli/latest/reference/cloudformation/describe-change-set.html](https://docs.aws.amazon.com/cli/latest/reference/cloudformation/describe-change-set.html)\. These are the values that are currently used in the stack definition for the corresponding Systems Manager parameter keys\. Note that these values are set when the stack is created or updated, so they might differ from the latest values in Parameter Store\.  
If you specify Secure Strings as parameter values using the `ssm-secure` pattern, AWS CloudFormation does not store the Secure String value or display it in the console or in the results of API calls\. 

Because the value of an `SSM` parameter is a Systems Manager parameter key, you should be aware of the following behavior:
+ For stack updates, the **Use existing value** option in the console and the `UsePreviousValue` attribute for [https://docs.aws.amazon.com/cli/latest/reference/cloudformation/update-stack.html](https://docs.aws.amazon.com/cli/latest/reference/cloudformation/update-stack.html) tell AWS CloudFormation to use the existing Systems Manager parameter key—not its value\. AWS CloudFormation always fetches the latest values from Parameter Store when it updates stacks\.

  However, if you use the `ssm` or `ssm-secure` dynamic parameter pattern to specify parameter values, you must specify a version of the Systems Manager parameter for AWS CloudFormation to use\.
+ AWS CloudFormation can perform validation on Systems Manager parameter keys, but not on their corresponding values\. For validation purposes, you can treat parameter keys as strings\. You should do any validation for Systems Manager parameter values in Parameter Store\.

See [`SSM` Parameter Types](#parameters-section-ssm-examples) for examples that use `SSM` parameter types\.

### Supported SSM parameter types<a name="aws-ssm-parameter-types-supported"></a>

AWS CloudFormation supports the following `SSM` parameter types:

`AWS::SSM::Parameter::Name`  
The name of a Systems Manager parameter key\.  
Use this parameter when you want to pass the parameter key\. For example, you can use this type to validate that the parameter exists\.

`AWS::SSM::Parameter::Value<String>`  
A Systems Manager parameter whose value is a string\. This corresponds to the `String` parameter type in Parameter Store\.

`AWS::SSM::Parameter::Value<List<String>>` or `AWS::SSM::Parameter::Value<CommaDelimitedList>`  
A Systems Manager parameter whose value is a list of strings\. This corresponds to the `StringList` parameter type in Parameter Store\.

`AWS::SSM::Parameter::Value<AWS-specific parameter type>`  
A Systems Manager parameter whose value is an [AWS\-specific parameter type](#aws-specific-parameter-types)\. For example, the following specifies the `AWS::EC2::KeyPair::KeyName` type:  
`AWS::SSM::Parameter::Value<AWS::EC2::KeyPair::KeyName>`

`AWS::SSM::Parameter::Value<List<AWS-specific parameter type>>`  
A Systems Manager parameter whose value is a list of [AWS\-specific parameter types](#aws-specific-parameter-types)\. For example, the following specifies a list of `AWS::EC2::KeyPair::KeyName` types:  
`AWS::SSM::Parameter::Value<List<AWS::EC2::KeyPair::KeyName>>`

### Unsupported SSM parameter types<a name="aws-ssm-parameter-types-unsupported"></a>

AWS CloudFormation doesn't support the following `SSM` parameter type:
+ Lists of `SSM` parameter types—for example: `List<AWS::SSM::Parameter::Value<String>>`

In addition, AWS CloudFormation does not support defining template parameters as `SecureString` Systems Manager parameter types\. However, you can specify Secure Strings as parameter *values* for certain resources by using dynamic parameter patterns\. For more information, see [Using dynamic references to specify template values](dynamic-references.md)\.

## Grouping and sorting parameters in the AWS CloudFormation console<a name="parameters-section-structure-grouping"></a>

When you use the AWS CloudFormation console to create or update a stack, the console alphabetically lists input parameters by their logical ID\. To override the default ordering, you can use the `AWS::CloudFormation::Interface` metadata key\. By grouping and ordering parameters, you make it easier for users to specify parameter values\. For example, you could group all VPC\-related parameters so that they aren't scattered throughout an alphabetical list\.

In the metadata key, you can specify the groups to create, the parameters to include in each group, and the order in which the console shows each parameter within its group\. You can also define friendly parameter names so that the console shows descriptive names instead of logical IDs\. All parameters that you reference in the metadata key must be declared in the `Parameters` section of the template\.

For more information and an example of the `AWS::CloudFormation::Interface` metadata key, see [AWS::CloudFormation::Interface](aws-resource-cloudformation-interface.md)\.

## Examples<a name="parameters-section-examples"></a>

### Basic input parameters<a name="parameters-section-examples-basic"></a>

The following example `Parameters` section declares two parameters\. The `DBPort` parameter is of type `Number` with a default of `3306`\. The minimum value that can be specified is `1150`, and the maximum value that can be specified is `65535`\. The `DBPwd` parameter is of type `String` with no default value\. The `NoEcho` property is set to `true` to prevent *describe stack* calls, such as the `aws cloudformation describe-stacks` AWS CLI command, from returning the parameter value\. The minimum length that can be specified is `1`, and the maximum length that can be specified is `41`\. The pattern allows lowercase and uppercase alphabetic characters and numerals\.

#### JSON<a name="parameters-section-structure-examples-example.json"></a>

```
"Parameters" : {
  "DBPort" : {
    "Default" : "3306",
    "Description" : "TCP/IP port for the database",
    "Type" : "Number",
    "MinValue" : "1150",
    "MaxValue" : "65535"
  },
  "DBPwd" : {
    "NoEcho" : "true",
    "Description" : "The database admin account password",
    "Type" : "String",
    "MinLength" : "1",
    "MaxLength" : "41",
    "AllowedPattern" : "^[a-zA-Z0-9]*$"
  }
}
```

#### YAML<a name="parameters-section-structure-examples-example.yaml"></a>

```
Parameters: 
  DBPort: 
    Default: 3306
    Description: TCP/IP port for the database
    Type: Number
    MinValue: 1150
    MaxValue: 65535
  DBPwd: 
    NoEcho: true
    Description: The database admin account password
    Type: String
    MinLength: 1
    MaxLength: 41
    AllowedPattern: ^[a-zA-Z0-9]*$
```

### AWS\-specific parameter types<a name="parameters-section-structure-aws-specific-types"></a>

When you use AWS\-specific parameter types, a user who uses your template to create or update a stack must specify existing AWS values that are in the user's account and in the region for the current stack\. AWS\-specific parameter types help ensure that input values for these types exist and are correct before AWS CloudFormation creates or updates any resources\. For example, if you use the `AWS::EC2::KeyPair::KeyName` parameter type, AWS CloudFormation validates the input value against users' existing key pair names before it creates any resources, such as Amazon EC2 instances\.

If a user uses the AWS Management Console, AWS CloudFormation [prepopulates AWS\-specific parameter types with valid values](cfn-using-console-create-stack-parameters.md)\. That way the user doesn't have to remember and correctly enter a specific name or ID\. They would just select one or more values from a drop\-down list\. Also, depending on the parameter type, users can search for values by ID, name, or Name tag value\. For more information, see [Specifying stack name and parameters](cfn-using-console-create-stack-parameters.md)\.

The following example declares two parameters with the types `AWS::EC2::KeyPair::KeyName` and `AWS::EC2::Subnet::Id`\. These types limit valid values to existing key pair names and subnet IDs\. Because the `mySubnetIDs` parameter is specified as a list, a user can specify one or more subnet IDs\.

#### JSON<a name="parameters-section-structure-examples-example2.json"></a>

```
"Parameters" : {
  "myKeyPair" : {
    "Description" : "Amazon EC2 Key Pair",
    "Type" : "AWS::EC2::KeyPair::KeyName"
  },
  "mySubnetIDs" : {
    "Description" : "Subnet IDs",
    "Type" : "List<AWS::EC2::Subnet::Id>"
  }
}
```

#### YAML<a name="parameters-section-structure-examples-example2.yaml"></a>

```
Parameters: 
  myKeyPair: 
    Description: Amazon EC2 Key Pair
    Type: "AWS::EC2::KeyPair::KeyName"
  mySubnetIDs: 
    Description: Subnet IDs
    Type: "List<AWS::EC2::Subnet::Id>"
```

#### AWS CLI and API support<a name="parameters-section-cli-support"></a>

Currently, users can't use the AWS CLI or AWS CloudFormation API to view a list of valid values for AWS\-specific parameters\. However, they can view information about each parameter, such as the parameter type, by using the [aws cloudformation get\-template\-summary](https://docs.aws.amazon.com/cli/latest/reference/cloudformation/get-template-summary.html) command or [https://docs.aws.amazon.com/AWSCloudFormation/latest/APIReference/API_GetTemplateSummary.html](https://docs.aws.amazon.com/AWSCloudFormation/latest/APIReference/API_GetTemplateSummary.html) API\.

### Comma\-delimited list parameter type<a name="parameters-section-structure-comma-list-type"></a>

You can use the `CommaDelimitedList` parameter type to specify multiple string values in a single parameter\. That way, you can use a single parameter instead of many different parameters to specify multiple values\. For example, if you create three different subnets with their own CIDR blocks, you could use three different parameters to specify three different CIDR blocks\. But it's simpler just to use a single parameter that takes a list of three CIDR blocks, as shown in the following snippet:

#### JSON<a name="parameters-section-structure-examples-example3.json"></a>

```
"Parameters" : {
  "DbSubnetIpBlocks": {
    "Description": "Comma-delimited list of three CIDR blocks",
    "Type": "CommaDelimitedList",
    "Default": "10.0.48.0/24, 10.0.112.0/24, 10.0.176.0/24"
  }
}
```

#### YAML<a name="parameters-section-structure-examples-example3.yaml"></a>

```
Parameters: 
  DbSubnetIpBlocks: 
    Description: "Comma-delimited list of three CIDR blocks"
    Type: CommaDelimitedList
    Default: "10.0.48.0/24, 10.0.112.0/24, 10.0.176.0/24"
```

#### Return a value from a comma\-delimited list parameter<a name="parameters-section-structure-examples-return-value"></a>

To refer to a specific value in a list, use the `Fn::Select` intrinsic function in the `Resources` section of your template\. You pass the index value of the object that you want and a list of objects, as shown in the following snippet:

##### JSON<a name="parameters-section-structure-examples-example4.json"></a>

```
"DbSubnet1" : {
  "Type" : "AWS::EC2::Subnet",
  "Properties" : {
    "AvailabilityZone" : {"Fn::Join" : ["",[ { "Ref" : "AWS::Region" }, { "Fn::Select" : [ "0", {"Ref" : "VpcAzs"} ] } ] ]} ,
    "VpcId" :  { "Ref" : "VPC" },
    "CidrBlock" : { "Fn::Select" : [ "0", {"Ref" : "DbSubnetIpBlocks"} ] }
  }
},
"DbSubnet2" : {
  "Type" : "AWS::EC2::Subnet",
  "Properties" : {
    "AvailabilityZone" : {"Fn::Join" : ["",[ { "Ref" : "AWS::Region" }, { "Fn::Select" : [ "1", {"Ref" : "VpcAzs"} ] } ] ]} ,
    "VpcId" : { "Ref" : "VPC" },
    "CidrBlock" : { "Fn::Select" : [ "1", {"Ref" : "DbSubnetIpBlocks"} ] }
  }
},
"DbSubnet3" : {
  "Type" : "AWS::EC2::Subnet",
  "Properties" : {
    "AvailabilityZone" : {"Fn::Join" : ["",[ { "Ref" : "AWS::Region" }, { "Fn::Select" : [ "2", {"Ref" : "VpcAzs"} ] } ] ]} ,
    "VpcId" : { "Ref" : "VPC" },
    "CidrBlock" : { "Fn::Select" : [ "2", {"Ref" : "DbSubnetIpBlocks"} ] }
  }
}
```

##### YAML<a name="parameters-section-structure-examples-example4.yaml"></a>

```
DbSubnet1:
  Type: AWS::EC2::Subnet
  Properties:
    AvailabilityZone: !Sub
      - "${AWS::Region}${AZ}"
      - AZ: !Select [0, !Ref VpcAzs]
    VpcId: !Ref VPC
    CidrBlock: !Select [0, !Ref DbSubnetIpBlocks]
DbSubnet2: 
  Type: AWS::EC2::Subnet
  Properties:
    AvailabilityZone: !Sub
      - "${AWS::Region}${AZ}"
      - AZ: !Select [1, !Ref VpcAzs]
    VpcId: !Ref VPC
    CidrBlock: !Select [1, !Ref DbSubnetIpBlocks]
DbSubnet3: 
  Type: AWS::EC2::Subnet
  Properties:
    AvailabilityZone: !Sub
      - "${AWS::Region}${AZ}"
      - AZ: !Select [2, !Ref VpcAzs]
    VpcId: !Ref VPC
    CidrBlock: !Select [2, !Ref DbSubnetIpBlocks]
```

### SSM parameter types<a name="parameters-section-ssm-examples"></a>



#### AWS::SSM::Parameter::Value<String> type<a name="parameters-section-ssm-examples-example1"></a>

The following template declares an `AWS::SSM::Parameter::Value<String>` parameter type\.

##### JSON<a name="parameters-ssm-string.json"></a>

```
{
  "Parameters": {
    "InstanceType": {
      "Type": "AWS::SSM::Parameter::Value<String>"
    }
  },
  "Resources": {
    "Instance": {
      "Type": "AWS::EC2::Instance",
      "Properties": {
        "InstanceType": {
          "Ref": "InstanceType"
        }
      }
    }
  }
}
```

##### YAML<a name="parameters-ssm-string.yaml"></a>

```
Parameters: 
  InstanceType: 
    Type: 'AWS::SSM::Parameter::Value<String>'
Resources: 
  Instance: 
    Type: 'AWS::EC2::Instance'
    Properties: 
      InstanceType: !Ref InstanceType
```

The following command creates a stack based on the example template\. It provides the Systems Manager parameter key \(`myInstanceType`\) as the value for the `InstanceType` template parameter\. This assumes that the `myInstanceType` parameter exists in Parameter Store under the caller's AWS account\.

```
aws cloudformation create-stack --stack-name S1 --template-body example template --parameters ParameterKey=InstanceType,ParameterValue=myInstanceType
```

 

#### AWS::SSM::Parameter::Value<AWS::EC2::Image::Id> type<a name="parameters-section-ssm-examples-example2"></a>

The following template declares an `AWS::SSM::Parameter::Value<AWS::EC2::Image::Id>` parameter type\.

##### JSON<a name="parameters-ssm-ec2keypair.json"></a>

```
{
  "Parameters": {
    "ImageId": {
      "Type": "AWS::SSM::Parameter::Value<AWS::EC2::Image::Id>"
    }
  },
  "Resources": {
    "Instance": {
      "Type": "AWS::EC2::Instance",
      "Properties": {
        "ImageId": {
          "Ref": "ImageId"
        }
      }
    }
  }
}
```

##### YAML<a name="parameters-ssm-ec2keypair.yaml"></a>

```
Parameters: 
  ImageId: 
    Type: 'AWS::SSM::Parameter::Value<AWS::EC2::Image::Id>'
Resources: 
  Instance: 
    Type: 'AWS::EC2::Instance'
    Properties:
      ImageId: !Ref ImageId
```

The following command creates a stack based on the example template\. It provides the Systems Manager parameter key \(`myLatestAMI`\) as the value for the `ImageId` template parameter\. This assumes that the `myLatestAMI` parameter exists in Parameter Store under the caller's AWS account\.

```
aws cloudformation create-stack --stack-name S2 --template-body example template --parameters ParameterKey=ImageId,ParameterValue=myLatestAMI
```