# AWS::LakeFormation::Resource<a name="aws-resource-lakeformation-resource"></a>

The AWS::LakeFormation::Resource is an AWS Lake Formation resource type that defines the resources to which permissions are to be granted\.

## Syntax<a name="aws-resource-lakeformation-resource-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-lakeformation-resource-syntax.json"></a>

```
{
  "Type" : "AWS::LakeFormation::Resource",
  "Properties" : {
      "[ResourceArn](#cfn-lakeformation-resource-resourcearn)" : String,
      "[RoleArn](#cfn-lakeformation-resource-rolearn)" : String,
      "[UseServiceLinkedRole](#cfn-lakeformation-resource-useservicelinkedrole)" : Boolean
    }
}
```

### YAML<a name="aws-resource-lakeformation-resource-syntax.yaml"></a>

```
Type: AWS::LakeFormation::Resource
Properties: 
  [ResourceArn](#cfn-lakeformation-resource-resourcearn): String
  [RoleArn](#cfn-lakeformation-resource-rolearn): String
  [UseServiceLinkedRole](#cfn-lakeformation-resource-useservicelinkedrole): Boolean
```

## Properties<a name="aws-resource-lakeformation-resource-properties"></a>

`ResourceArn`  <a name="cfn-lakeformation-resource-resourcearn"></a>
The Amazon Resource Name \(ARN\) of the resource\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RoleArn`  <a name="cfn-lakeformation-resource-rolearn"></a>
The IAM role that registered a resource\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`UseServiceLinkedRole`  <a name="cfn-lakeformation-resource-useservicelinkedrole"></a>
Designates a trusted caller, an IAM principal, by registering this caller with the Data Catalog\.  
*Required*: Yes  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return Values<a name="aws-resource-lakeformation-resource-return-values"></a>

### Ref<a name="aws-resource-lakeformation-resource-return-values-ref"></a>