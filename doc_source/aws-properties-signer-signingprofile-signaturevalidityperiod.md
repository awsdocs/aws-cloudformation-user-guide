# AWS::Signer::SigningProfile SignatureValidityPeriod<a name="aws-properties-signer-signingprofile-signaturevalidityperiod"></a>

The validity period for the signing job\.

## Syntax<a name="aws-properties-signer-signingprofile-signaturevalidityperiod-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-signer-signingprofile-signaturevalidityperiod-syntax.json"></a>

```
{
  "[Type](#cfn-signer-signingprofile-signaturevalidityperiod-type)" : String,
  "[Value](#cfn-signer-signingprofile-signaturevalidityperiod-value)" : Integer
}
```

### YAML<a name="aws-properties-signer-signingprofile-signaturevalidityperiod-syntax.yaml"></a>

```
  [Type](#cfn-signer-signingprofile-signaturevalidityperiod-type): String
  [Value](#cfn-signer-signingprofile-signaturevalidityperiod-value): Integer
```

## Properties<a name="aws-properties-signer-signingprofile-signaturevalidityperiod-properties"></a>

`Type`  <a name="cfn-signer-signingprofile-signaturevalidityperiod-type"></a>
The time unit for signature validity: DAYS \| MONTHS \| YEARS\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Value`  <a name="cfn-signer-signingprofile-signaturevalidityperiod-value"></a>
The numerical value of the time unit for signature validity\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)