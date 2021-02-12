# AWS::Lambda::LayerVersionPermission<a name="aws-resource-lambda-layerversionpermission"></a>

The `AWS::Lambda::LayerVersionPermission` resource adds permissions to the resource\-based policy of a version of an [AWS Lambda layer](https://docs.aws.amazon.com/lambda/latest/dg/configuration-layers.html)\. Use this action to grant layer usage permission to other accounts\. You can grant permission to a single account, all AWS accounts, or all accounts in an organization\.

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
Type: AWS::Lambda::LayerVersionPermission
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
*Pattern*: `lambda:GetLayerVersion`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`LayerVersionArn`  <a name="cfn-lambda-layerversionpermission-layerversionarn"></a>
The Amazon Resource Name \(ARN\) of the layer\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `140`  
*Pattern*: `(arn:[a-zA-Z0-9-]+:lambda:[a-zA-Z0-9-]+:\d{12}:layer:[a-zA-Z0-9-_]+)|[a-zA-Z0-9-_]+`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`OrganizationId`  <a name="cfn-lambda-layerversionpermission-organizationid"></a>
With the principal set to `*`, grant permission to all accounts in the specified organization\.  
*Required*: No  
*Type*: String  
*Pattern*: `o-[a-z0-9]{10,32}`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Principal`  <a name="cfn-lambda-layerversionpermission-principal"></a>
An account ID, or `*` to grant permission to all AWS accounts\.  
*Required*: Yes  
*Type*: String  
*Pattern*: `\d{12}|\*|arn:(aws[a-zA-Z-]*):iam::\d{12}:root`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-lambda-layerversionpermission-return-values"></a>

### Ref<a name="aws-resource-lambda-layerversionpermission-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the layer version ARN and statement ID, such as `arn:aws:lambda:us-west-2:123456789012:layer:my-layer:1#engineering-org`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-resource-lambda-layerversionpermission--examples"></a>



### Layer Version Permission<a name="aws-resource-lambda-layerversionpermission--examples--Layer_Version_Permission"></a>

Grant layer use permission to accounts in organization `o-t194hfs8cz`\.

#### JSON<a name="aws-resource-lambda-layerversionpermission--examples--Layer_Version_Permission--json"></a>

```
"MyLayerPermission": {
    "Type": "AWS::Lambda::LayerVersionPermission",
    "Properties": {
        "Action": "lambda:GetLayerVersion",
        "LayerVersionArn": "arn:aws:lambda:us-west-2:123456789012:layer:my-layer:1",
        "OrganizationId": "o-t194hfs8cz",
        "Principal": "*"
    }
}
```

#### YAML<a name="aws-resource-lambda-layerversionpermission--examples--Layer_Version_Permission--yaml"></a>

```
MyLayerPermission:
  Type: AWS::Lambda::LayerVersionPermission
  Properties:
    Action: lambda:GetLayerVersion
    LayerVersionArn: arn:aws:lambda:us-west-2:123456789012:layer:my-layer:1
    OrganizationId: o-t194hfs8cz
    Principal: *
```