# AWS::Transfer::Server<a name="aws-resource-transfer-server"></a>

Instantiates an auto\-scaling virtual server based on the selected file transfer protocol in AWS\. When you make updates to your file transfer protocol\-enabled server or when you work with users, use the service\-generated `ServerId` property that is assigned to the newly created server\.

## Syntax<a name="aws-resource-transfer-server-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-transfer-server-syntax.json"></a>

```
{
  "Type" : "AWS::Transfer::Server",
  "Properties" : {
      "[Certificate](#cfn-transfer-server-certificate)" : String,
      "[Domain](#cfn-transfer-server-domain)" : String,
      "[EndpointDetails](#cfn-transfer-server-endpointdetails)" : EndpointDetails,
      "[EndpointType](#cfn-transfer-server-endpointtype)" : String,
      "[IdentityProviderDetails](#cfn-transfer-server-identityproviderdetails)" : IdentityProviderDetails,
      "[IdentityProviderType](#cfn-transfer-server-identityprovidertype)" : String,
      "[LoggingRole](#cfn-transfer-server-loggingrole)" : String,
      "[PostAuthenticationLoginBanner](#cfn-transfer-server-postauthenticationloginbanner)" : String,
      "[PreAuthenticationLoginBanner](#cfn-transfer-server-preauthenticationloginbanner)" : String,
      "[ProtocolDetails](#cfn-transfer-server-protocoldetails)" : ProtocolDetails,
      "[Protocols](#cfn-transfer-server-protocols)" : [ Protocol, ... ],
      "[SecurityPolicyName](#cfn-transfer-server-securitypolicyname)" : String,
      "[Tags](#cfn-transfer-server-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ],
      "[WorkflowDetails](#cfn-transfer-server-workflowdetails)" : WorkflowDetails
    }
}
```

### YAML<a name="aws-resource-transfer-server-syntax.yaml"></a>

```
Type: AWS::Transfer::Server
Properties: 
  [Certificate](#cfn-transfer-server-certificate): String
  [Domain](#cfn-transfer-server-domain): String
  [EndpointDetails](#cfn-transfer-server-endpointdetails): 
    EndpointDetails
  [EndpointType](#cfn-transfer-server-endpointtype): String
  [IdentityProviderDetails](#cfn-transfer-server-identityproviderdetails): 
    IdentityProviderDetails
  [IdentityProviderType](#cfn-transfer-server-identityprovidertype): String
  [LoggingRole](#cfn-transfer-server-loggingrole): String
  [PostAuthenticationLoginBanner](#cfn-transfer-server-postauthenticationloginbanner): String
  [PreAuthenticationLoginBanner](#cfn-transfer-server-preauthenticationloginbanner): String
  [ProtocolDetails](#cfn-transfer-server-protocoldetails): 
    ProtocolDetails
  [Protocols](#cfn-transfer-server-protocols): 
    - Protocol
  [SecurityPolicyName](#cfn-transfer-server-securitypolicyname): String
  [Tags](#cfn-transfer-server-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
  [WorkflowDetails](#cfn-transfer-server-workflowdetails): 
    WorkflowDetails
```

## Properties<a name="aws-resource-transfer-server-properties"></a>

