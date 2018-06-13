# `Ref`<a name="intrinsic-function-reference-ref"></a>

The intrinsic function `Ref` returns the value of the specified *parameter* or *resource*\.
+ When you specify a parameter's logical name, it returns the value of the parameter\.
+ When you specify a resource's logical name, it returns a value that you can typically use to refer to that resource, such as a [physical ID](resources-section-structure.md)\.

When you are declaring a resource in a template and you need to specify another template resource by name, you can use the `Ref` to refer to that other resource\. In general, `Ref` returns the name of the resource\. For example, a reference to an [AWS::AutoScaling::AutoScalingGroup](aws-properties-as-group.md) returns the name of that Auto Scaling group resource\.

For some resources, an identifier is returned that has another significant meaning in the context of the resource\. An [AWS::EC2::EIP](aws-properties-ec2-eip.md) resource, for instance, returns the IP address, and an [AWS::EC2::Instance](aws-properties-ec2-instance.md) returns the instance ID\. 

At the bottom of this topic, there is a table that lists the values returned for many common resource types\. More information about `Ref` return values for a particular resource or property can be found in the documentation for that resource or property\.

**Tip**  
You can also use `Ref` to add values to Output messages\.

## Declaration<a name="w3ab2c21c28c68c15"></a>

### JSON<a name="intrinsic-function-reference-ref-syntax.json"></a>

```
{ "Ref" : "logicalName" }
```

### YAML<a name="intrinsic-function-reference-ref-syntax.yaml"></a>

Syntax for the full function name:

```
Ref: logicalName
```

Syntax for the short form:

```
!Ref logicalName
```

## Parameters<a name="w3ab2c21c28c68c17"></a>

logicalName  
The logical name of the resource or parameter you want to dereference\.

## Return Value<a name="w3ab2c21c28c68c19"></a>

The physical ID of the resource or the value of the parameter\.

## Example<a name="w3ab2c21c28c68c21"></a>

The following resource declaration for an Elastic IP address needs the instance ID of an EC2 instance and uses the `Ref` function to specify the instance ID of the MyEC2Instance resource:

### JSON<a name="intrinsic-function-reference-ref-example.json"></a>

```
"MyEIP" : {
   "Type" : "AWS::EC2::EIP",
   "Properties" : {
      "InstanceId" : { "Ref" : "MyEC2Instance" }
   }
}
```

### YAML<a name="intrinsic-function-reference-ref-example.yaml"></a>

```
MyEIP:
  Type: "AWS::EC2::EIP"
  Properties:
    InstanceId: !Ref MyEC2Instance
```

## Supported Functions<a name="w3ab2c21c28c68c23"></a>

You cannot use any functions in the `Ref` function\. You must specify a string that is a resource logical ID\.

## Resource Return Examples<a name="w3ab2c21c28c68c25"></a>

This section lists sample values returned by `Ref` for particular AWS CloudFormation resources\. For more information about `Ref` return values for a particular resource or property, refer to the documentation for that resource or property\.


