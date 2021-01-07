# AWS::Transfer::Server<a name="aws-resource-transfer-server"></a>

The `AWS::Transfer::Server` resource instantiates an autoscaling virtual server based on a file transfer protocol in AWS\. When you make updates to your server or when you work with users, use the service\-generated `ServerId` property that is assigned to the newly created server\.

## Syntax<a name="aws-resource-transfer-server-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-transfer-server-syntax.json"></a>

```
{
  "Type" : "AWS::Transfer::Server",
  "Properties" : {
      "[Certificate](#cfn-transfer-server-certificate)" : String,
      "[EndpointDetails](#cfn-transfer-server-endpointdetails)" : EndpointDetails,
      "[EndpointType](#cfn-transfer-server-endpointtype)" : String,
      "[IdentityProviderDetails](#cfn-transfer-server-identityproviderdetails)" : IdentityProviderDetails,
      "[IdentityProviderType](#cfn-transfer-server-identityprovidertype)" : String,
      "[LoggingRole](#cfn-transfer-server-loggingrole)" : String,
      "[Protocols](#cfn-transfer-server-protocols)" : [ Protocol, ... ],
      "[SecurityPolicyName](#cfn-transfer-server-securitypolicyname)" : String,
      "[Tags](#cfn-transfer-server-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-transfer-server-syntax.yaml"></a>

```
Type: AWS::Transfer::Server
Properties: 
  [Certificate](#cfn-transfer-server-certificate): String
  [EndpointDetails](#cfn-transfer-server-endpointdetails): 
    EndpointDetails
  [EndpointType](#cfn-transfer-server-endpointtype): String
  [IdentityProviderDetails](#cfn-transfer-server-identityproviderdetails): 
    IdentityProviderDetails
  [IdentityProviderType](#cfn-transfer-server-identityprovidertype): String
  [LoggingRole](#cfn-transfer-server-loggingrole): String
  [Protocols](#cfn-transfer-server-protocols): 
    - Protocol
  [SecurityPolicyName](#cfn-transfer-server-securitypolicyname): String
  [Tags](#cfn-transfer-server-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-transfer-server-properties"></a>

`Certificate`  <a name="cfn-transfer-server-certificate"></a>
The Amazon Resource Name \(ARN\) of the AWS Certificate Manager \(ACM\) certificate\. Required when `Protocols` is set to `FTPS`\.  
To request a new public certificate, see [Request a public certificate](https://docs.aws.amazon.com/acm/latest/userguide/gs-acm-request-public.html) in the * AWS Certificate Manager User Guide*\.  
To import an existing certificate into ACM, see [Importing certificates into ACM](https://docs.aws.amazon.com/acm/latest/userguide/import-certificate.html) in the * AWS Certificate Manager User Guide*\.  
To request a private certificate to use FTPS through private IP addresses, see [Creating and managing a Private CA](https://docs.aws.amazon.com/acm/latest/userguide/import-certificate.html) in the * AWS Certificate Manager User Guide*\.  
Certificates with the following cryptographic algorithms and key sizes are supported:  
+ 2048\-bit RSA \(RSA\_2048\)
+ 4096\-bit RSA \(RSA\_4096\)
+ Elliptic Prime Curve 256 bit \(EC\_prime256v1\)
+ Elliptic Prime Curve 384 bit \(EC\_secp384r1\)
+ Elliptic Prime Curve 521 bit \(EC\_secp521r1\)
The certificate must be a valid SSL/TLS X\.509 version 3 certificate with FQDN or IP address specified and information about the issuer\.
*Required*: No  
*Type*: String  
*Maximum*: `1600`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EndpointDetails`  <a name="cfn-transfer-server-endpointdetails"></a>
The virtual private cloud \(VPC\) endpoint settings that are configured for your server\. When you host your endpoint within your VPC, you can make it accessible only to resources within your VPC, or you can attach Elastic IPs and make it accessible to clients over the internet\. You VPC's default security groups are automatically assigned to your endpoint\.  
*Required*: No  
*Type*: [EndpointDetails](aws-properties-transfer-server-endpointdetails.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EndpointType`  <a name="cfn-transfer-server-endpointtype"></a>
The type of VPC endpoint that you want your server to connect to\. You can choose to connect to the public internet or a virtual private cloud \(VPC\) endpoint\. With a VPC endpoint, you can restrict access to your server and resources only within your VPC\.  
It is recommended that you use `VPC` as the `EndpointType`\. With this endpoint type, you have the option to directly associate up to three Elastic IPv4 addresses \(BYO IP included\) with your server's endpoint and use VPC security groups to restrict traffic by the client's public IP address\. This is not possible with `EndpointType` set to `VPC_ENDPOINT`\.
*Required*: Conditional  
*Type*: String  
*Allowed values*: `PUBLIC | VPC | VPC_ENDPOINT`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IdentityProviderDetails`  <a name="cfn-transfer-server-identityproviderdetails"></a>
Required when `IdentityProviderType` is set to `API_GATEWAY`\. Accepts an array containing all of the information required to call a customer\-supplied authentication API, including the API Gateway URL\. Not required when `IdentityProviderType` is set to `SERVICE_MANAGED`\.  
*Required*: No  
*Type*: [IdentityProviderDetails](aws-properties-transfer-server-identityproviderdetails.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IdentityProviderType`  <a name="cfn-transfer-server-identityprovidertype"></a>
Specifies the mode of authentication for a server\. The default value is `SERVICE_MANAGED`, which allows you to store and access user credentials within the AWS Transfer Family service\. Use the `API_GATEWAY` value to integrate with an identity provider of your choosing\. The `API_GATEWAY` setting requires you to provide an API Gateway endpoint URL to call for authentication using the `IdentityProviderDetails` parameter\.  
*Required*: No  
*Type*: String  
*Allowed values*: `API_GATEWAY | SERVICE_MANAGED`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`LoggingRole`  <a name="cfn-transfer-server-loggingrole"></a>
Allows the service to write your users' activity to your Amazon CloudWatch logs for monitoring and auditing purposes\.  
*Required*: No  
*Type*: String  
*Minimum*: `20`  
*Maximum*: `2048`  
*Pattern*: `arn:.*role/.*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Protocols`  <a name="cfn-transfer-server-protocols"></a>
Specifies the file transfer protocol or protocols over which your file transfer protocol client can connect to your server's endpoint\.  
*Required*: No  
*Type*: List of [Protocol](aws-properties-transfer-server-protocol.md)  
*Maximum*: `3`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SecurityPolicyName`  <a name="cfn-transfer-server-securitypolicyname"></a>
Specifies the name of the security policy that is attached to the server\.  
*Required*: No  
*Type*: String  
*Maximum*: `100`  
*Pattern*: `TransferSecurityPolicy-.+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-transfer-server-tags"></a>
Key\-value pairs that can be used to group and search for servers\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Maximum*: `50`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-transfer-server-return-values"></a>

### Ref<a name="aws-resource-transfer-server-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the ServerId, such as `s-01234567890abcdef`, and the server ARN, such as `arn:aws:transfer:us-east-1:123456789012:server/s-01234567890abcdef`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-transfer-server-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-transfer-server-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The Amazon Resource Name associated with the server, in the form `arn:aws:transfer:region:account-id:server/server-id/`\.  
An example of a server ARN is: `arn:aws:transfer:us-east-1:123456789012:server/s-01234567890abcdef`\.

`ServerId`  <a name="ServerId-fn::getatt"></a>
The service\-assigned ID of the server that is created\.  
An example `ServerId` is `s-01234567890abcdef`\.

## Examples<a name="aws-resource-transfer-server--examples"></a>



### Create a server with VPC hosted endpoint type<a name="aws-resource-transfer-server--examples--Create_a_server_with_VPC_hosted_endpoint_type"></a>

The following example creates a Secure Shell \(SSH\) File Transfer Protocol \(SFTP\)\-enabled server using a VPC hosted endpoint type with a custom identity provider, a CloudWatch logging role, security policy, and tags\.

#### JSON<a name="aws-resource-transfer-server--examples--Create_a_server_with_VPC_hosted_endpoint_type--json"></a>

```
{
    "AWSTemplateFormatVersion": "2010-09-09",
    "Description": "creates SFTP Server",
    "Resources": {
        "MyTransferServer": {
            "Type": "AWS::Transfer::Server",
            "Properties": {
                "EndpointDetails": {
                    "AddressAllocationIds": [
                        "AddressAllocationId-1",
                        "AddressAllocationId-2"
                    ],
                    "SubnetIds": [
                        "SubnetId-1",
                        "SubnetId-2"
                    ],
                    "VpcId": "VpcId"
                },
                "EndpointType": "VPC",
                "LoggingRole": "Logging-Role-ARN",
                "Protocols": [
                    "SFTP"
                ],
                "SecurityPolicyName": "Security-Policy-Name",
                "IdentityProviderDetails": {
                    "InvocationRole": "Invocation-Role-ARN",
                    "Url": "API_GATEWAY-Invocation-URL"
                },
                "IdentityProviderType": "API_GATEWAY",
                "Tags": [
                    {
                        "Key": "KeyName",
                        "Value": "ValueName"
                    }
                ]
            }
        }
    }
}
```

#### YAML<a name="aws-resource-transfer-server--examples--Create_a_server_with_VPC_hosted_endpoint_type--yaml"></a>

```
AWSTemplateFormatVersion: '2010-09-09'
Description: creates SFTP Server
Resources:
    MyTransferServer:
      Type : AWS::Transfer::Server
      Properties :
        EndpointDetails:
          AddressAllocationIds:
            - AddressAllocationId-1
            - AddressAllocationId-2
          SubnetIds:
            - SubnetId-1
            - SubnetId-2
          VpcId: VpcId
        EndpointType: VPC
        LoggingRole: Logging-Role-ARN
        Protocols: 
            - SFTP
        SecurityPolicyName: Security-Policy-Name
        IdentityProviderDetails: 
            InvocationRole: Invocation-Role-ARN
            Url: API_GATEWAY-Invocation-URL
        IdentityProviderType: API_GATEWAY
        Tags: 
          - Key: KeyName
            Value: ValueName
```

## See also<a name="aws-resource-transfer-server--seealso"></a>

[CreateServer](https://docs.aws.amazon.com/transfer/latest/userguide/API_CreateServer.html) in the *AWS Transfer Family User Guide*\.