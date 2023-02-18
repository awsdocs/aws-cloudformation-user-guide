# AWS::Connect::TaskTemplate Field<a name="aws-properties-connect-tasktemplate-field"></a>

Describes a single task template field\.

## Syntax<a name="aws-properties-connect-tasktemplate-field-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-connect-tasktemplate-field-syntax.json"></a>

```
{
  "[Description](#cfn-connect-tasktemplate-field-description)" : String,
  "[Id](#cfn-connect-tasktemplate-field-id)" : FieldIdentifier,
  "[SingleSelectOptions](#cfn-connect-tasktemplate-field-singleselectoptions)" : [ String, ... ],
  "[Type](#cfn-connect-tasktemplate-field-type)" : String
}
```

### YAML<a name="aws-properties-connect-tasktemplate-field-syntax.yaml"></a>

```
  [Description](#cfn-connect-tasktemplate-field-description): String
  [Id](#cfn-connect-tasktemplate-field-id): 
    FieldIdentifier
  [SingleSelectOptions](#cfn-connect-tasktemplate-field-singleselectoptions): 
    - String
  [Type](#cfn-connect-tasktemplate-field-type): String
```

## Properties<a name="aws-properties-connect-tasktemplate-field-properties"></a>

`Description`  <a name="cfn-connect-tasktemplate-field-description"></a>
The description of the field\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Id`  <a name="cfn-connect-tasktemplate-field-id"></a>
The unique identifier for the field\.  
*Required*: Yes  
*Type*: [FieldIdentifier](aws-properties-connect-tasktemplate-fieldidentifier.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SingleSelectOptions`  <a name="cfn-connect-tasktemplate-field-singleselectoptions"></a>
A list of options for a single select field\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Type`  <a name="cfn-connect-tasktemplate-field-type"></a>
Indicates the type of field\. Following are the valid field types: `NAME` `DESCRIPTION` \| `SCHEDULED_TIME` \| `QUICK_CONNECT` \| `URL` \| `NUMBER` \| `TEXT` \| `TEXT_AREA` \| `DATE_TIME` \| `BOOLEAN` \| `SINGLE_SELECT` \| `EMAIL`  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)