`Certificate`  <a name="cfn-transfer-server-certificate"></a>
The Amazon Resource Name \(ARN\) of the AWS Certificate Manager \(ACM\) certificate\. Required when `Protocols` is set to `FTPS`\.  
To request a new public certificate, see [Request a public certificate](https://docs.aws.amazon.com/acm/latest/userguide/gs-acm-request-public.html) in the * AWS Certificate Manager User Guide*\.  
To import an existing certificate into ACM, see [Importing certificates into ACM](https://docs.aws.amazon.com/acm/latest/userguide/import-certificate.html) in the * AWS Certificate Manager User Guide*\.  
To request a private certificate to use FTPS through private IP addresses, see [Request a private certificate](https://docs.aws.amazon.com/acm/latest/userguide/gs-acm-request-private.html) in the * AWS Certificate Manager User Guide*\.  
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

`Domain`  <a name="cfn-transfer-server-domain"></a>
Specifies the domain of the storage system that is used for file transfers\.  
*Required*: No  
*Type*: String  
*Allowed values*: `EFS | S3`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`EndpointDetails`  <a name="cfn-transfer-server-endpointdetails"></a>
The virtual private cloud \(VPC\) endpoint settings that are configured for your server\. When you host your endpoint within your VPC, you can make your endpoint accessible only to resources within your VPC, or you can attach Elastic IP addresses and make your endpoint accessible to clients over the internet\. Your VPC's default security groups are automatically assigned to your endpoint\.  
*Required*: No  
*Type*: [EndpointDetails](aws-properties-transfer-server-endpointdetails.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EndpointType`  <a name="cfn-transfer-server-endpointtype"></a>
The type of endpoint that you want your server to use\. You can choose to make your server's endpoint publicly accessible \(PUBLIC\) or host it inside your VPC\. With an endpoint that is hosted in a VPC, you can restrict access to your server and resources only within your VPC or choose to make it internet facing by attaching Elastic IP addresses directly to it\.  
*Required*: No  
*Type*: String  
*Allowed values*: `PUBLIC | VPC | VPC_ENDPOINT`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IdentityProviderDetails`  <a name="cfn-transfer-server-identityproviderdetails"></a>
Required when `IdentityProviderType` is set to `AWS_DIRECTORY_SERVICE` or `API_GATEWAY`\. Accepts an array containing all of the information required to use a directory in `AWS_DIRECTORY_SERVICE` or invoke a customer\-supplied authentication API, including the API Gateway URL\. Not required when `IdentityProviderType` is set to `SERVICE_MANAGED`\.  
*Required*: No  
*Type*: [IdentityProviderDetails](aws-properties-transfer-server-identityproviderdetails.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IdentityProviderType`  <a name="cfn-transfer-server-identityprovidertype"></a>
The mode of authentication for a server\. The default value is `SERVICE_MANAGED`, which allows you to store and access user credentials within the AWS Transfer Family service\.  
Use `AWS_DIRECTORY_SERVICE` to provide access to Active Directory groups in AWS Directory Service for Microsoft Active Directory or Microsoft Active Directory in your on\-premises environment or in AWS using AD Connector\. This option also requires you to provide a Directory ID by using the `IdentityProviderDetails` parameter\.  
Use the `API_GATEWAY` value to integrate with an identity provider of your choosing\. The `API_GATEWAY` setting requires you to provide an Amazon API Gateway endpoint URL to call for authentication by using the `IdentityProviderDetails` parameter\.  
Use the `AWS_LAMBDA` value to directly use an AWS Lambda function as your identity provider\. If you choose this value, you must specify the ARN for the Lambda function in the `Function` parameter or the `IdentityProviderDetails` data type\.  
*Required*: No  
*Type*: String  
*Allowed values*: `API_GATEWAY | AWS_DIRECTORY_SERVICE | AWS_LAMBDA | SERVICE_MANAGED`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`LoggingRole`  <a name="cfn-transfer-server-loggingrole"></a>
The Amazon Resource Name \(ARN\) of the AWS Identity and Access Management \(IAM\) role that allows a server to turn on Amazon CloudWatch logging for Amazon S3 or Amazon EFSevents\. When set, you can view user activity in your CloudWatch logs\.  
*Required*: No  
*Type*: String  
*Minimum*: `20`  
*Maximum*: `2048`  
*Pattern*: `arn:.*role/.*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PostAuthenticationLoginBanner`  <a name="cfn-transfer-server-postauthenticationloginbanner"></a>
Specifies a string to display when users connect to a server\. This string is displayed after the user authenticates\.  
The SFTP protocol does not support post\-authentication display banners\.
*Required*: No  
*Type*: String  
*Maximum*: `512`  
*Pattern*: `[\x09-\x0D\x20-\x7E]*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PreAuthenticationLoginBanner`  <a name="cfn-transfer-server-preauthenticationloginbanner"></a>
Specifies a string to display when users connect to a server\. This string is displayed before the user authenticates\. For example, the following banner displays details about using the system:  
 `This system is for the use of authorized users only. Individuals using this computer system without authority, or in excess of their authority, are subject to having all of their activities on this system monitored and recorded by system personnel.`   
*Required*: No  
*Type*: String  
*Maximum*: `512`  
*Pattern*: `[\x09-\x0D\x20-\x7E]*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ProtocolDetails`  <a name="cfn-transfer-server-protocoldetails"></a>
The protocol settings that are configured for your server\.  
+  To indicate passive mode \(for FTP and FTPS protocols\), use the `PassiveIp` parameter\. Enter a single dotted\-quad IPv4 address, such as the external IP address of a firewall, router, or load balancer\. 
+ To ignore the error that is generated when the client attempts to use the `SETSTAT` command on a file that you are uploading to an Amazon S3 bucket, use the `SetStatOption` parameter\. To have the AWS Transfer Family server ignore the `SETSTAT` command and upload files without needing to make any changes to your SFTP client, set the value to `ENABLE_NO_OP`\. If you set the `SetStatOption` parameter to `ENABLE_NO_OP`, Transfer Family generates a log entry to Amazon CloudWatch Logs, so that you can determine when the client is making a `SETSTAT` call\.
+ To determine whether your AWS Transfer Family server resumes recent, negotiated sessions through a unique session ID, use the `TlsSessionResumptionMode` parameter\.
+  `As2Transports` indicates the transport method for the AS2 messages\. Currently, only HTTP is supported\.
*Required*: No  
*Type*: [ProtocolDetails](aws-properties-transfer-server-protocoldetails.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Protocols`  <a name="cfn-transfer-server-protocols"></a>
Specifies the file transfer protocol or protocols over which your file transfer protocol client can connect to your server's endpoint\. The available protocols are:  
+  `SFTP` \(Secure Shell \(SSH\) File Transfer Protocol\): File transfer over SSH
+  `FTPS` \(File Transfer Protocol Secure\): File transfer with TLS encryption
+  `FTP` \(File Transfer Protocol\): Unencrypted file transfer
+  `AS2` \(Applicability Statement 2\): used for transporting structured business\-to\-business data
+ If you select `FTPS`, you must choose a certificate stored in AWS Certificate Manager \(ACM\) which is used to identify your server when clients connect to it over FTPS\.
+ If `Protocol` includes either `FTP` or `FTPS`, then the `EndpointType` must be `VPC` and the `IdentityProviderType` must be either `AWS_DIRECTORY_SERVICE`, `AWS_LAMBDA`, or `API_GATEWAY`\.
+ If `Protocol` includes `FTP`, then `AddressAllocationIds` cannot be associated\.
+ If `Protocol` is set only to `SFTP`, the `EndpointType` can be set to `PUBLIC` and the `IdentityProviderType` can be set any of the supported identity types: `SERVICE_MANAGED`, `AWS_DIRECTORY_SERVICE`, `AWS_LAMBDA`, or `API_GATEWAY`\.
+ If `Protocol` includes `AS2`, then the `EndpointType` must be `VPC`, and domain must be Amazon S3\.
*Required*: No  
*Type*: List of [Protocol](aws-properties-transfer-server-protocol.md)  
*Maximum*: `4`  
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

`WorkflowDetails`  <a name="cfn-transfer-server-workflowdetails"></a>
Specifies the workflow ID for the workflow to assign and the execution role that's used for executing the workflow\.  
In addition to a workflow to execute when a file is uploaded completely, `WorkflowDetails` can also contain a workflow ID \(and execution role\) for a workflow to execute on partial upload\. A partial upload occurs when a file is open when the session disconnects\.  
*Required*: No  
*Type*: [WorkflowDetails](aws-properties-transfer-server-workflowdetails.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-transfer-server-return-values"></a>

### Ref<a name="aws-resource-transfer-server-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the server ARN, such as `arn:aws:transfer:us-east-1:123456789012:server/s-01234567890abcdef`\.

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