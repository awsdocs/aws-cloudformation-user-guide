# AWS::Connect::TaskTemplate DefaultFieldValue<a name="aws-properties-connect-tasktemplate-defaultfieldvalue"></a>

Describes a default field and its corresponding value\.

## Syntax<a name="aws-properties-connect-tasktemplate-defaultfieldvalue-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-connect-tasktemplate-defaultfieldvalue-syntax.json"></a>

```
{
  "[DefaultValue](#cfn-connect-tasktemplate-defaultfieldvalue-defaultvalue)" : String,
  "[Id](#cfn-connect-tasktemplate-defaultfieldvalue-id)" : FieldIdentifier
}
```

### YAML<a name="aws-properties-connect-tasktemplate-defaultfieldvalue-syntax.yaml"></a>

```
  [DefaultValue](#cfn-connect-tasktemplate-defaultfieldvalue-defaultvalue): String
  [Id](#cfn-connect-tasktemplate-defaultfieldvalue-id): 
    FieldIdentifier
```

## Properties<a name="aws-properties-connect-tasktemplate-defaultfieldvalue-properties"></a>

`DefaultValue`  <a name="cfn-connect-tasktemplate-defaultfieldvalue-defaultvalue"></a>
Default value for the field\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Id`  <a name="cfn-connect-tasktemplate-defaultfieldvalue-id"></a>
Identifier of a field\.   
*Required*: Yes  
*Type*: [FieldIdentifier](aws-properties-connect-tasktemplate-fieldidentifier.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)