# AWS::Cloud9::EnvironmentEC2<a name="aws-resource-cloud9-environmentec2"></a>

The `AWS::Cloud9::EnvironmentEC2` resource creates an Amazon EC2 development environment in AWS Cloud9\. For more information, see [Creating an Environment](https://docs.aws.amazon.com/cloud9/latest/user-guide/create-environment.html) in the *AWS Cloud9 User Guide*\.

## Syntax<a name="aws-resource-cloud9-environmentec2-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-cloud9-environmentec2-syntax.json"></a>

```
{
  "Type" : "AWS::Cloud9::EnvironmentEC2",
  "Properties" : {
      "[AutomaticStopTimeMinutes](#cfn-cloud9-environmentec2-automaticstoptimeminutes)" : Integer,
      "[Description](#cfn-cloud9-environmentec2-description)" : String,
      "[InstanceType](#cfn-cloud9-environmentec2-instancetype)" : String,
      "[Name](#cfn-cloud9-environmentec2-name)" : String,
      "[OwnerArn](#cfn-cloud9-environmentec2-ownerarn)" : String,
      "[Repositories](#cfn-cloud9-environmentec2-repositories)" : [ [Repository](aws-properties-cloud9-environmentec2-repository.md), ... ],
      "[SubnetId](#cfn-cloud9-environmentec2-subnetid)" : String
    }
}
```

### YAML<a name="aws-resource-cloud9-environmentec2-syntax.yaml"></a>

```
Type: AWS::Cloud9::EnvironmentEC2
Properties:
  [AutomaticStopTimeMinutes](#cfn-cloud9-environmentec2-automaticstoptimeminutes): Integer
  [Description](#cfn-cloud9-environmentec2-description): String
  [InstanceType](#cfn-cloud9-environmentec2-instancetype): String
  [Name](#cfn-cloud9-environmentec2-name): String
  [OwnerArn](#cfn-cloud9-environmentec2-ownerarn): String
  [Repositories](#cfn-cloud9-environmentec2-repositories):
    - [Repository](aws-properties-cloud9-environmentec2-repository.md)
  [SubnetId](#cfn-cloud9-environmentec2-subnetid): String
```

## Properties<a name="aws-resource-cloud9-environmentec2-properties"></a>

`AutomaticStopTimeMinutes`  <a name="cfn-cloud9-environmentec2-automaticstoptimeminutes"></a>
The number of minutes until the running instance is shut down after the environment was last used\.
*Required*: No
*Type*: Integer
*Maximum*: `20160`
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Description`  <a name="cfn-cloud9-environmentec2-description"></a>
The description of the environment to create\.
*Required*: No
*Type*: String
*Maximum*: `200`
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`InstanceType`  <a name="cfn-cloud9-environmentec2-instancetype"></a>
The type of instance to connect to the environment \(for example, `t2.micro`\)\.
*Required*: Yes
*Type*: String
*Minimum*: `5`
*Maximum*: `20`
*Pattern*: `^[a-z][1-9][.][a-z0-9]+$`
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Name`  <a name="cfn-cloud9-environmentec2-name"></a>
The name of the environment\.
*Required*: No
*Type*: String
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`OwnerArn`  <a name="cfn-cloud9-environmentec2-ownerarn"></a>
The Amazon Resource Name \(ARN\) of the environment owner\. This ARN can be the ARN of any AWS Identity and Access Management \(IAM\) principal\. If this value is not specified, the ARN defaults to this environment's creator\.
*Required*: No
*Type*: String
*Pattern*: `arn:aws:(iam|sts)::\d+:(root|user|federated-user|assumed-role)\/?\S*`
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Repositories`  <a name="cfn-cloud9-environmentec2-repositories"></a>
Any AWS CodeCommit source code repositories to be cloned into the development environment\.
*Required*: No
*Type*: List of [Repository](aws-properties-cloud9-environmentec2-repository.md)
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SubnetId`  <a name="cfn-cloud9-environmentec2-subnetid"></a>
The ID of the subnet in Amazon Virtual Private Cloud \(Amazon VPC\) that AWS Cloud9 will use to communicate with the Amazon Elastic Compute Cloud \(Amazon EC2\) instance\.
*Required*: No
*Type*: String
*Minimum*: `5`
*Maximum*: `30`
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return Values<a name="aws-resource-cloud9-environmentec2-return-values"></a>

### Ref<a name="aws-resource-cloud9-environmentec2-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the ID of the development environment, such as `2bc3642873c342e485f7e0c561234567`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-cloud9-environmentec2-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-cloud9-environmentec2-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the development environment, such as `arn:aws:cloud9:us-east-2:123456789012:environment:2bc3642873c342e485f7e0c561234567`\.

`Name`  <a name="Name-fn::getatt"></a>
The name of the environment\.
