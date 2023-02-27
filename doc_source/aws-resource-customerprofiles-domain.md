# AWS::CustomerProfiles::Domain<a name="aws-resource-customerprofiles-domain"></a>

Specifies an Amazon Connect Customer Profiles Domain\.

## Syntax<a name="aws-resource-customerprofiles-domain-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-customerprofiles-domain-syntax.json"></a>

```
{
  "Type" : "AWS::CustomerProfiles::Domain",
  "Properties" : {
      "[DeadLetterQueueUrl](#cfn-customerprofiles-domain-deadletterqueueurl)" : String,
      "[DefaultEncryptionKey](#cfn-customerprofiles-domain-defaultencryptionkey)" : String,
      "[DefaultExpirationDays](#cfn-customerprofiles-domain-defaultexpirationdays)" : Integer,
      "[DomainName](#cfn-customerprofiles-domain-domainname)" : String,
      "[Tags](#cfn-customerprofiles-domain-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-customerprofiles-domain-syntax.yaml"></a>

```
Type: AWS::CustomerProfiles::Domain
Properties: 
  [DeadLetterQueueUrl](#cfn-customerprofiles-domain-deadletterqueueurl): String
  [DefaultEncryptionKey](#cfn-customerprofiles-domain-defaultencryptionkey): String
  [DefaultExpirationDays](#cfn-customerprofiles-domain-defaultexpirationdays): Integer
  [DomainName](#cfn-customerprofiles-domain-domainname): String
  [Tags](#cfn-customerprofiles-domain-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-customerprofiles-domain-properties"></a>

`DeadLetterQueueUrl`  <a name="cfn-customerprofiles-domain-deadletterqueueurl"></a>
The URL of the SQS dead letter queue, which is used for reporting errors associated with ingesting data from third party applications\. You must set up a policy on the DeadLetterQueue for the SendMessage operation to enable Amazon Connect Customer Profiles to send messages to the DeadLetterQueue\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DefaultEncryptionKey`  <a name="cfn-customerprofiles-domain-defaultencryptionkey"></a>
The default encryption key, which is an AWS managed key, is used when no specific type of encryption key is specified\. It is used to encrypt all data before it is placed in permanent or semi\-permanent storage\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DefaultExpirationDays`  <a name="cfn-customerprofiles-domain-defaultexpirationdays"></a>
The default number of days until the data within the domain expires\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DomainName`  <a name="cfn-customerprofiles-domain-domainname"></a>
The unique name of the domain\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-customerprofiles-domain-tags"></a>
The tags used to organize, track, or control access for this resource\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-customerprofiles-domain-return-values"></a>

### Ref<a name="aws-resource-customerprofiles-domain-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the DomainName of the domain\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-customerprofiles-domain-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-customerprofiles-domain-return-values-fn--getatt-fn--getatt"></a>

`CreatedAt`  <a name="CreatedAt-fn::getatt"></a>
The timestamp of when the domain was created\.

`LastUpdatedAt`  <a name="LastUpdatedAt-fn::getatt"></a>
The timestamp of when the domain was most recently edited\.

## Examples<a name="aws-resource-customerprofiles-domain--examples"></a>

The following example creates a Domain\.

### <a name="aws-resource-customerprofiles-domain--examples--"></a>

#### YAML<a name="aws-resource-customerprofiles-domain--examples----yaml"></a>

```
Type: "AWS::CustomerProfiles::Domain" 
Properties:
    DomainName: "ExampleDomain" 
    DefaultEncryptionKey: "arn:aws:kms:us-east-1:123456789012:key/1988472d-6b77-4bb6-ae39-efce5EXAMPLE"
    DeadLetterQueueUrl: "arn:aws:sqs:us-east-1:123456789012:DLQName" 
    DefaultExpirationDays: 6
```

#### JSON<a name="aws-resource-customerprofiles-domain--examples----json"></a>

```
"Type": "AWS::CustomerProfiles::Domain",
"Properties": { 
    "DomainName": "ExampleDomain", 
    "DefaultEncryptionKey": "arn:aws:kms:us-east-1:123456789012:key/1988472d-6b77-4bb6-ae39-efce5EXAMPLE",
    "DeadLetterQueueUrl": "arn:aws:sqs:us-east-1:123456789012:DLQName", 
    "DefaultExpirationDays": 6
}
```