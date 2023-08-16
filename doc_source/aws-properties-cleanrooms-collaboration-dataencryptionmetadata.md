# AWS::CleanRooms::Collaboration DataEncryptionMetadata<a name="aws-properties-cleanrooms-collaboration-dataencryptionmetadata"></a>

The settings for client\-side encryption for cryptographic computing\.

## Syntax<a name="aws-properties-cleanrooms-collaboration-dataencryptionmetadata-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-cleanrooms-collaboration-dataencryptionmetadata-syntax.json"></a>

```
{
  "[AllowCleartext](#cfn-cleanrooms-collaboration-dataencryptionmetadata-allowcleartext)" : Boolean,
  "[AllowDuplicates](#cfn-cleanrooms-collaboration-dataencryptionmetadata-allowduplicates)" : Boolean,
  "[AllowJoinsOnColumnsWithDifferentNames](#cfn-cleanrooms-collaboration-dataencryptionmetadata-allowjoinsoncolumnswithdifferentnames)" : Boolean,
  "[PreserveNulls](#cfn-cleanrooms-collaboration-dataencryptionmetadata-preservenulls)" : Boolean
}
```

### YAML<a name="aws-properties-cleanrooms-collaboration-dataencryptionmetadata-syntax.yaml"></a>

```
  [AllowCleartext](#cfn-cleanrooms-collaboration-dataencryptionmetadata-allowcleartext): Boolean
  [AllowDuplicates](#cfn-cleanrooms-collaboration-dataencryptionmetadata-allowduplicates): Boolean
  [AllowJoinsOnColumnsWithDifferentNames](#cfn-cleanrooms-collaboration-dataencryptionmetadata-allowjoinsoncolumnswithdifferentnames): Boolean
  [PreserveNulls](#cfn-cleanrooms-collaboration-dataencryptionmetadata-preservenulls): Boolean
```

## Properties<a name="aws-properties-cleanrooms-collaboration-dataencryptionmetadata-properties"></a>

`AllowCleartext`  <a name="cfn-cleanrooms-collaboration-dataencryptionmetadata-allowcleartext"></a>
Indicates whether encrypted tables can contain cleartext data \(true\) or are to cryptographically process every column \(false\)\.  
*Required*: Yes  
*Type*: Boolean  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`AllowDuplicates`  <a name="cfn-cleanrooms-collaboration-dataencryptionmetadata-allowduplicates"></a>
Indicates whether Fingerprint columns can contain duplicate entries \(true\) or are to contain only non\-repeated values \(false\)\.  
*Required*: Yes  
*Type*: Boolean  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`AllowJoinsOnColumnsWithDifferentNames`  <a name="cfn-cleanrooms-collaboration-dataencryptionmetadata-allowjoinsoncolumnswithdifferentnames"></a>
Indicates whether Fingerprint columns can be joined on any other Fingerprint column with a different name \(true\) or can only be joined on Fingerprint columns of the same name \(false\)\.  
*Required*: Yes  
*Type*: Boolean  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`PreserveNulls`  <a name="cfn-cleanrooms-collaboration-dataencryptionmetadata-preservenulls"></a>
Indicates whether NULL values are to be copied as NULL to encrypted tables \(true\) or cryptographically processed \(false\)\.  
*Required*: Yes  
*Type*: Boolean  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)