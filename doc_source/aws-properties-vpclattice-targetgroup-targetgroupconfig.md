# AWS::VpcLattice::TargetGroup TargetGroupConfig<a name="aws-properties-vpclattice-targetgroup-targetgroupconfig"></a>

Describes the configuration of a target group\. Lambda functions don't support target group configuration\.

## Syntax<a name="aws-properties-vpclattice-targetgroup-targetgroupconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-vpclattice-targetgroup-targetgroupconfig-syntax.json"></a>

```
{
  "[HealthCheck](#cfn-vpclattice-targetgroup-targetgroupconfig-healthcheck)" : HealthCheckConfig,
  "[IpAddressType](#cfn-vpclattice-targetgroup-targetgroupconfig-ipaddresstype)" : String,
  "[Port](#cfn-vpclattice-targetgroup-targetgroupconfig-port)" : Integer,
  "[Protocol](#cfn-vpclattice-targetgroup-targetgroupconfig-protocol)" : String,
  "[ProtocolVersion](#cfn-vpclattice-targetgroup-targetgroupconfig-protocolversion)" : String,
  "[VpcIdentifier](#cfn-vpclattice-targetgroup-targetgroupconfig-vpcidentifier)" : String
}
```

### YAML<a name="aws-properties-vpclattice-targetgroup-targetgroupconfig-syntax.yaml"></a>

```
  [HealthCheck](#cfn-vpclattice-targetgroup-targetgroupconfig-healthcheck): 
    HealthCheckConfig
  [IpAddressType](#cfn-vpclattice-targetgroup-targetgroupconfig-ipaddresstype): String
  [Port](#cfn-vpclattice-targetgroup-targetgroupconfig-port): Integer
  [Protocol](#cfn-vpclattice-targetgroup-targetgroupconfig-protocol): String
  [ProtocolVersion](#cfn-vpclattice-targetgroup-targetgroupconfig-protocolversion): String
  [VpcIdentifier](#cfn-vpclattice-targetgroup-targetgroupconfig-vpcidentifier): String
```

## Properties<a name="aws-properties-vpclattice-targetgroup-targetgroupconfig-properties"></a>

`HealthCheck`  <a name="cfn-vpclattice-targetgroup-targetgroupconfig-healthcheck"></a>
The health check configuration\.  
*Required*: No  
*Type*: [HealthCheckConfig](aws-properties-vpclattice-targetgroup-healthcheckconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IpAddressType`  <a name="cfn-vpclattice-targetgroup-targetgroupconfig-ipaddresstype"></a>
The type of IP address used for the target group\. The possible values are `ipv4` and `ipv6`\. This is an optional parameter\. If not specified, the default is `ipv4`\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Port`  <a name="cfn-vpclattice-targetgroup-targetgroupconfig-port"></a>
The port on which the targets are listening\. For HTTP, the default is 80\. For HTTPS, the default is 443\.  
*Required*: Yes  
*Type*: Integer  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Protocol`  <a name="cfn-vpclattice-targetgroup-targetgroupconfig-protocol"></a>
The protocol to use for routing traffic to the targets\. Default is the protocol of a target group\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ProtocolVersion`  <a name="cfn-vpclattice-targetgroup-targetgroupconfig-protocolversion"></a>
The protocol version\. Default value is `HTTP1`\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`VpcIdentifier`  <a name="cfn-vpclattice-targetgroup-targetgroupconfig-vpcidentifier"></a>
The ID of the VPC\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)