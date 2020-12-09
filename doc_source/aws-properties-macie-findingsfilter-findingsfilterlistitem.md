# AWS::Macie::FindingsFilter FindingsFilterListItem<a name="aws-properties-macie-findingsfilter-findingsfilterlistitem"></a>

Specifies the unique identifier and custom name of a findings filter\.

## Syntax<a name="aws-properties-macie-findingsfilter-findingsfilterlistitem-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-macie-findingsfilter-findingsfilterlistitem-syntax.json"></a>

```
{
  "[Id](#cfn-macie-findingsfilter-findingsfilterlistitem-id)" : String,
  "[Name](#cfn-macie-findingsfilter-findingsfilterlistitem-name)" : String
}
```

### YAML<a name="aws-properties-macie-findingsfilter-findingsfilterlistitem-syntax.yaml"></a>

```
  [Id](#cfn-macie-findingsfilter-findingsfilterlistitem-id): String
  [Name](#cfn-macie-findingsfilter-findingsfilterlistitem-name): String
```

## Properties<a name="aws-properties-macie-findingsfilter-findingsfilterlistitem-properties"></a>

`Id`  <a name="cfn-macie-findingsfilter-findingsfilterlistitem-id"></a>
The unique identifier for the filter\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-macie-findingsfilter-findingsfilterlistitem-name"></a>
The custom name of the filter\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)