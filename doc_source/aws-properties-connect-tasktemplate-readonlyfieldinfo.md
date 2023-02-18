# AWS::Connect::TaskTemplate ReadOnlyFieldInfo<a name="aws-properties-connect-tasktemplate-readonlyfieldinfo"></a>

Indicates a field that is read\-only to an agent\.

## Syntax<a name="aws-properties-connect-tasktemplate-readonlyfieldinfo-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-connect-tasktemplate-readonlyfieldinfo-syntax.json"></a>

```
{
  "[Id](#cfn-connect-tasktemplate-readonlyfieldinfo-id)" : FieldIdentifier
}
```

### YAML<a name="aws-properties-connect-tasktemplate-readonlyfieldinfo-syntax.yaml"></a>

```
  [Id](#cfn-connect-tasktemplate-readonlyfieldinfo-id): 
    FieldIdentifier
```

## Properties<a name="aws-properties-connect-tasktemplate-readonlyfieldinfo-properties"></a>

`Id`  <a name="cfn-connect-tasktemplate-readonlyfieldinfo-id"></a>
Identifier of the read\-only field\.  
*Required*: Yes  
*Type*: [FieldIdentifier](aws-properties-connect-tasktemplate-fieldidentifier.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)