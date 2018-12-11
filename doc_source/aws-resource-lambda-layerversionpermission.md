# AWS::Lambda::LayerVersionPermission<a name="aws-resource-lambda-layerversionpermission"></a>

The `AWS::Lambda::LayerVersionPermission` resource gives other accounts permission to use a layer version in AWS Lambda\. For more information, see [AWS Lambda Layers](https://docs.aws.amazon.com/lambda/latest/dg/configuration-layers.html) in the *AWS Lambda Developer Guide*\.

## Syntax<a name="aws-resource-lambda-layerversionpermission-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-lambda-layerversionpermission-syntax.json"></a>

```
{
  "Type" : "AWS::Lambda::LayerVersionPermission",
  "Properties" : {
    "[Action](#cfn-lambda-layerversionpermission-action)" : String,
    "[LayerVersionArn](#cfn-lambda-layerversionpermission-layerversionarn)" : String,
    "[OrganizationId](#cfn-lambda-layerversionpermission-organizationid)" : String,
    "[Principal](#cfn-lambda-layerversionpermission-principal)" : String
  }
}
```

### YAML<a name="aws-resource-lambda-layerversionpermission-syntax.yaml"></a>

```
Type: "AWS::Lambda::LayerVersionPermission"
Properties:
  [Action](#cfn-lambda-layerversionpermission-action): String
  [LayerVersionArn](#cfn-lambda-layerversionpermission-layerversionarn): String
  [OrganizationId](#cfn-lambda-layerversionpermission-organizationid): String
  [Principal](#cfn-lambda-layerversionpermission-principal): String
```

## Properties<a name="aws-resource-lambda-layerversionpermission-properties"></a>

`Action`  <a name="cfn-lambda-layerversionpermission-action"></a>
The API action that grants access to the layer\. For example, `lambda:GetLayerVersion`\.   
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`LayerVersionArn`  <a name="cfn-lambda-layerversionpermission-layerversionarn"></a>
The ARN of the layer version\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`OrganizationId`  <a name="cfn-lambda-layerversionpermission-organizationid"></a>
With the principal set to `*`, grant permission to all accounts in the specified organization\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`Principal`  <a name="cfn-lambda-layerversionpermission-principal"></a>
An account ID, or `*` to grant permission to all AWS accounts\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

## Return Values<a name="aws-resource-lambda-layerversionpermission-returnvalues"></a>

### Ref<a name="aws-resource-lambda-layerversionpermission-ref"></a>

When you pass the logical ID of an `AWS::Lambda::LayerVersionPermission` resource to the intrinsic `Ref` function, the function returns the layer version ARN and statement ID, such as `arn:aws:lambda:us-west-2:123456789012:layer:my-layer:1#engineering-org`\. 

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\. 

## Examples<a name="aws-resource-lambda-layerversionpermission-examples"></a>

### Grant permission to an organization<a name="aws-resource-lambda-layerversionpermission-example1"></a>

The following example grants all accounts in an organization permission to use a layer version\.

#### JSON<a name="aws-resource-lambda-layerversionpermission-example1.json"></a>

```
{
  "Type" : "AWS::Lambda::LayerVersionPermission",
  "Properties" : {
    "Action" : "lambda:GetLayerVersion",
    "LayerVersionArn" : "arn:aws:lambda:us-west-2:011685312445:layer:my-layer:1",
    "OrganizationId" : "o-t194hfs8cz",
    "Principal" : "*"
  }
}
```

#### YAML<a name="aws-resource-lambda-layerversionpermission-example1.yaml"></a>

```
Type: "AWS::Lambda::LayerVersionPermission"
Properties:
  Action: lambda:GetLayerVersion
  LayerVersionArn: arn:aws:lambda:us-west-2:011685312445:layer:my-layer:1
  OrganizationId: o-t194hfs8cz
  Principal: *
```

## See Also<a name="aws-resource-lambda-layerversionpermission-seealso"></a>
+ [AddLayerVersionPermission](https://docs.aws.amazon.com/lambda/latest/dg/API_AddLayerVersionPermission.html) in the *AWS Lambda Developer Guide*