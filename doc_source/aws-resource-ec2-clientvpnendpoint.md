# AWS::EC2::ClientVpnEndpoint<a name="aws-resource-ec2-clientvpnendpoint"></a>

Specifies a Client VPN endpoint\. A Client VPN endpoint is the resource you create and configure to enable and manage client VPN sessions\. It is the destination endpoint at which all client VPN sessions are terminated\.

## Syntax<a name="aws-resource-ec2-clientvpnendpoint-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ec2-clientvpnendpoint-syntax.json"></a>

```
{
  "Type" : "AWS::EC2::ClientVpnEndpoint",
  "Properties" : {
      "[AuthenticationOptions](#cfn-ec2-clientvpnendpoint-authenticationoptions)" : [ [ClientAuthenticationRequest](aws-properties-ec2-clientvpnendpoint-clientauthenticationrequest.md), ... ],
      "[ClientCidrBlock](#cfn-ec2-clientvpnendpoint-clientcidrblock)" : String,
      "[ConnectionLogOptions](#cfn-ec2-clientvpnendpoint-connectionlogoptions)" : [ConnectionLogOptions](aws-properties-ec2-clientvpnendpoint-connectionlogoptions.md),
      "[Description](#cfn-ec2-clientvpnendpoint-description)" : String,
      "[DnsServers](#cfn-ec2-clientvpnendpoint-dnsservers)" : [ String, ... ],
      "[ServerCertificateArn](#cfn-ec2-clientvpnendpoint-servercertificatearn)" : String,
      "[TagSpecifications](#cfn-ec2-clientvpnendpoint-tagspecifications)" : [ [TagSpecification](aws-properties-ec2-clientvpnendpoint-tagspecification.md), ... ],
      "[TransportProtocol](#cfn-ec2-clientvpnendpoint-transportprotocol)" : String
    }
}
```

### YAML<a name="aws-resource-ec2-clientvpnendpoint-syntax.yaml"></a>

```
Type: AWS::EC2::ClientVpnEndpoint
Properties: 
  [AuthenticationOptions](#cfn-ec2-clientvpnendpoint-authenticationoptions): 
    - [ClientAuthenticationRequest](aws-properties-ec2-clientvpnendpoint-clientauthenticationrequest.md)
  [ClientCidrBlock](#cfn-ec2-clientvpnendpoint-clientcidrblock): String
  [ConnectionLogOptions](#cfn-ec2-clientvpnendpoint-connectionlogoptions): 
    [ConnectionLogOptions](aws-properties-ec2-clientvpnendpoint-connectionlogoptions.md)
  [Description](#cfn-ec2-clientvpnendpoint-description): String
  [DnsServers](#cfn-ec2-clientvpnendpoint-dnsservers): 
    - String
  [ServerCertificateArn](#cfn-ec2-clientvpnendpoint-servercertificatearn): String
  [TagSpecifications](#cfn-ec2-clientvpnendpoint-tagspecifications): 
    - [TagSpecification](aws-properties-ec2-clientvpnendpoint-tagspecification.md)
  [TransportProtocol](#cfn-ec2-clientvpnendpoint-transportprotocol): String
```

## Properties<a name="aws-resource-ec2-clientvpnendpoint-properties"></a>

