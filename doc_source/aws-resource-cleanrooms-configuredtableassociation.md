# AWS::CleanRooms::ConfiguredTableAssociation<a name="aws-resource-cleanrooms-configuredtableassociation"></a>

Creates a configured table association\. A configured table association links a configured table with a collaboration\.

## Syntax<a name="aws-resource-cleanrooms-configuredtableassociation-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-cleanrooms-configuredtableassociation-syntax.json"></a>

```
{
  "Type" : "AWS::CleanRooms::ConfiguredTableAssociation",
  "Properties" : {
      "[ConfiguredTableIdentifier](#cfn-cleanrooms-configuredtableassociation-configuredtableidentifier)" : String,
      "[Description](#cfn-cleanrooms-configuredtableassociation-description)" : String,
      "[MembershipIdentifier](#cfn-cleanrooms-configuredtableassociation-membershipidentifier)" : String,
      "[Name](#cfn-cleanrooms-configuredtableassociation-name)" : String,
      "[RoleArn](#cfn-cleanrooms-configuredtableassociation-rolearn)" : String,
      "[Tags](#cfn-cleanrooms-configuredtableassociation-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-cleanrooms-configuredtableassociation-syntax.yaml"></a>

```
Type: AWS::CleanRooms::ConfiguredTableAssociation
Properties: 
  [ConfiguredTableIdentifier](#cfn-cleanrooms-configuredtableassociation-configuredtableidentifier): String
  [Description](#cfn-cleanrooms-configuredtableassociation-description): String
  [MembershipIdentifier](#cfn-cleanrooms-configuredtableassociation-membershipidentifier): String
  [Name](#cfn-cleanrooms-configuredtableassociation-name): String
  [RoleArn](#cfn-cleanrooms-configuredtableassociation-rolearn): String
  [Tags](#cfn-cleanrooms-configuredtableassociation-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-cleanrooms-configuredtableassociation-properties"></a>

`ConfiguredTableIdentifier`  <a name="cfn-cleanrooms-configuredtableassociation-configuredtableidentifier"></a>
A unique identifier for the configured table to be associated to\. Currently accepts a configured table ID\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `36`  
*Maximum*: `36`  
*Pattern*: `.*[0-9a-f]{8}-[0-9a-f]{4}-[0-9a-f]{4}-[0-9a-f]{4}-[0-9a-f]{12}.*`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Description`  <a name="cfn-cleanrooms-configuredtableassociation-description"></a>
A description of the configured table association\.  
*Required*: No  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `255`  
*Pattern*: `[\u0020-\uD7FF\uE000-\uFFFD\uD800\uDBFF-\uDC00\uDFFF\t\r\n]*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MembershipIdentifier`  <a name="cfn-cleanrooms-configuredtableassociation-membershipidentifier"></a>
The unique ID for the membership this configured table association belongs to\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `36`  
*Maximum*: `36`  
*Pattern*: `.*[0-9a-f]{8}-[0-9a-f]{4}-[0-9a-f]{4}-[0-9a-f]{4}-[0-9a-f]{12}.*`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Name`  <a name="cfn-cleanrooms-configuredtableassociation-name"></a>
The name of the configured table association, in lowercase\. The table is identified by this name when running protected queries against the underlying data\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `128`  
*Pattern*: `[a-zA-Z0-9_](([a-zA-Z0-9_ ]+-)*([a-zA-Z0-9_ ]+))?`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`RoleArn`  <a name="cfn-cleanrooms-configuredtableassociation-rolearn"></a>
The service will assume this role to access catalog metadata and query the table\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `32`  
*Maximum*: `512`  
*Pattern*: `arn:aws:iam::[\w]+:role/[\w+=,./@-]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-cleanrooms-configuredtableassociation-tags"></a>
An optional label that you can assign to a resource when you create it\. Each tag consists of a key and an optional value, both of which you define\. When you use tagging, you can also use tag\-based access control in IAM policies to control access to this resource\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-cleanrooms-configuredtableassociation-return-values"></a>

### Ref<a name="aws-resource-cleanrooms-configuredtableassociation-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref`function, `Ref`returns the `ConfiguredTableAssociation` and the ID of the Membership\. For example: `c1baf760-935e-4b2d-b36e-af8daaeb6e48|81a97460-2c40-46ce-a2fd-4ccda7398b2c`

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-cleanrooms-configuredtableassociation-return-values-fn--getatt"></a>

The `Fn::GetAtt`intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt`intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-cleanrooms-configuredtableassociation-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
Returns the Amazon Resource Name \(ARN\) of the specified configured table association\.  
Example: `arn:aws:cleanrooms:us-east-1:111122223333:configuredtable/a1b2c3d4-5678-90ab-cdef-EXAMPLE33333`

`ConfiguredTableAssociationIdentifier`  <a name="ConfiguredTableAssociationIdentifier-fn::getatt"></a>
Returns the unique identifier of the specified configured table association\.  
Example: `a1b2c3d4-5678-90ab-cdef-EXAMPLE33333`