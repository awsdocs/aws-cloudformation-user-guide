# AWS::Shield::ProactiveEngagement EmergencyContact<a name="aws-properties-shield-proactiveengagement-emergencycontact"></a>

Contact information that the SRT can use to contact you if you have proactive engagement enabled, for escalations to the SRT and to initiate proactive customer support\.

## Syntax<a name="aws-properties-shield-proactiveengagement-emergencycontact-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-shield-proactiveengagement-emergencycontact-syntax.json"></a>

```
{
  "[ContactNotes](#cfn-shield-proactiveengagement-emergencycontact-contactnotes)" : String,
  "[EmailAddress](#cfn-shield-proactiveengagement-emergencycontact-emailaddress)" : String,
  "[PhoneNumber](#cfn-shield-proactiveengagement-emergencycontact-phonenumber)" : String
}
```

### YAML<a name="aws-properties-shield-proactiveengagement-emergencycontact-syntax.yaml"></a>

```
  [ContactNotes](#cfn-shield-proactiveengagement-emergencycontact-contactnotes): String
  [EmailAddress](#cfn-shield-proactiveengagement-emergencycontact-emailaddress): String
  [PhoneNumber](#cfn-shield-proactiveengagement-emergencycontact-phonenumber): String
```

## Properties<a name="aws-properties-shield-proactiveengagement-emergencycontact-properties"></a>

`ContactNotes`  <a name="cfn-shield-proactiveengagement-emergencycontact-contactnotes"></a>
Additional notes regarding the contact\.   
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `1024`  
*Pattern*: `^[\w\s\.\-,:/()+@]*$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EmailAddress`  <a name="cfn-shield-proactiveengagement-emergencycontact-emailaddress"></a>
The email address for the contact\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `150`  
*Pattern*: `^\S+@\S+\.\S+$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PhoneNumber`  <a name="cfn-shield-proactiveengagement-emergencycontact-phonenumber"></a>
The phone number for the contact\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `16`  
*Pattern*: `^\+[1-9]\d{1,14}$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)