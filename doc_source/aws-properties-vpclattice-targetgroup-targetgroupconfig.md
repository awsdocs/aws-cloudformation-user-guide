# AWS::VpcLattice::TargetGroup TargetGroupConfig<a name="aws-properties-vpclattice-targetgroup-targetgroupconfig"></a>

Describes the configuration of a target group\.

## Syntax<a name="aws-properties-vpclattice-targetgroup-targetgroupconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-vpclattice-targetgroup-targetgroupconfig-syntax.json"></a>

```
{
  "[HealthCheck](#cfn-vpclattice-targetgroup-targetgroupconfig-healthcheck)" : HealthCheckConfig,
  "[IpAddressType](#cfn-vpclattice-targetgroup-targetgroupconfig-ipaddresstype)" : String,
  "[LambdaEventStructureVersion](#cfn-vpclattice-targetgroup-targetgroupconfig-lambdaeventstructureversion)" : String,
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
  [LambdaEventStructureVersion](#cfn-vpclattice-targetgroup-targetgroupconfig-lambdaeventstructureversion): String
  [Port](#cfn-vpclattice-targetgroup-targetgroupconfig-port): Integer
  [Protocol](#cfn-vpclattice-targetgroup-targetgroupconfig-protocol): String
  [ProtocolVersion](#cfn-vpclattice-targetgroup-targetgroupconfig-protocolversion): String
  [VpcIdentifier](#cfn-vpclattice-targetgroup-targetgroupconfig-vpcidentifier): String
```

## Properties<a name="aws-properties-vpclattice-targetgroup-targetgroupconfig-properties"></a>

`HealthCheck`  <a name="cfn-vpclattice-targetgroup-targetgroupconfig-healthcheck"></a>
The health check configuration\. Not supported if the target group type is `LAMBDA` or `ALB`\.  
*Required*: No  
*Type*: [HealthCheckConfig](aws-properties-vpclattice-targetgroup-healthcheckconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IpAddressType`  <a name="cfn-vpclattice-targetgroup-targetgroupconfig-ipaddresstype"></a>
The type of IP address used for the target group\. Supported only if the target group type is `IP`\. The default is `IPV4`\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`LambdaEventStructureVersion`  <a name="cfn-vpclattice-targetgroup-targetgroupconfig-lambdaeventstructureversion"></a>
The version of the event structure that your Lambda function receives\. Supported only if the target group type is `LAMBDA`\. The default is `V1`\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Port`  <a name="cfn-vpclattice-targetgroup-targetgroupconfig-port"></a>
The port on which the targets are listening\. For HTTP, the default is 80\. For HTTPS, the default is 443\. Not supported if the target group type is `LAMBDA`\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Protocol`  <a name="cfn-vpclattice-targetgroup-targetgroupconfig-protocol"></a>
The protocol to use for routing traffic to the targets\. The default is the protocol of the target group\. Not supported if the target group type is `LAMBDA`\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ProtocolVersion`  <a name="cfn-vpclattice-targetgroup-targetgroupconfig-protocolversion"></a>
The protocol version\. The default is `HTTP1`\. Not supported if the target group type is `LAMBDA`\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`VpcIdentifier`  <a name="cfn-vpclattice-targetgroup-targetgroupconfig-vpcidentifier"></a>
The ID of the VPC\. Not supported if the target group type is `LAMBDA`\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)