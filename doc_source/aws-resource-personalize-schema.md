# AWS::Personalize::Schema<a name="aws-resource-personalize-schema"></a>

Creates an Amazon Personalize schema from the specified schema string\. The schema you create must be in Avro JSON format\.

Amazon Personalize recognizes three schema variants\. Each schema is associated with a dataset type and has a set of required field and keywords\. If you are creating a schema for a dataset in a Domain dataset group, you provide the domain of the Domain dataset group\. You specify a schema when you call [CreateDataset](https://docs.aws.amazon.com/personalize/latest/dg/API_CreateDataset.html)\.

For more information on schemas, see [Datasets and schemas](https://docs.aws.amazon.com/personalize/latest/dg/how-it-works-dataset-schema.html)\.

**Related APIs**
+  [ListSchemas](https://docs.aws.amazon.com/personalize/latest/dg/API_ListSchemas.html) 
+  [DescribeSchema](https://docs.aws.amazon.com/personalize/latest/dg/API_DescribeSchema.html) 
+  [DeleteSchema](https://docs.aws.amazon.com/personalize/latest/dg/API_DeleteSchema.html) 

## Syntax<a name="aws-resource-personalize-schema-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-personalize-schema-syntax.json"></a>

```
{
  "Type" : "AWS::Personalize::Schema",
  "Properties" : {
      "[Domain](#cfn-personalize-schema-domain)" : String,
      "[Name](#cfn-personalize-schema-name)" : String,
      "[Schema](#cfn-personalize-schema-schema)" : String
    }
}
```

### YAML<a name="aws-resource-personalize-schema-syntax.yaml"></a>

```
Type: AWS::Personalize::Schema
Properties: 
  [Domain](#cfn-personalize-schema-domain): String
  [Name](#cfn-personalize-schema-name): String
  [Schema](#cfn-personalize-schema-schema): String
```

## Properties<a name="aws-resource-personalize-schema-properties"></a>

`Domain`  <a name="cfn-personalize-schema-domain"></a>
The domain of a schema that you created for a dataset in a Domain dataset group\.  
*Required*: No  
*Type*: String  
*Allowed values*: `ECOMMERCE | VIDEO_ON_DEMAND`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Name`  <a name="cfn-personalize-schema-name"></a>
The name of the schema\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `63`  
*Pattern*: `^[a-zA-Z0-9][a-zA-Z0-9\-_]*`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Schema`  <a name="cfn-personalize-schema-schema"></a>
The schema\.  
*Required*: Yes  
*Type*: String  
*Maximum*: `10000`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-personalize-schema-return-values"></a>

### Ref<a name="aws-resource-personalize-schema-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the name of the resource\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-personalize-schema-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-personalize-schema-return-values-fn--getatt-fn--getatt"></a>

`SchemaArn`  <a name="SchemaArn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the schema\.