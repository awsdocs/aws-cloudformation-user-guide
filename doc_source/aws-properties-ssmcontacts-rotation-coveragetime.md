# AWS::SSMContacts::Rotation CoverageTime<a name="aws-properties-ssmcontacts-rotation-coveragetime"></a>

Information about when an on\-call shift begins and ends\.

## Syntax<a name="aws-properties-ssmcontacts-rotation-coveragetime-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ssmcontacts-rotation-coveragetime-syntax.json"></a>

```
{
  "[EndTime](#cfn-ssmcontacts-rotation-coveragetime-endtime)" : String,
  "[StartTime](#cfn-ssmcontacts-rotation-coveragetime-starttime)" : String
}
```

### YAML<a name="aws-properties-ssmcontacts-rotation-coveragetime-syntax.yaml"></a>

```
  [EndTime](#cfn-ssmcontacts-rotation-coveragetime-endtime): String
  [StartTime](#cfn-ssmcontacts-rotation-coveragetime-starttime): String
```

## Properties<a name="aws-properties-ssmcontacts-rotation-coveragetime-properties"></a>

`EndTime`  <a name="cfn-ssmcontacts-rotation-coveragetime-endtime"></a>
Information about when an on\-call rotation shift ends\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StartTime`  <a name="cfn-ssmcontacts-rotation-coveragetime-starttime"></a>
Information about when an on\-call rotation shift begins\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)