`AuthenticationOptions`  <a name="cfn-ec2-clientvpnendpoint-authenticationoptions"></a>
Information about the authentication method to be used to authenticate clients\.  
*Required*: Yes  
*Type*: List of [ClientAuthenticationRequest](aws-properties-ec2-clientvpnendpoint-clientauthenticationrequest.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ClientCidrBlock`  <a name="cfn-ec2-clientvpnendpoint-clientcidrblock"></a>
The IPv4 address range, in CIDR notation, from which to assign client IP addresses\. The address range cannot overlap with the local CIDR of the VPC in which the associated subnet is located, or the routes that you add manually\. The address range cannot be changed after the Client VPN endpoint has been created\. The CIDR block should be /22 or greater\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ConnectionLogOptions`  <a name="cfn-ec2-clientvpnendpoint-connectionlogoptions"></a>
Information about the client connection logging options\.  
If you enable client connection logging, data about client connections is sent to a Cloudwatch Logs log stream\. The following information is logged:  
+ Client connection requests
+ Client connection results \(successful and unsuccessful\)
+ Reasons for unsuccessful client connection requests
+ Client connection termination time
*Required*: Yes  
*Type*: [ConnectionLogOptions](aws-properties-ec2-clientvpnendpoint-connectionlogoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Description`  <a name="cfn-ec2-clientvpnendpoint-description"></a>
A brief description of the Client VPN endpoint\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DnsServers`  <a name="cfn-ec2-clientvpnendpoint-dnsservers"></a>
Information about the DNS servers to be used for DNS resolution\. A Client VPN endpoint can have up to two DNS servers\. If no DNS server is specified, the DNS address of the VPC that is to be associated with Client VPN endpoint is used as the DNS server\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ServerCertificateArn`  <a name="cfn-ec2-clientvpnendpoint-servercertificatearn"></a>
The ARN of the server certificate\. For more information, see the [AWS Certificate Manager User Guide](https://docs.aws.amazon.com/acm/latest/userguide/)\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TagSpecifications`  <a name="cfn-ec2-clientvpnendpoint-tagspecifications"></a>
The tags to apply to the Client VPN endpoint during creation\.  
*Required*: No  
*Type*: List of [TagSpecification](aws-properties-ec2-clientvpnendpoint-tagspecification.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`TransportProtocol`  <a name="cfn-ec2-clientvpnendpoint-transportprotocol"></a>
The transport protocol to be used by the VPN session\.  
Default value: `udp`   
*Required*: No  
*Type*: String  
*Allowed Values*: `tcp | udp`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return Values<a name="aws-resource-ec2-clientvpnendpoint-return-values"></a>

### Ref<a name="aws-resource-ec2-clientvpnendpoint-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the Client VPN endpoint ID\. For example: `cvpn-endpoint-1234567890abcdef0`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-resource-ec2-clientvpnendpoint--examples"></a>

### Creating a Client VPN endpoint<a name="aws-resource-ec2-clientvpnendpoint--examples--Creating_a_Client_VPN_endpoint"></a>

The following example creates a Client VPN endpoint that uses Active Directory authentication and assigns client IP addresses from the `10.0.0.0/22` CIDR range\.

#### YAML<a name="aws-resource-ec2-clientvpnendpoint--examples--Creating_a_Client_VPN_endpoint--yaml"></a>

```
myClientVpnEndpoint:
  Type: AWS::EC2::ClientVpnEndpoint
  Properties: 
    AuthenticationOptions:
    - Type: "directory-service-authentication"
      ActiveDirectory:
        DirectoryId: d-926example
    ClientCidrBlock: "10.0.0.0/22"
    ConnectionLogOptions: 
      Enabled: false
    Description: "My Client VPN Endpoint"
    DnsServers: 
      - "11.11.0.1"
    ServerCertificateArn: "arn:aws:acm:us-east-1:111122223333:certificate/12345678-1234-1234-1234-123456789012"
    TagSpecifications:
      - ResourceType: "client-vpn-endpoint"
        Tags:
        - Key: "Purpose"
          Value: "Production"
    TransportProtocol: "udp"
```

#### JSON<a name="aws-resource-ec2-clientvpnendpoint--examples--Creating_a_Client_VPN_endpoint--json"></a>

```
"myClientVpnEndpoint": {
    "Type": "AWS::EC2::ClientVpnEndpoint",
    "Properties": {
        "AuthenticationOptions": [
            {
                "Type": "directory-service-authentication",
                "ActiveDirectory": {
                    "DirectoryId": "d-926example"
                }
            }
        ],
        "ClientCidrBlock": "10.0.0.0/22",
        "ConnectionLogOptions": {
            "Enabled": false
        },
        "Description": "My Client VPN Endpoint",
        "DnsServers": [
            "11.11.0.1"
        ],
        "ServerCertificateArn": "arn:aws:acm:us-east-1:111122223333:certificate/12345678-1234-1234-1234-123456789012",
        "TagSpecifications": [
            {
                "ResourceType": "client-vpn-endpoint",
                "Tags": [
                    {
                        "Key": "Purpose",
                        "Value": "Production"
                    }
                ]
            }
        ],
        "TransportProtocol": "udp"
    }
}
```

## See Also<a name="aws-resource-ec2-clientvpnendpoint--seealso"></a>
+ [ Getting Started with Client VPN](https://docs.aws.amazon.com/vpn/latest/clientvpn-admin/cvpn-getting-started.html) in the *AWS Client VPN Administrator Guide*
+ [Client VPN Endpoints](https://docs.aws.amazon.com/vpn/latest/clientvpn-admin/cvpn-working-endpoints.html) in the *AWS Client VPN Administrator Guide*