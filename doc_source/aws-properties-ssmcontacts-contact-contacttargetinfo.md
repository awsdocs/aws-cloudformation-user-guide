# AWS::SSMContacts::Contact ContactTargetInfo<a name="aws-properties-ssmcontacts-contact-contacttargetinfo"></a>

The contact that Incident Manager is engaging during an incident\.

## Syntax<a name="aws-properties-ssmcontacts-contact-contacttargetinfo-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ssmcontacts-contact-contacttargetinfo-syntax.json"></a>

```
{
  "[ContactId](#cfn-ssmcontacts-contact-contacttargetinfo-contactid)" : String,
  "[IsEssential](#cfn-ssmcontacts-contact-contacttargetinfo-isessential)" : Boolean
}
```

### YAML<a name="aws-properties-ssmcontacts-contact-contacttargetinfo-syntax.yaml"></a>

```
  [ContactId](#cfn-ssmcontacts-contact-contacttargetinfo-contactid): String
  [IsEssential](#cfn-ssmcontacts-contact-contacttargetinfo-isessential): Boolean
```

## Properties<a name="aws-properties-ssmcontacts-contact-contacttargetinfo-properties"></a>

`ContactId`  <a name="cfn-ssmcontacts-contact-contacttargetinfo-contactid"></a>
The Amazon Resource Name \(ARN\) of the contact\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `2048`  
*Pattern*: `arn:(aws|aws-cn|aws-us-gov):ssm-contacts:[-\w+=\/,.@]*:[0-9]+:([\w+=\/,.@:-]+)*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IsEssential`  <a name="cfn-ssmcontacts-contact-contacttargetinfo-isessential"></a>
A Boolean value determining if the contact's acknowledgement stops the progress of stages in the plan\.  
*Required*: Yes  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)