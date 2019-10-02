# AWS::EC2::ClientVpnEndpoint DirectoryServiceAuthenticationRequest<a name="aws-properties-ec2-clientvpnendpoint-directoryserviceauthenticationrequest"></a>

Describes the Active Directory to be used for client authentication\.

## Syntax<a name="aws-properties-ec2-clientvpnendpoint-directoryserviceauthenticationrequest-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ec2-clientvpnendpoint-directoryserviceauthenticationrequest-syntax.json"></a>

```
{
  "[DirectoryId](#cfn-ec2-clientvpnendpoint-directoryserviceauthenticationrequest-directoryid)" : String
}
```

### YAML<a name="aws-properties-ec2-clientvpnendpoint-directoryserviceauthenticationrequest-syntax.yaml"></a>

```
  [DirectoryId](#cfn-ec2-clientvpnendpoint-directoryserviceauthenticationrequest-directoryid): String
```

## Properties<a name="aws-properties-ec2-clientvpnendpoint-directoryserviceauthenticationrequest-properties"></a>

`DirectoryId`  <a name="cfn-ec2-clientvpnendpoint-directoryserviceauthenticationrequest-directoryid"></a>
The ID of the Active Directory to be used for authentication\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Supported Regions

This PropertyType is supported by the following regions:

- `ap-northeast-1`
- `ap-south-1`
- `ap-southeast-1`
- `ap-southeast-2`
- `eu-central-1`
- `eu-west-1`
- `eu-west-2`
- `us-east-1`
- `us-east-2`
- `us-west-2`
