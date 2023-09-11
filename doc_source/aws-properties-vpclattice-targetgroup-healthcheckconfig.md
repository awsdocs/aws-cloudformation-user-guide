# AWS::VpcLattice::TargetGroup HealthCheckConfig<a name="aws-properties-vpclattice-targetgroup-healthcheckconfig"></a>

Describes the health check configuration of a target group\. Health check configurations aren't used for target groups of type `LAMBDA` or `ALB`\.

## Syntax<a name="aws-properties-vpclattice-targetgroup-healthcheckconfig-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-vpclattice-targetgroup-healthcheckconfig-syntax.json"></a>

```
{
  "[Enabled](#cfn-vpclattice-targetgroup-healthcheckconfig-enabled)" : Boolean,
  "[HealthCheckIntervalSeconds](#cfn-vpclattice-targetgroup-healthcheckconfig-healthcheckintervalseconds)" : Integer,
  "[HealthCheckTimeoutSeconds](#cfn-vpclattice-targetgroup-healthcheckconfig-healthchecktimeoutseconds)" : Integer,
  "[HealthyThresholdCount](#cfn-vpclattice-targetgroup-healthcheckconfig-healthythresholdcount)" : Integer,
  "[Matcher](#cfn-vpclattice-targetgroup-healthcheckconfig-matcher)" : Matcher,
  "[Path](#cfn-vpclattice-targetgroup-healthcheckconfig-path)" : String,
  "[Port](#cfn-vpclattice-targetgroup-healthcheckconfig-port)" : Integer,
  "[Protocol](#cfn-vpclattice-targetgroup-healthcheckconfig-protocol)" : String,
  "[ProtocolVersion](#cfn-vpclattice-targetgroup-healthcheckconfig-protocolversion)" : String,
  "[UnhealthyThresholdCount](#cfn-vpclattice-targetgroup-healthcheckconfig-unhealthythresholdcount)" : Integer
}
```

### YAML<a name="aws-properties-vpclattice-targetgroup-healthcheckconfig-syntax.yaml"></a>

```
  [Enabled](#cfn-vpclattice-targetgroup-healthcheckconfig-enabled): Boolean
  [HealthCheckIntervalSeconds](#cfn-vpclattice-targetgroup-healthcheckconfig-healthcheckintervalseconds): Integer
  [HealthCheckTimeoutSeconds](#cfn-vpclattice-targetgroup-healthcheckconfig-healthchecktimeoutseconds): Integer
  [HealthyThresholdCount](#cfn-vpclattice-targetgroup-healthcheckconfig-healthythresholdcount): Integer
  [Matcher](#cfn-vpclattice-targetgroup-healthcheckconfig-matcher): 
    Matcher
  [Path](#cfn-vpclattice-targetgroup-healthcheckconfig-path): String
  [Port](#cfn-vpclattice-targetgroup-healthcheckconfig-port): Integer
  [Protocol](#cfn-vpclattice-targetgroup-healthcheckconfig-protocol): String
  [ProtocolVersion](#cfn-vpclattice-targetgroup-healthcheckconfig-protocolversion): String
  [UnhealthyThresholdCount](#cfn-vpclattice-targetgroup-healthcheckconfig-unhealthythresholdcount): Integer
```

## Properties<a name="aws-properties-vpclattice-targetgroup-healthcheckconfig-properties"></a>

`Enabled`  <a name="cfn-vpclattice-targetgroup-healthcheckconfig-enabled"></a>
Indicates whether health checking is enabled\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`HealthCheckIntervalSeconds`  <a name="cfn-vpclattice-targetgroup-healthcheckconfig-healthcheckintervalseconds"></a>
The approximate amount of time, in seconds, between health checks of an individual target\. The range is 5–300 seconds\. The default is 30 seconds\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`HealthCheckTimeoutSeconds`  <a name="cfn-vpclattice-targetgroup-healthcheckconfig-healthchecktimeoutseconds"></a>
The amount of time, in seconds, to wait before reporting a target as unhealthy\. The range is 1–120 seconds\. The default is 5 seconds\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`HealthyThresholdCount`  <a name="cfn-vpclattice-targetgroup-healthcheckconfig-healthythresholdcount"></a>
The number of consecutive successful health checks required before considering an unhealthy target healthy\. The range is 2–10\. The default is 5\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Matcher`  <a name="cfn-vpclattice-targetgroup-healthcheckconfig-matcher"></a>
The codes to use when checking for a successful response from a target\.  
*Required*: No  
*Type*: [Matcher](aws-properties-vpclattice-targetgroup-matcher.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Path`  <a name="cfn-vpclattice-targetgroup-healthcheckconfig-path"></a>
The destination for health checks on the targets\. If the protocol version is `HTTP/1.1` or `HTTP/2`, specify a valid URI \(for example, `/path?query`\)\. The default path is `/`\. Health checks are not supported if the protocol version is `gRPC`, however, you can choose `HTTP/1.1` or `HTTP/2` and specify a valid URI\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Port`  <a name="cfn-vpclattice-targetgroup-healthcheckconfig-port"></a>
The port used when performing health checks on targets\. The default setting is the port that a target receives traffic on\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Protocol`  <a name="cfn-vpclattice-targetgroup-healthcheckconfig-protocol"></a>
The protocol used when performing health checks on targets\. The possible protocols are `HTTP` and `HTTPS`\. The default is `HTTP`\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ProtocolVersion`  <a name="cfn-vpclattice-targetgroup-healthcheckconfig-protocolversion"></a>
The protocol version used when performing health checks on targets\. The possible protocol versions are `HTTP1` and `HTTP2`\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`UnhealthyThresholdCount`  <a name="cfn-vpclattice-targetgroup-healthcheckconfig-unhealthythresholdcount"></a>
The number of consecutive failed health checks required before considering a target unhealthy\. The range is 2–10\. The default is 2\.  
*Required*: No  
*Type*: Integer  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)