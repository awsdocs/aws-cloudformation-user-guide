# `Fn::GetAtt`<a name="intrinsic-function-reference-getatt"></a>

The `Fn::GetAtt` intrinsic function returns the value of an attribute from a resource in the template\.

## Declaration<a name="w3ab2c21c28c31b5"></a>

### JSON<a name="intrinsic-function-reference-getatt-syntax.json"></a>

```
{ "Fn::GetAtt" : [ "logicalNameOfResource", "attributeName" ] }
```

### YAML<a name="intrinsic-function-reference-getatt-syntax.yaml"></a>

Syntax for the full function name:

```
Fn::GetAtt: [ logicalNameOfResource, attributeName ]
```

Syntax for the short form:

```
!GetAtt logicalNameOfResource.attributeName
```

## Parameters<a name="w3ab2c21c28c31b7"></a>

`logicalNameOfResource`  
The logical name \(also called *logical ID*\) of the resource that contains the attribute that you want\.

`attributeName`  
The name of the resource\-specific attribute whose value you want\. See the resource's reference page for details about the attributes available for that resource type\.

## Return Value<a name="intrinsic-function-reference-getatt-return"></a>

The attribute value\.

## Examples<a name="intrinsic-function-reference-getatt-examples"></a>

### <a name="intrinsic-function-reference-getatt-example"></a>

This example snippet returns a string containing the DNS name of the load balancer with the logical name `myELB`\.

#### JSON<a name="intrinsic-function-reference-getatt-example.json"></a>

```
1. "Fn::GetAtt" : [ "myELB" , "DNSName" ]
```

#### YAML<a name="intrinsic-function-reference-getatt-example.yaml"></a>

```
1. !GetAtt myELB.DNSName
```

#### <a name="intrinsic-function-reference-getatt-example2"></a>

The following example template returns the `SourceSecurityGroup.OwnerAlias` and `SourceSecurityGroup.GroupName` of the load balancer with the logical name `myELB`\.

##### JSON<a name="intrinsic-function-reference-getatt-example2.json"></a>

```
{
    "AWSTemplateFormatVersion": "2010-09-09",
    "Resources": {
        "myELB": {
            "Type": "AWS::ElasticLoadBalancing::LoadBalancer",
            "Properties": {
                "AvailabilityZones": [
                    "eu-west-1a"
                ],
                "Listeners": [
                    {
                        "LoadBalancerPort": "80",
                        "InstancePort": "80",
                        "Protocol": "HTTP"
                    }
                ]
            }
        },
        "myELBIngressGroup": {
            "Type": "AWS::EC2::SecurityGroup",
            "Properties": {
                "GroupDescription": "ELB ingress group",
                "SecurityGroupIngress": [
                    {
                        "IpProtocol": "tcp",
                        "FromPort": "80",
                        "ToPort": "80",
                        "SourceSecurityGroupOwnerId": {
                            "Fn::GetAtt": [
                                "myELB",
                                "SourceSecurityGroup",
                                "OwnerAlias"
                            ]
                        },
                        "SourceSecurityGroupName": {
                            "Fn::GetAtt": [
                                "myELB",
                                "SourceSecurityGroup",
                                "GroupName"
                            ]
                        }
                    }
                ]
            }
        }
    }
}
```

##### YAML<a name="intrinsic-function-reference-getatt-example2.yaml"></a>

```
AWSTemplateFormatVersion: 2010-09-09
Resources:
  myELB:
    Type: 'AWS::ElasticLoadBalancing::LoadBalancer'
    Properties:
      AvailabilityZones:
        - eu-west-1a
      Listeners:
        - LoadBalancerPort: '80'
          InstancePort: '80'
          Protocol: HTTP
  myELBIngressGroup:
    Type: 'AWS::EC2::SecurityGroup'
    Properties:
      GroupDescription: ELB ingress group
      SecurityGroupIngress:
        - IpProtocol: tcp
          FromPort: '80'
          ToPort: '80'
          SourceSecurityGroupOwnerId: !GetAtt myELB.SourceSecurityGroup.OwnerAlias
          SourceSecurityGroupName: !GetAtt myELB.SourceSecurityGroup.GroupName
```

## Supported Functions<a name="w3ab2c21c28c31c13"></a>

For the `Fn::GetAtt` logical resource name, you cannot use functions\. You must specify a string that is a resource's logical ID\.

For the `Fn::GetAtt` attribute name, you can use the `Ref` function\.

## Attributes<a name="intrinsic-function-reference-getatt-attrib"></a>

