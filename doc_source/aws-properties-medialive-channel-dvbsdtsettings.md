# AWS::MediaLive::Channel DvbSdtSettings<a name="aws-properties-medialive-channel-dvbsdtsettings"></a>

A DVB Service Description Table \(SDT\)\.

The parent of this entity is M2tsSettings\.

## Syntax<a name="aws-properties-medialive-channel-dvbsdtsettings-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-medialive-channel-dvbsdtsettings-syntax.json"></a>

```
{
  "[OutputSdt](#cfn-medialive-channel-dvbsdtsettings-outputsdt)" : String,
  "[RepInterval](#cfn-medialive-channel-dvbsdtsettings-repinterval)" : Integer,
  "[ServiceName](#cfn-medialive-channel-dvbsdtsettings-servicename)" : String,
  "[ServiceProviderName](#cfn-medialive-channel-dvbsdtsettings-serviceprovidername)" : String
}
```

### YAML<a name="aws-properties-medialive-channel-dvbsdtsettings-syntax.yaml"></a>

```
  [OutputSdt](#cfn-medialive-channel-dvbsdtsettings-outputsdt): String
  [RepInterval](#cfn-medialive-channel-dvbsdtsettings-repinterval): Integer
  [ServiceName](#cfn-medialive-channel-dvbsdtsettings-servicename): String
  [ServiceProviderName](#cfn-medialive-channel-dvbsdtsettings-serviceprovidername): String
```

## Properties<a name="aws-properties-medialive-channel-dvbsdtsettings-properties"></a>

`OutputSdt`  <a name="cfn-medialive-channel-dvbsdtsettings-outputsdt"></a>
Selects a method of inserting SDT information into an output stream\. The sdtFollow setting copies SDT information from input stream to output stream\. The sdtFollowIfPresent setting copies SDT information from input stream to output stream if SDT information is present in the input\. Otherwise, it falls back on the user\-defined values\. The sdtManual setting means that the user will enter the SDT information\. The sdtNone setting means that the output stream will not contain SDT information\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RepInterval`  <a name="cfn-medialive-channel-dvbsdtsettings-repinterval"></a>
The number of milliseconds between instances of this table in the output transport stream\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ServiceName`  <a name="cfn-medialive-channel-dvbsdtsettings-servicename"></a>
The service name placed in the serviceDescriptor in the Service Description Table \(SDT\)\. The maximum length is 256 characters\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ServiceProviderName`  <a name="cfn-medialive-channel-dvbsdtsettings-serviceprovidername"></a>
The service provider name placed in the serviceDescriptor in the Service Description Table \(SDT\)\. The maximum length is 256 characters\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)