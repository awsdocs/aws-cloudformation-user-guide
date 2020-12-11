# AWS::ElasticLoadBalancingV2::TargetGroup<a name="aws-resource-elasticloadbalancingv2-targetgroup"></a>

Specifies a target group for an Application Load Balancer or Network Load Balancer\.

Before you register a Lambda function as a target, you must create a `AWS::Lambda::Permission` resource that grants the Elastic Load Balancing service principal permission to invoke the Lambda function\.

## Syntax<a name="aws-resource-elasticloadbalancingv2-targetgroup-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-elasticloadbalancingv2-targetgroup-syntax.json"></a>

```
{
  "Type" : "AWS::ElasticLoadBalancingV2::TargetGroup",
  "Properties" : {
      "[HealthCheckEnabled](#cfn-elasticloadbalancingv2-targetgroup-healthcheckenabled)" : Boolean,
      "[HealthCheckIntervalSeconds](#cfn-elasticloadbalancingv2-targetgroup-healthcheckintervalseconds)" : Integer,
      "[HealthCheckPath](#cfn-elasticloadbalancingv2-targetgroup-healthcheckpath)" : String,
      "[HealthCheckPort](#cfn-elasticloadbalancingv2-targetgroup-healthcheckport)" : String,
      "[HealthCheckProtocol](#cfn-elasticloadbalancingv2-targetgroup-healthcheckprotocol)" : String,
      "[HealthCheckTimeoutSeconds](#cfn-elasticloadbalancingv2-targetgroup-healthchecktimeoutseconds)" : Integer,
      "[HealthyThresholdCount](#cfn-elasticloadbalancingv2-targetgroup-healthythresholdcount)" : Integer,
      "[Matcher](#cfn-elasticloadbalancingv2-targetgroup-matcher)" : Matcher,
      "[Name](#cfn-elasticloadbalancingv2-targetgroup-name)" : String,
      "[Port](#cfn-elasticloadbalancingv2-targetgroup-port)" : Integer,
      "[Protocol](#cfn-elasticloadbalancingv2-targetgroup-protocol)" : String,
      "[Tags](#cfn-elasticloadbalancingv2-targetgroup-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ],
      "[TargetGroupAttributes](#cfn-elasticloadbalancingv2-targetgroup-targetgroupattributes)" : [ TargetGroupAttribute, ... ],
      "[Targets](#cfn-elasticloadbalancingv2-targetgroup-targets)" : [ TargetDescription, ... ],
      "[TargetType](#cfn-elasticloadbalancingv2-targetgroup-targettype)" : String,
      "[UnhealthyThresholdCount](#cfn-elasticloadbalancingv2-targetgroup-unhealthythresholdcount)" : Integer,
      "[VpcId](#cfn-elasticloadbalancingv2-targetgroup-vpcid)" : String
    }
}
```

### YAML<a name="aws-resource-elasticloadbalancingv2-targetgroup-syntax.yaml"></a>

```
Type: AWS::ElasticLoadBalancingV2::TargetGroup
Properties: 
  [HealthCheckEnabled](#cfn-elasticloadbalancingv2-targetgroup-healthcheckenabled): Boolean
  [HealthCheckIntervalSeconds](#cfn-elasticloadbalancingv2-targetgroup-healthcheckintervalseconds): Integer
  [HealthCheckPath](#cfn-elasticloadbalancingv2-targetgroup-healthcheckpath): String
  [HealthCheckPort](#cfn-elasticloadbalancingv2-targetgroup-healthcheckport): String
  [HealthCheckProtocol](#cfn-elasticloadbalancingv2-targetgroup-healthcheckprotocol): String
  [HealthCheckTimeoutSeconds](#cfn-elasticloadbalancingv2-targetgroup-healthchecktimeoutseconds): Integer
  [HealthyThresholdCount](#cfn-elasticloadbalancingv2-targetgroup-healthythresholdcount): Integer
  [Matcher](#cfn-elasticloadbalancingv2-targetgroup-matcher): 
    Matcher
  [Name](#cfn-elasticloadbalancingv2-targetgroup-name): String
  [Port](#cfn-elasticloadbalancingv2-targetgroup-port): Integer
  [Protocol](#cfn-elasticloadbalancingv2-targetgroup-protocol): String
  [Tags](#cfn-elasticloadbalancingv2-targetgroup-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
  [TargetGroupAttributes](#cfn-elasticloadbalancingv2-targetgroup-targetgroupattributes): 
    - TargetGroupAttribute
  [Targets](#cfn-elasticloadbalancingv2-targetgroup-targets): 
    - TargetDescription
  [TargetType](#cfn-elasticloadbalancingv2-targetgroup-targettype): String
  [UnhealthyThresholdCount](#cfn-elasticloadbalancingv2-targetgroup-unhealthythresholdcount): Integer
  [VpcId](#cfn-elasticloadbalancingv2-targetgroup-vpcid): String
```

