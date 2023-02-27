# AWS::Connect::User UserPhoneConfig<a name="aws-properties-connect-user-userphoneconfig"></a>

Contains information about the phone configuration settings for a user\.

## Syntax<a name="aws-properties-connect-user-userphoneconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-connect-user-userphoneconfig-syntax.json"></a>

```
{
  "[AfterContactWorkTimeLimit](#cfn-connect-user-userphoneconfig-aftercontactworktimelimit)" : Integer,
  "[AutoAccept](#cfn-connect-user-userphoneconfig-autoaccept)" : Boolean,
  "[DeskPhoneNumber](#cfn-connect-user-userphoneconfig-deskphonenumber)" : String,
  "[PhoneType](#cfn-connect-user-userphoneconfig-phonetype)" : String
}
```

### YAML<a name="aws-properties-connect-user-userphoneconfig-syntax.yaml"></a>

```
  [AfterContactWorkTimeLimit](#cfn-connect-user-userphoneconfig-aftercontactworktimelimit): Integer
  [AutoAccept](#cfn-connect-user-userphoneconfig-autoaccept): Boolean
  [DeskPhoneNumber](#cfn-connect-user-userphoneconfig-deskphonenumber): String
  [PhoneType](#cfn-connect-user-userphoneconfig-phonetype): String
```

## Properties<a name="aws-properties-connect-user-userphoneconfig-properties"></a>

`AfterContactWorkTimeLimit`  <a name="cfn-connect-user-userphoneconfig-aftercontactworktimelimit"></a>
The After Call Work \(ACW\) timeout setting, in seconds\.  
When returned by a `SearchUsers` call, `AfterContactWorkTimeLimit` is returned in milliseconds\. 
*Required*: No  
*Type*: Integer  
*Minimum*: `0`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AutoAccept`  <a name="cfn-connect-user-userphoneconfig-autoaccept"></a>
The Auto accept setting\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DeskPhoneNumber`  <a name="cfn-connect-user-userphoneconfig-deskphonenumber"></a>
The phone number for the user's desk phone\.  
*Required*: No  
*Type*: String  
*Pattern*: `\\+[1-9]\\d{1,14}$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PhoneType`  <a name="cfn-connect-user-userphoneconfig-phonetype"></a>
The phone type\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `DESK_PHONE | SOFT_PHONE`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)