# AWS::IAM::ServiceLinkedRole<a name="aws-resource-iam-servicelinkedrole"></a>

The `AWS::IAM::ServiceLinkedRole` resource creates a service\-linked role in AWS Identity and Access Management \(IAM\)\. A service\-linked role is a unique type of IAM role that is linked directly to an AWS service\. Service\-linked roles are predefined by the service and include all the permissions that the service requires to call other AWS services on your behalf\. The linked service also defines how you create, modify, and delete a service\-linked role\. For more information, see [CreateServiceLinkedRole](https://docs.aws.amazon.com/IAM/latest/APIReference/API_CreateServiceLinkedRole.html) in the *IAM API Reference* or [Using Service\-Linked Roles](https://docs.aws.amazon.com/IAM/latest/UserGuide/using-service-linked-roles.html) in the *IAM User Guide*\. 

**Topics**
+ [Syntax](#aws-resource-iam-servicelinkedrole-syntax)
+ [Properties](#aws-resource-iam-servicelinkedrole-properties)
+ [Examples](#aws-resource-iam-servicelinkedrole-examples)
+ [See Also](#aws-resource-iam-servicelinkedrole-seealso)

## Syntax<a name="aws-resource-iam-servicelinkedrole-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-iam-servicelinkedrole-syntax.json"></a>

```
{
  "Type" : "AWS::IAM::ServiceLinkedRole",
  "Properties" : {
    
    "[AWSServiceName](#cfn-iam-servicelinkedrole-awsservicename)" : String,
    "[CustomSuffix](#cfn-iam-servicelinkedrole-customsuffix)" : String,
    "[Description](#cfn-iam-servicelinkedrole-description)" : String
  }
}
```

### YAML<a name="aws-resource-iam-servicelinkedrole-syntax.yaml"></a>

```
Type: "AWS::IAM::ServiceLinkedRole"
Properties:
  [AWSServiceName](#cfn-iam-servicelinkedrole-awsservicename): String
  [CustomSuffix](#cfn-iam-servicelinkedrole-customsuffix): String
  [Description](#cfn-iam-servicelinkedrole-description): String
```

## Properties<a name="aws-resource-iam-servicelinkedrole-properties"></a>

`AWSServiceName`  <a name="cfn-iam-servicelinkedrole-awsservicename"></a>
 The service principal for the AWS service to which this role is attached\. You use a string similar to a URL but without the `http://` in front\. For example: `elasticbeanstalk.amazonaws.com`\.   
Service principals are unique and case sensitive\. To find the exact service principal for your service\-linked role, see [AWS Services That Work with IAM](https://docs.aws.amazon.com/IAM/latest/UserGuide/reference_aws-services-that-work-with-iam.html) in the *IAM User Guide*\. Look for the services that have **Yes **in the **Service\-Linked Role** column\. Choose the **Yes** link to view the service\-linked role documentation for that service\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`CustomSuffix`  <a name="cfn-iam-servicelinkedrole-customsuffix"></a>
 A string that you provide, which is combined with the service\-provided prefix to form the complete role name\. If you make multiple requests for the same service, then you must supply a different `CustomSuffix` for each request\. Otherwise the request fails with a duplicate role name error\. For example, you could add `-1` or `-debug` to the suffix\.  
Some services do not support the `CustomSuffix` parameter\. If you provide an optional suffix and the operation fails, try the operation again without the suffix\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`Description`  <a name="cfn-iam-servicelinkedrole-description"></a>
The description of the role\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

## Examples<a name="aws-resource-iam-servicelinkedrole-examples"></a>

### Create an IAM Service\-Linked Role for Auto Scaling<a name="aws-resource-iam-servicelinkedrole-example1"></a>

The following example creates a service\-linked role that can be assumed by the Auto Scaling service\.

#### YAML<a name="aws-resource-iam-servicelinkedrole-example1.yaml"></a>

```
---
Description: "SLR resource create test - Auto Scaling"
Resources:
  BasicSLR:
    Type: "AWS::IAM::ServiceLinkedRole"
    Properties:
      AWSServiceName: "autoscaling.amazonaws.com"
      Description: "Test SLR description"
      CustomSuffix: "TestSuffix"
Outputs:
  SLRId:
    Value: !Ref BasicSLR
```

## See Also<a name="aws-resource-iam-servicelinkedrole-seealso"></a>
+ [CreateServiceLinkedRole](https://docs.aws.amazon.com/IAM/latest/APIReference/API_CreateServiceLinkedRole.html) in the *IAM API Reference*
+ [Using Service\-Linked Roles](https://docs.aws.amazon.com/IAM/latest/UserGuide/using-service-linked-roles.html) in the *IAM User Guide*