## Properties<a name="aws-resource-elasticloadbalancingv2-targetgroup-properties"></a>

`HealthCheckEnabled`  <a name="cfn-elasticloadbalancingv2-targetgroup-healthcheckenabled"></a>
Indicates whether health checks are enabled\. If the target type is `lambda`, health checks are disabled by default but can be enabled\. If the target type is `instance` or `ip`, health checks are always enabled and cannot be disabled\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`HealthCheckIntervalSeconds`  <a name="cfn-elasticloadbalancingv2-targetgroup-healthcheckintervalseconds"></a>
The approximate amount of time, in seconds, between health checks of an individual target\. If the target group protocol is TCP, TLS, UDP, or TCP\_UDP, the supported values are 10 and 30 seconds\. If the target group protocol is HTTP or HTTPS, the default is 30 seconds\. If the target group protocol is GENEVE, the default is 10 seconds\. If the target type is `lambda`, the default is 35 seconds\.  
*Required*: No  
*Type*: Integer  
*Minimum*: `5`  
*Maximum*: `300`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`HealthCheckPath`  <a name="cfn-elasticloadbalancingv2-targetgroup-healthcheckpath"></a>
\[HTTP/HTTPS health checks\] The destination for health checks on the targets\.  
\[HTTP1 or HTTP2 protocol version\] The ping path\. The default is /\.  
\[GRPC protocol version\] The path of a custom health check method with the format /package\.service/method\. The default is /AWS\.ALB/healthcheck\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `1024`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`HealthCheckPort`  <a name="cfn-elasticloadbalancingv2-targetgroup-healthcheckport"></a>
The port the load balancer uses when performing health checks on targets\. If the protocol is HTTP, HTTPS, TCP, TLS, UDP, or TCP\_UDP, the default is `traffic-port`, which is the port on which each target receives traffic from the load balancer\. If the protocol is GENEVE, the default is port 80\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`HealthCheckProtocol`  <a name="cfn-elasticloadbalancingv2-targetgroup-healthcheckprotocol"></a>
The protocol the load balancer uses when performing health checks on targets\. For Application Load Balancers, the default is HTTP\. For Network Load Balancers and Gateway Load Balancers, the default is TCP\. The TCP protocol is not supported for health checks if the protocol of the target group is HTTP or HTTPS\. The GENEVE, TLS, UDP, and TCP\_UDP protocols are not supported for health checks\.  
*Required*: No  
*Type*: String  
*Allowed values*: `GENEVE | HTTP | HTTPS | TCP | TCP_UDP | TLS | UDP`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`HealthCheckTimeoutSeconds`  <a name="cfn-elasticloadbalancingv2-targetgroup-healthchecktimeoutseconds"></a>
The amount of time, in seconds, during which no response from a target means a failed health check\. For target groups with a protocol of HTTP, HTTPS, or GENEVE, the default is 5 seconds\. For target groups with a protocol of TCP or TLS, this value must be 6 seconds for HTTP health checks and 10 seconds for TCP and HTTPS health checks\. If the target type is `lambda`, the default is 30 seconds\.  
*Required*: No  
*Type*: Integer  
*Minimum*: `2`  
*Maximum*: `120`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`HealthyThresholdCount`  <a name="cfn-elasticloadbalancingv2-targetgroup-healthythresholdcount"></a>
The number of consecutive health checks successes required before considering an unhealthy target healthy\. For target groups with a protocol of HTTP or HTTPS, the default is 5\. For target groups with a protocol of TCP, TLS, or GENEVE, the default is 3\. If the target type is `lambda`, the default is 5\.  
*Required*: No  
*Type*: Integer  
*Minimum*: `2`  
*Maximum*: `10`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Matcher`  <a name="cfn-elasticloadbalancingv2-targetgroup-matcher"></a>
\[HTTP/HTTPS health checks\] The HTTP or gRPC codes to use when checking for a successful response from a target\.  
*Required*: No  
*Type*: [Matcher](aws-properties-elasticloadbalancingv2-targetgroup-matcher.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-elasticloadbalancingv2-targetgroup-name"></a>
The name of the target group\.  
This name must be unique per region per account, can have a maximum of 32 characters, must contain only alphanumeric characters or hyphens, and must not begin or end with a hyphen\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Port`  <a name="cfn-elasticloadbalancingv2-targetgroup-port"></a>
The port on which the targets receive traffic\. This port is used unless you specify a port override when registering the target\. If the target is a Lambda function, this parameter does not apply\. If the protocol is GENEVE, the supported port is 6081\.  
*Required*: Conditional  
*Type*: Integer  
*Minimum*: `1`  
*Maximum*: `65535`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Protocol`  <a name="cfn-elasticloadbalancingv2-targetgroup-protocol"></a>
The protocol to use for routing traffic to the targets\. For Application Load Balancers, the supported protocols are HTTP and HTTPS\. For Network Load Balancers, the supported protocols are TCP, TLS, UDP, or TCP\_UDP\. For Gateway Load Balancers, the supported protocol is GENEVE\. A TCP\_UDP listener must be associated with a TCP\_UDP target group\. If the target is a Lambda function, this parameter does not apply\.  
*Required*: Conditional  
*Type*: String  
*Allowed values*: `GENEVE | HTTP | HTTPS | TCP | TCP_UDP | TLS | UDP`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-elasticloadbalancingv2-targetgroup-tags"></a>
The tags\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TargetGroupAttributes`  <a name="cfn-elasticloadbalancingv2-targetgroup-targetgroupattributes"></a>
The attributes\.  
*Required*: No  
*Type*: List of [TargetGroupAttribute](aws-properties-elasticloadbalancingv2-targetgroup-targetgroupattribute.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Targets`  <a name="cfn-elasticloadbalancingv2-targetgroup-targets"></a>
The targets\.  
*Required*: No  
*Type*: List of [TargetDescription](aws-properties-elasticloadbalancingv2-targetgroup-targetdescription.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TargetType`  <a name="cfn-elasticloadbalancingv2-targetgroup-targettype"></a>
The type of target that you must specify when registering targets with this target group\. You can't specify targets for a target group using more than one target type\.  
+  `instance` \- Register targets by instance ID\. This is the default value\.
+  `ip` \- Register targets by IP address\. You can specify IP addresses from the subnets of the virtual private cloud \(VPC\) for the target group, the RFC 1918 range \(10\.0\.0\.0/8, 172\.16\.0\.0/12, and 192\.168\.0\.0/16\), and the RFC 6598 range \(100\.64\.0\.0/10\)\. You can't specify publicly routable IP addresses\.
+  `lambda` \- Register a single Lambda function as a target\.
*Required*: No  
*Type*: String  
*Allowed values*: `instance | ip | lambda`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`UnhealthyThresholdCount`  <a name="cfn-elasticloadbalancingv2-targetgroup-unhealthythresholdcount"></a>
The number of consecutive health check failures required before considering a target unhealthy\. If the target group protocol is HTTP or HTTPS, the default is 2\. If the target group protocol is TCP or TLS, this value must be the same as the healthy threshold count\. If the target group protocol is GENEVE, the default is 3\. If the target type is `lambda`, the default is 2\.  
*Required*: No  
*Type*: Integer  
*Minimum*: `2`  
*Maximum*: `10`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VpcId`  <a name="cfn-elasticloadbalancingv2-targetgroup-vpcid"></a>
The identifier of the virtual private cloud \(VPC\)\. If the target is a Lambda function, this parameter does not apply\. Otherwise, this parameter is required\.  
*Required*: Conditional  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-elasticloadbalancingv2-targetgroup-return-values"></a>

### Ref<a name="aws-resource-elasticloadbalancingv2-targetgroup-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the Amazon Resource Name \(ARN\) of the target group\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-elasticloadbalancingv2-targetgroup-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-elasticloadbalancingv2-targetgroup-return-values-fn--getatt-fn--getatt"></a>

`LoadBalancerArns`  <a name="LoadBalancerArns-fn::getatt"></a>
The Amazon Resource Names \(ARNs\) of the load balancers that route traffic to this target group\.

`TargetGroupFullName`  <a name="TargetGroupFullName-fn::getatt"></a>
The full name of the target group\. For example, `targetgroup/my-target-group/cbf133c568e0d028`\.

`TargetGroupName`  <a name="TargetGroupName-fn::getatt"></a>
The name of the target group\. For example, `my-target-group`\.

## Examples<a name="aws-resource-elasticloadbalancingv2-targetgroup--examples"></a>

The following example creates a target group where the target is a Lambda function\.

### <a name="aws-resource-elasticloadbalancingv2-targetgroup--examples--"></a>

#### YAML<a name="aws-resource-elasticloadbalancingv2-targetgroup--examples----yaml"></a>

```
Resources:
  MyLambdaInvokePermission:
    Type: AWS::Lambda::Permission
    Properties:
      FunctionName: !GetAtt 
        - MyLambdaFunction
        - Arn
      Action: 'lambda:InvokeFunction'
      Principal: elasticloadbalancing.amazonaws.com

  MyTargetGroup:
    Type: AWS::ElasticLoadBalancingV2::TargetGroup
    Properties:
      HealthCheckEnabled: false
      Name: MyTargets
      TargetType: lambda
      Targets:
      - Id: !GetAtt [ MyLambdaFunction, Arn ]

  MyLambdaFunction:
    Type: "AWS::Lambda::Function"
    Properties:
      Handler: "index.handler"
      Role: !GetAtt [ LambdaExecutionRole, Arn ]
      Code:
        ZipFile: !Sub |
          import json
          
          def handler(event, context):
            response = {
              "statusCode": 200,
              "statusDescription": "200 OK",
              "isBase64Encoded": False,
              "headers": {
                "Content-Type": "text/html; charset=utf-8"
              }
            }

            response['body'] = """<html>
            <head>
            <title>Hello World!</title>
            <style>
            html, body {
              margin: 0; padding: 0;
              font-family: arial; font-weight: 700; font-size: 3em;
              text-align: center;
            }
            </style>
            </head>
            <body>
            <p>Hello World from Lambda</p>
            </body>
            </html>"""
            return response      
      Runtime: "python3.6"
      Timeout: "25"

  LambdaExecutionRole:
    Type: "AWS::IAM::Role"
    Properties:
      AssumeRolePolicyDocument:
        Version: "2012-10-17"
        Statement:
          - Effect: Allow
            Principal:
              Service: lambda.amazonaws.com
            Action: "sts:AssumeRole"
```

## See also<a name="aws-resource-elasticloadbalancingv2-targetgroup--seealso"></a>
+  [CreateTargetGroup](https://docs.aws.amazon.com/elasticloadbalancing/latest/APIReference/API_CreateTargetGroup.html) in the *Elastic Load Balancing API Reference \(version 2015\-12\-01\)* 
+  [Target Groups](https://docs.aws.amazon.com/elasticloadbalancing/latest/application/load-balancer-target-groups.html) in the *User Guide for Application Load Balancers* 
+  [Target Groups](https://docs.aws.amazon.com/elasticloadbalancing/latest/network/load-balancer-target-groups.html) in the *User Guide for Network Load Balancers* 

