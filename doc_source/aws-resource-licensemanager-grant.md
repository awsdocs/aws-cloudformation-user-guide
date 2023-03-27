# AWS::LicenseManager::Grant<a name="aws-resource-licensemanager-grant"></a>

Specifies a grant\.

A grant shares the use of license entitlements with specific AWS accounts\. For more information, see [Granted licenses](https://docs.aws.amazon.com/license-manager/latest/userguide/granted-licenses.html) in the *AWS License Manager User Guide*\.

## Syntax<a name="aws-resource-licensemanager-grant-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-licensemanager-grant-syntax.json"></a>

```
{
  "Type" : "AWS::LicenseManager::Grant",
  "Properties" : {
      "[AllowedOperations](#cfn-licensemanager-grant-allowedoperations)" : [ String, ... ],
      "[GrantName](#cfn-licensemanager-grant-grantname)" : String,
      "[HomeRegion](#cfn-licensemanager-grant-homeregion)" : String,
      "[LicenseArn](#cfn-licensemanager-grant-licensearn)" : String,
      "[Principals](#cfn-licensemanager-grant-principals)" : [ String, ... ],
      "[Status](#cfn-licensemanager-grant-status)" : String
    }
}
```

### YAML<a name="aws-resource-licensemanager-grant-syntax.yaml"></a>

```
Type: AWS::LicenseManager::Grant
Properties: 
  [AllowedOperations](#cfn-licensemanager-grant-allowedoperations): 
    - String
  [GrantName](#cfn-licensemanager-grant-grantname): String
  [HomeRegion](#cfn-licensemanager-grant-homeregion): String
  [LicenseArn](#cfn-licensemanager-grant-licensearn): String
  [Principals](#cfn-licensemanager-grant-principals): 
    - String
  [Status](#cfn-licensemanager-grant-status): String
```

## Properties<a name="aws-resource-licensemanager-grant-properties"></a>

`AllowedOperations`  <a name="cfn-licensemanager-grant-allowedoperations"></a>
Allowed operations for the grant\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`GrantName`  <a name="cfn-licensemanager-grant-grantname"></a>
Grant name\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`HomeRegion`  <a name="cfn-licensemanager-grant-homeregion"></a>
Home Region of the grant\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LicenseArn`  <a name="cfn-licensemanager-grant-licensearn"></a>
License ARN\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Principals`  <a name="cfn-licensemanager-grant-principals"></a>
The grant principals\. You can specify one of the following as an Amazon Resource Name \(ARN\):  
+ An AWS account, which includes only the account specified\.
+ An organizational unit \(OU\), which includes all accounts in the OU\.
+ An organization, which will include all accounts across your organization\.
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Status`  <a name="cfn-licensemanager-grant-status"></a>
Granted license status\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-licensemanager-grant-return-values"></a>

### Ref<a name="aws-resource-licensemanager-grant-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the ID of the grant\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-licensemanager-grant-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-licensemanager-grant-return-values-fn--getatt-fn--getatt"></a>

`GrantArn`  <a name="GrantArn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the grant\.

`Version`  <a name="Version-fn::getatt"></a>
The grant version\.