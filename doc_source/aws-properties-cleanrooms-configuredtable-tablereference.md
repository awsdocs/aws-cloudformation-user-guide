# AWS::CleanRooms::ConfiguredTable TableReference<a name="aws-properties-cleanrooms-configuredtable-tablereference"></a>

A pointer to the dataset that underlies this table\. Currently, this can only be an AWS Glue table\.

## Syntax<a name="aws-properties-cleanrooms-configuredtable-tablereference-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-cleanrooms-configuredtable-tablereference-syntax.json"></a>

```
{
  "[Glue](#cfn-cleanrooms-configuredtable-tablereference-glue)" : GlueTableReference
}
```

### YAML<a name="aws-properties-cleanrooms-configuredtable-tablereference-syntax.yaml"></a>

```
  [Glue](#cfn-cleanrooms-configuredtable-tablereference-glue): 
    GlueTableReference
```

## Properties<a name="aws-properties-cleanrooms-configuredtable-tablereference-properties"></a>

`Glue`  <a name="cfn-cleanrooms-configuredtable-tablereference-glue"></a>
If present, a reference to the AWS Glue table referred to by this table reference\.  
*Required*: Yes  
*Type*: [GlueTableReference](aws-properties-cleanrooms-configuredtable-gluetablereference.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)