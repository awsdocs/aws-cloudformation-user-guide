# AWS::EventSchemas::RegistryPolicy<a name="aws-resource-eventschemas-registrypolicy"></a>

Use the `AWS::EventSchemas::RegistryPolicy` resource to specify resource\-based policies for an EventBridge Schema Registry\.

## Syntax<a name="aws-resource-eventschemas-registrypolicy-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-eventschemas-registrypolicy-syntax.json"></a>

```
{
  "Type" : "AWS::EventSchemas::RegistryPolicy",
  "Properties" : {
      "[Policy](#cfn-eventschemas-registrypolicy-policy)" : Json,
      "[RegistryName](#cfn-eventschemas-registrypolicy-registryname)" : String,
      "[RevisionId](#cfn-eventschemas-registrypolicy-revisionid)" : String
    }
}
```

### YAML<a name="aws-resource-eventschemas-registrypolicy-syntax.yaml"></a>

```
Type: AWS::EventSchemas::RegistryPolicy
Properties: 
  [Policy](#cfn-eventschemas-registrypolicy-policy): Json
  [RegistryName](#cfn-eventschemas-registrypolicy-registryname): String
  [RevisionId](#cfn-eventschemas-registrypolicy-revisionid): String
```

## Properties<a name="aws-resource-eventschemas-registrypolicy-properties"></a>

`Policy`  <a name="cfn-eventschemas-registrypolicy-policy"></a>
A resource\-based policy\.  
*Required*: Yes  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RegistryName`  <a name="cfn-eventschemas-registrypolicy-registryname"></a>
The name of the registry\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RevisionId`  <a name="cfn-eventschemas-registrypolicy-revisionid"></a>
The revision ID of the policy\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-eventschemas-registrypolicy-return-values"></a>

### Ref<a name="aws-resource-eventschemas-registrypolicy-return-values-ref"></a>

When you provide the logical ID of this resource to the `Ref` intrinsic function, `Ref` the name of the registry\.

### Fn::GetAtt<a name="aws-resource-eventschemas-registrypolicy-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-eventschemas-registrypolicy-return-values-fn--getatt-fn--getatt"></a>

`Id`  <a name="Id-fn::getatt"></a>
The ID of the policy\.

## Examples<a name="aws-resource-eventschemas-registrypolicy--examples"></a>

### <a name="aws-resource-eventschemas-registrypolicy--examples--"></a>

#### YAML<a name="aws-resource-eventschemas-registrypolicy--examples----yaml"></a>

```
Resources:
  RegistryPolicy:
    Type: AWS::EventSchemas::RegistryPolicy
    Properties:
      RegistryName: registryName
      Policy:
        Version: 2012-10-17
        Statement:
          Sid: 1
          Effect: Allow
          Principal:
            AWS: arn:aws:iam::012345678901:user/TestAccountForRegistryPolicy
          Action:
            - schemas:DescribeRegistry
            - schemas:CreateSchema
          Resource: registryArn
```

### <a name="aws-resource-eventschemas-registrypolicy--examples--"></a>

#### YAML<a name="aws-resource-eventschemas-registrypolicy--examples----yaml"></a>

```
Resources:
  RegistryPolicy:
    Type: 'AWS::EventSchemas::RegistryPolicy'
    Properties:
      RegistryName: 'MyRegistry'
      Policy:
        Version: '2012-10-17'
        Statement:
          - Sid: 'Test'
            Effect: 'Allow'
            Action:
              - 'schemas:*'
            Principal:
              AWS:
                - '109876543210'
            Resource:
              - 'arn:aws:schemas:us-east-1:012345678901:registry/MyRegistry'
              - 'arn:aws:schemas:us-east-1:012345678901:schema/MyRegistry*'
```

### <a name="aws-resource-eventschemas-registrypolicy--examples--"></a>

#### JSON<a name="aws-resource-eventschemas-registrypolicy--examples----json"></a>

```
{
  "Resources": {
    "RegistryPolicy": {
      "Type": "AWS::EventSchemas::RegistryPolicy",
      "Properties": {
        "RegistryName": "MyRegistry",
        "Policy": {
          "Version": "2012-10-17",
          "Statement": [
            {
              "Sid": "Test",
              "Effect": "Allow",
              "Action": [
                "schemas:*"
              ],
              "Principal": {
                "AWS": [
                  "109876543210"
                ]
              },
              "Resource": [
                "arn:aws:schemas:us-east-1:012345678901:registry/MyRegistry",
                "arn:aws:schemas:us-east-1:012345678901:schema/MyRegistry*"
              ]
            }
          ]
        }
      }
    }
  }
}
```