# AWS::MediaLive::Channel AutomaticInputFailoverSettings<a name="aws-properties-medialive-channel-automaticinputfailoversettings"></a>

Settings to configure the conditions that will define the input as unhealthy and that will make MediaLive fail over to the other input in the input failover pair\.

The parent of this entity is InputAttachment\.

## Syntax<a name="aws-properties-medialive-channel-automaticinputfailoversettings-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-medialive-channel-automaticinputfailoversettings-syntax.json"></a>

```
{
  "[ErrorClearTimeMsec](#cfn-medialive-channel-automaticinputfailoversettings-errorcleartimemsec)" : Integer,
  "[FailoverConditions](#cfn-medialive-channel-automaticinputfailoversettings-failoverconditions)" : [ FailoverCondition, ... ],
  "[InputPreference](#cfn-medialive-channel-automaticinputfailoversettings-inputpreference)" : String,
  "[SecondaryInputId](#cfn-medialive-channel-automaticinputfailoversettings-secondaryinputid)" : String
}
```

### YAML<a name="aws-properties-medialive-channel-automaticinputfailoversettings-syntax.yaml"></a>

```
  [ErrorClearTimeMsec](#cfn-medialive-channel-automaticinputfailoversettings-errorcleartimemsec): Integer
  [FailoverConditions](#cfn-medialive-channel-automaticinputfailoversettings-failoverconditions): 
    - FailoverCondition
  [InputPreference](#cfn-medialive-channel-automaticinputfailoversettings-inputpreference): String
  [SecondaryInputId](#cfn-medialive-channel-automaticinputfailoversettings-secondaryinputid): String
```

## Properties<a name="aws-properties-medialive-channel-automaticinputfailoversettings-properties"></a>

`ErrorClearTimeMsec`  <a name="cfn-medialive-channel-automaticinputfailoversettings-errorcleartimemsec"></a>
This clear time defines the requirement a recovered input must meet to be considered healthy\. The input must have no failover conditions for this length of time\. Enter a time in milliseconds\. This value is particularly important if the input\_preference for the failover pair is set to PRIMARY\_INPUT\_PREFERRED, because after this time, MediaLive will switch back to the primary input\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FailoverConditions`  <a name="cfn-medialive-channel-automaticinputfailoversettings-failoverconditions"></a>
A list of failover conditions\. If any of these conditions occur, MediaLive will perform a failover to the other input\.  
*Required*: No  
*Type*: List of [FailoverCondition](aws-properties-medialive-channel-failovercondition.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`InputPreference`  <a name="cfn-medialive-channel-automaticinputfailoversettings-inputpreference"></a>
Input preference when deciding which input to make active when a previously failed input has recovered\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SecondaryInputId`  <a name="cfn-medialive-channel-automaticinputfailoversettings-secondaryinputid"></a>
The input ID of the secondary input in the automatic input failover pair\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)