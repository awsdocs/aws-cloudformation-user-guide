# AWS::DeviceFarm::VPCEConfiguration<a name="aws-resource-devicefarm-vpceconfiguration"></a>

Creates a configuration record in Device Farm for your Amazon Virtual Private Cloud \(VPC\) endpoint service\.

## Syntax<a name="aws-resource-devicefarm-vpceconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-devicefarm-vpceconfiguration-syntax.json"></a>

```
{
  "Type" : "AWS::DeviceFarm::VPCEConfiguration",
  "Properties" : {
      "[ServiceDnsName](#cfn-devicefarm-vpceconfiguration-servicednsname)" : String,
      "[Tags](#cfn-devicefarm-vpceconfiguration-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ],
      "[VpceConfigurationDescription](#cfn-devicefarm-vpceconfiguration-vpceconfigurationdescription)" : String,
      "[VpceConfigurationName](#cfn-devicefarm-vpceconfiguration-vpceconfigurationname)" : String,
      "[VpceServiceName](#cfn-devicefarm-vpceconfiguration-vpceservicename)" : String
    }
}
```

### YAML<a name="aws-resource-devicefarm-vpceconfiguration-syntax.yaml"></a>

```
Type: AWS::DeviceFarm::VPCEConfiguration
Properties: 
  [ServiceDnsName](#cfn-devicefarm-vpceconfiguration-servicednsname): String
  [Tags](#cfn-devicefarm-vpceconfiguration-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
  [VpceConfigurationDescription](#cfn-devicefarm-vpceconfiguration-vpceconfigurationdescription): String
  [VpceConfigurationName](#cfn-devicefarm-vpceconfiguration-vpceconfigurationname): String
  [VpceServiceName](#cfn-devicefarm-vpceconfiguration-vpceservicename): String
```

## Properties<a name="aws-resource-devicefarm-vpceconfiguration-properties"></a>

`ServiceDnsName`  <a name="cfn-devicefarm-vpceconfiguration-servicednsname"></a>
The DNS name that Device Farm will use to map to the private service you want to access\.   
*Required*: Yes  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `2048`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-devicefarm-vpceconfiguration-tags"></a>
An array of key\-value pairs to apply to this resource\.  
For more information, see [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html) in the *AWS CloudFormation resource type reference guide*\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VpceConfigurationDescription`  <a name="cfn-devicefarm-vpceconfiguration-vpceconfigurationdescription"></a>
An optional description that provides details about your VPC endpoint configuration\.  
*Required*: No  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `2048`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VpceConfigurationName`  <a name="cfn-devicefarm-vpceconfiguration-vpceconfigurationname"></a>
The friendly name you give to your VPC endpoint configuration to manage your configurations more easily\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `1024`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VpceServiceName`  <a name="cfn-devicefarm-vpceconfiguration-vpceservicename"></a>
The name of the VPC endpoint service that you want to access from Device Farm\.  
The name follows the format `com.amazonaws.vpce.us-west-2.vpce-svc-id`\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `2048`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-devicefarm-vpceconfiguration-return-values"></a>

### Ref<a name="aws-resource-devicefarm-vpceconfiguration-return-values-ref"></a>

Not supported for this resource\.

### Fn::GetAtt<a name="aws-resource-devicefarm-vpceconfiguration-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-devicefarm-vpceconfiguration-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the VPC endpoint\. See [Amazon resource names](https://docs.aws.amazon.com/general/latest/gr/aws-arns-and-namespaces.html) in the *General Reference guide*\.