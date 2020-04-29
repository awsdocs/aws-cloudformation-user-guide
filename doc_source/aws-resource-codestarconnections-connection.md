# AWS::CodeStarConnections::Connection<a name="aws-resource-codestarconnections-connection"></a>

**Important**  
The CodeStar Connections feature is in preview release and is subject to change\.

The AWS::CodeStarConnections::Connection resource can be used to connect external source providers with services like AWS CodePipeline\.

 **Note:** A connection created through CloudFormation is in `PENDING` status by default\. You can make its status `AVAILABLE` by editing the connection in the CodePipeline console\.

## Syntax<a name="aws-resource-codestarconnections-connection-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-codestarconnections-connection-syntax.json"></a>

```
{
  "Type" : "AWS::CodeStarConnections::Connection",
  "Properties" : {
      "[ConnectionName](#cfn-codestarconnections-connection-connectionname)" : String,
      "[ProviderType](#cfn-codestarconnections-connection-providertype)" : String
    }
}
```

### YAML<a name="aws-resource-codestarconnections-connection-syntax.yaml"></a>

```
Type: AWS::CodeStarConnections::Connection
Properties: 
  [ConnectionName](#cfn-codestarconnections-connection-connectionname): String
  [ProviderType](#cfn-codestarconnections-connection-providertype): String
```

## Properties<a name="aws-resource-codestarconnections-connection-properties"></a>

`ConnectionName`  <a name="cfn-codestarconnections-connection-connectionname"></a>
The name of the connection\. Connection names must be unique in an AWS user account\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `32`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ProviderType`  <a name="cfn-codestarconnections-connection-providertype"></a>
The name of the external provider where your third\-party code repository is configured\. Currently, the valid provider type is Bitbucket\.  
*Required*: Yes  
*Type*: String  
*Allowed Values*: `Bitbucket`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return Values<a name="aws-resource-codestarconnections-connection-return-values"></a>

### Ref<a name="aws-resource-codestarconnections-connection-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the Amazon Resource Name \(ARN\) of the connection\. The ARN is used as the connection reference when the connection is shared between AWS services\. For example:

 `arn:aws:codestar-connections:us-west-2:123456789012:connection/39e4c34d-e13a-4e94-a886-ea67651bf042` 

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-codestarconnections-connection-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-codestarconnections-connection-return-values-fn--getatt-fn--getatt"></a>

`ConnectionArn`  <a name="ConnectionArn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the connection\. The ARN is used as the connection reference when the connection is shared between AWS services\. For example: `arn:aws:codestar-connections:us-west-2:123456789012:connection/39e4c34d-e13a-4e94-a886-ea67651bf042`\.

`ConnectionStatus`  <a name="ConnectionStatus-fn::getatt"></a>
The current status of the connection\. For example: `PENDING`, `AVAILABLE`, or `ERROR`\.

`OwnerAccountId`  <a name="OwnerAccountId-fn::getatt"></a>
The AWS account ID of the owner of the connection\. For Bitbucket, this is the account ID of the owner of the Bitbucket repository\. For example: `123456789012`\.

## Examples<a name="aws-resource-codestarconnections-connection--examples"></a>

### Bitbucket Connection Configuration<a name="aws-resource-codestarconnections-connection--examples--Bitbucket_Connection_Configuration"></a>

The following example creates a Connection with Bitbucket\.

#### JSON<a name="aws-resource-codestarconnections-connection--examples--Bitbucket_Connection_Configuration--json"></a>

```
{
    "AWSTemplateFormatVersion": "2010-09-09",
    "Resources": {
        "SampleConnection": {
            "Type": "AWS::CodeStarConnections::Connection",
            "Properties": {
                "ConnectionName": "MyConnection",
                "ProviderType": "Bitbucket"
            }
        }
    }
}
```

#### YAML<a name="aws-resource-codestarconnections-connection--examples--Bitbucket_Connection_Configuration--yaml"></a>

```
 AWSTemplateFormatVersion: 2010-09-09
 Resources:
    SampleConnection:
        Type: AWS::CodeStarConnections::Connection
        Properties:
            ConnectionName: MyConnection
            ProviderType: Bitbucket
```