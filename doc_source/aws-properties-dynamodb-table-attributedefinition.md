# AWS::DynamoDB::Table AttributeDefinition<a name="aws-properties-dynamodb-table-attributedefinition"></a>

Represents an attribute for describing the key schema for the table and indexes\.

## Syntax<a name="aws-properties-dynamodb-table-attributedefinition-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-dynamodb-table-attributedefinition-syntax.json"></a>

```
{
  "[AttributeName](#cfn-dynamodb-table-attributedefinition-attributename)" : String,
  "[AttributeType](#cfn-dynamodb-table-attributedefinition-attributetype)" : String
}
```

### YAML<a name="aws-properties-dynamodb-table-attributedefinition-syntax.yaml"></a>

```
  [AttributeName](#cfn-dynamodb-table-attributedefinition-attributename): String
  [AttributeType](#cfn-dynamodb-table-attributedefinition-attributetype): String
```

## Properties<a name="aws-properties-dynamodb-table-attributedefinition-properties"></a>

`AttributeName`  <a name="cfn-dynamodb-table-attributedefinition-attributename"></a>
A name for the attribute\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `255`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AttributeType`  <a name="cfn-dynamodb-table-attributedefinition-attributetype"></a>
The data type for the attribute, where:  
+  `S` \- the attribute is of type String
+  `N` \- the attribute is of type Number
+  `B` \- the attribute is of type Binary
*Required*: Yes  
*Type*: String  
*Allowed values*: `B | N | S`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)