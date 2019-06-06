# `Fn::GetAtt`<a name="intrinsic-function-reference-getatt"></a>

The `Fn::GetAtt` intrinsic function returns the value of an attribute from a resource in the template\.

## Declaration<a name="getatt-declaration"></a>

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

## Parameters<a name="getatt-parameters"></a>

`logicalNameOfResource`  
The logical name \(also called *logical ID*\) of the resource that contains the attribute that you want\.

`attributeName`  
The name of the resource\-specific attribute whose value you want\. See the resource's reference page for details about the attributes available for that resource type\.

## Return Value<a name="intrinsic-function-reference-getatt-return"></a>

The attribute value\.

## Examples<a name="intrinsic-function-reference-getatt-examples"></a>

### Return a String<a name="intrinsic-function-reference-getatt-example"></a>

This example snippet returns a string containing the DNS name of the load balancer with the logical name `myELB`\.

#### JSON<a name="intrinsic-function-reference-getatt-example.json"></a>

```
1. "Fn::GetAtt" : [ "myELB" , "DNSName" ]
```

#### YAML<a name="intrinsic-function-reference-getatt-example.yaml"></a>

```
1. !GetAtt myELB.DNSName
```

#### Return Multiple Strings<a name="intrinsic-function-reference-getatt-example2"></a>

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
                                "SourceSecurityGroup.OwnerAlias"
                            ]
                        },
                        "SourceSecurityGroupName": {
                            "Fn::GetAtt": [
                                "myELB",
                                "SourceSecurityGroup.GroupName"
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
    Type: AWS::ElasticLoadBalancing::LoadBalancer
    Properties:
      AvailabilityZones:
        - eu-west-1a
      Listeners:
        - LoadBalancerPort: '80'
          InstancePort: '80'
          Protocol: HTTP
  myELBIngressGroup:
    Type: AWS::EC2::SecurityGroup
    Properties:
      GroupDescription: ELB ingress group
      SecurityGroupIngress:
        - IpProtocol: tcp
          FromPort: '80'
          ToPort: '80'
          SourceSecurityGroupOwnerId: !GetAtt myELB.SourceSecurityGroup.OwnerAlias
          SourceSecurityGroupName: !GetAtt myELB.SourceSecurityGroup.GroupName
```

## Supported Functions<a name="getatt-supported-functions"></a>

For the `Fn::GetAtt` logical resource name, you cannot use functions\. You must specify a string that is a resource's logical ID\.

For the `Fn::GetAtt` attribute name, you can use the `Ref` function\.

## Attributes<a name="intrinsic-function-reference-getatt-attrib"></a>

You can retrieve the following attributes using `Fn::GetAtt`\.


| Resource TypeName | Attribute | Description | 
| --- | --- | --- | 
| [AWS::AmazonMQ::Broker](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-amazonmq-broker.html) | Arn | The Amazon Resource Name \(ARN\) of the Amazon MQ broker\. Example: arn:aws:mq:us\-east\-2:123456789012:broker:MyBroker:b\-1234a5b6\-78cd\-901e\-2fgh\-3i45j6k178l9 | 
| [AWS::AmazonMQ::Broker](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-amazonmq-broker.html) | ConfigurationId | The unique ID that Amazon MQ generates for the configuration\.Example: c\-1234a5b6\-78cd\-901e\-2fgh\-3i45j6k178l9 | 
| [AWS::AmazonMQ::Broker](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-amazonmq-broker.html) | ConfigurationRevision | The revision number of the Amazon MQ configuration\.Example: 1 | 
| [AWS::AmazonMQ::Configuration](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-amazonmq-configuration.html) | Arn | The Amazon Resource Name \(ARN\) of the Amazon MQ configuration\.Example: arn:aws:mq:us\-east\-2:123456789012:configuration:MyConfigurationDevelopment:c\-1234a5b6\-78cd\-901e\-2fgh\-3i45j6k178l9 | 
| [AWS::AmazonMQ::Configuration](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-amazonmq-configuration.html) | Revision | The revision number of the Amazon MQ configuration\.Example: 1 | 
|  [AWS::ApiGateway::DomainName](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-apigateway-domainname.html)  |  `DistributionDomainName`  |  The Amazon CloudFront distribution domain name that is mapped to the custom domain name\. Example: `d111111abcdef8.cloudfront.net`  | 
|  [AWS::ApiGateway::RestApi](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-apigateway-restapi.html)  |  `RootResourceId`  |  The root resource ID for a `RestApi` resource\. Example: `a0bc123d4e`  | 
|  [AWS::ApiGatewayV2::DomainName](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-apigatewayv2-domainname.html)  |  `RegionalDomainName`  |  The domain name associated with the regional endpoint for this custom domain name\. You set up this association by adding a DNS record that points the custom domain name to this regional domain name\.  | 
|  [AWS::ApiGatewayV2::DomainName](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-apigatewayv2-domainname.html)  |  `RegionalHostedZoneId`  |  The region\-specific Amazon Route 53 Hosted Zone ID of the regional endpoint\.  | 
|  [AWS::AppMesh::Mesh](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-appmesh-mesh.html)  |  `Arn`  |  The full Amazon Resource Name \(ARN\) for the mesh\.  | 
|  [AWS::AppMesh::Mesh](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-appmesh-mesh.html)  |  `MeshName`  |  The name of the service mesh\.  | 
|  [AWS::AppMesh::Mesh](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-appmesh-mesh.html)  |  `Uid`  |  The unique identifier for the mesh\.  | 
|  [AWS::AppMesh::Route](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-appmesh-route.html)  |  `Arn`  |  The full Amazon Resource Name \(ARN\) for the route\.  | 
|  [AWS::AppMesh::Route](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-appmesh-route.html)  |  `MeshName`  |  The name of the service mesh that the route resides in\.  | 
|  [AWS::AppMesh::Route](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-appmesh-route.html)  |  `RouteName`  |  The name of the route\.  | 
|  [AWS::AppMesh::Route](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-appmesh-route.html)  |  `Uid`  |  The unique identifier for the route\.  | 
|  [AWS::AppMesh::Route](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-appmesh-route.html)  |  `VirtualRouterName`  |  The name of the virtual router that the route is associated with\.  | 
|  [AWS::AppMesh::VirtualNode](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-appmesh-virtualnode.html)  |  `Arn`  |  The full Amazon Resource Name \(ARN\) for the virtual node\.  | 
|  [AWS::AppMesh::VirtualNode](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-appmesh-virtualnode.html)  |  `MeshName`  |  The name of the service mesh that the virtual node resides in\.  | 
|  [AWS::AppMesh::VirtualNode](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-appmesh-virtualnode.html)  |  `Uid`  |  The unique identifier for the virtual node\.  | 
|  [AWS::AppMesh::VirtualNode](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-appmesh-virtualnode.html)  |  `VirtualNodeName`  |  The name of the virtual node\.  | 
|  [AWS::AppMesh::VirtualRouter](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-appmesh-virtualrouter.html)  |  `Arn`  |  The full Amazon Resource Name \(ARN\) for the virtual router\.  | 
|  [AWS::AppMesh::VirtualRouter](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-appmesh-virtualrouter.html)  |  `MeshName`  |  The name of the service mesh that the virtual router resides in\.  | 
|  [AWS::AppMesh::VirtualRouter](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-appmesh-virtualrouter.html)  |  `Uid`  |  The unique identifier for the virtual router\.  | 
|  [AWS::AppMesh::VirtualRouter](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-appmesh-virtualrouter.html)  |  `VirtualRouterName`  |  The name of the virtual router\.  | 
|  [AWS::AppMesh::VirtualService](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-appmesh-virtualservice.html)  |  `Arn`  |  The full Amazon Resource Name \(ARN\) for the virtual service\.  | 
|  [AWS::AppMesh::VirtualService](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-appmesh-virtualservice.html)  |  `MeshName`  |  The name of the service mesh that the virtual service resides in\.  | 
|  [AWS::AppMesh::VirtualService](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-appmesh-virtualservice.html)  |  `Uid`  |  The unique identifier for the virtual service\.  | 
|  [AWS::AppMesh::VirtualService](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-appmesh-virtualservice.html)  |  `VirtualServiceName`  |  The name of the virtual service\.  | 
|  [AWS::AppStream::ImageBuilder](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-appstream-imagebuilder.html)  |  `StreamingUrl`  |  The URL to start an Amazon AppStream 2\.0 image builder streaming session  | 
|  [AWS::Cloud9::EnvironmentEC2](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-cloud9-environmentec2.html)  |  `Arn`  |  The Amazon Resource Name \(ARN\) of the AWS Cloud9 development environment\. Example: `arn:aws:cloud9:us-east-2:123456789012:environment:2bc3642873c342e485f7e0c561234567`  | 
|  [AWS::Backup::BackupPlan](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-backup-backupplan.html)  |  `BackupPlanArn`  |  An Amazon Resource Name \(ARN\) that uniquely identifies a backup plan; for example, arn:aws:backup:us\-east\-1:123456789012:plan:8F81F553\-3A74\-4A3F\-B93D\-B3360DC80C50\.   | 
|  [AWS::Backup::BackupPlan](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-backup-backupplan.html)  |  `BackupPlanId`  |  Uniquely identifies a backup plan\.  | 
|  [AWS::Backup::BackupPlan](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-backup-backupplan.html)  |  `VersionId`  |  Unique, randomly generated, Unicode, UTF\-8 encoded strings that are at most 1,024 bytes long\. Version Ids cannot be edited\.   | 
|  [AWS::Backup::BackupSelection](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-backup-backupselection.html)  |  `BackupPlanId`  |  Uniquely identifies a backup plan\.  | 
|  [AWS::Backup::BackupSelection](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-backup-backupselection.html)  |  `SelectionId`  |  Uniquely identifies a request to assign a set of resources to a backup plan\.  | 
|  [AWS::Backup::BackupVault](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-backup-backupvault.html)  |  `BackupVaultArn`  |  An Amazon Resource Name \(ARN\) that uniquely identifies a backup vault; for example, arn:aws:backup:us\-east\-1:123456789012:vault:aBackupVault\.  | 
|  [AWS::Backup::BackupVault](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-backup-backupvault.html)  |  `BackupVaultName`  |  The name of a logical container where backups are stored\. Backup vaults are identified by names that are unique to the account used to create them and the Region where they are created\. They consist of lowercase letters, numbers, and hyphens\.  | 
|  [AWS::Cloud9::EnvironmentEC2](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-cloud9-environmentec2.html)  |  `Name`  |  The name of the AWS Cloud9 development environment\. Example: `my-demo-environment`  | 
|  [AWS::CloudFormation::WaitCondition](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-waitcondition.html)  |  `Data`  |  A JSON\-format string containing the `UniqueId` and `Data` values from the wait condition signal\(s\) for the specified wait condition\. For more information about wait condition signals, see [Wait Condition Signal JSON Format](using-cfn-waitcondition.md#using-cfn-waitcondition-signaljson)\. Example of a wait condition with two signals: <pre>{"Signal1":"Step 1 complete.","Signal2":"Step 2 complete."}</pre>  | 
|  [AWS::CloudFormation::Stack](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-stack.html)  |  `Outputs.NestedStackOutputName`  |  The output value from the nested stack that you specified, where *NestedStackOutputName* is the name of the output value\.  | 
|  [AWS::CloudFront::Distribution](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-cloudfront-distribution.html)  |  `DomainName`  |  Example: `d2fadu0nynjpfn.cloudfront.net`  | 
|  [AWS::CloudFront::CloudFrontOriginAccessIdentity](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-cloudfront-cloudfrontoriginaccessidentity.html)  |  `S3CanonicalUserId`  |  Example: `b970b42360b81c8ddbd79d2f5df0069ba9033c8a79655752abe380cd6d63ba8bcf23384d568fcf89fc49700b5e11a0fd`  | 
|  [AWS::CloudTrail::Trail](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-cloudtrail-trail.html)  |  `Arn`  |  Example: `arn:aws:cloudtrail:us-east-2:123456789012:trail/myCloudTrail`  | 
|  [AWS::CloudTrail::Trail](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-cloudtrail-trail.html)  |  `SnsTopicArn`  |  The Amazon Resource Name \(ARN\) of the Amazon SNS topic that is associated with the CloudTrail trail\. Example: `arn:aws:sns:us-east-2:123456789012:mySNSTopic`  | 
|  [AWS::CloudWatch::Alarm](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-cw-alarm.html)  |  `Arn`  |  Example: `arn:aws:cloudwatch:us-east-2:123456789012:alarm:myCloudWatchAlarm-CPUAlarm-UXMMZK36R55Z`  | 
|  [AWS::CodeBuild::Project](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-codebuild-project.html)  |  `Arn`  |  Example: `arn:aws:codebuild:us-west-2:123456789012:project/myProjectName`  | 
|  [AWS::CodeCommit::Repository](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-codecommit-repository.html)  |  `Arn`  |  Example: `arn:aws:codecommit:``us-east-2``:123456789012:MyDemoRepo`  | 
|  [AWS::CodeCommit::Repository](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-codecommit-repository.html)  |  `CloneUrlHttp`  |  Example: `https://codecommit.``us-east-2``.amazonaws.com/v1/repos/MyDemoRepo`  | 
|  [AWS::CodeCommit::Repository](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-codecommit-repository.html)  |  `CloneUrlSsh`  |  Example: `ssh://git-codecommit.``us-east-2``.amazonaws.com/v1/repos//v1/repos/MyDemoRepo`  | 
|  [AWS::CodeCommit::Repository](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-codecommit-repository.html)  |  `Name`  |  Example: `MyDemoRepo`  | 
|  [AWS::CodePipeline::Pipeline](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-codepipeline-pipeline.html)  |  `Version`  |  The pipeline version\. Example: `1`   | 
|  [AWS::CodePipeline::Webhook](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-codepipeline-webhook.html)  |  `Url`  |  Example: `https://eu-central-1.webhooks.aws/trigger123456`   | 
|  [AWS::Config::ConfigRule](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-config-configrule.html)  |  `Arn`  |  Example: `arn:aws:config:``us-east-2``:123456789012:config-rule/config-rule-a1bzhi`  | 
|  [AWS::Config::ConfigRule](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-config-configrule.html)  |  `ConfigRuleId`  |  Example: `config-rule-a1bzhi`  | 
|  [AWS::Config::ConfigRule](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-config-configrule.html)  |  `Compliance.Type`  |  Example: `COMPLIANT`  | 
|  [AWS::DAX::Cluster](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-dax-cluster.html)  |  `Arn`  |  Example: `arn:aws:dax:us-east-1:111122223333:cache/MyDAXCluster`  | 
|  [AWS::DAX::Cluster](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-dax-cluster.html)  |  `ClusterDiscoveryEndpoint`  |  Example: `mydaxcluster.0h3d6x.clustercfg.dax.use1.cache.amazonaws.com:8111`  | 
|  [AWS::DirectoryService::MicrosoftAD](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-directoryservice-microsoftad.html) and [AWS::DirectoryService::SimpleAD](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-directoryservice-simplead.html)  |  `Alias`  |  The alias for a directory\. Examples: `d-12373a053a` or `alias4-mydirectory-12345abcgmzsk` \(if you have the `CreateAlias` property set to true\)  | 
|  [AWS::DirectoryService::MicrosoftAD](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-directoryservice-microsoftad.html) and [AWS::DirectoryService::SimpleAD](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-directoryservice-simplead.html)  |  `DnsIpAddresses`  |  The IP addresses of the DNS servers for the directory\. Example: `[ "192.0.2.1", "192.0.2.2" ]`  | 
|  [AWS::DLM::LifecyclePolicy](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-dlm-lifecyclepolicy.html)  |  `Arn`  |  Example: `arn:aws:dlm:us-west-2:012345678912:policy/policy-0123456789abcdef`  | 
|  [AWS::DocDB::DBCluster](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-docdb-dbcluster.html)  |  `ClusterResourceId`  |  The resource id for the DB cluster\. The cluster ID uniquely identifies the cluster and is used in things like IAM authentication policies\. Example: `cluster-ABCD1234EFGH5678IJKL90MNOP`  | 
|  [AWS::DocDB::DBCluster](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-docdb-dbcluster.html)  |  `Endpoint`  |  The connection endpoint for the DB cluster\. Example: `sample-cluster.cluster-abcdefghijkl.us-east-1.rds.amazonaws.com`  | 
|  [AWS::DocDB::DBCluster](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-docdb-dbcluster.html)  |  `Port`  |  The port number on which the DB cluster accepts connections\. Example: `27017`  | 
|  [AWS::DocDB::DBCluster](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-docdb-dbcluster.html)  |  `ReadEndpoint`  |  The read\-only connection endpoint for the cluster\. Example: `"sample-cluster.cluster-ro-abcdefghijkl.us-east-1.rds.amazonaws.com`  | 
|  [AWS::DocDB::DBInstance](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-docdb-dbinstance.html)  |  `Endpoint`  |  The connection endpoint for the DB instance\. Example: `sample-instance.abcdefghijkl.us-east-1.rds.amazonaws.com`  | 
|  [AWS::DocDB::DBInstance](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-docdb-dbinstance.html)  |  `Port`  |  The port number on which the DB cluster accepts connections\. Example: `27017`  | 
|  [AWS::DynamoDB::Table](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-dynamodb-table.html)  |  `Arn`  |  Example: `arn:aws:dynamodb:us-east-2:123456789012:table/myDynamoDBTable`  | 
|  [AWS::DynamoDB::Table](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-dynamodb-table.html)  |  `StreamArn`  |  The Amazon Resource Name \(ARN\) of the DynamoDB table stream\. To use this attribute, you must specify the DynamoDB table `StreamSpecification` property\. Example: `arn:aws:dynamodb:us-east-2:123456789012:table/testddbstack-myDynamoDBTable-012A1SL7SMP5Q/stream/2015-11-30T20:10:00.000`  | 
|  [AWS::EC2::CapacityReservation](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-capacityreservation.html)  |  `AvailabilityZone`  |  The Availability Zone in which the capacity is reserved\. Example: `us-east-1a`  | 
|  [AWS::EC2::CapacityReservation](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-capacityreservation.html)  |  `AvailableInstanceCount`  |  The remaining capacity, which indicates the number of instances that can be launched in the Capacity Reservation\. Example: `9`  | 
|  [AWS::EC2::CapacityReservation](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-capacityreservation.html)  |  `InstanceType`  |  The type of instance for which the capacity is reserved\. Example: `m4.large`  | 
|  [AWS::EC2::CapacityReservation](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-capacityreservation.html)  |  `Tenancy`  |  The tenancy of the Capacity Reservation\. Example: `dedicated`  | 
|  [AWS::EC2::CapacityReservation](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-capacityreservation.html)  |  `TotalInstanceCount`  |  The total number of instances for which the Capacity Reservation reserves capacity\. Example: `15`  | 
|  [AWS::EC2::EIP](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ec2-eip.html)  |  `AllocationId`  |  The ID that AWS assigns to represent the allocation of the address for use with Amazon VPC\. It is returned only for VPC Elastic IP addresses\. Example: `eipalloc-5723d13e`  | 
|  [AWS::EC2::Instance](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ec2-instance.html)  |  `AvailabilityZone`  |  The Availability Zone where the instance that you specified is launched\. Example: `us-east-1b`  | 
|  [AWS::EC2::Instance](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ec2-instance.html)  |  `PrivateDnsName`  |  The private DNS name of the instance that you specified\. Example: `ip-10-24-34-0.ec2.internal`  | 
|  [AWS::EC2::Instance](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ec2-instance.html)  |  `PublicDnsName`  |  The public DNS name of the instance that you specified\. Example: `ec2-107-20-50-45.compute-1.amazonaws.com`  | 
|  [AWS::EC2::Instance](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ec2-instance.html)  |  `PrivateIp`  |  The private IP address of the instance that you specified\. Example: `10.24.34.0`  | 
|  [AWS::EC2::Instance](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ec2-instance.html)  |  `PublicIp`  |  The public IP address of the instance that you specified\. Example: `192.0.2.0`  | 
|  [AWS::EC2::NetworkInterface](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-network-interface.html)  |  `PrimaryPrivateIpAddress`  |  The primary private IP address of the network interface that you specified\. Example: `10.0.0.192`  | 
|  [AWS::EC2::NetworkInterface](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-network-interface.html)  |  `SecondaryPrivateIpAddresses`  |  The secondary private IP addresses of the network interface that you specified\. Example: `["10.0.0.161", "10.0.0.162", "10.0.0.163"]`  | 
|  [AWS::EC2::SecurityGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ec2-security-group.html)  |  `GroupId`  |  The group ID of the specified security group\. Example: `sg-94b3a1f6`  | 
|  [AWS::EC2::SecurityGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ec2-security-group.html)  |  `VpcId`  |  The ID of the VPC\. Example: `vpc-3325caf2`  | 
|  [AWS::EC2::Subnet](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-subnet.html)  |  `AvailabilityZone`  |  The Availability Zone of the subnet\. Example: `us-east-1a`  | 
|  [AWS::EC2::Subnet](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-subnet.html)  |  `Ipv6CidrBlocks`  |  A list of IPv6 CIDR blocks that are associated with the subnet\. Example: `[ 2001:db8:1234:1a00::/64 ]`  | 
|  [AWS::EC2::Subnet](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-subnet.html)  |  `NetworkAclAssociationId`  |  The ID of the network ACL that is associated with the subnet's VPC\. Example: `acl-5fb85d36`  | 
|  [AWS::EC2::Subnet](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-subnet.html)  |  `VpcId`  |  The ID of the subnet's VPC\. Example: `vpc-11ad4878`  | 
|  [AWS::EC2::SubnetNetworkAclAssociation](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-subnet-network-acl-assoc.html)  |  `AssociationId`  |  The `NetworkAcl associationId` that is attached to a subnet\.  | 
|  [AWS::EC2::VPC](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-vpc.html)  |  `CidrBlock`  |  The set of IP addresses for the VPC\. Example: `10.0.0.0/16`  | 
|  [AWS::EC2::VPC](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-vpc.html)  |  `CidrBlockAssociations`  |  A list of IPv4 CIDR block association IDs for the VPC\. Example: `[ vpc-cidr-assoc-0280ab6b ]`  | 
|  [AWS::EC2::VPC](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-vpc.html)  |  `DefaultNetworkAcl`  |  The default network ACL ID that is associated with the VPC, which AWS creates when you create a VPC\. Example: `acl-814dafe3`  | 
|  [AWS::EC2::VPC](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-vpc.html)  |  `DefaultSecurityGroup`  |  The default security group ID that is associated with the VPC, which AWS creates when you create a VPC\. Example: `sg-b178e0d3`  | 
|  [AWS::EC2::VPC](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-vpc.html)  |  `Ipv6CidrBlocks`  |  A list of IPv6 CIDR blocks that are associated with the VPC\. Example: `[ 2001:db8:1234:1a00::/56 ]`  | 
|  [AWS::ECR::Repository](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ecr-repository.html)  |  `Arn`  |  Example: `arn:aws:ecr:us-east-2:123456789012:repository/test-repository`  | 
|  [AWS::ECS::Cluster](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ecs-cluster.html)  |  `Arn`  |  Example: `arn:aws:ecs:us-east-2:123456789012:cluster/MyECSCluster`  | 
|  [AWS::ECS::Service](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ecs-service.html)  |  `Name`  |  The name of an Amazon Elastic Container Service service\. Example: `sample-webapp`  | 
|  [AWS::EKS::Cluster](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-eks-cluster.html)  |  `Arn`  |  The ARN of the cluster\. Example: `arn:aws:eks:us-east-2:123456789012:cluster/MyECSCluster`  | 
|  [AWS::EKS::Cluster](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-eks-cluster.html)  |  `CertificateAuthorityData`  |  The `certificate-authority-data` for your cluster\.   | 
|  [AWS::EKS::Cluster](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-eks-cluster.html)  |  `Endpoint`  |  The endpoint for your Kubernetes API server\. Example: `https://EXAMPLEFBBB3BA591B746AFC5AB30262.yl4.us-west-2.eks.amazonaws.com`  | 
|  [AWS::ElastiCache::CacheCluster](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-elasticache-cache-cluster.html)  |  `ConfigurationEndpoint.Address`  |  The DNS address of the configuration endpoint for the Memcached cache cluster\. Example: `test.abc12a.cfg.use1.cache.amazonaws.com:11111`  | 
|  [AWS::ElastiCache::CacheCluster](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-elasticache-cache-cluster.html)  |  `ConfigurationEndpoint.Port`  |  The port number of the configuration endpoint for the Memcached cache cluster\.  | 
|  [AWS::ElastiCache::CacheCluster](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-elasticache-cache-cluster.html)  |  `RedisEndpoint.Address`  |  The DNS address of the configuration endpoint for the Redis cache cluster\. Example: `test.abc12a.cfg.use1.cache.amazonaws.com:11111`  | 
|  [AWS::ElastiCache::CacheCluster](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-elasticache-cache-cluster.html)  |  `RedisEndpoint.Port`  |  The port number of the configuration endpoint for the Redis cache cluster\.  | 
|  [AWS::ElastiCache::ReplicationGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-elasticache-replicationgroup.html)  |  `ConfigurationEndPoint.Address`  |  The DNS hostname of the cache node\.  | 
|  [AWS::ElastiCache::ReplicationGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-elasticache-replicationgroup.html)  |  `ConfigurationEndPoint.Port`  |  The port number that the cache engine is listening on\.  | 
|  [AWS::ElastiCache::ReplicationGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-elasticache-replicationgroup.html)  |  `PrimaryEndPoint.Address`  |  The DNS address of the primary read\-write cache node\.  | 
|  [AWS::ElastiCache::ReplicationGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-elasticache-replicationgroup.html)  |  `PrimaryEndPoint.Port`  |  The port number that the primary read\-write cache engine is listening on\.  | 
|  [AWS::ElastiCache::ReplicationGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-elasticache-replicationgroup.html)  |  `ReadEndPoint.Addresses`  |  A string with a list of endpoints for the read\-only replicas\. The order of the addresses maps to the order of the ports from the `ReadEndPoint.Ports` attribute\. Example: `"[abc12xmy3d1w3hv6-001.rep12a.0001.use1.cache.amazonaws.com, abc12xmy3d1w3hv6-002.rep12a.0001.use1.cache.amazonaws.com, abc12xmy3d1w3hv6-003.rep12a.0001.use1.cache.amazonaws.com]"`  | 
|  [AWS::ElastiCache::ReplicationGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-elasticache-replicationgroup.html)  |  `ReadEndPoint.Ports`  |  A string with a list of ports for the read\-only replicas\. The order of the ports maps to the order of the addresses from the `ReadEndPoint.Addresses` attribute\. Example: `"[6379, 6379, 6379]"`  | 
|  [AWS::ElastiCache::ReplicationGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-elasticache-replicationgroup.html)  |  `ReadEndPoint.Addresses.List`  |  A list of endpoints for the read\-only replicas\. Example: `["abc12xmy3d1w3hv6-001.rep12a.0001.use1.cache.amazonaws.com", "abc12xmy3d1w3hv6-002.rep12a.0001.use1.cache.amazonaws.com", "abc12xmy3d1w3hv6-003.rep12a.0001.use1.cache.amazonaws.com"]`  | 
|  [AWS::ElastiCache::ReplicationGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-elasticache-replicationgroup.html)  |  `ReadEndPoint.Ports.List`  |  A list of ports for the read\-only replicas\. Example: `["6379","6379","6379"]`  | 
|  [AWS::ElasticBeanstalk::Environment](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-beanstalk-environment.html)  |  `EndpointURL`  |  The URL to the load balancer for this environment\. Example: `awseb-myst-myen-132MQC4KRLAMD-1371280482.``us-east-2``.elb.amazonaws.com`  | 
|  [AWS::ElasticLoadBalancing::LoadBalancer](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ec2-elb.html)  |  `CanonicalHostedZoneName`  |  The name of the Route 53\-hosted zone that is associated with the load balancer\. Example: `mystack-myelb-15HMABG9ZCN57-1013119603.``us-east-2``.elb.amazonaws.com`  | 
|  [AWS::ElasticLoadBalancing::LoadBalancer](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ec2-elb.html)  |  `CanonicalHostedZoneNameID`  |  The ID of the Route 53 hosted zone name that is associated with the l oad balancer\. Example: `Z3DZXE0Q79N41H`  | 
|  [AWS::ElasticLoadBalancing::LoadBalancer](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ec2-elb.html)  |  `DNSName`  |  The DNS name for the load balancer\. Example: `mystack-myelb-15HMABG9ZCN57-1013119603.``us-east-2``.elb.amazonaws.com`  | 
|  [AWS::ElasticLoadBalancing::LoadBalancer](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ec2-elb.html)  |  `SourceSecurityGroup.GroupName`  |  The security group that you can use as part of your inbound rules for your load balancer's back\-end Amazon EC2 application instances\. Example: `amazon-elb`  | 
|  [AWS::ElasticLoadBalancing::LoadBalancer](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ec2-elb.html)  |  `SourceSecurityGroup.OwnerAlias`  |  The owner of the source security group\. Example: `amazon-elb-sg`  | 
|  [AWS::ElasticLoadBalancingV2::LoadBalancer](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-elasticloadbalancingv2-loadbalancer.html)  |  `DNSName`  |  The DNS name for the application load balancer\. Example: `my-load-balancer-424835706.us-west-2.elb.amazonaws.com`  | 
|  [AWS::ElasticLoadBalancingV2::LoadBalancer](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-elasticloadbalancingv2-loadbalancer.html)  |  `CanonicalHostedZoneID`  |  The ID of the Amazon Route 53\-hosted zone name that is associated with the load balancer\. Example: `Z2P70J7EXAMPLE`  | 
|  [AWS::ElasticLoadBalancingV2::LoadBalancer](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-elasticloadbalancingv2-loadbalancer.html)  |  `LoadBalancerFullName`  |  The full name of the application load balancer\. Example: `app/my-load-balancer/50dc6c495c0c9188`  | 
|  [AWS::ElasticLoadBalancingV2::LoadBalancer](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-elasticloadbalancingv2-loadbalancer.html)  |  `LoadBalancerName`  |  The name of the application load balancer\. Example: `my-load-balancer`  | 
|  [AWS::ElasticLoadBalancingV2::LoadBalancer](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-elasticloadbalancingv2-loadbalancer.html)  |  `SecurityGroups`  |  The IDs of the security groups for the application load balancer\. Example: `sg-123456a`  | 
|  [AWS::ElasticLoadBalancingV2::TargetGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-elasticloadbalancingv2-targetgroup.html)  |  `LoadBalancerArns`  |  The Amazon Resource Names \(ARNs\) of the load balancers that route traffic to this target group\. Example: `[ "arn:aws:elasticloadbalancing:us-west-2:123456789012:loadbalancer/app/my-load-balancer/50dc6c495c0c9188" ]`  | 
|  [AWS::ElasticLoadBalancingV2::TargetGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-elasticloadbalancingv2-targetgroup.html)  |  `TargetGroupFullName`  | The full name of the target group\.Example: `targetgroup/my-target-group/cbf133c568e0d028` | 
|  [AWS::ElasticLoadBalancingV2::TargetGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-elasticloadbalancingv2-targetgroup.html)  |  `TargetGroupName`  | The name of the target group\.Example: `my-target-group` | 
|  [AWS::Elasticsearch::Domain](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-elasticsearch-domain.html)  |  `DomainArn`  |  The Amazon Resource Name \(ARN\) of the domain\. Example: `arn:aws:es:us-west-2:123456789012:domain/mystack-elasti-1ab2cdefghij`  | 
|  [AWS::Elasticsearch::Domain](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-elasticsearch-domain.html)  |  `DomainEndpoint`  |  The domain\-specific endpoint that is used to submit index, search, and data upload requests to an Amazon Elasticsearch Service domain\. Example: `search-mystack-elasti-1ab2cdefghij-ab1c2deckoyb3hofw7wpqa3cm.us-west-2.es.amazonaws.com`  | 
|  [AWS::EMR::Cluster](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-emr-cluster.html)  |  `MasterPublicDNS`  |  The public DNS name of the master node \(instance\)\. Example: `ec2-12-123-123-123.us-west-2.compute.amazonaws.com`  | 
|  [AWS::Events::Rule](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-events-rule.html)  |  `Arn`  |  Example: `arn:aws:events:``us-east-2``:123456789012:rule/example`  | 
|  [AWS::Greengrass::ConnectorDefinition](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-greengrass-connectordefinition.html)  |  `Arn`  |  The ARN of the `ConnectorDefinition`\. Example: `arn:aws:greengrass:us-east-1:123456789012:/greengrass/definition/connectors/1234a5b6-78cd-901e-2fgh-3i45j6k178l9`  | 
|  [AWS::Greengrass::ConnectorDefinition](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-greengrass-connectordefinition.html)  |  `Id`  |  The ID of the `ConnectorDefinition`\. Example: `1234a5b6-78cd-901e-2fgh-3i45j6k178l9`  | 
|  [AWS::Greengrass::ConnectorDefinition](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-greengrass-connectordefinition.html)  |  `LatestVersionArn`  |  The ARN of the most recent `ConnectorDefinitionVersion` that was added to the `ConnectorDefinition`\. Example: `arn:aws:greengrass:us-east-1:123456789012:/greengrass/definition/connectors/1234a5b6-78cd-901e-2fgh-3i45j6k178l9/versions/9876ac30-4bdb-4f9d-95af-b5fdb66be1a2`  | 
|  [AWS::Greengrass::ConnectorDefinition](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-greengrass-connectordefinition.html)  |  `Name`  |  The name of the `ConnectorDefinition`\. Example: `MyConnectorDefinition`  | 
|  [AWS::Greengrass::CoreDefinition](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-greengrass-coredefinition.html)  |  `Arn`  |  The ARN of the `CoreDefinition`\. Example: `arn:aws:greengrass:us-east-1:123456789012:/greengrass/definition/cores/1234a5b6-78cd-901e-2fgh-3i45j6k178l9`  | 
|  [AWS::Greengrass::CoreDefinition](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-greengrass-coredefinition.html)  |  `Id`  |  The ID of the `CoreDefinition`\. Example: `1234a5b6-78cd-901e-2fgh-3i45j6k178l9`  | 
|  [AWS::Greengrass::CoreDefinition](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-greengrass-coredefinition.html)  |  `LatestVersionArn`  |  The ARN of the most recent `CoreDefinitionVersion` that was added to the `CoreDefinition`\. Example: `arn:aws:greengrass:us-east-1:123456789012:/greengrass/definition/cores/1234a5b6-78cd-901e-2fgh-3i45j6k178l9/versions/9876ac30-4bdb-4f9d-95af-b5fdb66be1a2`  | 
|  [AWS::Greengrass::CoreDefinition](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-greengrass-coredefinition.html)  |  `Name`  |  The name of the `CoreDefinition`\. Example: `MyCoreDefinition`  | 
|  [AWS::Greengrass::DeviceDefinition](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-greengrass-devicedefinition.html)  |  `Arn`  |  The ARN of the `DeviceDefinition`\. Example: `arn:aws:greengrass:us-east-1:123456789012:/greengrass/definition/devices/1234a5b6-78cd-901e-2fgh-3i45j6k178l9`  | 
|  [AWS::Greengrass::DeviceDefinition](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-greengrass-devicedefinition.html)  |  `Id`  |  The ID of the `DeviceDefinition`\. Example: `1234a5b6-78cd-901e-2fgh-3i45j6k178l9`  | 
|  [AWS::Greengrass::DeviceDefinition](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-greengrass-devicedefinition.html)  |  `LatestVersionArn`  |  The ARN of the most recent `DeviceDefinitionVersion` that was added to the `DeviceDefinition`\. Example: `arn:aws:greengrass:us-east-1:123456789012:/greengrass/definition/devices/1234a5b6-78cd-901e-2fgh-3i45j6k178l9/versions/9876ac30-4bdb-4f9d-95af-b5fdb66be1a2`  | 
|  [AWS::Greengrass::DeviceDefinition](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-greengrass-devicedefinition.html)  |  `Name`  |  The name of the `DeviceDefinition`\. Example: `MyDeviceDefinition`  | 
|  [AWS::Greengrass::FunctionDefinition](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-greengrass-functiondefinition.html)  |  ID  |  The ID of the `FunctionDefinition`\. Example: `1234a5b6-78cd-901e-2fgh-3i45j6k178l9`  | 
|  [AWS::Greengrass::FunctionDefinitionVersion](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-greengrass-functiondefinitionversion.html)  |  ARN  |  The ARN of the `FunctionDefinition`\. Example: `arn:aws:greengrass:us-east-1:123456789012:/greengrass/definition/functions/1234a5b6-78cd-901e-2fgh-3i45j6k178l9/versions/9876ac30-4bdb-4f9d-95af-b5fdb66be1a2`  | 
|  [AWS::Greengrass::Group](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-greengrass-group.html)  |  `Arn`  |  The ARN of the `Group`\. Example: `arn:aws:greengrass:us-east-1:123456789012:/greengrass/definition/groups/1234a5b6-78cd-901e-2fgh-3i45j6k178l9`  | 
|  [AWS::Greengrass::Group](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-greengrass-group.html)  |  `Id`  |  The ID of the `Group`\. Example: `1234a5b6-78cd-901e-2fgh-3i45j6k178l9`  | 
|  [AWS::Greengrass::Group](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-greengrass-group.html)  |  `LatestVersionArn`  |  The ARN of the most recent `GroupVersion` that was added to the `Group`\. Example: `arn:aws:greengrass:us-east-1:123456789012:/greengrass/definition/groups/1234a5b6-78cd-901e-2fgh-3i45j6k178l9/versions/9876ac30-4bdb-4f9d-95af-b5fdb66be1a2`  | 
|  [AWS::Greengrass::Group](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-greengrass-group.html)  |  `Name`  |  The name of the `Group`\. Example: `Mygroup`  | 
|  [AWS::Greengrass::Group](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-greengrass-group.html)  |  `RoleArn`  |  The ARN of the IAM role attached to the `Group`\. >Example: `arn:aws:iam::123456789012:role/role-name`  | 
|  [AWS::Greengrass::Group](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-greengrass-group.html)  |  `RoleAttachedAt`  |  The time \(in milliseconds since the epoch\) when the group role was associated with the `Group`\.  | 
|  [AWS::Greengrass::LoggerDefinition](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-greengrass-loggerdefinition.html)  |  `Arn`  |  The ARN of the `LoggerDefinition`\. Example: `arn:aws:greengrass:us-east-1:123456789012:/greengrass/definition/loggers/1234a5b6-78cd-901e-2fgh-3i45j6k178l9`  | 
|  [AWS::Greengrass::LoggerDefinition](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-greengrass-loggerdefinition.html)  |  `Id`  |  The ID of the `LoggerDefinition`\. Example: `1234a5b6-78cd-901e-2fgh-3i45j6k178l9`  | 
|  [AWS::Greengrass::LoggerDefinition](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-greengrass-loggerdefinition.html)  |  `LatestVersionArn`  |  The ARN of the most recent `LoggerDefinitionVersion` that was added to the `LoggerDefinition`\. Example: `arn:aws:greengrass:us-east-1:123456789012:/greengrass/definition/loggers/1234a5b6-78cd-901e-2fgh-3i45j6k178l9/versions/9876ac30-4bdb-4f9d-95af-b5fdb66be1a2`  | 
|  [AWS::Greengrass::LoggerDefinition](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-greengrass-loggerdefinition.html)  |  `Name`  |  The name of the `LoggerDefinition`\. Example: `MyLoggerDefinition`  | 
|  [AWS::Greengrass::ResourceDefinition](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-greengrass-resourcedefinition.html)  |  `Arn`  |  The ARN of the `ResourceDefinition`\. Example: `arn:aws:greengrass:us-east-1:123456789012:/greengrass/definition/resources/1234a5b6-78cd-901e-2fgh-3i45j6k178l9`  | 
|  [AWS::Greengrass::ResourceDefinition](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-greengrass-resourcedefinition.html)  |  `Id`  |  The ID of the `ResourceDefinition`\. Example: `1234a5b6-78cd-901e-2fgh-3i45j6k178l9`  | 
|  [AWS::Greengrass::ResourceDefinition](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-greengrass-resourcedefinition.html)  |  `LatestVersionArn`  |  The ARN of the most recent `ResourceDefinitionVersion` that was added to the `ResourceDefinition`\. Example: `arn:aws:greengrass:us-east-1:123456789012:/greengrass/definition/resources/1234a5b6-78cd-901e-2fgh-3i45j6k178l9/versions/9876ac30-4bdb-4f9d-95af-b5fdb66be1a2`  | 
|  [AWS::Greengrass::ResourceDefinition](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-greengrass-resourcedefinition.html)  |  `Name`  |  The name of the `ResourceDefinition`\. Example: `MyResourceDefinition`  | 
|  [AWS::Greengrass::SubscriptionDefinition](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-greengrass-subscriptiondefinition.html)  |  `Arn`  |  The ARN of the `SubscriptionDefinition`\. Example: `arn:aws:greengrass:us-east-1:123456789012:/greengrass/definition/subscriptions/1234a5b6-78cd-901e-2fgh-3i45j6k178l9`  | 
|  [AWS::Greengrass::SubscriptionDefinition](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-greengrass-subscriptiondefinition.html)  |  `Id`  |  The ID of the `SubscriptionDefinition`\. Example: `1234a5b6-78cd-901e-2fgh-3i45j6k178l9`  | 
|  [AWS::Greengrass::SubscriptionDefinition](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-greengrass-subscriptiondefinition.html)  |  `LatestVersionArn`  |  The ARN of the most recent `SubscriptionDefinitionVersion` that was added to the `SubscriptionDefinition`\. Example: `arn:aws:greengrass:us-east-1:123456789012:/greengrass/definition/subscriptions/1234a5b6-78cd-901e-2fgh-3i45j6k178l9/versions/9876ac30-4bdb-4f9d-95af-b5fdb66be1a2`  | 
|  [AWS::Greengrass::SubscriptionDefinition](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-greengrass-subscriptiondefinition.html)  |  `Name`  |  The name of the `SubscriptionDefinition`\. Example: `MySubscriptionDefinition`  | 
|  [AWS::IAM::AccessKey](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-iam-accesskey.html)  |  `SecretAccessKey`  |  The secret access key for the specified `Access Key`\. Example: `wJalrXUtnFEMI/K7MDENG/bPxRfiCYzEXAMPLEKEY`  | 
|  [AWS::IAM::Group](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-iam-group.html)  |  `Arn`  |  Example: `arn:aws:iam::123456789012:group/mystack-mygroup-1DZETITOWEKVO`  | 
|  [AWS::IAM::InstanceProfile](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-iam-instanceprofile.html)  |  `Arn`  |  Example: `arn:aws:iam::1234567890:instance-profile/MyProfile-ASDNSDLKJ`  | 
|  [AWS::IAM::Role](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-iam-role.html)  |  `Arn`  |  Example: `arn:aws:iam::1234567890:role/MyRole-AJJHDSKSDF`  | 
|  [AWS::IAM::User](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-iam-user.html)  |  `Arn`  |  Example: `arn:aws:iam::123456789012:user/mystack-myuser-1CCXAFG2H2U4D`  | 
|  [AWS::IoT::Certificate](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-iot-certificate.html)  | Arn | Example: arn:aws:iot:ap\-southeast\-2:123456789012:cert/a1234567b89c012d3e4fg567hij8k9l01mno1p23q45678901rs234567890t1u2 | 
|  [AWS::IoT::Policy](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-iot-policy.html)  |  `Arn`  |  Example: `arn:aws:iot:us-east-2:123456789012:policy/MyIoTPolicy`  | 
|  [AWS::IoT::TopicRule](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-iot-topicrule.html)  |  `Arn`  |  Example: `arn:aws:iot:us-east-2:123456789012:rule/MyIoTRule`  | 
|  [AWS::IoT1Click::Device](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-iot1click-device.html)  |  `Arn`  |  The ARN of the AWS IoT 1\-Click compatible device\. Example: `arn:aws:iot1click:us-west-2:123456789012:devices/G030PX0312744DWM`  | 
|  [AWS::IoT1Click::Device](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-iot1click-device.html)  |  `DeviceId`  |  The user specified device ID\. Example: `G030PX0312744DWM`  | 
|  [AWS::IoT1Click::Device](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-iot1click-device.html)  |  `Enabled`  |  A Boolean value indicating if the device is enabled \(`true`\) or disabled \(`false`\)\. Example: `true`  | 
|  [AWS::IoT1Click::Placement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-iot1click-placement.html)  |  `PlacementName`  |  The placement name associated with a project\. Example: `region27`  | 
|  [AWS::IoT1Click::Placement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-iot1click-placement.html)  |  `ProjectName`  |  The name of the project for a given placement\. Example: `seattle-region`  | 
|  [AWS::IoT1Click::Project](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-iot1click-project.html)  |  `ProjectName`  |  The name of the project\. Example: `seattle-region`  | 
|  [AWS::IoT1Click::Project](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-iot1click-project.html)  |  `Arn`  |  The ARN of the project\. Example: `arn:aws:iot1click:us-east-1:123456789012:projects/seattle-region`  | 
|  [AWS::Kinesis::Stream](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-kinesis-stream.html)  |  `Arn`  |  Example: `arn:aws:kinesis:``us-east-2``:123456789012:stream/stream-name`  | 
|  [AWS::Kinesis::StreamConsumer](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-kinesis-streamconsumer.html)  |  `ConsumerARN`  |  Example: `arn:aws:kinesis:us-east-1:123456789012:stream/stream-name/consumer/consumer-name:1234567890`  | 
|  [AWS::Kinesis::StreamConsumer](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-kinesis-streamconsumer.html)  |  `ConsumerCreationTimestamp`  |  Example: `2018-10-31T17:35:57.650Z`  | 
|  [AWS::Kinesis::StreamConsumer](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-kinesis-streamconsumer.html)  |  `ConsumerName`  |  Example: `example-consumer-name`  | 
|  [AWS::Kinesis::StreamConsumer](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-kinesis-streamconsumer.html)  |  `ConsumerStatus`  |  Example: `CREATING`  | 
|  [AWS::Kinesis::StreamConsumer](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-kinesis-streamconsumer.html)  |  `StreamARN`  |  Example: `arn:aws:kinesis:us-east-2:123456789012:stream/stream-name`  | 
|  [AWS::KinesisFirehose::DeliveryStream](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-kinesisfirehose-deliverystream.html)  |  `Arn`  |  Example: `arn:aws:firehose:``us-east-2``:123456789012:deliverystream/delivery-stream-name`  | 
|  [AWS::KMS::Key](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-kms-key.html)  |  `Arn`  |  Example: `arn:aws:kms:us-west-2:123456789012:key/12a34567-8c90-1defg-af84-0bf06c1747f3`  | 
|  [AWS::Lambda::Function](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-lambda-function.html)  |  `Arn`  |  Example: `arn:aws:lambda:us-west-2:123456789012:MyStack-AMILookUp-NT5EUXTNTXXD`  | 
|  [AWS::Lambda::Version](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-lambda-version.html)  |  `Version`  |  The version of a Lambda function\. Example: `1`  | 
|  [AWS::Logs::Destination](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-logs-destination.html)  |  `Arn`  |  Example: `arn:aws:logs:us-east-2:123456789012:destination:MyDestination`  | 
|  [AWS::Logs::LogGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-logs-loggroup.html)  |  `Arn`  |  Example: `arn:aws:logs:``us-east-2``:123456789012:log-group:/mystack-testgroup-12ABC1AB12A1:*`  | 
|  [AWS::MediaStore::Container](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-mediastore-container.html)  |  `Endpoint`  |   | 
|  [AWS::OpsWorks::Instance](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-opsworks-instance.html)  |  `AvailabilityZone`  |  The Availability Zone of an AWS OpsWorks instance\. Example: `us-east-2a`\.  | 
|  [AWS::OpsWorks::Instance](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-opsworks-instance.html)  |  `PrivateDnsName`  |  The private DNS name of an AWS OpsWorks instance\.  | 
|  [AWS::OpsWorks::Instance](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-opsworks-instance.html)  |  `PrivateIp`  |  The private IP address of an AWS OpsWorks instance\.  | 
|  [AWS::OpsWorks::Instance](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-opsworks-instance.html)  |  `PublicDnsName`  |  The public DNS name of an AWS OpsWorks instance\.  | 
|  [AWS::OpsWorks::Instance](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-opsworks-instance.html)  |  `PublicIp`  |  The public IP address of an AWS OpsWorks instance\.  To use this attribute, the AWS OpsWorks instance must be in an AWS OpsWorks layer that auto\-assigns public IP addresses\.  Example: `192.0.2.0`  | 
|  [AWS::OpsWorks::UserProfile](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-opsworks-userprofile.html)  |  `SshUserName`  |  The SSH user name of an AWS OpsWorks instance\.  | 
|  [AWS::OpsWorksCM::Server](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-opsworkscm-server.html)  |  `Arn`  |  Example: `arn:aws:OpsWorksCM:us-east-1:123456789012:server/server-a1bzhi`  | 
|  [AWS::OpsWorksCM::Server](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-opsworkscm-server.html)  |  `Endpoint`  |  Example: `myserver-asdfghjkl.us-east-1.opsworks.io`  | 
|  [AWS::Pinpoint::Campaign](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-pinpoint-campaign.html)  |  `CampaignId`  |   | 
|  [AWS::Pinpoint::Segment](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-pinpoint-segment.html)  |  `SegmentId`  |   | 
|  [AWS:RAM::ResourceShare](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ram-resourceshare.html)  |  `Arn`  |  The Amazon Resource Name \(ARN\) of the resource share\. Example: `arn:aws:ram:us-east-1:123456789012:resource-share/12345678-1234-1234-1234-12345678`  | 
|  [AWS::Redshift::Cluster](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-redshift-cluster.html)  |  `Endpoint.Address`  |  The connection endpoint for the cluster\. Example: `examplecluster.cg034hpkmmjt.``us-east-2``.redshift.amazonaws.com`  | 
|  [AWS::Redshift::Cluster](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-redshift-cluster.html)  |  `Endpoint.Port`  |  The connection port for the cluster\. Example: `5439`  | 
| [AWS::RDS::DBCluster](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-rds-dbcluster.html) |  `Endpoint.Address`  |  The connection endpoint for the DB cluster\. Example: `mystack-mydbcluster-1apw1j4phylrk.cg034hpkmmjt.``us-east-2``.rds.amazonaws.com`  | 
|  [AWS::RDS::DBCluster](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-rds-dbcluster.html)  |  `Endpoint.Port`  |  The port number on which the DB cluster accepts connections\. Example: `3306`  | 
|  [AWS::RDS::DBCluster](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-rds-dbcluster.html)  |  `ReadEndpoint.Address`  |  The reader endpoint for the DB cluster\. Example: `mystack-mydbcluster-ro-1apw1j4phylrk.cg034hpkmmjt.``us-east-2``.rds.amazonaws.com`  | 
|  [AWS::RDS::DBInstance](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-rds-database-instance.html)  |  `Endpoint.Address`  |  The connection endpoint for the database\. Example: `mystack-mydb-1apw1j4phylrk.cg034hpkmmjt.``us-east-2``.rds.amazonaws.com`  | 
|  [AWS::RDS::DBInstance](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-rds-database-instance.html)  |  `Endpoint.Port`  |  The port number on which the database accepts connections\. Example: `3306`  | 
|  [AWS::RoboMaker::Fleet](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-robomaker-fleet.html)  |  `Arn`  |  The Amazon Resource Name \(ARN\) of the fleet\. Example: `arn:aws:robomaker:us-west-2:123456789012:deployment-fleet/MyFleet/1539894765711`  | 
|  [AWS::RoboMaker::RobotApplication](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-robomaker-robotapplication.html)  |  `Arn`  |  The Amazon Resource Name \(ARN\) of the robot application\. Example: `arn:aws:robomaker:us-west-2:123456789012:robot-application/MyRobotApplication/1546541208251`  | 
|  [AWS::RoboMaker::RobotApplication](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-robomaker-robotapplication.html)  |  `CurrentRevisionId`  |  The current revision ID\. Example: `2`  | 
|  [AWS::RoboMaker::SimulationApplication](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-robomaker-simulationapplication.html)  |  `Arn`  |  The Amazon Resource Name \(ARN\) of the simulation application\. Example: `arn:aws:robo-maker:us-east-1:123456789012:simulation-application/simulation-application-a1bzhi`  | 
|  [AWS::RoboMaker::SimulationApplication](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-robomaker-simulationapplication.html)  |  `CurrentRevisionId`  |  The current revision ID\. Example: `2`  | 
|  [AWS::Route53::HostedZone](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-route53-hostedzone.html)  |  `NameServers`  |  The set of name servers for the specific hosted zone\. Example: `ns1.example.com` This attribute is not supported for private hosted zones\.  | 
|  [AWS::Route53Resolver::ResolverEndpoint](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-route53resolver-resolverendpoint.html)  |  `Arn`  |  The ARN for the inbound or outbound endpoint\. Example: `arn:aws:route53resolver:us-east-2:123456789012:resolver-endpoint/rslvr-out-fdc049932dexample`  | 
|  [AWS::Route53Resolver::ResolverEndpoint](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-route53resolver-resolverendpoint.html)  |  `Direction`  |  Whether this is an inbound or outbound endpoint\. Example: `INBOUND`  | 
|  [AWS::Route53Resolver::ResolverEndpoint](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-route53resolver-resolverendpoint.html)  |  `HostedVPCId`  |  The ID of the VPC that you want to create the resolver endpoint in\. Example: `vpc-0dd415a0edexample`  | 
|  [AWS::Route53Resolver::ResolverEndpoint](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-route53resolver-resolverendpoint.html)  |  `IpAddressCount`  |  The number of IP addresses that the resolver endpoint can use for DNS queries\. Example: `2`  | 
|  [AWS::Route53Resolver::ResolverEndpoint](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-route53resolver-resolverendpoint.html)  |  `Name`  |  The name for the inbound or outbound endpoint\. Example: `MyInboundEndpoint`  | 
|  [AWS::Route53Resolver::ResolverEndpoint](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-route53resolver-resolverendpoint.html)  |  `ResolverEndpointId`  |  The ID that Resolver assigned to the endpoint when you created it\. Example: `rslvr-out-fdc049932dexample`  | 
|  [AWS::Route53Resolver::ResolverRule](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-route53resolver-resolverrule.html)  |  `Arn`  |  The ARN for the rule\. Example: `arn:aws:route53resolver:us-east-2:123456789012:resolver-rule/rslvr-rr-5328a0899aexample`  | 
|  [AWS::Route53Resolver::ResolverRule](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-route53resolver-resolverrule.html)  |  `DomainName`  |  The domain name for outbound DNS queries that you want to forward to DNS resolvers in your network\. Example: `example.com`  | 
|  [AWS::Route53Resolver::ResolverRule](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-route53resolver-resolverrule.html)  |  `ResolverEndpointId`  |  The ID of the endpoint that the rule is associated with\. Example: `rslvr-out-fdc049932dexample`  | 
|  [AWS::Route53Resolver::ResolverRule](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-route53resolver-resolverrule.html)  |  `ResolverRuleId`  |  The ID that Resolver assigned to the rule when you created it\. Example: `rslvr-rr-5328a0899aexample`  | 
|  [AWS::Route53Resolver::ResolverRule](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-route53resolver-resolverrule.html)  |  `TargetIps`  |  The IPv4 IP addresses that you want Resolver to forward DNS queries to\. Example: `192.0.2.44`  | 
|  [AWS::Route53Resolver::ResolverRuleAssociation](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-route53resolver-resolverruleassociation.html)  |  `Name`  |  The name of an association between a resolver rule and a VPC\.  Example: `test.example.com in beta VPC`  | 
|  [AWS::Route53Resolver::ResolverRuleAssociation](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-route53resolver-resolverruleassociation.html)  |  `ResolverRuleAssociationId`  |  The ID of the resolver rule association that you want to get information about\. Example: `rslvr-rrassoc-97242eaf88example`  | 
|  [AWS::Route53Resolver::ResolverRuleAssociation](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-route53resolver-resolverruleassociation.html)  |  `ResolverRuleId`  |  The ID of the resolver rule that you associated with the VPC that is specified by `VPCId`\. Example: `rslvr-rr-5328a0899example`  | 
|  [AWS::Route53Resolver::ResolverRuleAssociation](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-route53resolver-resolverruleassociation.html)  |  `VPCId`  |  The ID of the VPC that you associated the resolver rule with\. Example: `vpc-03cf94c75cexample`  | 
|  [AWS::S3::Bucket](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-s3-bucket.html)  |  `Arn`  |  Example: `arn:aws:s3:::mybucket`  | 
|  [AWS::S3::Bucket](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-s3-bucket.html)  |  `DomainName`  |  The DNS name of the specified bucket\. Example: `mystack-mybucket-kdwwxmddtr2g.s3.amazonaws.com`  | 
|  [AWS::S3::Bucket](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-s3-bucket.html)  |  `DualStackDomainName`  |  The IPv6 DNS name of the specified bucket\. Example: `mystack-mybucket-kdwwxmddtr2g.s3.dualstack.``us-east-2``.amazonaws.com/`  | 
|  [AWS::S3::Bucket](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-s3-bucket.html)  |  `WebsiteURL`  |  The Amazon S3 website endpoint for the specified bucket\. Example: `http://mystack-mybucket-kdwwxmddtr2g.s3-website-``us-east-2``.amazonaws.com/`  | 
|  [AWS::Serverless::Function](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/transform-aws-serverless.html)  |  `Arn`  |  The ARN of an `AWS::Serverless::Function` resource\.  | 
|  [AWS::ServiceDiscovery::HttpNamespace](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-servicediscovery-httpnamespace.html)  |  `Arn`  |  Example: `arn:aws:servicediscovery:us-west-2:1234567890:namespace/ns-d6wz3hq6kexample`  | 
|  [AWS::ServiceDiscovery::HttpNamespace](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-servicediscovery-httpnamespace.html)  |  `Id`  |  Example: `ns-d6wz3hq6kexample`  | 
|  [AWS::ServiceDiscovery::PrivateDnsNamespace](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-servicediscovery-privatednsnamespace.html)  |  `Arn`  |  Example: `arn:aws:servicediscovery:us-west-2:1234567890:namespace/ns-t2kl4fs6xexample`  | 
|  [AWS::ServiceDiscovery::PrivateDnsNamespace](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-servicediscovery-privatednsnamespace.html)  |  `Id`  |  Example: `ns-t2kl4fs6xexample`  | 
|  [AWS::ServiceDiscovery::PublicDnsNamespace](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-servicediscovery-publicdnsnamespace.html)  |  `Arn`  |  Example: `arn:aws:servicediscovery:us-west-2:1234567890:namespace/ns-d6wz3hq6kexample`  | 
|  [AWS::ServiceDiscovery::PublicDnsNamespace](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-servicediscovery-publicdnsnamespace.html)  |  `Id`  |  Example: `ns-d6wz3hq6kexample`  | 
|  [AWS::ServiceDiscovery::Service](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-servicediscovery-service.html)  |  `Arn`  |  Example: `arn:aws:servicediscovery:us-west-2:1234567890:service/srv-7dfj3r6cyexample`  | 
|  [AWS::ServiceDiscovery::Service](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-servicediscovery-service.html)  |  `Id`  |  Example: `srv-7dfj3r6cyexample`  | 
|  [AWS::ServiceDiscovery::Service](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-servicediscovery-service.html)  |  `Name`  |  Example: `example`  | 
| [AWS::SNS::Topic](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-sns-topic.html) | TopicName |  The name of an Amazon SNS topic\. Example: `my-sns-topic`  | 
| [AWS::StepFunctions::Activity](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-stepfunctions-activity.html) | Name | The name of the AWS Step Functions activity\. | 
| [AWS::StepFunctions::StateMachine](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-stepfunctions-statemachine.html) | Name | The name of the Step Functions state machine\. | 
|  [AWS::SQS::Queue](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-sqs-queues.html)  |  `Arn`  |  Example: `arn:aws:sqs:``us-east-2``:123456789012:mystack-myqueue-15PG5C2FC1CW8`  | 
|  [AWS::SQS::Queue](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-sqs-queues.html)  |  `QueueName`  |  The name of an Amazon SQS queue\. Example: `mystack-myqueue-1VF9BKQH5BJVI`  | 
|  [AWS::Transfer::Server](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-transfer-server.html)  |  `Arn`  |  The ARN of the AWS Transfer for SFTP server Example: `arn:aws:transfer:us-east-1:123456789012:server/s-01234567890abcdef`  | 
|  [AWS::Transfer::Server](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-transfer-server.html)  |  `ServerId`  |  The service\-assigned ID of the SFTP server\. Example: `s-01234567890abcdef`  | 
|  [AWS::Transfer::User](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-transfer-user.html)  |  `Arn`  |  The ARN of the AWS Transfer for SFTP user\. Example: `arn:aws:transfer:us-east-1:123456789012:user/user1`  | 
|  [AWS::Transfer::User](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-transfer-user.html)  |  `ServerId`  |  The ID of the SFTP server to which the user is attached\. Example: `s-01234567890abcdef`  | 
|  [AWS::Transfer::User](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-transfer-user.html)  |  `UserName`  |  A unique string that identifies a user account associated with an SFTP server\. Example: `sftp-user-1`  | 