# AWS::Glue::Registry<a name="aws-resource-glue-registry"></a>

The AWS::Glue::Registry is an AWS Glue resource type that manages registries of schemas in the AWS Glue Schema Registry\.

## Syntax<a name="aws-resource-glue-registry-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-glue-registry-syntax.json"></a>

```
{
  "Type" : "AWS::Glue::Registry",
  "Properties" : {
      "[Description](#cfn-glue-registry-description)" : String,
      "[Name](#cfn-glue-registry-name)" : String,
      "[Tags](#cfn-glue-registry-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-glue-registry-syntax.yaml"></a>

```
Type: AWS::Glue::Registry
Properties: 
  [Description](#cfn-glue-registry-description): String
  [Name](#cfn-glue-registry-name): String
  [Tags](#cfn-glue-registry-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-glue-registry-properties"></a>

`Description`  <a name="cfn-glue-registry-description"></a>
A description of the registry\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-glue-registry-name"></a>
The name of the registry\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-glue-registry-tags"></a>
AWS tags that contain a key value pair and may be searched by console, command line, or API\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-glue-registry-return-values"></a>

### Ref<a name="aws-resource-glue-registry-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns a combination of "VersionId\|Key\|Value" as a string\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-glue-registry-return-values-fn--getatt"></a>

#### <a name="aws-resource-glue-registry-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
Not currently supported by AWS CloudFormation\.