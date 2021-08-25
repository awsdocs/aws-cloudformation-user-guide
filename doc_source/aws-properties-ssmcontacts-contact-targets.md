# AWS::SSMContacts::Contact Targets<a name="aws-properties-ssmcontacts-contact-targets"></a>

The contact or contact channel that's being engaged\.

## Syntax<a name="aws-properties-ssmcontacts-contact-targets-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ssmcontacts-contact-targets-syntax.json"></a>

```
{
  "[ChannelTargetInfo](#cfn-ssmcontacts-contact-targets-channeltargetinfo)" : ChannelTargetInfo,
  "[ContactTargetInfo](#cfn-ssmcontacts-contact-targets-contacttargetinfo)" : ContactTargetInfo
}
```

### YAML<a name="aws-properties-ssmcontacts-contact-targets-syntax.yaml"></a>

```
  [ChannelTargetInfo](#cfn-ssmcontacts-contact-targets-channeltargetinfo): 
    ChannelTargetInfo
  [ContactTargetInfo](#cfn-ssmcontacts-contact-targets-contacttargetinfo): 
    ContactTargetInfo
```

## Properties<a name="aws-properties-ssmcontacts-contact-targets-properties"></a>

`ChannelTargetInfo`  <a name="cfn-ssmcontacts-contact-targets-channeltargetinfo"></a>
Information about the contact channel Incident Manager is engaging\.  
*Required*: No  
*Type*: [ChannelTargetInfo](aws-properties-ssmcontacts-contact-channeltargetinfo.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ContactTargetInfo`  <a name="cfn-ssmcontacts-contact-targets-contacttargetinfo"></a>
The contact that Incident Manager is engaging during an incident\.  
*Required*: No  
*Type*: [ContactTargetInfo](aws-properties-ssmcontacts-contact-contacttargetinfo.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)