# AWS::ElasticLoadBalancing::LoadBalancer<a name="aws-properties-ec2-elb"></a>

Specifies a Classic Load Balancer\.

You can specify the `AvailabilityZones` or `Subnets` property, but not both\.



If this resource has a public IP address and is also in a VPC that is defined in the same template, you must use the [DependsOn attribute](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-attribute-dependson.html) to declare a dependency on the VPC\-gateway attachment\.

## Syntax<a name="aws-properties-ec2-elb-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ec2-elb-syntax.json"></a>

```
{
  "Type" : "AWS::ElasticLoadBalancing::LoadBalancer",
  "Properties" : {
      "[AccessLoggingPolicy](#cfn-ec2-elb-accessloggingpolicy)" : AccessLoggingPolicy,
      "[AppCookieStickinessPolicy](#cfn-ec2-elb-appcookiestickinesspolicy)" : [ AppCookieStickinessPolicy, ... ],
      "[AvailabilityZones](#cfn-ec2-elb-availabilityzones)" : [ String, ... ],
      "[ConnectionDrainingPolicy](#cfn-ec2-elb-connectiondrainingpolicy)" : ConnectionDrainingPolicy,
      "[ConnectionSettings](#cfn-ec2-elb-connectionsettings)" : ConnectionSettings,
      "[CrossZone](#cfn-ec2-elb-crosszone)" : Boolean,
      "[HealthCheck](#cfn-ec2-elb-healthcheck)" : HealthCheck,
      "[Instances](#cfn-ec2-elb-instances)" : [ String, ... ],
      "[LBCookieStickinessPolicy](#cfn-ec2-elb-lbcookiestickinesspolicy)" : [ LBCookieStickinessPolicy, ... ],
      "[Listeners](#cfn-ec2-elb-listeners)" : [ Listeners, ... ],
      "[LoadBalancerName](#cfn-ec2-elb-elbname)" : String,
      "[Policies](#cfn-ec2-elb-policies)" : [ Policies, ... ],
      "[Scheme](#cfn-ec2-elb-scheme)" : String,
      "[SecurityGroups](#cfn-ec2-elb-securitygroups)" : [ String, ... ],
      "[Subnets](#cfn-ec2-elb-subnets)" : [ String, ... ],
      "[Tags](#cfn-elasticloadbalancing-loadbalancer-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-properties-ec2-elb-syntax.yaml"></a>

```
Type: AWS::ElasticLoadBalancing::LoadBalancer
Properties: 
  [AccessLoggingPolicy](#cfn-ec2-elb-accessloggingpolicy): 
    AccessLoggingPolicy
  [AppCookieStickinessPolicy](#cfn-ec2-elb-appcookiestickinesspolicy): 
    - AppCookieStickinessPolicy
  [AvailabilityZones](#cfn-ec2-elb-availabilityzones): 
    - String
  [ConnectionDrainingPolicy](#cfn-ec2-elb-connectiondrainingpolicy): 
    ConnectionDrainingPolicy
  [ConnectionSettings](#cfn-ec2-elb-connectionsettings): 
    ConnectionSettings
  [CrossZone](#cfn-ec2-elb-crosszone): Boolean
  [HealthCheck](#cfn-ec2-elb-healthcheck): 
    HealthCheck
  [Instances](#cfn-ec2-elb-instances): 
    - String
  [LBCookieStickinessPolicy](#cfn-ec2-elb-lbcookiestickinesspolicy): 
    - LBCookieStickinessPolicy
  [Listeners](#cfn-ec2-elb-listeners): 
    - Listeners
  [LoadBalancerName](#cfn-ec2-elb-elbname): String
  [Policies](#cfn-ec2-elb-policies): 
    - Policies
  [Scheme](#cfn-ec2-elb-scheme): String
  [SecurityGroups](#cfn-ec2-elb-securitygroups): 
    - String
  [Subnets](#cfn-ec2-elb-subnets): 
    - String
  [Tags](#cfn-elasticloadbalancing-loadbalancer-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-properties-ec2-elb-properties"></a>

`AccessLoggingPolicy`  <a name="cfn-ec2-elb-accessloggingpolicy"></a>
Information about where and how access logs are stored for the load balancer\.  
*Required*: No  
*Type*: [AccessLoggingPolicy](aws-properties-ec2-elb-accessloggingpolicy.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AppCookieStickinessPolicy`  <a name="cfn-ec2-elb-appcookiestickinesspolicy"></a>
Information about a policy for application\-controlled session stickiness\.  
*Required*: No  
*Type*: [List](aws-properties-ec2-elb-AppCookieStickinessPolicy.md) of [AppCookieStickinessPolicy](aws-properties-ec2-elb-AppCookieStickinessPolicy.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`AvailabilityZones`  <a name="cfn-ec2-elb-availabilityzones"></a>
The Availability Zones for the load balancer\. For load balancers in a VPC, specify `Subnets` instead\.  
Update requires replacement if you did not previously specify an Availability Zone or if you are removing all Availability Zones\. Otherwise, update requires no interruption\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [Some interruptions](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-some-interrupt)

`ConnectionDrainingPolicy`  <a name="cfn-ec2-elb-connectiondrainingpolicy"></a>
If enabled, the load balancer allows existing requests to complete before the load balancer shifts traffic away from a deregistered or unhealthy instance\.  
For more information, see [Configure Connection Draining](https://docs.aws.amazon.com/elasticloadbalancing/latest/classic/config-conn-drain.html) in the *Classic Load Balancers Guide*\.  
*Required*: No  
*Type*: [ConnectionDrainingPolicy](aws-properties-ec2-elb-connectiondrainingpolicy.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ConnectionSettings`  <a name="cfn-ec2-elb-connectionsettings"></a>
If enabled, the load balancer allows the connections to remain idle \(no data is sent over the connection\) for the specified duration\.  
By default, Elastic Load Balancing maintains a 60\-second idle connection timeout for both front\-end and back\-end connections of your load balancer\. For more information, see [Configure Idle Connection Timeout](https://docs.aws.amazon.com/elasticloadbalancing/latest/classic/config-idle-timeout.html) in the *Classic Load Balancers Guide*\.  
*Required*: No  
*Type*: [ConnectionSettings](aws-properties-ec2-elb-connectionsettings.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CrossZone`  <a name="cfn-ec2-elb-crosszone"></a>
If enabled, the load balancer routes the request traffic evenly across all instances regardless of the Availability Zones\.  
For more information, see [Configure Cross\-Zone Load Balancing](https://docs.aws.amazon.com/elasticloadbalancing/latest/classic/enable-disable-crosszone-lb.html) in the *Classic Load Balancers Guide*\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`HealthCheck`  <a name="cfn-ec2-elb-healthcheck"></a>
The health check settings to use when evaluating the health of your EC2 instances\.  
Update requires replacement if you did not previously specify health check settings or if you are removing the health check settings\. Otherwise, update requires no interruption\.  
*Required*: No  
*Type*: [HealthCheck](aws-properties-ec2-elb-health-check.md)  
*Update requires*: [Some interruptions](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-some-interrupt)

`Instances`  <a name="cfn-ec2-elb-instances"></a>
The IDs of the instances for the load balancer\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LBCookieStickinessPolicy`  <a name="cfn-ec2-elb-lbcookiestickinesspolicy"></a>
Information about a policy for duration\-based session stickiness\.  
*Required*: No  
*Type*: [List](aws-properties-ec2-elb-LBCookieStickinessPolicy.md) of [LBCookieStickinessPolicy](aws-properties-ec2-elb-LBCookieStickinessPolicy.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Listeners`  <a name="cfn-ec2-elb-listeners"></a>
The listeners for the load balancer\. You can specify at most one listener per port\.  
If you update the properties for a listener, AWS CloudFormation deletes the existing listener and creates a new one with the specified properties\. While the new listener is being created, clients cannot connect to the load balancer\.  
*Required*: Yes  
*Type*: [List](aws-properties-ec2-elb-listener.md) of [Listeners](aws-properties-ec2-elb-listener.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LoadBalancerName`  <a name="cfn-ec2-elb-elbname"></a>
The name of the load balancer\. This name must be unique within your set of load balancers for the region\.  
If you don't specify a name, AWS CloudFormation generates a unique physical ID for the load balancer\. For more information, see [Name Type](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-name.html)\. If you specify a name, you cannot perform updates that require replacement of this resource, but you can perform other updates\. To replace the resource, specify a new name\.   
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Policies`  <a name="cfn-ec2-elb-policies"></a>
The policies defined for your Classic Load Balancer\. Specify only back\-end server policies\.  
*Required*: No  
*Type*: [List](aws-properties-ec2-elb-policy.md) of [Policies](aws-properties-ec2-elb-policy.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Scheme`  <a name="cfn-ec2-elb-scheme"></a>
The type of load balancer\. Valid only for load balancers in a VPC\.  
If `Scheme` is `internet-facing`, the load balancer has a public DNS name that resolves to a public IP address\.  
If `Scheme` is `internal`, the load balancer has a public DNS name that resolves to a private IP address\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SecurityGroups`  <a name="cfn-ec2-elb-securitygroups"></a>
The security groups for the load balancer\. Valid only for load balancers in a VPC\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Subnets`  <a name="cfn-ec2-elb-subnets"></a>
The IDs of the subnets for the load balancer\. You can specify at most one subnet per Availability Zone\.  
Update requires replacement if you did not previously specify a subnet or if you are removing all subnets\. Otherwise, update requires no interruption\. To update to a different subnet in the current Availability Zone, you must first update to a subnet in a different Availability Zone, then update to the new subnet in the original Availability Zone\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [Some interruptions](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-some-interrupt)

`Tags`  <a name="cfn-elasticloadbalancing-loadbalancer-tags"></a>
The tags associated with a load balancer\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-properties-ec2-elb-return-values"></a>

### Ref<a name="aws-properties-ec2-elb-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the name of the load balancer\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-properties-ec2-elb-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-properties-ec2-elb-return-values-fn--getatt-fn--getatt"></a>

`CanonicalHostedZoneName`  <a name="CanonicalHostedZoneName-fn::getatt"></a>
The name of the Route 53 hosted zone that is associated with the load balancer\. Internal\-facing load balancers don't use this value, use `DNSName` instead\.

`CanonicalHostedZoneNameID`  <a name="CanonicalHostedZoneNameID-fn::getatt"></a>
The ID of the Route 53 hosted zone name that is associated with the load balancer\.

`DNSName`  <a name="DNSName-fn::getatt"></a>
The DNS name for the load balancer\.

`SourceSecurityGroup.GroupName`  <a name="SourceSecurityGroup.GroupName-fn::getatt"></a>
The name of the security group that you can use as part of your inbound rules for your load balancer's back\-end instances\.

`SourceSecurityGroup.OwnerAlias`  <a name="SourceSecurityGroup.OwnerAlias-fn::getatt"></a>
The owner of the source security group\.

## Examples<a name="aws-properties-ec2-elb--examples"></a>

### <a name="aws-properties-ec2-elb--examples--"></a>

The following example specifies a Classic Load Balancer with a secure listener\.

#### JSON<a name="aws-properties-ec2-elb--examples----json"></a>

```
"MyLoadBalancer" : {
    "Type": "AWS::ElasticLoadBalancing::LoadBalancer",
    "Properties": {
        "AvailabilityZones": [ "us-east-2a" ],
        "CrossZone": "true",
        "Listeners": [{
            "InstancePort": "80",
            "InstanceProtocol": "HTTP",
            "LoadBalancerPort": "443",
            "Protocol": "HTTPS",
            "PolicyNames": [ "My-SSLNegotiation-Policy" ],
            "SSLCertificateId": "arn:aws:iam::123456789012:server-certificate/my-server-certificate"
        }],
        "HealthCheck": {
            "Target": "HTTP:80/",
            "HealthyThreshold": "2",
            "UnhealthyThreshold": "3",
            "Interval": "10",
            "Timeout": "5"
        },
        "Policies": [{
            "PolicyName": "My-SSLNegotiation-Policy",
            "PolicyType": "SSLNegotiationPolicyType",
            "Attributes": [{
                "Name": "Reference-Security-Policy",
                "Value": "ELBSecurityPolicy-TLS-1-2-2017-01"
            }]
        }]
    }
}
```

#### YAML<a name="aws-properties-ec2-elb--examples----yaml"></a>

```
MyLoadBalancer:
    Type: AWS::ElasticLoadBalancing::LoadBalancer
    Properties:
      AvailabilityZones:
      - "us-east-2a"
      CrossZone: true
      Listeners:
      - InstancePort: '80'
        InstanceProtocol: HTTP
        LoadBalancerPort: '443'
        Protocol: HTTPS
        PolicyNames: 
        - My-SSLNegotiation-Policy
        SSLCertificateId: arn:aws:iam::123456789012:server-certificate/my-server-certificate
      HealthCheck:
        Target: HTTP:80/
        HealthyThreshold: '2'
        UnhealthyThreshold: '3'
        Interval: '10'
        Timeout: '5'
      Policies:
      - PolicyName: My-SSLNegotiation-Policy
        PolicyType: SSLNegotiationPolicyType
        Attributes:
        - Name: Reference-Security-Policy
          Value: ELBSecurityPolicy-TLS-1-2-2017-01
```

## See also<a name="aws-properties-ec2-elb--seealso"></a>
+  [Elastic Load Balancing Template Snippets](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/quickref-elb.html) 
+  [CreateLoadBalancer](https://docs.aws.amazon.com/elasticloadbalancing/2012-06-01/APIReference/API_CreateLoadBalancer.html) in the *Elastic Load Balancing API Reference \(version 2012\-06\-01\)* 
+  [ModifyLoadBalancerAttributes](https://docs.aws.amazon.com/elasticloadbalancing/2012-06-01/APIReference/API_ModifyLoadBalancerAttributes.html) in the *Elastic Load Balancing API Reference \(version 2012\-06\-01\)* 
+  [ConfigureHealthCheck](https://docs.aws.amazon.com/elasticloadbalancing/2012-06-01/APIReference/API_ConfigureHealthCheck.html) in the *Elastic Load Balancing API Reference \(version 2012\-06\-01\)* 
+  [User Guide for Classic Load Balancers](https://docs.aws.amazon.com/elasticloadbalancing/latest/classic) 