| Resource Type | Reference Value | Example Return Value | 
| --- | --- | --- | 
|  [AWS::ApiGateway::Account](aws-resource-apigateway-account.md)  |  API Gateway account resource ID  |  `mysta-accou-01234b567890example`  | 
|  [AWS::ApiGateway::ApiKey](aws-resource-apigateway-apikey.md)  |  API key  |  `m2m1k7sybf`  | 
|  [AWS::ApiGateway::Authorizer](aws-resource-apigateway-authorizer.md)  |  Authorizer resource ID  |  `abcde1`  | 
|  [AWS::ApiGateway::ClientCertificate](aws-resource-apigateway-clientcertificate.md)  |  Client certificate name  |  `abc123`  | 
|  [AWS::ApiGateway::Deployment](aws-resource-apigateway-deployment.md)  |  Deployment resource ID  |  `abc123`  | 
|  [AWS::ApiGateway::DomainName](aws-resource-apigateway-domainname.md)  |  Domain name  |  `example.mydomain.com`  | 
|  [AWS::ApiGateway::Method](aws-resource-apigateway-method.md)  |  Method resource ID  |  `mysta-metho-01234b567890example`  | 
|  [AWS::ApiGateway::Model](aws-resource-apigateway-model.md)  |  Model name  |  `myModel`  | 
|  [AWS::ApiGateway::Resource](aws-resource-apigateway-resource.md)  |  API Gateway resource ID  |  `abc123`  | 
|  [AWS::ApiGateway::RestApi](aws-resource-apigateway-restapi.md)  |  Rest API resource ID  |  `a1bcdef2gh`  | 
|  [AWS::ApiGateway::Stage](aws-resource-apigateway-stage.md)   |  Stage name  |  `MyTestStage`  | 
| [AWS::ApplicationAutoScaling::ScalableTarget](aws-resource-applicationautoscaling-scalabletarget.md) |  Scalable Target ID  |  `service/ecsStack-MyECSCluster-AB12CDE3F4GH/ecsStack-MyECSService-AB12CDE3F4GH\|ecs:service:DesiredCount\|ecs`  | 
| [AWS::ApplicationAutoScaling::ScalingPolicy](aws-resource-applicationautoscaling-scalingpolicy.md) |  Application Auto Scaling policy Amazon Resource Name \(ARN\)  | arn:aws:autoscaling:us\-east\-1:123456789012:scalingPolicy:12ab3c4d\-56789\-0ef1\-2345\-6ghi7jk8lm90:resource/ecs/service/ecsStack\-MyECSCluster\-AB12CDE3F4GH/ecsStack\-MyECSService\-AB12CDE3F4GH:policyName/MyStepPolicy | 
|  [AWS::Athena::NamedQuery](aws-resource-athena-namedquery.md)  |  Named query name  |  `abc123`  | 
|  [AWS::AutoScaling::AutoScalingGroup](aws-properties-as-group.md)  |  Name  |  `mystack-myasgroup-NT5EUXTNTXXD`  | 
|  [AWS::AutoScaling::LaunchConfiguration](aws-properties-as-launchconfig.md)  |  Name  |  `mystack-mylaunchconfig-1DDYF1E3B3I`  | 
|  [AWS::AutoScaling::LifecycleHook](aws-resource-as-lifecyclehook.md)  |  Name  |  `mylifecyclehookname`  | 
|  [AWS::AutoScaling::ScalingPolicy](aws-properties-as-policy.md)  |  Scaling policy Amazon Resource Name \(ARN\)  |  `arn:aws:autoscaling:us-east-1:123456789012:scalingPolicy:ab12c4d5-a1b2-a1b2-a1b2-ab12c4d56789:autoScalingGroupName/myStack-AutoScalingGroup-AB12C4D5E6:policyName/myStack-myScalingPolicy-AB12C4D5E6`  | 
|  [AWS::AutoScaling::ScheduledAction](aws-resource-as-scheduledaction.md)  |  Name  |  `mystack-myscheduledaction-NT5EUXTNTXXD`  | 
| [AWS::Batch::ComputeEnvironment](aws-resource-batch-computeenvironment.md) |  AWS Batch Compute Environment Amazon Resource Name \(ARN\)  |  `arn:aws:batch:us-east-1:555555555555:compute-environment/M4OnDemand`  | 
| [AWS::Batch::JobDefinition](aws-resource-batch-jobdefinition.md) |  AWS Batch Job Definition Amazon Resource Name \(ARN\)  |  `arn:aws:batch:us-east-1:111122223333:job-definition/test-gpu:2`  | 
| [AWS::Batch::JobQueue](aws-resource-batch-jobqueue.md) |  AWS Batch Job Queue Amazon Resource Name \(ARN\)  |  `arn:aws:batch:us-east-1:111122223333:job-queue/HighPriority`  | 
| [AWS::CertificateManager::Certificate](aws-resource-certificatemanager-certificate.md) |  Certificate Amazon Resource Name \(ARN\)  |  `arn:aws:acm:us-east-1:123456789012:certificate/12ab3c4d-56789-0ef1-2345-3dab6fa3ee50`  | 
|  [AWS::Cloud9::EnvironmentEC2](aws-resource-cloud9-environmentec2.md)  |  Development environment ID  |  `2bc3642873c342e485f7e0c56example`  | 
|  [AWS::CloudFormation::Stack](aws-properties-stack.md)  |  Stack ID  |  `arn:aws:cloudformation:``us-east-2``:803981987763:stack/mystack-mynestedstack-sggfrhxhum7w/f449b250-b969-11e0-a185-5081d0136786`  | 
|  [AWS::CloudFormation::WaitCondition](aws-properties-waitcondition.md)  |  Name  |  `arn:aws:cloudformation:``us-east-2``:803981987763:stack/mystack/c325e210-bdf2-11e0-9638-50690880c386/mywaithandle`  | 
|  [AWS::CloudFormation::WaitConditionHandle](aws-properties-waitconditionhandle.md)  |  Wait Condition Signal URL  |  `https://cloudformation-waitcondition-``us-east-2``.s3.amazonaws.com/arn%3Aaws%3Acloudformation%3A``us-east-2``%3A803981987763%3Astack%2Fwaittest%2F054a33d0-bdee-11e0-8816-5081c490a786%2FmyWaitHandle?Expires=1312475488&AWSAccessKeyId=AKIAIOSFODNN7EXAMPLE&Signature=tUsrW3WvWVT46K69zMmgbEkwVGo%3D`  | 
|  [AWS::CloudFront::Distribution](aws-resource-cloudfront-distribution.md)  |  Distribution ID  |  `E27LVI50CSW06W`  | 
|  [AWS::CloudTrail::Trail](aws-resource-cloudtrail-trail.md)  |  Trail name  |  `awscloudtrail-example`  | 
|  [AWS::CloudWatch::Alarm](aws-properties-cw-alarm.md)  |  Name  |  `mystack-myalarm-3AOHFRGOXR5T`  | 
|  [AWS::CodeBuild::Project](aws-resource-codebuild-project.md)  |  Project name  |  `myProjectName`  | 
|  [AWS::CodeCommit::Repository](aws-resource-codecommit-repository.md)  |  Repository ID  |  `12a345b6-bbb7-4bb6-90b0-8c9577a2d2b9`  | 
| [AWS::CodeDeploy::Application](aws-resource-codedeploy-application.md) |  Application name  |  `myapplication-a123d0d1`  | 
| [AWS::CodeDeploy::DeploymentConfig](aws-resource-codedeploy-deploymentconfig.md) |  Deployment configuration name  |  `mydeploymentconfig-a123d0d1`  | 
| [AWS::CodeDeploy::DeploymentGroup](aws-resource-codedeploy-deploymentgroup.md) |  Deployment group name  |  `mydeploymentgroup-a123d0d1`  | 
| [AWS::CodePipeline::CustomActionType](aws-resource-codepipeline-customactiontype.md) |  Custom action name  |  `mysta-MyCus-A1BCDEFGHIJ2`  | 
| [AWS::CodePipeline::Pipeline](aws-resource-codepipeline-pipeline.md) |  Pipeline name  |  `mysta-MyPipeline-A1BCDEFGHIJ2`  | 
| [AWS::Config::ConfigRule](aws-resource-config-configrule.md) |  Configuration rule name  |  `mystack-MyConfigRule-12ABCFPXHV4OV`  | 
| [AWS::Config::ConfigurationRecorder](aws-resource-config-configurationrecorder.md) |  Configuration recorder name  |  `default`  | 
| [AWS::Config::DeliveryChannel](aws-resource-config-deliverychannel.md) |  Delivery channel name  |  `default`  | 
| [AWS::DataPipeline::Pipeline](aws-resource-datapipeline-pipeline.md) |  Pipeline ID  |  `df-sample322HVPGK130TOD`  | 
|  [AWS::DAX::Cluster](aws-resource-dax-cluster.md)  |  `Name`  |  `MyDAXCluster`  | 
| [AWS::DirectoryService::MicrosoftAD](aws-resource-directoryservice-microsoftad.md) |  Microsoft directory ID  |  `d-12345ab592`  | 
| [AWS::DirectoryService::SimpleAD](aws-resource-directoryservice-simplead.md) |  Directory ID  |  `d-12345ab592`  | 
| [AWS::DynamoDB::Table](aws-resource-dynamodb-table.md) |  Table Name  |  `MyDDBTable`  | 
|  [AWS::EC2::EIP](aws-properties-ec2-eip.md)  |  Elastic IP Address  |  `192.0.2.0`  | 
|  [AWS::EC2::EIPAssociation](aws-properties-ec2-eip-association.md)  |  Name  |  `mystack-myeipa-1NU3IL8LJ313N`  | 
|  [AWS::EC2::FlowLog](aws-resource-ec2-flowlog.md)  |  Flow log ID  |  `fl-1a23b456`  | 
|  [AWS::EC2::Host](aws-resource-ec2-host.md)  |  Host ID  |  `h-0ab123c45d67ef89`  | 
|  [AWS::EC2::Instance](aws-properties-ec2-instance.md)  |  Instance ID  |  `i-636be302`  | 
|  [AWS::EC2::NatGateway](aws-resource-ec2-natgateway.md)  |  NAT gateway ID  |  `nat-0a12bc456789de0fg`  | 
|  [AWS::EC2::NetworkInterfacePermission](aws-resource-ec2-networkinterfacepermission.md)  |  Network interface permission ID  |  `eni-perm-055663b682ea24b48`  | 
|  [AWS::EC2::PlacementGroup](aws-resource-ec2-placementgroup.md)  |  Placement group name  |  `mystack-myplacementgroup-CU6107MRVLR7`  | 
|  [AWS::EC2::RouteTable](aws-resource-ec2-route-table.md)  |  Route table ID  | rtb\-12a34567 | 
|  [AWS::EC2::SecurityGroup](aws-properties-ec2-security-group.md)  |  Name or security group ID \(for VPC security groups that are not in a default VPC\)  |  `mystack-mysecuritygroup-QQB406M8FISX or sg-94b3a1f6`  | 
|  [AWS::EC2::SecurityGroupIngress](aws-properties-ec2-security-group-ingress.md)  |  Name  |  `mysecuritygroupingress`  | 
|  [AWS::EC2::SpotFleet](aws-resource-ec2-spotfleet.md)  |  Name  |  `sfr-73fbd2ce-aa30-494c-8788-1cee4EXAMPLE`  | 
|  [AWS::EC2::Subnet](aws-resource-ec2-subnet.md)  |  Subnet ID  |  `subnet-e19f0178`  | 
|  [AWS::EC2::Volume](aws-properties-ec2-ebs-volume.md)  |  Volume ID  |  `vol-3cdd3f56`  | 
|  [AWS::EC2::VolumeAttachment](aws-properties-ec2-ebs-volumeattachment.md)  |  Name  |  `mystack-myvola-ERXHJITXMRLT`  | 
|  [AWS::EC2::VPC](aws-resource-ec2-vpc.md)  |  VPC ID  |  `vpc-18ac277d`  | 
| [AWS::EC2::VPCPeeringConnection](aws-resource-ec2-vpcpeeringconnection.md) |  VPC peering connection ID  |  `pcx-75de3e1d`  | 
|  [AWS::EC2::VPCEndpoint](aws-resource-ec2-vpcendpoint.md)  |  Endpoint ID  |  `vpce-a123d0d1`  | 
|  [AWS::ECR::Repository](aws-resource-ecr-repository.md)  |  Repository name  |  `test-repository`  | 
|  [AWS::ECS::Cluster](aws-resource-ecs-cluster.md)  |  Name  |  `MyStack-MyECSCluster-NT5EUXTNTXXD`  | 
|  [AWS::ECS::Service](aws-resource-ecs-service.md)  |  Service ARN  |  `arn:aws:ecs:us-west-2:123456789012:service/sample-webapp`  | 
|  [AWS::ECS::TaskDefinition](aws-resource-ecs-taskdefinition.md)  |  Task definition ARN  |  `arn:aws:ecs:us-west-2:123456789012:task-definition/TaskDefinitionFamily:1`  | 
|  [AWS::EFS::FileSystem](aws-resource-efs-filesystem.md)  |  File system ID  |  `fs-47a2c22e`  | 
|  [AWS::EFS::MountTarget](aws-resource-efs-mounttarget.md)  |  Mount target ID  |  `fsmt-55a4413c`  | 
|  [AWS::EKS::Cluster](aws-resource-eks-cluster.md)  |  Name  |  `EKSCluster-NT5EUXTNTXXD`  | 
|  [AWS::ElastiCache::ReplicationGroup](aws-resource-elasticache-replicationgroup.md)  |  Name  |  `abc12xmy3d1w3hv6`  | 
|  [AWS::ElastiCache::SubnetGroup](aws-properties-elasticache-subnetgroup.md)  |  Name  |  `myCachesubnetgroup`  | 
|  [AWS::ElasticLoadBalancingV2::Listener](aws-resource-elasticloadbalancingv2-listener.md)  |  Listener's Amazon Resource Name \(ARN\)  |  `arn:aws:elasticloadbalancing:us-west-2:123456789012:listener/app/my-load-balancer/50dc6c495c0c9188/f2f7dc8efc522ab2`  | 
|  [AWS::ElasticLoadBalancingV2::ListenerRule](aws-resource-elasticloadbalancingv2-listenerrule.md)  |  Listener rule's Amazon Resource Name \(ARN\)  |  `arn:aws:elasticloadbalancing:us-west-2:123456789012:listener-rule/app/my-load-balancer/50dc6c495c0c9188/f2f7dc8efc522ab2/9683b2d02a6cabee`  | 
|  [AWS::ElasticLoadBalancingV2::LoadBalancer](aws-resource-elasticloadbalancingv2-loadbalancer.md)  |  Application load balancer's Amazon Resource Name \(ARN\)  |  `arn:aws:elasticloadbalancing:us-west-2:123456789012:loadbalancer/app/my-internal-load-balancer/50dc6c495c0c9188`  | 
|  [AWS::ElasticLoadBalancingV2::TargetGroup](aws-resource-elasticloadbalancingv2-targetgroup.md)  |  Target group's Amazon Resource Name \(ARN\)  |  `arn:aws:elasticloadbalancing:us-west-2:123456789012:targetgroup/my-targets/73e2d6bc24d8a067`  | 
|  [AWS::Elasticsearch::Domain](aws-resource-elasticsearch-domain.md)  |  Domain name  |  `mystack-elasticsea-abc1d2efg3h4`  | 
|  [AWS::EMR::Cluster](aws-resource-emr-cluster.md)  |  Cluster ID  |  `j-1ABCD123AB1A`  | 
|  [AWS::EMR::InstanceGroupConfig](aws-resource-emr-instancegroupconfig.md)  |  Instance group ID  |  `ig-ABC12DEF3456`  | 
|  [AWS::EMR::SecurityConfiguration](aws-resource-emr-securityconfiguration.md)  |  Name  |  `mySecurityConfiguration`  | 
|  [AWS::EMR::Step](aws-resource-emr-step.md)  |  Step ID  |  `s-1A2BC3D4EFG56`  | 
|  [AWS::ElasticBeanstalk::Application](aws-properties-beanstalk.md)  |  Name  |  `mystack-myapplication-FM6BIXY7U8PK`  | 
|  [AWS::ElasticBeanstalk::ApplicationVersion](aws-properties-beanstalk-version.md)  |  Name  |  `mystack-myapplicationversion-iy8ptveuxjly`  | 
|  [AWS::ElasticBeanstalk::ConfigurationTemplate](aws-resource-beanstalk-configurationtemplate.md)  |  Name  |  `mystack-myconfigurationtemplate-108RPH64J195`  | 
|  [AWS::ElasticBeanstalk::Environment](aws-properties-beanstalk-environment.md)  |  Name  |  `mystack-myenv-LKGNQSFHO1DB`  | 
|  [AWS::ElasticLoadBalancing::LoadBalancer](aws-properties-ec2-elb.md)  |  Name  |  `mystack-myelb-1WQN7BJGDB5YQ`  | 
|  [AWS::Events::Rule](aws-resource-events-rule.md)  |  Event rule ID  |  `mystack-ScheduledRule-ABCDEFGHIJK`  | 
|  [AWS::GameLift::Alias](aws-resource-gamelift-alias.md)  |  Alias ID  |  `myalias-a01234b56-7890-1de2-f345-g67h8i901j2k`  | 
|  [AWS::GameLift::Build](aws-resource-gamelift-build.md)  |  Build ID  |  `mybuild-a01234b56-7890-1de2-f345-g67h8i901j2k`  | 
|  [AWS::GameLift::Fleet](aws-resource-gamelift-fleet.md)  |  Fleet ID  |  `myfleet-a01234b56-7890-1de2-f345-g67h8i901j2k`  | 
|  [AWS::Glue::Classifier](aws-resource-glue-classifier.md)  |  Name  |  `abc123`  | 
|  [AWS::Glue::Connection](aws-resource-glue-connection.md)  |  `ConnectionInput` name  |  `abc123`  | 
|  [AWS::Glue::Crawler](aws-resource-glue-crawler.md)  |  Name  |  `abc123`  | 
|  [AWS::Glue::Database](aws-resource-glue-database.md)  |  `DatabaseInput` name  |  `abc123`  | 
|  [AWS::Glue::Job](aws-resource-glue-job.md)  |  Name  |  `abc123`  | 
|  [AWS::Glue::Table](aws-resource-glue-table.md)  |  `TableInput` name  |  `abc123`  | 
|  [AWS::Glue::Trigger](aws-resource-glue-trigger.md)  |  Name  |  `abc123`  | 
|  [AWS::GuardDuty::Detector](aws-resource-guardduty-detector.md)  |  Detector ID  |  `12abc34d567e8fa901bc2d34e56789f0`  | 
|  [AWS::GuardDuty::IPSet](aws-resource-guardduty-ipset.md)  |  IPSet ID  |  `0cb0141ab9fbde177613ab9436212e90`  | 
|  [AWS::GuardDuty::Master](aws-resource-guardduty-master.md)  |  Master ID  |  `012345678901`  | 
|  [AWS::GuardDuty::Member](aws-resource-guardduty-member.md)  |  Member ID  |  `012345678901`  | 
|  [AWS::GuardDuty::ThreatIntelSet](aws-resource-guardduty-threatintelset.md)  |  ThreatIntel Set ID  |  `12a34567890bc1de2345f67ab8901234`  | 
|  [AWS::IAM::AccessKey](aws-properties-iam-accesskey.md)  |  AccessKeyId  |  `AKIAIOSFODNN7EXAMPLE`  | 
|  [AWS::IAM::Group](aws-properties-iam-group.md)  |  Group name  |  `mystack-mygroup-1DZETITOWEKVO`  | 
|  [AWS::IAM::ManagedPolicy](aws-resource-iam-managedpolicy.md)  |  Policy ARN  |  `arn:aws:iam::123456789012:policy/teststack-CreateTestDBPolicy-16M23YE3CS700`  | 
|  [AWS::IAM::User](aws-properties-iam-user.md)  |  User name  |  `mystack-myuser-1CCXAFG2H2U4D`  | 
| [AWS::IoT::Certificate](aws-resource-iot-certificate.md) | Certificate ID | a1234567b89c012d3e4fg567hij8k9l01mno1p23q45678901rs234567890t1u2 | 
| [AWS::IoT::Policy](aws-resource-iot-policy.md) | Policy name | MyPolicyName | 
| [AWS::IoT::Thing](aws-resource-iot-thing.md) | Thing name | MyStack\-MyThing\-AB1CDEFGHIJK | 
| [AWS::IoT::TopicRule](aws-resource-iot-topicrule.md) | Topic rule name | MyStackMyTopicRule12ABC3D456EFG | 
|  [AWS::Kinesis::Stream](aws-resource-kinesis-stream.md)  |  Name  |  `mystack-mystream-1NAOH4L1RIQ7I`  | 
|  [AWS::KinesisFirehose::DeliveryStream](aws-resource-kinesisfirehose-deliverystream.md)  |  Delivery stream name  |  `mystack-deliverystream-1ABCD2EF3GHIJ`  | 
|  [AWS::KMS::Alias](aws-resource-kms-alias.md)  |  Alias name  |  `alias/myAlias`  | 
|  [AWS::KMS::Key](aws-resource-kms-key.md)  |  Key ID  |  `123ab456-a4c2-44cb-95fd-b781f32fbb37`  | 
|  [AWS::Lambda::Alias](aws-resource-lambda-alias.md)  |  Amazon Resource Name of the AWS Lambda alias  | arn:aws:lambda:us\-west\-2:123456789012:function:helloworld:BETA | 
|  [AWS::Lambda::EventSourceMapping](aws-resource-lambda-eventsourcemapping.md)  |  Name  |  `MyStack-lambdaeventsourcemapping-CU6107MRVLR7`  | 
|  [AWS::Lambda::Function](aws-resource-lambda-function.md) |  Name  |  `MyStack-AMILookUp-NT5EUXTNTXXD`  | 
|  [AWS::Lambda::Version](aws-resource-lambda-version.md)  |  Amazon Resource Name of the AWS Lambda version  | arn:aws:lambda:us\-west\-2:123456789012:function:helloworld:1 | 
|  [AWS::Logs::Destination](aws-resource-logs-destination.md) |  Destination name  |  `TestDestination`  | 
|  [AWS::Logs::LogGroup](aws-resource-logs-loggroup.md) |  Name  |  `mystack-myLogGroup-1341JS4M96031`  | 
|  [AWS::Logs::LogStream](aws-resource-logs-logstream.md) |  Log stream name  |  `MyAppLogStream`  | 
|  [AWS::OpsWorks::App](aws-resource-opsworks-app.md)  |  AWS OpsWorks Application ID  |  `4fee5b96-0d10-4af1-bcc5-25f92e3c6acf`  | 
|  [AWS::OpsWorks::Instance](aws-resource-opsworks-instance.md)  |  AWS OpsWorks Instance ID  |  `aa2e9ae2-2b4b-491c-aeb6-8bf3ce9400fe`  | 
|  [AWS::OpsWorks::Layer](aws-resource-opsworks-layer.md)  |  AWS OpsWorks Layer ID  |  `730b238b-f7c4-461d-b7c0-3feb7ef1152a`  | 
|  [AWS::OpsWorks::Stack](aws-resource-opsworks-stack.md)  |  AWS OpsWorks Stack ID  |  `5c9f04e8-370e-4bd3-ae09-a4bbcc2998bb`  | 
|  [AWS::OpsWorks::UserProfile](aws-resource-opsworks-userprofile.md)  |  IAM user Amazon Resource Name  |  `arn:aws:iam::123456789012:user/opsworksuser`  | 
|  [AWS::OpsWorks::Volume](aws-resource-opsworks-volume.md)  |  AWS OpsWorks Volume ID  |  `1ab23cd4-92ff-4501-b37c-example`  | 
|  [AWS::RDS::DBCluster](aws-resource-rds-dbcluster.md)  |  Cluster name  |  `test-rdscluster-pdedtss0mfqr`  | 
|  [AWS::RDS::DBClusterParameterGroup](aws-resource-rds-dbclusterparametergroup.md)  |  Parameter group name  |  `test-dbparamgroup-4l8qqx46vjby`  | 
|  [AWS::RDS::DBInstance](aws-properties-rds-database-instance.md)  |  Name  |  `mystack-mydb-ea5ugmfvuaxg`  | 
|  [AWS::RDS::DBSecurityGroup](aws-properties-rds-security-group.md)  |  Name  |  `mystack-mydbsecuritygroup-1k5u5dxjb0nxs`  | 
|  [AWS::RDS::DBSubnetGroup](aws-resource-rds-dbsubnet-group.md)  |  DB subnet group name  |  `mystack-mydbsubnetgroup-1k5u5dxjb0nxs`  | 
|  [AWS::RDS::OptionGroup](aws-resource-rds-optiongroup.md)  |  Name  |  `mystack-myoptiongroup-1qmfawfea4vmz`  | 
|  [AWS::Redshift::Cluster](aws-resource-redshift-cluster.md)  |  Name  |  `mystack-myredshiftcluster-ranmiv3f0mad`  | 
|  [AWS::Redshift::ClusterParameterGroup](aws-resource-redshift-clusterparametergroup.md)  |  Name  |  `mysta-mypar-1AJYM1FL3WQBW`  | 
|  [AWS::Redshift::ClusterSecurityGroup](aws-resource-redshift-clustersecuritygroup.md)  |  Name  |  `mystack-myredshiftclustersecuritygroup-bjy2afmhy3ee`  | 
|  [AWS::Redshift::ClusterSubnetGroup](aws-resource-redshift-clustersubnetgroup.md)  |  Name  |  `mystack-myredshiftclustersubnetgroup-aq6rsdq8rp71`  | 
|  [AWS::Route53::HealthCheck](aws-resource-route53-healthcheck.md)  |  Amazon Route 53 health check ID  |  `e0a123b4-4dba-4650-935e-example`  | 
|  [AWS::Route53::HostedZone](aws-resource-route53-hostedzone.md)  | Hosted zone ID |  `Z23ABC4XYZL05B`  | 
|  [AWS::S3::Bucket](aws-properties-s3-bucket.md)  |  Name  |  `mystack-mys3bucket-1hbsmonr9mytq`  | 
|  [AWS::SDB::Domain](aws-properties-simpledb.md)  |  Name  |  `mystack-mysdbdomain-IVNAOZTDFVXL`  | 
|  [AWS::SNS::Topic](aws-properties-sns-topic.md)  |  Topic ARN  |  `arn:aws:sns:``us-east-2``:123456789012:mystack-mytopic-NZJ5JSMVGFIE`  | 
|  [AWS::SQS::Queue](aws-properties-sqs-queues.md)  |  Queue URL  |  `https://sqs.``us-east-2``.amazonaws.com/803981987763/aa4-MyQueue-Z5NOSZO2PZE9`  | 
|  [AWS::SSM::Document](aws-resource-ssm-document.md)  |  SSM document name  |  `ssm-myinstanceconfig-ABCNPH3XCAO6`  | 
|  [AWS::SSM::MaintenanceWindow](aws-resource-ssm-maintenancewindow.md)  |  Maintenance window ID  |  `mw-abcde1234567890yz`  | 
|  [AWS::SSM::MaintenanceWindowTarget](aws-resource-ssm-maintenancewindowtarget.md)  |  Maintenance window target ID  |  `12a345b6-bbb7-4bb6-90b0-8c9577a2d2b9`  | 
|  [AWS::SSM::MaintenanceWindowTask](aws-resource-ssm-maintenancewindowtask.md)  |  Maintenance window task ID  |  `12a345b6-bbb7-4bb6-90b0-8c9577a2d2b9`  | 
|  [AWS::SSM::PatchBaseline](aws-resource-ssm-patchbaseline.md)  |  Patch baseline ID  |  `pb-abcde1234567890yz` The ID of the default patch baseline provided by AWS is an ARN—for example `arn:aws:ssm:us-west-2:123456789012:patchbaseline/abcde1234567890yz`\.  | 
| [AWS::StepFunctions::Activity](aws-resource-stepfunctions-activity.md) | Amazon Resource Name \(ARN\) of the AWS Step Functions activity | arn:aws:states:us\-east\-1:111122223333:activity:myActivity | 
| [AWS::StepFunctions::StateMachine](aws-resource-stepfunctions-statemachine.md) | ARN of the created Step Functions state machine | arn:aws:states:us\-east\-1:111122223333:stateMachine:MyStateMachine\-ABCDEFGHIJ1K | 
|  [AWS::WAF::ByteMatchSet](aws-resource-waf-bytematchset.md)  |  Byte match ID  |  `aabc123a-fb4f-4fc6-becb-2b00831cadcf`  | 
|  [AWS::WAF::IPSet](aws-resource-waf-ipset.md)  |  IP set ID  |  `aabc123a-fb4f-4fc6-becb-2b00831cadcf`  | 
|  [AWS::WAF::Rule](aws-resource-waf-rule.md)  |  Rule ID  |  `aabc123a-fb4f-4fc6-becb-2b00831cadcf`  | 
|  [AWS::WAF::SizeConstraintSet](aws-resource-waf-sizeconstraintset.md)  |  Size constraint set ID  |  `aabc123a-fb4f-4fc6-becb-2b00831cadcf`  | 
|  [AWS::WAF::SqlInjectionMatchSet](aws-resource-waf-sqlinjectionmatchset.md)  |  SQL match set ID  |  `aabc123a-fb4f-4fc6-becb-2b00831cadcf`  | 
|  [AWS::WAF::WebACL](aws-resource-waf-webacl.md)  |  Web ACL ID  |  `aabc123a-fb4f-4fc6-becb-2b00831cadcf`  | 
|  [AWS::WAF::XssMatchSet](aws-resource-waf-xssmatchset.md)  |  XSS match set ID  |  `aabc123a-fb4f-4fc6-becb-2b00831cadcf`  | 
|  [AWS::WAFRegional::ByteMatchSet](aws-resource-wafregional-bytematchset.md)  |  Byte match ID  |  `aabc123a-fb4f-4fc6-becb-2b00831cadcf`  | 
|  [AWS::WAFRegional::IPSet](aws-resource-wafregional-ipset.md)  |  IP set ID  |  `aabc123a-fb4f-4fc6-becb-2b00831cadcf`  | 
|  [AWS::WAFRegional::Rule](aws-resource-wafregional-rule.md)  |  Rule ID  |  `aabc123a-fb4f-4fc6-becb-2b00831cadcf`  | 
|  [AWS::WAFRegional::SizeConstraintSet](aws-resource-wafregional-sizeconstraintset.md)  |  Size constraint set ID  |  `aabc123a-fb4f-4fc6-becb-2b00831cadcf`  | 
|  [AWS::WAFRegional::SqlInjectionMatchSet](aws-resource-wafregional-sqlinjectionmatchset.md)  |  SQL match set ID  |  `aabc123a-fb4f-4fc6-becb-2b00831cadcf`  | 
|  [AWS::WAFRegional::WebACL](aws-resource-wafregional-webacl.md)  |  Web ACL ID  |  `aabc123a-fb4f-4fc6-becb-2b00831cadcf`  | 
|  [AWS::WAFRegional::XssMatchSet](aws-resource-wafregional-xssmatchset.md)  |  XSS match set ID  |  `aabc123a-fb4f-4fc6-becb-2b00831cadcf`  | 
|  [AWS::WorkSpaces::Workspace](aws-resource-workspaces-workspace.md)  |  Workspace ID  |  `ws-cdd1gggh7`  | 
|  [Pseudo Parameter](pseudo-parameter-reference.md)  |  AWS::AccountId  |  `123456789012`  | 
|  [Pseudo Parameter](pseudo-parameter-reference.md)  |  AWS::NotificationARNs  |  `[arn:aws:sns:us-east-1:123456789012:MyTopic]`  | 
|  [Pseudo Parameter](pseudo-parameter-reference.md)  |  AWS::NoValue  |  Does not return a value\.  | 
|  [Pseudo Parameter](pseudo-parameter-reference.md)  |  AWS::Region  |  `us-east-2`  | 
|  [Pseudo Parameter](pseudo-parameter-reference.md)  |  AWS::StackId  |  `arn:aws:cloudformation:us-east-1:123456789012:stack/MyStack/1c2fa620-982a-11e3-aff7-50e2416294e0`  | 
|  [Pseudo Parameter](pseudo-parameter-reference.md)  |  AWS::StackName  |  `MyStack`  | 