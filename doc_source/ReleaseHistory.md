# Release History<a name="ReleaseHistory"></a>

The following table describes important changes in each release of the AWS CloudFormation User Guide after May 2018\. For notification about updates to this documentation, you can subscribe to an RSS feed\.

| Change | Description | Date | 
| --- |--- |--- |
| [UseOnlineResharding update policy now available\.](#ReleaseHistory) | To modify a replication group's shards by adding or removing shards, rather than replacing the entire `AWS::ElastiCache::ReplicationGroup` resource, use the `UseOnlineResharding` update policy\. For more information, see [UseOnlineResharding Policy](aws-attribute-updatepolicy.md#cfn-attributes-updatepolicy-useonlineresharding)\. | September 20, 2018 | 
| [Updated resources ](#ReleaseHistory) | The following resources have been updated: AWS::ApiGateway::Deployment, AWS::ApiGateway::Method, AWS::ApiGateway::Stage, AWS::ApiGateway::UsagePlan, AWS::CodeBuild::Project, AWS::CodeDeploy::DeploymentGroup, AWS::EC2::FlowLog, AWS::EC2::SpotFleet, AWS::EC2::VPCEndpoint, AWS::ECS::Service, AWS::ECS::TaskDefinition, and AWS::RDS::DBCluster\. 

 [AWS::ApiGateway::Deployment](aws-resource-apigateway-deployment.md)   
Use the `DeploymentCanarySettings` property to specify settings for the canary deployment\.  
In the [API Gateway Deployment StageDescription](aws-properties-apigateway-deployment-stagedescription.md) property type:   
+ Use the `AccessLogSetting` property to specify settings for logging access in this stage\.
+ Use the `CanarySetting` property to specify settings for the canary deployment in this stage\. 

 [AWS::ApiGateway::Method](aws-resource-apigateway-method.md)   
Use the `AuthorizationScopes` property to specify a list of authorization scopes configured on the method\.  
In the [API Gateway Method Integration](aws-properties-apitgateway-method-integration.md):   
+ Use the `ConnectionId` property to specify the ID of the VpcLink used for the integration when `connectionType=VPC_LINK`\.
+ Use the `ConnectionType` property to specify the type of the network connection to the integration endpoint\. 
+ Use the `TimeoutInMillis` property to specify a custom timeout between 50 and 29,000 milliseconds\. 

 [AWS::ApiGateway::Stage](aws-resource-apigateway-stage.md)   
Use the `AccessLogSetting` property to specify settings for logging access in this stage\.  
Use the `CanarySetting` property to specify settings for the canary deployment in this stage\. 

 [AWS::ApiGateway::UsagePlan](aws-resource-apigateway-usageplan.md)   
In the [](aws-properties-apigateway-usageplan-apistage.md) property type, use the `Throttle` property to specify a map containing method\-level throttling information for API stage in a usage plan\. 

 [AWS::CodeBuild::Project](aws-resource-codebuild-project.md)   
Use the `LogsConfig` property specify logs for a project\. Logs can be CloudWatch Logs, uploaded to a specified S3 bucket, or both\.  
In the [AWS CodeBuild Project LogsConfig](aws-properties-codebuild-project-logsconfig.md) property type:  
+ Use the `CloudWatchLogs` property to specify details about CloudWatch Logs\.
+ Use the `S3Logs` property to specify details about logs that are uploaded to an S3 bucket\. 

 [AWS::CodeDeploy::DeploymentGroup](aws-resource-codedeploy-deploymentgroup.md)   
Use the `Ec2TagSet` property to specify information about groups of tags applied to EC2 instances\. The deployment group will include only EC2 instances identified by all the tag groups\.  
Use the `OnPremisesInstanceTagSet` property to specify information about groups of tags applied to on\-premises instances\. The deployment group will include only on\-premises instances identified by all the tag groups\.  
The `DeliverLogsPermissionArn` and `LogGroupName` properties are no longer required\. 

 [AWS::EC2::FlowLog](aws-resource-ec2-flowlog.md)   
Use the `LogDestination` property to specify the destination to which the flow log data is to be published\.   
Use the `LogDestinationType` property to specify the type of destination to which the flow log data is to be published\. Flow log data can be published to CloudWatch Logs or Amazon S3\. 

 [AWS::EC2::SpotFleet](aws-resource-ec2-spotfleet.md)   
In the `SpotFleetRequestConfigData` property type, use the `InstanceInterruptionBehavior` property to specify the behavior when a Spot Instance is interrupted\.  
In the `SpotFleetRequestConfigData` property type, use the `LoadBalancersConfig` property to specify one or more Classic Load Balancers and target groups to attach to the Spot Fleet request\. Spot Fleet registers the running Spot Instances with the specified Classic Load Balancers and target groups\.  
In the `Placement` property type, use the `Tenancy` property to specify the tenancy of the instance \(if the instance is running in a VPC\)\. An instance with a tenancy of dedicated runs on single\-tenant hardware\. The host tenancy is not supported for Spot Instances\. 

 [AWS::EC2::VPCEndpoint](aws-resource-ec2-vpcendpoint.md)   
Use the following attributes with the `Fn::GetAtt` function to return attribute values\.  
+ Use `CreationTimestamp` to return the date and time the VPC endpoint was created\.
+ Use `DnsEntries` to return the DNS entries for the endpoint\.
+ Use `NetworkInterfaceIds` to return the network interfaces for the endpoint\. 

 [AWS::ECS::Service](aws-resource-ecs-service.md)   
The `ServiceRegistries` property now requires replacement upon update\.  
Use the `SchedulingStrategy` property to specify the scheduling strategy to use for the service\.   
In the [Amazon ECS Service ServiceRegistry](aws-properties-ecs-service-serviceregistry.md) property type:   
+ Use the `ContainerName` property to specify the container name value, already specified in the task definition, to be used for your service discovery service\. 
+ Use the `ContainerPort` property to specify the port value, already specified in the task definition, to be used for your service discovery service\. 

 [AWS::ECS::TaskDefinition](aws-resource-ecs-taskdefinition.md)   
In the [Amazon ECS TaskDefinition LinuxParameters](aws-properties-ecs-taskdefinition-linuxparameters.md) property type:   
+ Use the `Tmpfs` property to specify the container path, mount options, and size of the tmpfs mount\.
+ Use the `SharedMemorySize` property to specify the size \(in MiB\) of the `/dev/shm` volume\. 
In the [Amazon ECS TaskDefinition Volumes](aws-properties-ecs-taskdefinition-volumes.md) property type, use the `DockerVolumeConfiguration` property to specify the configuration of a Docker volume\.  
In the [Amazon ECS TaskDefinition ContainerDefinition](aws-properties-ecs-taskdefinition-containerdefinitions.md) property type, use the `RepositoryCredentials` property to specify the repository credentials for private registry authentication\. 

 [AWS::ElastiCache::ReplicationGroup](aws-resource-elasticache-replicationgroup.md)   
The `NodeGroupConfiguration` and `NumNodeGroups` properties are now conditional for some update operations\.  
In the [ElastiCache ReplicationGroup NodeGroupConfiguration](aws-properties-elasticache-replicationgroup-nodegroupconfiguration.md) property type, use the `NodeGroupId` property to specify either the ElastiCache for Redis supplied 4\-digit id or a user supplied id for the node group these configuration values apply to\. 

 [AWS::RDS::DBCluster](aws-resource-rds-dbcluster.md)   
Use the `EngineMode` property to specify the DB engine mode of the DB cluster\.  
Use the `ScalingConfiguration` property to specify the scaling properties of the DB cluster, for DB clusters in `serverless` DB engine mode\.  | September 20, 2018 | 
| [New resources](#ReleaseHistory) | The following resources were added: AWS::IoT1Click::Device, AWS::IoT1Click::Placement, and AWS::IoT1Click::Project\. 

 [AWS::IoT1Click::Device](aws-resource-iot1click-device.md)   
Use the `AWS::IoT1Click::Device` resource to change the enabled state of an AWS IoT 1\-Click compatible device\. 

 [AWS::IoT1Click::Placement](aws-resource-iot1click-placement.md)   
Use the `AWS::IoT1Click::Placement` resource to create an empty AWS IoT 1\-Click placement\. 

 [AWS::IoT1Click::Project](aws-resource-iot1click-project.md)   
Use the `AWS::IoT1Click::Project` resource to create an empty project with a placement template\.  | September 20, 2018 | 
| [New resource](#ReleaseHistory) | Added the AWS::CloudFormation::Macro resource\. 

 [AWS::CloudFormation::Macro](aws-resource-cloudformation-macro.md)   
Use the `AWS::CloudFormation::Macro` resource to create a template macro to perform custom processing on AWS CloudFormation templates\.  | September 6, 2018 | 
| [Macros now available](#ReleaseHistory) | Use macros to to perform custom processing on templates, from simple actions like find\-and\-replace operations to extensive transformations of entire templates\. See [Using AWS CloudFormation Macros to Perform Custom Processing on Templates](template-macros.md) for more information\. | September 6, 2018 | 
| [Updated resources](#ReleaseHistory) | Added the Logs property to AWS::AmazonMQ::Broker\. Added the SecondaryArtifacts and SecondarySources properties to AWS::CodeBuild::Project\. 

[AWS::AmazonMQ::Broker](aws-resource-amazonmq-broker.md)   
Use the `Logs` property to enable general or audit logging for an Amazon MQ broker\. 

 [AWS::CodeBuild::Project](aws-resource-codebuild-project.md)   
In the [AWS CodeBuild Project Artifacts](aws-properties-codebuild-project-artifacts.md) property type, you can use the `SecondaryArtifacts` property to specify secondary artifacts for a build project\. You can use the `SecondarySources` property to specify secondary inputs for a build project\.  | August 30, 2018 | 
| [Updated resources](#ReleaseHistory) | Added the Configuration property to AWS::Glue::Crawler\. Added the JsonClassifier and XMLClassifier properties to AWS::Glue::Classifier\. 

 [AWS::Glue::Crawler](aws-resource-glue-crawler.md)   
Use the `Configuration` property to specify crawler configuration information\. This versioned JSON string allows users to specify aspects of a crawler's behavior\. 

 [AWS::Glue::Classifier](aws-resource-glue-classifier.md)   
Use the `JsonClassifier` property to specify AWS Glue classifier for JSON\.  
Use the `XMLClassifier` property to specify AWS Glue classifier for XML content\.  | August 23, 2018 | 
| [AWS CloudFormation now supports VPC endpoints powered by PrivateLink\.](#ReleaseHistory) | You can use a VPC endpoint to create a private connection between your VPC and AWS CloudFormation without requiring access over the Internet, through a NAT instance, a VPN connection, or AWS Direct Connect\. For more information, see [Setting Up VPC Endpoints for AWS CloudFormation](cfn-vpce-bucketnames.md)\. | August 22, 2018 | 
| [Dynamic references support secure strings](#ReleaseHistory) | Use new dynamic references to specify values that are stored and managed in other services, including Systems Manager Parameter Store SecureString type parameters, in your stack templates\.For more information, see [Using Dynamic References to Specify Template ValuesSpecifying Dynamic References in Stack Templates](dynamic-references.md)\. | August 16, 2018 | 
| [Updated resources](#ReleaseHistory) | The following resources were updated: AWS::ApiGateway::DomainName, AWS::CertificateManager::Certificate, AWS::EC2::VPCPeeringConnection, AWS::EFS::FileSystem, AWS::EMR::Cluster, AWS::RDS::DBClusterParameterGroup, AWS::SNS::Subscription, and AWS::SQS::Queue\. 

 [AWS::ApiGateway::DomainName](aws-resource-apigateway-domainname.md)   

Use the following attributes with the `Fn::GetAtt` intrinsic function:
+ The `DistributionHostedZoneId` attribute returns the region\-agnostic Amazon Route 53 Hosted Zone ID of the edge\-optimized endpoint\. 
+ The `RegionalDomainName` attribute returns the domain name associated with the regional endpoint for this custom domain name\. 
+ The `RegionalHostedZoneId` attribute returns the region\-specific Amazon Route 53 Hosted Zone ID of the regional endpoint\. 

 [AWS::CertificateManager::Certificate](aws-resource-certificatemanager-certificate.md)   
Use the `ValidationMethod` property to specify the method you want to use if you are requesting a public certificate to validate that you own or control a domain\. 

 [AWS::EC2::VPCPeeringConnection](aws-resource-ec2-vpcpeeringconnection.md)   
Use the `PeerRegion` property to specify the region code for the accepter VPC, if the accepter VPC is located in a region other than the region in which you make the request\. 

 [AWS::EFS::FileSystem](aws-resource-efs-filesystem.md)   
+ Use the `ProvisionedThroughputInMibps` property to specify the throughput, measured in MiB/s, that you want to provision for a file system that you're creating\. 
+ Use the `ThroughputMode` property to specify the throughput mode for the file system to be created\.  

 [AWS::EMR::Cluster](aws-resource-emr-cluster.md)   
Use the `KerberosAttributes` property to specify attributes for Kerberos configuration when Kerberos authentication is enabled using a security configuration\. 

 [AWS::RDS::DBClusterParameterGroup](aws-resource-rds-dbclusterparametergroup.md)   
The `Tags` property now requires no interruption to update\. 

 [AWS::SNS::Subscription](aws-resource-sns-subscription.md)   
+ Use the `DeliveryPolicy` property to specify the JSON serialization of the subscription's delivery policy\.
+ Use the `FilterPolicy` property to specify the filter policy JSON that is assigned to the subscription\.
+ Use the `RawMessageDelivery` property to specify if raw message delivery is enabled for the subscription\.
+ Use the `Region` property to specify the region in which the topic resides\. 

 [AWS::SQS::Queue](aws-properties-sqs-queues.md)   
Use the `Tags` property to specify the tags that you want to attach to this queue\.  | August 15, 2018 | 
| [Updated resource](#ReleaseHistory) | Added the SSESpecification property to AWS::DAX::Cluster\. 

 [AWS::DAX::Cluster](aws-resource-dax-cluster.md)   
Use the `SSESpecification` property to specify the settings to enable server\-side encryption\.   | August 9, 2018 | 
| [New resource](#ReleaseHistory) | Added the AWS::EC2::VPCEndpointServicePermissions resource\. 

 [AWS::EC2::VPCEndpointServicePermissions](aws-resource-ec2-vpcendpointservicepermissions.md)   
Grant or revoke permissions for service consumers to connect the VPC endpoint service\.  | August 9, 2018 | 
| [Updated resource](#ReleaseHistory) | Added the OverrideArtifactName property to AWS::CodeBuild::Project\. 

 [AWS::CodeBuild::Project](aws-resource-codebuild-project.md)   
In the [AWS CodeBuild Project Artifacts](aws-properties-codebuild-project-artifacts.md) property type, set the `OverrideArtifactName` property to true to override the artifact name with a name specified in the buildspec file\. The name specified in a buildspec file is calculated at build time and uses the Shell command language\. For example, you can append a date and time to your artifact name so that it is always unique\.  | August 7, 2018 | 
| [Updated resource](#ReleaseHistory) | Added the EncryptionDisabled property to AWS::CodeBuild::Project\. 

 [AWS::CodeBuild::Project](aws-resource-codebuild-project.md)   
In the [AWS CodeBuild Project Artifacts](aws-properties-codebuild-project-artifacts.md) property type, set the `EncryptionDisabled` property to true to disable encryption for build output artifacts\. This option is only valid if your artifact type is Amazon S3\. If this is set to true with another artifact type, an invalidInputException will be thrown\.  | July 26, 2018 | 
| [Updated resource](#ReleaseHistory) | Added the Timeout property to AWS::Batch::JobDefinition\. 

 [AWS::Batch::JobDefinition](aws-resource-batch-jobdefinition.md)   
Use the `Timeout` property type to specify a job timeout configuration\.  | July 19, 2018 | 
| [New resource](#ReleaseHistory) | The following resource was added: AWS::IAM::ServiceLinkedRole\. 

 [AWS::IAM::ServiceLinkedRole](aws-resource-iam-servicelinkedrole.md)   
Use the `AWS::IAM::ServiceLinkedRole` resource to create a service\-linked role in IAM\. A service\-linked role is a unique type of IAM role that is linked directly to an AWS service\. Service\-linked roles are predefined by the service and include all the permissions that the service requires to call other AWS services on your behalf\.  | July 19, 2018 | 
| [Updated resources](#ReleaseHistory) | Added the FieldLevelEncryptionId property to AWS::CloudFront::Distribution property types\. 

 [AWS::CloudFront::Distribution](aws-resource-cloudfront-distribution.md)   
In the [CloudFront Distribution CacheBehavior](aws-properties-cloudfront-distribution-cachebehavior.md) and [CloudFront Distribution DefaultCacheBehavior](aws-properties-cloudfront-distribution-defaultcachebehavior.md) property types, use the `FieldLevelEncryptionId` property to specify the ID for the field\-level encryption configuration that you want CloudFront to use for encrypting specific fields of data for a cache behavior or for the default cache behavior\.  | July 18, 2018 | 
| [Updated resource](#ReleaseHistory) | Added the HttpConfig property to AWS::AppSync::DataSource\. 

 [AWS::AppSync::DataSource](aws-resource-appsync-datasource.md)   
Use the `HttpConfig` property type to specify HttpConfig for an AWS AppSync data source\.  | July 12, 2018 | 
| [Updated resource](#ReleaseHistory) | Added the ReportBuildStatus property to AWS::CodeBuild::Project\. 

 [AWS::CodeBuild::Project](aws-resource-codebuild-project.md)   
In the [AWS CodeBuild Project Source](aws-properties-codebuild-project-source.md) property type, use the `ReportBuildStatus` property to specify whether to send your source provider the status of a build's start and completion\.  | July 10, 2018 | 
| [New resource](#ReleaseHistory) | The following resource was added: AWS::CodePipeline::Webhook\. 

 [AWS::CodePipeline::Webhook](aws-resource-codepipeline-webhook.md)   
Use the `AWS::CodePipeline::Webhook` resource to create a webhook that connects your pipeline to an external event, such as a GitHub source repository change, which triggers your pipeline to start every time the external event occurs\.  | July 5, 2018 | 
| [Updated resource](#ReleaseHistory) | Added the following properties to AWS::EC2::VPCEndpoint: PrivateDnsEnabled, SecurityGroupIds, SubnetIds, and VpcEndpointType\. 

 [AWS::EC2::VPCEndpoint](aws-resource-ec2-vpcendpoint.md)   
Use the `PrivateDnsEnabled` property to indicate whether to associate a private hosted zone with the specified VPC\.  
Use the `SecurityGroupIds` property to specify the ID of one or more security groups to associate with the endpoint network interface\.  
Use the `SubnetIds` property to specify the ID of one or more subnets in which to create an endpoint network interface\.  
Use the `VpcEndpointType` property to specify the type of endpoint\.   | June 21, 2018 | 
| [New resources](#ReleaseHistory) | The following resources were added: AWS::EC2::VPCEndpointConnectionNotification and AWS::EC2::VPCEndpointService\. 

 [AWS::EC2::VPCEndpointConnectionNotification](aws-resource-ec2-vpcendpointconnectionnotification.md)   
Use the `AWS::EC2::VPCEndpointConnectionNotification` resource to create a connection notification for the specified VPC endpoint or VPC endpoint service\. 

 [AWS::EC2::VPCEndpointService](aws-resource-ec2-vpcendpointservice.md)   
Use the `AWS::EC2::VPCEndpointService` resource to create a VPC endpoint service configuration to which service consumers \(AWS accounts, IAM users, and IAM roles\) can connect\.  | June 21, 2018 | 
| [Updated resource](#ReleaseHistory) | Added the following property to AWS::ServiceDiscovery::Service: HealthCheckCustomConfig\. 

 [AWS::ServiceDiscovery::Service](aws-resource-servicediscovery-service.md)   
Use the `HealthCheckCustomConfig` property to specify information about an optional custom health check\.  | June 14, 2018 | 
| [New resources](#ReleaseHistory) | The following new resources were released: AWS::AmazonMQ::Broker and AWS::AmazonMQ::Configuration\.  

 [AWS::AmazonMQ::Broker](aws-resource-amazonmq-broker.md)   
Use the `AWS::AmazonMQ::Broker` resource to create a broker, add configuration changes or modify users for the specified broker, return information about the specified broker, or delete the specified broker\. 

 [AWS::AmazonMQ::Configuration](aws-resource-amazonmq-configuration.md)   
Use the `AWS::AmazonMQ::Configuration` resource to create a configuration, update the specified configuration, or return information about the specified configuration\.   | June 14, 2018 | 
| [New resource](#ReleaseHistory) | The following resource was released: : AWS::SSM::ResourceDataSync\. 

 [AWS::SSM::ResourceDataSync](aws-resource-ssm-resourcedatasync.md)   
Use the `AWS::SSM::ResourceDataSync` resource to create or delete a Resource Data Sync for Systems Manager Inventory\. You can use Resource Data Sync to send Inventory data collected from all of your Systems Manager managed instances to a single Amazon S3 bucket\.  | June 11, 2018 | 
| [New resource](#ReleaseHistory) | The following resource was released: AWS::EKS::Cluster\. 

 [AWS::EKS::Cluster](aws-resource-eks-cluster.md)   
Use the `AWS::EKS::Cluster` resource to create Amazon EKS clusters\.  | June 5, 2018 | 
| [Updated resource](#ReleaseHistory) | For the AWS::GuardDuty::Master resource, the InvitationId property is now optional\. 

 [AWS::GuardDuty::Master](aws-resource-guardduty-master.md)   
The `InvitationId` property is now optional\.  | May 31, 2018 | 
| [New resources](#ReleaseHistory) | The following new resources were released: AWS::SageMaker::Endpoint, AWS::SageMaker::EndpointConfig, AWS::SageMaker::Model, AWS::SageMaker::NotebookInstance, and AWS::SageMaker::NotebookInstanceLifecycleConfig\. 

 [AWS::SageMaker::Endpoint](aws-resource-sagemaker-endpoint.md)   
Use the `AWS::SageMaker::Endpoint` resource to create a SageMaker endpoint to host trained models\. 

 [AWS::SageMaker::EndpointConfig](aws-resource-sagemaker-endpointconfig.md)   
Use the `AWS::SageMaker::EndpointConfig` resource to create a configuration for an endpoint\. 

 [AWS::SageMaker::Model](aws-resource-sagemaker-model.md)   
Use the `AWS::SageMaker::Model` resource to create a model to host at an Amazon SageMaker endpoint\. 

 [AWS::SageMaker::NotebookInstance](aws-resource-sagemaker-notebookinstance.md)   
Use the `AWS::SageMaker::NotebookInstance` resource to create an Amazon SageMaker notebook instance\. 

 [AWS::SageMaker::NotebookInstanceLifecycleConfig](aws-resource-sagemaker-notebookinstancelifecycleconfig.md)   
Use the `AWS::SageMaker::NotebookInstanceLifecycleConfig` resource to specify shell scripts that run when you create or start a notebook instance\.  | May 31, 2018 | 
| [Stack sets now support customized execution roles](#ReleaseHistory) | Use customized execution roles in target accounts to control the stack resources that users or groups can include in their stack sets\. For more information, see [Prerequisites: Granting Permissions for Stack Set Operations](stacksets-prereqs.md)\.  | May 30, 2018 | 
| [Selective updates of stack instances](#ReleaseHistory) | Use the optional Accounts and Regions parameters to specify the accounts and regions in which to update stack instances during a stack set update operation\. For more information, see [UpdateStackSet](https://docs.aws.amazon.com/AWSCloudFormation/latest/APIReference/API_UpdateStackSet.html) in the *AWS CloudFormation API Reference*\. | May 30, 2018 | 
| [New resources](#ReleaseHistory) | The following new resources were released: AWS::Neptune::DBCluster, AWS::Neptune::DBClusterParameterGroup, AWS::Neptune::DBInstance, AWS::Neptune::DBParameterGroup, and AWS::Neptune::DBSubnetGroup\. 

 [AWS::Neptune::DBCluster](aws-resource-neptune-dbcluster.md)   
Use the `AWS::Neptune::DBCluster` resource to create an Amazon Neptune DB cluster\. 

 [AWS::Neptune::DBClusterParameterGroup](aws-resource-neptune-dbclusterparametergroup.md)   
Use the `AWS::Neptune::DBClusterParameterGroup` resource to create a DB cluster parameter group\. 

 [AWS::Neptune::DBInstance](aws-resource-neptune-dbinstance.md)   
Use the `AWS::Neptune::DBInstance` resource to create an Amazon Neptune database instance\. 

 [AWS::Neptune::DBParameterGroup](aws-resource-neptune-dbparametergroup.md)   
Use the `AWS::Neptune::DBParameterGroup` resource to create a custom parameter group for Amazon Neptune\. 

 [AWS::Neptune::DBSubnetGroup](aws-resource-neptune-dbsubnetgroup.md)   
Use the `AWS::Neptune::DBSubnetGroup` resource to create an Amazon Neptune database subnet group that contains subnets\.  | May 30, 2018 | 
| [Updated resources](#ReleaseHistory) | The following resources were updated: AWS::ApiGateway::RestApi, AWS::AutoScaling::AutoScalingGroup, AWS::AutoScaling::LaunchConfiguration, AWS::DirectoryService::MicrosoftAD, AWS::DynamoDB::Table, AWS::EC2::Instance, AWS::ECS::Service, AWS::ECS::TaskDefinition, AWS::Elasticsearch::Domain, AWS::IAM::Role, AWS::KinesisFirehose::DeliveryStream, AWS::Lambda::EventSourceMapping, AWS::Logs::MetricFilter, and AWS::SSM::Association\. 

 [AWS::ApiGateway::RestApi](aws-resource-apigateway-restapi.md)   
Use the `Policy` property to specify a policy document that contains the permissions for the specified RestAPI\. 

 [AWS::AutoScaling::AutoScalingGroup](aws-properties-as-group.md)   
Use the `ServiceLinkedRoleARN` property to specify the Amazon Resource Name \(ARN\) of the service\-linked role that the Auto Scaling group uses to call other AWS services on your behalf\. 

 [AWS::AutoScaling::LaunchConfiguration](aws-properties-as-launchconfig.md)   
Use the `LaunchConfigurationName` property to specify the name of the launch configuration\.  

 [AWS::DirectoryService::MicrosoftAD](aws-resource-directoryservice-microsoftad.md)   
Use the `Edition` property to specify the AWS Microsoft AD edition to use\. 

 [AWS::DynamoDB::Table](aws-resource-dynamodb-table.md)   
Use the `PointInTimeRecoverySpecification` property to specify the settings used to enable point in time recovery\. 

 [AWS::EC2::Instance](aws-properties-ec2-instance.md)   
Use the `LaunchTemplate` property to specify the launch template to use for an Amazon EC2 instance\. 

 [AWS::ECS::Service](aws-resource-ecs-service.md)   
Use the `ServiceRegistry` property type to specify the details of the service registry\. 

 [AWS::ECS::TaskDefinition](aws-resource-ecs-taskdefinition.md)   
Use the `HealthCheck` property type to specify a container health check\. 

 [AWS::Elasticsearch::Domain](aws-resource-elasticsearch-domain.md)   
Use the `EncryptionAtRestOptions` property type to specify whether the domain should encrypt data at rest, and if so, the AWS Key Management Service \(KMS\) key to use\. 

 [AWS::IAM::Role](aws-resource-iam-role.md)   
Use the `RoleId` attribute to have `Fn::GetAtt` return the stable and unique string identifying the role\.   
Use the `MaxSessionDuration` property to specify the maximum session duration \(in seconds\) for the specified role\. 

 [AWS::KinesisFirehose::DeliveryStream](aws-resource-kinesisfirehose-deliverystream.md)   
Use the `SplunkDestinationConfiguration` property to specify the configuration of a destination in Splunk for a Kinesis Data Firehose delivery stream\. 

 [AWS::Lambda::EventSourceMapping](aws-resource-lambda-eventsourcemapping.md)   
The `StartingPosition` property is no longer required\. 

 [AWS::Logs::MetricFilter](aws-resource-logs-metricfilter.md)   
In the [CloudWatch Logs MetricFilter MetricTransformation Property](aws-properties-logs-metricfilter-metrictransformation.md) property type, use the `DefaultValue` property to specify the value to emit when a filter pattern does not match a log event\.  

 [AWS::SSM::Association](aws-resource-ssm-association.md)   
Use the `OutputLocation` property to specify an Amazon S3 bucket where you want to store the results of an association request\.  | May 24, 2018 | 
| [New resources](#ReleaseHistory) | The following new resources were released: AWS::ServiceCatalog::AcceptedPortfolioShare, AWS::ServiceCatalog::CloudFormationProduct, AWS::ServiceCatalog::LaunchNotificationConstraint, AWS::ServiceCatalog::LaunchRoleConstraint, AWS::ServiceCatalog::LaunchTemplateConstraint, AWS::ServiceCatalog::Portfolio, AWS::ServiceCatalog::PortfolioPrincipalAssociation, AWS::ServiceCatalog::PortfolioProductAssociation, AWS::ServiceCatalog::PortfolioShare, AWS::ServiceCatalog::TagOption, and AWS::ServiceCatalog::TagOptionAssociation\. 

 [AWS::ServiceCatalog::AcceptedPortfolioShare](aws-resource-servicecatalog-acceptedportfolioshare.md)   
Use the `AWS::ServiceCatalog::AcceptedPortfolioShare` resource to accept an offer to share the specified portfolio for AWS Service Catalog\. 

 [AWS::ServiceCatalog::CloudFormationProduct](aws-resource-servicecatalog-cloudformationproduct.md)   
Use the `AWS::ServiceCatalog::CloudFormationProduct` resource to create a product for AWS Service Catalog\. 

 [AWS::ServiceCatalog::LaunchNotificationConstraint](aws-resource-servicecatalog-launchnotificationconstraint.md)   
Use the `AWS::ServiceCatalog::LaunchNotificationConstraint` resource to create a notification constraint for AWS Service Catalog\. 

 [AWS::ServiceCatalog::LaunchRoleConstraint](aws-resource-servicecatalog-launchroleconstraint.md)   
Use the `AWS::ServiceCatalog::LaunchRoleConstraint` resource to create a launch constraint for AWS Service Catalog\. 

 [AWS::ServiceCatalog::LaunchTemplateConstraint](aws-resource-servicecatalog-launchtemplateconstraint.md)   
Use the `AWS::ServiceCatalog::LaunchTemplateConstraint` resource to create a template constraint for AWS Service Catalog\. 

 [AWS::ServiceCatalog::Portfolio](aws-resource-servicecatalog-portfolio.md)   
Use the `AWS::ServiceCatalog::Portfolio` resource to create a portfolio for AWS Service Catalog\. 

 [AWS::ServiceCatalog::PortfolioPrincipalAssociation](aws-resource-servicecatalog-portfolioprincipalassociation.md)   
Use the `AWS::ServiceCatalog::PortfolioPrincipalAssociation` resource to associate a principal with a portfolio for AWS Service Catalog\. 

 [AWS::ServiceCatalog::PortfolioProductAssociation](aws-resource-servicecatalog-portfolioproductassociation.md)   
Use the `AWS::ServiceCatalog::PortfolioProductAssociation` resource to associate a product with a portfolio for AWS Service Catalog\. 

 [AWS::ServiceCatalog::PortfolioShare](aws-resource-servicecatalog-portfolioshare.md)   
Use the `AWS::ServiceCatalog::PortfolioShare` resource to share a portfolio for AWS Service Catalog\. 

 [AWS::ServiceCatalog::TagOption](aws-resource-servicecatalog-tagoption.md)   
Use the `AWS::ServiceCatalog::TagOption` resource to create a TagOption\. 

 [AWS::ServiceCatalog::TagOptionAssociation](aws-resource-servicecatalog-tagoptionassociation.md)   
Use the `AWS::ServiceCatalog::TagOptionAssociation` resource to associate a TagOption with a resource for AWS Service Catalog\.   | May 24, 2018 | 
| [AWS CloudFormation now creates S3 buckets with encryption enabled](#ReleaseHistory) | For Amazon S3 buckets that AWS CloudFormation creates to store uploaded stack templates, server\-side encryption is now enabled by default, thereby encrypting all objects stored in those buckets\. For more information, see [Selecting a Stack Template](cfn-using-console-create-stack-template.md)\.  | May 24, 2018 | 
| [New resource](#ReleaseHistory) | The following resource was released: AWS::Budgets::Budget\. 

 [AWS::Budgets::Budget](aws-resource-budgets-budget.md)   
Use the `AWS::Budgets::Budget` resource to create a budget\.  | May 22, 2018 | 
| [FIPS endpoints added](#ReleaseHistory) | AWS CloudFormation now offers new endpoints which use FIPS 140\-2 validated cryptographic modules in the following public US regions: US\-East\-1, US\-East\-2, US\-West\-1, and US\-West\-2\. See [Regions and Endpoints](https://docs.aws.amazon.com/general/latest/gr/rande.html#cfn_region) in the *[Amazon Web Services General Reference](https://docs.aws.amazon.com/general/latest/gr/)* for the new FIPS\-compliant endpoint URLs\. | May 17, 2018 | 
| [New resource](#ReleaseHistory) | The following resource was released: AWS::AutoScalingPlans::ScalingPlan\. 

 [AWS::AutoScalingPlans::ScalingPlan](aws-resource-autoscalingplans-scalingplan.md)   
Use the `AWS::AutoScalingPlans::ScalingPlan` resource to create a scaling plan for the scalable resources for your application\.  | May 9, 2018 | 
| [New resource](#ReleaseHistory) | The following resource was released: AWS::GuardDuty::Filter\. 

 [AWS::GuardDuty::Filter](aws-resource-guardduty-filter.md)   
Use the `AWS::GuardDuty::Filter` resource to create a filter for your GuardDuty findings\.  | May 8, 2018 | 
| [Updated resources](#ReleaseHistory) | The following resources were updated: AWS::AppSync::GraphQLApi and AWS::GuardDuty::Member\. 

 [AWS::AppSync::GraphQLApi](aws-resource-appsync-graphqlapi.md)   
Use the `OpenIDConnectConfig` property to specify the authorization configuration for using an OpenId Connect compliant service with your GraphQL endpoint\. 

 [AWS::GuardDuty::Member](aws-resource-guardduty-member.md)   
Use the `DisableEmailNotification` property to specify whether an email notification is to be sent to the accounts that you want to invite to GuardDuty as members\. When set to 'True', email notification is not sent to the invitees\.  | May 1, 2018 | 
| [New resource](#ReleaseHistory) | The following resource was released: AWS::ServiceCatalog::CloudFormationProvisionedProduct\.  

 [AWS::ServiceCatalog::CloudFormationProvisionedProduct](aws-resource-servicecatalog-cloudformationprovisionedproduct.md)   
Use the `AWS::ServiceCatalog::CloudFormationProvisionedProduct` resource to provision the specified product for AWS Service Catalog\.   | May 1, 2018 | 

## Earlier Updates<a name="release-history-earlier-updates"></a>

The following table describes important changes in each release of the AWS CloudFormation User Guide before May 2018\.


| Change | Release Date | Description | API Version | 
| --- | --- | --- | --- | 
|  Stack set naming convention  |  April 10, 2018  |  AWS CloudFormation stacks created using stack sets now follow a new naming convention, in which the stack name contains the stack set name\.  |  2010\-05\-15  | 
|  New resources  |  April 10, 2018  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html)  |  2010\-05\-15  | 
|  Updated resource  |  April 10, 2018  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html)  |  2010\-05\-15  | 
|  New resources  |  April 4, 2018  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html)  |  2010\-05\-15  | 
|  Stack sets now support customized administrator roles  |  March 29, 2018  |  Use customized administrator roles to control which users or groups can manage specific stack sets within the same administrator account\. For more information, see [Prerequisites: Granting Permissions for Stack Set Operations](stacksets-prereqs.md)\.  |  2010\-05\-15  | 
|  New resource  |  March 29, 2018  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html)  |  2010\-05\-15  | 
|  Updated resources  |  March 29, 2018  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html)  |  2010\-05\-15  | 
|  New `Fn::Cidr` intrinsic function  |  March 6, 2018  |  Returns the specified Cidr address block\. For more information, see [`Fn::Cidr`](intrinsic-function-reference-cidr.md)\.  |  2010\-05\-15  | 
|  New resources  |  March 6, 2018  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html)  | 2010\-05\-15 | 
|  Updated resources  |  March 6, 2018  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html)  |  2010\-05\-15  | 
|  Updated resource  |  February 19, 2018  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html)  |  2010\-05\-15  | 
|  Updated resource  |  February 8, 2018  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html)  |  2010\-05\-15  | 
| Updated resource |  February 5, 2018 |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html)  |  2010\-05\-15 | 
|  Updated resources |  January 23, 2018 |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html)  |  2010\-05\-15 | 
| Rollback triggers added to the AWS CloudFormation console\. |  January 15, 2018  | Rollback triggers enable you to have AWS CloudFormation monitor the state of your application during stack creation and updating, and to roll back that operation if the application breaches the threshold of any of the alarms you've specified\. For more information, see [Monitor and Roll Back Stack Operations](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-rollback-triggers.html)\. |  2010\-05\-15  | 
|  Updated resource |  January 12, 2018 |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html)  |  2010\-05\-15 | 
|  New resources  |  December 5, 2017  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html)  |  2010\-05\-15  | 
|  Updated resource |  December 5, 2017 |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html)  |  2010\-05\-15 | 
|  Updated resource |  December 1, 2017 |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html)  |  2010\-05\-15 | 
|  New resource  |  November 30, 2017  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html)  |  2010\-05\-15  | 
| Updated resources | November 29, 2017 |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html)  | 2010\-05\-15 | 
|  New resources  |  November 28, 2017  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html)  |  2010\-05\-15  | 
|  Updated resources  |  November 28, 2017  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html)  |  2010\-05\-15  | 
|  New `CodeDeployLambdaAliasUpdate` update policy  |  November 28, 2017  |  Use the `CodeDeployLambdaAliasUpdate` update policy to perform an AWS CodeDeploy deployment when the version changes on an `AWS::Lambda::Alias` resource\. For more information, see [UpdatePolicy](aws-attribute-updatepolicy.md)\.  |  2010\-05\-15  | 
|  New `SSM` parameter types  |  November 21, 2017  |  Use `SSM` parameter types to use existing parameters from Systems Manager Parameter Store\. **Note**: AWS CloudFormation doesn't currently support the `SecureString` type\. For more information, see [SSM Parameter Types](parameters-section-structure.md#aws-ssm-parameter-types)\.  |  2010\-05\-15  | 
|  New `ResolvedValue` field for `Parameter` data type  |  November 21, 2017  |  The `ResolvedValue` field returns the value that's used in the stack definition for an `SSM` parameter\. For more information, see the [ Parameter](https://docs.aws.amazon.com/AWSCloudFormation/latest/APIReference/API_Parameter.html) data type in the *AWS CloudFormation API Reference*\.  |  2010\-05\-15  | 
|  Updated resources  |  November 20, 2017  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html)  |  2010\-05\-15  | 
|  New `NoEcho` field for custom resource `Response` objects  |  November 20, 2017  |  You can now use the optional `NoEcho` field to mask the output of a custom resource\. For more information, see [Custom Resource Response Objects](crpg-ref-responses.md)\. The corresponding `noEcho` parameter is supported by the `send` method\. For more information, see [cfn\-response Module](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-lambda-function-code.html#cfn-lambda-function-code-cfnresponsemodule)\.  |  2010\-05\-15  | 
|  Stack instance overrides added for stack sets\.  |  November 17, 2017  |  AWS CloudFormation StackSets allows you to override parameter values in stack instances by account and region\. You can override parameter values when you create the stack instances, or when updating existing stack instances\. For more information, see [Override Parameters on Stack Instances](stackinstances-override.md)\.  |  2010\-05\-15  | 
|  Updated resource  |  November 15, 2017  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html)  |  2010\-05\-15  | 
|  StackSets now supports a maximum of 500 stack instances per stack set\.  |  November 6, 2017  |  You can now create up to a maximum of 500 stack instances per stack set\. For more information on AWS CloudFormation limits, see [AWS CloudFormation Limits](cloudformation-limits.md)\.  |  2010\-05\-15  | 
|  New resources  |  November 2, 2017  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html)  |  2010\-05\-15  | 
| Updated resources | November 2, 2017 |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html)  | 2010\-05\-15 | 
|  New resources  |  October 24, 2017  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html)  |  2010\-05\-15  | 
|  New resources  |  October 11, 2017  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html)  |  2010\-05\-15  | 
|  New resource  |  October 10, 2017  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html)  |  2010\-05\-15  | 
|  New resource  |  September 27, 2017  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html)  |  2010\-05\-15  | 
| Updated resources | September 27, 2017 |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html)  | 2010\-05\-15 | 
| Termination protection added for stacks\. | September 26, 2017 | Enabling termination protection on a stack prevents it from being accidentally deleted\. A user cannot delete a stack with termination protection enabled\. For more information, see [Protecting a Stack From Being Deleted](using-cfn-protect-stacks.md)\. | 2010\-05\-15 |
|  Changed default `umask` value from version 1\.4\-22 onwards  |  September 14, 2017  |  The default `umask` parameter value for the cfn\-hup\.conf configuration file is now `022`\. For more information, see [cfn\-hup](cfn-hup.md)\.  |   | 
| Updated resources | September 7, 2017 |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html)  | 2010\-05\-15 | 
|  Rollback triggers added to the AWS CloudFormation API  |  August 31, 2017  |  Rollback triggers enable you to have AWS CloudFormation monitor the state of your application during stack creation and updating, and to roll back that operation if the application breaches the threshold of any of the alarms you've specified\. For more information, see [ RollbackConfiguration](https://docs.aws.amazon.com/AWSCloudFormation/latest/APIReference/API_RollbackConfiguration.html) in the *AWS CloudFormation API Reference*\.  |  2010\-05\-15  | 
|  New `umask` parameter for cfn\-hup\.conf file  |  August 31, 2017  |  Use the `umask` parameter in the cfn\-hup\.conf configuration file to control file permissions used by the cfn\-hup daemon \(version 1\.4\-21\)\. For more information, see [cfn\-hup](cfn-hup.md)\.  |   | 
|  Updated resources for VPC Sizing support  |  August 29, 2017  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html)  |  2010\-05\-15  | 
|  Updated resources  |  August 23, 2017  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html)  |  2010\-05\-15  | 
|  New pseudo parameters  |  August 23, 2017  |  Use the `AWS::Partition` pseudo parameter to return the partition that a resource is in\. Use the `AWS::URLSuffix` pseudo parameter to return the suffix for a domain\. For more information, see [Pseudo Parameters Reference](pseudo-parameter-reference.md)\.  |  2010\-05\-15  | 
| New resources for DAX support | August 22, 2017 |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html)  | 2010\-05\-15 | 
|  New resources  |  August 18, 2017  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html)  |  2010\-05\-15  | 
|  Updated resources  |  August 18, 2017  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html) Added the `Arn` attribute to the `Fn::GetAtt` intrinsic function for the following resources: [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html)  |  2010\-05\-15  | 
|  Support for stack tags in AWS CodePipeline artifacts  |  August 18, 2017  |  You can now specify tags for stacks in template configuration files for use as artifacts for AWS CodePipeline pipelines\. Specified tags are applied to stacks created using the template configuration file\. For more information, see [AWS CloudFormation Artifacts](continuous-delivery-codepipeline-cfn-artifacts.md)\.  |  2010\-05\-15  | 
|  Create encrypted file systems  |  August 14, 2017  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html)  |  2010\-05\-15  | 
|  New resources for AWS Batch support  |  August 8, 2017  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html)  |  2010\-05\-15  | 
|  New resources for Amazon Kinesis Data Analytics support  |  July 28, 2017  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html)  |  2010\-05\-15  | 
|  Use StackSets to centrally manage stacks across accounts and regions  |  July 25, 2017  |  StackSets enables you to create, update, or delete stacks across multiple accounts and regions in a single operation\. Using an administrator account, you define and manage an AWS CloudFormation template, and use the template as the basis for provisioning stacks into selected target accounts across specified regions\. For more information about StackSets, see [Working with AWS CloudFormation StackSets](what-is-cfnstacksets.md)\.  |  2010\-05\-15  | 
|  View stack events by client request token  |  July 14, 2017  |  In the console, stack operations display the client request token on the **Events** tab\. All events triggered by a given stack operation are assigned the same client request token, which you can use to track operations\. For more information, see [Viewing Stack Data and Resources](cfn-console-view-stack-data-resources.md) and [StackEvent](https://docs.aws.amazon.com/AWSCloudFormation/latest/APIReference/API_StackEvent.html) in the *AWS CloudFormation API Reference*\.  |  2010\-05\-15  | 
|  Use stack quick\-create links  |  July 14, 2017  |  Use quick\-create links to get stacks up and running quickly\. You can specify the template URL, stack name, and template parameters to prepopulate a single **Create Stack Wizard** page\. For more information, see [Creating Quick\-Create Links for Stacks](cfn-console-create-stacks-quick-create-links.md)\.  |   | 
|  New resources for AWS Database Migration Service support  |  July 12, 2017  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html)  |  2010\-05\-15  | 
|  New resources  |  July 5, 2017  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html)  |  2010\-05\-15  | 
|  Updated resources  |  July 5, 2017  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html)  |  2010\-05\-15  | 
|  New resources  |  June 6, 2017  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html)  |  2010\-05\-15  | 
|  Updated resources  |  June 6, 2017  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html)  |  2010\-05\-15  | 
|  New resources  |  May 11, 2017  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html)  |  2010\-05\-15  | 
|  New resources  |  April 28, 2017  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html)  |  2010\-05\-15  | 
|  Updated resources  |  April 28, 2017  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html)  |  2010\-05\-15  | 
|  Edit templates in YAML and JSON using AWS CloudFormation Designer  |  April 6, 2017  |  When you create AWS CloudFormation templates using Designer, you can now edit your template in both YAML and JSON in the integrated editor\. You can also convert JSON templates to YAML and vice\-versa, depending on your preferred template authoring language\. For more information, see [What Is AWS CloudFormation Designer?](working-with-templates-cfn-designer.md)\.  |  2010\-05\-15  | 
|  New resource  |  April 6, 2017  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html)  |  2010\-05\-15  | 
|  `AWS::Include` transform  |  March 28, 2017  |  Use the `AWS::Include` transform to reference reusable snippets stored in an Amazon S3 bucket\. For more information, see [AWS::Include Transform](create-reusable-transform-function-snippets-and-add-to-your-template-with-aws-include-transform.md)\.  |  2010\-05\-15  | 
|  Peer your Amazon VPC with another account  |  March 28, 2017  |  You can now use AWS CloudFormation to peer your Amazon VPC with a VPC in another AWS account\. For more information, see [Walkthrough: Peer with an Amazon VPC in Another AWS Account](peer-with-vpc-in-another-account.md)\.  |  2010\-05\-15  | 
|  New resource  |  March 28, 2017  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html)  |  2010\-05\-15  | 
|  Updated resources  |  March 28, 2017  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html)  |  2010\-05\-15  | 
| New resources  | February 10, 2017 |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html)  | 2010\-05\-15 | 
|  New intrinsic function  |  January 17, 2017  |  Use the `Fn::Split` function to split a string into a list of string values\. For more information, see [`Fn::Split`](intrinsic-function-reference-split.md)\.  |  2010\-05\-15  | 
|  Console support for listing imports  |  January 17, 2017  |  Use the AWS CloudFormation console to see all of the stacks that are importing an exported output value\. For more information, see [Listing Stacks That Import an Exported Output Value](using-cfn-stack-imports.md)\.  |  2010\-05\-15  | 
|  Updated resources  |  January 17, 2017  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html)  |  2010\-05\-15  | 
|  New resources  |  December 01, 2016  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html)  |  2010\-05\-15  | 
|  Updated resources for IPv6 support  |  December 01, 2016  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html)  |  2010\-05\-15  | 
|  Resource specification  |  November 22, 2016  |  Use the AWS CloudFormation resource specification to builds tools that help you create AWS CloudFormation templates\. The specification is a machine\-readable, JSON\-formatted text file\. For more information, see [AWS CloudFormation Resource Specification](cfn-resource-specification.md)\.  |  2010\-05\-15  | 
|  New resources  |  November 22, 2016  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html)  |  2010\-05\-15  | 
|  Updated resources  |  November 22, 2016  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html)  |  2010\-05\-15  | 
|  List imports  |  November 22, 2016  |  List imports of an exported output value to track which AWS CloudFormation stacks are importing the value\. For more information, see [Listing Stacks That Import an Exported Output Value](using-cfn-stack-imports.md)\.  |  2010\-05\-15  | 
|  Transforms  |  November 17, 2016  |   Specify the AWS Serverless Application Model \(AWS SAM\) that AWS CloudFormation uses to process AWS SAM syntax for serverless applications\. For more information, see [Transform](transform-section-structure.md)\.  |  2010\-05\-15  | 
|  New resource  |  November 17, 2016  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html)  |  2010\-05\-15  | 
|  Updated resource  |  November 17, 2016  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html)  |  2010\-05\-15  | 
|  New CLI commands  |  November 17, 2016  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html)  |  2010\-05\-15  | 
|  Updated resource  |  November 03, 2016  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html)  |  2010\-05\-15  | 
|  List stack exports  |  November 03, 2016  |  Use the AWS CloudFormation console, API, or AWS CLI to see a list of all the exported output values for a region\. For more information, see [Exporting Stack Output Values](using-cfn-stack-exports.md)\.  |  2010\-05\-15  | 
|  Continuous delivery with stacks  |  November 03, 2016  |  Use AWS CodePipeline to build continuous delivery workflows with AWS CloudFormation stacks\. For more information, see [Continuous Delivery with AWS CodePipeline](continuous-delivery-codepipeline.md)\.  |  2010\-05\-15  | 
|  Skip resources during rollback  |  November 03, 2016  |  If you have a stack in the `UPDATE_ROLLBACK_FAILED` state, use the `ResourcesToSkip` parameter for the `ContinueUpdateRollback` action to skip resources that AWS CloudFormation can't rollback\. For more information, see the Troubleshooting section in [Update Rollback Failed](troubleshooting.md#troubleshooting-errors-update-rollback-failed)\.  |  2010\-05\-15  | 
|  Change sets enhancement  |  November 03, 2016  |  You can [create a new stack using a change set](cfn-console-create-stacks-changesets.md)\.  |  2010\-05\-15  | 
|  Updated resource  |  October 12, 2016  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html)  |  2010\-05\-15  | 
|  New resources  |  October 06, 2016  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html)  |  2010\-05\-15  | 
|  Updated resources  |  October 06, 2016  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html)  |  2010\-05\-15  | 
|  Cross\-stack reference enhancement  |  October 06, 2016  | Use intrinsic functions to customize the Name value of an [export](outputs-section-structure.md) or to refer to a value in the [ImportValue](intrinsic-function-reference-importvalue.md) function\. |  2010\-05\-15  | 
|  AWS CloudFormation service role  |  September 26, 2016  |  Use an AWS Identity and Access Management \(IAM\) service role for AWS CloudFormation stack operations\. AWS CloudFormation uses the role's credentials to make calls to stack resources on your behalf\. For more information, see [AWS CloudFormation Service Role](using-iam-servicerole.md)\.  |  2010\-05\-15  | 
|  New feature  |  September 19, 2016  |  You can use the `Export` output field and the `Fn::ImportValue` intrinsic function to have one stack refer to resource outputs in another stack\. For more information, see [Outputs](outputs-section-structure.md), [`Fn::ImportValue`](intrinsic-function-reference-importvalue.md), and [Walkthrough: Refer to Resource Outputs in Another AWS CloudFormation Stack](walkthrough-crossstackref.md)\.  |  2010\-05\-15  | 
|  YAML support  |  September 19, 2016  |  You can use the YAML format to author AWS CloudFormation templates\. YAML also allows you to, for example, add comments to your templates or use the short form for intrinsic functions\. For more information, see [AWS CloudFormation Template Formats](template-formats.md)\.  |  2010\-05\-15  | 
|  New intrinsic function  |  September 19, 2016  |  Use the `Fn::Sub` function to substitute variables in an input string with values that you specify\. For more information, see [`Fn::Sub`](intrinsic-function-reference-sub.md)\.  |  2010\-05\-15  | 
|  New resources  |  September 19, 2016  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html)  |  | 
|  Updated resources  |  September 19, 2016  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html)  |  2010\-05\-15  | 
|  New resources  |  August 11, 2016  |  Use the following Elastic Load Balancing Application load balancer resources to distribute incoming application traffic to multiple targets, such as EC2 instances, in multiple Availability Zones: [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html)  |  2010\-05\-15  | 
|  Updated resource  |  August 11, 2016  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html)  |  2010\-05\-15  | 
|  New resources  |  August 09, 2016  |  AWS CloudFormation added the following resources: [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html)  |  2010\-05\-15  | 
|  Updated resources  |  August 09, 2016  |  AWS CloudFormation updated the following resources: [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html)  |  2010\-05\-15  | 
| New resources |  July 20, 2016  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html)  |  2010\-05\-15  | 
|  Updated resources  |  July 20, 2016  |  AWS CloudFormation updated the following resources: [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html)  |  2010\-05\-15  | 
|  Auto Scaling group UpdatePolicy  |  June 9, 2016  |  For the `UpdatePolicy` attribute, use the `AutoScalingReplacingUpdate` property to specify whether an Auto Scaling group and the instances it contains are replaced when you update the Auto Scaling group\. During a replacement, AWS CloudFormation retains the old Auto Scaling group until it creates the new one successfully so that AWS CloudFormation can roll back to the old Auto Scaling group if the update fails\. For more information, see [UpdatePolicy](aws-attribute-updatepolicy.md)\.  |  2010\-05\-15  | 
|  New resource  |  June 9, 2016  |  AWS CloudFormation added the following resources: [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html)  |  2010\-05\-15  | 
|  Updated resources  |  June 9, 2016  |  AWS CloudFormation updated the following resources: [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html)  |  2010\-05\-15  | 
|  New resource  |  April 25, 2016  |  Use the [AWS::EC2::Host](aws-resource-ec2-host.md) resource to allocate a fully dedicated physical server for launching EC2 instances\.  |  2010\-05\-15  | 
|  Updated resources  |  April 25, 2016  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html)  |  2010\-05\-15  | 
|  New resources  |  April 18, 2016  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html)  |  2010\-05\-15  | 
|  New resources  |  March 31, 2016  |  Use the [AWS::Lambda::Alias](aws-resource-lambda-alias.md) resource to create aliases for your AWS Lambda functions and the [AWS::Lambda::Version](aws-resource-lambda-version.md) resource to create versions of your functions\.  |  2010\-05\-15  | 
|  Updated resources  |  March 31, 2016  |  AWS CloudFormation updated the following resources: [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html)  |  2010\-05\-15  | 
|  Change sets  |  March 29, 2016  |  Before updating stacks, use change sets to see how your changes might affect your running resources\. For more information, see [Updating Stacks Using Change Sets](using-cfn-updating-stacks-changesets.md)\.  |  2010\-05\-15  | 
|  New resources  |  March 15, 2016  |  Use the [AWS::GameLift::Alias](aws-resource-gamelift-alias.md), [AWS::GameLift::Build](aws-resource-gamelift-build.md), and [AWS::GameLift::Fleet](aws-resource-gamelift-fleet.md) resources to deploy multiplayer game servers in AWS\.  |  2010\-05\-15  | 
|  New resources  |  February 26, 2016  |  AWS CloudFormation added the following resources: [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html)  |  2010\-05\-15  | 
|  Updated resources  |  February 26, 2016  |  AWS CloudFormation updated the following resources: [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html)  |  2010\-05\-15  | 
|  Retain resources  |  February 26, 2016  |  For stacks in the `DELETE_FAILED` state, use the `RetainResources` parameter to retain resources that AWS CloudFormation can't delete\. For more information, see [Delete Stack Fails](troubleshooting.md#troubleshooting-errors-delete-stack-fails)\.  |  2010\-05\-15  | 
|  Update stack tags  |  February 26, 2016  |  You can add, modify, or remove stack tags when you update a stack\. For more information, see [AWS CloudFormation Stacks Updates](using-cfn-updating-stacks.md)\.  |  2010\-05\-15  | 
|  Continue rolling back failed update rollbacks  |  January 25, 2016  |  For a stack in the `UPDATE_ROLLBACK_FAILED` state, you can continue rolling back the update to get your stack in a working state\. That way, you can return the stack to its original settings and try to update it again\. For more information, see [Continue Rolling Back an Update](using-cfn-updating-stacks-continueupdaterollback.md)\.  |  2010\-05\-15  | 
|  New sample templates available for the Asia Pacific \(Seoul\) region\.  |  January 7, 2016  |  The following collection of AWS CloudFormation sample templates are for the ap\-northeast\-2 region: [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html) For more information, see [Sample Templates](cfn-sample-templates.md)\.  |  2010\-05\-15  | 
|  New resources  |  December 28, 2015  |  AWS CloudFormation added the following resources: [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html)  |  2010\-05\-15  | 
|  Resource updates  |  December 28, 2015  |  AWS CloudFormation updated the following resources: [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html)  |  2010\-05\-15  | 
|  Parameter grouping and sorting  |  December 3, 2015  |  Use the [AWS::CloudFormation::Interface](aws-resource-cloudformation-interface.md) metadata key to group and sort parameters in the AWS CloudFormation console when users create or update a stack with your template\.  |  2010\-05\-15  | 
|  Update policy attribute  |  December 3, 2015  |  For an Auto Scaling [update policy attribute](aws-attribute-updatepolicy.md), use the `MinSuccessfulInstancesPercent` property to specify the percentage of instances that must signal success for a successful update\.  |  2010\-05\-15  | 
|  New resources  |  December 3, 2015  |  AWS CloudFormation added the following resources: [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html)  |  2010\-05\-15  | 
|  Resources update  |  December 3, 2015  |  AWS CloudFormation updated the following resources: [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html)  |  2010\-05\-15  | 
|  Resource update  |  November 4, 2015  |  For the [AWS::EC2::Volume](aws-properties-ec2-ebs-volume.md) resource, use the `AutoEnableIO` property to automatically resume I/O operations if a volume's data becomes inconsistent\.   |  2010\-05\-15  | 
|  New resources  |  October 1, 2015  |  AWS CloudFormation added the following resources: [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html)  |  2010\-05\-15  | 
|  Resource updates  |  October 1, 2015  |  AWS CloudFormation updated the following resources: [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html)  |  2010\-05\-15  | 
|  IAM condition keys  |  October 1, 2015  |  For AWS Identity and Access Management \(IAM\) policies, use AWS CloudFormation\-specific condition keys to specify when an IAM policy takes effect\. For more information, see [Controlling Access with AWS Identity and Access Management](using-iam-template.md)\.  |  2010\-05\-15  | 
|  AWS CloudFormation Designer  |  October 1, 2015  |  Use [AWS CloudFormation Designer](working-with-templates-cfn-designer.md) to create and modify templates using a drag\-and\-drop interface\.  |  2010\-05\-15  | 
|  New resource  |  August 24, 2015  |  Use the [AWS::EC2::VPCEndpoint](aws-resource-ec2-vpcendpoint.md) resource to establish a private connection between your VPC and another AWS service\.  |  2010\-05\-15  | 
|  Resource updates  |  August 24, 2015  |  AWS CloudFormation updated the following resources: [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html)  |  2010\-05\-15  | 
|  Amazon S3 template URL  |  August 24, 2015  |  For versioning\-enabled buckets, you can specify a version ID in an Amazon S3 template URL when you create or update a stack, such as `https://s3.amazonaws.com/templates/myTemplate.template?versionId=123ab1cdeKdOW5IH4GAcYbEngcpTJTDW`\.  |  2010\-05\-15  | 
|  New resource  |  August 3, 2015  |  Use the [AWS::EFS::FileSystem](aws-resource-efs-filesystem.md) resource to create an Amazon Elastic File System \(Amazon EFS\) file system and the [AWS::EFS::MountTarget](aws-resource-efs-mounttarget.md) resource to create a mount point for a file system\.  |  2010\-05\-15  | 
|  Permission requirement change  |  June 11, 2015  |  When you create or update an [AWS::RDS::DBInstance](aws-properties-rds-database-instance.md) resource, you must now also have permission to call the `ec2:DescribeAccountAttributes` action\.  |  2010\-05\-15  | 
|  New resources  |  June 11, 2015  |  AWS CloudFormation added the following resources: [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html)  |  2010\-05\-15  | 
|  Resource updates  |  June 11, 2015  |  AWS CloudFormation updated the following resources: [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html)  |  2010\-05\-15  | 
|  New parameter types  |  May 19, 2015  |  Whenever you use the AWS CloudFormation console to create or update a stack, you can search for AWS\-specific parameter type values by ID, name, or Name tag value\. AWS CloudFormation also added support for the following AWS\-specific parameter types\. For more information, see [Parameters](parameters-section-structure.md)\. [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html)  |  2010\-05\-15  | 
|  New resources  |  April 16, 2015  |  AWS CloudFormation added the following resources: [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html)  |  2010\-05\-15  | 
|  Resource updates  |  April 16, 2015  |  AWS CloudFormation updated the following resources: [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html)  |  2010\-05\-15  | 
|  New template section  |  April 16, 2015  |  Add the [Metadata](metadata-section-structure.md) section to your templates to include arbitrary JSON objects that describe your templates, such as the design or implementation details\.  |  2010\-05\-15  | 
|  Resource update  |  April 8, 2015  |  For the [AWS::CloudFormation::CustomResource](aws-resource-cfn-customresource.md) resource, you can specify Lambda function Amazon Resource Names \(ARNs\) in the `ServiceToken` property\.  |  2010\-05\-15  | 
|  Amazon RDS update  |  December 24, 2014  |  AWS CloudFormation added two new properties for RDS DB instances\. You can associate an option group with a DB instance and specify the DB instance storage type\. For more information, see [AWS::RDS::DBInstance](aws-properties-rds-database-instance.md)\.  |  2010\-05\-15  | 
|  Elastic Load Balancing update  |  December 24, 2014  |  You can use the `ConnectionSettings` property to specify how long connections can remain idle\. For more information, see [AWS::ElasticLoadBalancing::LoadBalancer](aws-properties-ec2-elb.md)\.  |  2010\-05\-15  | 
|  Route 53 update  |  November 6, 2014  |  You can now provision and manage Route 53 [hosted zones](aws-resource-route53-hostedzone.md), [health checks](aws-resource-route53-healthcheck.md), [failover record sets](aws-properties-route53-recordset.md), and [geolocation record sets](aws-properties-route53-recordset-geolocation.md)\.  |  2010\-05\-15  | 
|  Auto Scaling rolling update enhancement  |  November 6, 2014  |  During an update, you can use the `WaitOnResourceSignals` flag to instruct AWS CloudFormation to wait for instances to signal success\. That way, AWS CloudFormation won't update the next batch of instances until the current batch is ready\. For more information, see [UpdatePolicy](aws-attribute-updatepolicy.md)\.  |  2010\-05\-15  | 
|  New VPC Fn:GetAtt attributes  |  November 6, 2014  |  Given a VPC ID, you can retrieve the default security group and network ACL for that VPC\. For more information, see [`Fn::GetAtt`](intrinsic-function-reference-getatt.md)\.  |  2010\-05\-15  | 
|  New AWS\-specific parameter types  |  November 6, 2014  |  You can specify AWS\-specific parameter types in your AWS CloudFormation templates\. In the AWS CloudFormation console, these parameter types provide a drop\-down list of valid values\. With the API or CLI, AWS CloudFormation can quickly validate values for these parameter types before creating or updating a stack\. For more information, see [Parameters](parameters-section-structure.md)\.  |  2010\-05\-15  | 
|  CreationPolicy attribute  |  November 6, 2014  |  With the CreationPolicy attribute, you can instruct AWS CloudFormation to wait until applications are ready on EC2 instances before proceeding with stack creation\. You can use a creation policy instead of a wait condition and wait condition handle\. For more information, see [CreationPolicy](aws-attribute-creationpolicy.md)\.  |  2010\-05\-15  | 
|  Amazon CloudFront forwarded values  |  September 29, 2014  |  For cache behaviors, you can forward headers to the origin\. See [CloudFront Distribution ForwardedValues](aws-properties-cloudfront-distribution-forwardedvalues.md)\.  |  2010\-05\-15  | 
|  AWS OpsWorks update  |  September 29, 2014  |  For Chef 11\.10, you can use the `ChefConfiguration` property to enable Berkshelf\. You can also use the AWS OpsWorks built\-in security groups with your AWS OpsWorks stacks\. For more information, see [AWS::OpsWorks::Stack](aws-resource-opsworks-stack.md)\.  |  2010\-05\-15  | 
|  Elastic Load Balancing tagging support  |  September 29, 2014  |  AWS CloudFormation tags Elastic Load Balancing load balancers with stack\-level tags\. You can also add your own tags to a load balancer\. See [AWS::ElasticLoadBalancing::LoadBalancer](aws-properties-ec2-elb.md)\.  |  2010\-05\-15  | 
|  Amazon Simple Notification Service topic policy update  |  September 29, 2014  |  You can now update Amazon SNS topic policies\. For more information, see [AWS::SNS::TopicPolicy](aws-properties-sns-policy.md)\.  |  2010\-05\-15  | 
|  RDS DB instance update  |  September 5, 2014  |  You can specify whether a DB instance is Internet\-facing by using the `PubliclyAccessible` property in the [AWS::RDS::DBInstance](aws-properties-rds-database-instance.md) resource\.  |  2010\-05\-15  | 
|  UpdatePolicy attribute update  |  September 05, 2014  |  You can specify an update policy for an Auto Scaling group that has an associated scheduled action\. For more information, see [UpdatePolicy](aws-attribute-updatepolicy.md)\.  |  2010\-05\-15  | 
|  Amazon CloudWatch support  |  July 10, 2014  |  You can use AWS CloudFormation to provision and manage Amazon CloudWatch Logs \(CloudWatch Logs\) log groups and metric filters\. For more information, see [AWS::Logs::LogGroup](aws-resource-logs-loggroup.md) or [AWS::Logs::MetricFilter](aws-resource-logs-metricfilter.md)\.  |  2010\-05\-15  | 
|  Amazon CloudFront distribution configuration update  |  June 17, 2014  |  You can specify additional CloudFront distribution configuration properties: [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html) For more information, see [AWS::CloudFront::Distribution](aws-resource-cloudfront-distribution.md)\.  |  2010\-05\-15  | 
|  EC2 instance update  |  June 17, 2014  |  You can specify whether an instance stops or terminates when you invoke the instance's operating system shutdown command\. For more information, see [AWS::EC2::Instance](aws-properties-ec2-instance.md)\.  |  2010\-05\-15  | 
|  EBS volume update  |  June 17, 2014  |  You can use encrypted EBS volumes with supported instance types\. For more information, see [AWS::EC2::Volume](aws-properties-ec2-ebs-volume.md)\.  |  2010\-05\-15  | 
|  New Amazon VPC peering connection  |  June 17, 2014  |  You can use AWS CloudFormation to create an Amazon Virtual Private Cloud \(Amazon VPC\) peering connection, which establishes a network connection between two VPCs\. For more information, see [AWS::EC2::VPCPeeringConnection](aws-resource-ec2-vpcpeeringconnection.md)\.  |  2010\-05\-15  | 
|  Amazon EC2 Auto Scaling group update  |  June 17, 2014  |  You can specify an existing cluster placement group in which to launch instances for an Amazon EC2 Auto Scaling group\. For more information, see [AWS::AutoScaling::AutoScalingGroup](aws-properties-as-group.md)\.  |  2010\-05\-15  | 
|  AWS CloudTrail support  |  June 17, 2014  |  AWS CloudFormation supports AWS CloudTrail, which can capture API calls made from your AWS account and publish the logs at a location you designate\. For more information, see [AWS::CloudTrail::Trail](aws-resource-cloudtrail-trail.md)\.  |  2010\-05\-15  | 
|  Update stack enhancements  |  May 12, 2014  |  AWS CloudFormation supports additional features for updating stacks: [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html) For more information, see [AWS CloudFormation Stacks Updates](using-cfn-updating-stacks.md)\.  |  2010\-05\-15  | 
|  Amazon Kinesis support  |  May 6, 2014  |  You can use AWS CloudFormation to create Amazon Kinesis streams that capture and transport data records from data sources\. For more information, see [AWS::Kinesis::Stream](aws-resource-kinesis-stream.md)\.  |  2010\-05\-15  | 
|  New S3 bucket properties  |  May 5, 2014  |  AWS CloudFormation supports additional S3 bucket properties: [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html) For more information, see [AWS::S3::Bucket](aws-properties-s3-bucket.md)\.  |  2010\-05\-15  | 
|  Amazon EC2 Auto Scaling support  |  May 5, 2014  |  AWS CloudFormation supports metrics collection for an Auto Scaling group\. For more information, see [AWS::AutoScaling::AutoScalingGroup](aws-properties-as-group.md)\.  |  2010\-05\-15  | 
|  `Fn::If` update  |  May 5, 2014  | You can use the Fn::If intrinsic function in the output section of a template\. For more information, see [Condition Functions](intrinsic-function-reference-conditions.md)\. |  2010\-05\-15  | 
|  API logging with AWS CloudTrail  |  April 2, 2014  |   You can use AWS CloudTrail \(CloudTrail\) to log AWS CloudFormation requests\. With CloudTrail you can get a history of AWS CloudFormation API calls for your account\. For more information, see [Logging AWS CloudFormation API Calls with AWS CloudTrail](cfn-api-logging-cloudtrail.md)\.   |  2010\-05\-15  | 
|  Elastic Load Balancing update  |  March 20, 2014  |  You can specify an access logging policy to capture information about requests made to your load balancer\. You can also specify a connection draining policy that describes how to handle in\-flight requests when instances are deregistered or become unhealthy\. For more information, see [AWS::ElasticLoadBalancing::LoadBalancer](aws-properties-ec2-elb.md)\.  |  2010\-05\-15  | 
|  AWS OpsWorks support  |  March 3, 2014  |  You can use AWS CloudFormation to provision and manage AWS OpsWorks stacks\. For more information, see [AWS::OpsWorks::Stack](aws-resource-opsworks-stack.md) or [AWS OpsWorks Template Snippets](quickref-opsworks.md)\.  |  2010\-05\-15  | 
|  Amazon S3 template size limit increase  |  February 18, 2014  |  You can specify template sizes up to 460,800 bytes in Amazon S3\.  |  2010\-05\-15  | 
|  Amazon Redshift support  |  February 10, 2014  |  You can use AWS CloudFormation to provision and manage Amazon Redshift clusters\. For more information, see [Amazon Redshift Template Snippets](quickref-redshift.md) or [AWS::Redshift::Cluster](aws-resource-redshift-cluster.md)\.  |  2010\-05\-15  | 
|  S3 buckets and bucket policies update  |  February 10, 2014  |  You can update some properties of the S3 bucket and bucket policy resources\. For more information, see [AWS::S3::Bucket](aws-properties-s3-bucket.md) or [AWS::S3::BucketPolicy](aws-properties-s3-policy.md)\.  |  2010\-05\-15  | 
|  Elastic Beanstalk environments and application versions update  |  February 10, 2014  |  You can update Elastic Beanstalk environment configurations and application versions\. For more information, see [AWS::ElasticBeanstalk::Environment](aws-properties-beanstalk-environment.md), [AWS::ElasticBeanstalk::ConfigurationTemplate](aws-resource-beanstalk-configurationtemplate.md), or [AWS::ElasticBeanstalk::ApplicationVersion](aws-properties-beanstalk-version.md)\.  |  2010\-05\-15  | 
|  Amazon SQS update  |  January 29, 2014  |  You can specify a dead letter queue for an Amazon SQS queue\. For more information, see [AWS::SQS::Queue](aws-properties-sqs-queues.md)\.  |  2010\-05\-15  | 
|  Auto Scaling scheduled actions  |  January 27, 2014  |  You can scale the number of EC2 instances in an Auto Scaling group based on a schedule\. By using a schedule, you can scale applications in response to predictable load changes\. For more information, see [AWS::AutoScaling::ScheduledAction](aws-resource-as-scheduledaction.md)\.  |  2010\-05\-15  | 
|  DynamoDB secondary indexes  |  January 27, 2014  |  You can create local and global secondary indexes for DynamoDB databases\. By using secondary indexes, you can efficiently access data with attributes other than the primary key\. For more information, see [AWS::DynamoDB::Table](aws-resource-dynamodb-table.md)\.  |  2010\-05\-15  | 
|  Auto Scaling update  |  January 2, 2014  |  You can specify an instance ID for an Auto Scaling group or launch configuration\. You can also specify additional Auto Scaling block device properties\. For more information, see [AWS::AutoScaling::AutoScalingGroup](aws-properties-as-group.md) or [AWS::AutoScaling::LaunchConfiguration](aws-properties-as-launchconfig.md)\.  |  2010\-05\-15  | 
|  Amazon SQS update  |  January 2, 2014  |  You can update SQS queues and specify additional properties\. For more information, see [AWS::SQS::Queue](aws-properties-sqs-queues.md)\.  |  2010\-05\-15  | 
|  Limit increases  |  January 2, 2014  |  You can specify up to 60 parameters and 60 outputs in your AWS CloudFormation templates\.  |  2010\-05\-15  | 
|  New console  |  December 19, 2013  |  The new [AWS CloudFormation console](https://console.aws.amazon.com/cloudformation/) adds features like auto\-refreshing stack events and alphabetical ordering of stack parameters\.  |  2010\-05\-15  | 
|  Cross\-zone load balancing  |  December 19, 2013  |  With cross\-zone load balancing, you can route traffic to back\-end instances across all Availability Zones \(AZs\)\. For more information, see [AWS::ElasticLoadBalancing::LoadBalancer](aws-properties-ec2-elb.md)\.  |  2010\-05\-15  |
|  AWS Elastic Beanstalk environment tiers  |  December 19, 2013  |  You can specify whether AWS Elastic Beanstalk provisions resources to support a web server or to handle background processing tasks\. For more information, see [AWS::ElasticBeanstalk::Environment](aws-properties-beanstalk-environment.md)\.  |  2010\-05\-15  | 
|  Resource names  |  December 19, 2013  |  You can assign names \(physical IDs\) to the following resources: [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html) For more information, see [Name Type](aws-properties-name.md)\.  |  2010\-05\-15  | 
|  VPN support  |  November 22, 2013  |  You can enable a virtual private gateway \(VGW\) to propagate routes to the routing tables of a VPC\. For more information, see [AWS::EC2::VPNGatewayRoutePropagation](aws-resource-ec2-vpn-gatewayrouteprop.md)\.  |  2010\-05\-15  | 
|  Conditionally create resources and assign properties  |  November 8, 2013  |  Using input parameters, you can control the creation and settings of designated stack resources by defining conditions in your AWS CloudFormation templates\. For example, you can use conditions to create stack resources for a production environment\. Using the same template, you can create similar stack resources with lower capacity for a test environment\. For more information, see [Condition Functions](intrinsic-function-reference-conditions.md)\.  |  2010\-05\-15  | 
|  Prevent accidental updates to stack resources  |  November 8, 2013  |  You can prevent stack updates that might result in unintentional changes to stack resources\. For example, if you have a stack with a database layer that should rarely be updated, you can set a stack policy that prevents most users from updating that database layer\. For more information, see [Prevent Updates to Stack Resources](protect-stack-resources.md)\.  |  2010\-05\-15  | 
|  Name resources  |  November 8, 2013  |  Instead of using AWS CloudFormation\-generated physical IDs, you can assign names to certain resources\. The following AWS CloudFormation resources support naming [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html) For more information, see [Name Type](aws-properties-name.md)\.  |  2010\-05\-15  | 
|  Assign custom resource types  |  November 8, 2013  |  In your templates, you can specify your own resource type for AWS CloudFormation custom resources \(`AWS::CloudFormation::CustomResource`\)\. By using your own custom resource type name, you can quickly identify the type of custom resources that you have in your stack\. For example, you can specify `"Type": "Custom::MyCustomResource"`\. For more information, see [AWS::CloudFormation::CustomResource](aws-resource-cfn-customresource.md)\.  |  2010\-05\-15  | 
|  Add pseudo parameter  |  November 8, 2013  |  You can now refer to the AWS AccountID inside AWS CloudFormation templates by referring to the `AWS::AccountID` pseudo parameter\. For more information, see [Pseudo Parameters Reference](pseudo-parameter-reference.md)\.  |  2010\-05\-15  | 
|  Specify stacks in IAM policies  |  November 8, 2013  |  You can allow or deny IAM users, groups, or roles to operate on specific AWS CloudFormation stacks\. For example, you can deny the delete stack action on a specific stack ID\. For more information, see [Controlling Access with AWS Identity and Access Management](using-iam-template.md)\.  |  2010\-05\-15  | 
|  Federation support  |  October 14, 2013  |  AWS CloudFormation supports temporary security credentials from IAM roles, which enable scenarios such as federation and single sign\-on to the AWS Management Console\. You can also make calls to AWS CloudFormation from EC2 instances without embedding long\-term security credentials by using IAM roles\. For more information about AWS CloudFormation and IAM, see [Controlling Access with AWS Identity and Access Management](using-iam-template.md)\.  |  2010\-05\-15  | 
|  Amazon RDS read replica support  |  September 24, 2013  |  You can now create Amazon RDS read replicas from a source DB instance\. For more information, see the `SourceDBInstanceIdentifier `property in the [AWS::RDS::DBInstance](aws-properties-rds-database-instance.md) resource\.  |  2010\-05\-15  | 
|  Associate public IP address with instances in an Auto Scaling group  |  September 19, 2013  |   You can now associate public IP addresses with instances in an Auto Scaling group\. For more information, see [AWS::AutoScaling::LaunchConfiguration](aws-properties-as-launchconfig.md)\.  |  2010\-05\-15  | 
|  Additional VPC support  |  September 17, 2013  |  AWS CloudFormation adds several enhancements to support VPC and VPN functionality [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html)  |  2010\-05\-15  | 
|  Redis and VPC security groups support for Amazon ElastiCache  |  September 3, 2013  |  You can now specify Redis as the cache engine for an Amazon ElastiCache \(ElastiCache\) cluster\. You can also now assign VPC security groups to ElastiCache clusters\. For more information, see [AWS::ElastiCache::CacheCluster](aws-properties-elasticache-cache-cluster.md)\.  |  2010\-05\-15  | 
|  Parallel stack creation, update and deletion, and nested stack updates   |  August 12, 2013  |  AWS CloudFormation now creates, updates, and deletes resources in parallel, improving the operations' performance\. If you update a top\-level template, AWS CloudFormation automatically updates nested stacks that have changed\. For more information, see [AWS CloudFormation Stacks Updates](using-cfn-updating-stacks.md)\.  |  2010\-05\-15  | 
|  VPC security groups can now be set in RDS DB instances  |  February 28, 2013  |  You can now assign VPC security groups to an RDS DB instance with AWS CloudFormation\. For more information, see the [VPCSecurityGroups](aws-properties-rds-database-instance.md#cfn-rds-dbinstance-vpcsecuritygroups) property in [AWS::RDS::DBInstance](aws-properties-rds-database-instance.md)\.  |  2010\-05\-15  | 
|  Rolling deployments for Amazon EC2 Auto Scaling groups  |  February 20, 2013  |  AWS CloudFormation now supports update policies on Amazon EC2 Auto Scaling groups, which describe how instances in the Amazon EC2 Auto Scaling group are replaced or modified when the Amazon EC2 Auto Scaling group adds or removes instances\. You can modify these settings at stack creation or during a stack update\. For more information and an example, see [UpdatePolicy](aws-attribute-updatepolicy.md)\.  |  2010\-05\-15  | 
|  Cancel and rollback action for stack updates  |  February 20, 2013  |  AWS CloudFormation supports the ability to cancel a stack update\. The stack must be in the UPDATE\_IN\_PROGRESS state when the update request is made\. More information is available in the following topics: [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html)  |  2010\-05\-15  | 
|  EBS\-optimized instances for Amazon EC2 Auto Scaling groups  |  February 20, 2013  |  You can now provision EBS\-optimized instances in Amazon EC2 Auto Scaling groups for dedicated throughput to Amazon Elastic Block Store \(Amazon EBS\) in autoscaled instances\. The implementation is similar to that of the previously released support for optimized Amazon EBS EC2 instances\. For more information, see the new `EbsOptimized` property in [AWS::AutoScaling::LaunchConfiguration](aws-properties-as-launchconfig.md)\.  |  2010\-05\-15  | 
|  New documentation  |  December 21, 2012  |  [AWS::EC2::Instance](aws-properties-ec2-instance.md) now provides a `BlockDeviceMappings` property to allow you to set block device mappings for your EC2 instance\. With this change, two new types have been added: [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html)  |  2010\-05\-15  | 
|  New documentation  |  December 21, 2012  |  New sections have been added to describe the procedures for creating and viewing stacks using the recently redesigned AWS Management Console\. You can find them here: [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html)  |  2010\-05\-15  | 
|  New documentation  |  November 15, 2012  |  Information about custom resources is provided in the following topics: [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html)  |  2010\-05\-15  | 
|  Updated documentation  |  November 15, 2012  |  AWS CloudFormation now supports specifying provisioned I/O operations per second \(IOPS\) for RDS DB instances\. You can set this value from 1000–10,000 in 1000 IOPS increments by using the new [Iops](aws-properties-rds-database-instance.md#cfn-rds-dbinstance-iops) property in [AWS::RDS::DBInstance](aws-properties-rds-database-instance.md)\. For more information about specifying IOPS for RDS DB instances, see [Provisioned IOPS](http://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/RDSFAQ.PIOPS.html) in the *Amazon Relational Database Service User Guide*\.  |  2010\-05\-15  | 
|  New and updated documentation  |  August 27, 2012  |  Topics have been reorganized to more clearly provide specific information about using the AWS Management Console and using the AWS CloudFormation command\-line interface \(CLI\)\. Information about tagging AWS CloudFormation stacks has been added, including new guides and updated reference topics: [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html) New information about [working with Windows stacks](cfn-windows-stacks.md): [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html) New topic: [Using Regular Expressions in AWS CloudFormation Templates](cfn-regexes.md)\.  |  2010\-05\-15  | 
|  New feature  |  April 25, 2012  |  AWS CloudFormation now provides full support for Virtual Private Cloud \(VPC\) security with Amazon EC2 You can now create and populate an entire VPC with every type of VPC resource \(subnets, gateways, network ACLs, route tables, and so forth\) using a single AWS CloudFormation template\. Templates that demonstrate new VPC features can be downloaded: [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html) Documentation for the following resource types has been updated: [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html) New resource types have been added to the documentation: [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html)  |  2010\-05\-15  | 
|  New feature  |  April 13, 2012  |  AWS CloudFormation now allows you to add or remove elements from a stack when updating it\. [AWS CloudFormation Stacks Updates](using-cfn-updating-stacks.md) has been updated, and a new section has been added to the walkthrough: [Change the Stack's Resources](updating.stacks.walkthrough.md#update.walkthrough.change.resources), which describes how to add and remove resources when updating the stack\.  |  2010\-05\-15  | 
|  New feature  |  February 2, 2012  |  AWS CloudFormation now provides support for resources in an existing Amazon Virtual Private Cloud \(Amazon VPC\)\. With this release, you can: [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html)  |  2010\-05\-15  | 
|  New feature  |  February 2, 2012  |  You can now update properties for the following resources in an existing stack: [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html) For a complete list of updatable resources and details about what to consider when updating a stack, see [AWS CloudFormation Stacks Updates](using-cfn-updating-stacks.md)\.  |  2010\-05\-15  | 
|  Restructured guide  |  February 2, 2012  |  Reorganized existing sections into new sections: [Working with AWS CloudFormation Templates](template-guide.md) and **Managing Stacks**\. Moved [Template Reference](template-reference.md) to the top level of the Table of Contents\. Moved [Estimating the Cost of Your AWS CloudFormation Stack](using-cfn-paying.md) to the Getting Started section\.  |  2010\-05\-15  | 
|  New content  |  February 2, 2012  |  Added three new sections: [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html)  |  2010\-05\-15  | 
|  New feature  |  May 26, 2011  |  AWS CloudFormation now provides the aws cloudformation list\-stacks command, which enables you to list stacks filtered by stack status\. Deleted stacks can be listed for up to 90 days after they have been deleted\.  For more information, see [Describing and Listing Your Stacks](using-cfn-describing-stacks.md)\.  |  2010\-05\-15  | 
|  New features  |  May 26, 2011  |  The aws cloudformation describe\-stack\-resources and aws cloudformation get\-template commands now enable you to get information from stacks that have been deleted for 90 days after they have been deleted\.  For more information, see [Listing Resources](using-cfn-listing-stack-resources.md) and [Retrieving a Template](using-cfn-get-template.md)\.  |  2010\-05\-15  | 
|  New link  |  March 1, 2011  |  AWS CloudFormation endpoint information is now located in the AWS General Reference\. For more information, go to Regions and Endpoints in [Amazon Web Services General Reference](http://docs.aws.amazon.com/general/latest/gr/index.html?rande.html)\.  |  2010\-05\-15  | 
|  Initial release  |  February 25, 2011  |  This is the initial public release of AWS CloudFormation\.  |  2010\-05\-15  | 