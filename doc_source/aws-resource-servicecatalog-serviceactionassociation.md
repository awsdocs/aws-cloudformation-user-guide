# AWS::ServiceCatalog::ServiceActionAssociation<a name="aws-resource-servicecatalog-serviceactionassociation"></a>

A self\-service action association consisting of the Action ID, the Product ID, and the Provisioning Artifact ID\.

## Syntax<a name="aws-resource-servicecatalog-serviceactionassociation-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-servicecatalog-serviceactionassociation-syntax.json"></a>

```
{
  "Type" : "AWS::ServiceCatalog::ServiceActionAssociation",
  "Properties" : {
      "[ProductId](#cfn-servicecatalog-serviceactionassociation-productid)" : String,
      "[ProvisioningArtifactId](#cfn-servicecatalog-serviceactionassociation-provisioningartifactid)" : String,
      "[ServiceActionId](#cfn-servicecatalog-serviceactionassociation-serviceactionid)" : String
    }
}
```

### YAML<a name="aws-resource-servicecatalog-serviceactionassociation-syntax.yaml"></a>

```
Type: AWS::ServiceCatalog::ServiceActionAssociation
Properties: 
  [ProductId](#cfn-servicecatalog-serviceactionassociation-productid): String
  [ProvisioningArtifactId](#cfn-servicecatalog-serviceactionassociation-provisioningartifactid): String
  [ServiceActionId](#cfn-servicecatalog-serviceactionassociation-serviceactionid): String
```

## Properties<a name="aws-resource-servicecatalog-serviceactionassociation-properties"></a>

`ProductId`  <a name="cfn-servicecatalog-serviceactionassociation-productid"></a>
The product identifier\. For example, `prod-abcdzk7xy33qa`\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `100`  
*Pattern*: `^[a-zA-Z0-9_\-]*`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ProvisioningArtifactId`  <a name="cfn-servicecatalog-serviceactionassociation-provisioningartifactid"></a>
The identifier of the provisioning artifact\. For example, `pa-4abcdjnxjj6ne`\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `100`  
*Pattern*: `^[a-zA-Z0-9_\-]*`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ServiceActionId`  <a name="cfn-servicecatalog-serviceactionassociation-serviceactionid"></a>
The self\-service action identifier\. For example, `act-fs7abcd89wxyz`\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `100`  
*Pattern*: `^[a-zA-Z0-9_\-]*`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-servicecatalog-serviceactionassociation-return-values"></a>

### Ref<a name="aws-resource-servicecatalog-serviceactionassociation-return-values-ref"></a>