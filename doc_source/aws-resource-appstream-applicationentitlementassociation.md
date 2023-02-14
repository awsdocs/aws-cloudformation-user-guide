# AWS::AppStream::ApplicationEntitlementAssociation<a name="aws-resource-appstream-applicationentitlementassociation"></a>

Associates an application to an entitlement\.

## Syntax<a name="aws-resource-appstream-applicationentitlementassociation-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-appstream-applicationentitlementassociation-syntax.json"></a>

```
{
  "Type" : "AWS::AppStream::ApplicationEntitlementAssociation",
  "Properties" : {
      "[ApplicationIdentifier](#cfn-appstream-applicationentitlementassociation-applicationidentifier)" : String,
      "[EntitlementName](#cfn-appstream-applicationentitlementassociation-entitlementname)" : String,
      "[StackName](#cfn-appstream-applicationentitlementassociation-stackname)" : String
    }
}
```

### YAML<a name="aws-resource-appstream-applicationentitlementassociation-syntax.yaml"></a>

```
Type: AWS::AppStream::ApplicationEntitlementAssociation
Properties: 
  [ApplicationIdentifier](#cfn-appstream-applicationentitlementassociation-applicationidentifier): String
  [EntitlementName](#cfn-appstream-applicationentitlementassociation-entitlementname): String
  [StackName](#cfn-appstream-applicationentitlementassociation-stackname): String
```

## Properties<a name="aws-resource-appstream-applicationentitlementassociation-properties"></a>

`ApplicationIdentifier`  <a name="cfn-appstream-applicationentitlementassociation-applicationidentifier"></a>
The identifier of the application\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`EntitlementName`  <a name="cfn-appstream-applicationentitlementassociation-entitlementname"></a>
The name of the entitlement\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`StackName`  <a name="cfn-appstream-applicationentitlementassociation-stackname"></a>
The name of the stack\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-appstream-applicationentitlementassociation-return-values"></a>

### Ref<a name="aws-resource-appstream-applicationentitlementassociation-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the combination of the `StackName`, `EntitlementName`, and `ApplicationIdentifier`, such as `abcdefStack|abcdefEntitlement|abcdefApplication`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.