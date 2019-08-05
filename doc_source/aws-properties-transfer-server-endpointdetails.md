# AWS::Transfer::Server EndpointDetails<a name="aws-properties-transfer-server-endpointdetails"></a>

The virtual private cloud \(VPC\) endpoint settings that you want to configure for your SFTP server\. This parameter is required when you specify a value for the `EndpointType` parameter\.

## Syntax<a name="aws-properties-transfer-server-endpointdetails-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-transfer-server-endpointdetails-syntax.json"></a>

```
{
  "[VpcEndpointId](#cfn-transfer-server-endpointdetails-vpcendpointid)" : String
}
```

### YAML<a name="aws-properties-transfer-server-endpointdetails-syntax.yaml"></a>

```
  [VpcEndpointId](#cfn-transfer-server-endpointdetails-vpcendpointid): String
```

## Properties<a name="aws-properties-transfer-server-endpointdetails-properties"></a>

`VpcEndpointId`  <a name="cfn-transfer-server-endpointdetails-vpcendpointid"></a>
The ID of the VPC endpoint\.
*Required*: Yes
*Type*: String
*Pattern*: `^vpce-[0-9a-f]{17}$`
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)
