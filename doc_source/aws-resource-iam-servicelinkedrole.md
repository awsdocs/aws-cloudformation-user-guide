# AWS::IAM::ServiceLinkedRole<a name="aws-resource-iam-servicelinkedrole"></a>

Creates an IAM role that is linked to a specific AWS service\. The service controls the attached policies and when the role can be deleted\. This helps ensure that the service is not broken by an unexpectedly changed or deleted role, which could put your AWS resources into an unknown state\. Allowing the service to control the role helps improve service stability and proper cleanup when a service and its role are no longer needed\. For more information, see [Using Service\-Linked Roles](https://docs.aws.amazon.com/IAM/latest/UserGuide/using-service-linked-roles.html) in the *IAM User Guide*\. 

To attach a policy to this service\-linked role, you must make the request using the AWS service that depends on this role\.

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
Type: AWS::IAM::ServiceLinkedRole
Properties: 
  [AWSServiceName](#cfn-iam-servicelinkedrole-awsservicename): String
  [CustomSuffix](#cfn-iam-servicelinkedrole-customsuffix): String
  [Description](#cfn-iam-servicelinkedrole-description): String
```

## Properties<a name="aws-resource-iam-servicelinkedrole-properties"></a>

`AWSServiceName`  <a name="cfn-iam-servicelinkedrole-awsservicename"></a>
The service principal for the AWS service to which this role is attached\. You use a string similar to a URL but without the http:// in front\. For example: `elasticbeanstalk.amazonaws.com`\.   
Service principals are unique and case\-sensitive\. To find the exact service principal for your service\-linked role, see [AWS Services That Work with IAM](https://docs.aws.amazon.com/IAM/latest/UserGuide/reference_aws-services-that-work-with-iam.html) in the *IAM User Guide*\. Look for the services that have **Yes **in the **Service\-Linked Role** column\. Choose the **Yes** link to view the service\-linked role documentation for that service\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `128`  
*Pattern*: `[\w+=,.@-]+`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`CustomSuffix`  <a name="cfn-iam-servicelinkedrole-customsuffix"></a>
  
A string that you provide, which is combined with the service\-provided prefix to form the complete role name\. If you make multiple requests for the same service, then you must supply a different `CustomSuffix` for each request\. Otherwise the request fails with a duplicate role name error\. For example, you could add `-1` or `-debug` to the suffix\.  
Some services do not support the `CustomSuffix` parameter\. If you provide an optional suffix and the operation fails, try the operation again without the suffix\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `64`  
*Pattern*: `[\w+=,.@-]+`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Description`  <a name="cfn-iam-servicelinkedrole-description"></a>
The description of the role\.  
*Required*: No  
*Type*: String  
*Maximum*: `1000`  
*Pattern*: `[\p{L}\p{M}\p{Z}\p{S}\p{N}\p{P}]*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-iam-servicelinkedrole-return-values"></a>

### Ref<a name="aws-resource-iam-servicelinkedrole-return-values-ref"></a>

When the logical ID of this resource is provided to the `Ref` intrinsic function, `Ref` returns the resource name\.

For example:

 `{ "Ref": "BasicSLR" }` 

For the `AWS::IAM::ServiceLinkedRole` resource with the logical ID `BasicSLR`, `Ref` will return the name of the service\-linked role\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-resource-iam-servicelinkedrole--examples"></a>



### Create an IAM Service\-Linked Role for Auto Scaling<a name="aws-resource-iam-servicelinkedrole--examples--Create_an_IAM_Service-Linked_Role_for_Auto_Scaling"></a>

The following example creates a service\-linked role that can be assumed by the Auto Scaling service\.

#### JSON<a name="aws-resource-iam-servicelinkedrole--examples--Create_an_IAM_Service-Linked_Role_for_Auto_Scaling--json"></a>

```
{
    "Description": "SLR resource create test - Auto Scaling",
    "Resources": {
        "BasicSLR": {
            "Type": "AWS::IAM::ServiceLinkedRole",
            "Properties": {
                "AWSServiceName": "autoscaling.amazonaws.com",
                "Description": "Test SLR description",
                "CustomSuffix": "TestSuffix"
            }
        }
    },
    "Outputs": {
        "SLRId": {
            "Value": {
                "Ref": "BasicSLR"
            }
        }
    }
}
```

#### YAML<a name="aws-resource-iam-servicelinkedrole--examples--Create_an_IAM_Service-Linked_Role_for_Auto_Scaling--yaml"></a>

```
Description: SLR resource create test - Auto Scaling
Resources:
  BasicSLR:
    Type: 'AWS::IAM::ServiceLinkedRole'
    Properties:
      AWSServiceName: autoscaling.amazonaws.com
      Description: Test SLR description
      CustomSuffix: TestSuffix
Outputs:
  SLRId:
    Value: !Ref BasicSLR
```