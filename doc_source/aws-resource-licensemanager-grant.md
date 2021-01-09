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
      "[AllowedOperations](#cfn-licensemanager-grant-allowedoperations)" : AllowedOperationList,
      "[ClientToken](#cfn-licensemanager-grant-clienttoken)" : String,
      "[Filters](#cfn-licensemanager-grant-filters)" : FilterList,
      "[GrantArns](#cfn-licensemanager-grant-grantarns)" : ArnList,
      "[GrantedOperations](#cfn-licensemanager-grant-grantedoperations)" : AllowedOperationList,
      "[GranteePrincipalArn](#cfn-licensemanager-grant-granteeprincipalarn)" : String,
      "[GrantName](#cfn-licensemanager-grant-grantname)" : String,
      "[GrantStatus](#cfn-licensemanager-grant-grantstatus)" : String,
      "[HomeRegion](#cfn-licensemanager-grant-homeregion)" : String,
      "[LicenseArn](#cfn-licensemanager-grant-licensearn)" : String,
      "[MaxResults](#cfn-licensemanager-grant-maxresults)" : Integer,
      "[NextToken](#cfn-licensemanager-grant-nexttoken)" : String,
      "[ParentArn](#cfn-licensemanager-grant-parentarn)" : String,
      "[Principals](#cfn-licensemanager-grant-principals)" : ArnList,
      "[SourceVersion](#cfn-licensemanager-grant-sourceversion)" : String,
      "[Status](#cfn-licensemanager-grant-status)" : String,
      "[StatusReason](#cfn-licensemanager-grant-statusreason)" : String,
      "[Tags](#cfn-licensemanager-grant-tags)" : TagList,
      "[Version](#cfn-licensemanager-grant-version)" : String
    }
}
```

### YAML<a name="aws-resource-licensemanager-grant-syntax.yaml"></a>

```
Type: AWS::LicenseManager::Grant
Properties: 
  [AllowedOperations](#cfn-licensemanager-grant-allowedoperations): 
    AllowedOperationList
  [ClientToken](#cfn-licensemanager-grant-clienttoken): String
  [Filters](#cfn-licensemanager-grant-filters): 
    FilterList
  [GrantArns](#cfn-licensemanager-grant-grantarns): 
    ArnList
  [GrantedOperations](#cfn-licensemanager-grant-grantedoperations): 
    AllowedOperationList
  [GranteePrincipalArn](#cfn-licensemanager-grant-granteeprincipalarn): String
  [GrantName](#cfn-licensemanager-grant-grantname): String
  [GrantStatus](#cfn-licensemanager-grant-grantstatus): String
  [HomeRegion](#cfn-licensemanager-grant-homeregion): String
  [LicenseArn](#cfn-licensemanager-grant-licensearn): String
  [MaxResults](#cfn-licensemanager-grant-maxresults): Integer
  [NextToken](#cfn-licensemanager-grant-nexttoken): String
  [ParentArn](#cfn-licensemanager-grant-parentarn): String
  [Principals](#cfn-licensemanager-grant-principals): 
    ArnList
  [SourceVersion](#cfn-licensemanager-grant-sourceversion): String
  [Status](#cfn-licensemanager-grant-status): String
  [StatusReason](#cfn-licensemanager-grant-statusreason): String
  [Tags](#cfn-licensemanager-grant-tags): 
    TagList
  [Version](#cfn-licensemanager-grant-version): String
```

## Properties<a name="aws-resource-licensemanager-grant-properties"></a>

`AllowedOperations`  <a name="cfn-licensemanager-grant-allowedoperations"></a>
Allowed operations for the grant\.  
*Required*: No  
*Type*: [AllowedOperationList](aws-properties-licensemanager-grant-allowedoperationlist.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ClientToken`  <a name="cfn-licensemanager-grant-clienttoken"></a>
Unique, case\-sensitive identifier that you provide to ensure the idempotency of the request\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Filters`  <a name="cfn-licensemanager-grant-filters"></a>
Filters to scope the results\. The following filters are supported:  
+  `LicenseARN` 
+  `Status` 
*Required*: No  
*Type*: [FilterList](aws-properties-licensemanager-grant-filterlist.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`GrantArns`  <a name="cfn-licensemanager-grant-grantarns"></a>
Amazon Resource Names \(ARNs\) of the grants\.  
*Required*: No  
*Type*: [ArnList](aws-properties-licensemanager-grant-arnlist.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`GrantedOperations`  <a name="cfn-licensemanager-grant-grantedoperations"></a>
Granted operations\.  
*Required*: No  
*Type*: [AllowedOperationList](aws-properties-licensemanager-grant-allowedoperationlist.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`GranteePrincipalArn`  <a name="cfn-licensemanager-grant-granteeprincipalarn"></a>
The grantee principal ARN\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`GrantName`  <a name="cfn-licensemanager-grant-grantname"></a>
Grant name\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`GrantStatus`  <a name="cfn-licensemanager-grant-grantstatus"></a>
Grant status\.  
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

`MaxResults`  <a name="cfn-licensemanager-grant-maxresults"></a>
Maximum number of results to return in a single call\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NextToken`  <a name="cfn-licensemanager-grant-nexttoken"></a>
Token for the next set of results\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ParentArn`  <a name="cfn-licensemanager-grant-parentarn"></a>
Parent ARN\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Principals`  <a name="cfn-licensemanager-grant-principals"></a>
The grant principals\.  
*Required*: No  
*Type*: [ArnList](aws-properties-licensemanager-grant-arnlist.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SourceVersion`  <a name="cfn-licensemanager-grant-sourceversion"></a>
Current version of the grant\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Status`  <a name="cfn-licensemanager-grant-status"></a>
Granted license status\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StatusReason`  <a name="cfn-licensemanager-grant-statusreason"></a>
Grant status reason\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-licensemanager-grant-tags"></a>
One or more tags\.  
*Required*: No  
*Type*: [TagList](aws-properties-licensemanager-grant-taglist.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Version`  <a name="cfn-licensemanager-grant-version"></a>
Grant version\.  
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