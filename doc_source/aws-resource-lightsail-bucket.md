# AWS::Lightsail::Bucket<a name="aws-resource-lightsail-bucket"></a>

The `AWS::Lightsail::Bucket` resource specifies a bucket\.

## Syntax<a name="aws-resource-lightsail-bucket-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-lightsail-bucket-syntax.json"></a>

```
{
  "Type" : "AWS::Lightsail::Bucket",
  "Properties" : {
      "[AccessRules](#cfn-lightsail-bucket-accessrules)" : AccessRules,
      "[BucketName](#cfn-lightsail-bucket-bucketname)" : String,
      "[BundleId](#cfn-lightsail-bucket-bundleid)" : String,
      "[ObjectVersioning](#cfn-lightsail-bucket-objectversioning)" : Boolean,
      "[ReadOnlyAccessAccounts](#cfn-lightsail-bucket-readonlyaccessaccounts)" : [ String, ... ],
      "[ResourcesReceivingAccess](#cfn-lightsail-bucket-resourcesreceivingaccess)" : [ String, ... ],
      "[Tags](#cfn-lightsail-bucket-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-lightsail-bucket-syntax.yaml"></a>

```
Type: AWS::Lightsail::Bucket
Properties: 
  [AccessRules](#cfn-lightsail-bucket-accessrules): 
    AccessRules
  [BucketName](#cfn-lightsail-bucket-bucketname): String
  [BundleId](#cfn-lightsail-bucket-bundleid): String
  [ObjectVersioning](#cfn-lightsail-bucket-objectversioning): Boolean
  [ReadOnlyAccessAccounts](#cfn-lightsail-bucket-readonlyaccessaccounts): 
    - String
  [ResourcesReceivingAccess](#cfn-lightsail-bucket-resourcesreceivingaccess): 
    - String
  [Tags](#cfn-lightsail-bucket-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-lightsail-bucket-properties"></a>

`AccessRules`  <a name="cfn-lightsail-bucket-accessrules"></a>
An object that describes the access rules for the bucket\.  
*Required*: No  
*Type*: [AccessRules](aws-properties-lightsail-bucket-accessrules.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`BucketName`  <a name="cfn-lightsail-bucket-bucketname"></a>
The name of the bucket\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`BundleId`  <a name="cfn-lightsail-bucket-bundleid"></a>
The bundle ID for the bucket \(for example, `small_1_0`\)\.  
A bucket bundle specifies the monthly cost, storage space, and data transfer quota for a bucket\.  
*Required*: Yes  
*Type*: String  
*Pattern*: `.*\S.*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ObjectVersioning`  <a name="cfn-lightsail-bucket-objectversioning"></a>
Indicates whether object versioning is enabled for the bucket\.  
The following options can be configured:  
+  `Enabled` \- Object versioning is enabled\.
+  `Suspended` \- Object versioning was previously enabled but is currently suspended\. Existing object versions are retained\.
+  `NeverEnabled` \- Object versioning has never been enabled\.
*Required*: No  
*Type*: Boolean  
*Pattern*: `.*\S.*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ReadOnlyAccessAccounts`  <a name="cfn-lightsail-bucket-readonlyaccessaccounts"></a>
An array of AWS account IDs that have read\-only access to the bucket\.  
*Required*: No  
*Type*: List of String  
*Maximum*: `10`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ResourcesReceivingAccess`  <a name="cfn-lightsail-bucket-resourcesreceivingaccess"></a>
An array of Lightsail instances that have access to the bucket\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-lightsail-bucket-tags"></a>
An array of key\-value pairs to apply to this resource\.  
For more information, see [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html) in the *AWS CloudFormation User Guide*\.  
The `Value` of `Tags` is optional for Lightsail resources\.
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-lightsail-bucket-return-values"></a>

### Ref<a name="aws-resource-lightsail-bucket-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns a unique identifier for this resource\.

### Fn::GetAtt<a name="aws-resource-lightsail-bucket-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-lightsail-bucket-return-values-fn--getatt-fn--getatt"></a>

`AbleToUpdateBundle`  <a name="AbleToUpdateBundle-fn::getatt"></a>
A Boolean value indicating whether the bundle that is currently applied to your distribution can be changed to another bundle\.

`BucketArn`  <a name="BucketArn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the bucket\.

`Url`  <a name="Url-fn::getatt"></a>
The URL of the bucket\.