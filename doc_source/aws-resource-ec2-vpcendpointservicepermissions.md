# AWS::EC2::VPCEndpointServicePermissions<a name="aws-resource-ec2-vpcendpointservicepermissions"></a>

Grant or revoke permissions for service consumers \(IAM users, IAM roles, and AWS accounts\) to connect to a VPC endpoint service\.

If you grant permissions to all principals, the service is public\. Any users who know the name of a public service can send a request to attach an endpoint\. If the service does not require manual approval, attachments are automatically approved\.

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
Type: AWS::EC2::VPCEndpointServicePermissions
Properties: 
  [AllowedPrincipals](#cfn-ec2-vpcendpointservicepermissions-allowedprincipals): 
    - String
  [ServiceId](#cfn-ec2-vpcendpointservicepermissions-serviceid): String
```

## Properties<a name="aws-resource-ec2-vpcendpointservicepermissions-properties"></a>

`AllowedPrincipals`  <a name="cfn-ec2-vpcendpointservicepermissions-allowedprincipals"></a>
The Amazon Resource Names \(ARN\) of one or more principals \(IAM users, IAM roles, and AWS accounts\)\. Permissions are granted to the principals in this list\. To grant permissions to all principals, specify an asterisk \(\*\)\. Permissions are revoked for principals not in this list\. If the list is empty, then all permissions are revoked\.   
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ServiceId`  <a name="cfn-ec2-vpcendpointservicepermissions-serviceid"></a>
The ID of the service\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-ec2-vpcendpointservicepermissions-return-values"></a>

### Ref<a name="aws-resource-ec2-vpcendpointservicepermissions-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the ID of the VPC endpoint service permissions\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.