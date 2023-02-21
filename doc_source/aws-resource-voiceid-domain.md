# AWS::VoiceID::Domain<a name="aws-resource-voiceid-domain"></a>

Creates a domain that contains all Amazon Connect Voice ID data, such as speakers, fraudsters, customer audio, and voiceprints\. 

## Syntax<a name="aws-resource-voiceid-domain-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-voiceid-domain-syntax.json"></a>

```
{
  "Type" : "AWS::VoiceID::Domain",
  "Properties" : {
      "[Description](#cfn-voiceid-domain-description)" : String,
      "[Name](#cfn-voiceid-domain-name)" : String,
      "[ServerSideEncryptionConfiguration](#cfn-voiceid-domain-serversideencryptionconfiguration)" : ServerSideEncryptionConfiguration,
      "[Tags](#cfn-voiceid-domain-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-voiceid-domain-syntax.yaml"></a>

```
Type: AWS::VoiceID::Domain
Properties: 
  [Description](#cfn-voiceid-domain-description): String
  [Name](#cfn-voiceid-domain-name): String
  [ServerSideEncryptionConfiguration](#cfn-voiceid-domain-serversideencryptionconfiguration): 
    ServerSideEncryptionConfiguration
  [Tags](#cfn-voiceid-domain-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-voiceid-domain-properties"></a>

`Description`  <a name="cfn-voiceid-domain-description"></a>
The client\-provided description of the domain\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-voiceid-domain-name"></a>
The client\-provided name for the domain\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ServerSideEncryptionConfiguration`  <a name="cfn-voiceid-domain-serversideencryptionconfiguration"></a>
The server\-side encryption configuration containing the KMS key identifier you want Voice ID to use to encrypt your data\.  
*Required*: Yes  
*Type*: [ServerSideEncryptionConfiguration](aws-properties-voiceid-domain-serversideencryptionconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-voiceid-domain-tags"></a>
The tags used to organize, track, or control access for this resource\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-voiceid-domain-return-values"></a>

### Ref<a name="aws-resource-voiceid-domain-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the `DomainId` of the domain\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-voiceid-domain-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-voiceid-domain-return-values-fn--getatt-fn--getatt"></a>

`DomainId`  <a name="DomainId-fn::getatt"></a>
The identifier of the domain\.