# AWS::Transfer::Server<a name="aws-resource-transfer-server"></a>

Instantiates an autoscaling virtual server based on Secure File Transfer Protocol \(SFTP\) in AWS\. When you make updates to your server or when you work with users, use the service\-generated `ServerId` property that is assigned to the newly created server\.

## Syntax<a name="aws-resource-transfer-server-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-transfer-server-syntax.json"></a>

```
{
  "Type" : "AWS::Transfer::Server",
  "Properties" : {
      "[EndpointDetails](#cfn-transfer-server-endpointdetails)" : [EndpointDetails](aws-properties-transfer-server-endpointdetails.md),
      "[EndpointType](#cfn-transfer-server-endpointtype)" : String,
      "[IdentityProviderDetails](#cfn-transfer-server-identityproviderdetails)" : [IdentityProviderDetails](aws-properties-transfer-server-identityproviderdetails.md),
      "[IdentityProviderType](#cfn-transfer-server-identityprovidertype)" : String,
      "[LoggingRole](#cfn-transfer-server-loggingrole)" : String,
      "[Tags](#cfn-transfer-server-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-transfer-server-syntax.yaml"></a>

```
Type: AWS::Transfer::Server
Properties:
  [EndpointDetails](#cfn-transfer-server-endpointdetails):
    [EndpointDetails](aws-properties-transfer-server-endpointdetails.md)
  [EndpointType](#cfn-transfer-server-endpointtype): String
  [IdentityProviderDetails](#cfn-transfer-server-identityproviderdetails):
    [IdentityProviderDetails](aws-properties-transfer-server-identityproviderdetails.md)
  [IdentityProviderType](#cfn-transfer-server-identityprovidertype): String
  [LoggingRole](#cfn-transfer-server-loggingrole): String
  [Tags](#cfn-transfer-server-tags):
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-transfer-server-properties"></a>

`EndpointDetails`  <a name="cfn-transfer-server-endpointdetails"></a>
The virtual private cloud \(VPC\) endpoint settings that you want to configure for your SFTP server\. This parameter is required when you specify a value for the `EndpointType` parameter\.
*Required*: No
*Type*: [EndpointDetails](aws-properties-transfer-server-endpointdetails.md)
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EndpointType`  <a name="cfn-transfer-server-endpointtype"></a>
The type of VPC endpoint that you want your SFTP server to connect to\. If you connect to a VPC endpoint, your SFTP server isn't accessible over the public internet\.
*Required*: Conditional
*Type*: String
*Allowed Values*: `PUBLIC | VPC_ENDPOINT`
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IdentityProviderDetails`  <a name="cfn-transfer-server-identityproviderdetails"></a>
This parameter is required when the `IdentityProviderType` is set to `API_GATEWAY`\. Accepts an array containing all of the information required to call a customer\-supplied authentication API, including the API Gateway URL\. This property is not required when the `IdentityProviderType` is set to `SERVICE_MANAGED`\.
*Required*: No
*Type*: [IdentityProviderDetails](aws-properties-transfer-server-identityproviderdetails.md)
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IdentityProviderType`  <a name="cfn-transfer-server-identityprovidertype"></a>
Specifies the mode of authentication for the SFTP server\. The default value is `SERVICE_MANAGED`, which allows you to store and access SFTP user credentials within the AWS Transfer for SFTP service\. Use the `API_GATEWAY` value to integrate with an identity provider of your choosing\. The `API_GATEWAY` setting requires you to provide an API Gateway endpoint URL to call for authentication using the `IdentityProviderDetails` parameter\.
*Required*: No
*Type*: String
*Allowed Values*: `API_GATEWAY | SERVICE_MANAGED`
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`LoggingRole`  <a name="cfn-transfer-server-loggingrole"></a>
A value that allows the service to write your SFTP users' activity to your Amazon CloudWatch logs for monitoring and auditing purposes\.
*Required*: No
*Type*: String
*Pattern*: `arn:.*role/.*`
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-transfer-server-tags"></a>
Key\-value pairs that can be used to group and search for servers\.
*Required*: No
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
*Maximum*: `50`
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return Values<a name="aws-resource-transfer-server-return-values"></a>

### Ref<a name="aws-resource-transfer-server-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the ServerId, such as `s-01234567890abcdef`, and the server ARN, such as `arn:aws:transfer:us-east-1:123456789012:server/s-01234567890abcdef`\.

### Fn::GetAtt<a name="aws-resource-transfer-server-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-transfer-server-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The Amazon Resource Name associated with the AWS Transfer SFTP server, in the form `arn:aws:transfer:region:account-id:server/server-id/`\.
An example of a server ARN is: `arn:aws:transfer:us-east-1:123456789012:server/s-01234567890abcdef`\.

`ServerId`  <a name="ServerId-fn::getatt"></a>
The service\-assigned ID of the SFTP server that is created\.
An example `ServerId` is `s-01234567890abcdef`\.
