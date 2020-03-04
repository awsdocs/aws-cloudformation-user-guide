# AWS::Transfer::Server<a name="aws-resource-transfer-server"></a>

The `AWS::Transfer::Server` resource instantiates an autoscaling virtual server based on Secure File Transfer Protocol \(SFTP\) in AWS\. When you make updates to your server or when you work with users, use the service\-generated `ServerId` property that is assigned to the newly created server\.

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
The virtual private cloud \(VPC\) endpoint settings that are configured for your SFTP server\. When you host your endpoint within your VPC, you can make it accessible only to resources within your VPC, or you can attach Elastic IPs and make it accessible to clients over the internet\. You VPC's default security groups are automatically assigned to your endpoint\.  
*Required*: No  
*Type*: [EndpointDetails](aws-properties-transfer-server-endpointdetails.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EndpointType`  <a name="cfn-transfer-server-endpointtype"></a>
The type of VPC endpoint that you want your SFTP server to connect to\. You can choose to connect to the public internet or a virtual private cloud \(VPC\) endpoint\. With a VPC endpoint, you can restrict access to your SFTP server and resources only within your VPC\.  
It is recommended that you use `VPC` as the `EndpointType`\. With this endpoint type, you have the option to directly associate up to three Elastic IPv4 addresses \(BYO IP included\) with your server's endpoint and use VPC security groups to restrict traffic by the client's public IP address\. This is not possible with `EndpointType` set to `VPC_ENDPOINT`\.
*Required*: Conditional  
*Type*: String  
*Allowed Values*: `PUBLIC | VPC | VPC_ENDPOINT`  
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
*Minimum*: `20`  
*Maximum*: `2048`  
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

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

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

## Examples<a name="aws-resource-transfer-server--examples"></a>

### SFTP Server with VPC Endpoint Type<a name="aws-resource-transfer-server--examples--SFTP_Server_with_VPC_Endpoint_Type"></a>

The following example creates a new SFTP server using a VPC endpoint type\.

#### JSON<a name="aws-resource-transfer-server--examples--SFTP_Server_with_VPC_Endpoint_Type--json"></a>

```
{
   "MySFTPServer": {
        "Type": "AWS::Transfer::Server",
        "Properties": {
            "EndpointDetails": {
                "AddressAllocationIds": [
                    {
                        "Ref": "MySFTPServerAddressAllocationId01"
                    },
                    {
                        "Ref": "MySFTPServerAddressAllocationId02"
                    }
                ],
                "SubnetIds": [
                    {
                        "Ref": "MySFTPServerSubnet01"
                    },
                    {
                        "Ref": "MySFTPServerSubnet02"
                    }
                ]
            },
            "EndpointType": "VPC",
            "IdentityProviderDetails": {
                "InvocationRole": {
                    "Ref": "MySFTPServerIdentityProviderInvocationRole"
                },
                "Url": {
                    "Ref": "MySFTPServerIdentityProviderUrl"
                }
            },
            "IdentityProviderType": "API_GATEWAY",
            "LoggingRole": {
                "Ref": "MySFTPServerLoggingRole"
            },
            "Tags": [
                {
                    "Key": "Name",
                    "Value": "MySFTPServer"
                }
            ]
        }
    }
}
```

#### YAML<a name="aws-resource-transfer-server--examples--SFTP_Server_with_VPC_Endpoint_Type--yaml"></a>

```
MySFTPServer:
  Type : AWS::Transfer::Server
  Properties :
    EndpointDetails:
      AddressAllocationIds:
        - Ref: MySFTPServerAddressAllocationId01
        - Ref: MySFTPServerAddressAllocationId02
      SubnetIds:
        - Ref: MySFTPServerSubnet01
        - Ref: MySFTPServerSubnet02
    EndpointType: VPC
    IdentityProviderDetails: 
      InvocationRole:
        Ref: MySFTPServerIdentityProviderInvocationRole
      Url:
        Ref: MySFTPServerIdentityProviderUrl
    IdentityProviderType: API_GATEWAY
    LoggingRole:
      Ref: MySFTPServerLoggingRole
    Tags: 
      - Key: Name
        Value: MySFTPServer
```

## See Also<a name="aws-resource-transfer-server--seealso"></a>

[CreateServer](https://docs.aws.amazon.com/transfer/latest/userguide/API_CreateServer.html) in the *AWS Transfer for SFTP User Guide*\.