# AWS::IVS::PlaybackKeyPair<a name="aws-resource-ivs-playbackkeypair"></a>

The `AWS::IVS::PlaybackKeyPair` resource is used to sign and validate a playback authorization token\. For more information, see [Setting Up Private Channels](https://docs.aws.amazon.com/ivs/latest/userguide/private-channels.html) in the *Amazon Interactive Video Service User Guide*\.

## Syntax<a name="aws-resource-ivs-playbackkeypair-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ivs-playbackkeypair-syntax.json"></a>

```
{
  "Type" : "AWS::IVS::PlaybackKeyPair",
  "Properties" : {
      "[Name](#cfn-ivs-playbackkeypair-name)" : String,
      "[PublicKeyMaterial](#cfn-ivs-playbackkeypair-publickeymaterial)" : String,
      "[Tags](#cfn-ivs-playbackkeypair-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-ivs-playbackkeypair-syntax.yaml"></a>

```
Type: AWS::IVS::PlaybackKeyPair
Properties: 
  [Name](#cfn-ivs-playbackkeypair-name): String
  [PublicKeyMaterial](#cfn-ivs-playbackkeypair-publickeymaterial): String
  [Tags](#cfn-ivs-playbackkeypair-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-ivs-playbackkeypair-properties"></a>

`Name`  <a name="cfn-ivs-playbackkeypair-name"></a>
An arbitrary string \(a nickname\) assigned to a playback key pair that helps the customer identify that resource\. The value does not need to be unique\.  
*Required*: No  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `128`  
*Pattern*: `^[a-zA-Z0-9-_]*$`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`PublicKeyMaterial`  <a name="cfn-ivs-playbackkeypair-publickeymaterial"></a>
The public portion of a customer\-generated key pair\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-ivs-playbackkeypair-tags"></a>
An array of key\-value pairs to apply to this resource\.  
For more information, see [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-ivs-playbackkeypair-return-values"></a>

### Ref<a name="aws-resource-ivs-playbackkeypair-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the playback key pair ARN\. For example:

 `{ "Ref": "myPlaybackKeyPair" }` 

For the Amazon IVS playback key pair `myPlaybackKeyPair`, Ref returns the playback key pair ARN\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-ivs-playbackkeypair-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-ivs-playbackkeypair-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
Key\-pair ARN\. For example: `arn:aws:ivs:us-west-2:693991300569:playback-key/f99cde61-c2b0-4df3-8941-ca7d38acca1a`

`Fingerprint`  <a name="Fingerprint-fn::getatt"></a>
Key\-pair identifier\. For example: `98:0d:1a:a0:19:96:1e:ea:0a:0a:2c:9a:42:19:2b:e7`

## Examples<a name="aws-resource-ivs-playbackkeypair--examples"></a>



### Playback Key Pair Template Examples<a name="aws-resource-ivs-playbackkeypair--examples--Playback_Key_Pair_Template_Examples"></a>

The following examples create an Amazon IVS playback key pair\.

#### JSON<a name="aws-resource-ivs-playbackkeypair--examples--Playback_Key_Pair_Template_Examples--json"></a>

```
 {
     "AWSTemplateFormatVersion": "2010-09-09",
     "Resources": {
         "PlaybackKeyPair": {
             "Type": "AWS::IVS::PlaybackKeyPair",
             "Properties": {
                 "PublicKeyMaterial": "-----BEGIN PUBLIC KEY-----\nMHYwEAYHKoZIzj0CAQYFK4EEACIDYgAEwOR43ETwEoWif1i14aL8GtDMNkT/kBQm\nh4sas9P//bjCU988rmQQXVBfftKT9xngg+W6hzOEpeUlCRlAtz6b6U79naYYRaSk\nK/UhYGWkXlbJlc9zn13imYWgVGe/BMFp\n-----END PUBLIC KEY-----\n",
                 "Name": "MyPlaybackKeyPair",
                 "Tags": [
                     {
                         "Key": "MyKey",
                         "Value": "MyValue"
                     }
                 ]
             }
         }
     },
     "Outputs": {
         "PlaybackKeyPairArn": {
             "Value": {"Ref": "PlaybackKeyPair"}
         },
         "PlaybackKeyPairFingerprint": {
             "Value": {
                 "Fn::GetAtt": [
                     "PlaybackKeyPair",
                     "Fingerprint"
                 ]
             }
         }
     }
 }
```

#### YAML<a name="aws-resource-ivs-playbackkeypair--examples--Playback_Key_Pair_Template_Examples--yaml"></a>

```
 AWSTemplateFormatVersion: 2010-09-09
 Resources:
  PlaybackKeyPair:
    Type: AWS::IVS::PlaybackKeyPair
    Properties:
      PublicKeyMaterial: |
        -----BEGIN PUBLIC KEY-----
        MHYwEAYHKoZIzj0CAQYFK4EEACIDYgAEwOR43ETwEoWif1i14aL8GtDMNkT/kBQm
        h4sas9P//bjCU988rmQQXVBfftKT9xngg+W6hzOEpeUlCRlAtz6b6U79naYYRaSk
        K/UhYGWkXlbJlc9zn13imYWgVGe/BMFp
        -----END PUBLIC KEY-----
      Name: MyPlaybackKeyPair
      Tags:
        - Key: MyKey
          Value: MyValue
 Outputs:
  PlaybackKeyPairArn:
    Value: !Ref PlaybackKeyPair
  PlaybackKeyPairFingerprint:
    Value: !GetAtt PlaybackKeyPair.Fingerprint
```

## See also<a name="aws-resource-ivs-playbackkeypair--seealso"></a>
+ [Setting Up Private Channels](https://docs.aws.amazon.com/ivs/latest/userguide/private-channels.html)
+ [PlaybackKeyPair](https://docs.aws.amazon.com/ivs/latest/APIReference/API_PlaybackKeyPair.html) data type
+ [ImportPlaybackKeyPair](https://docs.aws.amazon.com/ivs/latest/APIReference/API_ImportPlaybackKeyPair.html) API endpoint