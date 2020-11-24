# AWS::Glue::Schema Registry<a name="aws-properties-glue-schema-registry"></a>

Specifies a registry in the AWS Glue Schema Registry\.

## Syntax<a name="aws-properties-glue-schema-registry-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-glue-schema-registry-syntax.json"></a>

```
{
  "[Arn](#cfn-glue-schema-registry-arn)" : String,
  "[Name](#cfn-glue-schema-registry-name)" : String
}
```

### YAML<a name="aws-properties-glue-schema-registry-syntax.yaml"></a>

```
  [Arn](#cfn-glue-schema-registry-arn): String
  [Name](#cfn-glue-schema-registry-name): String
```

## Properties<a name="aws-properties-glue-schema-registry-properties"></a>

`Arn`  <a name="cfn-glue-schema-registry-arn"></a>
The Amazon Resource Name \(ARN\) of the registry\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Name`  <a name="cfn-glue-schema-registry-name"></a>
The name of the registry\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)