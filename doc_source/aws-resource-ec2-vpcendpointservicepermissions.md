# AWS::EC2::VPCEndpointServicePermissions<a name="aws-resource-ec2-vpcendpointservicepermissions"></a>

Grant or revoke permissions for service consumers \(IAM users, IAM roles, and AWS accounts\) to connect to the VPC endpoint service\. For more information, see [ModifyVpcEndpointServicePermissions](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_ModifyVpcEndpointServicePermissions.html) in the *Amazon EC2 API Reference*\.

If you grant permissions to all principals, the service is public\. Any users who know the name of a public service can send a request to attach an endpoint\. If the service does not require manual approval, attachments are automatically approved\.

**Topics**
+ [Syntax](#aws-resource-ec2-vpcendpointservicepermissions-syntax)
+ [Properties](#aws-resource-ec2-vpcendpointservicepermissions-properties)
+ [Return Values](#aws-resource-ec2-vpcendpointservicepermissions-returnvalues)

## Syntax<a name="aws-resource-ec2-vpcendpointservicepermissions-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ec2-vpcendpointservicepermissions-syntax.json"></a>

```
{
  "Type" : "AWS::EC2::VPCEndpointServicePermissions",
  "Properties" : {
    "[AllowedPrincipals](#cfn-ec2-vpcendpointservicepermissions-allowedprincipals)" : [ String, ... ],
    "[ServiceId](#cfn-ec2-vpcendpointservicepermissions-serviceid)" : String
  }
}
```

### YAML<a name="aws-resource-ec2-vpcendpointservicepermissions-syntax.yaml"></a>

```
Type: "AWS::EC2::VPCEndpointServicePermissions"
Properties:
  [AllowedPrincipals](#cfn-ec2-vpcendpointservicepermissions-allowedprincipals): 
    - String
  [ServiceId](#cfn-ec2-vpcendpointservicepermissions-serviceid): String
```

## Properties<a name="aws-resource-ec2-vpcendpointservicepermissions-properties"></a>

`AllowedPrincipals`  <a name="cfn-ec2-vpcendpointservicepermissions-allowedprincipals"></a>
The Amazon Resource Names \(ARN\) of one or more principals \(IAM users, IAM roles, and AWS accounts\)\. Permissions are granted to the principals in this list\. To grant permissions to all principals, specify an asterisk \(\*\)\. Permissions are revoked for principals not in this list\. If the list is empty, then all permissions are revoked\.  
*Required*: No  
*Type*: List of String values  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`ServiceId`  <a name="cfn-ec2-vpcendpointservicepermissions-serviceid"></a>
The ID of the VPC endpoint service\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

## Return Values<a name="aws-resource-ec2-vpcendpointservicepermissions-returnvalues"></a>

### Ref<a name="aws-resource-ec2-vpcendpointservicepermissions-ref"></a>

When you pass the logical ID of an `AWS::EC2::VPCEndpointServicePermissions` resource to the intrinsic `Ref` function, the function returns the ID of the VPC endpoint service\.

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\. 