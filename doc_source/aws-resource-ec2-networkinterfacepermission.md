# AWS::EC2::NetworkInterfacePermission<a name="aws-resource-ec2-networkinterfacepermission"></a>

Specifies a permission for an Amazon EC2 network interface\. For example, you can grant an AWS authorized partner account permission to attach the specified network interface to an instance in their account\.

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
Type: AWS::EC2::NetworkInterfacePermission
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
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`NetworkInterfaceId`  <a name="cfn-ec2-networkinterfacepermission-networkinterfaceid"></a>
The ID of the network interface\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Permission`  <a name="cfn-ec2-networkinterfacepermission-permission"></a>
The type of permission to grant: `INSTANCE-ATTACH` or `EIP-ASSOCIATE`\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `EIP-ASSOCIATE | INSTANCE-ATTACH`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-ec2-networkinterfacepermission-return-values"></a>

### Ref<a name="aws-resource-ec2-networkinterfacepermission-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the resource name\. For example: `eni-perm-055663b682ea24b48`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-resource-ec2-networkinterfacepermission--examples"></a>



### Grant INSTANCE\-ATTACH Permission<a name="aws-resource-ec2-networkinterfacepermission--examples--Grant_INSTANCE-ATTACH_Permission"></a>

The following example creates a permission \(`INSTANCE-ATTACH`\) for a specified network interface and AWS account\.

#### JSON<a name="aws-resource-ec2-networkinterfacepermission--examples--Grant_INSTANCE-ATTACH_Permission--json"></a>

```
"MyNetworkInterfacePermission": {
   "Type": "AWS::EC2::NetworkInterfacePermission",
   "Properties": {
      "NetworkInterfaceId": "eni-030e3xxx",
      "AwsAccountId": "11111111111",
      "Permission": "INSTANCE-ATTACH"
   }
}
```

#### YAML<a name="aws-resource-ec2-networkinterfacepermission--examples--Grant_INSTANCE-ATTACH_Permission--yaml"></a>

```
   MyNetworkInterfacePermission:
      Type: AWS::EC2::NetworkInterfacePermission
      Properties:
         NetworkInterfaceId: eni-030e3xxx
         AwsAccountId: '11111111111'
         Permission: INSTANCE-ATTACH
```