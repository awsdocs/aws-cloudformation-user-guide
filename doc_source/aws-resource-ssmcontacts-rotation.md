# AWS::SSMContacts::Rotation<a name="aws-resource-ssmcontacts-rotation"></a>

Creates a rotation in an on\-call schedule\.

## Syntax<a name="aws-resource-ssmcontacts-rotation-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ssmcontacts-rotation-syntax.json"></a>

```
{
  "Type" : "AWS::SSMContacts::Rotation",
  "Properties" : {
      "[ContactIds](#cfn-ssmcontacts-rotation-contactids)" : [ String, ... ],
      "[Name](#cfn-ssmcontacts-rotation-name)" : String,
      "[Recurrence](#cfn-ssmcontacts-rotation-recurrence)" : RecurrenceSettings,
      "[StartTime](#cfn-ssmcontacts-rotation-starttime)" : String,
      "[Tags](#cfn-ssmcontacts-rotation-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ],
      "[TimeZoneId](#cfn-ssmcontacts-rotation-timezoneid)" : String
    }
}
```

### YAML<a name="aws-resource-ssmcontacts-rotation-syntax.yaml"></a>

```
Type: AWS::SSMContacts::Rotation
Properties: 
  [ContactIds](#cfn-ssmcontacts-rotation-contactids): 
    - String
  [Name](#cfn-ssmcontacts-rotation-name): String
  [Recurrence](#cfn-ssmcontacts-rotation-recurrence): 
    RecurrenceSettings
  [StartTime](#cfn-ssmcontacts-rotation-starttime): String
  [Tags](#cfn-ssmcontacts-rotation-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
  [TimeZoneId](#cfn-ssmcontacts-rotation-timezoneid): String
```

## Properties<a name="aws-resource-ssmcontacts-rotation-properties"></a>

`ContactIds`  <a name="cfn-ssmcontacts-rotation-contactids"></a>
The Amazon Resource Names \(ARNs\) of the contacts assigned to the rotation team\.  
*Required*: Yes  
*Type*: List of String  
*Maximum*: `25`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-ssmcontacts-rotation-name"></a>
The name of the rotation\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `255`  
*Pattern*: `^[a-zA-Z0-9_\-\s\.]*$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Recurrence`  <a name="cfn-ssmcontacts-rotation-recurrence"></a>
Information about when an on\-call rotation is in effect and how long the rotation period lasts\.  
*Required*: Yes  
*Type*: [RecurrenceSettings](aws-properties-ssmcontacts-rotation-recurrencesettings.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StartTime`  <a name="cfn-ssmcontacts-rotation-starttime"></a>
The date and time the rotation becomes active\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-ssmcontacts-rotation-tags"></a>
Property description not available\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TimeZoneId`  <a name="cfn-ssmcontacts-rotation-timezoneid"></a>
The time zone the rotation’s activity is based on, in Internet Assigned Numbers Authority \(IANA\) format\. For example: "America/Los\_Angeles", "UTC", or "Asia/Seoul"\.   
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `255`  
*Pattern*: `^[:a-zA-Z0-9_\-\s\.\\/]*$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-ssmcontacts-rotation-return-values"></a>

### Ref<a name="aws-resource-ssmcontacts-rotation-return-values-ref"></a>

### Fn::GetAtt<a name="aws-resource-ssmcontacts-rotation-return-values-fn--getatt"></a>

#### <a name="aws-resource-ssmcontacts-rotation-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
Property description not available\.