You can retrieve the following attributes using `Fn::GetAtt`\.


| Resource TypeName | Attribute | Description | 
| --- | --- | --- | 
|  [AWS::ApiGateway::DomainName](aws-resource-apigateway-domainname.md)  |  `DistributionDomainName`  |  The Amazon CloudFront distribution domain name that is mapped to the custom domain name\. Example: `d111111abcdef8.cloudfront.net`  | 
|  [AWS::ApiGateway::RestApi](aws-resource-apigateway-restapi.md)  |  `RootResourceId`  |  The root resource ID for a `RestApi` resource\. Example: `a0bc123d4e`  | 
|  [AWS::Cloud9::EnvironmentEC2](aws-resource-cloud9-environmentec2.md)  |  `Arn`  |  The Amazon Resource Name \(ARN\) of the AWS Cloud9 development environment\. Example: `arn:aws:cloud9:us-east-2:123456789012:environment:2bc3642873c342e485f7e0c561234567`  | 
|  [AWS::Cloud9::EnvironmentEC2](aws-resource-cloud9-environmentec2.md)  |  `Name`  |  The name of the AWS Cloud9 development environment\. Example: `my-demo-environment`  | 
|  [AWS::CloudFormation::WaitCondition](aws-properties-waitcondition.md)  |  `Data`  |  A JSON\-format string containing the `UniqueId` and `Data` values from the wait condition signal\(s\) for the specified wait condition\. For more information about wait condition signals, see [Wait Condition Signal JSON Format](using-cfn-waitcondition.md#using-cfn-waitcondition-signaljson)\. Example of a wait condition with two signals: <pre>{"Signal1":"Step 1 complete.","Signal2":"Step 2 complete."}</pre>  | 
|  [AWS::CloudFormation::Stack](aws-properties-stack.md)  |  `Outputs.NestedStackOutputName`  |  The output value from the nested stack that you specified, where *NestedStackOutputName* is the name of the output value\.  | 
|  [AWS::CloudFront::Distribution](aws-resource-cloudfront-distribution.md)  |  `DomainName`  |  Example: `d2fadu0nynjpfn.cloudfront.net`  | 
|  [AWS::CloudTrail::Trail](aws-resource-cloudtrail-trail.md)  |  `Arn`  |  Example: `arn:aws:cloudtrail:us-east-2:123456789012:trail/myCloudTrail`  | 
|  [AWS::CloudTrail::Trail](aws-resource-cloudtrail-trail.md)  |  `SnsTopicArn`  |  The Amazon Resource Name \(ARN\) of the Amazon SNS topic that is associated with the CloudTrail trail\. Example: `arn:aws:sns:us-east-2:123456789012:mySNSTopic`  | 
|  [AWS::CloudWatch::Alarm](aws-properties-cw-alarm.md)  |  `Arn`  |  Example: `arn:aws:cloudwatch:us-east-2:123456789012:alarm:myCloudWatchAlarm-CPUAlarm-UXMMZK36R55Z`  | 
|  [AWS::CodeBuild::Project](aws-resource-codebuild-project.md)  |  `Arn`  |  Example: `arn:aws:codebuild:us-west-2:123456789012:project/myProjectName`  | 
|  [AWS::CodeCommit::Repository](aws-resource-codecommit-repository.md)  |  `Arn`  |  Example: `arn:aws:codecommit:``us-east-2``:123456789012:MyDemoRepo`  | 
|  [AWS::CodeCommit::Repository](aws-resource-codecommit-repository.md)  |  `CloneUrlHttp`  |  Example: `https://codecommit.``us-east-2``.amazonaws.com/v1/repos/MyDemoRepo`  | 
|  [AWS::CodeCommit::Repository](aws-resource-codecommit-repository.md)  |  `CloneUrlSsh`  |  Example: `ssh://git-codecommit.``us-east-2``.amazonaws.com/v1/repos//v1/repos/MyDemoRepo`  | 
|  [AWS::CodeCommit::Repository](aws-resource-codecommit-repository.md)  |  `Name`  |  Example: `MyDemoRepo`  | 
|  [AWS::Config::ConfigRule](aws-resource-config-configrule.md)  |  `Arn`  |  Example: `arn:aws:config:``us-east-2``:123456789012:config-rule/config-rule-a1bzhi`  | 
|  [AWS::Config::ConfigRule](aws-resource-config-configrule.md)  |  `ConfigRuleId`  |  Example: `config-rule-a1bzhi`  | 
|  [AWS::Config::ConfigRule](aws-resource-config-configrule.md)  |  `Compliance.Type`  |  Example: `COMPLIANT`  | 
|  [AWS::DAX::Cluster](aws-resource-dax-cluster.md)  |  `Arn`  |  Example: `arn:aws:dax:us-east-1:111122223333:cache/MyDAXCluster`  | 
|  [AWS::DAX::Cluster](aws-resource-dax-cluster.md)  |  `ClusterDiscoveryEndpoint`  |  Example: `mydaxcluster.0h3d6x.clustercfg.dax.use1.cache.amazonaws.com:8111`  | 
|  [AWS::DirectoryService::MicrosoftAD](aws-resource-directoryservice-microsoftad.md) and [AWS::DirectoryService::SimpleAD](aws-resource-directoryservice-simplead.md)  |  `Alias`  |  The alias for a directory\. Examples: `d-12373a053a` or `alias4-mydirectory-12345abcgmzsk` \(if you have the `CreateAlias` property set to true\)  | 
|  [AWS::DirectoryService::MicrosoftAD](aws-resource-directoryservice-microsoftad.md) and [AWS::DirectoryService::SimpleAD](aws-resource-directoryservice-simplead.md)  |  `DnsIpAddresses`  |  The IP addresses of the DNS servers for the directory\. Example: `[ "192.0.2.1", "192.0.2.2" ]`  | 
|  [AWS::DynamoDB::Table](aws-resource-dynamodb-table.md)  |  `Arn`  |  Example: `arn:aws:dynamodb:us-east-2:123456789012:table/myDynamoDBTable`  | 
|  [AWS::DynamoDB::Table](aws-resource-dynamodb-table.md)  |  `StreamArn`  |  The Amazon Resource Name \(ARN\) of the DynamoDB table stream\. To use this attribute, you must specify the DynamoDB table `StreamSpecification` property\. Example: `arn:aws:dynamodb:us-east-2:123456789012:table/testddbstack-myDynamoDBTable-012A1SL7SMP5Q/stream/2015-11-30T20:10:00.000`  | 
|  [AWS::EC2::EIP](aws-properties-ec2-eip.md)  |  `AllocationId`  |  The ID that AWS assigns to represent the allocation of the address for use with Amazon VPC\. It is returned only for VPC Elastic IP addresses\. Example: `eipalloc-5723d13e`  | 
|  [AWS::EC2::Instance](aws-properties-ec2-instance.md)  |  `AvailabilityZone`  |  The Availability Zone where the instance that you specified is launched\. Example: `us-east-1b`  | 
|  [AWS::EC2::Instance](aws-properties-ec2-instance.md)  |  `PrivateDnsName`  |  The private DNS name of the instance that you specified\. Example: `ip-10-24-34-0.ec2.internal`  | 
|  [AWS::EC2::Instance](aws-properties-ec2-instance.md)  |  `PublicDnsName`  |  The public DNS name of the instance that you specified\. Example: `ec2-107-20-50-45.compute-1.amazonaws.com`  | 
|  [AWS::EC2::Instance](aws-properties-ec2-instance.md)  |  `PrivateIp`  |  The private IP address of the instance that you specified\. Example: `10.24.34.0`  | 
|  [AWS::EC2::Instance](aws-properties-ec2-instance.md)  |  `PublicIp`  |  The public IP address of the instance that you specified\. Example: `192.0.2.0`  | 
|  [AWS::EC2::NetworkInterface](aws-resource-ec2-network-interface.md)  |  `PrimaryPrivateIpAddress`  |  The primary private IP address of the network interface that you specified\. Example: `10.0.0.192`  | 
|  [AWS::EC2::NetworkInterface](aws-resource-ec2-network-interface.md)  |  `SecondaryPrivateIpAddresses`  |  The secondary private IP addresses of the network interface that you specified\. Example: `["10.0.0.161", "10.0.0.162", "10.0.0.163"]`  | 
|  [AWS::EC2::SecurityGroup](aws-properties-ec2-security-group.md)  |  `GroupId`  |  The group ID of the specified security group\. Example: `sg-94b3a1f6`  | 
|  [AWS::EC2::Subnet](aws-resource-ec2-subnet.md)  |  `AvailabilityZone`  |  The Availability Zone of the subnet\. Example: `us-east-1a`  | 
|  [AWS::EC2::Subnet](aws-resource-ec2-subnet.md)  |  `Ipv6CidrBlocks`  |  A list of IPv6 CIDR blocks that are associated with the subnet\. Example: `[ 2001:db8:1234:1a00::/64 ]`  | 
|  [AWS::EC2::Subnet](aws-resource-ec2-subnet.md)  |  `NetworkAclAssociationId`  |  The ID of the network ACL that is associated with the subnet's VPC\. Example: `acl-5fb85d36`  | 
|  [AWS::EC2::Subnet](aws-resource-ec2-subnet.md)  |  `VpcId`  |  The ID of the subnet's VPC\. Example: `vpc-11ad4878`  | 
|  [AWS::EC2::SubnetNetworkAclAssociation](aws-resource-ec2-subnet-network-acl-assoc.md)  |  `AssociationId`  |  The `NetworkAcl associationId` that is attached to a subnet\.  | 
|  [AWS::EC2::VPC](aws-resource-ec2-vpc.md)  |  `CidrBlock`  |  The set of IP addresses for the VPC\. Example: `10.0.0.0/16`  | 
|  [AWS::EC2::VPC](aws-resource-ec2-vpc.md)  |  `CidrBlockAssociations`  |  A list of IPv4 CIDR block association IDs for the VPC\. Example: `[ vpc-cidr-assoc-0280ab6b ]`  | 
|  [AWS::EC2::VPC](aws-resource-ec2-vpc.md)  |  `DefaultNetworkAcl`  |  The default network ACL ID that is associated with the VPC, which AWS creates when you create a VPC\. Example: `acl-814dafe3`  | 
|  [AWS::EC2::VPC](aws-resource-ec2-vpc.md)  |  `DefaultSecurityGroup`  |  The default security group ID that is associated with the VPC, which AWS creates when you create a VPC\. Example: `sg-b178e0d3`  | 
|  [AWS::EC2::VPC](aws-resource-ec2-vpc.md)  |  `Ipv6CidrBlocks`  |  A list of IPv6 CIDR blocks that are associated with the VPC\. Example: `[ 2001:db8:1234:1a00::/56 ]`  | 
|  [AWS::ECS::Cluster](aws-resource-ecs-cluster.md)  |  `Arn`  |  Example: `arn:aws:ecs:us-east-2:123456789012:cluster/MyECSCluster`  | 
|  [AWS::ECS::Service](aws-resource-ecs-service.md)  |  `Name`  |  The name of an Amazon Elastic Container Service service\. Example: `sample-webapp`  | 
|  [AWS::EKS::Cluster](aws-resource-eks-cluster.md)  |  `Arn`  |  The ARN of the cluster\. Example: `arn:aws:eks:us-east-2:123456789012:cluster/MyECSCluster`  | 
|  [AWS::EKS::Cluster](aws-resource-eks-cluster.md)  |  `CertificateAuthorityData`  |  The `certificate-authority-data` for your cluster\.   | 
|  [AWS::EKS::Cluster](aws-resource-eks-cluster.md)  |  `Endpoint`  |  The endpoint for your Kubernetes API server\. Example: `https://EXAMPLEFBBB3BA591B746AFC5AB30262.yl4.us-west-2.eks.amazonaws.com`  | 
|  [AWS::ElastiCache::CacheCluster](aws-properties-elasticache-cache-cluster.md)  |  `ConfigurationEndpoint.Address`  |  The DNS address of the configuration endpoint for the Memcached cache cluster\. Example: `test.abc12a.cfg.use1.cache.amazonaws.com:11111`  | 
|  [AWS::ElastiCache::CacheCluster](aws-properties-elasticache-cache-cluster.md)  |  `ConfigurationEndpoint.Port`  |  The port number of the configuration endpoint for the Memcached cache cluster\.  | 
|  [AWS::ElastiCache::CacheCluster](aws-properties-elasticache-cache-cluster.md)  |  `RedisEndpoint.Address`  |  The DNS address of the configuration endpoint for the Redis cache cluster\. Example: `test.abc12a.cfg.use1.cache.amazonaws.com:11111`  | 
|  [AWS::ElastiCache::CacheCluster](aws-properties-elasticache-cache-cluster.md)  |  `RedisEndpoint.Port`  |  The port number of the configuration endpoint for the Redis cache cluster\.  | 
|  [AWS::ElastiCache::ReplicationGroup](aws-resource-elasticache-replicationgroup.md)  |  `ConfigurationEndPoint.Address`  |  The DNS hostname of the cache node\.  | 
|  [AWS::ElastiCache::ReplicationGroup](aws-resource-elasticache-replicationgroup.md)  |  `ConfigurationEndPoint.Port`  |  The port number that the cache engine is listening on\.  | 
|  [AWS::ElastiCache::ReplicationGroup](aws-resource-elasticache-replicationgroup.md)  |  `PrimaryEndPoint.Address`  |  The DNS address of the primary read\-write cache node\.  | 
|  [AWS::ElastiCache::ReplicationGroup](aws-resource-elasticache-replicationgroup.md)  |  `PrimaryEndPoint.Port`  |  The port number that the primary read\-write cache engine is listening on\.  | 
|  [AWS::ElastiCache::ReplicationGroup](aws-resource-elasticache-replicationgroup.md)  |  `ReadEndPoint.Addresses`  |  A string with a list of endpoints for the read\-only replicas\. The order of the addresses maps to the order of the ports from the `ReadEndPoint.Ports` attribute\. Example: `"[abc12xmy3d1w3hv6-001.rep12a.0001.use1.cache.amazonaws.com, abc12xmy3d1w3hv6-002.rep12a.0001.use1.cache.amazonaws.com, abc12xmy3d1w3hv6-003.rep12a.0001.use1.cache.amazonaws.com]"`  | 
|  [AWS::ElastiCache::ReplicationGroup](aws-resource-elasticache-replicationgroup.md)  |  `ReadEndPoint.Ports`  |  A string with a list of ports for the read\-only replicas\. The order of the ports maps to the order of the addresses from the `ReadEndPoint.Addresses` attribute\. Example: `"[6379, 6379, 6379]"`  | 
|  [AWS::ElastiCache::ReplicationGroup](aws-resource-elasticache-replicationgroup.md)  |  `ReadEndPoint.Addresses.List`  |  A list of endpoints for the read\-only replicas\. Example: `["abc12xmy3d1w3hv6-001.rep12a.0001.use1.cache.amazonaws.com", "abc12xmy3d1w3hv6-002.rep12a.0001.use1.cache.amazonaws.com", "abc12xmy3d1w3hv6-003.rep12a.0001.use1.cache.amazonaws.com"]`  | 
|  [AWS::ElastiCache::ReplicationGroup](aws-resource-elasticache-replicationgroup.md)  |  `ReadEndPoint.Ports.List`  |  A list of ports for the read\-only replicas\. Example: `["6379","6379","6379"]`  | 
|  [AWS::ElasticBeanstalk::Environment](aws-properties-beanstalk-environment.md)  |  `EndpointURL`  |  The URL to the load balancer for this environment\. Example: `awseb-myst-myen-132MQC4KRLAMD-1371280482.``us-east-2``.elb.amazonaws.com`  | 
|  [AWS::ElasticLoadBalancing::LoadBalancer](aws-properties-ec2-elb.md)  |  `CanonicalHostedZoneName`  |  The name of the Route 53\-hosted zone that is associated with the load balancer\. Example: `mystack-myelb-15HMABG9ZCN57-1013119603.``us-east-2``.elb.amazonaws.com`  | 
|  [AWS::ElasticLoadBalancing::LoadBalancer](aws-properties-ec2-elb.md)  |  `CanonicalHostedZoneNameID`  |  The ID of the Route 53 hosted zone name that is associated with the l oad balancer\. Example: `Z3DZXE0Q79N41H`  | 
|  [AWS::ElasticLoadBalancing::LoadBalancer](aws-properties-ec2-elb.md)  |  `DNSName`  |  The DNS name for the load balancer\. Example: `mystack-myelb-15HMABG9ZCN57-1013119603.``us-east-2``.elb.amazonaws.com`  | 
|  [AWS::ElasticLoadBalancing::LoadBalancer](aws-properties-ec2-elb.md)  |  `SourceSecurityGroup.GroupName`  |  The security group that you can use as part of your inbound rules for your load balancer's back\-end Amazon EC2 application instances\. Example: `amazon-elb`  | 
|  [AWS::ElasticLoadBalancing::LoadBalancer](aws-properties-ec2-elb.md)  |  `SourceSecurityGroup.OwnerAlias`  |  The owner of the source security group\. Example: `amazon-elb-sg`  | 
|  [AWS::ElasticLoadBalancingV2::LoadBalancer](aws-resource-elasticloadbalancingv2-loadbalancer.md)  |  `DNSName`  |  The DNS name for the application load balancer\. Example: `my-load-balancer-424835706.us-west-2.elb.amazonaws.com`  | 
|  [AWS::ElasticLoadBalancingV2::LoadBalancer](aws-resource-elasticloadbalancingv2-loadbalancer.md)  |  `CanonicalHostedZoneID`  |  The ID of the Amazon Route 53\-hosted zone name that is associated with the load balancer\. Example: `Z2P70J7EXAMPLE`  | 
|  [AWS::ElasticLoadBalancingV2::LoadBalancer](aws-resource-elasticloadbalancingv2-loadbalancer.md)  |  `LoadBalancerFullName`  |  The full name of the application load balancer\. Example: `app/my-load-balancer/50dc6c495c0c9188`  | 
|  [AWS::ElasticLoadBalancingV2::LoadBalancer](aws-resource-elasticloadbalancingv2-loadbalancer.md)  |  `LoadBalancerName`  |  The name of the application load balancer\. Example: `my-load-balancer`  | 
|  [AWS::ElasticLoadBalancingV2::LoadBalancer](aws-resource-elasticloadbalancingv2-loadbalancer.md)  |  `SecurityGroups`  |  The IDs of the security groups for the application load balancer\. Example: `sg-123456a`  | 
|  [AWS::ElasticLoadBalancingV2::TargetGroup](aws-resource-elasticloadbalancingv2-targetgroup.md)  |  `LoadBalancerArns`  |  The Amazon Resource Names \(ARNs\) of the load balancers that route traffic to this target group\. Example: `[ "arn:aws:elasticloadbalancing:us-west-2:123456789012:loadbalancer/app/my-load-balancer/50dc6c495c0c9188" ]`  | 
|  [AWS::ElasticLoadBalancingV2::TargetGroup](aws-resource-elasticloadbalancingv2-targetgroup.md)  |  `TargetGroupFullName`  | The full name of the target group\.Example: `targetgroup/my-target-group/cbf133c568e0d028` | 
|  [AWS::ElasticLoadBalancingV2::TargetGroup](aws-resource-elasticloadbalancingv2-targetgroup.md)  |  `TargetGroupName`  | The name of the target group\.Example: `my-target-group` | 
|  [AWS::Elasticsearch::Domain](aws-resource-elasticsearch-domain.md)  |  `DomainArn`  |  The Amazon Resource Name \(ARN\) of the domain\. Example: `arn:aws:es:us-west-2:123456789012:domain/mystack-elasti-1ab2cdefghij`  | 
|  [AWS::Elasticsearch::Domain](aws-resource-elasticsearch-domain.md)  |  `DomainEndpoint`  |  The domain\-specific endpoint that is used to submit index, search, and data upload requests to an Amazon Elasticsearch Service domain\. Example: `search-mystack-elasti-1ab2cdefghij-ab1c2deckoyb3hofw7wpqa3cm.us-west-2.es.amazonaws.com`  | 
|  [AWS::EMR::Cluster](aws-resource-emr-cluster.md)  |  `MasterPublicDNS`  |  The public DNS name of the master node \(instance\)\. Example: `ec2-12-123-123-123.us-west-2.compute.amazonaws.com`  | 
|  [AWS::Events::Rule](aws-resource-events-rule.md)  |  `Arn`  |  Example: `arn:aws:events:``us-east-2``:123456789012:rule/example`  | 
|  [AWS::IAM::AccessKey](aws-properties-iam-accesskey.md)  |  `SecretAccessKey`  |  The secret access key for the specified `Access Key`\. Example: `wJalrXUtnFEMI/K7MDENG/bPxRfiCYzEXAMPLEKEY`  | 
|  [AWS::IAM::Group](aws-properties-iam-group.md)  |  `Arn`  |  Example: `arn:aws:iam::123456789012:group/mystack-mygroup-1DZETITOWEKVO`  | 
|  [AWS::IAM::InstanceProfile](aws-resource-iam-instanceprofile.md)  |  `Arn`  |  Example: `arn:aws:iam::1234567890:instance-profile/MyProfile-ASDNSDLKJ`  | 
|  [AWS::IAM::Role](aws-resource-iam-role.md)  |  `Arn`  |  Example: `arn:aws:iam::1234567890:role/MyRole-AJJHDSKSDF`  | 
|  [AWS::IAM::User](aws-properties-iam-user.md)  |  `Arn`  |  Example: `arn:aws:iam::123456789012:user/mystack-myuser-1CCXAFG2H2U4D`  | 
|  [AWS::IoT::Certificate](aws-resource-iot-certificate.md)  | Arn | Example: arn:aws:iot:ap\-southeast\-2:123456789012:cert/a1234567b89c012d3e4fg567hij8k9l01mno1p23q45678901rs234567890t1u2 | 
|  [AWS::IoT::Policy](aws-resource-iot-policy.md)  |  `Arn`  |  Example: `arn:aws:iot:us-east-2:123456789012:policy/MyIoTPolicy`  | 
|  [AWS::IoT::TopicRule](aws-resource-iot-topicrule.md)  |  `Arn`  |  Example: `arn:aws:iot:us-east-2:123456789012:rule/MyIoTRule`  | 
|  [AWS::Kinesis::Stream](aws-resource-kinesis-stream.md)  |  `Arn`  |  Example: `arn:aws:kinesis:``us-east-2``:123456789012:stream/stream-name`  | 
|  [AWS::KinesisFirehose::DeliveryStream](aws-resource-kinesisfirehose-deliverystream.md)  |  `Arn`  |  Example: `arn:aws:firehose:``us-east-2``:123456789012:deliverystream/delivery-stream-name`  | 
|  [AWS::KMS::Key](aws-resource-kms-key.md)  |  `Arn`  |  Example: `arn:aws:kms:us-west-2:123456789012:key/12a34567-8c90-1defg-af84-0bf06c1747f3`  | 
|  [AWS::Lambda::Function](aws-resource-lambda-function.md)  |  `Arn`  |  Example: `arn:aws:lambda:us-west-2:123456789012:MyStack-AMILookUp-NT5EUXTNTXXD`  | 
|  [AWS::Lambda::Version](aws-resource-lambda-version.md)  |  `Version`  |  The version of a Lambda function\. Example: `1`  | 
|  [AWS::Logs::Destination](aws-resource-logs-destination.md)  |  `Arn`  |  Example: `arn:aws:logs:us-east-2:123456789012:destination:MyDestination`  | 
|  [AWS::Logs::LogGroup](aws-resource-logs-loggroup.md)  |  `Arn`  |  Example: `arn:aws:logs:``us-east-2``:123456789012:log-group:/mystack-testgroup-12ABC1AB12A1:*`  | 
|  [AWS::OpsWorks::Instance](aws-resource-opsworks-instance.md)  |  `AvailabilityZone`  |  The Availability Zone of an AWS OpsWorks instance\. Example: `us-east-2a`\.  | 
|  [AWS::OpsWorks::Instance](aws-resource-opsworks-instance.md)  |  `PrivateDnsName`  |  The private DNS name of an AWS OpsWorks instance\.  | 
|  [AWS::OpsWorks::Instance](aws-resource-opsworks-instance.md)  |  `PrivateIp`  |  The private IP address of an AWS OpsWorks instance\.  | 
|  [AWS::OpsWorks::Instance](aws-resource-opsworks-instance.md)  |  `PublicDnsName`  |  The public DNS name of an AWS OpsWorks instance\.  | 
|  [AWS::OpsWorks::Instance](aws-resource-opsworks-instance.md)  |  `PublicIp`  |  The public IP address of an AWS OpsWorks instance\.  To use this attribute, the AWS OpsWorks instance must be in an AWS OpsWorks layer that auto\-assigns public IP addresses\.  Example: `192.0.2.0`  | 
|  [AWS::OpsWorks::UserProfile](aws-resource-opsworks-userprofile.md)  |  `SshUserName`  |  The SSH user name of an AWS OpsWorks instance\.  | 
|  [AWS::Redshift::Cluster](aws-resource-redshift-cluster.md)  |  `Endpoint.Address`  |  The connection endpoint for the cluster\. Example: `examplecluster.cg034hpkmmjt.``us-east-2``.redshift.amazonaws.com`  | 
|  [AWS::Redshift::Cluster](aws-resource-redshift-cluster.md)  |  `Endpoint.Port`  |  The connection port for the cluster\. Example: `5439`  | 
| [AWS::RDS::DBCluster](aws-resource-rds-dbcluster.md) |  `Endpoint.Address`  |  The connection endpoint for the DB cluster\. Example: `mystack-mydbcluster-1apw1j4phylrk.cg034hpkmmjt.``us-east-2``.rds.amazonaws.com`  | 
|  [AWS::RDS::DBCluster](aws-resource-rds-dbcluster.md)  |  `Endpoint.Port`  |  The port number on which the DB cluster accepts connections\. Example: `3306`  | 
|  [AWS::RDS::DBCluster](aws-resource-rds-dbcluster.md)  |  `ReadEndpoint.Address`  |  The reader endpoint for the DB cluster\. Example: `mystack-mydbcluster-ro-1apw1j4phylrk.cg034hpkmmjt.``us-east-2``.rds.amazonaws.com`  | 
|  [AWS::RDS::DBInstance](aws-properties-rds-database-instance.md)  |  `Endpoint.Address`  |  The connection endpoint for the database\. Example: `mystack-mydb-1apw1j4phylrk.cg034hpkmmjt.``us-east-2``.rds.amazonaws.com`  | 
|  [AWS::RDS::DBInstance](aws-properties-rds-database-instance.md)  |  `Endpoint.Port`  |  The port number on which the database accepts connections\. Example: `3306`  | 
|  [AWS::Route53::HostedZone](aws-resource-route53-hostedzone.md)  |  `NameServers`  |  The set of name servers for the specific hosted zone\. Example: `ns1.example.com` This attribute is not supported for private hosted zones\.  | 
|  [AWS::S3::Bucket](aws-properties-s3-bucket.md)  |  `Arn`  |  Example: `arn:aws:s3:::mybucket`  | 
|  [AWS::S3::Bucket](aws-properties-s3-bucket.md)  |  `DomainName`  |  The DNS name of the specified bucket\. Example: `mystack-mybucket-kdwwxmddtr2g.s3.amazonaws.com`  | 
|  [AWS::S3::Bucket](aws-properties-s3-bucket.md)  |  `DualStackDomainName`  |  The IPv6 DNS name of the specified bucket\. Example: `mystack-mybucket-kdwwxmddtr2g.s3.dualstack.``us-east-2``.amazonaws.com/`  | 
|  [AWS::S3::Bucket](aws-properties-s3-bucket.md)  |  `WebsiteURL`  |  The Amazon S3 website endpoint for the specified bucket\. Example: `http://mystack-mybucket-kdwwxmddtr2g.s3-website-``us-east-2``.amazonaws.com/`  | 
|  [AWS::Serverless::Function](transform-aws-serverless.md)  |  No attribute\.  |  The ARN of an `AWS::Serverless::Function` resource\.  | 
|  [AWS::ServiceDiscovery::PrivateDnsNamespace](aws-resource-servicediscovery-privatednsnamespace.md)  |  `Id`  |  Example: `ns-t2kl4fs6xexample`  | 
|  [AWS::ServiceDiscovery::PrivateDnsNamespace](aws-resource-servicediscovery-privatednsnamespace.md)  |  `Arn`  |  Example: `arn:aws:servicediscovery:us-west-2:1234567890:namespace/ns-t2kl4fs6xexample`  | 
|  [AWS::ServiceDiscovery::PublicDnsNamespace](aws-resource-servicediscovery-publicdnsnamespace.md)  |  `Id`  |  Example: `ns-d6wz3hq6kexample`  | 
|  [AWS::ServiceDiscovery::PublicDnsNamespace](aws-resource-servicediscovery-publicdnsnamespace.md)  |  `Arn`  |  Example: `arn:aws:servicediscovery:us-west-2:1234567890:namespace/ns-d6wz3hq6kexample`  | 
|  [AWS::ServiceDiscovery::Service](aws-resource-servicediscovery-service.md)  |  `Id`  |  Example: `srv-7dfj3r6cyexample`  | 
|  [AWS::ServiceDiscovery::Service](aws-resource-servicediscovery-service.md)  |  `Arn`  |  Example: `arn:aws:servicediscovery:us-west-2:1234567890:service/srv-7dfj3r6cyexample`  | 
|  [AWS::ServiceDiscovery::Service](aws-resource-servicediscovery-service.md)  |  `Name`  |  Example: `example`  | 
| [AWS::SNS::Topic](aws-properties-sns-topic.md) | TopicName |  The name of an Amazon SNS topic\. Example: `my-sns-topic`  | 
| [AWS::StepFunctions::Activity](aws-resource-stepfunctions-activity.md) | Name | The name of the AWS Step Functions activity\. | 
| [AWS::StepFunctions::StateMachine](aws-resource-stepfunctions-statemachine.md) | Name | The name of the Step Functions state machine\. | 
|  [AWS::SQS::Queue](aws-properties-sqs-queues.md)  |  `Arn`  |  Example: `arn:aws:sqs:``us-east-2``:123456789012:mystack-myqueue-15PG5C2FC1CW8`  | 
|  [AWS::SQS::Queue](aws-properties-sqs-queues.md)  |  `QueueName`  |  The name of an Amazon SQS queue\. Example: `mystack-myqueue-1VF9BKQH5BJVI`  | 