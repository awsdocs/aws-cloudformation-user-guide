# AWS::SSMContacts::Rotation<a name="aws-resource-ssmcontacts-rotation"></a>

Specifies a rotation in an on\-call schedule\.

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
The Amazon Resource Names \(ARNs\) of the contacts to add to the rotation\.  
The order in which you list the contacts is their shift order in the rotation schedule\.  
*Required*: Yes  
*Type*: List of String  
*Maximum*: `25`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-ssmcontacts-rotation-name"></a>
The name for the rotation\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `255`  
*Pattern*: `^[a-zA-Z0-9_\-\s\.]*$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Recurrence`  <a name="cfn-ssmcontacts-rotation-recurrence"></a>
Information about the rule that specifies when shift team members rotate\.  
*Required*: Yes  
*Type*: [RecurrenceSettings](aws-properties-ssmcontacts-rotation-recurrencesettings.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StartTime`  <a name="cfn-ssmcontacts-rotation-starttime"></a>
The date and time the rotation goes into effect\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-ssmcontacts-rotation-tags"></a>
Optional metadata to assign to the rotation\. Tags enable you to categorize a resource in different ways, such as by purpose, owner, or environment\. For more information, see [Tagging Incident Manager resources](https://docs.aws.amazon.com/incident-manager/latest/userguide/tagging.html) in the *Incident Manager User Guide*\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TimeZoneId`  <a name="cfn-ssmcontacts-rotation-timezoneid"></a>
The time zone to base the rotation’s activity on, in Internet Assigned Numbers Authority \(IANA\) format\. For example: "America/Los\_Angeles", "UTC", or "Asia/Seoul"\. For more information, see the [Time Zone Database](https://www.iana.org/time-zones) on the IANA website\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `255`  
*Pattern*: `^[:a-zA-Z0-9_\-\s\.\\/]*$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-ssmcontacts-rotation-return-values"></a>

### Ref<a name="aws-resource-ssmcontacts-rotation-return-values-ref"></a>

### Fn::GetAtt<a name="aws-resource-ssmcontacts-rotation-return-values-fn--getatt"></a>

The `Fn::GetAtt`intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt`intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-ssmcontacts-rotation-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the `Rotation` resource\.