# AWS::BackupGateway::Hypervisor<a name="aws-resource-backupgateway-hypervisor"></a>

Represents the hypervisor's permissions to which the gateway will connect\.

A hypervisor is hardware, software, or firmware that creates and manages virtual machines, and allocates resources to them\.

## Syntax<a name="aws-resource-backupgateway-hypervisor-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-backupgateway-hypervisor-syntax.json"></a>

```
{
  "Type" : "AWS::BackupGateway::Hypervisor",
  "Properties" : {
      "[Host](#cfn-backupgateway-hypervisor-host)" : String,
      "[KmsKeyArn](#cfn-backupgateway-hypervisor-kmskeyarn)" : String,
      "[LogGroupArn](#cfn-backupgateway-hypervisor-loggrouparn)" : String,
      "[Name](#cfn-backupgateway-hypervisor-name)" : String,
      "[Password](#cfn-backupgateway-hypervisor-password)" : String,
      "[Tags](#cfn-backupgateway-hypervisor-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ],
      "[Username](#cfn-backupgateway-hypervisor-username)" : String
    }
}
```

### YAML<a name="aws-resource-backupgateway-hypervisor-syntax.yaml"></a>

```
Type: AWS::BackupGateway::Hypervisor
Properties: 
  [Host](#cfn-backupgateway-hypervisor-host): String
  [KmsKeyArn](#cfn-backupgateway-hypervisor-kmskeyarn): String
  [LogGroupArn](#cfn-backupgateway-hypervisor-loggrouparn): String
  [Name](#cfn-backupgateway-hypervisor-name): String
  [Password](#cfn-backupgateway-hypervisor-password): String
  [Tags](#cfn-backupgateway-hypervisor-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
  [Username](#cfn-backupgateway-hypervisor-username): String
```

## Properties<a name="aws-resource-backupgateway-hypervisor-properties"></a>

`Host`  <a name="cfn-backupgateway-hypervisor-host"></a>
The server host of the hypervisor\. This can be either an IP address or a fully\-qualified domain name \(FQDN\)\.  
*Required*: No  
*Type*: String  
*Minimum*: `3`  
*Maximum*: `128`  
*Pattern*: `.+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`KmsKeyArn`  <a name="cfn-backupgateway-hypervisor-kmskeyarn"></a>
The Amazon Resource Name \(ARN\) of the AWS Key Management Service used to encrypt the hypervisor\.  
*Required*: No  
*Type*: String  
*Minimum*: `50`  
*Maximum*: `500`  
*Pattern*: `(^arn:(aws|aws-cn|aws-us-gov):kms:([a-zA-Z0-9-]+):([0-9]+):(key|alias)/(\S+)$)|(^alias/(\S+)$)`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`LogGroupArn`  <a name="cfn-backupgateway-hypervisor-loggrouparn"></a>
The Amazon Resource Name \(ARN\) of the group of gateways within the requested log\.  
*Required*: No  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `2048`  
*Pattern*: `$|^arn:(aws|aws-cn|aws-us-gov):logs:([a-zA-Z0-9-]+):([0-9]+):log-group:[a-zA-Z0-9_\-\/\.]+:\*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-backupgateway-hypervisor-name"></a>
The name of the hypervisor\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `100`  
*Pattern*: `[a-zA-Z0-9-]*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Password`  <a name="cfn-backupgateway-hypervisor-password"></a>
The password for the hypervisor\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `100`  
*Pattern*: `[ -~]+`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-backupgateway-hypervisor-tags"></a>
The tags of the hypervisor configuration to import\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Username`  <a name="cfn-backupgateway-hypervisor-username"></a>
The username for the hypervisor\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `100`  
*Pattern*: `[ -\.0-\[\]-~]*[!-\.0-\[\]-~][ -\.0-\[\]-~]*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-backupgateway-hypervisor-return-values"></a>

### Ref<a name="aws-resource-backupgateway-hypervisor-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns `HypervisorArn`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-backupgateway-hypervisor-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-backupgateway-hypervisor-return-values-fn--getatt-fn--getatt"></a>

`HypervisorArn`  <a name="HypervisorArn-fn::getatt"></a>
Returns `HypervisorArn`, an Amazon Resource Name \(ARN\) that uniquely identifies a Hypervisor\. For example: `arn:aws:backup-gateway:us-east-1:123456789012:hypervisor/hype-1234D67D`