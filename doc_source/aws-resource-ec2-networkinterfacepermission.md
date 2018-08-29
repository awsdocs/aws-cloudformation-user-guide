# AWS::EC2::NetworkInterfacePermission<a name="aws-resource-ec2-networkinterfacepermission"></a>

The `AWS::EC2::NetworkInterfacePermission` resource specifies a permission for an Amazon EC2 network interface\. For example, you can grant an AWS authorized partner account permission to attach the specified network interface to an instance in their account\. For more information, see [CreateNetworkInterfacePermission](http://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_CreateNetworkInterfacePermission.html) and [NetworkInterfacePermission](http://docs.aws.amazon.com/AWSEC2/latest/APIReference/API_NetworkInterfacePermission.html) in the *Amazon EC2 API Reference*\. 

**Topics**
+ [Syntax](#aws-resource-ec2-networkinterfacepermission-syntax)
+ [Properties](#aws-resource-ec2-networkinterfacepermission-properties)
+ [Return Values](#aws-resource-ec2-networkinterfacepermission-returnvalues)
+ [Examples](#aws-resource-ec2-networkinterfacepermission-examples)

## Syntax<a name="aws-resource-ec2-networkinterfacepermission-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-ec2-networkinterfacepermission-syntax.json"></a>

```
{
  "Type" : "AWS::EC2::NetworkInterfacePermission",
  "Properties" : {
    "[AwsAccountId](#cfn-ec2-networkinterfacepermission-awsaccountid)" : String,
    "[NetworkInterfaceId](#cfn-ec2-networkinterfacepermission-networkinterfaceid)" : String,
    "[Permission](#cfn-ec2-networkinterfacepermission-permission)" : String
  }
}
```

### YAML<a name="aws-resource-ec2-networkinterfacepermission-syntax.yaml"></a>

```
Type: "AWS::EC2::NetworkInterfacePermission"
Properties:
  [AwsAccountId](#cfn-ec2-networkinterfacepermission-awsaccountid): String
  [NetworkInterfaceId](#cfn-ec2-networkinterfacepermission-networkinterfaceid): String
  [Permission](#cfn-ec2-networkinterfacepermission-permission): String
```

## Properties<a name="aws-resource-ec2-networkinterfacepermission-properties"></a>

`AwsAccountId`  <a name="cfn-ec2-networkinterfacepermission-awsaccountid"></a>
The AWS account ID\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`NetworkInterfaceId`  <a name="cfn-ec2-networkinterfacepermission-networkinterfaceid"></a>
The ID of the network interface\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`Permission`  <a name="cfn-ec2-networkinterfacepermission-permission"></a>
The type of permission to grant: `INSTANCE-ATTACH` or `EIP-ASSOCIATE`\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

## Return Values<a name="aws-resource-ec2-networkinterfacepermission-returnvalues"></a>

### Ref<a name="w3ab2c21c10d445c10b3"></a>

When you pass the logical ID of an `AWS::EC2::NetworkInterfacePermission` resource to the intrinsic `Ref` function, the function returns the network interface permission ID\. For example, `eni-perm-055663b682ea24b48`\.

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\. 

## Examples<a name="aws-resource-ec2-networkinterfacepermission-examples"></a>

### Grant `INSTANCE-ATTACH` Permission<a name="aws-resource-ec2-networkinterfacepermission-example1"></a>

The following example creates a permission \(`INSTANCE-ATTACH`\) for a specified network interface and AWS account\.

#### JSON<a name="aws-resource-ec2-networkinterfacepermission-example1.json"></a>

```
{
    "AWSTemplateFormatVersion": "2010-09-09",
    "Resources": {
        "MyNetworkInterfacePermission": {
            "Type": "AWS::EC2::NetworkInterfacePermission",
            "Properties": {
                "NetworkInterfaceId": "eni-030e3xxx",
                "AwsAccountId": "11111111111",
                "Permission": "INSTANCE-ATTACH"
            }
        }
    },
    "Outputs": {
        "ReferenceId": {
            "Value": {
                "Ref": "MyNetworkInterfacePermission"
            }
        }
    }
}
```

#### YAML<a name="aws-resource-ec2-networkinterfacepermission-example1.yaml"></a>

```
AWSTemplateFormatVersion: 2010-09-09
Resources:
  MyNetworkInterfacePermission:
    Type: 'AWS::EC2::NetworkInterfacePermission'
    Properties:
      NetworkInterfaceId: eni-030e3xxx
      AwsAccountId: '11111111111'
      Permission: INSTANCE-ATTACH
Outputs:
  ReferenceId:
    Value: !Ref MyNetworkInterfacePermission
```