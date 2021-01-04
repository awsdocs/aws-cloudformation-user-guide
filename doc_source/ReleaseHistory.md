# Release history<a name="ReleaseHistory"></a>

The following table describes important changes in each release of the AWS CloudFormation User Guide after May 2018\. For notification about updates to this documentation, you can subscribe to an [RSS feed](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-cloudformation-release-notes.rss)\.

| Change | Description | Date | 
| --- |--- |--- |
| [AWS::ServiceCatalog transform added](#ReleaseHistory) | The AWS::ServiceCatalog transform enables Service Catalog users to reference outputs from an existing Service Catalog provisioned product in their CloudFormation template\.For more details, see [AWS::ServiceCatalog transform](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/transform-aws-servicecatalog.html)\. | December 23, 2020 | 
| [New resource](AWS_MWAA.md) | The following resource was added AWS::MWAA::Environment 

 [AWS::MWAA::Environment](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-mwaa-environment.html)   
Use the `AWS::MWAA::Environment` resource to create an environment in Amazon Managed Workflows for Apache Airflow \(MWAA\)\.  | December 21, 2020 | 
| [Updated resources](AWS_EC2.md) | The following resources were updated: AWS::EC2::Instance, AWS::EC2::SpotFleet, AWS::EC2::Volume\. 

 [AWS::EC2::Instance](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ec2-instance.html)   
Use the `EnclaveOptions` property to indicate whether the instance is enabled for AWS Nitro Enclaves\. 

 [AWS::EC2::SpotFleet SpotCapacityRebalance](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ec2-spotfleet-spotcapacityrebalance.html)   
Use the `SpotCapacityRebalance` property when Amazon EC2 emits a signal that your Spot Instance is at an elevated risk of being interrupted\. 

 [AWS::EC2::SpotFleet SpotMaintenanceStrategies](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ec2-spotfleet-spotmaintenancestrategies.html)   
Use the `SpotMaintenanceStrategies` property to manage your Spot Instances that are at an elevated risk of being interrupted\. \. 

 [AWS::EC2::Volume](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ec2-ebs-volume.html)   
Use the `Throughput` property to specify the throughput that the volume supports, in MiB/s\.  | December 18, 2020 | 
| [Updated resources](AWS_ECR.md) | The following resources were updated: AWS::ECR::PublicRepository 

 [AWS::ECR::PublicRepository](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ecr-public-repository.html)   
Use the `PublicRepository` property to create or update a public repository\.  | December 18, 2020 | 
| [Updated resources](AWS_ECS.md) | The following resources were updated: AWS::ECS::Service 

 [AWS::ECS::Service](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ecs-service.html)   
Use the `DeploymentCircuitBreaker` property to enable the deployment circuit breaker for a service\.  | December 18, 2020 | 
| [Updated resources](AWS_ElastiCache.md) | The following resource was updated: AWS::ElastiCache::ReplicationGroup\. 

 [AWS::ElastiCache::ReplicationGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-elasticache-replicationgroup.html#cfn-elasticache-replicationgroup-usergroupids)   
Use the `UserGroupIds` property to associate a list of user groups with the replication group\.  | December 18, 2020 | 
| [Updated resource](AWS_Batch.md) | The following resource was updated: [AWS::Batch::JobDefinition](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-batch-jobdefinition.html) 

[AWS::Batch::JobDefinition](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-batch-jobdefinition.html)  
Use the `PlatformCapabilities` property to specify whether the job requires `EC2` or `FARGATE` resources\.  
Use the `PropagateTags` property to specify whether to propagate tags from the job definition to the corresponding Amazon ECS task\.  
In the [ContainerProperties](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-batch-jobdefinition-containerproperties.html) property type:  
+ Use the `FargatePlatformConfiguration` property to specify the Fargate platform version to use for jobs running on Fargate resources\.
+ Use the `NetworkConfiguration` property to specify the network configuration for jobs running on Fargate resources\. 

[AWS::Batch::JobDefinition](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-batch-jobdefinition.html)  
In the [ContainerProperties](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-batch-jobdefinition-containerproperties.html) property type, use the [FargatePlatformConfiguration](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-batch-jobdefinition-containerproperties.html#cfn-batch-jobdefinition-containerproperties-fargateplatformconfiguration) property to define the version of the Fargate platform used for the job\.  | December 18, 2020 | 
| [Updated resource](AWS_FSx.md) | The following resource was updated: AWS::FSx::FileSystem 

[AWS::FSx::FileSystem](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-fsx-filesystem.html)  
The `StorageCapacity` property was updated to `"Required": conditional`\.  
In the [WindowsConfiguration](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-fsx-filesystem-windowsconfiguration.html) property type, the `ThroughputCapacity` property was updated to `"Required": true`\.  | December 18, 2020 | 
| [Updated resource](AWS_S3.md) | The following resources were updated: AWS::S3::Bucket 

 [SourceSelectionCriteria](https://docs.aws.amazon.com/AmazonS3/latest/API/API_SourceSelectionCriteria.html)   
Use the `ReplicaModifications` property in `AWS::S3::Bucket SourceSelectionCriteria` to filter modifications on replicas\. 

 [Amazon S3 Bucket Keys](https://docs.aws.amazon.com/AmazonS3/latest/dev/bucket-key.html)   
Use the `BucketKeyEnabled` property to specify an S3 Bucket Key with default encryption using AWS Key Management Service\.  | December 18, 2020 | 
| [New resources](AWS_DevOpsGuru.md) | The following resources were added: `AWS::DevOpsGuru::NotificationChannel`, `AWS::DevOpsGuru::AWS::DevOpsGuru::ResourceCollection` 

 [AWS::DevOpsGuru::NotificationChannel](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-devopsguru-notificationchannel.html)   
Use the `AWS::DevOpsGuru::NotificationChannel` resource to add a notification channel to Amazon DevOps Guru\. The notification channel is used to notify you about important events\. For example, the creation of an insight or a change in an insight's severity\. 

 [AWS::DevOpsGuru::ResourceCollection](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-devopsguru-resourcecollection.html)   
Use the `AWS::DevOpsGuru::ResourceCollection` resource to specify a collection of resources in your account that you want Amazon DevOps Guru to analyze\. The specified resources are analyzed to generate insights that contain recommendations, related metrics, and operational data to help you improve the performance of your operational solutions\.  | December 18, 2020 | 
| [New resources](AWS_EC2.md) | The following resources were added: AWS::EC2::NetworkInsightsPath and AWS::EC2::NetworkInsightsAnalysis\. 

 [AWS::EC2::NetworkInsightsPath](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-networkinsightspath.html)   
Use the `NetworkInsightsPath` property to specify a path to analyze for reachability\. 

 [AWS::EC2::NetworkInsightsAnalysis](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-networkinsightsanalysis.html)   
Use the `NetworkInsightsAnalysis` property to specify a network insights analysis\.  | December 18, 2020 | 
| [New resources](AWS_ElastiCache.md) | The following resources were added: AWS::ElastiCache::User and AWS::ElastiCache::UserGroup\. 

 [AWS::ElastiCache::User](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-elasticache-user.html)   
For Redis engine version 6\.x onwards: Creates a Redis user\. For more information, see [Using Role Based Access Control \(RBAC\)](red-ug/Clusters.RBAC.html)  

 [AWS::ElastiCache::UserGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-elasticache-usergroup.html)   
For Redis engine version 6\.x onwards: Creates a Redis user group\. For more information, see [Using Role Based Access Control \(RBAC\)](/AmazonElastiCache/latest/red-ug/Clusters.RBAC.html)  | December 18, 2020 | 
| [New resources](AWS_IoTWireless.md) | The following resources were added: 

AWS::IoTWireless::Destination  
 Use the `Destination` resource to specify a destination for a wireless device to use\.  

AWS::IoTWireless::DeviceProfile  
 Use the `DeviceProfile` resource to specify a device profile for a wireless device to use\.  

AWS::IoTWireless::ServiceProfile  
 Use the `ServiceProfile` resource to specify a service profile for a wireless device to use\.  

AWS::IoTWireless::WirelessDevice  
 Use the `WirelessDevice` resource to specify a wireless device in an AWS IoT Core for LoRaWAN solution\.  

AWS::IoTWireless::WirelessGateway  
 Use the `WirelessGateway` resource to specify a wireless gateway in an AWS IoT Core for LoRaWAN solution\.   | December 18, 2020 | 
| [New resources](AWS_LicenseManager.md) | The following resources were added: AWS::LicenseManager::Grant and AWS::LicenseManager::License\. 

 [AWS::LicenseManager::Grant](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-licensemanager-grant.html)   
Use the `AWS::LicenseManager::Grant` resource to specify a grant in the AWS License Manager service\. 

 [AWS::LicenseManager::License](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-licensemanager-license.html)   
Use the `AWS::LicenseManager::License` resource to specify a granted license in the AWS License Manager service\.  | December 18, 2020 | 
| [New resources](AWS_SageMaker.md) | The following resources were added: AWS::SageMaker::DataQualityJobDefinition, AWS::SageMaker::Device, AWS::SageMaker::DeviceFleet, AWS::SageMaker::ModelBiasJobDefinition, AWS::SageMaker::ModelExplainabilityJobDefinition, AWS::SageMaker::ModelQualityJobDefinition, AWS::SageMaker::ModelPackageGroup, and AWS::SageMaker::Pipeline\. 

 [AWS::SageMaker::DataQualityJobDefinition](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-sagemaker-dataqualityjobdefinition.html)   
Use the `AWS::SageMaker::DataQualityJobDefinition` resource to create a monitoring job that monitors drift in data quality\. 

 [AWS::SageMaker::Device](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-sagemaker-device.html)   
Use the `AWS::SageMaker::Device` resource to register your Devices against an existing SageMaker Edge Manager DeviceFleet\. Each device must be listed individually in the CFN specification\. 

 [AWS::SageMaker::DeviceFleet](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-sagemaker-devicefleet.html)   
Use the `AWS::SageMaker::DeviceFleet` resource to create a DeviceFleet that manages your SageMaker Edge Manager Devices\. You must register your devices against the `DeviceFleet` separately\. 

 [AWS::SageMaker::ModelBiasJobDefinition](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-sagemaker-modelbiasjobdefinition.html)   
Use the `AWS::SageMaker::ModelBiasJobDefinition` resource to create a monitoring job that monitors potential bias in your model\. 

 [AWS::SageMaker::ModelExplainabilityJobDefinition](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-sagemaker-modelexplainabilityjobdefinition.html)   
Use the `AWS::SageMaker::ModelExplainabilityJobDefinition` resource to create a monitoring job that monitors feature attribution drift in your model\. 

 [AWS::SageMaker::ModelQualityJobDefinition](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-sagemaker-modelqualityjobdefinition.html)   
Use the `AWS::SageMaker::ModelQualityJobDefinition` resource to create a monitoring job that monitors quality drift in your model\. 

 [AWS::SageMaker::ModelPackageGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-sagemaker-modelpackagegroup.html)   
Use the `AWS::SageMaker::ModelPackageGroup` resource to create a a group of related models\. 

 [AWS::SageMaker::Pipeline](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-sagemaker-pipeline.html)   
Use the `AWS::SageMaker::Pipeline` resource to specify shell scripts that run when you create and/or start a SageMaker Pipeline\. For information about SageMaker Pipelines, see [SageMaker Pipelines](https://docs.aws.amazon.com/sagemaker/latest/dg/pipelines.html) in the *Amazon SageMaker Developer Guide*\.  | December 18, 2020 | 
| [New resources](#ReleaseHistory) | The following resources were added: AWS::CloudFormation::ModuleDefaultVersion and AWS::CloudFormation::ModuleVersion\. 

 [AWS::CloudFormation::ModuleDefaultVersion](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-cloudformation-moduledefaultversion.html)   
Use the `AWS::CloudFormation::ModuleDefaultVersion` resource to specify the default version of a module, which will be used in CloudFormation operations for this account and region\. 

 [AWS::CloudFormation::ModuleVersion](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-cloudformation-moduleversion.html)   
Use the `AWS::CloudFormation::ModuleVersion` resource to register the specified version of the module with the CloudFormation service, making it available for use in CloudFormation templates in this account and region\.  | December 18, 2020 | 
| [New resource](AWS_AuditManager.md) | The following resource was added: AWS::AuditManager::Assessment 

 [AWS::AuditManager::Assessment](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-auditmanager-assessment.html)   
Use the `AWS::AuditManager::Assessment` resource to specify a new assessment in AWS Audit Manager\.  | December 18, 2020 | 
| [New resource](AWS_GreengrassV2.md) | The following resources were added: AWS::GreengrassV2::ComponentVersion\. 

 [AWS::GreengrassV2::ComponentVersion](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-greengrassv2-componentversion.html)   
Use the `AWS::GreengrassV2::ComponentVersion` resource to create a new component version in AWS IoT Greengrass\.  | December 18, 2020 | 
| [New resource](AWS_IoT.md) | The following resource is new: AWS::IoT::TopicRuleDestination 

 [AWS::IoT::TopicRuleDestination](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-iot-topicruledestination.html)   
Use the `AWS::IoT::TopicRuleDestination` to specify a topic rule destination\.  | December 18, 2020 | 
| [New resource](AWS_IoTSiteWise.md) | The following resources were added: AWS::IoTSitewise::AccessPolicy, AWS::IoTSiteWise::Dasboard, AWS::IoTSiteWise::Portal, and AWS::IoTSiteWise::Project\. 

 [AWS::IoTSiteWise::AccessPolicy](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-iotsitewise-accesspolicy.html)   
Use the `AWS::IoTSiteWise::AccessPolicy` resource to create a new access policy in AWS IoT SiteWise\. 

 [AWS::IoTSiteWise::Dasboard](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-iotsitewise-dashboard.html)   
Use the `AWS::IoTSiteWise::Dasboard` resource to create a new dashboard in AWS IoT SiteWise\. 

 [AWS::IoTSiteWise::Portal](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-iotsitewise-portal.html)   
Use the `AWS::IoTSiteWise::Portal` resource to create a new portal in AWS IoT SiteWise\. 

 [AWS::IoTSiteWise::Project](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-iotsitewise-project.html)   
Use the `AWS::IoTSiteWise::Project` resource to create a new project in AWS IoT SiteWise\.  | December 18, 2020 | 
| [New resource](AWS_Lambda.md) | The following resources were updated: AWS::Lambda::CreateEventSourceMapping and AWS::Lambda::Function\. 

 [AWS::Lambda::EventSourceMapping](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-lambda-eventsourcemapping.html#cfn-lambda-eventsourcemapping)   
Use the `TumblingWindowInSeconds` property to set the window size for SQS event sources\.  
Lambda now supports a Self\-Managed Apache Kafka cluster as an event source\. 

 [AWS::Lambda::Function](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-lambda-function.html)   
Lambda now supports functions deployed as container images\. Use the [ImageUri](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-lambda-function-code.html#cfn-lambda-function-code-imageuri) property to specify the container image location\.  
In the [Code](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-lambda-function-code.html) property type, new property `ImageUri` specifies the image to associate with your Lambda function\.  | December 18, 2020 | 
| [New resource](AWS_SSO.md) | The following resource was added: AWS::SSO::InstanceAccessControlAttributeConfiguration\.  

 [AWS::SSO::InstanceAccessControlAttributeConfiguration](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-sso-instanceaccesscontrolattributeconfiguration.html)   
Use the `AWS::SSO::InstanceAccessControlAttributeConfiguration` resource to configure attribute\-based access control \(ABAC\) in AWS SSO\.  | December 18, 2020 | 
| [Updated resource](AWS_EKS.md) | The following resource was updated to support specifying a capacity type for a node group: AWS::EKS::Nodegroup\. 

 [AWS::EKS::Nodegroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-eks-nodegroup.html)   
Use the `CapacityType` property to specify whether you want to use Spot or On\-Demand instance types for your node group\.  | December 17, 2020 | 
| [Updated resource](AWS_GameLift.md) | The following resource was updated: AWS::GameLift::MatchmakingConfiguration\. 

 [AWS::GameLift::MatchmakingConfiguration](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-gamelift-build.html)   
Use the `FlexMatchMode` property to specify that the matchmaker is for a standalone FlexMatch solution or for matchmaking with GameLift managed hosting\.  | November 24, 2020 | 
| [Updated resource](AWS_Lambda.md) | The following resource was updated: AWS::Lambda::CreateEventSourceMapping\. 

 [AWS::Lambda::EventSourceMapping\.BatchSize](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-lambda-eventsourcemapping.html#cfn-lambda-eventsourcemapping-batchsize)   
The `BatchSize` has been increased for standard SQS queues, and allows for the use of a `MaximumBatchingWindowInSeconds`\.  | November 24, 2020 | 
| [Modules](#ReleaseHistory) | Modules are a way for you to package resource configurations for inclusion across stack templates, in a transparent, manageable, and repeatable way\. Modules can encapsulate common service configurations and best practices as modular, customizable building blocks for you to include in your stack templates\. For more information, see [Using modules to encapsulate and reuse resource configurations](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/modules.html)\. | November 24, 2020 | 
| [New resource](AWS_Lambda.md) | The following resource was added: AWS::Lambda::CodeSigningConfig\. 

 [AWS::Lambda::CodeSigningConfig](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-lambda-codesigningconfig.html)   
Use the `CodeSigningConfig` resource to specify code\-signing capability to your Lambda functions\.  | November 23, 2020 | 
| [Updated resource](AWS_Amplify.md) | The following resource was updated: AWS::Amplify::App 

 [AWS::Amplify::App](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-amplify-app.html)   
Use the `CustomHeaders` property to declare custom headers for each HTTP request made to your Amplify Apps\.  | November 19, 2020 | 
| [Updated resource](AWS_EC2.md) | The following resources were updated: AWS::EC2::LaunchTemplate and AWS::EC2::ClientVpnEndpoint\. 

 [AWS::EC2::ClientVpnEndpoint](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-clientvpnendpoint.html)   
Use the `ClientConnectOptions` property to indicate whether client connect options are used for Client VPN\. 

 [AWS::EC2::LaunchTemplate](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-launchtemplate.html)   
Use the `AssociateCarrierIpAddress` property to indicates whether to associate a Carrier IP address with eth0 for a new network interface\. 

 [AWS::EC2::LaunchTemplate](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-launchtemplate.html)   
Use the `EnclaveOptions` property to indicate whether the instance is enabled for AWS Nitro Enclaves\. 

 [AWS::EC2::LaunchTemplate](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-launchtemplate.html)   
Use the `NetworkCardIndex` property to specify the network card index\.  | November 19, 2020 | 
| [Updated resource](AWS_Events.md) | The following resource was upded: AWS::Events::EventBusPolicy\. 

 [AWS::Events::EventBusPolicy](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-events-eventbuspolicy.html)   
Added the `Statement` property\. Use the `Statement` property to add a statement to the policy attached to an event bus\.  | November 19, 2020 | 
| [Updated resource](AWS_KMS.md) | The following resource was updated: AWS::KMS::Key\. 

 [AWS::KMS::Key](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-kms-key.html)   
Added support for asymmetric CMKs, including the `KeySpec` property and the SIGN\_VERIFY value for the `KeyUsage` property\.  | November 19, 2020 | 
| [Update resource](AWS_CloudFront.md) | The following resource was updated: AWS::CloudFront::Distribution\. 

 [AWS::CloudFront::Distribution](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-cloudfront-distribution.html)   
In the [CacheBehavior](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-cloudfront-distribution-cachebehavior.html) and [DefaultCacheBehavior](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-cloudfront-distribution-defaultcachebehavior.html) property types, use the `TrustedKeyGroups` property to specify a list of the key groups that CloudFront can use to verify signed URLs or signed cookies\.  
For more information, see [Serving private content](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/PrivateContent.html) in the *Amazon CloudFront Developer Guide*\.  | November 19, 2020 | 
| [New resources](AWS_CloudFront.md) | The following resources were added: AWS::CloudFront::KeyGroup and AWS::CloudFront::PublicKey\. 

 [AWS::CloudFront::KeyGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-cloudfront-keygroup.html)   
Use the `AWS::CloudFront::KeyGroup` resource to create a key group in Amazon CloudFront to use with CloudFront signed URLs and signed cookies\.  
For more information, see [Serving private content](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/PrivateContent.html) in the *Amazon CloudFront Developer Guide*\. 

 [AWS::CloudFront::PublicKey](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-cloudfront-publickey.html)   
Use the `AWS::CloudFront::PublicKey` resource to create a public key in Amazon CloudFront to use with CloudFront signed URLs and signed cookies, or with field\-level encryption\.  
For more information, see [Serving private content](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/PrivateContent.html) or [Using field\-level encryption to help protect sensitive data](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/field-level-encryption.html) in the *Amazon CloudFront Developer Guide*\.  | November 19, 2020 | 
| [New resource](AWS_Glue.md) | The following resource was added: AWS::Glue::Registry 

 [AWS::Glue::Registry](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-glue-registry.html)   
Use the `AWS::Glue::Registry` resource to manage registries in the AWS Glue Schema Registry\.  | November 19, 2020 | 
| [New resource](AWS_Glue.md) | The following resource was added: AWS::Glue::Schema 

 [AWS::Glue::Schema](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-glue-schema.html)   
Use the `AWS::Glue::Schema` resource to manage schemas in the AWS Glue Schema Registry\.  | November 19, 2020 | 
| [New resource](AWS_Glue.md) | The following resource was added: AWS::Glue::SchemaVersion 

 [AWS::Glue::SchemaVersion](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-glue-schemaversion.html)   
Use the `AWS::Glue::SchemaVersion` resource to manage schema versions in the AWS Glue Schema Registry\.  | November 19, 2020 | 
| [New resource](AWS_Glue.md) | The following resource was added: AWS::Glue::SchemaVersionMetadata 

 [AWS::Glue::SchemaVersionMetadata](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-glue-schemaversionmetadata.html)   
Use the `AWS::Glue::SchemaVersionMetadata` resource to manage schema version metadata in the AWS Glue Schema Registry\.  | November 19, 2020 | 
| [New resource](AWS_NetworkFirewall.md) | The following resources were added: AWS::NetworkFirewall::Firewall, AWS::NetworkFirewall::FirewallPolicy, AWS::NetworkFirewall::LoggingConfiguration, and AWS::NetworkFirewall::RuleGroup 

 [AWS::NetworkFirewall::Firewall](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-networkfirewall-firewall.html)   
Use the `AWS::NetworkFirewall::Firewall` resource to specify stateful, managed, network firewall and intrusion detection and prevention for your VPCs in Amazon VPC\.  

 [AWS::NetworkFirewall::FirewallPolicy](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-networkfirewall-firewallpolicy.html)   
Use the `AWS::NetworkFirewall::FirewallPolicy` resource to specify the stateless and stateful network traffic filtering behavior for your `AWS::NetworkFirewall::Firewall`\.  

 [AWS::NetworkFirewall::LoggingConfiguration](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-networkfirewall-loggingconfiguration.html)   
Use the `AWS::NetworkFirewall::LoggingConfiguration` resource to specify the destinations and logging options for an `AWS::NetworkFirewall::Firewall`\.  

 [AWS::NetworkFirewall::RuleGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-networkfirewall-rulegroup.html)   
Use the `AWS::NetworkFirewall::RuleGroup` resource to specify a reusable collection of stateless or stateful network traffic filtering rules for use in your `AWS::NetworkFirewall::FirewallPolicy`\.   | November 19, 2020 | 
| [New resource](AWS_S3.md) | The following resource was added: AWS::S3::StorageLens 

 [S3 Storage Lens](https://docs.aws.amazon.com/AmazonS3/latest/dev/storage_lens.html)   
Use the `AWS::S3::StorageLens` resource to create a S3 Storage Lens configuration in the *Amazon Simple Storage Service*\.  | November 19, 2020 | 
| [Change sets for nested stacks](#ReleaseHistory) | With change sets for nested stacks you can preview the changes to your application and infrastructure resources across the entire nested stack hierarchy and proceed with updates when you’ve confirmed that all the changes are as intended\. For more information, see [Change sets for nested stacks](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/change-sets-for-nested-stacks.html)\. | November 18, 2020 | 
| [Updated resource](AWS_EC2.md) | The following resources were updated: AWS::EC2::Route and AWS::EC2::VPCEndpointService\. 

 [AWS::EC2::Route](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-route.html)   
Use the `VpcEndpointId` property to create a route to a Gateway Load Balancer endpoint\. 

 [AWS::EC2::VPCEndpointService](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-vpcendpointservice.html)   
Use the `GatewayLoadBalancerArns` property to specify a Gateway Load Balancer for your VPC endpoint service\.  | November 12, 2020 | 
| [Updated resource](AWS_Kendra.md) | The following resource was updated: AWS::Kendra::DataSource\. 

 [AWS::Kendra::DataSource](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-kendra-datasource.html)   
Use the new `CUSTOM` value to specify the custom data sources\.  | November 12, 2020 | 
| [New resources: AWS Glue DataBrew](AWS_DataBrew.md) | This is the first release of [AWS Glue DataBrew](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/AWS_DataBrew.html)\. | November 12, 2020 | 
| [New resource](AWS_AppMesh.md) | The following resource was updated: AWS::AppMesh::VirtualNode and AWS::AppMesh::VirtualGateway 

 [AWS::AppMesh::VirtualNode](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-appmesh-virtualnode.html)   
Use the `ConnectionPool` property to specify the type of connection pool for the listener\.  
Use the `VirtualNodeHttp2ConnectionPool` property to specify an http2 type of connection pool\.  
Use the `VirtualNodeGrpcConnectionPool` property to specify a grpc type of connection pool\.  
Use the `VirtualNodeConnectionPool` property to specify the type of virtual node connection pool\.  
Use the `VirtualNodeHttpConnectionPool` property to specify an http type of connection pool\.  
Use the `OutlierDetection` property to specify the type of outlier detection for the listener\.  
Use the `VirtualNodeTcpConnectionPool` property to specify an http2 type of connection pool\. 

 [AWS::AppMesh::VirtualGateway](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-appmesh-virtualgateway.html)   
Use the `ConnectionPool` property to specify the type of connection pool for the listener\.  
Use the `VirtualGatewayHttpConnectionPool` property to specify an http type of connection pool\.  
Use the `VirtualGatewayHttp2ConnectionPool` property to specify an http2 type of connection pool\.  
Use the `VirtualGatewayConnectionPool` property to specify the type of virtual gateway connection pool\.  
Use the `VirtualGatewayGrpcConnectionPool` property to specify a grpc type of connection pool\.  | November 12, 2020 | 
| [Updated resource](AWS_S3.md) | The following resources were updated: AWS::S3::Bucket 

 [IntelligentTieringConfiguration](https://docs.aws.amazon.com/AmazonS3/latest/dev/storage-class-intro.html#sc-dynamic-data-access)   
Use the `IntelligentTieringConfiguration` property to specify an S3 Intelligent\-Tiering configuration\. 

 [OwnershipControls](https://docs.aws.amazon.com/AmazonS3/latest/dev/about-object-ownership.html)   
Use the `OwnershipControls` property to specify object ownership on a bucket\.  | November 9, 2020 | 
| [Updated resources](AWS_CodeArtifact.md) | The following resources were updated: AWS::CodeArtifact::Domain and AWS::CodeArtifact::Repository\. 

 [AWS::CodeArtifact::Domain](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-codeartifact-domain.html)   
The `AWS::CodeArtifact::Domain` resource now supports tags\. 

 [AWS::CodeArtifact::Repository](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-codeartifact-repository.html)   
The `AWS::CodeArtifact::Repository` resource now supports tags\.  | November 5, 2020 | 
| [Updated resource](AWS_AutoScaling.md) | The following resource was updated: AWS::AutoScaling::AutoScalingGroup\. 

 [CapacityRebalance](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-as-group.html#cfn-as-group-capacityrebalance)   
Use the `CapacityRebalance` property to indicate whether Capacity Rebalancing is enabled\.  | November 5, 2020 | 
| [Updated resource](AWS_Batch.md) | The following resource was updated: [AWS::Batch::JobDefinition](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-batch-jobdefinition.html) 

[AWS::Batch::JobDefinition](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-batch-jobdefinition.html)  
In the [RetryStrategy](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-batch-jobdefinition-retrystrategy.html) property type, use the [EvaluateOnExit](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-batch-jobdefinition-retrystrategy.html#cfn-batch-jobdefinition-retrystrategy-evaluateonexit) property to specify a set of conditions to be met, and an action to take \(`RETRY` or `EXIT`\) if all conditions are met\.  | November 5, 2020 | 
| [Updated resource](AWS_EC2.md) | The following resource was updated: AWS::EC2::Route\. 

 [AWS::EC2::Route](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-route.html)   
Use the `CarrierGatewayId` property to create a route to a carrier gateway\.  | November 5, 2020 | 
| [Updated resource](AWS_Lambda.md) | The following resource was updated: AWS::Lambda::EventSourceMapping\. 

 [AWS::Lambda::EventSourceMapping](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-lambda-eventsourcemapping.html)   
Use the `Queues` property to specify the Amazon MQ queue to stream to a Lambda function\. Use the `Source access configuration` property to specify the Secrets Manager secret that stores your MQ broker credentials\.  | November 5, 2020 | 
| [New resource](AWS_Events.md) | The following new resource was added: AWS::Events::Archive\. 

 [AWS::Events::Archive](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-events-archive.html)   
Use the `Archive` resource to create an EventBridge archive to store events in\.  | November 5, 2020 | 
| [New resource](AWS_IoT.md) | The following resource was added: AWS::IoT::DomainConfiguration\. 

 [AWS::IoT::DomainConfiguration](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-iot-domainconfiguration.html)   
Use the `AWS::IoT::DomainConfiguration` resource to specify a domain configuration in AWS IoT Core\.  | November 5, 2020 | 
| [New resource](AWS_RDS.md) | The following resource was added: AWS::RDS::GlobalCluster\. 

 [AWS::RDS::GlobalCluster](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-rds-globalcluster.html)   
Use the `AWS::RDS::GlobalCluster` resource to create or update an Aurora global database cluster\.  | November 5, 2020 | 
| [New resource](AWS_SES.md) | The following resource was added: AWS::SES::ContactList 

 [AWS::SES::ContactList](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/AWS_SES.html)   
Use the `ContactList` resource to create a list that contains contacts that have subscribed to a particular topic or topics\.  | November 5, 2020 | 
| [Updated resource](AWS_AmazonMQ.md) | The following resources were updated: AWS::AmazonMQ::Broker, AWS::AmazonMQ::Configuration, AWS::AmazonMQ::ConfigurationAssociation 

 [AWS::AmazonMQ::Broker](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-amazonmq-broker.html)   
Amazon MQ now supports RabbitMQ broker engine\.  | November 4, 2020 | 
| [New resources](AWS_IVS.md) | The following resources were added: AWS::IVS::Channel, AWS::IVS::StreamKey, and AWS::IVS::PlaybackKeyPair 

 [AWS::IVS::Channel](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ivs-channel.html)   
Use the `AWS::IVS::Channel` resource to specify an Amazon IVS Channel, which stores configuration information related to your live stream\. 

 [AWS::IVS::StreamKey](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ivs-streamkey.html)   
Use the `AWS::IVS::StreamKey` resource to specify an Amazon IVS Stream Key, which creates a stream key for the specified IVS Channel\. Use a stream key to initiate a live stream\. 

 [AWS::IVS::PlaybackKeyPair](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ivs-playbackkeypair.html)   
Use the `AWS::IVS::PlaybackKeyPair` resource to specify an Amazon IVS PlaybackKeyPair, which is used to sign and validate a playback authorization token for a private channel\.  | October 29, 2020 | 
| [New resource](AWS_IoTSiteWise.md) | The following resources were added: AWS::IoTSitewise::Asset, AWS::IoTSiteWise::AssetModel, and AWS::IoTSiteWise::Gateway\. 

 [AWS::IoTSiteWise::Asset](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-iotsitewise-asset.html)   
Use the `AWS::IoTSiteWise::Asset` resource to create a new asset in AWS IoT SiteWise\. 

 [AWS::IoTSiteWise::AssetModel](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-iotsitewise-assetmodel.html)   
Use the `AWS::IoTSiteWise::AssetModel` resource to create a new asset model in AWS IoT SiteWise\. 

 [AWS::IoTSiteWise::Gateway](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-iotsitewise-gateway.html)   
Use the `AWS::IoTSiteWise::Gateway` resource to create a new gateway in AWS IoT SiteWise\.  | October 28, 2020 | 
| [Updated resource](AWS_AutoScaling.md) | The following resource was updated: AWS::AutoScaling::AutoScalingGroup\. 

 [AWS::AutoScaling::AutoScalingGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-as-group.html)   
Use the `NewInstancesProtectedFromScaleIn` property to specify whether newly launched instances are protected from termination by Amazon EC2 Auto Scaling when scaling in\.  | October 26, 2020 | 
| [Updated resources](AWS_AppStream.md) | The following resources were updated: `AWS::AppStream::Fleet` and `AWS::AppStream::ImageBuilder` 

 [AWS::AppStream::Fleet](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-appstream-fleet.html)   
Use the `IAMRoleArn` property to specify an ARN for the IAM role to apply to the fleet\.  
Use the `StreamView` property to specify the AppStream 2\.0 view that is displayed to your users when they stream from the fleet\. 

 [AWS::AppStream::ImageBuilder](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-appstream-imagebuilder.html)   
Use the `IAMRoleArn` property to specify an ARN for the IAM role to apply to the image builder\.  | October 22, 2020 | 
| [Updated resources](AWS_Batch.md) | The following resources were updated: [AWS::Batch::ComputeEnvironment](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-batch-computeenvironment.html), [AWS::Batch::JobDefinition](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-batch-jobdefinition.html), and [AWS::Batch::JobQueue](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-batch-jobqueue.html)\. 

[AWS::Batch::ComputeEnvironment](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-batch-computeenvironment.html)  
Use the `Tags` property to specify tags for the compute environment\. 

[AWS::Batch::JobDefinition](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-batch-jobdefinition.html)  
Use the `Tags` property to specify tags for the job definition\. 

[AWS::Batch::JobQueue](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-batch-jobqueue.html)  
Use the `Tags` property to specify tags for the job queue\.  | October 22, 2020 | 
| [Updated resource](AWS_AppSync.md) | The following resource was updated: AWS::AppSync::ApiKey\. 

 [AWS::AppSync::ApiKey](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-appsync-apikey.html)   
Use the `ApiKeyID` property to specify the API key ID\.  | October 22, 2020 | 
| [Updated resource](AWS_CloudFront.md) | The following resource was updated: AWS::CloudFront::Distribution\. 

[AWS::CloudFront::Distribution](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-cloudfront-distribution.html)  
In the [Origin](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-cloudfront-distribution-origin.html) property type, use the `OriginShield` property to enable CloudFront Origin Shield\.  
For more information, see [Using Origin Shield](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/origin-shield.html) in the *Amazon CloudFront Developer Guide*\.  | October 22, 2020 | 
| [Updated resource](AWS_Elasticsearch.md) | The following resource was updated: AWS::Elasticsearch::Domain\. 

 [AWS::Elasticsearch::Domain](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-elasticsearch-domain.html)   
In the [ElasticsearchClusterConfig](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-elasticsearch-domain-elasticsearchclusterconfig.html) property type:  
+ Use the `WarmCount` property to specify the number of warm nodes in the cluster\.
+ Use the `WarmEnabled` property to specify whether to enable warm storage for the cluster\.
+ Use the `WarmType` property to specify the instance type for the cluster's warm nodes\.  | October 22, 2020 | 
| [Updated resource](AWS_EMR.md) | The following resource was updated: AWS::EMR::Cluster\. 

 [AWS::EMR::Cluster](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-elasticmapreduce-cluster.html)   
Use the `LogEncryptionKmsKeyId` property to specify the AWS KMS customer master key \(CMK\) used for encrypting log files\.  
Use the `ManagedScalingPolicy` property to create a managed scaling policy for an Amazon EMR cluster\.  
Use the `StepConcurrencyLevel` property to specify the number of steps that can be executed concurrently\.  | October 22, 2020 | 
| [Updated resource](AWS_Events.md) | The following resource was updated: AWS::Events::Rule\. 

 [AWS::Events::Rule](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-events-rule.html)   
Added [AWS::Events::Rule DeadLetterConfig](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-events-rule-deadletterconfig.html)  
Added [AWS::Events::Rule RetryPolicy](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-events-rule-retrypolicy.html) 

[AWS::Events::Rule Target](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-events-rule-target.html)  
Added the [DeadLetterConfig](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-events-rule-target.html#cfn-events-rule-target-deadletterconfig) property of the Target property type\.  
Added the [RetryPolicy](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-events-rule-target.html##cfn-events-rule-target-retrypolicy) property of the Target property type\.  | October 22, 2020 | 
| [Updated resource](AWS_Kendra.md) | Added a new property, `FileFormat`, to the FAQ resource\. For more information, see [https://docs.aws.amazon.com/kendra/latest/dg/in-creating-faq.html](https://docs.aws.amazon.com/kendra/latest/dg/in-creating-faq.html) | October 22, 2020 | 
| [Updated resource](AWS_KinesisFirehose.md) | The following resource was updated: AWS::KinesisFirehose::DeliveryStream 

 [AWS::KinesisFirehose::DeliveryStream](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-kinesisfirehose-deliverystream.html)   
DeliveryStreamEncryptionConfigurationInput property type is now supported for the delivery streams in CloudFormation\.  | October 22, 2020 | 
| [Updated resource](AWS_SNS.md) | The following resource was updated: AWS::SNS::Topic\. 

 [AWS::SNS::Topic](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-sns-topic.html)   
Use the `ContentBasedDeduplication` property to enable content\-based deduplication for FIFO topics\.  
Use the `FifoTopic` property to create a FIFO topic\.  | October 22, 2020 | 
| [Updated resource](AWS_Transfer.md) | The following resource was updated: AWS::Transfer::Server\. 

 [AWS::Transfer::Server](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-transfer-server.html)   
In the [EndpointDetails](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-transfer-server-endpointdetails.html) property type, use the `SecurityGroupIds` property to specify a list of security groups IDs that are available to attach to your server's endpoint\.  | October 22, 2020 | 
| [New resources](AWS_MediaPackage.md) | The following resources were added: AWS::MediaPackage::Asset, AWS::MediaPackage::Channel, , AWS::MediaPackage::OriginEndpoint, AWS::MediaPackage::PackagingConfiguration, and AWS::MediaPackage::PackagingGroup\. 

 [AWS::MediaPackage::Asset\.](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-mediapackage-asset.html)   
Use the `AWS::MediaPackage::Asset` to specify an asset to ingest VOD content\. 

 [AWS::MediaPackage::Channel\.](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-mediapackage-channel.html)   
Use the `AWS::MediaPackage::Channel` to specify a channel to receive content\. 

 [AWS::MediaPackage::OriginEndpoint\.](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-mediapackage-originendpoint.html)   
Use the `AWS::MediaPackage::OriginEndpoint` to specify an endpoint on an AWS Elemental MediaPackage channel\. 

 [AWS::MediaPackage::PackagingConfiguration\.](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-mediapackage-packagingconfiguration.html)   
Use the `AWS::MediaPackage::PackagingConfiguration` to specify a packaging configuration in a packaging group\. 

 [AWS::MediaPackage::PackagingGroup\.](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-mediapackage-packaginggroup.html)   
Use the `AWS::MediaPackage::PackagingGroup` to specify a packaging group\.  | October 22, 2020 | 
| [New resource](AWS_SecretsManager.md) | The following new resource was added: `BlockPublicPolicy` 

 [Resource Policies](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-secretsmanager-resourcepolicy.html)   
Use the `BlockPublicPolicy` when adding resource policies to Secrets Manager\.  | October 22, 2020 | 
| [Increased quotas](#ReleaseHistory) | The following AWS CloudFormation quotas have been updated\.  You can now declare a maximum of `200` mappings in your AWS CloudFormation template\.   You can now declare a maximum of `200` mapping attributes for each mapping in your AWS CloudFormation template\.   You can now declare a maximum of `200` outputs in your AWS CloudFormation template\.   You can now declare a maximum of `200` parameters in your AWS CloudFormation template\.   You can now declare a maximum of `500` resources in your AWS CloudFormation template\.   You can now pass a template body with a maximum size of `1 MB` in an Amazon S3 object\.   | October 22, 2020 | 
| [Updated resource](AWS_AmazonMQ.md) | The following resource was updated: AWS::AmazonMQ::Broker\. 

 [AWS::AmazonMQ::Broker](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-amazonmq-broker.html)   
Use the `LdapServerMetadata` property to to authenticate and authorize connections to a broker\.  | October 9, 2020 | 
| [Updated resource](AWS_Backup.md) | The following resource was updated: AWS::Backup::BackupPlan 

 [AWS::Backup::BackupPlan](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-backup-backupplan.html)   
In the [BackupPlanResourceType](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-backup-backupplan-backupplanresourcetype.html) property type, use the `AdvancedBackupSetting` property to specify a list of backup options for each resource type you want to back up\.  | October 8, 2020 | 
| [New resources](AWS_CodeArtifact.md) | The following resources were added: AWS::CodeArtifact::Domain and AWS::CodeArtifact::Repository\. 

 [AWS::CodeArtifact::Domain](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-codeartifact-domain.html)   
Use the `AWS::CodeArtifact::Domain` resource to create an AWS CodeArtifact domain\. 

 [AWS::CodeArtifact::Repository](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-codeartifact-repository.html)   
Use the `AWS::CodeArtifact::Repository` resource to create an AWS CodeArtifact repository\.  | October 8, 2020 | 
| [Updated resources](AWS_ECS.md) | The following resources were updated: AWS::ECS::Service 

 [AWS::ECS::Service](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ecs-service.html)   
Use the `CapacityProviderStrategy` property to specify a custom capacity provider strategy when creating a service\.  | October 1, 2020 | 
| [Updated resource](AWS_Batch.md) | The following resource was updated: [AWS::Batch::JobDefinition](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-batch-jobdefinition.html)\.These property types were added\. 

[LogConfiguration](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-batch-jobdefinition-containerproperties-logconfiguration.html)  
Use the [LogConfiguration](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-batch-jobdefinition-containerproperties-logconfiguration.html) property type to specify the log configuration options to send to a custom log driver for the container\. 

[Secrets](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-batch-jobdefinition-secret.html)  
Use the [Secrets](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-batch-jobdefinition-secret.html) property type to specify a secret to expose to the container\. 

[Tmpfs](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-batch-jobdefinition-tmpfs.html)  
Use the [Tmpfs](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-batch-jobdefinition-tmpfs.html) property type to specify the details of a `tmpfs` mount\. These property types were updated\. 

[ContainerProperties](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-batch-jobdefinition-containerproperties.html)  
These properties were added\.    
ExecutionRoleArn  
Specifies the execution role to be assumed for the job\.  
LogConfiguration  
Specifies the log configuration for a custom log driver for the job\.  
Secrets  
Specifies the secrets provided for the job\. 

[LinuxParameters](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-batch-jobdefinition-containerproperties-linuxparameters.html)  
These properties were added\.    
InitProcessEnabled  
Indicates that an init process should be enabled inside the container that forwards signals and reaps processes\.  
MaxSwap  
Specifies the total amount of swap memory \(in MiB\) a job can use\.  
SharedMemorySize  
Specifies the size \(in MiB\) of the `/dev/shm` volume\.   
Swappiness  
Specifies the job container's memory swappiness behavior\.  
Tmpfs  
Specifies the details of the job's `tmpfs` mount\.  | October 1, 2020 | 
| [Updated resource](AWS_CloudFront.md) | The following resource was updated: AWS::CloudFront::CachePolicy\. 

 [AWS::CloudFront::CachePolicy](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-cloudfront-cachepolicy.html)   
In the `AWS::CloudFront::CachePolicy` resource, some properties are now required that previously were not required\.  
In the [AWS::CloudFront::CachePolicy ParametersInCacheKeyAndForwardedToOrigin](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-cloudfront-cachepolicy-parametersincachekeyandforwardedtoorigin.html) property type, use the `EnableAcceptEncodingBrotli` property to enable CloudFront to serve compressed objects to viewers that support the Brotli compression format\. For more information, see [Compression support](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/controlling-the-cache-key.html#cache-policy-compressed-objects) in the *Amazon CloudFront Developer Guide*\.  | October 1, 2020 | 
| [Updated resource](AWS_EKS.md) | The following resource was updated to support specifying a custom CIDR for Kubernetes service IP address assignment: AWS::EKS::Cluster\. 

 [AWS::EKS::Cluster](https://docs.aws.amazon.com/aws-resource-eks-cluster.html)   
Use the `KubernetesNetworkConfig` property to specify a Kubernetes network configuration\. 

 [AWS::EKS::Cluster KubernetesNetworkConfig](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-eks-cluster-kubernetesnetworkconfig.html)   
Use the `ServiceIpv4Cidr` property to specify the CIDR block that you want Kubernetes to assign service IP addresses from\.  | October 1, 2020 | 
| [New resource](AWS_WorkSpaces.md) | The following resource was added: `AWS::WorkSpaces::ConnectionAlias` 

 [AWS::WorkSpaces::ConnectionAlias](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-workspaces-connectionalias.html)   
Use the `AWS::WorkSpaces::ConnectionAlias` resource to specify a connection alias\. Connection aliases are used for cross\-Region redirection\.   | October 1, 2020 | 
| [Drift detection for private resources](#ReleaseHistory) | CloudFormation supports drift detection operations on an expanded list of AWS resources, as well as private resources that are defined as provisonable\.In addition to the resources that previously supported drift detection, CloudFormation now supports drift detection on all resources defined as provisionable in the CloudFormation registry\. For more information, see [Resources that support import and drift detection operations](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/resource-import-supported-resources.html)\. | October 1, 2020 | 
| [Updated resource](AWS_ApiGateway.md) | The following resource was updated: `AWS::ApiGateway::DomainName`\. 

 [AWS::ApiGateway::DomainName](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-apigateway-domainname.html)   
Use the `AWS::ApiGateway::DomainName` resource to configure mutual TLS authentication for an API\.  | September 17, 2020 | 
| [Updated resource](AWS_ApiGatewayV2.md) | The following resource was updated: `AWS::ApiGatewayV2::DomainName`\. 

 [AWS::ApiGatewayV2::DomainName](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-apigatewayv2-domainname.html)   
Use the `AWS::ApiGatewayV2::DomainName` resource to configure mutual TLS authentication for an API\.  | September 17, 2020 | 
| [Updated resource](AWS_ApiGatewayV2.md) | The following resource was updated: `AWS::ApiGatewayV2::Api`\. 

 [AWS::ApiGatewayV2::Api](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-apigatewayv2-api.html)   
Use the `AWS::ApiGatewayV2::Api` resource to disable the default endpoint for an HTTP API\.  | September 17, 2020 | 
| [New resources](AWS_AppFlow.md) | The following resources were added: AWS::AppFlow::Flow and AWS::AppFlow::ConnectorProfile\. 

 [AWS::AppFlow::Flow](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-appflow-flow.html)   
Use the `AWS::AppFlow::Flow` resource to specify a new flow in Amazon AppFlow\. 

 [AWS::AppFlow::ConnectorProfile](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-appflow-connectorprofile.html)   
Use the `AWS::AppFlow::ConnectorProfile` describe an instance of a connector in Amazon AppFlow\.  | September 17, 2020 | 
| [New resources](AWS_CloudFormation.md) | The following resource was added: AWS::CloudFormation::StackSet\. 

 [AWS::CloudFormation::StackSet](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-cloudformation-stackset.html)   
Use the `AWS::CloudFormation::StackSet` resource to provision stacks into AWS accounts and across Regions by using a single CloudFormation template\.  | September 17, 2020 | 
| [Updated resource](AWS_ApiGatewayV2.md) | The following resource was updated: `AWS::ApiGatewayV2::Authorizer`\. 

 [AWS::ApiGatewayV2::Authorizer](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-apigatewayv2-authorizer.html)   
Use the `AWS::ApiGatewayV2::Authorizer` resource to create a Lambda authorizer for an HTTP API\.  | September 10, 2020 | 
| [Updated resource](AWS_CodeBuild.md) | The following resource was updated: AWS::CodeBuild::ReportGroup 

 [AWS::CodeBuild::ReportGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-codebuild-reportgroup.html)   
Use the `DeleteReports` property to specify if any reports that belong to the report group should be deleted when the report group is deleted\.   | September 10, 2020 | 
| [Updated resource](AWS_StepFunctions.md) | The following resource was updated: `AWS::StepFunctions::StateMachine`\. 

 [AWS::StepFunctions::StateMachine](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-stepfunctions-statemachine.html)   
The `AWS::StepFunctions::StateMachine` now supports X\-Ray tracing\. You can use the `TracingConfiguration` property to enable X\-Ray tracing for your state machines\.  | September 10, 2020 | 
| [New resources](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/AWS_Kendra) | This is the first release of Amazon Kendra in AWS CloudFormation\. | September 10, 2020 | 
| [New resources](AWS_SSO.md) | The following resources were added: AWS::SSO::Assignment, AWS::SSO::PermissionSet\.  

 [AWS::SSO::Assignment](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-sso-assignment.html)   
Use the `AWS::SSO::Assignment` resource to assign access to a principal for a specified AWS account using a specified permission set\. 

 [AWS::SSO::PermissionSet](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-sso-permissionset.html)   
Use the `AWS::SSO::PermissionSet` resource to create a permission set within a specified SSO instance\.  | September 10, 2020 | 
| [Update resource](AWS_CloudFront.md) | The following resource was updated: AWS::CloudFront::Distribution\. 

 [AWS::CloudFront::Distribution](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-cloudfront-distribution.html)   
In the [CacheBehavior](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-cloudfront-distribution-cachebehavior.html) and [DefaultCacheBehavior](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-cloudfront-distribution-defaultcachebehavior.html) property types, use the `RealtimeLogConfigArn` property to specify the Amazon Resource Name \(ARN\) of the real\-time log configuration for the cache behavior\.  
For more information, see [Real\-time logs](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/real-time-logs.html) in the *Amazon CloudFront Developer Guide*\.  | September 3, 2020 | 
| [New resources](AWS_CloudFront.md) | The following resources were added: AWS::CloudFront::CachePolicy, AWS::CloudFront::OriginRequestPolicy, and AWS::CloudFront::RealtimeLogConfig\. 

 [AWS::CloudFront::CachePolicy](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-cloudfront-cachepolicy.html)   
Use the `AWS::CloudFront::CachePolicy` resource to create a new cache policy in Amazon CloudFront\. 

 [AWS::CloudFront::OriginRequestPolicy](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-cloudfront-originrequestpolicy.html)   
Use the `AWS::CloudFront::OriginRequestPolicy` resource to create a new origin request policy in Amazon CloudFront\. 

 [AWS::CloudFront::RealtimeLogConfig](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-cloudfront-realtimelogconfig.html)   
Use the `AWS::CloudFront::RealtimeLogConfig` resource to create a new real\-time log configuration in Amazon CloudFront\.  | September 3, 2020 | 
| [New resource](AWS_CodeGuruReviewer.md) | The following resource was added: AWS::CodeGuruReviewer::RepositoryAssociation 

 [AWS::CodeGuruReviewer::RepositoryAssociation](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-codegurureviewer-repositoryassociation.html)   
The `AWS::CodeGuruReviewer::RepositoryAssociation` resource describes an associated repository that contains source code to be analyzed by AWS CodeGuru Reviewer\. For more information, see [RespositoryAssociation](https://docs.aws.amazon.com/codeguru/latest/reviewer-api/API_RepositoryAssociation.html) in the *AWS CodeGuru Reviewer API Reference*\.  | September 3, 2020 | 
| [New resource](AWS_EKS.md) | The following resource was added: AWS::EKS::FargateProfile\. 

 [AWS::EKS::FargateProfile](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-eks-fargateprofile.html)   
Use the `AWS::EKS::FargateProfile` resource to create an AWS Fargate profile\.  | September 3, 2020 | 
| [Updated resource](AWS_CodeCommit.md) | The following resource was updated: AWS::CodeCommit::Repository Code 

 [AWS::CodeCommit::Repository Code](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-codecommit-repository-code.html)   
Use the `BranchName` property to specify a branch name to be used as the default branch when importing code into a repository\.  | August 31, 2020 | 
| [Updated resource](AWS_ServiceCatalog.md) | The following resource was updated: AWS::ServiceCatalog::CloudFormationProvisionedProduct\. 

 [AWS::ServiceCatalog::CloudFormationProvisionedProduct](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-servicecatalog-cloudformationprovisionedproduct.html)   
The `PathName` property is now available as an alternative to `PathId`\.  | August 27, 2020 | 
| [New resources](AWS_GameLift.md) | The following resources were added: AWS::GameLift::GameServerGroup 

 [AWS::GameLift::GameServerGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-gamelift-gameservergroup.html)   
Use the `AWS::GameLift::GameServerGroup` resource to create a GameLift FleetIQ game server group to run low\-cost game hosting on your Amazon EC2 instances\.  | August 27, 2020 | 
| [New resources](AWS_Route53Resolver.md) | The following resources were added: AWS::Route53Resolver::ResolverQueryLoggingConfig and AWS::Route53Resolver::ResolverQueryLoggingConfigAssociation\. 

 [AWS::Route53Resolver::ResolverQueryLoggingConfig](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-route53resolver-resolverqueryloggingconfig.html)   
Use the `AWS::Route53Resolver::ResolverQueryLoggingConfig` resource to specify settings for a query logging configuration\. 

 [AWS::Route53Resolver::ResolverQueryLoggingConfigAssociation](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-route53resolver-resolverqueryloggingconfigassociation.html)   
Use the `AWS::Route53Resolver::ResolverQueryLoggingConfigAssociation` resource to configure DNS query logging\.  | August 27, 2020 | 
| [Updated resource](AWS_KMS.md) | The following resource was updated: AWS::KMS::Key\. 

 [AWS::KMS::Key](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-kms-key.html)   
Added a `KeyId` attribute to the [return values](https://docs.aws.amazon.com/https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-kms-key.html#aws-resource-kms-key-return-values)\.  | August 26, 2020 | 
| [Updated resource](AWS_EKS.md) | The following resource was updated to support use of a launch template: AWS::EKS::Nodegroup\. 

 [AWS::EKS::Nodegroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-eks-nodegroup.html)   
Use the `LaunchTemplate` property to specify a launch template specification that can be used to deploy or update a managed node group\. If you use a launch template to deploy a node group, some settings that you normally set for a node group must be moved into the launch template\. The text for affected settings has been updated to note that\.  | August 20, 2020 | 
| [Updated resources](AWS_ECS.md) | The following resources were updated: AWS::ECS::TaskDefinition 

 [AWS::ECS::TaskDefinition](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ecs-taskdefinition.html)   
Use the `EnvironmentFiles` property to specify a list of files containing the environment variables to pass to a container\.  | August 13, 2020 | 
| [Updated resource](AWS_FSx.md) | The following resource was updated: AWS::FSx::FileSystem 

[AWS::FSx::FileSystem](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-fsx-filesystem.html)  
In the [LustreConfiguration](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-fsx-filesystem-lustreconfiguration.html) property type, use `DriveCacheType` to specify the type of drive cache used by `PERSISTENT_1` file systems that are provisioned with HDD storage devices\.  | August 13, 2020 | 
| [Updated resource](AWS_Lambda.md) | The following resource was updated: AWS::Lambda::EventSourceMapping\. 

 [AWS::Lambda::EventSourceMapping](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-lambda-eventsourcemapping.html)   
Use the `Topics` property to specify the Amazon MSK topics to stream to a Lambda function\.  | August 13, 2020 | 
| [New resource](AWS_ApplicationInsights.md) | The following resource was added: AWS::ApplicationInsights::Application  

 [AWS::ApplicationInsights::Application](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-applicationinsights-application.html)   
Use the `AWS::ApplicationInsights::Application` resource to add an application that is created from a resource group\.  | August 13, 2020 | 
| [New resource](AWS_EC2.md) | The following resource was added: AWS::EC2::CarrierGateway\. 

 [AWS::EC2::CarrierGateway](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-carriergateway.html)   
Use the `CarrierGateway` resource to create a carrier gateway\.  | August 13, 2020 | 
| [Updated permissions required for registering resource providers](#ReleaseHistory) | Registering a resource provider in your account now requires you have permission to access the schema handler package uploaded to an S3 bucket for that resource provider\.For more information, see [Registering resource providers in CloudFormation](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/registry.html#registry-register)\. | August 7, 2020 | 
| [Updated resource](AWS_CodeBuild.md) | The following resource was updated: AWS::CodeBuild::Project 

 [AWS::CodeBuild::Project](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-codebuild-project.html)   
Use the `BuildBatchConfig` property to specify configuration information for a batch build\.  | August 6, 2020 | 
| [Updated resource](AWS_FSx.md) | The following resource was updated: AWS::FSx::FileSystem 

[AWS::FSx::FileSystem](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-fsx-filesystem.html)  
In the [LustreConfiguration](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-fsx-filesystem-lustreconfiguration.html) property type, `AutoImportPolicyType` was changed to `AutoImportPolicy`\. Use `AutoImportPolicy` to configure your Amazon FSx for Lustre file system to automatically import metadata of objects that are added to or changed in your linked S3 bucket after file system creation\.  | August 6, 2020 | 
| [Updated resources](AWS_ECS.md) | The following resources were updated: AWS::ECS::TaskDefinition 

 [AWS::ECS::TaskDefinition](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ecs-taskdefinition.html)   
Use the `EFSVolumeConfiguration` property to specify an Amazon Elastic File System file system for task storage\.  | July 30, 2020 | 
| [Updated resource](AWS_EC2.md) | The following resource was updated: AWS::EC2::FlowLog\. 

 [AWS::EC2::FlowLog](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-flowlog.html)   
Use the `LogFormat` property to specify the fields for the flow log record\.  
Use the `MaxAggregationInterval` property to specify the maximum interval for capturing and aggregating flows\.  
Use the `Tags` property to specify tags for the flow log\.  | July 30, 2020 | 
| [Updated resource](AWS_GroundStation.md) | The following resource was updated: AWS::GroundStation::DataflowEndpointGroup\. 

 [MTU property](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-groundstation-dataflowendpointgroup-dataflowendpoint.html#cfn-groundstation-dataflowendpointgroup-dataflowendpoint-mtu)   
The `MTU` property sets the maximum transmission unit used for a dataflow endpoint\.  | July 30, 2020 | 
| [New resources](AWS_AppMesh.md) | The following resources were added: AWS::AppMesh::VirtualGateway and AWS::AppMesh::GatewayRoute 

 [AWS::AppMesh::VirtualGateway](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-appmesh-virtualgateway.html)   
Use the `AWS::AppMesh::VirtualGateway` resource to create a virtual gateway that allows resources outside of your mesh to communicate to resources that are inside of your mesh\. 

 [AWS::AppMesh::GatewayRoute](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-appmesh-gatewayroute.html)   
Use the `AWS::AppMesh::GatewayRoute` resource to create a gateway route that routes traffic to a virtual service\.  | July 30, 2020 | 
| [New resources](AWS_SageMaker.md) | The following resource was added: AWS::SageMaker::MonitoringSchedule 

 [AWS::SageMaker::MonitoringSchedule](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-sagemaker-monitoringschedule.html)   
Use the `AWS::SageMaker::MonitoringSchedule` resource to create a monitoring schedule to regularly start an Amazon SageMaker processing job to monitor the data captured for a SageMaker endpoint\.  | July 30, 2020 | 
| [New property](AWS_CodeGuruProfiler.md) | The following properties were added: `AWS::CodeGuruProfiler::ProfilingGroup.AnomalyDetectionNotificationConfiguration` and `AWS::CodeGuruProfiler::ProfilingGroup.Tags`\. 

 [AWS::CodeGuruProfiler::ProfilingGroup\.AnomalyDetectionNotificationConfiguration](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-codeguruprofiler-profilinggroup.html)   
Use the `AWS::CodeGuruProfiler::ProfilingGroup.AnomalyDetectionNotificationConfiguration` property to configure notifications for your profiling group\. 

 [AWS::CodeGuruProfiler::ProfilingGroup\.Tags](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-codeguruprofiler-profilinggroup.html)   
Use the `AWS::CodeGuruProfiler::ProfilingGroup.Tags` property to add tags to a profiling group\.  | July 30, 2020 | 
| [Updated resources](AWS_WAFv2.md) | The following resources were updated: AWS::WAFv2::WebACL and AWS::WAFv2::RuleGroup 

 [AWS::WAFv2::WebACL](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-wafv2-webacl.html)   
Rule statements that use IP addresses now support using IP addresses that are forwarded in an HTTP header in the web request, instead of using the IP address that's reported by the web request origin\. This option is available for all rule statements that use an IP address: `GeoMatchStatement`, `RateBasedStatement`, and `IPSetReferenceStatement`\. The following new properties support this functionality: `IPSetForwardedIPConfiguration` and `ForwardedIPConfiguration`\. 

 [AWS::WAFv2::RuleGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-wafv2-rulegroup.html)   
Rule statements that use IP addresses now support using IP addresses that are forwarded in an HTTP header in the web request, instead of using the IP address that's reported by the web request origin\. This option is available for all rule statements that use an IP address: `GeoMatchStatement`, `RateBasedStatement`, and `IPSetReferenceStatement`\. The following new properties support this functionality: `IPSetForwardedIPConfiguration` and `ForwardedIPConfiguration`\.  | July 23, 2020 | 
| [Updated resource](AWS_CloudFront.md) | The following resource was updated: AWS::CloudFront::Distribution\. 

 [AWS::CloudFront::Distribution](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-cloudfront-distribution.html)   
In the [CacheBehavior](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-cloudfront-distribution-cachebehavior.html) and [DefaultCacheBehavior](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-cloudfront-distribution-defaultcachebehavior.html) property types:  
+ Use the `CachePolicyId` property to specify the ID of the cache policy for the cache behavior\.
+ Use the `OriginRequestPolicyId` property to specify the ID of the origin request policy for the cache behavior\.
For more information, see [Working with policies](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/working-with-policies.html) in the *Amazon CloudFront Developer Guide*\.  | July 23, 2020 | 
| [Updated resource](AWS_CodeStarConnections.md) | The following resource was updated: AWS::CodeStarConnections::Connection 

 [AWS::CodeStarConnections::Connection](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-codestarconnections-connection.html)   
Use the `HostArn` property to specify the host associated with connections you want to make to an installed provider\.  | July 23, 2020 | 
| [Updated resource](AWS_EFS.md) | The following resource was updated: AWS::EFS::FileSystem 

[AWS::EFS::FileSystem](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-efs-filesystem-backuppolicy.html)  
Use the `BackupPolicy` property to turn automatic backups on or off for your Amazon EFS file system\.  | July 23, 2020 | 
| [Updated resource](AWS_FSx.md) | The following resource was updated: AWS::FSx::FileSystem 

[AWS::FSx::FileSystem](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-fsx-filesystem.html)  
In the [LustreConfiguration](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-fsx-filesystem-lustreconfiguration.html) property type, use `AutoImportPolicy` to configure how FSx imports new files and file changes in the linked data repository into the file system\.  | July 23, 2020 | 
| [Updated resource](AWS_SageMaker.md) | The following resource was updated: EndpointConfig 

 [AWS::SageMaker::EndpointConfig](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-sagemaker-endpointconfig.html)   
Use the `CaptureContentTypeHeader` property to specify content types \(JSON and/or CSV\) to capture\.  
Use the `CaptureOption` property to specify whether to capture input data, output data, or both\.  
Use the `DataCaptureConfig` resource/property to configure how the endpoint captures data\.  | July 23, 2020 | 
| [Updated resource](AWS_Amplify.md) | The following resource was updated: AWS::Amplify::App 

 [AWS::Amplify::App](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-amplify-app.html)   
Use the `EnableBranchAutoDeletion` property to automatically disconnect a branch in the Amplify Console when you delete a branch from your Git repository\.  | July 9, 2020 | 
| [Updated resource](AWS_Amplify.md) | The following resource was updated: AWS::Amplify::Domain 

 [AWS::Amplify::Domain](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-amplify-domain.html)   
Use the `AutoSubDomainCreationPatterns` property to set branch patterns for automatic subdomain creation\.  
Use the `AutoSubDomainIAMRole` property to specify the required AWS Identity and Access Management \(IAM\) service role for the Amazon Resource Name \(ARN\) for automatically creating subdomains\.  
Use the `EnableAutoSubDomain` property to enable the automated creation of subdomains for branches\.  | July 9, 2020 | 
| [Updated resource](AWS_ElasticLoadBalancingV2.md) | The following resource was updated: AWS::ElasticLoadBalancingV2::Listener\. 

 [AWS::ElasticLoadBalancingV2::Listener](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-elasticloadbalancingv2-listener.html)   
Use the `AlpnPolicy` property to specify the name of the Application\-Layer Protocol Negotiation \(ALPN\) policy for TLS listeners\.  | July 9, 2020 | 
| [Updated resource](AWS_FSx.md) | The following resource was updated: AWS::FSx::FileSystem 

[AWS::FSx::FileSystem](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-fsx-filesystem.html)  
The `StorageCapacity` property has changed so that an update requires no interruption\.  
In the [WindowsConfiguration](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-fsx-filesystem-windowsconfiguration.html) property type, the `ThroughputCapacity` property has changed so that an update requires no interruption\.  
In the [LustreConfiguration](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-fsx-filesystem-lustreconfiguration.html) property type:  
+ Use the `DailyAutomaticBackupStartTime` property to specify the time that the daily automatic backup window starts\.
+ Use the `CopyTagsToBackups` boolean property to copy file system tags to its backups\.
+ Use the `AutomaticBackupRetentionDays` property to set the number of days to retain file system backups\.  | July 9, 2020 | 
| [Updated resource](AWS_ServiceCatalog.md) | The following resource was updated: AWS::ServiceCatalog::CloudFormationProvisionedProduct\. 

 [AWS::ServiceCatalog::CloudFormationProvisionedProduct](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-servicecatalog-cloudformationprovisionedproduct.html)   
Use the `Outputs` property to view the output of the product you are provisioning\.   | July 9, 2020 | 
| [Updated resource](AWS_Synthetics.md) | The following resource was updated: AWS::Synthetics::Canary\. 

 [AWS::Synthetics::Canary](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-synthetics-canary.html)   
The MemoryInMB parameter was added\. Also, the RunConfig parameter is no longer required, and DurationInSeconds is no longer required\.   | July 9, 2020 | 
| [New resource](AWS_Athena.md) | The following resource was added: AWS::Athena::DataCatalog 

 [AWS::Athena::DataCatalog](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-athena-datacatalog.html)   
Use the `AWS::Athena::DataCatalog` resource to register external data sources with Athena\.  | July 9, 2020 | 
| [New resource](AWS_EC2.md) | The following resource was added: AWS::EC2::PrefixList\. 

 [AWS::EC2::PrefixList](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-prefixlist.html)   
Use the `PrefixList` resource to create a prefix list\.  | July 9, 2020 | 
| [New resource](AWS_QLDB.md) | The following resource was added: AWS::QLDB::Stream 

 [AWS::QLDB::Stream](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-qldb-stream.html)   
Use the `AWS::QLDB::Stream` resource to specify a new journal stream for a given Amazon Quantum Ledger Database \(Amazon QLDB\) ledger\.  | July 9, 2020 | 
| [New property](AWS_CodeBuild.md) | The following property was added to AWS::CodeBuild::Project Source: BuildStatusConfig 

 [AWS::CodeBuild::Project Source](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-codebuild-project-source.html#cfn-codebuild-project-source-buildstatusconfig)   
Use the `buildStatusConfig` property to specify build status information to the source provider\.  | July 9, 2020 | 
| [New property](AWS_CodeGuruProfiler.md) | The following resource was added: `AWS::CodeGuruProfiler::ProfilingGroup.ComputePlatform`\. 

 [AWS::CodeGuruProfiler::ProfilingGroup\.ComputePlatform](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-codeguruprofiler-profilinggroup.html)   
Use `AWS::CodeGuruProfiler::ProfilingGroup.ComputePlatform` to specify the compute platform of the profiling group\.  | July 9, 2020 | 
| [Updated resource](AWS_Events.md) | The following resource was updated: AWS::Events::Rule\. 

 [AWS::Events::Rule](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-events-rule.html)   
In the [Target](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-events-rule-target.html) property type, use the `HttpParameters` property to specify the HTTP parameters to use when the target is a API Gateway REST endpoint\.  | July 6, 2020 | 
| [New resource](AWS_AppConfig.md) | The following resource was added: AWS::AppConfig::HostedConfigurationVersion 

 [AWS::AppConfig::HostedConfigurationVersion](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-appconfig-hostedconfigurationversion.html)   
This resource lets you create a new configuration in the AppConfig hosted configuration store\.  | June 25, 2020 | 
| [Updated resources](AWS_ServiceDiscovery.md) | The following resources were updated: `AWS::ServiceDiscovery::HttpNamespace` `AWS::ServiceDiscovery::PrivateDnsNamespace` `AWS::ServiceDiscovery::PublicDnsNamespac`e `AWS::ServiceDiscovery::Service`  

 [AWS::ServiceDiscovery::HttpNamespace](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-servicediscovery-httpnamespace.html)   
Use the `Tags` property to add tag keys and values to an AWS CloudMap HTTP namespace\. 

 [AWS::ServiceDiscovery::PrivateDnsNamespace](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-servicediscovery-privatednsnamespace.html)   
Use the `Tags` property to add tag keys and values to an AWS CloudMap private DNS namespace\. 

 [AWS::ServiceDiscovery::PublicDnsNamespace](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-servicediscovery-publicdnsnamespace.html)   
Use the `Tags` property to add tag keys and values to an AWS CloudMap public DNS namespace\. 

 [AWS::ServiceDiscovery::Service](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-servicediscovery-service.html)   
Use the `Tags` property to add tag keys and values to an AWS CloudMap service\.  | June 22, 2020 | 
| [Updated resources](AWS_ECS.md) | The following resources were updated: AWS::ECS::Cluster 

 [AWS::ECS::Cluster](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ecs-cluster.html)   
Use the `CapacityProviderStrategyItem` property to specify the capacity provider strategy when creating a cluster\.  | June 18, 2020 | 
| [Updated resource](AWS_FMS.md) | The following resources were updated: AWS::FMS::Policy IEMap 

 [AWS::FMS::Policy IEMap](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-fms-policy-iemap.html)   
The `AWS::FMS::Policy IEMap` resource now allows you to specify accounts using AWS Organizations organizational units \(OUs\), in addition to account IDs\.   | June 18, 2020 | 
| [New resources](AWS_ECS.md) | The following resources were added: AWS::ECS::CapacityProvider\. 

 [AWS::ECS::CapacityProvider](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ecs-capacityprovider.html)   
Use the `AWS::ECS::CapacityProvider` resource to create a new capacity provider\.  | June 18, 2020 | 
| [Updated resource](AWS_EFS.md) | The following resource was updated: AWS::EFS::FileSystem 

[AWS::EFS::FileSystem](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-efs-filesystem.html)  
Use the `FileSystemPolicy` property to create a new resource policy to control NFS access to your Amazon EFS file system\.  | June 16, 2020 | 
| [Updated resource](AWS_EFS.md) | The following resource was updated: AWS::EFS::AccessPoint 

[AWS::EFS::AccessPoint](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-efs-accesspoint.html)  
Fn::GetAtt now returns the `AccessPointId` and `Arn` attributes\.  | June 16, 2020 | 
| [Updated resource](AWS_Lambda.md) | The following resource was updated: AWS::Lambda::Function\. 

 [AWS::Lambda::Function](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-lambda-function.html)   
Use the `FileSystemConfigs` property to specify connection settings for an Amazon EFS file system\.  | June 16, 2020 | 
| [Updated resources](AWS_EC2.md) | The following resource was updated: AWS::EC2::Volume\. 

 [AWS::EC2::Volume](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ec2-ebs-volume.html)   
Use the `OutpostArn` property to specify the Amazon Resource Name \(ARN\) of the Outpost\.  | June 11, 2020 | 
| [Updated resource](AWS_CertificateManager.md) | The following resource was updated: AWS::CertificateManager::Certificate 

 [AWS::CertificateManager::Certificate](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-certificatemanager-certificate.html)   
Use the `CertificateAuthorityArn` property to specify the Amazon Resource Name \(ARN\) of the private certificate authority \(CA\) that will be used to issue the certificate\.  
Use the `CertificateTransparencyLoggingPreference` property to enable or disable certificate transparency logging\.  | June 11, 2020 | 
| [Updated resource](AWS_CloudFront.md) | The following resource was updated: AWS::CloudFront::Distribution\. 

 [AWS::CloudFront::Distribution](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-cloudfront-distribution.html)   
In the [Origin](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-cloudfront-distribution-origin.html) property type, use the `ConnectionAttempts` property to specify the number of times that CloudFront attempts to connect to the origin\.  
In the [Origin](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-cloudfront-distribution-origin.html) property type, use the `ConnectionTimeout` property to specify the number of seconds that CloudFront waits when trying to establish a connection to the origin\.  | June 11, 2020 | 
| [Updated resource](AWS_ElastiCache.md) | The following resource was updated: AWS::ElastiCache::ReplicationGroup\. 

 [AWS::ElastiCache::ReplicationGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-elasticache-replicationgroup.html)   
Use the `MultiAZEnabled` attribute to indicate if you have Multi\-AZ enabled\.  | June 11, 2020 | 
| [Updated resource](AWS_ElasticLoadBalancingV2.md) | The following resource was updated: AWS::ElasticLoadBalancingV2::LoadBalancer\. 

 [AWS::ElasticLoadBalancingV2::LoadBalancer](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-elasticloadbalancingv2-loadbalancer-subnetmapping.html)   
Use the `SubnetMapping` attribute to specify a subnet to attach to an Application Load Balancer or a Network Load Balancer\.  | June 11, 2020 | 
| [New resource](AWS_RDS.md) | The following resources were added: AWS::RDS::DBProxy and AWS::RDS::DBProxyTargetGroup\. 

 [AWS::RDS::DBProxy](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-rds-dbproxy.html)   
Use the `AWS::RDS::DBProxy` resource to create or update a DB proxy\. Use the `AWS::RDS::DBProxyTargetGroup` resource to specify a set of RDS DB instances, Aurora DB clusters, or both that a proxy can connect to\.  | June 4, 2020 | 
| [Resource import supports provisionable private resource types](#ReleaseHistory) | Import operations now support private resource types that are *provisionable*; that is, whose provisioning type is either `FULLY_MUTABLE` or `IMMUTABLE`\. For more information, see [Resources that support import operations](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/resource-import-supported-resources.html)\. | June 3, 2020 | 
| [New property](AWS_CodeGuruProfiler.md) | The following property was added: `AWS::CodeGuruProfiler::ProfilingGroup.AgentPermissions`\. 

 [AWS::CodeGuruProfiler::ProfilingGroup\.AgentPermissions](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-codeguruprofiler-profilinggroup.html)   
The `AWS::CodeGuruProfiler::ProfilingGroup.AgentPermissions` property shows the agent permissions attached to this profiling group\.  | June 3, 2020 | 
| [Updated resource](AWS_EC2.md) | The following resource was updated: AWS::EC2::ClientVpnEndpoint 

 [AWS::EC2::ClientVpnEndpoint ClientAuthenticationRequest](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ec2-clientvpnendpoint-clientauthenticationrequest.html)   
Use the `FederatedAuthentication` property to specify an IAM SAML identity provider for your Client VPN endpoint\.  | May 28, 2020 | 
| [Updated resource](AWS_MSK.md) | The following resource was updated: AWS::MSK::Cluster 

 [AWS::MSK::Cluster](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-msk-cluster.html)   
You can now update an existing MSK cluster to a newer version of Apache Kafka\. You can't update it to an older version\.  | May 28, 2020 | 
| [Updated resource](AWS_CodeBuild.md) | The following resource was updated: AWS::CodeBuild::ReportGroup 

 [AWS::CodeBuild::ReportGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-codebuild-reportgroup.html)   
Use the `tags` property to specify the name and value of any tags that you want supporting AWS services to use for a report group\.  | May 21, 2020 | 
| [Updated resource](AWS_StepFunctions.md) | The following resource was updated: `AWS::StepFunctions::StateMachine`\. 

 [AWS::StepFunctions::StateMachine](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-stepfunctions-statemachine.html)   
The `AWS::StepFunctions::StateMachine` has two new properties\. You can use the `DefinitionS3Location` property to reference a state machine JSON definition file stored in an S3 bucket\. You can use the `DefinitionSubstitutions` property to pass variables into the state machine definition file referenced by `DefinitionS3Location`\.  | May 21, 2020 | 
| [Updated resource](AWS_SSM.md) | The following resource was updated: AWS::SSM::Parameter 

 [AWS::SSM::Parameter](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ssm-parameter.html)   
When you create a `String` parameter, you can now specify a DataType value as `aws:ec2:image` to ensure that the parameter value you enter is a valid Amazon Machine Image \(AMI\) ID format\. Support for AMI ID formats lets you avoid updating all your scripts and templates with a new ID each time the AMI that you want to use in your processes changes\. You can create a parameter with the data type `aws:ec2:image`, and for its value, enter the ID of an AMI\. This is the AMI from which you currently want new instances to be created\. You then reference this parameter in your templates and commands\. When you’re ready to use a different AMI, update the parameter value\. Parameter Store validates the new AMI ID, and you don’t need to update your scripts and templates\.   | May 21, 2020 | 
| [ECS blue/green deployments through CodeDeploy](#ReleaseHistory) | You can now use CloudFormation to perform ECS blue/green deployments through CodeDeploy\. Blue/green deployments are a safe deployment strategy provided by AWS CodeDeploy for minimizing interruptions caused by changing application versions\.For more information, see [Performing ECS blue/green deployments through CodeDeploy using AWS CloudFormation](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/blue-green.html)\. | May 19, 2020 | 
| [AWS CloudFormation StackSets Region availability](#ReleaseHistory) | AWS CloudFormation StackSets is now available in the AWS GovCloud \(US\-West\) Region\. | May 18, 2020 | 
| [Updated resource](AWS_CodeStarConnections.md) | The following resource was updated: AWS::CodeStarConnections::Connection 

 [AWS::CodeStarConnections::Connection](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-codestarconnections-connection.html)   
Use the `Tags` property to specify the tags applied to your connections resource\.  | May 14, 2020 | 
| [Updated resource](AWS_MediaStore.md) | The following resource was updated: AWS::MediaStore::Container\. 

 [AWS::MediaStore::Container](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-mediastore-container.html)   
Use the `MetricPolicy` property to enable metrics at the object level\.  
Use the `Tags` property to attach metadata to the `AWS::MediaStore::Container` resource\.  | May 14, 2020 | 
| [Updated resource](AWS_ServiceCatalog.md) | The following resource was updated: AWS::ServiceCatalog::CloudFormationProduct\. 

 [AWS::ServiceCatalog::CloudFormationProduct](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-servicecatalog-cloudformationproduct.html)   
Use the `ReplaceProvisioningArtifacts` property to choose whether provisioning artifact identifiers are replaced when you update a product\.  | May 14, 2020 | 
| [Updated resource](AWS_Synthetics.md) | The following resource was updated: AWS::Synthetics::Canary\. 

 [AWS::Synthetics::Canary](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-synthetics-canary.html)   
The RunConfig parameter is required\.  | May 14, 2020 | 
| [New resources](AWS_GlobalAccelerator.md) | The following resources were added: AWS::GlobalAccelerator::Accelerator, AWS::GlobalAccelerator::EndpointGroup, and AWS::GlobalAccelerator::Listener 

 [ AWS::GlobalAccelerator::Accelerator](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-globalaccelerator-accelerator.html)   
Use the `AWS::GlobalAccelerator::Accelerator` resource to create or update an accelerator for AWS Global Accelerator\. 

 [ AWS::GlobalAccelerator::EndpointGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-globalaccelerator-endpointgroup.html)   
Use the `AWS::GlobalAccelerator::EndpointGroup` resource to create or update an endpoint group for AWS Global Accelerator\. 

 [ AWS::GlobalAccelerator::Listener](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-globalaccelerator-listener.html)   
Use the `AWS::GlobalAccelerator::Listener` resource to create or update a listener for AWS Global Accelerator\.  | May 14, 2020 | 
| [New resources](AWS_Macie.md) | The following resources were added: AWS::Macie::CustomDataIdentifier, AWS::Macie::FindingsFilter, and AWS::Macie::Session 

 [AWS::Macie::CustomDataIdentifier](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-macie-customdataidentifier.html)   
Use the `AWS::Macie::CustomDataIdentifier` resource to create a custom data identifier in Amazon Macie\. 

 [AWS::Macie::FindingsFilter](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-macie-findingsfilter.html)   
Use the `AWS::Macie::FindingsFilter` resource to create a custom filter for findings in Amazon Macie\. 

 [AWS::Macie::Session](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-macie-session.html)   
Use the `AWS::Macie::Session` resource to enable Amazon Macie\.  | May 14, 2020 | 
| [Updated resource](AWS_IoTEvents.md) | The following resource was updated: AWS::IoTEvents::DetectorModel\. 

 [ AWS::IoTEvents::DetectorModel](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-iotevents-detectormodel.html)   
Added the following properties: `AssetPropertyTimestamp`, `AssetPropertyValue`, `AssetPropertyVariant`, `DynamoDB`, `DynamoDBv2`, `IotSiteWise`, and `Payload`\.  
Updated the following property: `SetTimer`\.  | May 7, 2020 | 
| [Updated resource](AWS_SSM.md) | The following resource was updated: AWS::SSM::Association 

 [AWS::SSM::Association](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ssm-association.html)   
Use the `WaitForSuccessTimeoutSeconds` property to specify the number of seconds the service should wait for the association status to show "Success" before proceeding with the stack execution\. If the association status doesn't show "Success" after the specified number of seconds, then stack creation fails\.  | May 7, 2020 | 
| [New resource](AWS_ImageBuilder.md) | The following resource was added: AWS::ImageBuilder::Image\. 

 [AWS::ImageBuilder::Image](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-imagebuilder-image.html)   
Use the `AWS::ImageBuilder::Image` resource to create an image in the EC2 Image Builder service\.  | May 7, 2020 | 
| [Updated resource](AWS_Synthetics.md) | The following resource was updated: AWS::Synthetics::Canary\. 

 [AWS::Synthetics::Canary](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-synthetics-canary.html)   
Use the `Name` property to specify the name for this canary\.  | April 30, 2020 | 
| [New resource](AWS_EventSchemas.md) | The following resource was added: `AWS::EventSchemas::RegistryPolicy`\. 

 [AWS::EventSchemas::RegistryPolicy](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-eventschemas-registrypolicy.html)   
Use the `AWS::EventSchemas::RegistryPolicy` resource to specify a resource\-based policy associated with a schema registry\.   | April 30, 2020 | 
| [Updated resource](AWS_FSx.md) | The following resource was updated: AWS::FSx::FileSystem 

[AWS::FSx::FileSystem](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-fsx-filesystem.html)  
Use the `LustreMountName` attribute when mounting an Amazon FSx for Lustre file system\.  | April 23, 2020 | 
| [New resources](AWS_ImageBuilder.md) | The following resources were added: AWS::ImageBuilder::Component, AWS::ImageBuilder::DistributionConfiguration, AWS::ImageBuilder::ImagePipeline, AWS::ImageBuilder::ImageRecipe, and AWS::ImageBuilder::InfrastructureConfiguration\. 

 [AWS::ImageBuilder::Component](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-imagebuilder-component.html)   
Use the `AWS::ImageBuilder::Component` resource to create a component in the EC2 Image Builder service\. 

 [AWS::ImageBuilder::DistributionConfiguration](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-imagebuilder-distributionconfiguration.html)   
Use the `AWS::ImageBuilder::DistributionConfiguration` resource to create a distribution configuration in the EC2 Image Builder service\. 

 [AWS::ImageBuilder::ImagePipeline](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-imagebuilder-imagepipeline.html)   
Use the `AWS::ImageBuilder::ImagePipeline` resource to create an image pipeline in the EC2 Image Builder service\. 

 [AWS::ImageBuilder::ImageRecipe](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-imagebuilder-imagerecipe.html)   
Use the `AWS::ImageBuilder::ImageRecipe` resource to create an image recipe in the EC2 Image Builder service\.  

 [AWS::ImageBuilder::InfrastructureConfiguration](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-imagebuilder-infrastructureconfiguration.html)   
Use the `AWS::ImageBuilder::InfrastructureConfiguration` resource to create an infrastructure configuration in the EC2 Image Builder service\.  | April 23, 2020 | 
| [New resource](AWS_CE.md) | The following resource was added: AWS::CE::CostCategory 

 [AWS::CE::CostCategory](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/AWS_CE.html)   
Use the `AWS::CE::CostCategory` resource to create groupings of costs that you can use across products in the AWS Billing and Cost Management console\.  | April 23, 2020 | 
| [New resource](AWS_Synthetics.md) | The following resource was added: AWS::Synthetics::Canary\. 

 [AWS::Synthetics::Canary](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-synthetics-canary.html)   
Use the `AWS::Synthetics::Canary` resource to create a canary\. Canaries are configurable scripts that run on a schedule and monitor your endpoints and APIs\. By using canaries, you can discover issues before your customers do\.  | April 23, 2020 | 
| [Updated resource](AWS_Glue.md) | The following resource was updated: AWS::Glue::DevEndpoint 

 [AWS::Glue::DevEndpoint](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-glue-devendpoint.html)   
Use the `PublicKeys` property to specify a list of public keys to be used by a development endpoint for authentication\.  | April 16, 2020 | 
| [Updated resource](AWS_Glue.md) | The following resource was updated: AWS::Glue::MLTransform 

 [AWS::Glue::MLTransform](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-glue-mltransform.html)   
Use the `Tags` property to specify the AWS resource tags to use to manage access to a machine learning transform\.  | April 16, 2020 | 
| [New resource](AWS_ResourceGroups.md) | The following resource was added: AWS::ResourceGroups::Group 

 [AWS::ResourceGroups::Group](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-resourcegroups-group.html)   
Use the `AWS::ResourceGroups::Group` resource to create a resource group with the specified name, description, and resource query\.  | April 16, 2020 | 
| [Updated resource](AWS_CloudWatch.md) | The following resource was updated: AWS::CloudWatch::InsightRule\. 

 [AWS::CloudWatch::InsightRule](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-cloudwatch-insightrule.html)   
The AWS::CloudWatch::InsightRule resource now supports tags\. Use the AWS::CloudWatch::InsightRule resource to create Contributor Insights rules\. For more information, see [ Using Contributor Insights to Analyze High\-Cardinality Data](https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/ContributorInsights.html)\.  | April 2, 2020 | 
| [Updated resource](AWS_FSx.md) | The following resource was updated: AWS::FSx::FileSystem 

[AWS::FSx::FileSystem](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-fsx-filesystem.html)  
Use the `StorageType` property to specify the type of storage for the file system, either solid state drive, `SSD` or hard disk drive, `HDD`\.  
In the [WindowsConfiguration](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-fsx-filesystem-windowsconfiguration.html) property type, use the `DeploymentType` property to specify a new Amazon FSx for Windows File Server file system deployment type, `SINGLE_AZ_2`, the latest generation of Single\-AZ file systems\.  | April 2, 2020 | 
| [Updated resource](AWS_ServiceCatalog.md) | The following resource was updated: AWS::ServiceCatalog::LaunchRoleConstraint\. 

 [AWS::ServiceCatalog::LaunchRoleConstraint](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-servicecatalog-launchroleconstraint.html)   
Use the `LocalRoleName` property to specify an IAM role to use when an account uses a launch constraint\.  | April 2, 2020 | 
| [Updated resource](AWS_ApiGatewayV2.md) | The following resource was updated: `AWS::ApiGatewayV2::Integration`\. 

 [AWS::ApiGatewayV2::Integration](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-apigatewayv2-integration.html)   
Use the `AWS::ApiGatewayV2::Integration` resource to create a private integration for an HTTP API\.  | March 26, 2020 | 
| [Updated resource](AWS_AutoScaling.md) | The following resource was updated: AWS::AutoScaling::AutoScalingGroup\. 

 [AWS::AutoScaling::AutoScalingGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-as-group.html)   
Use the `MaxInstanceLifetime` property to specify the maximum amount of time, in seconds, that an instance can be in service\.  | March 26, 2020 | 
| [Updated resource](AWS_Cognito.md) | The following resource was updated: AWS::Cognito::UserPool 

 [AWS::Cognito::UserPool](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-cognito-userpool.html)   
Use the `UsernameConfiguration` property to set case sensitivity on the username input for the selected sign\-in option\.  | March 26, 2020 | 
| [Updated resource](AWS_EC2.md) | The following resource was updated: AWS::EC2::Volume 

 [AWS::EC2::Volume](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ec2-ebs-volume.html)   
Use the `MultiAttachEnabled` property to indicate whether Amazon EBS Multi\-Attach is enabled\.  | March 26, 2020 | 
| [Updated resource](AWS_RDS.md) | The following resource was updated: AWS::RDS::DBInstance 

 [AWS::RDS::DBInstance](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-rds-database-instance.html)   
The `AWS::RDS::DBInstance` resource now supports Read Replica across multiple Availability Zone deployments\.  | March 26, 2020 | 
| [New resources](AWS_Detective.md) | The following resources were added: AWS::Detective::Graph and AWS::Detective::MemberInvitation 

 [AWS::Detective::Graph](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-detective-graph.html)   
Use the `AWS::Detective::Graph` resource to specify a Detective behavior graph\. 

 [AWS::Detective::MemberInvitation](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-detective-memberinvitation.html)   
Use the `AWS::Detective::MemberInvitation` resource to send an invitation to join a Detective behavior graph\.  | March 26, 2020 | 
| [Updated resource](AWS_EC2.md) | The following resource was updated: AWS::EC2::ClientVpnEndpoint\. 

 [AWS::EC2::ClientVpnEndpoint](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-clientvpnendpoint.html)   
Use the `VpcId` and `SecurityGroupIds` properties to assign security groups to your Client VPN endpoint\.  | March 19, 2020 | 
| [New resources](AWS_NetworkManager.md) | The following resources were added: AWS::NetworkManager::CustomerGatewayAssociation, AWS::NetworkManager::Device, AWS::NetworkManager::GlobalNetwork, AWS::NetworkManager::Link, AWS::NetworkManager::LinkAssociation, AWS::NetworkManager::Site, and AWS::NetworkManager::TransitGatewayRegistration 

 [AWS::NetworkManager::CustomerGatewayAssociation](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-networkmanager-customergatewayassociation.html)   
Use the `AWS::NetworkManager::CustomerGatewayAssociation` resource to specify an association between a customer gateway, device, and link\.  

 [AWS::NetworkManager::Device](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-networkmanager-device.html)   
Use the `AWS::NetworkManager::Device` resource to specify a device in a global network\.  

 [AWS::NetworkManager::GlobalNetwork](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-networkmanager-globalnetwork.html)   
Use the `AWS::NetworkManager::GlobalNetwork` resource to specify a global network\.  

 [AWS::NetworkManager::Link](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-networkmanager-link.html)   
Use the `AWS::NetworkManager::Link` resource to specify a link for a site\.  

 [AWS::NetworkManager::LinkAssociation](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-networkmanager-linkassociation.html)   
Use the `AWS::NetworkManager::LinkAssociation` resource to specify an association between a device and a link\.  

 [AWS::NetworkManager::Site](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-networkmanager-site.html)   
Use the `AWS::NetworkManager::Site` resource to specify a site in a global network\.  

 [AWS::NetworkManager::TransitGatewayRegistration](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-networkmanager-transitgatewayregistration.html)   
Use the `AWS::NetworkManager::TransitGatewayRegistration` resource to specify the registration of a transit gateway in a global network\.  | March 19, 2020 | 
| [New resource](AWS_CodeGuruProfiler.md) | The following resource was added: `AWS::CodeGuruProfiler::ProfilingGroup`\. 

 [AWS::CodeGuruProfiler::ProfilingGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-codeguruprofiler-profilinggroup.html)   
Use the `AWS::CodeGuruProfiler::ProfilingGroup` resource to create a profiling group\.  | March 19, 2020 | 
| [New resources](AWS_Cassandra.md) | The following resources were added: `AWS::Cassandra::Keyspace` and `AWS::Cassandra::Table`\. 

 [AWS::Cassandra::Keyspace](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-cassandra-keyspace.html)   
Use the `AWS::Cassandra::Keyspace` resource to create a new keyspace in Amazon Keyspaces \(for Apache Cassandra\)\. 

 [AWS::Cassandra::Table](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-cassandra-table.html)   
Use the `AWS::Cassandra::Table` resource to create a new table in Amazon Keyspaces \(for Apache Cassandra\)\.  | March 16, 2020 | 
| [Updated resource](AWS_AppMesh.md) | The following resources were updated: AWS::AppMesh::VirtualNode, AWS::AppMesh::VirtualRouter, AWS::AppMesh::VirtualService, and AWS::AppMesh::Route 

 [AWS::AppMesh::VirtualNode](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-appmesh-virtualnode.html)   
Use the `MeshOwner` property to specify the account ID that owns a shared mesh\. 

 [AWS::AppMesh::Route](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-appmesh-route.html)   
Use the `MeshOwner` property to specify the account ID that owns a shared mesh\. 

 [AWS::AppMesh::VirtualRouter](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-appmesh-virtualrouter.html)   
Use the `MeshOwner` property to specify the account ID that owns a shared mesh\. 

 [AWS::AppMesh::VirtualService](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-appmesh-virtualservice.html)   
Use the `MeshOwner` property to specify the account ID that owns a shared mesh\.  | March 12, 2020 | 
| [Updated resource](AWS_MSK.md) | The following resource was updated: AWS::MSK::Cluster 

 [AWS::MSK::Cluster](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-msk-cluster.html)   
Use the `LoggingInfo` to stream broker logs to one or more of the following destination types: Amazon CloudWatch Logs, Amazon S3, Amazon Kinesis Data Firehose\.  | March 12, 2020 | 
| [New and updated resources](AWS_ApiGatewayV2.md) | The following resources were added or updated: `AWS::ApiGatewayV2::ApiGatewayManagedOverrides`, `AWS::ApiGatewayV2::Integration`, and `AWS::ApiGatewayV2::VpcLink`\. 

 [AWS::ApiGatewayV2::ApiGatewayManagedOverrides](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-apigatewayv2-apigatewaymanagedoverrides.html)   
Use the `AWS::ApiGatewayV2::ApiGatewayManagedOverrides` resource to override the default properties of API Gateway managed resources\. 

 [AWS::ApiGatewayV2::Integration](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-apigatewayv2-integration.html)   
Use the `AWS::ApiGatewayV2::Integration` resource to create a private integration for an HTTP API\. 

 [AWS::ApiGatewayV2::VpcLink](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-apigatewayv2-vpclink.html)   
Use the `AWS::ApiGatewayV2::VpcLink` resource to create a VPC link for an HTTP API\.  | March 12, 2020 | 
| [Updated resources](AWS_Greengrass.md) | The following resources were updated: AWS::Greengrass::ResourceDefinition and AWS::Greengrass::ResourceDefinitionVersion 

 [AWS::Greengrass::ResourceDefinition](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-greengrass-resourcedefinition.html)   
In the [ S3MachineLearningModelResourceData](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-greengrass-resourcedefinition-s3machinelearningmodelresourcedata.html) property type that defines a resource instance, use the `OwnerSetting` property to specify the Linux OS group owner and permissions for the downloaded machine learning resource\.  
In the [ SageMakerMachineLearningModelResourceData](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-greengrass-resourcedefinition-sagemakermachinelearningmodelresourcedata.html) property type that defines a resource instance, use the `OwnerSetting` property to specify the Linux OS group owner and permissions for the downloaded machine learning resource\. 

 [AWS::Greengrass::ResourceDefinitionVersion](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-greengrass-resourcedefinitionversion.html)   
In the [ S3MachineLearningModelResourceData](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-greengrass-resourcedefinitionversion-s3machinelearningmodelresourcedata.html) property type that defines a resource instance, use the `OwnerSetting` property to specify the Linux OS group owner and permissions for the downloaded machine learning resource\.  
In the [ SageMakerMachineLearningModelResourceData](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-greengrass-resourcedefinitionversion-sagemakermachinelearningmodelresourcedata.html) property type that defines a resource instance, use the `OwnerSetting` property to specify the Linux OS group owner and permissions for the downloaded machine learning resource\.  | March 9, 2020 | 
| [Updated resource](AWS_CloudFront.md) | The following resource was updated: AWS::CloudFront::Distribution\. 

 [AWS::CloudFront::Distribution](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-cloudfront-distribution.html)   
In the [DistributionConfig](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-cloudfront-distribution-distributionconfig.html) property type, use the `OriginGroups` property to specify information about origin groups for this distribution\.  | March 5, 2020 | 
| [Updated resource](AWS_EKS.md) | The following resource was updated to support envelope encryption of secrets with AWS KMS: AWS::EKS::Cluster 

 [AWS::EKS::Cluster EncryptionConfig](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-eks-cluster-encryptionconfig.html)   
Use the `AWS::EKS::Cluster EncryptionConfig` property to specify the encryption configuration for a Amazon EKS cluster\. 

 [AWS::EKS::Cluster Provider](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-eks-cluster-provider.html)   
Use the `AWS::EKS::Cluster Provider` property to specify the AWS Key Management Service \(AWS KMS\) customer master key \(CMK\) used to encrypt the secrets for a Amazon EKS cluster\.  | March 5, 2020 | 
| [New resource](AWS_Athena.md) | The following resource was added: AWS::Athena::WorkGroup 

 [AWS::Athena::WorkGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-athena-workgroup.html)   
Use the `AWS::Athena::WorkGroup` resource to separate users, teams, applications, or workloads, set limits on the amount of data the workgroup or its queries can process, and track costs\.  | March 5, 2020 | 
| [New resource](AWS_Chatbot.md) | The following resource was added: AWS::Chatbot::SlackChannelConfiguration 

 [AWS::Chatbot::SlackChannelConfiguration](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/AWS_Chatbot.html)   
Use the `AWS::Chatbot::SlackChannelConfiguration` resource to configure a Slack channel with AWS Chatbot\.  | March 5, 2020 | 
| [New resource](AWS_CodeStarConnections.md) | The following resource was added: AWS::CodeStarConnections::Connection 

 [AWS::CodeStarConnections::Connection](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-codestarconnections-connection.html)   
Use the `AWS::CodeStarConnections::Connection` resource to specify Connection\.  | March 5, 2020 | 
| [New resource](AWS_CloudWatch.md) | The following resource was added: AWS::CloudWatch::CompositeAlarm\. 

 [AWS::CloudWatch::CompositeAlarm](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-cloudwatch-compositealarm.html)   
Use the `AWS::CloudWatch::CompositeAlarm` property to create a composite alarm\. Composite alarms evaluate their alarm state based on the alarm states of other CloudWatch rules\.  | March 2, 2020 | 
| [Updated resource](AWS_AppMesh.md) | The following resource was updated: AWS::AppMesh::VirtualNode 

 [AWS::AppMesh::VirtualNode](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-appmesh-virtualnode.html)   
Use the `BackendDefaults` property to specify a client policy for a backend\.  
Use the `ClientPolicy` property to specify a client policy\.  
Use the `ClientPolicyTls` property to specify a Transport Layer Security \(TLS\) client policy\.  
Use the `ListenerTls` property to specify a TLS listener\.  
Use the `ListenerTlsCertificate` property to specify the type of certificate to use for a client policy\.  
Use the `ListenerTlsAcmCertificate` property to specify an AWS Certificate Manager certificate\.  
Use the `ListenerTlsFileCertificate` property to specify properties of a local file certificate\.  
Use the `TlsValidationContext` property to specify a TLS validation context trust\.  
Use the `TlsValidationContextAcmTrust` property to specify a context trust for an AWS Certificate Manager certificate\.  
Use the `TlsValidationContextFileTrust` property to specify a file that contains the certificate trust chain for a local file certificate\.  
Use the `TlsValidationContextTrust` property to specify a TLS validation context trust\.  
Use the `VirtualNodeSpec` property to specify `BackendDefaults`\.  
Use the `Listener` property to specify a `ListenerTls`\.  | February 27, 2020 | 
| [Updated resource](AWS_FSx.md) | The following resource was updated: AWS::FSx::FileSystem 

[AWS::FSx::FileSystem](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-fsx-filesystem.html)  
In the [LustreConfiguration](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-fsx-filesystem-lustreconfiguration.html) property type:  
+ Use the `DeploymentType` property to specify the Amazon FSx for Lustre file system deployment type, either `PERSISTENT_1`, `SCRATCH_2`, or `SCRATCH_1`\.
+ Use the `PerUnitStorageThroughput` property to specify the throughput in MB/s/TiB for a `PERSISTENT_1` Amazon FSx for Lustre file system deployment type\.  | February 27, 2020 | 
| [New resources](AWS_GroundStation.md) | The following resources were added: AWS::GroundStation::Config, AWS::GroundStation::DataflowEndpointGroup, and AWS::GroundStation::MissionProfile 

 [AWS::GroundStation::Config](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-groundstation-config.html)   
Use the `AWS::GroundStation::Config` resource to specify a Config with the specified parameters\. 

 [AWS::GroundStation::DataflowEndpointGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-groundstation-dataflowendpointgroup.html)   
Use the `AWS::GroundStation::DataflowEndpointGroup` resource to specify a Dataflow Endpoint Group request\. 

 [AWS::GroundStation::MissionProfile](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-groundstation-missionprofile.html)   
Use the `AWS::GroundStation::MissionProfile` resource to specify parameters and provide references to config objects to define how Ground Station lists and executes contacts\.  | February 27, 2020 | 
| [Updated resource](AWS_CodeBuild.md) | The following resources was updated: AWS::CodeBuild::Project 

 [AWS::CodeBuild::Project](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-codebuild-project.html)   
Use the `ProjectFileSystemLocation` property to specify a file system that your AWS CodeBuild build project mounts\. You use Amazon Elastic File System \(EFS\) to create the file system\. For more information, see [Amazon Elastic File System Sample for CodeBuild](https://docs.aws.amazon.com/codebuild/latest/userguide/sample-efs.html)\.  | February 20, 2020 | 
| [Updated resource](AWS_Neptune.md) | The following resource was updated: AWS::Neptune::DBCluster 

[AWS::Neptune::DBCluster](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-neptune-dbcluster.html)  
Use the `DeletionProtection` property to help prevent inadvertent deletion of your DB cluster\.  
Use the `EngineVersion` property to specify the engine version that your new DB cluster will use\.  | February 18, 2020 | 
| [New resources](AWS_EC2.md) | The following resources were added: AWS::EC2::LocalGatewayRoute and AWS::EC2::LocalGatewayRouteTableVPCAssociation\. 

 [AWS::EC2::LocalGatewayRoute](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-localgatewayroute.html)   
Use the `LocalGatewayRoute` resource to associate the specified VPC with the specified local gateway route table\. 

 [AWS::EC2::LocalGatewayRouteTableVPCAssociation](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-localgatewayroutetablevpcassociation.html)   
Use the `LocalGatewayRouteTableVPCAssociation` resource to associate the specified VPC with the specified local gateway route table\.  | February 14, 2020 | 
| [Updated resources](AWS_ElasticLoadBalancingV2.md) | The following resource were updated: AWS::ElasticLoadBalancingV2::Listener and AWS::ElasticLoadBalancingV2::ListenerRule 

 [AWS::ElasticLoadBalancingV2::Listener](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-elasticloadbalancingv2-listener.html)   
In the [Action](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-elasticloadbalancingv2-listener-defaultactions.html) property type, use the `ForwardConfig` property to specify an action that distributes requests among one or more target groups\. 

 [AWS::ElasticLoadBalancingV2::ListenerRule](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-elasticloadbalancingv2-listenerrule.html)   
In the [Action](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-elasticloadbalancingv2-listenerrule-actions.html) property type, use the `ForwardConfig` property to specify an action that distributes requests among one or more target groups\.  | February 13, 2020 | 
| [New resource ](AWS_Config.md) | The following resources was added: AWS::Config::ConformancePack 

 [ AWS::Config::ConformancePack](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-config-conformancepack.html)   
Use the `AWS::Config::ConformancePack` resource to create a Conformance Pack that is a collection of AWS Config rules that can be easily deployed in an account and a region and across AWS Organization\.  | February 13, 2020 | 
| [New resource ](AWS_Config.md) | The following resources was added: AWS::Config::OrganizationConformancePack 

 [ AWS::Config::OrganizationConformancePack](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-config-organizationconformancepack.html)   
Use the `AWS::Config::OrganizationConformancePack` resource to create an OrganizationConformancePack that has information about conformance packs that AWS Config creates in the member accounts\.  | February 13, 2020 | 
| [New resource](AWS_FMS.md) | The following resources were added: AWS::FMS::NotificationChannel and AWS::FMS::Policy 

 [AWS::FMS::NotificationChannel](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-fms-notificationchannel.html)   
Use the `AWS::FMS::NotificationChannel` resource to designate the IAM role and Amazon Simple Notification Service \(SNS\) topic that AWS Firewall Manager uses to record SNS logs\. 

 [AWS::FMS::Policy](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-fms-policy.html)   
Use the `AWS::FMS::Policy` resource to specify an AWS Firewall Manager policy\.  | February 13, 2020 | 
| [AWS CloudFormation StackSets integrates with AWS Organizations](#ReleaseHistory) | Use StackSets to centrally manage deployments to all the accounts in your organization or specific organizational units \(OUs\) in AWS Organizations\. You can enable automatic deployments to any new accounts added to your organization or OUs\. The permissions needed to deploy across accounts will automatically be handled by StackSets\. For more information, see [Working with AWS CloudFormation StackSets](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/what-is-cfnstacksets.html)\. | February 11, 2020 | 
| [Updated resources](AWS_EC2.md) | The following resources were updated: AWS::EC2::LaunchTemplate and AWS::EC2::ClientVpnEndpoint 

 [AWS::EC2::LaunchTemplate](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-launchtemplate.html)   
Use the `MetadataOptions` property to configure the Instance Metadata Service \(IMDS\) for the instance\.  
Use the `HostResourceGroupArn` property to specify the ARN of the host resource group in which to launch the instances\.  
Use the `PartitionNumber` property to specify a target partition in a partition placement group\.  
Use the `LaunchTemplateElasticInferenceAccelerator` property to specify the number of elastic inference accelerators to attach to the instance\. 

 [AWS::EC2::ClientVpnEndpoint](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-clientvpnendpoint.html)   
Use the `VpnPort` property to assign a port number for TCP and UDP traffic\.  | February 6, 2020 | 
| [Updated resource](AWS_AppSync.md) | The following resource was updated: AWS::AppSync::GraphQLApi\. 

 [AWS::AppSync::GraphQLApi](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-appsync-graphqlapi.html)   
When the property `xrayEnabled` is set to `TRUE`, X\-Ray tracing is enabled for this `GraphqlApi`\.  | February 6, 2020 | 
| [Updated resource](AWS_Cognito.md) | The following resource was updated: AWS::Cognito::UserPool 

 [AWS::Cognito::UserPool](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-cognito-userpool.html)   
Added `AccountRecoverySetting` parameter to define which verified available method a user can use to recover their password\.  | February 6, 2020 | 
| [Updated resource](AWS_OpsWorksCM.md) | The following resource was updated: AWS::OpsWorksCM::Server 

 [AWS::OpsWorksCM::Server](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-opsworkscm-server.html)   
Use the `Tags` property to add tag keys and values to an AWS OpsWorks for Chef Automate or AWS OpsWorks for Puppet Enterprise server\.  | February 6, 2020 | 
| [New resource](AWS_WAFv2.md) | The following resource was added: AWS::WAFv2::WebACLAssociation\. 

 [AWS WAFv2](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/AWS_WAFv2.html)   
Use the web ACL association to define an association between a Web ACL and a regional application resource, to protect the resource\. A regional application can be an Application Load Balancer \(ALB\), Amazon API Gateway REST API, or an AWS AppSync GraphQL API\. For CloudFront distributions, you use AWS::CloudFront::Distribution to manage the association\.   | February 6, 2020 | 
| [Updated resources](AWS_Pinpoint.md) | The following resources were updated: AWS::Pinpoint::EmailTemplate, AWS::Pinpoint::PushTemplate, and AWS::Pinpoint::SmsTemplate 

 [AWS::Pinpoint::EmailTemplate](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-pinpoint-emailtemplate.html)   
Use the `DefaultSubstitutions` property to specify the default values to use for message variables in a message template\. Use the `TemplateDescription` property to specify a custom description of a message template\. 

 [AWS::Pinpoint::PushTemplate](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-pinpoint-pushtemplate.html)   
Use the `DefaultSubstitutions` property to specify the default values to use for message variables in a message template\. Use the `TemplateDescription` property to specify a custom description of a message template\. 

 [AWS::Pinpoint::SmsTemplate](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-pinpoint-smstemplate.html)   
Use the `DefaultSubstitutions` property to specify the default values to use for message variables in a message template\. Use the `TemplateDescription` property to specify a custom description of a message template\.  | January 23, 2020 | 
| [New resources](AWS_ACMPCA.md) | The following resources were added: AWS::ACMPCA::Certificate, AWS::ACMPCA::CertificateAuthority, and AWS::ACMPCA::CertificateAuthorityActivation\. 

 [AWS::ACMPCA::Certificate](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-acmpca-certificate.html)   
The `AWS::ACMPCA::Certificate` resource is used to issue a certificate using your private certificate authority\. 

 [AWS::ACMPCA::CertificateAuthority](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-acmpca-certificateauthority.html)   
Use the `AWS::ACMPCA::CertificateAuthority` resource to create a private CA\.  

 [AWS::ACMPCA::CertificateAuthorityActivation](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-acmpca-certificateauthorityactivation.html)   
The `AWS::ACMPCA::CertificateAuthorityActivation` resource creates and installs a CA certificate on a CA\.   | January 23, 2020 | 
| [New resource](AWS_AppConfig.md) | The following resources were added: AWS::AppConfig::Application, AWS::AppConfig::ConfigurationProfile, AWS::AppConfig::Deployment, AWS::AppConfig::Environment, and AWS::AppConfig::DeploymentStrategy 

 [AWS::AppConfig::Application](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-appconfig-application.html)   
The `AWS::AppConfig::Application` resource creates an application, which is a logical unit of code that provides capabilities for your customers\. 

 [AWS::AppConfig::ConfigurationProfile](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-appconfig-configurationprofile.html)   
The `AWS::AppConfig::ConfigurationProfile` resource creates a configuration profile that enables AppConfig to access the configuration source\.  

 [AWS::AppConfig::Deployment](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-appconfig-deployment.html)   
The `AWS::AppConfig::Deployment` resource starts a deployment\.  

 [AWS::AppConfig::Environment](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-appconfig-environment.html)   
The `AWS::AppConfig::Environment` resource creates an environment, which is a logical deployment group of AppConfig targets, such as applications in a `Beta` or `Production` environment\. 

 [AWS::AppConfig::DeploymentStrategy](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-appconfig-deploymentstrategy.html)   
The `AWS::AppConfig::DeploymentStrategy` resource creates an AppConfig deployment strategy\.   | January 23, 2020 | 
| [Updated resources](AWS_Lambda.md) | The following resource was updated: AWS::Lambda::Function\. 

 [AWS::Lambda::Function](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-lambda-function.html)   
In the [Code](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-lambda-function-code.html) property type, `ZipFile` supports `nodejs12.x` for `RunTime`\.  | January 16, 2020 | 
| [Updated resource](AWS_AutoScaling.md) | The following resource was updated: AWS::AutoScaling::AutoScalingGroup\. 

 [AWS::AutoScaling::AutoScalingGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-as-group.html)   
Use the `WeightedCapacity` property to specify the number of capacity units, which gives the instance type a proportional weight to other instance types\.  | January 16, 2020 | 
| [Updated resource](AWS_EC2.md) | The following resource was updated: AWS::EC2::Instance\. 

 [AWS::EC2::Instance](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ec2-instance.html)   
Use the `HibernationOptions` property to indicate whether the instance is enabled for hibernation\.  
Use the `HostResourceGroupArn` property to specify the ARN of the host resource group in which to launch the instances\.  | January 16, 2020 | 
| [Updated resource](AWS_LakeFormation.md) | The following resource was updated: AWS::LakeFormation::Permissions 

 [AWS::LakeFormation::Permissions](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-lakeformation-permissions.html)   
Use the `DataLocationResource` property to specify a structure for a data location object where permissions are granted or revoked\.  
Use the `TableWithColumnsResource` property to specify a structure for a table with columns object\. This object is only used when granting a SELECT permission\.  | January 16, 2020 | 
| [Updated resource](AWS_RDS.md) | The following resource was updated: AWS::RDS::DBInstance\. 

 [AWS::RDS::DBInstance](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-rds-database-instance.html)   
Use the `CACertificateIdentifier` property to specify the identifier of the CA certificate for this DB instance\.  | January 16, 2020 | 
| [Updated resource](AWS_SSM.md) | The following resource was updated: AWS::SSM::ResourceDataSync 

 [AWS::SSM::ResourceDataSync](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ssm-resourcedatasync.html)   
Use the `SyncType` property with `SyncFromSource` to synchronize Systems Manager Explorer OpsItems and OpsData from AWS Organizations or from multiple AWS Regions\.  | January 16, 2020 | 
| [Updated resources](#ReleaseHistory) | The following resources were updated: AWS::MSK::Cluster, AWS::RDS::DBInstance, and AWS::SSM::Document 

 [AWS::MSK::Cluster](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-msk-cluster.html)   
Use the `OpenMonitoring` property to enable monitoring with Prometheus, an open\-source monitoring system for time\-series metric data\. You can also use tools that are compatible with Prometheus\-formatted metrics or tools that integrate with Amazon MSK Open Monitoring\. 

 [AWS::SSM::Document](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ssm-document.html)   
Use the `Name` property to specify a name for the Systems Manager document\. 

 [AWS::RDS::DBInstance](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-rds-database-instance.html)   
Use the `MaxAllocatedStorage` property to specify the upper limit to which Amazon RDS can automatically scale the storage of the DB instance\.  | December 20, 2019 | 
| [New resource](#ReleaseHistory) | The following resource was added: AWS::CodeBuild::ReportGroup 

 [AWS::CodeBuild::ReportGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-codebuild-reportgroup.html)   
Use the `AWS::CodeBuild::ReportGroup` resource to specify information about a report group\. When you specify a report group in a CodeBuild project, a build of the project creates reports in the report group that contain results from running test cases\.  | December 20, 2019 | 
| [New resource](#ReleaseHistory) | The following resource was added: AWS::EC2::GatewayRouteTableAssociation\. 

 [AWS::EC2::GatewayRouteTableAssociation](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-gatewayroutetableassociation.html)   
Use the `AWS::EC2::GatewayRouteTableAssociation` property to associate a virtual private gateway or internet gateway with a route table\.  | December 20, 2019 | 
| [Updated resources](AWS_RDS.md) | The following resource was updated: AWS::RDS::DBInstance\. 

 [AWS::RDS::DBInstance](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-rds-database-instance.html)   
Use the `MaxAllocatedStorage` property to specify the upper limit to which Amazon RDS can automatically scale the storage of the DB instance\.  | December 19, 2019 | 
| [Updated resource](AWS_FSx.md) | The following resource was updated: AWS::FSx::FileSystem  

 [AWS::FSx::FileSystem](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-fsx-filesystem.html)   
In the [WindowsConfiguration](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-fsx-filesystem-windowsconfiguration.html) property type:  
+ Use the `DeploymentType` property to specify the Amazon FSx Windows file system deployment type\.
+ Use the `PreferredSubnetId` property to specify the subnet in which you want the preferred file server to be located for a `MULTI_AZ_1` Amazon FSx for Windows file system deployment type\.  | December 19, 2019 | 
| [Updated resource](#ReleaseHistory) | The following resource was updated: AWS::FSx::FileSystem  

 [AWS::FSx::FileSystem](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-fsx-filesystem.html)   
In the [WindowsConfiguration](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-fsx-filesystem-windowsconfiguration.html) property type:  
+ Use the `DeploymentType` property to specify the file system deployment type\.
+ Use the `PreferredSubnetId` property to specify the subnet in which you want the preferred file server to be located\.  | December 19, 2019 | 
| [New resource](AWS_EC2.md) | The following resource was added: AWS::EC2::GatewayRouteTableAssociation\. 

 [AWS::EC2::GatewayRouteTableAssociation](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-gatewayroutetableassociation.html)   
Use the `AWS::EC2::GatewayRouteTableAssociation` property to associate a virtual private gateway or internet gateway with a route table\.  | December 19, 2019 | 
| [Updated resource](#ReleaseHistory) | The following resource was updated: AWS::EC2::Instance\. 

 [AWS::EC2::Instance](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ec2-instance.html)   
In the [ElasticInferenceAccelerator](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ec2-instance-elasticinferenceaccelerator.html) property type, use the `Count` property to specify the number of elastic inference accelerators to attach to the instance\.  | December 12, 2019 | 
| [New resource](AWS_CodeBuild.md) | The following resource was added: AWS::CodeBuild::ReportGroup 

 [AWS::CodeBuild::ReportGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-codebuild-reportgroup.html)   
Use the `AWS::CodeBuild::ReportGroup` resource to specify information about a report group\. When you specify a report group in a CodeBuild project, a build of the project creates reports in the report group that contain results from running test cases\.  | December 12, 2019 | 
| [Updated resources](AWS_ApiGatewayV2.md) | The following resources were updated: `AWS::ApiGatewayV2::Api`, `AWS::ApiGatewayV2::Authorizer`, `AWS::ApiGatewayV2::Integration`, `AWS::ApiGatewayV2::Stage`\. 

 [AWS::ApiGatewayV2::Api](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-apigatewayv2-api.html)   
Use the `AWS::ApiGatewayV2::Api` resource to create an HTTP API \(beta\)\. 

 [AWS::ApiGatewayV2::Authorizer](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-apigatewayv2-authorizer.html)   
Use the `AWS::ApiGatewayV2::Authorizer` resource to create a JWT authorizer for an HTTP API \(beta\)\. 

 [AWS::ApiGatewayV2::Integration](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-apigatewayv2-integration.html)   
Use the `AWS::ApiGatewayV2::Integration` resource to create an integration for an HTTP API \(beta\)\. 

 [AWS::ApiGatewayV2::Stage](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-apigatewayv2-stage.html)   
Use the `AWS::ApiGatewayV2::Stage` resource to create a stage for an HTTP API \(beta\)\.  | December 4, 2019 | 
| [Updated resources](AWS_Lambda.md) | The following resources were updated: AWS::Lambda::Alias and AWS::Lambda::Version\. 

 [AWS::Lambda::Alias](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-lambda-alias.html)   
Use the `ProvisionedConcurrencyConfiguration` property to specify a provisioned concurrency configuration for a function's alias\. 

 [AWS::Lambda::Version](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-lambda-version.html)   
Use the `ProvisionedConcurrencyConfiguration` property to specify a provisioned concurrency configuration for a function's version\.  | December 3, 2019 | 
| [Updated resource](AWS_StepFunctions.md) | The following resource was updated: `AWS::StepFunctions::StateMachine`\. 

 [AWS::StepFunctions::StateMachine](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-stepfunctions-statemachine.html)   
The `AWS::StepFunctions::StateMachine` now supports Express workflows using the new `StateMachineType` parameter\. You can also configure CloudWatch Logging information for Express workflows using `LoggingConfiguration`, `LogDestination`, and `CloudWatchLogsLogGroup`\.   | December 3, 2019 | 
| [New resource](AWS_S3.md) | The following resource was added: AWS::S3::AccessPoint 

 [Access Points](https://docs.aws.amazon.com/AmazonS3/latest/dev/access-points.html)   
Use the `AWS::S3::AccessPoint` resource to specify an S3 access point\.  | December 3, 2019 | 
| [New resource](AWS_AccessAnalyzer.md) | The following resource was added: AWS::AccessAnalyzer::Analyzer 

 [AWS::AccessAnalyzer::Analyzer](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-accessanalyzer-analyzer.html)   
Use the `AWS::AccessAnalyzer::Analyzer` resource to create an analyzer for IAM Access Analyzer\.  | December 2, 2019 | 
| [New resource](AWS_EventSchemas.md) | The following resources were added: `AWS::EventSchemas::Discoverer`, `AWS::EventSchemas::Registry`, and `AWS::EventSchemas::Schema`\. 

 [AWS::EventSchemas::Discoverer](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-eventschemas-discoverer.html)   
Use the `AWS::EventSchemas::Discoverer` resource to specify a discoverer that is associated with an event bus\. A discoverer allows the Amazon EventBridge Schema Registry to automatically generate schemas based on events on an event bus\. 

 [AWS::EventSchemas::Registry](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-eventschemas-registry.html)   
Use the `AWS::EventSchemas::Registry` to specify a schema registry\. Schema registries are containers for Schemas\. Registries collect and organize schemas so that your schemas are in logical groups\. 

 [AWS::EventSchemas::Schema](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-eventschemas-schema.html)   
Use the `AWS::EventSchemas::Schema` resource to specify an event schema\.  | December 1, 2019 | 
| [New resource](AWS_Lambda.md) | The following resource was added: AWS::Lambda::EventInvokeConfig 

 [AWS::Lambda::EventInvokeConfig](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-lambda-eventinvokeconfig.html)   
Use the `EventInvokeConfig` resource to configure destinations and error handling for asynchronous invocation\.  | November 26, 2019 | 
| [Updated resource](AWS_CloudWatch.md) | The following resource was updated: AWS::CloudWatch::Alarm\. 

 [AWS::CloudWatch::Alarm](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-cw-alarm.html)   
In the [MetricDataQuery](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-cloudwatch-alarm-metricdataquery.html) property type, use the `Period` property to specify the granularity, in seconds, of the returned data points\.  | November 25, 2019 | 
| [Updated resource](AWS_CodePipeline.md) | The following resource was updated: AWS::CodePipeline::Pipeline\. 

 [AWS::CodePipeline::Pipeline](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-codepipeline-pipeline.html)   
In the [ActionDeclaration](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-codepipeline-pipeline-stages-actions.html) property type, use the `Namespace` property to specify the variable namespace associated with the action\. All variables produced as output by this action fall under this namespace\.  | November 25, 2019 | 
| [Updated resource](AWS_Lambda.md) | The following resource was updated: AWS::Lambda::EventSourceMapping\. 

 [AWS::Lambda::EventSourceMapping](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-lambda-eventsourcemapping.html)   
For stream sources \(DynamoDB and Kinesis\), use the `BisectBatchOnFunctionError` property to split the batch in two and retry if the function returns an error\.  
For stream sources \(DynamoDB and Kinesis\), use the `DestinationConfig` property to specify an Amazon SQS queue or Amazon SNS topic destination for discarded records\.  
For stream sources \(DynamoDB and Kinesis\), use the `MaximumRecordAgeInSeconds` property to specify the maximum age of a record that Lambda sends to a function for processing\.  
For stream sources \(DynamoDB and Kinesis\), use the `MaximumRetryAttempts` property to specify the maximum number of times to retry when the function returns an error\.  
For stream sources \(DynamoDB and Kinesis\), use the `ParallelizationFactor` property to specify the number of batches to process from each shard concurrently\.  | November 25, 2019 | 
| [Updated resource](#ReleaseHistory) | The following resource was updated: AWS::CloudWatch::Alarm\. 

 [AWS::CloudWatch::Alarm](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-cw-alarm.html)   
In the [MetricDataQuery](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-cloudwatch-alarm-metricdataquery.html) property type, use the `Period` property to specify the granularity, in seconds, of the returned data points\.  | November 25, 2019 | 
| [New resources](AWS_ECS.md) | The following resources were added: AWS::ECS::PrimaryTaskSet, AWS::ECS::TaskSet\. 

 [AWS::ECS::PrimaryTaskSet](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ecs-primarytaskset.html)   
Use the `AWS::ECS::PrimaryTaskSet` resource to specify which task set in a service is the primary task set\. Any parameters that are updated on the primary task set in a service will transition to the service\. This is used when a service uses the `EXTERNAL` deployment controller type\. 

 [AWS::ECS::TaskSet](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ecs-taskset.html)   
Use the `AWS::ECS::TaskSet` resource to create a task set in the specified cluster and service\. This is used when a service uses the `EXTERNAL` deployment controller type\.  | November 25, 2019 | 
| [New resource](AWS_CloudWatch.md) | The following resource was added: AWS::CloudWatch::InsightRule\. 

 [AWS::CloudWatch::InsightRule](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-cloudwatch-insightrule.html)   
Use the `AWS::CloudWatch::InsightRule` property to create a Contributor Insights rule\. Rules evaluate log events in a CloudWatch Logs log group, enabling you to find contributor data for the log events in that log group\.  | November 25, 2019 | 
| [New resource](AWS_WAFv2.md) | The following resource was added: AWS WAFv2 

 [AWS WAFv2](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/AWS_WAFv2.html)   
This is the latest version of AWS WAF, a web application firewall that lets you monitor HTTP\(S\) requests that are forwarded to an Amazon API Gateway REST API, Amazon CloudFront, Application Load Balancer, or an AWS AppSync GraphQL API\. AWS WAF also lets you control access to your content\.  | November 25, 2019 | 
| [Updated resources](AWS_AppSync.md) | The following resource were updated: AWS::AppSync::Resolver, AWS::AppSync::DataSource\. 

 [AWS::AppSync::Resolver](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-appsync-resolver.html)   
Use the `CachingConfig` property to specify the caching behavior of your AWS AppSync resolver\.  

 [AWS::AppSync::Resolver](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-appsync-resolver.html)   
Use the `SyncConfig` property to specify the conflict detection and resolution strategy of your AWS AppSync resolver\.  

 [AWS::AppSync::Resolver](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-appsync-resolver.html)   
Use the `LambdaConflictHandlerConfig` property to specify the ARN of the lambda that is used for handling conflicts in your AWS AppSync resolver\.  

 [AWS::AppSync::DataSource](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-appsync-datasource.html)   
Use the `DeltaSyncConfig` property to specify the delta sync configurations for your versioned AWS AppSync data source\.   | November 21, 2019 | 
| [Updated resources](AWS_ECS.md) | The following resources were updated: AWS::ECS::Cluster, AWS::ECS::Service, and AWS::ECS::TaskDefinition\. 

 [AWS::ECS::Cluster](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ecs-cluster.html)   
Use the `ClusterSettings` property to specify the setting to use when creating a cluster\. This parameter is used to enable CloudWatch Container Insights for a cluster\. 

 [AWS::ECS::Service](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ecs-service.html)   
Use the `DeploymentController` property to specify the deployment controller to use for the service\. 

 [AWS::ECS::TaskDefinition](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ecs-taskdefinition.html)   
In the [ContainerDefinition](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ecs-taskdefinition-containerdefinitions.html) property type, use the `FirelensConfiguration` property to specify the FireLens configuration for the container\. This is used to specify and configure a log router for container logs\.  
In the [LinuxParameters](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ecs-taskdefinition-linuxparameters.html) property type:  
+ use the `MaxSwap` property to specify the total amount of swap memory \(in MiB\) a container can use\.
+ use the `Swappiness` property to tune a container's memory swappiness behavior\. A `swappiness` value of `0` will cause swapping to not happen unless absolutely necessary\. A `swappiness` value of `100` will cause pages to be swapped very aggressively\.  | November 21, 2019 | 
| [Updated resources](AWS_RDS.md) | The following resources were updated: AWS::RDS::DBCluster and AWS::RDS::DBInstance\. 

 [AWS::RDS::DBCluster](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-rds-dbcluster.html)   
Use the `EnableHttpEndpoint` property to indicate whether to enable the HTTP endpoint for an Aurora Serverless DB cluster\. By default, the HTTP endpoint is disabled\. When enabled, the HTTP endpoint provides a connectionless web service API for running SQL queries on the Aurora Serverless DB cluster\. You can also query your database from inside the RDS console with the query editor\. 

 [AWS::RDS::DBInstance](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-rds-database-instance.html)   
For Oracle DB instances, Amazon RDS can use Kerberos Authentication to authenticate users that connect to the DB instance\.  | November 21, 2019 | 
| [Updated resource](AWS_ApiGateway.md) | The following resource was updated: AWS::ApiGateway::RestApi\. 

 [AWS::ApiGateway::RestApi](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-apigateway-restapi.html)   
Use the `VpcEndpointIds` property to specify VPC endpoint IDs of an API \([AWS::ApiGateway::RestApi](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-apigateway-restapi.html)\) against which to create Route53 ALIASes\. It is only supported for `PRIVATE` endpoint type\.  | November 21, 2019 | 
| [Updated resource](AWS_CertificateManager.md) | The following resource was updated: AWS::CertificateManager::Certificate 

 [AWS::CertificateManager::Certificate](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-certificatemanager-certificate.html)   
Use the `CertificateTransparencyLoggingPreference` property to enable or disable certificate transparency logging\.  
Use the `PrivateCertificateAuthorityArn` property to specify an ACM Private CA as certificate issuer\.  
Use the `GetAtt` function to retrieve the `CertificateARN` of the `AWS::CertificateManager::Certificate` resource\.  
Use the `GetAtt` function to retrieve the `CertificateStatus` of the `AWS::CertificateManager::Certificate` resource\.  
In the [DomainValidationOption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-certificatemanager-certificate-domainvalidationoption.html.html) property type, use the `HostedZoneId` property to validate a domain with a Route 53 hosted zone ID\.  | November 21, 2019 | 
| [Updated resource](AWS_Cognito.md) | The following resources were updated: AWS::Cognito::UserPool 

 [AWS::Cognito::UserPool](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-cognito-userpool.html)   
Added `ConfigurationSet` and `From` properties to the `EmailConfiguration` parameter\. 

 [AWS::Cognito::UserPoolClient](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-cognito-userpoolclient.html)   
Added `PreventUserExistenceErrors` parameter to help manage errors and responses when a user does not exist in the user pool\. 

 [AWS::Cognito::UserPoolUser](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-cognito-userpooluser.html)   
Use the `ClientMetadata` parameter to provide input to the AWS Lambda function that is invoked by the *pre sign\-up* trigger\.  | November 21, 2019 | 
| [Updated resource](AWS_EC2.md) | The following resource was updated: AWS::EC2::EIP\. 

 [AWS::EC2::EIP](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ec2-eip.html)   
Use the `Tags` property to specify any tags for the Elastic IP address\.  | November 21, 2019 | 
| [Updated resource](AWS_Elasticsearch.md) | The following resource was updated: AWS::Elasticsearch::Domain\. 

 [AWS::Elasticsearch::Domain](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-elasticsearch-domain.html)   
Use the `CognitoOptions` property to configure Amazon ES to use Amazon Cognito authentication for Kibana\.  
Use the [EnableVersionUpgrade](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-attribute-updatepolicy.html#cfn-attributes-updatepolicy-upgradeelasticsearchversion) update policy to update the `ElasticsearchVersion` property without replacing the `AWS::Elasticsearch::Domain` resource\.  | November 21, 2019 | 
| [Updated resource](AWS_Glue.md) | The following resource was updated: AWS::Glue::MLTransform 

 [AWS::Glue::MLTransform](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-glue-mltransform.html)   
Use the `GlueVersion` property to specify which version of AWS Glue this machine learning transform is compatible with\.  | November 21, 2019 | 
| [Updated resource](AWS_IAM.md) | The following resource was updated: AWS::IAM::User\. 

 [AWS::IAM::User](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-iam-user.html)   
Use the `Tags` property to specify a list of tags that you want to attach to the newly created user\.  | November 21, 2019 | 
| [Updated resource](AWS_OpsWorksCM.md) | The following resource was updated: AWS::OpsWorksCM::Server 

 [AWS::OpsWorksCM::Server](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-opsworkscm-server.html)   
Use the `CustomDomain` property to specify a custom domain on an OpsWorks for Chef Automate Server running Chef Automate 2\.0\.  
Use the `CustomCertificate` property to specify a PEM\-formatted HTTPS certificate for a server with a custom domain\.  
Use the `CustomPrivateKey` property to specify a private key in PEM format for connecting to a server that uses a custom domain\.  | November 21, 2019 | 
| [Updated resource](#ReleaseHistory) | The following resource was updated: AWS::S3::Bucket\. 

 [AWS::S3::Bucket](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-s3-bucket.html)   
In the [Transition](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-s3-bucket-lifecycleconfig-rule-transition.html) property type, the `StorageClass` property supports `DEEP_ARCHIVE`\.  | November 21, 2019 | 
| [Updated resource](#ReleaseHistory) | The following resource was updated: AWS::Lambda::Function\. 

 [AWS::Lambda::Function](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-lambda-function.html)   
In the [Code](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-lambda-function-code.html) property type, `ZipFile` supports `nodejs10.x` for `RunTime`\.  | November 21, 2019 | 
| [New resource](AWS_AppSync.md) | The following resource was added: AWS::AppSync::ApiCache\. 

 [AWS::AppSync::ApiCache](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-appsync-apicache.html)   
Use the `AWS::AppSync::ApiCache` resource to enable resolver caching with AWS AppSync\.  | November 21, 2019 | 
| [Drift Detection for Stack Sets](#ReleaseHistory) | You can now run drift detection on a stack set and all the stack instances it includes\. When CloudFormation performs drift detection on a stack set, it performs drift detection on the stack associated with each stack instance in the stack set\. For more details, see [Detecting Unmanaged Configuration Changes in Stack Sets](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/stacksets-drift.html)\. | November 19, 2019 | 
| [Updated resource](AWS_EKS.md) | The following resource was updated to support Amazon EKS managed node groups: AWS::EKS::Cluster 

 [AWS::EKS::Cluster](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-eks-cluster.html)   
Use the `AWS::EKS::Cluster` resource to create a new Amazon EKS cluster\.  | November 18, 2019 | 
| [New resource](AWS_EKS.md) | The following resource was added: AWS::EKS::Nodegroup 

 [AWS::EKS::Nodegroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-eks-nodegroup.html)   
Use the `AWS::EKS::Nodegroup` resource to create a new Amazon EKS managed node group\.  | November 18, 2019 | 
| [CloudFormation registry now available](#ReleaseHistory) | Use the CloudFormation registry to view private and public resources that are available for use in your CloudFormation account\.For more information, see [Using the CloudFormation Registry](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/registry.html) | November 18, 2019 | 
| [CloudFormation registry API actions](#ReleaseHistory) | The following API actions for managing types in the CloudFormation registry are now available\.For more information about the CloudFormation registry, see [Using the CloudFormation Registry](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/registry.html) 

 [DeregisterType](https://docs.aws.amazon.com/AWSCloudFormation/latest/APIReference/API_DeregisterType.html)   
Removes a type or type version from active use in the CloudFormation registry\. 

 [DescribeType](https://docs.aws.amazon.com/AWSCloudFormation/latest/APIReference/API_DescribeType.html)   
Returns detailed information about a registered type\. 

 [DescribeTypeRegistration](https://docs.aws.amazon.com/AWSCloudFormation/latest/APIReference/API_DescribeTypeRegistration.html)   
Returns information about a type's registration, including its current status and type and version identifiers\. 

 [ListTypeRegistrations](https://docs.aws.amazon.com/AWSCloudFormation/latest/APIReference/API_ListTypeRegistrations.html)   
Returns a list of registration request identifiers for the specified type\. 

 [ListTypes](https://docs.aws.amazon.com/AWSCloudFormation/latest/APIReference/API_ListTypes.html)   
Returns summary information about types that have been registered with CloudFormation\. 

 [ListTypeVersions](https://docs.aws.amazon.com/AWSCloudFormation/latest/APIReference/API_ListTypeVersions.html)   
Returns summary information about the versions of a type\. 

 [RegisterType](https://docs.aws.amazon.com/AWSCloudFormation/latest/APIReference/API_RegisterType.html)   
Registers a type with the CloudFormation service\. Registering a type makes it available for use in CloudFormation templates in your AWS account\. 

 [SetTypeDefaultVersion](https://docs.aws.amazon.com/AWSCloudFormation/latest/APIReference/API_SetTypeDefaultVersion.html)   
Specify the default version of a type\. The default version of a type will be used in CloudFormation operations\.  | November 18, 2019 | 
| [Updated resources](AWS_GameLift.md) | The following resources were updated: AWS::GameLift::Build, AWS::GameLift::Fleet\. 

 [AWS::GameLift::Build](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-gamelift-build.html)   
Use the `OperatingSystem` property to specify the operating system that the build files run on\. 

 [AWS::GameLift::Fleet](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-gamelift-fleet.html)   
Use the `CertificateConfiguration` property to generate a TLS/SSL certificate for the new fleet\.  
Use the `FleetType` property to specify use of On\-Demand or Spot instances in the fleet\.  
Use the `InstanceRoleArn` property to manage access to your non\-GameLift AWS resources from GameLift fleet instances\.  
Use the `MetricGroups` property to add fleet metrics to a CloudWatch metric group\.  
Use the `NewGameSessionProtectionPolicy` property to prevent the fleet's active game sessions from being terminated during a scale down event\.  
Use the `PeerVpcAwsAccountId` property when setting up VPC peering for the fleet\.  
Use the `PeerVpcId` property when setting up VPC peering for the fleet\.  
Use the `ResourceCreationLimitPolicy` property to limit an individual player's ability to use the fleet's available hosting resources\.  
Use the `RuntimeConfiguration` property to configure what processes are run on each instance in the fleet\.  
Use the `ScriptId` property to create a Realtime Servers fleet and configure it with a Realtime script\.  | November 14, 2019 | 
| [New resources](AWS_GameLift.md) | The following resources were added: AWS::GameLift::Script, AWS::GameLift::GameSessionQueue, AWS::GameLift::MatchmakingConfiguration, AWS::GameLift::MatchmakingRuleSet\. 

 [AWS::GameLift::Script](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-gamelift-script.html)   
Use the `Script` resource to upload a configuration script for a Realtime Servers fleet\. 

 [AWS::GameLift::GameSessionQueue](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-gamelift-gamesessionqueue.html)   
Use the `GameSessionQueue` resource to create a game session queue that processes player requests for new game sessions\. 

 [AWS::GameLift::MatchmakingConfiguration](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-gamelift-matchmakingconfiguration.html)   
Use the `MatchmakingConfiguration` resource to create a matchmaker that processes player requests for new matched game sessions\. 

 [AWS::GameLift::MatchmakingRuleSet](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-gamelift-matchmakingruleset.html)   
Use the `MatchmakingRuleSet` resource to create rules that specify how to form matches and evaluate players for inclusion in a match\.  | November 14, 2019 | 
| [Resource import added](#ReleaseHistory) | If you created an AWS resource outside of AWS CloudFormation management, you can bring this existing resource into CloudFormation management using `resource import`\.For more information, see [Bringing Existing Resources Into CloudFormation Management](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/resource-import.html)\. | November 11, 2019 | 
| [New resource](AWS_CodeStarNotifications.md) | The following resource was added: AWS::CodeStarNotifications::NotificationRule 

 [AWS::CodeStarNotifications::NotificationRule](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-codestarnotifications-notificationrule.html)   
Use the `AWS::CodeStarNotifications::NotificationRule` resource to create notification rules for resources in AWS CodeBuild, AWS CodeCommit, AWS CodeDeploy, and AWS CodePipeline\.  | November 7, 2019 | 
| [New resource](#ReleaseHistory) | The following resources were added: AWS::MediaConvert::JobTemplate, AWS::MediaConvert::Preset, AWS::MediaConvert::Queue 

 [AWS::MediaConvert::JobTemplate](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-mediaconvert-jobtemplate.html)   
Use the `AWS::MediaConvert::JobTemplate` resource to specify a job template for transcoding jobs\. 

 [AWS::MediaConvert::Preset](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-mediaconvert-preset.html)   
Use the `AWS::MediaConvert::Preset` resource to specify an output preset as part of a transcoding job\. 

 [AWS::MediaConvert::Queue](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-mediaconvert-queue.html)   
Use the `AWS::MediaConvert::Queue` resource to specify an on\-demand transcoding queue\.  | November 6, 2019 | 
| [Updated resource](AWS_Glue.md) | The following resource was updated: AWS::Glue::Crawler 

 [AWS::Glue::Crawler](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-glue-crawler.html)   
Use the `DynamoDBTargets` property to specify a list of Amazon DynamoDB targets\.  
Use the `CatalogTargets` property to specify a list of AWS Glue Data Catalog targets\.  | November 4, 2019 | 
| [Updated resources](AWS_ApiGateway.md) | The following resources were updated: AWS::ApiGateway::ApiKey, AWS::ApiGateway::ClientCertificate, AWS::ApiGateway::DomainName, AWS::ApiGateway::RestApi, and AWS::ApiGateway::UsagePlan\. 

 [AWS::ApiGateway::ApiKey](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-apigateway-apikey.html)   
Use the `Tags` property to specify an array of arbitrary tags \(key\-value pairs\) to associate with the API key\. 

 [AWS::ApiGateway::ClientCertificate](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-apigateway-clientcertificate.html)   
Use the `Tags` property to specify an array of arbitrary tags \(key\-value pairs\) to associate with the client certificate\. 

 [AWS::ApiGateway::DomainName](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-apigateway-domainname.html)   
Use the `SecurityPolicy` property to the Transport Layer Security \(TLS\) version \+ cipher suite for this domain name\.  
Use the `Tags` property to specify an array of arbitrary tags \(key\-value pairs\) to associate with the domain name\. 

 [AWS::ApiGateway::RestApi](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-apigateway-restapi.html)   
Use the `Tags` property to specify an array of arbitrary tags \(key\-value pairs\) to associate with the API\. 

 [AWS::ApiGateway::UsagePlan](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-apigateway-usageplan.html)   
Use the `Tags` property to specify an array of arbitrary tags \(key\-value pairs\) to associate with the usage plan\.  | October 31, 2019 | 
| [Updated resources](AWS_CodePipeline.md) | The following resources were updated: AWS::CodePipeline::CustomActionType, AWS::CodePipeline::Pipeline\. 

 [AWS::CodePipeline::CustomActionType](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-codepipeline-customactiontype.html)   
Use the `Tags` property to specify the tags for the custom action\. 

 [AWS::CodePipeline::Pipeline](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-codepipeline-pipeline.html)   
Use the `Tags` property to specify the tags for the pipeline\.  | October 31, 2019 | 
| [Updated resource](AWS_Amplify.md) | The following resource was updated: AWS::Amplify::App 

 [AWS::Amplify::App](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-amplify-app.html)   
Use the `EnablePullRequestPreview` property to specify whether pull request previews are enabled for each branch that Amplify Console automatically creates for your app\.  
Use the `PullRequestEnvironmentName` property to specify a dedicated backend environment for your pull request previews\.  | October 31, 2019 | 
| [Updated resource](AWS_ECS.md) | The following resource was updated: AWS::ECS::TaskDefinition\. 

 [AWS::ECS::TaskDefinition](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ecs-taskdefinition.html)   
Use the `InferenceAccelerator` property to specify the Elastic Inference accelerators to use for the containers in the task\.  | October 31, 2019 | 
| [Updated resource](AWS_Elasticsearch.md) | The following resource was updated: AWS::Elasticsearch::Domain\. 

 [AWS::Elasticsearch::Domain](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-elasticsearch-domain.html)   
Use the `LogPublishingOptions` property to configure slow log publishing\.  | October 31, 2019 | 
| [Updated resource](AWS_Events.md) | The following resource was updated: AWS::Events::Rule\. 

 [AWS::Events::Rule](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-events-rule.html)   
In the [Target](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-events-rule-target.html) property type, use the `BatchParameters` property to specify the job definition, job name, and other parameters, if the event target is an AWS Batch job\.  | October 31, 2019 | 
| [New resources](AWS_Pinpoint.md) | The following resources were added: AWS::Pinpoint::EmailTemplate, AWS::Pinpoint::PushTemplate, and AWS::Pinpoint::SmsTemplate 

 [AWS::Pinpoint::EmailTemplate](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-pinpoint-emailtemplate.html)   
Use the `AWS::Pinpoint::EmailTemplate` resource to create a message template that you can use in messages that are sent through the email channel\. 

 [AWS::Pinpoint::PushTemplate](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-pinpoint-pushtemplate.html)   
Use the `AWS::Pinpoint::PushTemplate` resource to create a message template that you can use in messages that are sent through a push notification channel\. 

 [AWS::Pinpoint::SmsTemplate](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-pinpoint-smstemplate.html)   
Use the `AWS::Pinpoint::SmsTemplate` resource to create a message template that you can use in messages that are sent through the SMS channel\.  | October 31, 2019 | 
| [Updated resource](AWS_Amplify.md) | The following resource was updated: AWS::Amplify::Branch 

 [AWS::Amplify::Branch](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-amplify-branch.html)   
Use the `EnablePullRequestPreview` property to specify whether Amplify Console creates a preview for each pull request that is made for the branch\.  
Use the `PullRequestEnvironmentName` property to specify a dedicated backend environment for your pull request previews\.  | October 24, 2019 | 
| [Updated resource](AWS_Cognito.md) | The following resource was updated: AWS::Cognito::UserPool 

 [AWS::Cognito::UserPool](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-cognito-userpool.html)   
Use the `Schema` parameter to add or update schema attributes\. 

 [AWS::Cognito::UserPool](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-cognito-userpool.html)   
Use the `AliasAttributes` parameter to add or update an alias for the user pool\. 

 [AWS::Cognito::UserPool](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-cognito-userpool.html)   
Use the `UsernameAttributes` parameter to determine if email addresses or phone numbers can be used as user names when a user signs up\.  | October 24, 2019 | 
| [Updated resources](#ReleaseHistory) | The following resource was updated: AWS::MSK::Cluster\. 

 [AWS::MSK::Cluster](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-msk-cluster.html)   
Use the `NumberOfBrokerNodes` property to submit an update to change the number of broker nodes in the cluster\.  | October 17, 2019 | 
| [Updated resource](AWS_Cognito.md) | The following resource was updated: AWS::Cognito::IdentityPoolRoleAttachment 

 [AWS::Cognito::IdentityPoolRoleAttachment](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-cognito-identitypoolroleattachment.html)   
Use the `IdentityProvider` parameter to specify the identity provider for which the role is mapped\.  | October 17, 2019 | 
| [Updated resource](AWS_FSx.md) | The following resource was updated: AWS::FSx::FileSystem 

 [AWS::FSx::FileSystem](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-fsx-filesystem.html)   
In the [WindowsConfiguration](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-fsx-filesystem-windowsconfiguration.html) property type, use the `SelfManagedActiveDirectoryConfiguration` property to join an Amazon FSx Windows File Server instance to your self\-managed \(including on\-premises\) Microsoft Active Directory \(AD\) directory\.  | October 17, 2019 | 
| [Updated Resource](#ReleaseHistory) | The following resource was updated: AWS::Batch::ComputeEnvironment 

 [ComputeResources](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-batch-computeenvironment-computeresources.html)  
In the [ComputeResources](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-batch-computeenvironment-computeresources.html) property type, use the `AllocationStrategy` property to specify the strategy to use to select instance types\.  | October 17, 2019 | 
| [Updated resources](AWS_Events.md) | The following resource were updated: AWS::Events::EventBusPolicy, AWS::Events::Rule 

 [AWS::Events::EventBusPolicy](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-events-eventbuspolicy.html)   
Use the `EventBusName` property to specify the name of the event bus to associate with this policy\. 

 [AWS::Events::Rule](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-events-rule.html)   
Use the `EventBusName` property to specify the name of the event bus to associate with this rule\.  | October 3, 2019 | 
| [Updated resources](AWS_Pinpoint.md) | The following resources were updated: AWS::Pinpoint::App, AWS::Pinpoint::Campaign, and AWS::Pinpoint::Segment 

 [AWS::Pinpoint::App](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-pinpoint-app.html)   
The `ARN` attribute returns the Amazon Resource Name \(ARN\) of the application\.  
Use the `Tags` property to specify a string\-to\-string map of key\-value pairs that defines the tags to associate with the application\. 

 [AWS::Pinpoint::Campaign](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-pinpoint-campaign.html)   
The `ARN` attribute returns the Amazon Resource Name \(ARN\) of the campaign\.  
Use the `Tags` property to specify a string\-to\-string map of key\-value pairs that defines the tags to associate with the campaign\. 

 [AWS::Pinpoint::Segment](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-pinpoint-segment.html)   
The `ARN` attribute returns the Amazon Resource Name \(ARN\) of the segment\.  
Use the `Tags` property to specify a string\-to\-string map of key\-value pairs that defines the tags to associate with the segment\.  | October 3, 2019 | 
| [Updated resource](AWS_Budgets.md) | The following resource was updated: AWS::Budgets::Budget 

 [AWS::Budgets::Budget](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-budgets-budget.html)   
In the [BudgetData](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-budgets-budget-budgetdata.html) property type, use the `PlannedBudgetLimits` property to specify a map containing multiple budget limits, including current or future limits\.  | October 3, 2019 | 
| [Updated resource](AWS_Cognito.md) | The following resource was updated: AWS::Cognito::UserPool 

 [AWS::Cognito::UserPool](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-cognito-userpool.html)   
Use the `EnabledMfas` parameter to enable MFA on a specified user pool\.  | October 3, 2019 | 
| [New resources](AWS_Cognito.md) | The following resources were added: AWS::Cognito::UserPoolDomain, AWS::Cognito::UserPoolResourceServer, AWS::Cognito::UserPoolIdentityProvider, AWS::Cognito::RiskConfigurationAttachment, AWS::Cognito::UICustomizationAttachment\.  

 [AWS::Cognito::UserPoolDomain](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-cognito-userpooldomain.html)   
Use the `AWS::Cognito::UserPoolDomain` resource to create a new domain for a user pool\. 

 [AWS::Cognito::UserPoolResourceServer](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-cognito-userpoolresourceserver.html)   
Use the `AWS::Cognito::UserPoolResourceServer` resource to create a new OAuth2\.0 resource server and define custom scopes in it\. 

 [AWS::Cognito::UserPoolIdentityProvider](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-cognito-userpoolidentityprovider.html)   
Use the `AWS::Cognito::UserPoolIdentityProvider` resource to create an identity provider for a user pool\. 

 [AWS::Cognito::UserPoolRiskConfigurationAttachment ](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-cognito-userpoolriskconfigurationattachment.html)   
Use the `AWS::Cognito::UserPoolRiskConfigurationAttachment` resource to set the risk configuration that is used for Amazon Cognito advanced security features\. 

 [AWS::Cognito::UserPoolUICustomizationAttachment ](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-cognito-userpooluicustomizationattachment.html)   
Use the `AWS::Cognito::UserPoolUICustomizationAttachment` resource to set the UI customization information for a user pool's built\-in app UI\.  | October 3, 2019 | 
| [New resources](AWS_EC2.md) | The following resource were added: AWS::EC2::TrafficMirrorFilter, AWS::EC2::TrafficMirrorFilterRule, AWS::EC2::TrafficMirrorSession, and AWS::EC2::TrafficMirrorTarget 

 [AWS::EC2::TrafficMirrorFilter](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-trafficmirrorfilter.html)   
Use the `AWS::EC2::TrafficMirrorFilter` resource to specify a traffic mirror filter\. 

 [AWS::EC2::TrafficMirrorFilterRule](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-trafficmirrorfilterrule.html)   
Use the `AWS::EC2::TrafficMirrorFilterRule` resource to manage traffic mirror filter rules\. 

 [AWS::EC2::TrafficMirrorSession](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-trafficmirrorsession.html)   
Use the `AWS::EC2::TrafficMirrorSession` resource to specify a traffic mirror session\. 

 [AWS::EC2::TrafficMirrorTarget](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-trafficmirrortarget.html)   
Use the `AWS::EC2::TrafficMirrorTarget` resource to specify a traffic mirror target\.  | October 3, 2019 | 
| [New resource](AWS_Events.md) | The following resource was added: AWS::Events::EventBus 

 [AWS::Events::EventBus](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-events-eventbus.html)   
Use the `EventBus` resource to create or update a custom event bus or a partner event bus\.  | October 3, 2019 | 
| [Updated resource](AWS_Glue.md) | The following resource was updated: AWS::Glue::DevEndpoint 

 [AWS::Glue::DevEndpoint](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-glue-devendpoint.html)   
Use the `WorkerType` property to specify a type of predefined worked allocated to the development endpoint\.  
Use the `NumberOfWorkers` property to specify the number of workers of a defined `workerType` that are allocated to the development endpoint\.  
Use the `GlueVersion` property to specify the versions of Apache Spark and Python that AWS Glue supports for the development endpoint\.  
Use the `Arguments` property to specify a map of arguments used to configure the `DevEndpoint`\.  | September 27, 2019 | 
| [Updated resource](AWS_Glue.md) | The following resource was updated: AWS::Glue::Job 

 [AWS::Glue::Job](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-glue-job.html)   
Use the `Timeout` property to specify the job timeout in minutes\.  
Use the `NotificationProperty` property to specify the configuration properties of a notification\.  
Use the `NotifyDelayAfter` property to specify the number of minutes to wait before sending a job run delay notification after a job run starts\.  | September 26, 2019 | 
| [Updated resource](AWS_Glue.md) | The following resource was updated: AWS::Glue::Trigger 

 [AWS::Glue::Trigger](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-glue-trigger.html)   
Use the `StartOnCreation` property to specify starting `SCHEDULED` and `CONDITIONAL` triggers when created\.  
Use the `WorkflowName` property to specify the name of the workflow associated with the trigger\.  | September 26, 2019 | 
| [Updated resource](#ReleaseHistory) | The following resource was updated: AWS::DocDB::DBCluster\. 

 [AWS::DocDB::DBCluster](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-docdb-dbcluster.html)   
Use the `EnableCloudwatchLogsExports` property to specify the list of log types that need to be enabled for exporting to CloudWatch Logs\.  | September 26, 2019 | 
| [New resource](AWS_Glue.md) | The following resource was added: AWS::Glue::Workflow 

 [AWS::Glue::Workflow](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-glue-workflow.html)   
Use the `AWS::Glue::Workflow` resource to manage AWS Glue workflows\.  | September 26, 2019 | 
| [Updated resource](#ReleaseHistory) | The following resource was updated: AWS::Config::RemediationConfiguration\. 

 [AWS::Config::RemediationConfiguration](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-config-remediationconfiguration.html)   
Use the `ExecutionControls` property to specify an `ExecutionControls` object\.  | September 12, 2019 | 
| [New resource](AWS_QLDB.md) | The following resource was added: AWS::QLDB::Ledger 

 [AWS::QLDB::Ledger](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-qldb-ledger.html)   
Use the `AWS::QLDB::Ledger` resource to specify a new Amazon Quantum Ledger Database \(Amazon QLDB\) ledger\.  | September 12, 2019 | 
| [Updated resources ](#ReleaseHistory) | The following resources were updated: AWS::ApplicationAutoScaling::ScalableTarget, AWS::DynamoDB::Table, AWS::EC2::Instance, AWS::ECS::TaskDefinition, AWS::ElastiCache::ReplicationGroup, AWS::Events::Rule, AWS::IAM::Role, and AWS::Lambda::EventSourceMapping\. 

 [AWS::ApplicationAutoScaling::ScalableTarget](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-applicationautoscaling-scalabletarget.html)   
Use the `SuspendedState` property to suspend and resume automatic scaling\. Setting the value of an attribute to `true` suspends the specified scaling activities\. Setting it to `false` \(default\) resumes the specified scaling activities\. 

 [AWS::DynamoDB::Table](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-dynamodb-table.html)   
In the [SSESpecification](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-dynamodb-table-ssespecification.html) property type, use the `SSEType` property to specify server\-side encryption type\. 

 [AWS::EC2::Instance](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ec2-instance.html)   
Use the `CpuOptions` property to specify the CPU options for the instance\.  
In the [Ebs](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ec2-blockdev-template.html) property type, use the `KmsKeyId` property to specify an identifier \(key ID, key alias, ID ARN, or alias ARN\) for a customer managed CMK under which the EBS volume is encrypted\. 

 [AWS::ECS::TaskDefinition](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ecs-taskdefinition.html)   
Use the `IpcMode` property to specify the IPC resource namespace to use for the containers in the task\. The valid values are `host`, `task`, or `none`\.  
Use the `PidMode` property to specify the process namespace to use for the containers in the task\. The valid values are `host` or `task`\.  
In the [ContainerDefinition](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ecs-taskdefinition-containerdefinitions.html) property type:  
+ When the `Interactive` property is set to `true`, this allows you to deploy containerized applications that require `stdin` or a `tty` to be allocated\.
+ When the `PseudoTerminal` proprety is set to `true`, a TTY is allocated\.
+ Use the `SystemControls` property to specify a list of namespaced kernel parameters to set in the container\. 
In the [LogConfiguration](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ecs-taskdefinition-containerdefinitions-logconfiguration.html) property type, use the `SecretOptions` property to specify the secrets to pass to the log configuration\. 

 [AWS::ElastiCache::ReplicationGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-elasticache-replicationgroup.html)   
Use the `KmsKeyId` property to specify the ID of the KMS key used to encrypt the disk on the cluster\. 

 [AWS::Events::Rule](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-events-rule.html)   
In the [EcsParameters](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-events-rule-ecsparameters.html) property type:  
+ Use the `Group` property to specify an ECS task group for the task\.
+ Use the `LaunchType` property to specify the launch type on which your task is running\.
+ If the ECS task uses the `awsvpc` network mode, use the `NetworkConfiguration` property to specify the VPC subnets and security groups associated with the task and whether a public IP address is to be used\.
+ Use the `PlatformVersion` property to specify the platform version for the task\. 

 [AWS::IAM::Role](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-iam-role.html)   
Use the `Description` property to provide a description for the role\.  
Use the `Tags` property to specify a list of tags that are attached to the specified role\. 

 [AWS::Lambda::EventSourceMapping](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-lambda-eventsourcemapping.html)   
Use the `MaximumBatchingWindowInSeconds` property to specify the maximum amount of time to gather records before invoking the function, in seconds\.  | August 29, 2019 | 
| [Updated resources](AWS_RDS.md) | The following resources were updated: AWS::RDS::DBCluster and AWS::RDS::DBInstance 

 [AWS::RDS::DBCluster](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-rds-dbcluster.html)   
Use the `AssociatedRoles` property to specify the AWS Identity and Access Management \(IAM\) roles associated with the DB instance\.  
Use the `RestoreType` property to specify the type of restore to be performed\.   
Use the `SourceDBClusterIdentifier` property to specify the identifier of the source DB cluster from which to restore\.   
Use the `UseLatestRestorableTime` property to specify whether to restore the DB cluster to the latest restorable backup time\.  

 [AWS::RDS::DBInstance](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-rds-database-instance.html)   
Use the `AssociatedRoles` property to specify the AWS Identity and Access Management \(IAM\) roles associated with the DB instance\.  | August 29, 2019 | 
| [Updated resource](AWS_CloudWatch.md) | The following resource was updated: AWS::CloudWatch::Alarm 

 [AWS::CloudWatch::Alarm](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-cw-alarm.html)   
Use the `ThresholdMetricId` property to specify the ID of the ANOMALY\_DETECTION\_BAND function used as the threshold for the alarm\.  | August 29, 2019 | 
| [Updated resource](AWS_Elasticsearch.md) | The following resource was updated: AWS::Elasticsearch::Domain\. 

 [AWS::Elasticsearch::Domain](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-elasticsearch-domain.html)   
In the [ElasticsearchClusterConfig](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-elasticsearch-domain-elasticsearchclusterconfig.html) property type, use the `ZoneAwarenessConfig` property to specify zone awareness configuration options\.  | August 29, 2019 | 
| [New resource ](AWS_Config.md) | The following resource was added: AWS::Config::OrganizationConfigRule 

 [AWS::Config::OrganizationConfigRule](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-config-organizationconfigrule.html)   
Use the `AWS::Config::OrganizationConfigRule` resource to create an OrganizationConfigRule that has information about config rules that AWS Config creates in the member accounts\.  | August 29, 2019 | 
| [Updated resource](#ReleaseHistory) | The following resource was updated: AWS::Neptune::DBCluster\. 

 [AWS::Neptune::DBCluster](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-neptune-dbcluster.html)   
Use the `EnableCloudwatchLogsExports` property to specify a list of log types that are enabled for export to CloudWatch Logs\.  | August 22, 2019 | 
| [Updated resource](AWS_DMS.md) | The following resource was updated: AWS::DMS::ReplicationTask 

 [AWS::DMS::ReplicationTask](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-dms-replicationtask.html)   
Use the `CdcStartPosition` property to indicate when you want a change data capture \(CDC\) operation to start\.  
Use the `CdcStopPosition` property to indicate when you want a change data capture \(CDC\) operation to stop\.  | August 16, 2019 | 
| [Updated resources](#ReleaseHistory) | The following resources were updated: AWS::EC2::ClientVpnEndpoint, AWS::Greengrass::Group, AWS::Greengrass::ConnectorDefinition, AWS::Greengrass::CoreDefinition, AWS::Greengrass::DeviceDefinition, AWS::Greengrass::FunctionDefinition, AWS::Greengrass::LoggerDefinition, AWS::Greengrass::ResourceDefinition, and AWS::Greengrass::SubscriptionDefinition\.  

 [AWS::EC2::ClientVpnEndpoint](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-clientvpnendpoint.html)   
Use the `SplitTunnel` parameter to specify whether split\-tunnel is enabled on the AWS Client VPN endpoint\. 

 [AWS::Greengrass::ConnectorDefinition](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-greengrass-connectordefinition.html)   
Use the `Tags` property to attach metadata to the `AWS::Greengrass::ConnectorDefinition` resource\. 

 [AWS::Greengrass::CoreDefinition](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-greengrass-coredefinition.html)   
Use the `Tags` property to attach metadata to the `AWS::Greengrass::CoreDefinition` resource\. 

 [AWS::Greengrass::DeviceDefinition](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-greengrass-devicedefinition.html)   
Use the `Tags` property to attach metadata to the `AWS::Greengrass::DeviceDefinition` resource\. 

 [AWS::Greengrass::FunctionDefinition](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-greengrass-functiondefinition.html)   
Use the `Tags` property to attach metadata to the `AWS::Greengrass::FunctionDefinition` resource\. 

 [AWS::Greengrass::Group](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-greengrass-group.html)   
Use the `Tags` property to attach metadata to the `AWS::Greengrass::Group` resource\. 

 [AWS::Greengrass::LoggerDefinition](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-greengrass-loggerdefinition.html)   
Use the `Tags` property to attach metadata to the `AWS::Greengrass::LoggerDefinition` resource\. 

 [AWS::Greengrass::ResourceDefinition](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-greengrass-resourcedefinition.html)   
Use the `Tags` property to attach metadata to the `AWS::Greengrass::ResourceDefinition` resource\. 

 [AWS::Greengrass::SubscriptionDefinition](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-greengrass-subscriptiondefinition.html)   
Use the `Tags` property to attach metadata to the `AWS::Greengrass::SubscriptionDefinition` resource\.  | August 8, 2019 | 
| [Updated resource](AWS_AppSync.md) | The following resource was updated: AWS::AppSync::GraphQLApi\. 

 [AWS::AppSync::GraphQLApi](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-appsync-graphqlapi.html)   
In the [LogConfig](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-appsync-graphqlapi-logconfig.html) property type, when set to `TRUE`, the `excludeVerboseContent` property excludes sections that contain information such as headers, context, and evaluated mapping templates, regardless of logging level\.  | August 8, 2019 | 
| [New resources](#ReleaseHistory) | The following resources were added: AWS::ManagedBlockchain::Member and AWS::ManagedBlockchain::Node\. 

 [AWS::ManagedBlockchain::Member](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-managedblockchain-member.html)   
Use the `Member` resource to create the first member or an additional member of an Amazon Managed Blockchain network\. 

 [AWS::ManagedBlockchain::Node](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-managedblockchain-node.html)   
Use the `Node` resource to create a peer node in a member of an Amazon Managed Blockchain network\.  | August 8, 2019 | 
| [New resource](AWS_Glue.md) | The following resource was added: AWS::Glue::MLTransform 

 [AWS::Glue::MLTransform](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-glue-mltransform.html)   
Use the `AWS::Glue::MLTransform` resource to manage machine learning transforms\.  | August 8, 2019 | 
| [New resource](AWS_LakeFormation.md) | The following resource was added: AWS::LakeFormation::DataLakeSettings 

 [AWS::LakeFormation::DataLakeSettings](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-lakeformation-datalakesettings.html)   
Use the `AWS::LakeFormation::DataLakeSettings` resource to manage data lake settings\.  | August 8, 2019 | 
| [New resource](AWS_LakeFormation.md) | The following resource was added: AWS::LakeFormation::Permissions 

 [AWS::LakeFormation::Permissions](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-lakeformation-permissions.html)   
Use the `AWS::LakeFormation:Permissions` resource to grant or revoke AWS Lake Formation permissions\.  | August 8, 2019 | 
| [New resource](AWS_LakeFormation.md) | The following resource was added: AWS::LakeFormation::Resource 

 [AWS::LakeFormation::Resource](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-lakeformation-resource.html)   
Use the `AWS::LakeFormation::Resource` resource to define the resources to which permissions are to be granted\.  | August 8, 2019 | 
| [New resource](AWS_CodeBuild.md) | The following resource was added: AWS::CodeBuild::SourceCredential 

 [AWS::CodeBuild::SourceCredential](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-codebuild-source-credential.html)   
Use the `AWS::CodeBuild::SourceCredential` resource to specify information about the credentials for a GitHub, GitHub Enterprise, or Bitbucket repository used in an AWS CodeBuild build project\.  | August 7, 2019 | 
| [Updated resources](#ReleaseHistory) | The following resources were updated: AWS::Batch::JobDefinition, AWS::Cognito::UserPool, AWS::Cognito::UserPoolClient, and AWS::Glue::Job\. 

 [AWS::Batch::JobDefinition](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-batch-jobdefinition.html)   
In the [ContainerProperties](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-batch-jobdefinition-containerproperties.html) property type, use the `LinuxParameters` property to specify Linux\-specific modifications that are applied to the container, such as details for device mappings\. 

[AWS::Cognito::UserPool](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-cognito-userpool.html)  
Use the `UserPoolAddOns` property to enable advanced security risk detection\.  
Use the `VerificationMessageTemplate` property to define the template for verification messages\. 

[AWS::Cognito::UserPoolClient](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-cognito-userpoolclient.html)  
Use the `AnalyticsConfiguration` property to define the Amazon Pinpoint analytics configuration for collecting metrics for this user pool\. 

 [AWS::Glue::Job](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-glue-job.html)   
Use the `GlueVersion` property to determine the versions of Apache Spark and Python that AWS Glue supports\. The Python version indicates the version supported for jobs of type Spark\.  
Use the `MaxCapacity` property to specify the number of AWS Glue data processing units \(DPUs\) that can be allocated when this job runs\. A DPU is a relative measure of processing power that consists of 4 vCPUs of compute capacity and 16 GB of memory\.  
For the `NumberofWorkers` property, when you specify a Python shell job \(`JobCommand.Name`="pythonshell"\), you can allocate either 0\.0625 or 1 DPU\. The default is 0\.0625 DPU\. When you specify an Apache Spark ETL job \(`JobCommand.Name`="glueetl"\), you can allocate from 2 to 100 DPUs\. The default is 10 DPUs\. This job type cannot have a fractional DPU allocation\.  
Use the `WorkerType` property to specify the type of predefined worker that is allocated when a job runs\.  
In the [JobCommand](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-glue-job-jobcommand.html) property type, use the `PythonVersion` property to specify the Python version being used to execute a Python shell job\.  | August 2, 2019 | 
| [Stack set limit increases](#ReleaseHistory) | You can now create a maximum of 100 stack sets in your administrator account, create a maximum of 2000 stack instances per stack set, and run a maximum of 3500 stack instance operations in each region at the same time, per administrator account\.For more details, see [AWS CloudFormation quotas](cloudformation-limits.md)\. | August 2, 2019 | 
| [New resource](#ReleaseHistory) | The following resource was added: AWS::CodeStar::GitHubRepository\. 

 [AWS::CodeStar::GitHubRepository](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-codestar-githubrepository.html)   
Use the `AWS::CodeStar::GitHubRepository` resource to create a GitHub repository where you can store source code for use with AWS workflows\. If provided, your source code is uploaded to the repository after it is created\.  | August 2, 2019 | 
| [Updated resource](#ReleaseHistory) | You can now add tags to a CodeCommit repository in your AWS CloudFormation template\. 

 [AWS::CodeCommit::Repository](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-codecommit-repository.html)   
Use the `Tags` property to provide information about one or more tag key\-value pairs to use when tagging a repository\.  | July 25, 2019 | 
| [Updated resources](#ReleaseHistory) | The following resource was updated: AWS::AmazonMQ::Broker\. 

 [ AWS::AmazonMQ::Broker](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-amazonmq-broker.html)   
Use the `encryptionOptions` property to specify an AWS\-owned CMK or a customer\-managed CMK\.  | July 22, 2019 | 
| [Updated resources](#ReleaseHistory) | The following resources were updated: AWS::Amplify::App and AWS::Amplify::Branch\. 

[AWS::Amplify::App](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-amplify-app.html)  
Use the `AutoBranchCreationConfig` property type to automatically create branches that match a certain pattern\. 

[AWS::Amplify::Branch](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-amplify-branch.html)  
Use the `EnableAutoBuild` property to enable automatic builds for a branch\.  | July 18, 2019 | 
| [New resources](#ReleaseHistory) | The following resources were added: AWS::IoTEvents::DetectorModel and AWS::IoTEvents::Input\. 

 [ AWS::IoTEvents::DetectorModel](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-iotevents-detectormodel.html)   
Use the `DetectorModel` resource to create a detector model\. 

 [ AWS::IoTEvents::Input](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-iotevents-input.html)   
Use the `Input` resource to create an input\.  | July 18, 2019 | 
| [New resource](#ReleaseHistory) | The following resource was added: AWS::CloudWatch::AnomalyDetector\. 

 [AWS::CloudWatch::AnomalyDetector](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-cloudwatch-anomalydetector.html)   
Use the `AWS::CloudWatch::AnomalyDetector` resource to specify an anomaly detection band for a certain metric and statistic\. The band represents the expected "normal" range for the metric values\.  | July 12, 2019 | 
| [Updated resources](#ReleaseHistory) | The following resources were updated: AWS::IoTAnalytics::Channel and AWS::IoTAnalytics::Datastore\. 

 [AWS::IoTAnalytics::Channel](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-iotanalytics-channel.html)   
Use the `ChannelStorage` property to specify channel data is stored\. 

 [AWS::IoTAnalytics::Datastore](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-iotanalytics-datastore.html)   
Use the `DatastoreStorage` property to specify where data store data is stored\.  | June 27, 2019 | 
| [New resources](#ReleaseHistory) | The following resources were added: AWS::MediaLive::Channel, AWS::MediaLive::Input, and AWS::MediaLive::InputSecurityGroup\. 

 [AWS::MediaLive::Channel](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-medialive-channel.html)   
The `AWS::MediaLive::Channel` resource creates a channel\. A MediaLive channel ingests and transcodes \(decodes and encodes\) source content from the inputs that are attached to that channel, and packages the new content into outputs\.  

 [AWS::MediaLive::Input](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-medialive-input.html)   
The `AWS::MediaLive::Input` resource creates an input\. A MediaLive input holds information that describes how the MediaLive channel is connected to the upstream system that is providing the source content that is to be transcoded\.  

 [AWS::MediaLive::InputSecurityGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-medialive-inputsecuritygroup.html)   
The `AWS::MediaLive::InputSecurityGroup` resource creates an input security group\. A MediaLive input security group is associated with a MediaLive input\. The input security group is an "allow list" of IP addresses that controls whether an external IP address can push content to the associated MediaLive input\.   | June 27, 2019 | 
| [Updated resource](#ReleaseHistory) | The following resource was updated: AWS::EC2::LaunchTemplate 

 [ AWS::EC2::LaunchTemplate](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-launchtemplate.html)   
In the [ SpotOptions](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ec2-launchtemplate-launchtemplatedata-instancemarketoptions-spotoptions.html) property type, use `BlockDurationMinutes` to specify the required duration for the Spot Instances, and use `ValidUntil` to specify the end date for the Spot request\.  | June 25, 2019 | 
| [New resource](#ReleaseHistory) | The following resource was added: AWS::SecurityHub::Hub 

 [AWS::SecurityHub::Hub](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-securityhub-hub.html)   
Use the [AWS::SecurityHub::Hub](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-securityhub-hub.html) resource to specify the implementation of the AWS Security Hub service in your account\.   | June 25, 2019 | 
| [Updated resources](#ReleaseHistory) | The following resource were updated: AWS::AppStream::Fleet, AWS::ServiceCatalog::CloudFormationProvisionedProduct  

 [AWS::ServiceCatalog::CloudFormationProvisionedProduct](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-servicecatalog-cloudformationprovisionedproduct.html)   
Use the `ProvisioningPreferences` property to specify user\-defined preferences that will be applied when updating a provisioned product\. 

 [AWS::AppStream::Fleet](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-appstream-fleet.html)   
Use the `IdleDisconnectTimeoutInSeconds` property to specify the amount of time that users can be idle \(inactive\) before they are disconnected from their streaming session and the `DisconnectTimeoutInSeconds` time interval begins\.  | June 20, 2019 | 
| [New resources](#ReleaseHistory) | The following resource was added: AWS::Config::RemediationConfiguration, AWS::ServiceCatalog::StackSetConstraint 

 [AWS::Config::RemediationConfiguration](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-config-remediationconfiguration.html)   
Use the `AWS::Config::RemediationConfiguration` resource to specify the details about the remediation configuration, including the remediation action, parameters, and data to execute the action\. 

 [AWS::ServiceCatalog::StackSetConstraint](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-servicecatalog-stacksetconstraint.html)   
Use the `AWS::ServiceCatalog::StackSetConstraint` resource to specify a stack set constraint\.  | June 20, 2019 | 
| [Updated resources](#ReleaseHistory) | The following resources were updated: AWS::AppMesh::VirtualNode, AWS::CodeBuild::Project, AWS::EC2::Host, AWS::EC2::Route, AWS::EC2::VPNConnection, AWS::ECS::Cluster, AWS::ECS::Service, AWS::ECS::TaskDefinition, AWS::EFS::MountTarget, AWS::ElasticLoadBalancingV2::ListenerRule, AWS::EMR::Cluster, AWS::IoTAnalytics::Dataset, AWS::KinesisFirehose::DeliveryStream, AWS::S3::Bucket\. 

 [AWS::AppMesh::VirtualNode](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-appmesh-virtualnode.html)   
Use `ServiceDiscovery` to specify whether to use `AWSCloudMap` or `DNS` for service discovery\. If using AWS Cloud Map for service discovery, use `AwsCloudMapServiceDiscovery` to specify `ServiceName`, `NamespaceName`, and `Attributes` properties\. Use `AwsCloudMapInstanceAttribute` to specify key and value pairs for `AwsCloudMapServiceDiscovery`\. 

 [AWS::CodeBuild::Project](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-codebuild-project.html)   
Use the `SecondarySourceVersions` property to specify an array of `ProjectSourceVersion` objects\. If `secondarySourceVersions` is specified at the build level, then they take over these `secondarySourceVersions` \(at the project level\)\. 

 [AWS::DLM::LifecyclePolicy](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-dlm-lifecyclepolicy.html)   
In the [PolicyDetails](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-dlm-lifecyclepolicy-policydetails.html) property type:  
+ Use the `PolicyType` property to determine the valid target resource types and actions a policy can manage\. This field defaults to EBS\_SNAPSHOT\_MANAGEMENT if not present\.
+ Use the `Parameters` property to specify a set of optional parameters that can be provided by the policy\.
In the [Schedule](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-dlm-lifecyclepolicy-schedule.html) property type, use the `VariableTags` property to specify a collection of key/value pairs with values determined dynamically when the policy is executed\. Keys may be any valid Amazon EC2 tag key\. Values must be in one of the two following formats: `$(instance-id)` or `$(timestamp)`\. Variable tags are only valid for EBS Snapshot Management – Instance policies\. 

 [AWS::EC2::Host](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-host.html)   
Use the `HostRecovery` property to indicates whether to enable or disable host recovery for the Dedicated Host\. 

 [AWS::EC2::Route](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-route.html)   
Use the `TransitGatewayId` property to specify the ID of a transit gateway\. 

 [AWS::EC2::VPNConnection](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-vpn-connection.html)   
Use the `TransitGatewayId` property to specify the ID of the transit gateway associated with the VPN connection\.  
Use the `VpnGatewayId` property to specify the ID of the virtual private gateway at the AWS side of the VPN connection\. 

 [AWS::ECR::Repository](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ecr-repository.html)   
Use the `Tags` property to specify an array of key\-value pairs to apply to this resource\. 

 [AWS::ECS::Cluster](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ecs-cluster.html)   
Use the `Tags` property to apply metadata to clusters to help you categorize and organize them\. 

 [AWS::ECS::Service](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ecs-service.html)   
Use the `EnableECSManagedTags` property to specify whether to enable Amazon ECS managed tags for the tasks within the service\.  
Use the `PropagateTags` property to specify whether to propagate the tags from the task definition or the service to the tasks in the service\.  
Use the `Tags` property to apply metadata to services to help you categorize and organize them\. 

 [AWS::ECS::TaskDefinition](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ecs-taskdefinition.html)   
In the [ContainerDefinition](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ecs-taskdefinition-containerdefinitions.html) property type:  
+ Use the `ResourceRequirements` property to specify the type and amount of a resource to assign to a container\. The only supported resource is a GPU\.
+ Use the `Secrets` property to specify the secrets to pass to the container\.
Use the `Tags` property to apply metadata to task definitions to help you categorize and organize them\. 

 [AWS::EFS::FileSystem](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-efs-filesystem.html)   
Use the `LifecyclePolicies` property to specify a list of policies used by EFS lifecycle management to transition files to the Infrequent Access \(IA\) storage class\. 

 [AWS::EFS::MountTarget](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-efs-mounttarget.html)   
Use the `IpAddress` attribute to return the IPv4 address of the mount target\. 

 [AWS::ElasticLoadBalancingV2::ListenerRule](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-elasticloadbalancingv2-listenerrule.html)   
In the [RuleCondition](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-elasticloadbalancingv2-listenerrule-conditions.html) property type:  
+ Use the `HostHeaderConfig` property to specify information for a host header condition\.
+ Use the `HttpHeaderConfig` property to specify information for an HTTP header condition\. 
+ Use the `HttpRequestMethodConfig` property to specify information for an HTTP method condition\. 
+ Use the `PathPatternConfig` property to specify information for a path pattern condition\. 
+ Use the `QueryStringConfig` property to specify information for a query string condition\. 
+ Use the `SourceIpConfig` property to specify information for a source IP condition\.  

 [AWS::EMR::Cluster](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-elasticmapreduce-cluster.html)   
In the [JobFlowInstancesConfig](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-elasticmapreduce-cluster-jobflowinstancesconfig.html) property type, use the `Ec2SubnetIds` property to specify multiple EC2 subnet IDs\. 

 [AWS::IoTAnalytics::Dataset](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-iotanalytics-dataset.html)   
When data set contents are created they are delivered to destinations specified in the `ContentDeliveryRules` property\.  
Use the `VersioningConfiguration` property to specify how many versions of data set contents are kept\. If not specified or set to null, only the latest version plus the latest succeeded version \(if they are different\) are kept for the time period specified by the "retentionPeriod" parameter\. 

 [AWS::KinesisFirehose::DeliveryStream](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-kinesisfirehose-deliverystream-extendeds3destinationconfiguration.html)   
In the [ExtendedS3DestinationConfiguration](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-kinesisfirehose-deliverystream-extendeds3destinationconfiguration.html) property type:   
+ Use the `DataFormatConversionConfiguration` property to specify the serializer, deserializer, and schema for converting data from the JSON format to the Parquet or ORC format before writing it to Amazon S3\.
+ Use the `ErrorOutputPrefix` property to specify a prefix that Kinesis Data Firehose evaluates and adds to failed records before writing them to S3\.
+ The `Prefix` property is no longer required\.
In the [S3DestinationConfiguration](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-kinesisfirehose-deliverystream-s3destinationconfiguration.html) property type, use the `ErrorOutputPrefix` property to specify a prefix that Kinesis Data Firehose evaluates and adds to failed records before writing them to S3\. 

 [AWS::S3::Bucket](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-s3-bucket.html)   
Use the `ObjectLockConfiguration` property to specify an object lock configuration for the specified bucket\.  
Use the `ObjectLockEnabled` property to specify whether this bucket has an object lock configuration enabled\.  | June 13, 2019 | 
| [New resources](#ReleaseHistory) | The following resources were added: AWS::Amplify::App, AWS::Amplify::Branch, AWS::Amplify::Domain, AWS::EC2::ClientVpnAuthorizationRule, AWS::EC2::ClientVpnEndpoint, AWS::EC2::ClientVpnRoute, AWS::EC2::ClientVpnTargetNetworkAssociation, AWS::MSK::Cluster\. 

[AWS::Amplify::App](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-amplify-app.html)  
Creates apps in AWS Amplify Console\. An app is a collection of branches\. 

[AWS::Amplify::Branch](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-amplify-branch.html)  
Creates a new branch within an AWS Amplify Console app\. 

[AWS::Amplify::Domain](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-amplify-domain.html)  
Allows you to connect a custom domain to your AWS Amplify Console app\. 

 [ AWS::EC2::ClientVpnAuthorizationRule](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-clientvpnauthorizationrule.html)   
Specifies an ingress authorization rule to add to a Client VPN endpoint\. Ingress authorization rules act as firewall rules that grant access to networks\. 

 [ AWS::EC2::ClientVpnEndpoint](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-clientvpnendpoint.html)   
Specifies a Client VPN endpoint\. A Client VPN endpoint is the resource you create and configure to enable and manage client VPN sessions\. It is the destination endpoint at which all client VPN sessions are terminated\. 

 [ AWS::EC2::ClientVpnRoute](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-clientvpnroute.html)  
Specifies a network route to add to a Client VPN endpoint\. Each Client VPN endpoint has a route table that describes the available destination network routes\. Each route in the route table specifies the path for traﬃc to speciﬁc resources or networks\. 

 [ AWS::EC2::ClientVpnTargetNetworkAssociation](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-clientvpntargetnetworkassociation.html)   
Specifies a target network to associate with a Client VPN endpoint\. A target network is a subnet in a VPC\. You can associate multiple subnets from the same VPC with a Client VPN endpoint\. 

 [AWS::MSK::Cluster](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-msk-cluster.html)   
Use the `AWS::MSK::Cluster` resource to create an Amazon MSK cluster\.  | June 13, 2019 | 
| [Updated resources](#ReleaseHistory) | The following resource was updated: AWS::SageMaker::NotebookInstance\. 

 [AWS::SageMaker::NotebookInstance](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-sagemaker-notebookinstance.html)   
Use the `AcceleratorTypes` property to specify a list of Elastic Inference \(EI\) instance types to associate with this notebook instance\.  
Use the `AdditionalCodeRepositories` property to specify an array of up to three Git repositories associated with the notebook instance\.  
Use the `DefaultCodeRepository` property to specify the Git repository associated with the notebook instance as its default code repository\.  | June 3, 2019 | 
| [New resources](#ReleaseHistory) | The following resources were added: AWS::IoTThingsGraph::FlowTemplate, AWS::Pinpoint::ADMChannel, AWS::Pinpoint::APNSChannel, AWS::Pinpoint::APNSSandboxChannel, AWS::Pinpoint::APNSVoipChannel, AWS::Pinpoint::APNSVoipSandboxChannel, AWS::Pinpoint::App, AWS::Pinpoint::ApplicationSettings, AWS::Pinpoint::BaiduChannel, AWS::Pinpoint::Campaign, AWS::Pinpoint::EmailChannel, AWS::Pinpoint::EventStream, AWS::Pinpoint::GCMChannel, AWS::Pinpoint::SMSChannel, AWS::Pinpoint::Segment, AWS::Pinpoint::VoiceChannel, AWS::SageMaker::CodeRepository, and AWS::MSK::Cluster\. 

 [AWS::IoTThingsGraph::FlowTemplate](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-iotthingsgraph-flowtemplate.html)   
Use the `AWS::IoTThingsGraph::FlowTemplate` resource to specify a workflow template\. 

 [AWS::Pinpoint::ADMChannel](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-pinpoint-admchannel.html)   
Use the `AWS::Pinpoint::ADMChannel` resource to specify an ADM channel\. You can use the ADM channel to send push notifications through the Amazon Device Messaging \(ADM\) service to apps that run on Amazon devices, such as Kindle Fire tablets\. 

 [AWS::Pinpoint::APNSChannel](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-pinpoint-apnschannel.html)   
Use the `AWS::Pinpoint::APNSChannel` resource to specify an APNs channel\. You can use the APNs channel to send push notification messages to the Apple Push Notification service \(APNs\)\. 

 [AWS::Pinpoint::APNSSandboxChannel](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-pinpoint-apnssandboxchannel.html)   
Use the `AWS::Pinpoint::APNSSandboxChannel` resource to specify an APNs sandbox channel\. You can use the APNs sandbox channel to send push notification messages to the sandbox environment of the Apple Push Notification service \(APNs\)\. 

 [AWS::Pinpoint::APNSVoipChannel](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-pinpoint-apnsvoipchannel.html)   
Use the `AWS::Pinpoint::APNSVoipChannel` resource to specify an APNs VoIP channel\. You can use the APNs VoIP channel to send VoIP notification messages to the Apple Push Notification service \(APNs\)\. 

 [AWS::Pinpoint::APNSVoipSandboxChannel](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-pinpoint-apnsvoipsandboxchannel.html)   
Use the `AWS::Pinpoint::APNSVoipSandboxChannel` resource to specify an APNs VoIP sandbox channel\. You can use the APNs VoIP sandbox channel to send VoIP notification messages to the sandbox environment of the Apple Push Notification service \(APNs\)\. 

 [AWS::Pinpoint::App](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-pinpoint-app.html)   
Use the `AWS::Pinpoint::App` resource to specify an app\. 

 [AWS::Pinpoint::ApplicationSettings](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-pinpoint-applicationsettings.html)   
Use the `AWS::Pinpoint::ApplicationSettings` resource to specify the settings for an Amazon Pinpoint app\. 

 [AWS::Pinpoint::BaiduChannel](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-pinpoint-baiduchannel.html)   
Use the `AWS::Pinpoint::BaiduChannel` resource to update the settings of the Baidu channel for an application\. 

 [AWS::Pinpoint::Campaign](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-pinpoint-campaign.html)   
Use the `AWS::Pinpoint::Campaign` resource to update the settings for a campaign\. 

 [AWS::Pinpoint::EmailChannel](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-pinpoint-emailchannel.html)   
Use the `AWS::Pinpoint::EmailChannel` resource to update the status and settings of the email channel for an application\. 

 [AWS::Pinpoint::EventStream](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-pinpoint-eventstream.html)   
Use the `AWS::Pinpoint::EventStream` resource to create a new event stream for an application or update the settings of an existing event stream for an application\. 

 [AWS::Pinpoint::GCMChannel](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-pinpoint-gcmchannel.html)   
Use the `AWS::Pinpoint::GCMChannel` resource to specify a GCM channel\. You can use the GCM channel to send push notification messages to the Firebase Cloud Messaging \(FCM\) service, which replaced the Google Cloud Messaging \(GCM\) service\. 

 [AWS::Pinpoint::SMSChannel](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-pinpoint-smschannel.html)   
Use the `AWS::Pinpoint::SMSChannel` resource to specify an SMS channel\. To send an SMS text message, you send the message through the SMS channel\. 

 [AWS::Pinpoint::Segment](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-pinpoint-segment.html)   
Use the `AWS::Pinpoint::Segment` resource to create a new segment for an application or update the configuration, dimension, and other settings for an existing segment that's associated with an application\. 

 [AWS::Pinpoint::VoiceChannel](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-pinpoint-voicechannel.html)   
Use the `AWS::Pinpoint::VoiceChannel` resource to update the status and settings of the voice channel for an application\. 

 [AWS::SageMaker::CodeRepository](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-sagemaker-coderepository.html)   
Use the `AWS::SageMaker::CodeRepository` resource to specify a Git repository as a resource in your SageMaker account\.  | June 3, 2019 | 
| [Updated resources](#ReleaseHistory) | The following resources were updated: AWS::CodeCommit::Repository and AWS::EC2::LaunchTemplate\. 

 [Code](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-codecommit-repository-code.html)   
Use the `Code` resource to provide information about code to be committed\. 

 [S3](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-codecommit-repository-s3.html)   
Use the `S3` resource to provide information about the Amazon S3 bucket that contains the code that will be committed to the new repository\. 

 [AWS::EC2::LaunchTemplate](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-launchtemplate.html)   
In the [NetworkInterface](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ec2-launchtemplate-networkinterface.html) property, use `InterfaceType` to specify the type of network interface\.  | May 23, 2019 | 
| [New resources](#ReleaseHistory) | The following resources were added: AWS::Backup::BackupPlan, AWS::Backup::BackupSelection, AWS::Backup::BackupVault, AWS::PinpointEmail::ConfigurationSet, AWS::PinpointEmail::ConfigurationSetEventDestination, AWS::PinpointEmail::DedicatedIpPool, AWS::PinpointEmail::Identity, AWS::Transfer::Server, AWS::Transfer::User, AWS::WAFRegional::GeoMatchSet, AWS::WAFRegional::RateBasedRule, and AWS::WAFRegional::RegexPatternSet\. 

 [AWS::Backup::BackupPlan](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-backup-backupplan.html)   
Contains an optional backup plan display name and an array of BackupRule objects, each of which specifies a backup rule\. Each rule in a backup plan is a separate scheduled task and can back up a different selection of AWS resources\.  

[AWS::Backup::BackupSelection](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-backup-backupselection.html)  
Specifies a set of resources to assign to a backup plan\. 

[AWS::Backup::BackupVault](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-backup-backupvault.html)  
Creates a logical container where backups are stored\. A CreateBackupVault request includes a name, optionally one or more resource tags, an encryption key, and a request ID\. 

 [AWS::PinpointEmail::ConfigurationSet](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-pinpointemail-configurationset.html)   
Use the `AWS::PinpointEmail::ConfigurationSet` resource to specify configuration sets for the Amazon Pinpoint Email API\. 

 [AWS::PinpointEmail::ConfigurationSetEventDestination](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-pinpointemail-configurationseteventdestination.html)   
Use the `AWS::PinpointEmail::ConfigurationSetEventDestination` resource to specify destinations for events related to sending email in the Amazon Pinpoint Email API\. 

 [AWS::PinpointEmail::DedicatedIpPool](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-pinpointemail-dedicatedippool.html)   
Use the `AWS::PinpointEmail::DedicatedIpPool` resource to specify groups of dedicated IP addresses in the Amazon Pinpoint Email API\. 

 [AWS::PinpointEmail::Identity](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-pinpointemail-identity.html)   
Use the `AWS::PinpointEmail::Identity` resource to specify identities \(email addresses or domains\) for sending email through the Amazon Pinpoint Email API\. 

 [AWS::Transfer::Server](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-transfer-server.html)   
Creates an autoscaling virtual server based on Secure File Transfer Protocol \(SFTP\) in AWS\. 

 [AWS::Transfer::User](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-transfer-user.html)   
Creates a user and associates them with an existing Secure File Transfer Protocol \(SFTP\) server\. 

 [AWS::WafRegional::GeoMatchSet](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-wafregional-geomatchset.html)  
The `AWS::WAFRegional::GeoMatchSet` resource contains one or more countries that AWS WAF will search for\. 

 [AWS::WafRegional::RateBasedRule](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-wafregional-ratebasedrule.html)  
The `AWS::WAFRegional::RateBasedRule` resource is identical to a regular Rule, with one addition: a RateBasedRule counts the number of requests that arrive from a specified IP address every five minutes\. 

 [AWS::WafRegional::RegexPatternSet](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-wafregional-regexpatternset.html)  
The `AWS::WAFRegional::RegexPatternSet` resource specifies the regular expression \(regex\) pattern that you want AWS WAF to search for\.  | May 23, 2019 | 
| [Updated resources](#ReleaseHistory) | The following resources were updated: AWS::AppSync::GraphQLApi, AWS::Cognito::UserPool, AWS::Glue::Classifier, AWS::Glue::Crawler, AWS::Glue::DevEndpoint, AWS::Glue::Job, and AWS::Glue::Trigger\. 

 [AWS::AppSync::GraphQLApi](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-appsync-graphqlapi.html)   
Use the `AdditionalAuthenticationProviders` property to specify a list of additional authentication providers for the GraphqlApi API\.  
Use the `Tags` property to specify an arbitrary set of tags \(key\-value pairs\) for this GraphQL API\. 

 [AWS::Cognito::UserPool](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-cognito-userpool.html)   
In the [PasswordPolicy](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-cognito-userpool-passwordpolicy.html) property type, use the `TemporaryPasswordValidityDays` property to specify the number of days a temporary password is valid\. If the user does not sign\-in during this time, their password will need to be reset by an administrator\.  
When you set `TemporaryPasswordValidityDays` for a user pool, you will no longer be able to set the deprecated `UnusedAccountValidityDays` value for that user pool\. 

[AWS::Glue::Classifier](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-glue-classifier.html)  
Use the `CsvClassifier` property to specify a classifier for comma\-separated values \(CSV\)\. 

 [AWS::Glue::Crawler](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-glue-crawler.html)   
Use the `CrawlerSecurityConfiguration` property to specify the name of the `SecurityConfiguration` structure to be used by this crawler\.  
Use the `Tags` property to specify the tags to use with this crawler request\. You can use tags to limit access to the crawler\. 

 [AWS::Glue::DevEndpoint](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-glue-devendpoint.html)   
Use the `SecurityConfiguration` property to specify the name of the `SecurityConfiguration` structure to be used by this `DevEndpoint`\.  
Use the `Tags` property to specify the tags to use with this `DevEndpoint`\. You can use tags to limit access to the `DevEndpoint`\. 

 [AWS::Glue::Job](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-glue-job.html)   
Use the `SecurityConfiguration` property to specify the name of the `SecurityConfiguration` structure to be used with this job\.  
Use the `Tags` property to specify the tags to use with this job\. You can use tags to limit access to the job\. 

 [AWS::Glue::Trigger](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-glue-trigger.html)   
Use the `Tags` property to specify the tags to use with this trigger\. You can use tags to limit access to the trigger\.  | May 17, 2019 | 
| [New resources](#ReleaseHistory) | The following resources were added: AWS::Glue::DataCatalogEncryptionSettings, AWS::Glue::SecurityConfiguration, and AWS::MediaStore::Container\. 

 [AWS::Glue::DataCatalogEncryptionSettings](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-glue-datacatalogencryptionsettings.html)   
Sets the security configuration for a specified catalog\. After the configuration has been set, the specified encryption is applied to every catalog write thereafter\. 

 [AWS::Glue::SecurityConfiguration](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-glue-securityconfiguration.html)   
Creates a new security configuration\. 

[AWS::MediaStore::Container](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-mediastore-container.html)  
The `AWS::MediaStore::Container` resource specifies a storage container to hold objects\. A container is similar to a bucket in Amazon S3\.  
When you create a container using AWS CloudFormation, the template manages data for five API actions: creating a container, setting access logging, updating the default container policy, adding a cross\-origin resource sharing \(CORS\) policy, and adding an object lifecycle policy\.  | May 17, 2019 | 
| [Updated resource](#ReleaseHistory) | The following resource was updated: AWS::ServiceCatalog::CloudFormationProduct\. 

 [AWS::ServiceCatalog::CloudFormationProduct](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-servicecatalog-cloudformationproduct.html)   
In the [ProvisioningArtifactProperties](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-servicecatalog-cloudformationproduct-provisioningartifactproperties.html) property type, if `DisableTemplateValidation` is set to `true`, AWS Service Catalog stops validating the specified provisioning artifact even if it is invalid\.  | May 3, 2019 | 
| [New resources](#ReleaseHistory) | The following resources were added: AWS::ApiGatewayV2::ApiMapping and AWS::ApiGatewayV2::DomainName\. 

 [AWS::ApiGatewayV2::ApiMapping](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-apigatewayv2-apimapping.html)   
The AWS CloudFormation `AWS::ApiGatewayV2::ApiMapping` resource contains an API mapping\. 

 [AWS::ApiGatewayV2::DomainName](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-apigatewayv2-domainname.html)   
Use the AWS CloudFormation `AWS::ApiGatewayV2::DomainName` resource to specify a custom, friendly URL for your API in API Gateway\.  | May 3, 2019 | 
| [Limit for resources in concurrent stack operations ](#ReleaseHistory) | CloudFormation now enforces an account limit for the number of resources in concurrent stack operations\. This limit is determined by region\.For more information, see [AWS CloudFormation quotas](cloudformation-limits.md) | April 30, 2019 | 
| [Updated resources](#ReleaseHistory) | The following resources were updated: AWS::Greengrass::FunctionDefinition and AWS::Greengrass::FunctionDefinitionVersion\. 

 [AWS::Greengrass::FunctionDefinition](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-greengrass-functiondefinition.html)   
In the `FunctionConfiguration` property type, the `MemorySize` and `Timeout` properties are no longer required\. 

 [AWS::Greengrass::FunctionDefinitionVersion](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-greengrass-functiondefinitionversion.html)   
In the `FunctionConfiguration` property type, the `MemorySize` and `Timeout` properties are no longer required\.  | April 25, 2019 | 
| [Updated resources](#ReleaseHistory) | The following resources were updated: AWS::ECS::TaskDefinition, AWS::ElasticLoadBalancingV2::TargetGroup  

 [AWS::ECS::TaskDefinition](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ecs-taskdefinition.html)   
Use the `ProxyConfiguration` property to specify the configuration details for an App Mesh proxy\.  
In the `[ContainerDefinition](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ecs-taskdefinition-containerdefinitions.html)` property type:   
+ Use the `DependsOn` property to specify the dependencies defined for container startup and shutdown\.
+ Use the `StartTimeout` property to specify the time duration to wait before giving up on resolving dependencies for a container\.
+ Use the `StopTimeout` property to specify the time duration to wait before the container is forcefully killed if it doesn't exit normally on its own\.  

 [AWS::ElasticLoadBalancingV2::TargetGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-elasticloadbalancingv2-targetgroup.html)   
Use the `HealthCheckEnabled` property to indicate whether health checks are enabled\.  
The `Port`, `Protocol`, and `VpcId` properties are now required only if the target type is `instance` or `ip`\.  | April 18, 2019 | 
| [New resource](#ReleaseHistory) | The following resource was added: AWS::EC2::CapacityReservation\. 

 [AWS::EC2::CapacityReservation](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-capacityreservation.html)   
Use the `AWS::EC2::CapacityReservation` resource to create a Capacity Reservation\.  | April 18, 2019 | 
| [Updated resources](#ReleaseHistory) | The following resource was updated: AWS::Batch::JobDefinition and AWS::ServiceCatalog::CloudFormationProvisionedProduct\. 

 [AWS::Batch::JobDefinition](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-batch-jobdefinition.html)   
Use the [ResourceRequirement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-batch-jobdefinition-resourcerequirement.html) property type to specify the type and amount of a resource to assign to a container\. Currently, the only supported resource type is `GPU`\.  

 [AWS::ServiceCatalog::CloudFormationProvisionedProduct](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-servicecatalog-cloudformationprovisionedproduct.html)   
The `Tags` property requires the provisioned product to have a `RESOURCE_UPDATE` constraint with `TagUpdatesOnProvisionedProduct` set to `ALLOWED` to allow tag updates\.  
The `Tags` property now requires no interruption upon update\.  | April 4, 2019 | 
| [New resource](#ReleaseHistory) | The following resource was added: AWS::ServiceCatalog::ResourceUpdateConstraint\. 

 [AWS::ServiceCatalog::ResourceUpdateConstraint](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-servicecatalog-resourceupdateconstraint.html)   
Use the `AWS::ServiceCatalog::ResourceUpdateConstraint` resource to create a RESOURCE\_UPDATE constraint for Service Catalog\.  | April 4, 2019 | 
| [Updated resources](#ReleaseHistory) | The following resources were updated: AWS::AppStream::Fleet, AWS::AppStream::ImageBuilder, AWS::AppStream::Stack, and AWS::EKS::Cluster\. 

 [AWS::AppStream::Fleet](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-appstream-fleet.html), [AWS::AppStream::ImageBuilder](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-appstream-imagebuilder.html), and [AWS::AppStream::Stack](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-appstream-stack.html)   
Use the `Tags` property to add or overwrite one or more tags for an Amazon AppStream 2\.0 fleet, stack, or image builder\. 

 [AWS::EKS::Cluster](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-eks-cluster.html)   
Updates to the `Version` property no longer require replacement\.  | March 28, 2019 | 
| [New resources](#ReleaseHistory) | The following resources were added: AWS::AppMesh::Mesh, AWS::AppMesh::Route, AWS::AppMesh::VirtualNode, AWS::AppMesh::VirtualRouter, and AWS::AppMesh::VirtualService\. 

 [AWS::AppMesh::Mesh](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-appmesh-mesh.html)   
The `AWS::AppMesh::Mesh` resource to specify a service mesh\. A service mesh is a logical boundary for network traffic between the services that reside within it\. 

 [AWS::AppMesh::Route](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-appmesh-route.html)   
Use the `AWS::AppMesh::Route` resource to specify a route that is associated with a virtual router\. 

 [AWS::AppMesh::VirtualNode](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-appmesh-virtualnode.html)   
Use the `AWS::AppMesh::VirtualNode` resource to specify a virtual node within a service mesh\. 

 [AWS::AppMesh::VirtualRouter](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-appmesh-virtualrouter.html)   
Use the `AWS::AppMesh::VirtualRouter` resource to specify a virtual router within a service mesh\. 

 [AWS::AppMesh::VirtualService](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-appmesh-virtualservice.html.html)   
Use the `AWS::AppMesh::VirtualService` resource to specify a virtual service within a service mesh\.  | March 27, 2019 | 
| [New resources](#ReleaseHistory) | The following resources were added: AWS::Greengrass::ConnectorDefinition, AWS::Greengrass::ConnectorDefinitionVersion, AWS::Greengrass::CoreDefinition, AWS::Greengrass::CoreDefinitionVersion, AWS::Greengrass::DeviceDefinition, AWS::Greengrass::DeviceDefinitionVersion, AWS::Greengrass::FunctionDefinition, AWS::Greengrass::FunctionDefinitionVersion, AWS::Greengrass::Group, AWS::Greengrass::GroupVersion, AWS::Greengrass::LoggerDefinition, AWS::Greengrass::LoggerDefinitionVersion, AWS::Greengrass::ResourceDefinition, AWS::Greengrass::ResourceDefinitionVersion, AWS::Greengrass::SubscriptionDefinition, and AWS::Greengrass::SubscriptionDefinitionVersion\. 

 [AWS::Greengrass::ConnectorDefinition](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-greengrass-connectordefinition.html) and [AWS::Greengrass::ConnectorDefinitionVersion](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-greengrass-connectordefinitionversion.html)   
Use the `AWS::Greengrass::ConnectorDefinition` and `AWS::Greengrass::ConnectorDefinitionVersion` resources to create and manage your connectors\. 

 [AWS::Greengrass::CoreDefinition](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-greengrass-coredefinition.html) and [AWS::Greengrass::CoreDefinitionVersion](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-greengrass-coredefinitionversion.html)   
Use the `AWS::Greengrass::CoreDefinition` and `AWS::Greengrass::CoreDefinitionVersion` resources to create and manage your cores\. 

 [AWS::Greengrass::DeviceDefinition](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-greengrass-devicedefinition.html) and [AWS::Greengrass::DeviceDefinitionVersion](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-greengrass-devicedefinitionversion.html)   
Use the `AWS::Greengrass::DeviceDefinition` and `AWS::Greengrass::DeviceDefinitionVersion` resources to create and manage your devices\. 

 [AWS::Greengrass::FunctionDefinition](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-greengrass-functiondefinition.html) and [AWS::Greengrass::FunctionDefinitionVersion](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-greengrass-functiondefinitionversion.html)   
Use the `AWS::Greengrass::FunctionDefinition` and `AWS::Greengrass::FunctionDefinitionVersion` resources to create and manage your functions\. 

 [AWS::Greengrass::Group](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-greengrass-group.html) and [AWS::Greengrass::GroupVersion](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-greengrass-groupversion.html)   
Use the `AWS::Greengrass::Group` and `AWS::Greengrass::GroupVersion` resources to create and manage your Greengrass groups\. 

 [AWS::Greengrass::LoggerDefinitionVersion](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-greengrass-loggerdefinition.html) and [AWS::Greengrass::LoggerDefinition](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-greengrass-loggerdefinitionversion.html)   
Use the `AWS::Greengrass::LoggerDefinition` and `AWS::Greengrass::LoggerDefinitionVersion` resources to create and manage your logging configuration\. 

 [AWS::Greengrass::ResourceDefinition](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-greengrass-resourcedefinition.html) and [AWS::Greengrass::ResourceDefinitionVersion](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-greengrass-resourcedefinitionversion.html)   
Use the `AWS::Greengrass::ResourceDefinition` and `AWS::Greengrass::ResourceDefinitionVersion` resources to create and manage your local, machine learning, and secret resources\. 

 [AWS::Greengrass::SubscriptionDefinition](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-greengrass-subscriptiondefinition.html) and [AWS::Greengrass::SubscriptionDefinitionVersion](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-greengrass-subscriptiondefinitionversion.html)   
Use the `AWS::Greengrass::SubscriptionDefinition` and `AWS::Greengrass::SubscriptionDefinitionVersion` resources to create and manage your subscriptions\.  | March 15, 2019 | 
| [Updated resources](#ReleaseHistory) | The following resources were updated: AWS::CodeBuild::Project, AWS::OpsWorksCM::Server, and AWS::SageMaker::NotebookInstance\. 

 [AWS::CodeBuild::Project](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-codebuild-project.html)   
In the [Project Source](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-codebuild-project-source.html) property type, use the `GitSubmodulesConfig` property to get information about Git submodules for a project\.  
In the [Project S3Logs](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-codebuild-project-s3logs.html) property type, use the `EncryptionDisabled` property to disable encryption on S3 build logs\. 

 [AWS::OpsWorksCM::Server](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-opsworkscm-server.html)   
Use the `AssociatePublicIpAddress` property to associate a public IP address with the server\. 

 [AWS::SageMaker::NotebookInstance](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-sagemaker-notebookinstance.html)   
Use the `RootAccess` property to specify whether root access is enabled or disabled for users of the notebook instance\.  | March 14, 2019 | 
| [Updated resources](#ReleaseHistory) | The following resources were updated: AWS::StepFunctions::Activity and AWS::StepFunctions::StateMachine\. 

 [AWS::StepFunctions::Activity](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-stepfunctions-activity.html)   
Use the `Tags` property to specify the tags \(key\-value pairs\) that you want to attach to the Step Functions activity\. 

 [AWS::StepFunctions::StateMachine](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-stepfunctions-statemachine.html)   
Use the `Tags` property to specify the tags \(key\-value pairs\) that you want to attach to the Step Functions state machine\.  | March 7, 2019 | 
| [Updated resource](#ReleaseHistory) | The following resource was updated: AWS::SageMaker::NotebookInstance\. 

 [AWS::SageMaker::NotebookInstance](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-sagemaker-notebookinstance.html)   
Use the `VolumeSizeInGB` property to specify the size in GB of the persisted machine learning storage volume that is provisioned and attached to the SageMaker notebook instance\.  | February 28, 2019 | 
| [Updated resources](#ReleaseHistory) | The following resources were updated: AWS::ApiGateway::ApiKey, AWS::CodeBuild::Project, AWS::Elasticsearch::Domain, AWS::RDS::DBCluster, and AWS::RDS::DBInstance\. 

 [AWS::ApiGateway::ApiKey](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-apigateway-apikey.html)   
Use the `Value` property to specify the value of the API key\. 

 [AWS::CodeBuild::Project](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-codebuild-project.html)   
In the [ProjectCache](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-codebuild-project-projectcache.html) property type, you can use the `Modes` property to specify the type cache an AWS CodeBuild project uses\.  

 [AWS::Elasticsearch::Domain](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-elasticsearch-domain.html)   
Use the `NodeToNodeEncryptionOptions` property to specify whether node\-to\-node encryption is enabled\. 

 [AWS::RDS::DBCluster](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-rds-dbcluster.html)   
Use the `SourceRegion` property to specify the AWS Region which contains the source DB cluster when replicating a DB cluster\.  

 [AWS::RDS::DBInstance](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-rds-database-instance.html)   
Use the `UseDefaultProcessorFeatures` property to specify that the DB instance class of the DB instance uses its default processor features\.  | February 21, 2019 | 
| [New resources](#ReleaseHistory) | The following resources were added: AWS::RAM::ResourceShare, AWS::RoboMaker::Fleet, AWS::RoboMaker::Robot, AWS::RoboMaker::RobotApplication, AWS::RoboMaker::RobotApplicationVersion, AWS::RoboMaker::SimulationApplication, and AWS::RoboMaker::SimulationApplicationVersion\. 

 [AWS::RAM::ResourceShare](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ram-resourceshare.html)   
Use the `AWS::RAM::ResourceShare` resource to create, update, and delete an Amazon ResourceShare\. 

 [AWS::RoboMaker::Fleet](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-robomaker-fleet.html)   
Use the `AWS::RoboMaker::Fleet` resource to to create an AWS RoboMaker fleet\. 

 [AWS::RoboMaker::Robot](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-robomaker-robot.html)   
Use the `AWS::RoboMaker::Robot` resource to create an AWS RoboMaker robot\. 

 [AWS::RoboMaker::RobotApplication](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-robomaker-robotapplication.html)   
Use the `AWS::RoboMaker::RobotApplication` resource to create an AWS RoboMaker robot application\. 

 [AWS::RoboMaker::RobotApplicationVersion](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-robomaker-robotapplicationversion.html)   
Use the `AWS::RoboMaker::RobotApplicationVersion` resource to create a version of an AWS RoboMaker robot application\. 

 [AWS::RoboMaker::SimulationApplication](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-robomaker-simulationapplication.html)   
Use the `AWS::RoboMaker::SimulationApplication` resource to create an AWS RoboMaker simulation application\. 

 [AWS::RoboMaker::SimulationApplicationVersion](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-robomaker-simulationapplicationversion.html)   
Use the `AWS::RoboMaker::SimulationApplicationVersion` resource to create a version of an AWS RoboMaker simulation application\.  | February 21, 2019 | 
| [Updated resource](#ReleaseHistory) | The following resource was updated: AWS::CodeBuild::Project\. 

 [AWS::CodeBuild::Project](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-codebuild-project.html)   
In the [ProjectTriggers](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-codebuild-project-projecttriggers.html) property type, you can use the `WebhookFilters` property to specify the webhook events that trigger a new AWS CodeBuild build\.   | February 15, 2019 | 
| [New resources](#ReleaseHistory) | The following resources were added: AWS::FSx::FileSystem, AWS::KinesisAnalyticsv2::Application, AWS::KinesisAnalyticsv2::ApplicationCloudWatchLoggingOption, AWS::KinesisAnalyticsv2::ApplicationOutput, and AWS::KinesisAnalyticsv2::ApplicationReferenceDataSource\. 

 [AWS::FSx::FileSystem](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-fsx-filesystem.html)   
Use the `AWS::FSx::FileSystem` resource to create a new Amazon FSx for Lustre or Amazon FSx for Windows File Server file system\. 

 [AWS::KinesisAnalyticsV2::Application](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-kinesisanalyticsv2-application.html)   
Use the `AWS::KinesisAnalyticsV2::Application` resource to create an Amazon Kinesis Data Analytics application\. 

 [AWS::KinesisAnalyticsV2::ApplicationCloudWatchLoggingOption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-kinesisanalyticsv2-applicationcloudwatchloggingoption.html)   
Use the `AWS::KinesisAnalyticsV2::ApplicationCloudWatchLoggingOption` resource to add an Amazon CloudWatch log stream to monitor application configuration errors\. 

 [AWS::KinesisAnalyticsV2::ApplicationOutput](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-kinesisanalyticsv2-applicationoutput.html)   
Use the `AWS::KinesisAnalyticsV2::ApplicationOutput` resource to describe a SQL\-based Amazon Kinesis Data Analytics application's output configuration\. 

 [AWS::KinesisAnalyticsV2::ApplicationReferenceDataSource](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-kinesisanalyticsv2-applicationreferencedatasource.html)   
Use the `AWS::KinesisAnalyticsV2::ApplicationReferenceDataSource` resource to describe a reference data source for a SQL\-based Amazon Kinesis Data Analytics application\.  | February 15, 2019 | 
| [Updated resources](#ReleaseHistory) | The following resources were updated: AWS::OpsWorksCM::Server, AWS::ServiceDiscovery::Instance, and AWS::ServiceDiscovery::Service\. 

 [AWS::OpsWorksCM::Server](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-opsworkscm-server.html)   
`EngineAttributes` were updated to include additional attributes that you can use to create an AWS OpsWorks for Puppet Enterprise master server\. 

 [AWS::ServiceDiscovery::Instance](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-servicediscovery-instance.html)   
The `InstanceAttributes` property now takes a `String map` value\. 

 [AWS::ServiceDiscovery::Service](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-servicediscovery-service.html)   
The `DNSConfig` property is no longer required\.  
An update to the `HealthCheckCustomConfig` property now requires replacement\.  | February 8, 2019 | 
| [New resources](#ReleaseHistory) | The following resources were added: AWS::ApiGatewayV2::Api,  AWS::ApiGatewayV2::Authorizer, AWS::ApiGatewayV2::Deployment,  AWS::ApiGatewayV2::Integration, AWS::ApiGatewayV2::IntegrationResponse, AWS::ApiGatewayV2::Model, AWS::ApiGatewayV2::Route, AWS::ApiGatewayV2::RouteResponse, and AWS::ApiGatewayV2::Stage\. 

[AWS::ApiGatewayV2::Api](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-apigatewayv2-api.html)  
Use the `AWS::ApiGatewayV2::Api` resource to manage an API Gateway WebSocket API\. 

[AWS::ApiGatewayV2::Authorizer](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-apigatewayv2-authorizer.html)  
Use the `AWS::ApiGatewayV2::Authorizer` resource to represent an API Gateway authorizer function\. 

[AWS::ApiGatewayV2::Deployment](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-apigatewayv2-deployment.html)  
Use the `AWS::ApiGatewayV2::Deployment` resource to create an API Gateway WebSocket API deployment\. 

[AWS::ApiGatewayV2::Integration](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-apigatewayv2-integration.html)  
Use the `AWS::ApiGatewayV2::Integration` resource to specify information about the target backend that an API Gateway route calls\. 

[AWS::ApiGatewayV2::IntegrationResponse](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-apigatewayv2-integrationresponse.html)  
Use the `AWS::ApiGatewayV2::IntegrationResponse` resource to specify the response that API Gateway sends after a route's backend finishes processing a WebSocket message\. 

[AWS::ApiGatewayV2::Model](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-apigatewayv2-model.html)  
Use the `AWS::ApiGatewayV2::Model` resource to define the structure of a route request or response payload for an API Gateway WebSocket API\. 

[AWS::ApiGatewayV2::Route](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-apigatewayv2-route.html)  
Use the `AWS::ApiGatewayV2::Route` resource to specify information that is expected to be present in a WebSocket message payload\. 

[AWS::ApiGatewayV2::RouteResponse](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-apigatewayv2-routeresponse.html)  
Use the `AWS::ApiGatewayV2::RouteResponse` resource to define the responses that can be sent to the client that sends a message to an API Gateway WebSocket API\. 

[AWS::ApiGatewayV2::Stage](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-apigatewayv2-stage.html)  
Use the `AWS::ApiGatewayV2::Stage` resource to create a stage for an API Gateway WebSocket API deployment\.  | February 8, 2019 | 
| [Updated resources](#ReleaseHistory) | The following resources were updated: AWS::CodeBuild::Project and AWS::ElasticLoadBalancingV2::Listener\. 

 [AWS::CodeBuild::Project](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-codebuild-project.html)   
In the [Environment](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-codebuild-project-environment.html) property type, you can use the `ImagePullCredentialsType` property to specify the type of credentials AWS CodeBuild uses to pull images in your build\.   
In the [Environment](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-codebuild-project-environment.html) property type, you can use the `RegistryCredential` property to provide information about credentials that provide access to a private Docker registry\.  

 [AWS::ElasticLoadBalancingV2::Listener](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-elasticloadbalancingv2-listener.html)   
Create TLS listeners for your Network Load Balancers\.  | January 24, 2019 | 
| [New resource](#ReleaseHistory) | The following resource was added: AWS::OpsWorksCM::Server\. 

 [AWS::OpsWorksCM::Server](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-opsworkscm-server.html)   
Use the `AWS::OpsWorksCM::Server` resource to create an AWS OpsWorks for Chef Automate or AWS OpsWorks for Puppet Enterprise server\.  | January 24, 2019 | 
| [UpdateReplacePolicy attribute added](#ReleaseHistory) | Use the UpdateReplacePolicy attribute to retain or \(in some cases\) backup the existing physical instance of a resource when it is replaced during a stack update operation\. For more information, see [UpdateReplacePolicy Attribute](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-attribute-updatereplacepolicy.html)\. | January 23, 2019 | 
| [Updated resource](#ReleaseHistory) | The following resource was updated: AWS::Inspector::AssessmentTarget 

 [AWS::Inspector::AssessmentTarget](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-inspector-assessmenttarget.html)   
The `ResourceGroupArn` property is no longer required\. If unspecified, all Amazon EC2 instances in your AWS account in the current region will be included in the assessment target\.  | January 17, 2019 | 
| [Updated resource](#ReleaseHistory) | The following resource was updated: AWS::ServiceCatalog::CloudFormationProvisionedProduct\. 

 [AWS::ServiceCatalog::CloudFormationProvisionedProduct](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-servicecatalog-cloudformationprovisionedproduct.html)   
The `ProductId` property now requires no interruption upon update\.  
The `ProductName` property now requires no interruption upon update\.  
Each time a stack is created or updated, if `ProductName` is provided it will successfully resolve to `ProductId` as long as only one product exists in the account/region with that `ProductName`\.  | January 10, 2019 | 
| [New resources](#ReleaseHistory) | The following resources were added: AWS::DocDB::DBCluster, AWS::DocDB::DBClusterParameterGroup, AWS::DocDB::DBInstance, and AWS::DocDB::DBSubnetGroup\. 

[AWS::DocDB::DBCluster](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-docdb-dbcluster.html)  
Use the `AWS::DocDB::DBCluster` resource to manage an Amazon DocumentDB cluster\. 

[AWS::DocDB::DBClusterParameterGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-docdb-dbclusterparametergroup.html)  
Use the `AWS::DocDB::DBClusterParameterGroup` resource to manage an Amazon DocumentDB cluster parameter group\. 

[AWS::DocDB::DBInstance](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-docdb-dbinstance.html)  
Use the `AWS::DocDB::DBInstance` resource to manage an Amazon DocumentDB instance\. 

[AWS::DocDB::DBSubnetGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-docdb-dbsubnetgroup.html)  
Use the `AWS::DocDB::DBSubnetGroup` resource to describe an Amazon DocumentDB subnet group\.  | January 10, 2019 | 
| [Updated resources](#ReleaseHistory) | The following resources were updated: AWS::AmazonMQ::Broker, AWS::AmazonMQ::Configuration, and AWS::SageMaker::Model\. 

 [AWS::AmazonMQ::Broker](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-amazonmq-broker.html)   
Use the `Tags` property to specify an array of key\-value pairs for cost allocation tagging\. 

 [AWS::AmazonMQ::Configuration](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-amazonmq-configuration.html)   
Use the `Tags` property to specify an array of key\-value pairs for cost allocation tagging\. 

 [AWS::SageMaker::Model](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-sagemaker-model.html)   
Use the `Containers` property to specify the list of containers in the inference pipeline\.  | January 3, 2019 | 
| [New resource](#ReleaseHistory) | The following resource was added: AWS::Route53Resolver::ResolverRuleAssociation\. 

 [AWS::Route53Resolver::ResolverRuleAssociation](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-route53resolver-resolverruleassociation.html)   
Use the `AWS::Route53Resolver::ResolverRuleAssociation` resource to associate an Amazon Route 53 Resolver rule and a VPC that you created using Amazon Virtual Private Cloud \(Amazon VPC\)\.  | January 3, 2019 | 
| [Updated resource](#ReleaseHistory) | The following resource was updated: AWS::AmazonMQ::Broker\. 

 [AWS::AmazonMQ::Broker](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-amazonmq-broker.html)   
The following attributes are now available using the `Fn::Getatt` intrinsic function:  
+ `IpAddresses`
+ `MqttEndpoints`
+ `OpenWireEndpoints`
+ `AmqpEndpoints`
+ `StompEndpoints`
+ `WssEndpoints`  | December 13, 2018 | 
| [Stack instance operation limit](#ReleaseHistory) | For StackSets, you can have a maximum of 1500 stack instance operations running in a given region at the same time, per administrator account\.For more information, see [AWS CloudFormation quotas](cloudformation-limits.md)\. | December 13, 2018 | 
| [New resources](#ReleaseHistory) | The following resources were added: AWS::AmazonMQ::ConfigurationAssociation, AWS::IoTAnalytics::Channel, AWS::IoTAnalytics::Dataset, AWS::IoTAnalytics::Datastore, and AWS::IoTAnalytics::Pipeline\. 

[AWS::AmazonMQ::ConfigurationAssociation](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-amazonmq-configurationassociation.html)  
Use the `AWS::AmazonMQ::ConfigurationAssociation` resource to associate a configuration with a broker, or return information about the specified configuration association\. 

 [AWS::IoTAnalytics::Channel](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-iotanalytics-channel.html)   
Use the `AWS::IoTAnalytics::Channel` resource to create a channel\. A channel collects data from an MQTT topic and archives the raw, unprocessed messages before publishing the data to a pipeline\. 

 [AWS::IoTAnalytics::Dataset](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-iotanalytics-dataset.html)   
Use the `AWS::IoTAnalytics::Dataset` resource to create a data set\. A data set retrieves data from a data store and allows you to explore and analyze your data using machine learning tools\. 

 [AWS::IoTAnalytics::Datastore](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-iotanalytics-datastore.html)   
Use the `AWS::IoTAnalytics::Datastore` resource to create a data store\. A data store holds messages from a channel which have been processed through a pipeline\. 

 [AWS::IoTAnalytics::Pipeline](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-iotanalytics-pipeline.html)   
Use the `AWS::IoTAnalytics::Pipeline` resource to create a pipeline\. A pipeline consumes messages from one or more channels and allows you to process the messages before storing them in a data store\.  | December 13, 2018 | 
| [The CAPABILITY\_AUTO\_EXPAND capability is now available\.](#ReleaseHistory) | Use the `CAPABILITY_AUTO_EXPAND` capability to create or update a stack directly from a stack template that contains macros, without first reviewing the resulting changes in a change set first\.For more information, see [CreateStack](https://docs.aws.amazon.com/AWSCloudFormation/latest/APIReference/API_CreateStack.html) or [UpdateStack](https://docs.aws.amazon.com/AWSCloudFormation/latest/APIReference/API_UpdateStack.html) in *AWS CloudFormation API Reference*\. | December 7, 2018 | 
| [Updated resource](#ReleaseHistory) | The following resource was updated: AWS::CodeBuild::Project\. 

 [AWS::CodeBuild::Project](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-codebuild-project.html)   
+ In the [Environment](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-codebuild-project-environment.html) property type, you can use the `Certificate` property to specify a certificate to use with your build project\. 
+ In the [Artifacts](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-codebuild-project-artifacts.html) property type, you can use the `ArtifactIdentifier` property to identify the project artifact\. 
+ In the [Source](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-codebuild-project-source.html) property type, you can use the `SourceIdentifier` property to identify the project source\.   | December 6, 2018 | 
| [Updated resource](#ReleaseHistory) | The following resource was updated: AWS::Lambda::Function 

 [AWS::Lambda::Function](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-lambda-function.html)   
Use the `Layers` property to specify a list of Amazon Resource Names \(ARNs\) for the function layers to add to the function's execution environment\.   | November 29, 2018 | 
| [New resources](#ReleaseHistory) | The following resources were added: AWS::Lambda::LayerVersion, AWS::Lambda::LayerVersionPermission\. 

 [AWS::Lambda::LayerVersion](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-lambda-layerversion.html)   
Use the AWS CloudFormation `AWS::Lambda::LayerVersion` resource to create a layer version in AWS Lambda\. 

 [AWS::Lambda::LayerVersionPermission](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-lambda-layerversionpermission.html)   
Use the AWS CloudFormation `AWS::Lambda::LayerVersionPermission` resource to give other accounts permission to use a layer version in AWS Lambda\.  | November 29, 2018 | 
| [Updated resources](#ReleaseHistory) | The following resources were updated: AWS::DynamoDB::Table, AWS::EC2::Instance, and AWS::ServiceDiscovery::Service\. 

 [AWS::DynamoDB::Table](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-dynamodb-table.html)   
Use the `BillingMode` property to specify how you are charged for read and write throughput and how you manage capacity\.  
The `ProvisionedThroughput` property is now conditional\.  
In the [GlobalSecondaryIndex](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-dynamodb-gsi.html) property type, the `ProvisionedThroughput` property is now conditional\. 

 [AWS::EC2::Instance](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ec2-instance.html)   
Use the `ElasticInferenceAccelerators` property to specify a list of elastic inference accelerators for an instance\.  
Use the `LicenseSpecifications` property to associate a list of license configuration with an instance\. 

 [AWS::ServiceDiscovery::Service](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-servicediscovery-service.html)   
Use the `NamespaceId` property to specify the ID of the namespace that you want to use to create the service\.  
In the [DnsConfig](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-servicediscovery-service-dnsconfig.html) property type, use the `RoutingPolicy` property to specify the routing policy that you want to apply to all DNS records that AWS Cloud Map creates when you register an instance and specify this service\.  | November 28, 2018 | 
| [New resource](#ReleaseHistory) | The following resource was added: AWS::ServiceDiscovery::HttpNamespace\. 

 [AWS::ServiceDiscovery::HttpNamespace](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-servicediscovery-httpnamespace.html)   
Use the `HttpNamespace` resource to create an HTTP namespace for Cloud Map\.  | November 28, 2018 | 
| [New resources](#ReleaseHistory) | The following resources were added: AWS::EC2::TransitGateway, AWS::EC2::TransitGatewayAttachment, AWS::EC2::TransitGatewayRoute, AWS::EC2::TransitGatewayRouteTable, AWS::EC2::TransitGatewayRouteTableAssociation, and AWS::EC2::TransitGatewayRouteTablePropagation\. 

 [AWS::EC2::TransitGateway](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-transitgateway.html)   
Use the `AWS::EC2::TransitGateway` resource to create a transit gateway\. 

 [AWS::EC2::TransitGatewayAttachment](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-transitgatewayattachment.html)   
Use the `AWS::EC2::TransitGatewayAttachment` resource to create an attachment between a VPC and a transit gateway\. 

 [AWS::EC2::TransitGatewayRoute](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-transitgatewayroute.html)   
Use the `AWS::EC2::TransitGatewayRoute` resource to create a static route for a transit gateway route table\. 

 [AWS::EC2::TransitGatewayRouteTable](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-transitgatewayroutetable.html)   
Use the `AWS::EC2::TransitGatewayRouteTable` resource to create a route table for a transit gateway\. 

 [AWS::EC2::TransitGatewayRouteTableAssociation](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-transitgatewayroutetableassociation.html)   
Use the `AWS::EC2::TransitGatewayRouteTableAssociation` resource to associate an attachment with a transit gateway route table\. 

 [AWS::EC2::TransitGatewayRouteTablePropagation](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-transitgatewayroutetablepropagation.html)   
Use the `AWS::EC2::TransitGatewayRouteTablePropagation` resource to enable an attachment to propagate routes\.  | November 26, 2018 | 
| [New resources](#ReleaseHistory) | The following resources were added: Alexa::ASK::Skill, AWS::AppSync::FunctionConfiguration, AWS::EC2::EC2Fleet, AWS::Kinesis::StreamConsumer, AWS::Route53Resolver:ResolverEndpoint, and AWS::Route53Resolver::ResolverRule\. 

 [Alexa::ASK::Skill](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ask-skill.html)   
Use the `Alexa::ASK::Skill` resource to create an Alexa skill\. 

 [AWS::AppSync::FunctionConfiguration](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-appsync-functionconfiguration.html)   
Use the `AWS::AppSync::FunctionConfiguration` resource to describe the functions defined with appsync datasource in AWS AppSync\. 

 [AWS::EC2::EC2Fleet](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-ec2fleet.html)   
Use the `AWS::EC2::EC2Fleet` resource to launch an EC2 Fleet that can include multiple launch specifications that vary by instance type, AMI, Availability Zone, or subnet\. 

 [AWS::Kinesis::StreamConsumer](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-kinesis-streamconsumer.html)   
Use the `AWS::Kinesis::StreamConsumer` resource to to register a consumer with a Kinesis data stream\. 

 [AWS::Route53Resolver::ResolverEndpoint](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-route53resolver-resolverendpoint.html)   
Use the `AWS::Route53Resolver::ResolverEndpoint` resource to specify settings for inbound or outbound endpoints for Amazon Route 53\. 

 [AWS::Route53Resolver::ResolverRule](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-route53resolver-resolverrule.html)   
Use the `AWS::Route53Resolver::ResolverRule` resource to specify detailed information about a resolver rule, which specifies how to route DNS queries out of a VPC for Amazon Route 53\.  | November 20, 2018 | 
| [Updated resources ](#ReleaseHistory) | The following resources were updated: AWS::ApiGateway::Deployment, AWS::ApiGateway::Stage, AWS::AutoScaling::AutoScalingGroup, AWS::EC2::EIP, AWS::ElasticLoadBalancingV2::Listener, AWS::EMR::Cluster, AWS::OpsWorks::Layer, AWS::RDS::DBCluster, AWS::RDS::DBInstance, AWS::S3::Bucket, and AWS::SNS::Topic\. 

 [AWS::ApiGateway::Deployment](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-apigateway-deployment.html)   
In the [StageDescription](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-apigateway-deployment-stagedescription.html) property type, use the `Tags` property to specify the AWS CloudFormation resource tags to associate with the stage\. 

 [AWS::ApiGateway::Stage](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-apigateway-stage.html)   
Use the `Tags` property to specify the AWS CloudFormation resource tags to associate with the stage\. 

 [AWS::AutoScaling::AutoScalingGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-as-group.html)   
Use the `MixedInstancesPolicy` property to provision a combination of On\-Demand Instances and Spot Instances across multiple instance types\. When you create your Auto Scaling group, you can specify a launch configuration or template as a parameter for the top\-level object, or you can specify a mixed instances policy, but not both at the same time\. 

 [AWS::EC2::EIP](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ec2-eip.html)   
Use the `PublicIpv4Pool` property to specify the ID of an address pool that you own to let Amazon EC2 select an address from the address pool\. 

 [AWS::ElasticLoadBalancingV2::Listener](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-elasticloadbalancingv2-listener.html)   
In the [Action](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-elasticloadbalancingv2-listener-defaultactions.html) property type:  
+ Use the `AuthenticateCognitoConfig` property to specify request parameters to use when integrating with Amazon Cognito to authenticate users\.
+ Use the `AuthenticateOidcConfig` property to request parameters when using an identity provider \(IdP\) that is compliant with OpenID Connect \(OIDC\) to authenticate users\.
+ Use the `FixedResponseConfig` property to specify information about an action that returns a custom HTTP response\.
+ Use the `RedirectConfig` property to specify information about a redirect action\. 

 [AWS::ElasticLoadBalancingV2::ListenerRule](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-elasticloadbalancingv2-listenerrule.html)   
In the [Actions](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-elasticloadbalancingv2-listenerrule-actions.html) property type:  
+ Use the `AuthenticateCognitoConfig` property to specify request parameters to use when integrating with Amazon Cognito to authenticate users\.
+ Use the `AuthenticateOidcConfig` property to request parameters when using an identity provider \(IdP\) that is compliant with OpenID Connect \(OIDC\) to authenticate users\.
+ Use the `FixedResponseConfig` property to specify information about an action that returns a custom HTTP response\.
+ Use the `RedirectConfig` property to specify information about a redirect action\. 

 [AWS::EMR::Cluster](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-emr-cluster.html)   
Use the [HadoopJarStepConfig](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-elasticmapreduce-cluster-hadoopjarstepconfig.html) property type to specify a job flow step consisting of a JAR file whose main function will be executed\.  
Use the [StepConfig](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-elasticmapreduce-cluster-stepconfig.html) property type to specify a cluster \(job flow\) step\.  
Use the [KeyValue](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-elasticmapreduce-cluster-keyvalue.html) property type to specify a key value pair\.  
In the [JobFlowInstancesConfig](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-emr-cluster-jobflowinstancesconfig.html) property type, use `KeepJobFlowAliveWhenNoSteps` property to specify whether the cluster should remain available after completing all steps\. 

 [AWS::OpsWorks::Layer](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-opsworks-layer-volumeconfig.html)   
In the [VolumeConfiguration](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-opsworks-layer-volumeconfig.html) property type, use the `Encrypted` property to specify whether an Amazon EBS volume is encrypted\.  

 [AWS::RDS::DBCluster](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-rds-dbcluster.html)   
Use the `DeletionProtection` property to indicate whether the DB cluster should have deletion protection enabled\. The database can't be deleted when this value is set to `true`\. If you want to delete a stack with a protected cluster, update this value to `false` before you delete the stack\. 

 [AWS::RDS::DBInstance](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-rds-database-instance.html)   
Use the `DeleteAutomatedBackups` property to indicate whether automated backups should be deleted \(`true`\) or retained \(`false`\) when you delete a DB instance\. The default is `true`\.  
Use the `DeletionProtection` property to indicate whether the DB instance should have deletion protection enabled\. The database can't be deleted when this value is set to `true`\. If you want to delete a stack with a protected instance, update this value to `false` before you delete the stack\. 

 [AWS::S3::Bucket](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-s3-bucket.html)   
Use the `PublicAccessBlockConfiguration` property to specify the public access configuration for an Amazon S3 bucket\.  

 [AWS::SNS::Topic](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-sns-topic.html)   
Use the `KmsMasterKeyId` property to specify an AWS KMS key identifier\. This can be a key ID, key ARN, or key alias\.  | November 19, 2018 | 
| [Updated resource](#ReleaseHistory) | The following resource was updated: AWS::CodePipeline::Pipeline\. 

 [AWS::CodePipeline::Pipeline](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-codepipeline-pipeline.html)   
Use the `ArtifactStores` property to specify a list of `ArtifactStoreMap` mappings\. There must be an artifact store for the pipeline region and for each cross\-region action within the pipeline\. You can only use either `ArtifactStore` or `ArtifactStores`, not both\.  
In the [Actions](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-codepipeline-pipeline-stages-actions.html) property type, use the `Region` property to specify the action’s AWS Region, such as `us-east-1`\.  | November 13, 2018 | 
| [Stack drift detection added](#ReleaseHistory) | Drift detection enables you to detect whether a stack's actual configuration differs, or has *drifted*, from its expected template configuration as defined within AWS CloudFormation\. You can have AWS CloudFormation detect drift on an entire stack, or individual stack resources\.For more information, see [Detecting Unmanaged Configuration Changes to Stacks and Resources](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-stack-drift.html)\. | November 13, 2018 | 
| [Updated resources](#ReleaseHistory) | The following resources have been updated: AWS::ApiGateway::Deployment, AWS::ApiGateway::Stage, AWS::CloudWatch::Alarm, AWS::EC2::SecurityGroupIngress, AWS::IAM::Role, AWS::IAM::User, AWS::IoT::TopicRule, AWS::KMS::Key, AWS::RDS::DBCluster, AWS::RDS::DBInstance, AWS::Route53::RecordSet, AWS::S3::Bucket, and AWS::Workspaces::Workspace\. 

 [AWS::ApiGateway::Deployment](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-apigateway-deployment.html)   
In the [StageDescription](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-apigateway-deployment-stagedescription.html) property type, use the `TracingEnabled` property to specify whether active tracing with X\-ray is enabled for this stage\. 

 [AWS::ApiGateway::Stage](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-apigateway-stage.html)   
Use the `TracingEnabled` property to specify whether active tracing with X\-ray is enabled for this stage\. 

 [AWS::CloudWatch::Alarm](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-cw-alarm.html)   
Use the `DatapointsToAlarm` property to specify the number of datapoints that must be breaching to trigger the alarm\. This is used only if you are setting an "M out of N" alarm\. In that case, this value is the M\. 

 [AWS::EC2::SecurityGroupIngress](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ec2-security-group-ingress.html)   
Use the `SourcePrefixListId` property to specify the AWS service prefix of an Amazon VPC endpoint\. 

 [AWS::IAM::Role](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-iam-role.html)   
Use the `PermissionsBoundary` property to specify the policy that is used to set the permissions boundary for the role\. 

 [AWS::IAM::User](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-iam-user.html)   
Use the `PermissionsBoundary` property to specify the policy that is used to set the permissions boundary for the user\. 

 [AWS::IoT::TopicRule](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-iot-topicrule.html)   
In the [TopicRulePayload](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-iot-topicrule-topicrulepayload.html) property type, use the `ErrorActions` property to specify the action to take when an error occurs\.  
In the [Action](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-iot-topicrule-action.html) property type:  
+ Use the `IoTAnalytics` property to send message data to an AWS IoT Analytics channel\.
+ Use the `StepFunctionsAction` property to start execution of a Step Functions state machine\. 

 [AWS::KMS::Key](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-kms-key.html)   
Use the `PendingWindowInDays` property to specify the waiting period, specified in number of days, after which AWS KMS deletes the customer master key \(CMK\)\. 

 [AWS::RDS::DBInstance](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-rds-database-instance.html)   
Use the `EnableCloudwatchLogsExports` property to specify the list of log types that need to be enabled for exporting to CloudWatch Logs\.  
Use the `EnableIAMDatabaseAuthentication` property to enable mapping of AWS Identity and Access Management \(IAM\) accounts to database accounts\.  
Use the `EnablePerformanceInsights` property to enable Performance Insights for the DB instance\.  
Use the `PerformanceInsightsKMSKeyId` property to specify the AWS KMS key identifier for encryption of Performance Insights data\. The AWS KMS key ID is the Amazon Resource Name \(ARN\), AWS KMS key identifier, or the AWS KMS key alias for the AWS KMS encryption key\.  
Use the `PerformanceInsightsRetentionPeriod` property to specify the amount of time, in days, to retain Performance Insights data\.  
Use the `ProcessorFeatures` property to specify the number of CPU cores and the number of threads per core for the DB instance class of the DB instance\.  
Use the `PromotionTier` property to specify the order in which an Aurora Replica is promoted to the primary instance after a failure of the existing primary instance\. 

 [AWS::RDS::DBCluster](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-rds-dbcluster.html)   
Use the `EnableCloudwatchLogsExports` property to specify the list of log types that need to be enabled for exporting to CloudWatch Logs\.  
Use the `EnableIAMDatabaseAuthentication` property to enable mapping of AWS Identity and Access Management \(IAM\) accounts to database accounts\.  
Use the `BacktrackWindow` property to specify the target backtrack window, in seconds\. To disable backtracking, specify 0\. If specified, this property must be set to a number from 0 to 259,200 \(72 hours\)\. 

 [AWS::Route53::RecordSet](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-route53-recordset.html)   
Use the `MultiValueAnswer` property to route traffic approximately randomly to multiple resources, such as web servers\. Create one multivalue answer record for each resource and specify true for `MultiValueAnswer`\. 

 [AWS::S3::Bucket](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-s3-bucket.html)   
Use the `RegionalDomainName` attribute with the Fn::GetAtt function to return the regional domain name of the specified bucket\. 

 [AWS::Workspaces::Workspace](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-workspaces-workspace.html)   
Use the `Tags` property to specify the tags \(key\-value pairs\) that you want to attach to the WorkSpace\.  
Use the `WorkspaceProperties` property to specify information about a WorkSpace\.  | November 9, 2018 | 
| [The secretsmanager dynamic reference is now available\.](#ReleaseHistory) | Use the `secretsmanager` dynamic reference to retrieve entire secrets or secret values that are stored in AWS Secrets Manager for use in your templates\. *Secrets* can be database credentials, passwords, third\-party API keys, and even arbitrary text\. Using the `secretsmanager` dynamic reference guarantees that neither Secrets Manager nor CloudFormation logs or persists any resolved secret value\. For more information, see [Using Dynamic References to Specify Template Values](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/dynamic-references.html)\. | November 9, 2018 | 
| [New resources](#ReleaseHistory) | The following resources were added: AWS::DLM::LifecyclePolicy, AWS::SecretsManager::ResourcePolicy, AWS::SecretsManager::RotationSchedule, AWS::SecretsManager::Secret, and AWS::SecretsManager::SecretTargetAttachment\. 

 [AWS::DLM::LifecyclePolicy](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-dlm-lifecyclepolicy.html)   
The `AWS::DLM::LifecyclePolicy` resource creates a lifecycle policy for Amazon Data Lifecycle Manager\. 

 [AWS::SecretsManager::ResourcePolicy](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-secretsmanager-resourcepolicy.html)   
Use the `AWS::SecretsManager::ResourcePolicy` resource to define a resource\-based policy and attach it to a secret that's stored in Secrets Manager\. 

 [AWS::SecretsManager::RotationSchedule](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-secretsmanager-rotationschedule.html)   
Use the `AWS::SecretsManager::RotationSchedule` resource to configure rotation for a secret\. 

 [AWS::SecretsManager::Secret](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-secretsmanager-secret.html)   
Use the `AWS::SecretsManager::Secret` resource to create a secret and stores it in Secrets Manager\.  

 [AWS::SecretsManager::SecretTargetAttachment](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-secretsmanager-secrettargetattachment.html)   
Use the `AWS::SecretsManager::SecretTargetAttachment` resource to complete the final link between a Secrets Manager secret and its associated database\.  | November 9, 2018 | 
| [Updated resource](#ReleaseHistory) | The following resource was updated: AWS::SSM:MaintenanceWindow\. 

 [AWS::SSM:MaintenanceWindow](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ssm-maintenancewindow.html)   
Use the `StartDate` and `StartDate` property types to specify when you want the Maintenance Window to become active or inactive\. Use the `ScheduleTimezone` property type to specify the time zone to base scheduled Maintenance Window executions on, in Internet Assigned Numbers Authority \(IANA\) format\.  | November 1, 2018 | 
| [Updated resources](#ReleaseHistory) | The following resources were updated: AWS::AppSync::DataSource, AWS::AppSync::Resolver, AWS::AutoScalingPlans::ScalingPlan, AWS::Batch::JobDefinition, AWS::Batch::ComputeEnvironment, AWS::CloudWatch::Alarm, AWS::IoT1Click::Placement, and AWS::IoT1Click::Project\. 

 [AWS::AppSync::DataSource](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-appsync-datasource.html)   
Use the `RelationalDatabaseConfig` property type to specify RelationalDatabaseConfig for an AWS AppSync data source\.  
In the `HttpConfig` property type, use the `AuthorizationConfig` property to specify the authorization type and configurations for an AWS AppSync http data source\. 

 [AWS::AppSync::Resolver](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-appsync-resolver.html)   
Use the `PipelineConfig` property type to specify PipelineConfig for an AWS AppSync data source to connect with functions\. 

 [AWS::AutoScalingPlans::ScalingPlan](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-autoscalingplans-scalingplan.html)   
Use the `ScalingInstruction` property type to configure predictive scaling as part of the scaling configuration for an Amazon EC2 Auto Scaling group in an AWS Auto Scaling scaling plan\.   
Use the `PredefinedLoadMetricSpecification` property type to specify a predefined load metric for predictive scaling to use with AWS Auto Scaling\.  
Use the `CustomizedLoadMetricSpecification` property type to specify a customized load metric for predictive scaling to use with AWS Auto Scaling\. 

 [AWS::Batch::JobDefinition](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-batch-jobdefinition.html)   
The `AWS::Batch::JobDefinition` resource was updated to support AWS Batch multi\-node parallel jobs\. 

 [AWS::Batch::ComputeEnvironment](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-batch-computeenvironment.html)   
The `AWS::Batch::ComputeEnvironment` resource was updated to support Amazon EC2 launch templates and placement groups\. 

 [AWS::CloudWatch::Alarm](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-cw-alarm.html)   
Use the `Metrics` property to specify the metric data to return\.  
The `MetricName`, `Namespace`, and `Period` properties are now optional\. 

 [AWS::IoT1Click::Placement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-iot1click-placement.html)   
The `PlacementName` property is now optional\. 

 [AWS::IoT1Click::Project](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-iot1click-project.html)   
The `ProjectName` property is now optional\.  | October 25, 2018 | 
| [New resources](#ReleaseHistory) | The following resources were added: AWS::AppStream::DirectoryConfig, AWS::AppStream::Fleet, AWS::AppStream::ImageBuilder, AWS::AppStream::Stack, AWS::AppStream::StackFleetAssociation, AWS::AppStream::StackUserAssociation, AWS::AppStream::User\. 

 [AWS::AppStream::DirectoryConfig](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-appstream-directoryconfig.html)   
Use the `AWS::AppStream::DirectoryConfig` resource to describe the configuration information required to join Amazon AppStream 2\.0 fleets and image builders to Microsoft Active Directory domains\. 

 [AWS::AppStream::Fleet](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-appstream-fleet.html)   
Use the `AWS::AppStream::Fleet` resource to create a fleet for Amazon AppStream 2\.0\. A fleet consists of streaming instances that run a specified image\. 

 [AWS::AppStream::ImageBuilder](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-appstream-imagebuilder.html)   
Use the `AWS::AppStream::ImageBuilder` resource to create an image builder for Amazon AppStream 2\.0\. 

 [AWS::AppStream::Stack](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-appstream-stack.html)   
Use the `AWS::AppStream::Stack` resource to create a stack to start streaming applications to Amazon AppStream 2\.0 users\. 

 [AWS::AppStream::StackFleetAssociation](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-appstream-stackfleetassociation.html)   
Use the `AWS::AppStream::StackFleetAssociation` resource to associate a fleet with a stack for Amazon AppStream 2\.0\. 

 [AWS::AppStream::StackUserAssociation](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-appstream-stackuserassociation.html)   
Use the `AWS::AppStream::StackUserAssociation` resource to associate the specified stacks with the specified users for Amazon AppStream 2\.0\. Users in a user pool cannot be assigned to stacks with fleets that are joined to an Active Directory domain\. 

 [AWS::AppStream::User](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-appstream-user.html)   
Use the `AWS::AppStream::User` resource to create a new user in the user pool for Amazon AppStream 2\.0\.   | October 25, 2018 | 
| [Updated resource ](#ReleaseHistory) | Updated the following resources: AWS::AmazonMQ::Broker, AWS::GuardDuty::Detector, and AWS::SSM::PatchBaseline\. 

[AWS::AmazonMQ::Broker](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-amazonmq-broker.html)   
Amazon MQ now supports engine versions 5\.15\.6 and 5\.15\.0\. Property changes include:  
+ The `EngineVersion` property now requires some interruptions upon update\. 
+ The `AutoMinorVersionUpgrade` property now requires no interruption upon update\.  

 [AWS::GuardDuty::Detector](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-guardduty-detector.html)   
Use the `FindingPublishingFrequency` property to specify the frequency of notifications sent about the subsequent finding occurrences\. 

 [AWS::SSM::PatchBaseline](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ssm-patchbaseline.html)   
Use the `PatchSource` property type to provide information about the patches to use to update target instances\.  | October 18, 2018 | 
| [New resource](#ReleaseHistory) | Added the AWS::Events::EventBusPolicy resource\. 

 [AWS::Events::EventBusPolicy](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-events-eventbuspolicy.html)   
Use the `AWS::Events::EventBusPolicy` resource to grant permission to other AWS accounts that send events to your account\.  | October 18, 2018 | 
| [UseOnlineResharding update policy now available\.](#ReleaseHistory) | To modify a replication group's shards by adding or removing shards, rather than replacing the entire `AWS::ElastiCache::ReplicationGroup` resource, use the `UseOnlineResharding` update policy\. For more information, see [UseOnlineResharding Policy](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-attribute-updatepolicy.html#cfn-attributes-updatepolicy-useonlineresharding)\. | September 20, 2018 | 
| [Updated resources ](#ReleaseHistory) | The following resources have been updated: AWS::ApiGateway::Deployment, AWS::ApiGateway::Method, AWS::ApiGateway::Stage, AWS::ApiGateway::UsagePlan, AWS::CodeBuild::Project, AWS::CodeDeploy::DeploymentGroup, AWS::EC2::FlowLog, AWS::EC2::SpotFleet, AWS::EC2::VPCEndpoint, AWS::ECS::Service, AWS::ECS::TaskDefinition, and AWS::RDS::DBCluster\. 

 [AWS::ApiGateway::Deployment](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-apigateway-deployment.html)   
Use the `DeploymentCanarySettings` property to specify settings for the canary deployment\.  
In the [StageDescription](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-apigateway-deployment-stagedescription.html) property type:   
+ Use the `AccessLogSetting` property to specify settings for logging access in this stage\.
+ Use the `CanarySetting` property to specify settings for the canary deployment in this stage\. 

 [AWS::ApiGateway::Method](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-apigateway-method.html)   
Use the `AuthorizationScopes` property to specify a list of authorization scopes configured on the method\.  
In the [Integration](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-apitgateway-method-integration.html):   
+ Use the `ConnectionId` property to specify the ID of the VpcLink used for the integration when `connectionType=VPC_LINK`\.
+ Use the `ConnectionType` property to specify the type of the network connection to the integration endpoint\. 
+ Use the `TimeoutInMillis` property to specify a custom timeout between 50 and 29,000 milliseconds\. 

 [AWS::ApiGateway::Stage](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-apigateway-stage.html)   
Use the `AccessLogSetting` property to specify settings for logging access in this stage\.  
Use the `CanarySetting` property to specify settings for the canary deployment in this stage\. 

 [AWS::ApiGateway::UsagePlan](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-apigateway-usageplan.html)   
In the [ApiStage](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-apigateway-usageplan-apistage.html) property type, use the `Throttle` property to specify a map containing method\-level throttling information for API stage in a usage plan\. 

 [AWS::CodeBuild::Project](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-codebuild-project.html)   
Use the `LogsConfig` property specify logs for a project\. Logs can be CloudWatch Logs, uploaded to a specified S3 bucket, or both\.  
In the [LogsConfig](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-codebuild-project-logsconfig.html) property type:  
+ Use the `CloudWatchLogs` property to specify details about CloudWatch Logs\.
+ Use the `S3Logs` property to specify details about logs that are uploaded to an S3 bucket\. 

 [AWS::CodeDeploy::DeploymentGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-codedeploy-deploymentgroup.html)   
Use the `Ec2TagSet` property to specify information about groups of tags applied to EC2 instances\. The deployment group will include only EC2 instances identified by all the tag groups\.  
Use the `OnPremisesInstanceTagSet` property to specify information about groups of tags applied to on\-premises instances\. The deployment group will include only on\-premises instances identified by all the tag groups\.  
The `DeliverLogsPermissionArn` and `LogGroupName` properties are no longer required\. 

 [AWS::EC2::FlowLog](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-flowlog.html)   
Use the `LogDestination` property to specify the destination to which the flow log data is to be published\.   
Use the `LogDestinationType` property to specify the type of destination to which the flow log data is to be published\. Flow log data can be published to CloudWatch Logs or Amazon S3\. 

 [AWS::EC2::SpotFleet](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-spotfleet.html)   
In the `SpotFleetRequestConfigData` property type, use the `InstanceInterruptionBehavior` property to specify the behavior when a Spot Instance is interrupted\.  
In the `SpotFleetRequestConfigData` property type, use the `LoadBalancersConfig` property to specify one or more Classic Load Balancers and target groups to attach to the Spot Fleet request\. Spot Fleet registers the running Spot Instances with the specified Classic Load Balancers and target groups\.  
In the `Placement` property type, use the `Tenancy` property to specify the tenancy of the instance \(if the instance is running in a VPC\)\. An instance with a tenancy of dedicated runs on single\-tenant hardware\. The host tenancy is not supported for Spot Instances\. 

 [AWS::EC2::VPCEndpoint](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-vpcendpoint.html)   
Use the following attributes with the `Fn::GetAtt` function to return attribute values\.  
+ Use `CreationTimestamp` to return the date and time the VPC endpoint was created\.
+ Use `DnsEntries` to return the DNS entries for the endpoint\.
+ Use `NetworkInterfaceIds` to return the network interfaces for the endpoint\. 

 [AWS::ECS::Service](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ecs-service.html)   
The `ServiceRegistries` property now requires replacement upon update\.  
Use the `SchedulingStrategy` property to specify the scheduling strategy to use for the service\.   
In the [ServiceRegistry](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ecs-service-serviceregistry.html) property type:   
+ Use the `ContainerName` property to specify the container name value, already specified in the task definition, to be used for your service discovery service\. 
+ Use the `ContainerPort` property to specify the port value, already specified in the task definition, to be used for your service discovery service\. 

 [AWS::ECS::TaskDefinition](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ecs-taskdefinition.html)   
In the [LinuxParameters](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ecs-taskdefinition-linuxparameters.html) property type:   
+ Use the `Tmpfs` property to specify the container path, mount options, and size of the tmpfs mount\.
+ Use the `SharedMemorySize` property to specify the size \(in MiB\) of the `/dev/shm` volume\. 
In the [Volumes](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ecs-taskdefinition-volumes.html) property type, use the `DockerVolumeConfiguration` property to specify the configuration of a Docker volume\.  
In the [ContainerDefinition](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ecs-taskdefinition-containerdefinitions.html) property type, use the `RepositoryCredentials` property to specify the repository credentials for private registry authentication\. 

 [AWS::ElastiCache::ReplicationGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-elasticache-replicationgroup.html)   
The `NodeGroupConfiguration` and `NumNodeGroups` properties are now conditional for some update operations\.  
In the [NodeGroupConfiguration](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-elasticache-replicationgroup-nodegroupconfiguration.html) property type, use the `NodeGroupId` property to specify either the ElastiCache for Redis supplied 4\-digit id or a user supplied id for the node group these configuration values apply to\. 

 [AWS::RDS::DBCluster](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-rds-dbcluster.html)   
Use the `EngineMode` property to specify the DB engine mode of the DB cluster\.  
Use the `ScalingConfiguration` property to specify the scaling properties of the DB cluster, for DB clusters in `serverless` DB engine mode\.  | September 20, 2018 | 
| [New resources](#ReleaseHistory) | The following resources were added: AWS::IoT1Click::Device, AWS::IoT1Click::Placement, and AWS::IoT1Click::Project\. 

 [AWS::IoT1Click::Device](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-iot1click-device.html)   
Use the `AWS::IoT1Click::Device` resource to change the enabled state of an AWS IoT 1\-Click compatible device\. 

 [AWS::IoT1Click::Placement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-iot1click-placement.html)   
Use the `AWS::IoT1Click::Placement` resource to create an empty AWS IoT 1\-Click placement\. 

 [AWS::IoT1Click::Project](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-iot1click-project.html)   
Use the `AWS::IoT1Click::Project` resource to create an empty project with a placement template\.  | September 20, 2018 | 
| [New resource](#ReleaseHistory) | Added the AWS::CloudFormation::Macro resource\. 

 [AWS::CloudFormation::Macro](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-cloudformation-macro.html)   
Use the `AWS::CloudFormation::Macro` resource to create a template macro to perform custom processing on AWS CloudFormation templates\.  | September 6, 2018 | 
| [Macros now available](#ReleaseHistory) | Use macros to to perform custom processing on templates, from simple actions like find\-and\-replace operations to extensive transformations of entire templates\. See [Using AWS CloudFormation Macros to Perform Custom Processing on Templates](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/template-macros.html) for more information\. | September 6, 2018 | 
| [Updated resources](#ReleaseHistory) | Added the Logs property to AWS::AmazonMQ::Broker\. Added the SecondaryArtifacts and SecondarySources properties to AWS::CodeBuild::Project\. 

[AWS::AmazonMQ::Broker](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-amazonmq-broker.html)   
Use the `Logs` property to enable general or audit logging for an Amazon MQ broker\. 

 [AWS::CodeBuild::Project](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-codebuild-project.html)   
In the [Artifacts](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-codebuild-project-artifacts.html) property type, you can use the `SecondaryArtifacts` property to specify secondary artifacts for a build project\. You can use the `SecondarySources` property to specify secondary inputs for a build project\.  | August 30, 2018 | 
| [Updated resources](#ReleaseHistory) | Added the Configuration property to AWS::Glue::Crawler\. Added the JsonClassifier and XMLClassifier properties to AWS::Glue::Classifier\. 

 [AWS::Glue::Crawler](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-glue-crawler.html)   
Use the `Configuration` property to specify crawler configuration information\. This versioned JSON string allows users to specify aspects of a crawler's behavior\. 

 [AWS::Glue::Classifier](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-glue-classifier.html)   
Use the `JsonClassifier` property to specify AWS Glue classifier for JSON\.  
Use the `XMLClassifier` property to specify AWS Glue classifier for XML content\.  | August 23, 2018 | 
| [AWS CloudFormation now supports VPC endpoints powered by PrivateLink\.](#ReleaseHistory) | You can use a VPC endpoint to create a private connection between your VPC and AWS CloudFormation without requiring access over the Internet, through a NAT instance, a VPN connection, or AWS Direct Connect\. For more information, see [Setting Up VPC Endpoints for AWS CloudFormation](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/cfn-vpce-bucketnames.html)\. | August 22, 2018 | 
| [Dynamic references support secure strings](#ReleaseHistory) | Use new dynamic references to specify values that are stored and managed in other services, including Systems Manager Parameter Store SecureString type parameters, in your stack templates\.For more information, see [Using Dynamic References to Specify Template Values](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/dynamic-references.html)\. | August 16, 2018 | 
| [Updated resources](#ReleaseHistory) | The following resources were updated: AWS::ApiGateway::DomainName, AWS::CertificateManager::Certificate, AWS::EC2::VPCPeeringConnection, AWS::EFS::FileSystem, AWS::EMR::Cluster, AWS::RDS::DBClusterParameterGroup, AWS::SNS::Subscription, and AWS::SQS::Queue\. 

 [AWS::ApiGateway::DomainName](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-apigateway-domainname.html)   

Use the following attributes with the `Fn::GetAtt` intrinsic function:
+ The `DistributionHostedZoneId` attribute returns the region\-agnostic Amazon Route 53 Hosted Zone ID of the edge\-optimized endpoint\. 
+ The `RegionalDomainName` attribute returns the domain name associated with the regional endpoint for this custom domain name\. 
+ The `RegionalHostedZoneId` attribute returns the region\-specific Amazon Route 53 Hosted Zone ID of the regional endpoint\. 

 [AWS::CertificateManager::Certificate](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-certificatemanager-certificate.html)  
Use the `ValidationMethod` property to specify the method you want to use if you are requesting a public certificate to validate that you own or control a domain\. 

 [AWS::EC2::VPCPeeringConnection](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-vpcpeeringconnection.html)   
Use the `PeerRegion` property to specify the region code for the accepter VPC, if the accepter VPC is located in a region other than the region in which you make the request\. 

 [AWS::EFS::FileSystem](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-efs-filesystem.html)   
+ Use the `ProvisionedThroughputInMibps` property to specify the throughput, measured in MiB/s, that you want to provision for a file system that you're creating\. 
+ Use the `ThroughputMode` property to specify the throughput mode for the file system to be created\.  

 [AWS::EMR::Cluster](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-emr-cluster.html)   
Use the `KerberosAttributes` property to specify attributes for Kerberos configuration when Kerberos authentication is enabled using a security configuration\. 

 [AWS::RDS::DBClusterParameterGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-rds-dbclusterparametergroup.html)   
The `Tags` property now requires no interruption to update\. 

 [AWS::SNS::Subscription](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-sns-subscription.html)   
+ Use the `DeliveryPolicy` property to specify the JSON serialization of the subscription's delivery policy\.
+ Use the `FilterPolicy` property to specify the filter policy JSON that is assigned to the subscription\.
+ Use the `RawMessageDelivery` property to specify if raw message delivery is enabled for the subscription\.
+ Use the `Region` property to specify the region in which the topic resides\. 

 [AWS::SQS::Queue](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-sqs-queues.html)   
Use the `Tags` property to specify the tags that you want to attach to this queue\.  | August 15, 2018 | 
| [Updated resource](#ReleaseHistory) | Added the SSESpecification property to AWS::DAX::Cluster\. 

 [AWS::DAX::Cluster](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-dax-cluster.html)   
Use the `SSESpecification` property to specify the settings to enable server\-side encryption\.   | August 9, 2018 | 
| [New resource](#ReleaseHistory) | Added the AWS::EC2::VPCEndpointServicePermissions resource\. 

 [AWS::EC2::VPCEndpointServicePermissions](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-vpcendpointservicepermissions.html)   
Grant or revoke permissions for service consumers to connect the VPC endpoint service\.  | August 9, 2018 | 
| [Updated resource](#ReleaseHistory) | Added the OverrideArtifactName property to AWS::CodeBuild::Project\. 

 [AWS::CodeBuild::Project](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-codebuild-project.html)   
In the [Artifacts](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-codebuild-project-artifacts.html) property type, set the `OverrideArtifactName` property to true to override the artifact name with a name specified in the buildspec file\. The name specified in a buildspec file is calculated at build time and uses the Shell command language\. For example, you can append a date and time to your artifact name so that it is always unique\.  | August 7, 2018 | 
| [Updated resource](#ReleaseHistory) | Added the EncryptionDisabled property to AWS::CodeBuild::Project\. 

 [AWS::CodeBuild::Project](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-codebuild-project.html)   
In the [Artifacts](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-codebuild-project-artifacts.html) property type, set the `EncryptionDisabled` property to true to disable encryption for build output artifacts\. This option is only valid if your artifact type is Amazon S3\. If this is set to true with another artifact type, an invalidInputException will be thrown\.  | July 26, 2018 | 
| [Updated resource](#ReleaseHistory) | Added the Timeout property to AWS::Batch::JobDefinition\. 

 [AWS::Batch::JobDefinition](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-batch-jobdefinition.html)   
Use the `Timeout` property type to specify a job timeout configuration\.  | July 19, 2018 | 
| [New resource](#ReleaseHistory) | The following resource was added: AWS::IAM::ServiceLinkedRole\. 

 [AWS::IAM::ServiceLinkedRole](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-iam-servicelinkedrole.html)   
Use the `AWS::IAM::ServiceLinkedRole` resource to create a service\-linked role in IAM\. A service\-linked role is a unique type of IAM role that is linked directly to an AWS service\. Service\-linked roles are predefined by the service and include all the permissions that the service requires to call other AWS services on your behalf\.  | July 19, 2018 | 
| [Updated resources](#ReleaseHistory) | Added the FieldLevelEncryptionId property to AWS::CloudFront::Distribution property types\. 

 [AWS::CloudFront::Distribution](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-cloudfront-distribution.html)   
In the [CacheBehavior](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-cloudfront-distribution-cachebehavior.html) and [DefaultCacheBehavior](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-cloudfront-distribution-defaultcachebehavior.html) property types, use the `FieldLevelEncryptionId` property to specify the ID for the field\-level encryption configuration that you want CloudFront to use for encrypting specific fields of data for a cache behavior or for the default cache behavior\.  | July 18, 2018 | 
| [Updated resource](#ReleaseHistory) | Added the HttpConfig property to AWS::AppSync::DataSource\. 

 [AWS::AppSync::DataSource](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-appsync-datasource.html)   
Use the `HttpConfig` property type to specify HttpConfig for an AWS AppSync data source\.  | July 12, 2018 | 
| [Updated resource](#ReleaseHistory) | Added the ReportBuildStatus property to AWS::CodeBuild::Project\. 

 [AWS::CodeBuild::Project](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-codebuild-project.html)   
In the [Source](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-codebuild-project-source.html) property type, use the `ReportBuildStatus` property to specify whether to send your source provider the status of a build's start and completion\.  | July 10, 2018 | 
| [New resource](#ReleaseHistory) | The following resource was added: AWS::CodePipeline::Webhook\. 

 [AWS::CodePipeline::Webhook](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-codepipeline-webhook.html)   
Use the `AWS::CodePipeline::Webhook` resource to create a webhook that connects your pipeline to an external event, such as a GitHub source repository change, which triggers your pipeline to start every time the external event occurs\.  | July 5, 2018 | 
| [Updated resource](#ReleaseHistory) | Added the following properties to AWS::EC2::VPCEndpoint: PrivateDnsEnabled, SecurityGroupIds, SubnetIds, and VpcEndpointType\. 

 [AWS::EC2::VPCEndpoint](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-vpcendpoint.html)   
Use the `PrivateDnsEnabled` property to indicate whether to associate a private hosted zone with the specified VPC\.  
Use the `SecurityGroupIds` property to specify the ID of one or more security groups to associate with the endpoint network interface\.  
Use the `SubnetIds` property to specify the ID of one or more subnets in which to create an endpoint network interface\.  
Use the `VpcEndpointType` property to specify the type of endpoint\.   | June 21, 2018 | 
| [New resources](#ReleaseHistory) | The following resources were added: AWS::EC2::VPCEndpointConnectionNotification and AWS::EC2::VPCEndpointService\. 

 [AWS::EC2::VPCEndpointConnectionNotification](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-vpcendpointconnectionnotification.html)   
Use the `AWS::EC2::VPCEndpointConnectionNotification` resource to create a connection notification for the specified VPC endpoint or VPC endpoint service\. 

 [AWS::EC2::VPCEndpointService](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-vpcendpointservice.html)   
Use the `AWS::EC2::VPCEndpointService` resource to create a VPC endpoint service configuration to which service consumers \(AWS accounts, IAM users, and IAM roles\) can connect\.  | June 21, 2018 | 
| [Updated resource](#ReleaseHistory) | Added the following property to AWS::ServiceDiscovery::Service: HealthCheckCustomConfig\. 

 [AWS::ServiceDiscovery::Service](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-servicediscovery-service.html)   
Use the `HealthCheckCustomConfig` property to specify information about an optional custom health check\.  | June 14, 2018 | 
| [New resources](#ReleaseHistory) | The following new resources were released: AWS::AmazonMQ::Broker and AWS::AmazonMQ::Configuration\.  

 [AWS::AmazonMQ::Broker](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-amazonmq-broker.html)   
Use the `AWS::AmazonMQ::Broker` resource to create a broker, add configuration changes or modify users for the specified broker, return information about the specified broker, or delete the specified broker\. 

 [AWS::AmazonMQ::Configuration](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-amazonmq-configuration.html)   
Use the `AWS::AmazonMQ::Configuration` resource to create a configuration, update the specified configuration, or return information about the specified configuration\.   | June 14, 2018 | 
| [New resource](#ReleaseHistory) | The following resource was added: AWS::SSM::ResourceDataSync\. 

 [AWS::SSM::ResourceDataSync](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ssm-resourcedatasync.html)   
Use the `AWS::SSM::ResourceDataSync` resource to create or delete a Resource Data Sync for Systems Manager Inventory\. You can use Resource Data Sync to send Inventory data collected from all of your Systems Manager managed instances to a single Amazon S3 bucket\.  | June 11, 2018 | 
| [New resource](#ReleaseHistory) | The following resource was released: AWS::EKS::Cluster\. 

 [AWS::EKS::Cluster](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-eks-cluster.html)   
Use the `AWS::EKS::Cluster` resource to create Amazon EKS clusters\.  | June 5, 2018 | 
| [Updated resource](#ReleaseHistory) | For the AWS::GuardDuty::Master resource, the InvitationId property is now optional\. 

 [AWS::GuardDuty::Master](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-guardduty-master.html)   
The `InvitationId` property is now optional\.  | May 31, 2018 | 
| [New resources](#ReleaseHistory) | The following new resources were released: AWS::SageMaker::Endpoint, AWS::SageMaker::EndpointConfig, AWS::SageMaker::Model, AWS::SageMaker::NotebookInstance, and AWS::SageMaker::NotebookInstanceLifecycleConfig\. 

 [AWS::SageMaker::Endpoint](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-sagemaker-endpoint.html)   
Use the `AWS::SageMaker::Endpoint` resource to create a SageMaker endpoint to host trained models\. 

 [AWS::SageMaker::EndpointConfig](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-sagemaker-endpointconfig.html)   
Use the `AWS::SageMaker::EndpointConfig` resource to create a configuration for an endpoint\. 

 [AWS::SageMaker::Model](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-sagemaker-model.html)   
Use the `AWS::SageMaker::Model` resource to create a model to host at an Amazon SageMaker endpoint\. 

 [AWS::SageMaker::NotebookInstance](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-sagemaker-notebookinstance.html)   
Use the `AWS::SageMaker::NotebookInstance` resource to create an Amazon SageMaker notebook instance\. 

 [AWS::SageMaker::NotebookInstanceLifecycleConfig](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-sagemaker-notebookinstancelifecycleconfig.html)   
Use the `AWS::SageMaker::NotebookInstanceLifecycleConfig` resource to specify shell scripts that run when you create or start a notebook instance\.  | May 31, 2018 | 
| [Stack sets now support customized execution roles](#ReleaseHistory) | Use customized execution roles in target accounts to control the stack resources that users or groups can include in their stack sets\. For more information, see [Granting Permissions for Stack Set Operations](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/stacksets-prereqs.html)\.  | May 30, 2018 | 
| [Selective updates of stack instances](#ReleaseHistory) | Use the optional Accounts and Regions parameters to specify the accounts and regions in which to update stack instances during a stack set update operation\. For more information, see [UpdateStackSet](https://docs.aws.amazon.com/AWSCloudFormation/latest/APIReference/API_UpdateStackSet.html) in the *AWS CloudFormation API Reference*\. | May 30, 2018 | 
| [New resources](#ReleaseHistory) | The following new resources were released: AWS::Neptune::DBCluster, AWS::Neptune::DBClusterParameterGroup, AWS::Neptune::DBInstance, AWS::Neptune::DBParameterGroup, and AWS::Neptune::DBSubnetGroup\. 

 [AWS::Neptune::DBCluster](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-neptune-dbcluster.html)   
Use the `AWS::Neptune::DBCluster` resource to create an Amazon Neptune DB cluster\. 

 [AWS::Neptune::DBClusterParameterGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-neptune-dbclusterparametergroup.html)   
Use the `AWS::Neptune::DBClusterParameterGroup` resource to create a DB cluster parameter group\. 

 [AWS::Neptune::DBInstance](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-neptune-dbinstance.html)   
Use the `AWS::Neptune::DBInstance` resource to create an Amazon Neptune database instance\. 

 [AWS::Neptune::DBParameterGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-neptune-dbparametergroup.html)   
Use the `AWS::Neptune::DBParameterGroup` resource to create a custom parameter group for Amazon Neptune\. 

 [AWS::Neptune::DBSubnetGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-neptune-dbsubnetgroup.html)   
Use the `AWS::Neptune::DBSubnetGroup` resource to create an Amazon Neptune database subnet group that contains subnets\.  | May 30, 2018 | 
| [Updated resources](#ReleaseHistory) | The following resources were updated: AWS::ApiGateway::RestApi, AWS::AutoScaling::AutoScalingGroup, AWS::AutoScaling::LaunchConfiguration, AWS::DirectoryService::MicrosoftAD, AWS::DynamoDB::Table, AWS::EC2::Instance, AWS::ECS::Service, AWS::ECS::TaskDefinition, AWS::Elasticsearch::Domain, AWS::IAM::Role, AWS::KinesisFirehose::DeliveryStream, AWS::Lambda::EventSourceMapping, AWS::Logs::MetricFilter, and AWS::SSM::Association\. 

 [AWS::ApiGateway::RestApi](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-apigateway-restapi.html)   
Use the `Policy` property to specify a policy document that contains the permissions for the specified RestAPI\. 

 [AWS::AutoScaling::AutoScalingGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-as-group.html)   
Use the `ServiceLinkedRoleARN` property to specify the Amazon Resource Name \(ARN\) of the service\-linked role that the Auto Scaling group uses to call other AWS services on your behalf\. 

 [AWS::AutoScaling::LaunchConfiguration](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-as-launchconfig.html)   
Use the `LaunchConfigurationName` property to specify the name of the launch configuration\.  

 [AWS::DirectoryService::MicrosoftAD](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-directoryservice-microsoftad.html)   
Use the `Edition` property to specify the AWS Microsoft AD edition to use\. 

 [AWS::DynamoDB::Table](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-dynamodb-table.html)   
Use the `PointInTimeRecoverySpecification` property to specify the settings used to enable point in time recovery\. 

 [AWS::EC2::Instance](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ec2-instance.html)   
Use the `LaunchTemplate` property to specify the launch template to use for an Amazon EC2 instance\. 

 [AWS::ECS::Service](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ecs-service.html)   
Use the `ServiceRegistry` property type to specify the details of the service registry\. 

 [AWS::ECS::TaskDefinition](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ecs-taskdefinition.html)   
Use the `HealthCheck` property type to specify a container health check\. 

 [AWS::Elasticsearch::Domain](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-elasticsearch-domain.html)   
Use the `EncryptionAtRestOptions` property type to specify whether the domain should encrypt data at rest, and if so, the AWS Key Management Service \(KMS\) key to use\. 

 [AWS::IAM::Role](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-iam-role.html)   
Use the `RoleId` attribute to have `Fn::GetAtt` return the stable and unique string identifying the role\.   
Use the `MaxSessionDuration` property to specify the maximum session duration \(in seconds\) for the specified role\. 

 [AWS::KinesisFirehose::DeliveryStream](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-kinesisfirehose-deliverystream.html)   
Use the `SplunkDestinationConfiguration` property to specify the configuration of a destination in Splunk for a Kinesis Data Firehose delivery stream\. 

 [AWS::Lambda::EventSourceMapping](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-lambda-eventsourcemapping.html)   
The `StartingPosition` property is no longer required\. 

 [AWS::Logs::MetricFilter](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-logs-metricfilter.html)   
In the [MetricTransformation](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-logs-metricfilter-metrictransformation.html) property type, use the `DefaultValue` property to specify the value to emit when a filter pattern does not match a log event\.  

 [AWS::SSM::Association](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ssm-association.html)   
Use the `OutputLocation` property to specify an Amazon S3 bucket where you want to store the results of an association request\.  | May 24, 2018 | 
| [New resources](#ReleaseHistory) | The following new resources were released: AWS::ServiceCatalog::AcceptedPortfolioShare, AWS::ServiceCatalog::CloudFormationProduct, AWS::ServiceCatalog::LaunchNotificationConstraint, AWS::ServiceCatalog::LaunchRoleConstraint, AWS::ServiceCatalog::LaunchTemplateConstraint, AWS::ServiceCatalog::Portfolio, AWS::ServiceCatalog::PortfolioPrincipalAssociation, AWS::ServiceCatalog::PortfolioProductAssociation, AWS::ServiceCatalog::PortfolioShare, AWS::ServiceCatalog::TagOption, and AWS::ServiceCatalog::TagOptionAssociation\. 

 [AWS::ServiceCatalog::AcceptedPortfolioShare](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-servicecatalog-acceptedportfolioshare.html)   
Use the `AWS::ServiceCatalog::AcceptedPortfolioShare` resource to accept an offer to share the specified portfolio for AWS Service Catalog\. 

 [AWS::ServiceCatalog::CloudFormationProduct](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-servicecatalog-cloudformationproduct.html)   
Use the `AWS::ServiceCatalog::CloudFormationProduct` resource to create a product for AWS Service Catalog\. 

 [AWS::ServiceCatalog::LaunchNotificationConstraint](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-servicecatalog-launchnotificationconstraint.html)   
Use the `AWS::ServiceCatalog::LaunchNotificationConstraint` resource to create a notification constraint for AWS Service Catalog\. 

 [AWS::ServiceCatalog::LaunchRoleConstraint](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-servicecatalog-launchroleconstraint.html)   
Use the `AWS::ServiceCatalog::LaunchRoleConstraint` resource to create a launch constraint for AWS Service Catalog\. 

 [AWS::ServiceCatalog::LaunchTemplateConstraint](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-servicecatalog-launchtemplateconstraint.html)   
Use the `AWS::ServiceCatalog::LaunchTemplateConstraint` resource to create a template constraint for AWS Service Catalog\. 

 [AWS::ServiceCatalog::Portfolio](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-servicecatalog-portfolio.html)   
Use the `AWS::ServiceCatalog::Portfolio` resource to create a portfolio for AWS Service Catalog\. 

 [AWS::ServiceCatalog::PortfolioPrincipalAssociation](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-servicecatalog-portfolioprincipalassociation.html)   
Use the `AWS::ServiceCatalog::PortfolioPrincipalAssociation` resource to associate a principal with a portfolio for AWS Service Catalog\. 

 [AWS::ServiceCatalog::PortfolioProductAssociation](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-servicecatalog-portfolioproductassociation.html)   
Use the `AWS::ServiceCatalog::PortfolioProductAssociation` resource to associate a product with a portfolio for AWS Service Catalog\. 

 [AWS::ServiceCatalog::PortfolioShare](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-servicecatalog-portfolioshare.html)   
Use the `AWS::ServiceCatalog::PortfolioShare` resource to share a portfolio for AWS Service Catalog\. 

 [AWS::ServiceCatalog::TagOption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-servicecatalog-tagoption.html)   
Use the `AWS::ServiceCatalog::TagOption` resource to create a TagOption\. 

 [AWS::ServiceCatalog::TagOptionAssociation](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-servicecatalog-tagoptionassociation.html)   
Use the `AWS::ServiceCatalog::TagOptionAssociation` resource to associate a TagOption with a resource for AWS Service Catalog\.   | May 24, 2018 | 
| [AWS CloudFormation now creates S3 buckets with encryption enabled](#ReleaseHistory) | For Amazon S3 buckets that AWS CloudFormation creates to store uploaded stack templates, server\-side encryption is now enabled by default, thereby encrypting all objects stored in those buckets\. For more information, see [Selecting a Stack Template](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/cfn-using-console-create-stack-template.html)\.  | May 24, 2018 | 
| [New resource](#ReleaseHistory) | The following resource was released: AWS::Budgets::Budget\. 

 [AWS::Budgets::Budget](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-budgets-budget.html)   
Use the `AWS::Budgets::Budget` resource to create a budget\.  | May 22, 2018 | 
| [FIPS endpoints added](#ReleaseHistory) | AWS CloudFormation now offers new endpoints which use FIPS 140\-2 validated cryptographic modules in the following public US regions: US\-East\-1, US\-East\-2, US\-West\-1, and US\-West\-2\. See [Regions and Endpoints](https://docs.aws.amazon.com/general/latest/gr/rande.html#cfn_region) in the *[Amazon Web Services General Reference](https://docs.aws.amazon.com/general/latest/gr/)* for the new FIPS\-compliant endpoint URLs\. | May 17, 2018 | 
| [New resource](#ReleaseHistory) | The following resource was released: AWS::AutoScalingPlans::ScalingPlan\. 

 [AWS::AutoScalingPlans::ScalingPlan](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-autoscalingplans-scalingplan.html)   
Use the `AWS::AutoScalingPlans::ScalingPlan` resource to create a scaling plan for the scalable resources for your application\.  | May 9, 2018 | 
| [New resource](#ReleaseHistory) | The following resource was released: AWS::GuardDuty::Filter\. 

 [AWS::GuardDuty::Filter](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-guardduty-filter.html)   
Use the `AWS::GuardDuty::Filter` resource to create a filter for your GuardDuty findings\.  | May 8, 2018 | 
| [Updated resources](#ReleaseHistory) | The following resources were updated: AWS::AppSync::GraphQLApi and AWS::GuardDuty::Member\. 

 [AWS::AppSync::GraphQLApi](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-appsync-graphqlapi.html)   
Use the `OpenIDConnectConfig` property to specify the authorization configuration for using an OpenId Connect compliant service with your GraphQL endpoint\. 

 [AWS::GuardDuty::Member](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-guardduty-member.html)   
Use the `DisableEmailNotification` property to specify whether an email notification is to be sent to the accounts that you want to invite to GuardDuty as members\. When set to 'True', email notification is not sent to the invitees\.  | May 1, 2018 | 
| [New resource](#ReleaseHistory) | The following resource was released: AWS::ServiceCatalog::CloudFormationProvisionedProduct\.  

 [AWS::ServiceCatalog::CloudFormationProvisionedProduct](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-servicecatalog-cloudformationprovisionedproduct.html)   
Use the `AWS::ServiceCatalog::CloudFormationProvisionedProduct` resource to provision the specified product for AWS Service Catalog\.   | May 1, 2018 | 

## Earlier updates<a name="release-history-earlier-updates"></a>

The following table describes important changes in each release of the AWS CloudFormation User Guide before May 2018\.


| Change | Release Date | Description | API Version | 
| --- | --- | --- | --- | 
|  Updated resources  |  July 22, 2019  |  Use the `encryptionOptions` property to specify an AWS\-owned CMK or a customer\-managed CMK for Amazon MQ brokers\.  |  2010\-05\-15  | 
|  Stack set naming convention  |  April 10, 2018  |  AWS CloudFormation stacks created using stack sets now follow a new naming convention, in which the stack name contains the stack set name\.  |  2010\-05\-15  | 
|  New resources  |  April 10, 2018  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html)  |  2010\-05\-15  | 
|  Updated resource  |  April 10, 2018  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html)  |  2010\-05\-15  | 
|  New resources  |  April 4, 2018  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html)  |  2010\-05\-15  | 
|  Stack sets now support customized administrator roles  |  March 29, 2018  |  Use customized administrator roles to control which users or groups can manage specific stack sets within the same administrator account\. For more information, see [Granting Permissions for Stack Set Operations](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/stacksets-prereqs.html)\.  |  2010\-05\-15  | 
|  New resource  |  March 29, 2018  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html)  |  2010\-05\-15  | 
|  Updated resources  |  March 29, 2018  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html)  |  2010\-05\-15  | 
|  New `Fn::Cidr` intrinsic function  |  March 6, 2018  |  Returns the specified Cidr address block\. For more information, see [Fn::Cidr](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-cidr.html)\.  |  2010\-05\-15  | 
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
|  New `CodeDeployLambdaAliasUpdate` update policy  |  November 28, 2017  |  Use the `CodeDeployLambdaAliasUpdate` update policy to perform an CodeDeploy deployment when the version changes on an `AWS::Lambda::Alias` resource\. For more information, see [UpdatePolicy Attribute](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-attribute-updatepolicy.html)\.  |  2010\-05\-15  | 
|  New `SSM` parameter types  |  November 21, 2017  |  Use `SSM` parameter types to use existing parameters from Systems Manager Parameter Store\. **Note**: AWS CloudFormation doesn't currently support the `SecureString` type\. For more information, see [SSM Parameter Types](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/parameters-section-structure.html#aws-ssm-parameter-types)\.  |  2010\-05\-15  | 
|  New `ResolvedValue` field for `Parameter` data type  |  November 21, 2017  |  The `ResolvedValue` field returns the value that's used in the stack definition for an `SSM` parameter\. For more information, see the [ Parameter](https://docs.aws.amazon.com/AWSCloudFormation/latest/APIReference/API_Parameter.html) data type in the *AWS CloudFormation API Reference*\.  |  2010\-05\-15  | 
|  Updated resources  |  November 20, 2017  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html)  |  2010\-05\-15  | 
|  New `NoEcho` field for custom resource `Response` objects  |  November 20, 2017  |  You can now use the optional `NoEcho` field to mask the output of a custom resource\. For more information, see [Custom Resource Response Objects](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/crpg-ref-responses.html)\. The corresponding `noEcho` parameter is supported by the `send` method\. For more information, see [cfn\-response Module](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-lambda-function-code.html#cfn-lambda-function-code-cfnresponsemodule)\.  |  2010\-05\-15  | 
|  Stack instance overrides added for stack sets\.  |  November 17, 2017  |  AWS CloudFormation StackSets allows you to override parameter values in stack instances by account and region\. You can override parameter values when you create the stack instances, or when updating existing stack instances\. For more information, see [Override Parameters on Stack Instances](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/stackinstances-override.html)\.  |  2010\-05\-15  | 
|  Updated resource  |  November 15, 2017  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html)  |  2010\-05\-15  | 
|  StackSets now supports a maximum of 500 stack instances per stack set\.  |  November 6, 2017  |  You can now create up to a maximum of 500 stack instances per stack set\. For more information on AWS CloudFormation limits, see [AWS CloudFormation Limits](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/cloudformation-limits.html)\.  |  2010\-05\-15  | 
|  New resources  |  November 2, 2017  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html)  |  2010\-05\-15  | 
| Updated resources | November 2, 2017 |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html)  | 2010\-05\-15 | 
|  New resources  |  October 24, 2017  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html)  |  2010\-05\-15  | 
|  New resources  |  October 11, 2017  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html)  |  2010\-05\-15  | 
|  New resource  |  October 10, 2017  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html)  |  2010\-05\-15  | 
|  New resource  |  September 27, 2017  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html)  |  2010\-05\-15  | 
| Updated resources | September 27, 2017 |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html)  | 2010\-05\-15 | 
| Termination protection added for stacks\. | September 26, 2017 | Enabling termination protection on a stack prevents it from being accidentally deleted\. A user cannot delete a stack with termination protection enabled\. For more information, see [Protecting a Stack From Being Deleted](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-protect-stacks.html)\. | 2010\-05\-15 | 
|  Changed default `umask` value from version 1\.4\-22 onwards  |  September 14, 2017  |  The default `umask` parameter value for the cfn\-hup\.conf configuration file is now `022`\. For more information, see [cfn\-hup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/cfn-hup.html) \.  |    | 
| Updated resources | September 7, 2017 |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html)  | 2010\-05\-15 | 
|  Rollback triggers added to the AWS CloudFormation API  |  August 31, 2017  |  Rollback triggers enable you to have AWS CloudFormation monitor the state of your application during stack creation and updating, and to roll back that operation if the application breaches the threshold of any of the alarms you've specified\. For more information, see [ RollbackConfiguration](https://docs.aws.amazon.com/AWSCloudFormation/latest/APIReference/API_RollbackConfiguration.html) in the *AWS CloudFormation API Reference*\.  |  2010\-05\-15  | 
|  New `umask` parameter for cfn\-hup\.conf file  |  August 31, 2017  |  Use the `umask` parameter in the cfn\-hup\.conf configuration file to control file permissions used by the cfn\-hup daemon \(version 1\.4\-21\)\. For more information, see [cfn\-hup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/cfn-hup.html)\.  |    | 
|  Updated resources for VPC Sizing support  |  August 29, 2017  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html)  |  2010\-05\-15  | 
|  Updated resources  |  August 23, 2017  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html)  |  2010\-05\-15  | 
|  New pseudo parameters  |  August 23, 2017  |  Use the `AWS::Partition` pseudo parameter to return the partition that a resource is in\. Use the `AWS::URLSuffix` pseudo parameter to return the suffix for a domain\. For more information, see [Pseudo Parameters Reference](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/pseudo-parameter-reference.html)\.  |  2010\-05\-15  | 
| New resources for DAX support | August 22, 2017 |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html)  | 2010\-05\-15 | 
|  New resources  |  August 18, 2017  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html)  |  2010\-05\-15  | 
|  Updated resources  |  August 18, 2017  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html) Added the `Arn` attribute to the `Fn::GetAtt` intrinsic function for the following resources: [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html)  |  2010\-05\-15  | 
|  Support for stack tags in CodePipeline artifacts  |  August 18, 2017  |  You can now specify tags for stacks in template configuration files for use as artifacts for CodePipeline pipelines\. Specified tags are applied to stacks created using the template configuration file\. For more information, see [AWS CloudFormation Artifacts](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/continuous-delivery-codepipeline-cfn-artifacts.html)\.  |  2010\-05\-15  | 
|  Create encrypted file systems  |  August 14, 2017  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html)  |  2010\-05\-15  | 
|  New resources for AWS Batch support  |  August 8, 2017  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html)  |  2010\-05\-15  | 
|  New resources for Amazon Kinesis Data Analytics support  |  July 28, 2017  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html)  |  2010\-05\-15  | 
|  Use StackSets to centrally manage stacks across accounts and regions  |  July 25, 2017  |  StackSets enables you to create, update, or delete stacks across multiple accounts and regions in a single operation\. Using an administrator account, you define and manage an AWS CloudFormation template, and use the template as the basis for provisioning stacks into selected target accounts across specified regions\. For more information about StackSets, see [Working with AWS CloudFormation StackSets](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/what-is-cfnstacksets.html)\.  |  2010\-05\-15  | 
|  View stack events by client request token  |  July 14, 2017  |  In the console, stack operations display the client request token on the **Events** tab\. All events triggered by a given stack operation are assigned the same client request token, which you can use to track operations\. For more information, see [Viewing AWS CloudFormation Stack Data and Resources on the AWS Management Console](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/cfn-console-view-stack-data-resources.html) and [StackEvent](https://docs.aws.amazon.com/AWSCloudFormation/latest/APIReference/API_StackEvent.html) in the *AWS CloudFormation API Reference*\.  |  2010\-05\-15  | 
|  Use stack quick\-create links  |  July 14, 2017  |  Use quick\-create links to get stacks up and running quickly\. You can specify the template URL, stack name, and template parameters to prepopulate a single **Create Stack Wizard** page\. For more information, see [Creating Quick\-Create Links for Stacks](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/cfn-console-create-stacks-quick-create-links.html)\.  | 2010\-05\-15 | 
|  New resources for AWS Database Migration Service support  |  July 12, 2017  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html)  |  2010\-05\-15  | 
|  New resources  |  July 5, 2017  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html)  |  2010\-05\-15  | 
|  Updated resources  |  July 5, 2017  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html)  |  2010\-05\-15  | 
|  New resources  |  June 6, 2017  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html)  |  2010\-05\-15  | 
|  Updated resources  |  June 6, 2017  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html)  |  2010\-05\-15  | 
|  New resources  |  May 11, 2017  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html)  |  2010\-05\-15  | 
|  New resources  |  April 28, 2017  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html)  |  2010\-05\-15  | 
|  Updated resources  |  April 28, 2017  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html)  |  2010\-05\-15  | 
|  Edit templates in YAML and JSON using AWS CloudFormation Designer  |  April 6, 2017  |  When you create AWS CloudFormation templates using Designer, you can now edit your template in both YAML and JSON in the integrated editor\. You can also convert JSON templates to YAML and vice\-versa, depending on your preferred template authoring language\. For more information, see [What Is AWS CloudFormation Designer?](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/working-with-templates-cfn-designer.html)\.  |  2010\-05\-15  | 
|  New resource  |  April 6, 2017  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html)  |  2010\-05\-15  | 
|  `AWS::Include` transform  |  March 28, 2017  |  Use the `AWS::Include` transform to reference reusable snippets stored in an Amazon S3 bucket\. For more information, see [AWS::Include Transform](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/create-reusable-transform-function-snippets-and-add-to-your-template-with-aws-include-transform.html)\.  |  2010\-05\-15  | 
|  Peer your Amazon VPC with another account  |  March 28, 2017  |  You can now use AWS CloudFormation to peer your Amazon VPC with a VPC in another AWS account\. For more information, see [Peer with an Amazon VPC in Another AWS Account](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/peer-with-vpc-in-another-account.html)\.  |  2010\-05\-15  | 
|  New resource  |  March 28, 2017  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html)  |  2010\-05\-15  | 
|  Updated resources  |  March 28, 2017  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html)  |  2010\-05\-15  | 
| New resources  | February 10, 2017 |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html)  | 2010\-05\-15 | 
|  New intrinsic function  |  January 17, 2017  |  Use the `Fn::Split` function to split a string into a list of string values\. For more information, see [Fn::Split](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-split.html)\.  |  2010\-05\-15  | 
|  Console support for listing imports  |  January 17, 2017  |  Use the AWS CloudFormation console to see all of the stacks that are importing an exported output value\. For more information, see [Listing Stacks That Import an Exported Output Value](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-stack-imports.html)\.  |  2010\-05\-15  | 
|  Updated resources  |  January 17, 2017  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html)  |  2010\-05\-15  | 
|  New resources  |  December 01, 2016  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html)  |  2010\-05\-15  | 
|  Updated resources for IPv6 support  |  December 01, 2016  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html)  |  2010\-05\-15  | 
|  Resource specification  |  November 22, 2016  |  Use the AWS CloudFormation resource specification to builds tools that help you create AWS CloudFormation templates\. The specification is a machine\-readable, JSON\-formatted text file\. For more information, see [AWS CloudFormation Resource Specification](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/cfn-resource-specification.html)\.  |  2010\-05\-15  | 
|  New resources  |  November 22, 2016  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html)  |  2010\-05\-15  | 
|  Updated resources  |  November 22, 2016  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html)  |  2010\-05\-15  | 
|  List imports  |  November 22, 2016  |  List imports of an exported output value to track which AWS CloudFormation stacks are importing the value\. For more information, see [Listing Stacks That Import an Exported Output Value](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-stack-imports.html)\.  |  2010\-05\-15  | 
|  Transforms  |  November 17, 2016  |   Specify the AWS Serverless Application Model \(AWS SAM\) that AWS CloudFormation uses to process AWS SAM syntax for serverless applications\. For more information, see [Transform](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/transform-section-structure.html)\.  |  2010\-05\-15  | 
|  New resource  |  November 17, 2016  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html)  |  2010\-05\-15  | 
|  Updated resource  |  November 17, 2016  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html)  |  2010\-05\-15  | 
|  New CLI commands  |  November 17, 2016  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html)  |  2010\-05\-15  | 
|  Updated resource  |  November 03, 2016  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html)  |  2010\-05\-15  | 
|  List stack exports  |  November 03, 2016  |  Use the AWS CloudFormation console, API, or AWS CLI to see a list of all the exported output values for a region\. For more information, see [Exporting Stack Output Values](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-stack-exports.html)\.  |  2010\-05\-15  | 
|  Continuous delivery with stacks  |  November 03, 2016  |  Use AWS CodePipeline to build continuous delivery workflows with AWS CloudFormation stacks\. For more information, see [Continuous Delivery with CodePipeline](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/continuous-delivery-codepipeline.html)\.  |  2010\-05\-15  | 
|  Skip resources during rollback  |  November 03, 2016  |  If you have a stack in the `UPDATE_ROLLBACK_FAILED` state, use the `ResourcesToSkip` parameter for the `ContinueUpdateRollback` action to skip resources that AWS CloudFormation can't rollback\. For more information, see the Troubleshooting section in [Update Rollback Failed](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/troubleshooting-errors-update-rollback-failed.html)\.  |  2010\-05\-15  | 
|  Change sets enhancement  |  November 03, 2016  |  You can [create a new stack using a change set](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/cfn-console-create-stacks-changesets.html)\.  |  2010\-05\-15  | 
|  Updated resource  |  October 12, 2016  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html)  |  2010\-05\-15  | 
|  New resources  |  October 06, 2016  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html)  |  2010\-05\-15  | 
|  Updated resources  |  October 06, 2016  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html)  |  2010\-05\-15  | 
|  Cross\-stack reference enhancement  |  October 06, 2016  | Use intrinsic functions to customize the Name value of an [export](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/outputs-section-structure.html) or to refer to a value in the [ImportValue](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-importvalue.html)  function\. |  2010\-05\-15  | 
|  AWS CloudFormation service role  |  September 26, 2016  |  Use an AWS Identity and Access Management \(IAM\) service role for AWS CloudFormation stack operations\. AWS CloudFormation uses the role's credentials to make calls to stack resources on your behalf\. For more information, see [AWS CloudFormation Service Role](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-iam-servicerole.html)\.  |  2010\-05\-15  | 
|  New feature  |  September 19, 2016  |  You can use the `Export` output field and the `Fn::ImportValue` intrinsic function to have one stack refer to resource outputs in another stack\. For more information, see [Outputs](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/outputs-section-structure.html), [Fn::ImportValue](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-importvalue.html), and [Walkthrough: Refer to Resource Outputs in Another AWS CloudFormation Stack](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/walkthrough-crossstackref.html)\.  |  2010\-05\-15  | 
|  YAML support  |  September 19, 2016  |  You can use the YAML format to author AWS CloudFormation templates\. YAML also allows you to, for example, add comments to your templates or use the short form for intrinsic functions\. For more information, see [AWS CloudFormation Template Formats](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/template-formats.html)\.  |  2010\-05\-15  | 
|  New intrinsic function  |  September 19, 2016  |  Use the `Fn::Sub` function to substitute variables in an input string with values that you specify\. For more information, see [Fn::Sub](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-sub.html)\.  |  2010\-05\-15  | 
|  New resources  |  September 19, 2016  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html)  |  | 
|  Updated resources  |  September 19, 2016  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html)  |  2010\-05\-15  | 
|  New resources  |  August 11, 2016  |  Use the following Elastic Load Balancing Application Load Balancer resources to distribute incoming application traffic to multiple targets, such as EC2 instances, in multiple Availability Zones: [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html)  |  2010\-05\-15  | 
|  Updated resource  |  August 11, 2016  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html)  |  2010\-05\-15  | 
|  New resources  |  August 09, 2016  |  AWS CloudFormation added the following resources: [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html)  |  2010\-05\-15  | 
|  Updated resources  |  August 09, 2016  |  AWS CloudFormation updated the following resources: [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html)  |  2010\-05\-15  | 
| New resources |  July 20, 2016  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html)  |  2010\-05\-15  | 
|  Updated resources  |  July 20, 2016  |  AWS CloudFormation updated the following resources: [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html)  |  2010\-05\-15  | 
|  Auto Scaling group UpdatePolicy  |  June 9, 2016  |  For the `UpdatePolicy` attribute, use the `AutoScalingReplacingUpdate` property to specify whether an Auto Scaling group and the instances it contains are replaced when you update the Auto Scaling group\. During a replacement, AWS CloudFormation retains the old Auto Scaling group until it creates the new one successfully so that AWS CloudFormation can roll back to the old Auto Scaling group if the update fails\. For more information, see [UpdatePolicy Attribute](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-attribute-updatepolicy.html)\.  |  2010\-05\-15  | 
|  New resource  |  June 9, 2016  |  AWS CloudFormation added the following resources: [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html)  |  2010\-05\-15  | 
|  Updated resources  |  June 9, 2016  |  AWS CloudFormation updated the following resources: [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html)  |  2010\-05\-15  | 
|  New resource  |  April 25, 2016  |  Use the [AWS::EC2::Host](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-host.html) resource to allocate a fully dedicated physical server for launching EC2 instances\.  |  2010\-05\-15  | 
|  Updated resources  |  April 25, 2016  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html)  |  2010\-05\-15  | 
|  New resources  |  April 18, 2016  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html)  |  2010\-05\-15  | 
|  New resources  |  March 31, 2016  |  Use the [AWS::Lambda::Alias](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-lambda-alias.html) resource to create aliases for your AWS Lambda functions and the [AWS::Lambda::Version](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-lambda-version.html) resource to create versions of your functions\.  |  2010\-05\-15  | 
|  Updated resources  |  March 31, 2016  |  AWS CloudFormation updated the following resources: [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html)  |  2010\-05\-15  | 
|  Change sets  |  March 29, 2016  |  Before updating stacks, use change sets to see how your changes might affect your running resources\. For more information, see [Updating Stacks Using Change Sets](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-changesets.html)\.  |  2010\-05\-15  | 
|  New resources  |  March 15, 2016  |  Use the [AWS::GameLift::Alias](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-gamelift-alias.html), [AWS::GameLift::Build](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-gamelift-build.html), and [AWS::GameLift::Fleet](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-gamelift-fleet.html) resources to deploy multiplayer game servers in AWS\.  |  2010\-05\-15  | 
|  New resources  |  February 26, 2016  |  AWS CloudFormation added the following resources: [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html)  |  2010\-05\-15  | 
|  Updated resources  |  February 26, 2016  |  AWS CloudFormation updated the following resources: [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html)  |  2010\-05\-15  | 
|  Retain resources  |  February 26, 2016  |  For stacks in the `DELETE_FAILED` state, use the `RetainResources` parameter to retain resources that AWS CloudFormation can't delete\. For more information, see [Delete Stack Fails](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/troubleshooting.html#troubleshooting-errors-delete-stack-fails)\.  |  2010\-05\-15  | 
|  Update stack tags  |  February 26, 2016  |  You can add, modify, or remove stack tags when you update a stack\. For more information, see [AWS CloudFormation Stacks Updates](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks.html)\.  |  2010\-05\-15  | 
|  Continue rolling back failed update rollbacks  |  January 25, 2016  |  For a stack in the `UPDATE_ROLLBACK_FAILED` state, you can continue rolling back the update to get your stack in a working state\. That way, you can return the stack to its original settings and try to update it again\. For more information, see [Continue Rolling Back an Update](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-continueupdaterollback.html)\.  |  2010\-05\-15  | 
|  New sample templates available for the Asia Pacific \(Seoul\) region\.  |  January 7, 2016  |  The following collection of AWS CloudFormation sample templates are for the ap\-northeast\-2 region: [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html) For more information, see [Sample Templates](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/cfn-sample-templates.html)\.  |  2010\-05\-15  | 
|  New resources  |  December 28, 2015  |  AWS CloudFormation added the following resources: [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html)  |  2010\-05\-15  | 
|  Resource updates  |  December 28, 2015  |  AWS CloudFormation updated the following resources: [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html)  |  2010\-05\-15  | 
|  Parameter grouping and sorting  |  December 3, 2015  |  Use the [AWS::CloudFormation::Interface](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-cloudformation-interface.html) metadata key to group and sort parameters in the AWS CloudFormation console when users create or update a stack with your template\.  |  2010\-05\-15  | 
|  Update policy attribute  |  December 3, 2015  |  For an Auto Scaling [update policy attribute](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-attribute-updatepolicy.html), use the `MinSuccessfulInstancesPercent` property to specify the percentage of instances that must signal success for a successful update\.  |  2010\-05\-15  | 
|  New resources  |  December 3, 2015  |  AWS CloudFormation added the following resources: [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html)  |  2010\-05\-15  | 
|  Resources update  |  December 3, 2015  |  AWS CloudFormation updated the following resources: [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html)  |  2010\-05\-15  | 
|  Resource update  |  November 4, 2015  |  For the [AWS::EC2::Volume](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ec2-ebs-volume.html) resource, use the `AutoEnableIO` property to automatically resume I/O operations if a volume's data becomes inconsistent\.   |  2010\-05\-15  | 
|  New resources  |  October 1, 2015  |  AWS CloudFormation added the following resources: [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html)  |  2010\-05\-15  | 
|  Resource updates  |  October 1, 2015  |  AWS CloudFormation updated the following resources: [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html)  |  2010\-05\-15  | 
|  IAM condition keys  |  October 1, 2015  |  For AWS Identity and Access Management \(IAM\) policies, use AWS CloudFormation\-specific condition keys to specify when an IAM policy takes effect\. For more information, see [Controlling Access with AWS Identity and Access Management](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-iam-template.html)\.  |  2010\-05\-15  | 
|  AWS CloudFormation Designer  |  October 1, 2015  |  Use [AWS CloudFormation Designer](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/working-with-templates-cfn-designer.html) to create and modify templates using a drag\-and\-drop interface\.  |  2010\-05\-15  | 
|  New resource  |  August 24, 2015  |  Use the [AWS::EC2::VPCEndpoint](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-vpcendpoint.html) resource to establish a private connection between your VPC and another AWS service\.  |  2010\-05\-15  | 
|  Resource updates  |  August 24, 2015  |  AWS CloudFormation updated the following resources: [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html)  |  2010\-05\-15  | 
|  Amazon S3 template URL  |  August 24, 2015  |  For versioning\-enabled buckets, you can specify a version ID in an Amazon S3 template URL when you create or update a stack, such as `https://s3.amazonaws.com/templates/myTemplate.template?versionId=123ab1cdeKdOW5IH4GAcYbEngcpTJTDW`\.  |  2010\-05\-15  | 
|  New resource  |  August 3, 2015  |  Use the [AWS::EFS::FileSystem](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-efs-filesystem.html) resource to create an Amazon Elastic File System \(Amazon EFS\) file system and the [AWS::EFS::MountTarget](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-efs-mounttarget.html) resource to create a mount point for a file system\.  |  2010\-05\-15  | 
|  Permission requirement change  |  June 11, 2015  |  When you create or update an [AWS::RDS::DBInstance](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-rds-database-instance.html) resource, you must now also have permission to call the `ec2:DescribeAccountAttributes` action\.  |  2010\-05\-15  | 
|  New resources  |  June 11, 2015  |  AWS CloudFormation added the following resources: [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html)  |  2010\-05\-15  | 
|  Resource updates  |  June 11, 2015  |  AWS CloudFormation updated the following resources: [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html)  |  2010\-05\-15  | 
|  New parameter types  |  May 19, 2015  |  Whenever you use the AWS CloudFormation console to create or update a stack, you can search for AWS\-specific parameter type values by ID, name, or Name tag value\. AWS CloudFormation also added support for the following AWS\-specific parameter types\. For more information, see [Parameters](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/parameters-section-structure.html)\. [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html)  |  2010\-05\-15  | 
|  New resources  |  April 16, 2015  |  AWS CloudFormation added the following resources: [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html)  |  2010\-05\-15  | 
|  Resource updates  |  April 16, 2015  |  AWS CloudFormation updated the following resources: [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html)  |  2010\-05\-15  | 
|  New template section  |  April 16, 2015  |  Add the [Metadata](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/metadata-section-structure.html) section to your templates to include arbitrary JSON objects that describe your templates, such as the design or implementation details\.  |  2010\-05\-15  | 
|  Resource update  |  April 8, 2015  |  For the [AWS::CloudFormation::CustomResource](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-cfn-customresource.html) resource, you can specify Lambda function Amazon Resource Names \(ARNs\) in the `ServiceToken` property\.  |  2010\-05\-15  | 
|  Amazon RDS update  |  December 24, 2014  |  AWS CloudFormation added two new properties for RDS DB instances\. You can associate an option group with a DB instance and specify the DB instance storage type\. For more information, see [AWS::RDS::DBInstance](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-rds-database-instance.html)\.  |  2010\-05\-15  | 
|  Elastic Load Balancing update  |  December 24, 2014  |  You can use the `ConnectionSettings` property to specify how long connections can remain idle\. For more information, see [AWS::ElasticLoadBalancing::LoadBalancer](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ec2-elb.html)\.  |  2010\-05\-15  | 
|  Route 53 update  |  November 6, 2014  |  You can now provision and manage Route 53 [hosted zones](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-route53-hostedzone.html) , [health checks](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-route53-healthcheck.html), [failover record sets](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-route53-recordset.html) , and [geolocation record sets](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-route53-recordset-geolocation.html) \.  |  2010\-05\-15  | 
|  Auto Scaling rolling update enhancement  |  November 6, 2014  |  During an update, you can use the `WaitOnResourceSignals` flag to instruct AWS CloudFormation to wait for instances to signal success\. That way, AWS CloudFormation won't update the next batch of instances until the current batch is ready\. For more information, see [UpdatePolicy Attribute](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-attribute-updatepolicy.html)\.  |  2010\-05\-15  | 
|  New VPC Fn:GetAtt attributes  |  November 6, 2014  |  Given a VPC ID, you can retrieve the default security group and network ACL for that VPC\. For more information, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.  |  2010\-05\-15  | 
|  New AWS\-specific parameter types  |  November 6, 2014  |  You can specify AWS\-specific parameter types in your AWS CloudFormation templates\. In the AWS CloudFormation console, these parameter types provide a drop\-down list of valid values\. With the API or CLI, AWS CloudFormation can quickly validate values for these parameter types before creating or updating a stack\. For more information, see [Parameters](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/parameters-section-structure.html)\.  |  2010\-05\-15  | 
|  CreationPolicy attribute  |  November 6, 2014  |  With the CreationPolicy attribute, you can instruct AWS CloudFormation to wait until applications are ready on EC2 instances before proceeding with stack creation\. You can use a creation policy instead of a wait condition and wait condition handle\. For more information, see [CreationPolicy Attribute](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-attribute-creationpolicy.html)\.  |  2010\-05\-15  | 
|  Amazon CloudFront forwarded values  |  September 29, 2014  |  For cache behaviors, you can forward headers to the origin\. See [ForwardedValues](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-cloudfront-distribution-forwardedvalues.html)\.  |  2010\-05\-15  | 
|  AWS OpsWorks update  |  September 29, 2014  |  For Chef 11\.10, you can use the `ChefConfiguration` property to enable Berkshelf\. You can also use the AWS OpsWorks built\-in security groups with your AWS OpsWorks stacks\. For more information, see [AWS::OpsWorks::Stack](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-opsworks-stack.html)\.  |  2010\-05\-15  | 
|  Elastic Load Balancing tagging support  |  September 29, 2014  |  AWS CloudFormation tags Elastic Load Balancing load balancers with stack\-level tags\. You can also add your own tags to a load balancer\. See [AWS::ElasticLoadBalancing::LoadBalancer](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ec2-elb.html)\.  |  2010\-05\-15  | 
|  Amazon Simple Notification Service topic policy update  |  September 29, 2014  |  You can now update Amazon SNS topic policies\. For more information, see [AWS::SNS::TopicPolicy](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-sns-policy.html)\.  |  2010\-05\-15  | 
|  RDS DB instance update  |  September 5, 2014  |  You can specify whether a DB instance is Internet\-facing by using the `PubliclyAccessible` property in the [AWS::RDS::DBInstance](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-rds-database-instance.html) resource\.  |  2010\-05\-15  | 
|  UpdatePolicy attribute update  |  September 05, 2014  |  You can specify an update policy for an Auto Scaling group that has an associated scheduled action\. For more information, see [UpdatePolicy Attribute](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-attribute-updatepolicy.html)\.  |  2010\-05\-15  | 
|  Amazon CloudWatch support  |  July 10, 2014  |  You can use AWS CloudFormation to provision and manage Amazon CloudWatch Logs \(CloudWatch Logs\) log groups and metric filters\. For more information, see [AWS::Logs::LogGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-logs-loggroup.html) or [AWS::Logs::MetricFilter](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-logs-metricfilter.html)\.  |  2010\-05\-15  | 
|  Amazon CloudFront distribution configuration update  |  June 17, 2014  |  You can specify additional CloudFront distribution configuration properties: [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html) For more information, see [AWS::CloudFront::Distribution](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-cloudfront-distribution.html)\.  |  2010\-05\-15  | 
|  EC2 instance update  |  June 17, 2014  |  You can specify whether an instance stops or terminates when you invoke the instance's operating system shutdown command\. For more information, see [AWS::EC2::Instance](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ec2-instance.html)\.  |  2010\-05\-15  | 
|  EBS volume update  |  June 17, 2014  |  You can use encrypted EBS volumes with supported instance types\. For more information, see [AWS::EC2::Volume](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ec2-ebs-volume.html)\.  |  2010\-05\-15  | 
|  New Amazon VPC peering connection  |  June 17, 2014  |  You can use AWS CloudFormation to create an Amazon Virtual Private Cloud \(Amazon VPC\) peering connection, which establishes a network connection between two VPCs\. For more information, see [AWS::EC2::VPCPeeringConnection](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-vpcpeeringconnection.html)\.  |  2010\-05\-15  | 
|  Amazon EC2 Auto Scaling group update  |  June 17, 2014  |  You can specify an existing cluster placement group in which to launch instances for an Amazon EC2 Auto Scaling group\. For more information, see [AWS::AutoScaling::AutoScalingGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-as-group.html)\.  |  2010\-05\-15  | 
|  AWS CloudTrail support  |  June 17, 2014  |  AWS CloudFormation supports AWS CloudTrail, which can capture API calls made from your AWS account and publish the logs at a location you designate\. For more information, see [AWS::CloudTrail::Trail](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-cloudtrail-trail.html)\.  |  2010\-05\-15  | 
|  Update stack enhancements  |  May 12, 2014  |  AWS CloudFormation supports additional features for updating stacks: [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html) For more information, see [AWS CloudFormation Stacks Updates](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks.html)\.  |  2010\-05\-15  | 
|  Amazon Kinesis support  |  May 6, 2014  |  You can use AWS CloudFormation to create Amazon Kinesis streams that capture and transport data records from data sources\. For more information, see [AWS::Kinesis::Stream](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-kinesis-stream.html)\.  |  2010\-05\-15  | 
|  New S3 bucket properties  |  May 5, 2014  |  AWS CloudFormation supports additional S3 bucket properties: [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html) For more information, see [AWS::S3::Bucket](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-s3-bucket.html)\.  |  2010\-05\-15  | 
|  Amazon EC2 Auto Scaling support  |  May 5, 2014  |  AWS CloudFormation supports metrics collection for an Auto Scaling group\. For more information, see [AWS::AutoScaling::AutoScalingGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-as-group.html)\.  |  2010\-05\-15  | 
|  `Fn::If` update  |  May 5, 2014  | You can use the Fn::If intrinsic function in the output section of a template\. For more information, see [Condition Functions](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-conditions.html)\. |  2010\-05\-15  | 
|  API logging with AWS CloudTrail  |  April 2, 2014  |   You can use AWS CloudTrail \(CloudTrail\) to log AWS CloudFormation requests\. With CloudTrail you can get a history of AWS CloudFormation API calls for your account\. For more information, see [Logging AWS CloudFormation API Calls with AWS CloudTrail](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/cfn-api-logging-cloudtrail.html)\.   |  2010\-05\-15  | 
|  Elastic Load Balancing update  |  March 20, 2014  |  You can specify an access logging policy to capture information about requests made to your load balancer\. You can also specify a connection draining policy that describes how to handle in\-flight requests when instances are deregistered or become unhealthy\. For more information, see [AWS::ElasticLoadBalancing::LoadBalancer](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ec2-elb.html)\.  |  2010\-05\-15  | 
|  AWS OpsWorks support  |  March 3, 2014  |  You can use AWS CloudFormation to provision and manage AWS OpsWorks stacks\. For more information, see [AWS::OpsWorks::Stack](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-opsworks-stack.html) or [AWS OpsWorks Template Snippets](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/quickref-opsworks.html)\.  |  2010\-05\-15  | 
|  Amazon S3 template size limit increase  |  February 18, 2014  |  You can specify template sizes up to 460,800 bytes in Amazon S3\.  |  2010\-05\-15  | 
|  Amazon Redshift support  |  February 10, 2014  |  You can use AWS CloudFormation to provision and manage Amazon Redshift clusters\. For more information, see [Amazon Redshift Template Snippets](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/quickref-redshift.html) or [AWS::Redshift::Cluster](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-redshift-cluster.html)\.  |  2010\-05\-15  | 
|  S3 buckets and bucket policies update  |  February 10, 2014  |  You can update some properties of the S3 bucket and bucket policy resources\. For more information, see [AWS::S3::Bucket](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-s3-bucket.html) or [AWS::S3::BucketPolicy](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-s3-policy.html)\.  |  2010\-05\-15  | 
|  Elastic Beanstalk environments and application versions update  |  February 10, 2014  |  You can update Elastic Beanstalk environment configurations and application versions\. For more information, see [AWS::ElasticBeanstalk::Environment](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-beanstalk-environment.html), [AWS::ElasticBeanstalk::ConfigurationTemplate](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-beanstalk-configurationtemplate.html), or [AWS::ElasticBeanstalk::ApplicationVersion](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-beanstalk-version.html)\.  |  2010\-05\-15  | 
|  Amazon SQS update  |  January 29, 2014  |  You can specify a dead letter queue for an Amazon SQS queue\. For more information, see [AWS::SQS::Queue](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-sqs-queues.html)\.  |  2010\-05\-15  | 
|  Auto Scaling scheduled actions  |  January 27, 2014  |  You can scale the number of EC2 instances in an Auto Scaling group based on a schedule\. By using a schedule, you can scale applications in response to predictable load changes\. For more information, see [AWS::AutoScaling::ScheduledAction](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-as-scheduledaction.html)\.  |  2010\-05\-15  | 
|  DynamoDB secondary indexes  |  January 27, 2014  |  You can create local and global secondary indexes for DynamoDB databases\. By using secondary indexes, you can efficiently access data with attributes other than the primary key\. For more information, see [AWS::DynamoDB::Table](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-dynamodb-table.html)\.  |  2010\-05\-15  | 
|  Auto Scaling update  |  January 2, 2014  |  You can specify an instance ID for an Auto Scaling group or launch configuration\. You can also specify additional Auto Scaling block device properties\. For more information, see [AWS::AutoScaling::AutoScalingGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-as-group.html) or [AWS::AutoScaling::LaunchConfiguration](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-as-launchconfig.html)\.  |  2010\-05\-15  | 
|  Amazon SQS update  |  January 2, 2014  |  You can update SQS queues and specify additional properties\. For more information, see [AWS::SQS::Queue](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-sqs-queues.html)\.  |  2010\-05\-15  | 
|  Limit increases  |  January 2, 2014  |  You can specify up to 60 parameters and 60 outputs in your AWS CloudFormation templates\.  |  2010\-05\-15  | 
|  New console  |  December 19, 2013  |  The new [AWS CloudFormation console](https://console.aws.amazon.com/cloudformation/) adds features like auto\-refreshing stack events and alphabetical ordering of stack parameters\.  |  2010\-05\-15  | 
|  Cross\-zone load balancing  |  December 19, 2013  |  With cross\-zone load balancing, you can route traffic to back\-end instances across all Availability Zones \(AZs\)\. For more information, see [AWS::ElasticLoadBalancing::LoadBalancer](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ec2-elb.html)\.  |  2010\-05\-15  | 
|  AWS Elastic Beanstalk environment tiers  |  December 19, 2013  |  You can specify whether AWS Elastic Beanstalk provisions resources to support a web server or to handle background processing tasks\. For more information, see [AWS::ElasticBeanstalk::Environment](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-beanstalk-environment.html)\.  |  2010\-05\-15  | 
|  Resource names  |  December 19, 2013  |  You can assign names \(physical IDs\) to the following resources: [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html) For more information, see [Name Type](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-name.html)\.  |  2010\-05\-15  | 
|  VPN support  |  November 22, 2013  |  You can enable a virtual private gateway \(VGW\) to propagate routes to the routing tables of a VPC\. For more information, see [AWS::EC2::VPNGatewayRoutePropagation](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-vpn-gatewayrouteprop.html)\.  |  2010\-05\-15  | 
|  Conditionally create resources and assign properties  |  November 8, 2013  |  Using input parameters, you can control the creation and settings of designated stack resources by defining conditions in your AWS CloudFormation templates\. For example, you can use conditions to create stack resources for a production environment\. Using the same template, you can create similar stack resources with lower capacity for a test environment\. For more information, see [Condition Functions](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-conditions.html)\.  |  2010\-05\-15  | 
|  Prevent accidental updates to stack resources  |  November 8, 2013  |  You can prevent stack updates that might result in unintentional changes to stack resources\. For example, if you have a stack with a database layer that should rarely be updated, you can set a stack policy that prevents most users from updating that database layer\. For more information, see [Prevent Updates to Stack Resources](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/protect-stack-resources.html)\.  |  2010\-05\-15  | 
|  Name resources  |  November 8, 2013  |  Instead of using AWS CloudFormation\-generated physical IDs, you can assign names to certain resources\. The following AWS CloudFormation resources support naming [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html) For more information, see [Name Type](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-name.html)\.  |  2010\-05\-15  | 
|  Assign custom resource types  |  November 8, 2013  |  In your templates, you can specify your own resource type for AWS CloudFormation custom resources \(`AWS::CloudFormation::CustomResource`\)\. By using your own custom resource type name, you can quickly identify the type of custom resources that you have in your stack\. For example, you can specify `"Type": "Custom::MyCustomResource"`\. For more information, see [AWS::CloudFormation::CustomResource](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-cfn-customresource.html)\.  |  2010\-05\-15  | 
|  Add pseudo parameter  |  November 8, 2013  |  You can now refer to the AWS AccountID inside AWS CloudFormation templates by referring to the `AWS::AccountID` pseudo parameter\. For more information, see [Pseudo Parameters Reference](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/pseudo-parameter-reference.html)\.  |  2010\-05\-15  | 
|  Specify stacks in IAM policies  |  November 8, 2013  |  You can allow or deny IAM users, groups, or roles to operate on specific AWS CloudFormation stacks\. For example, you can deny the delete stack action on a specific stack ID\. For more information, see [Controlling Access with AWS Identity and Access Management](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-iam-template.html)\.  |  2010\-05\-15  | 
|  Federation support  |  October 14, 2013  |  AWS CloudFormation supports temporary security credentials from IAM roles, which enable scenarios such as federation and single sign\-on to the AWS Management Console\. You can also make calls to AWS CloudFormation from EC2 instances without embedding long\-term security credentials by using IAM roles\. For more information about AWS CloudFormation and IAM, see [Controlling Access with AWS Identity and Access Management](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-iam-template.html)\.  |  2010\-05\-15  | 
|  Amazon RDS read replica support  |  September 24, 2013  |  You can now create Amazon RDS read replicas from a source DB instance\. For more information, see the `SourceDBInstanceIdentifier `property in the [AWS::RDS::DBInstance](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-rds-database-instance.html) resource\.  |  2010\-05\-15  | 
|  Associate public IP address with instances in an Auto Scaling group  |  September 19, 2013  |   You can now associate public IP addresses with instances in an Auto Scaling group\. For more information, see [AWS::AutoScaling::LaunchConfiguration](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-as-launchconfig.html)\.  |  2010\-05\-15  | 
|  Additional VPC support  |  September 17, 2013  |  AWS CloudFormation adds several enhancements to support VPC and VPN functionality [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html)  |  2010\-05\-15  | 
|  Redis and VPC security groups support for Amazon ElastiCache  |  September 3, 2013  |  You can now specify Redis as the cache engine for an Amazon ElastiCache \(ElastiCache\) cluster\. You can also now assign VPC security groups to ElastiCache clusters\. For more information, see [AWS::ElastiCache::CacheCluster](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-elasticache-cache-cluster.html)\.  |  2010\-05\-15  | 
|  Parallel stack creation, update and deletion, and nested stack updates   |  August 12, 2013  |  AWS CloudFormation now creates, updates, and deletes resources in parallel, improving the operations' performance\. If you update a top\-level template, AWS CloudFormation automatically updates nested stacks that have changed\. For more information, see [AWS CloudFormation Stacks Updates](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks.html)\.  |  2010\-05\-15  | 
|  VPC security groups can now be set in RDS DB instances  |  February 28, 2013  |  You can now assign VPC security groups to an RDS DB instance with AWS CloudFormation\. For more information, see the [VPCSecurityGroups](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/cfn-rds-dbinstance-vpcsecuritygroups.html) property in [AWS::RDS::DBInstance](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-rds-database-instance.html)\.  |  2010\-05\-15  | 
|  Rolling deployments for Amazon EC2 Auto Scaling groups  |  February 20, 2013  |  AWS CloudFormation now supports update policies on Amazon EC2 Auto Scaling groups, which describe how instances in the Amazon EC2 Auto Scaling group are replaced or modified when the Amazon EC2 Auto Scaling group adds or removes instances\. You can modify these settings at stack creation or during a stack update\. For more information and an example, see [UpdatePolicy Attribute](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-attribute-updatepolicy.html)\.  |  2010\-05\-15  | 
|  Cancel and rollback action for stack updates  |  February 20, 2013  |  AWS CloudFormation supports the ability to cancel a stack update\. The stack must be in the UPDATE\_IN\_PROGRESS state when the update request is made\. More information is available in the following topics: [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html)  |  2010\-05\-15  | 
|  EBS\-optimized instances for Amazon EC2 Auto Scaling groups  |  February 20, 2013  |  You can now provision EBS\-optimized instances in Amazon EC2 Auto Scaling groups for dedicated throughput to Amazon Elastic Block Store \(Amazon EBS\) in autoscaled instances\. The implementation is similar to that of the previously released support for optimized Amazon EBS EC2 instances\. For more information, see the new `EbsOptimized` property in [AWS::AutoScaling::LaunchConfiguration](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-as-launchconfig.html)\.  |  2010\-05\-15  | 
|  New documentation  |  December 21, 2012  |  [AWS::EC2::Instance](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ec2-instance.html) now provides a `BlockDeviceMappings` property to allow you to set block device mappings for your EC2 instance\. With this change, two new types have been added: [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html)  |  2010\-05\-15  | 
|  New documentation  |  December 21, 2012  |  New sections have been added to describe the procedures for creating and viewing stacks using the recently redesigned AWS Management Console\. You can find them here: [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html)  |  2010\-05\-15  | 
|  New documentation  |  November 15, 2012  |  Information about custom resources is provided in the following topics: [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html)  |  2010\-05\-15  | 
|  Updated documentation  |  November 15, 2012  |  AWS CloudFormation now supports specifying provisioned I/O operations per second \(IOPS\) for RDS DB instances\. You can set this value from 1000–10,000 in 1000 IOPS increments by using the new [Iops](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/cfn-rds-dbinstance-iops.html) property in [AWS::RDS::DBInstance](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-rds-database-instance.html) \. For more information about specifying IOPS for RDS DB instances, see [Provisioned IOPS](http://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/RDSFAQ.PIOPS.html) in the *Amazon Relational Database Service User Guide*\.  |  2010\-05\-15  | 
|  New and updated documentation  |  August 27, 2012  |  Topics have been reorganized to more clearly provide specific information about using the AWS Management Console and using the AWS CloudFormation command\-line interface \(CLI\)\. Information about tagging AWS CloudFormation stacks has been added, including new guides and updated reference topics: [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html) New information about [working with Windows stacks](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/cfn-windows-stacks.html): [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html) New topic: [Using Regular Expressions in AWS CloudFormation Templates](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/cfn-regexes.html)\.  |  2010\-05\-15  | 
|  New feature  |  April 25, 2012  |  AWS CloudFormation now provides full support for Virtual Private Cloud \(VPC\) security with Amazon EC2 You can now create and populate an entire VPC with every type of VPC resource \(subnets, gateways, network ACLs, route tables, and so forth\) using a single AWS CloudFormation template\. Templates that demonstrate new VPC features can be downloaded: [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html) Documentation for the following resource types has been updated: [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html) New resource types have been added to the documentation: [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html)  |  2010\-05\-15  | 
|  New feature  |  April 13, 2012  |  AWS CloudFormation now allows you to add or remove elements from a stack when updating it\. [AWS CloudFormation Stacks Updates](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks.html) has been updated, and a new section has been added to the walkthrough: [Change the Stack's Resources](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/updating.stacks.walkthrough.html#update.walkthrough.change.resources), which describes how to add and remove resources when updating the stack\.  |  2010\-05\-15  | 
|  New feature  |  February 2, 2012  |  AWS CloudFormation now provides support for resources in an existing Amazon Virtual Private Cloud \(Amazon VPC\)\. With this release, you can: [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html)  |  2010\-05\-15  | 
|  New feature  |  February 2, 2012  |  You can now update properties for the following resources in an existing stack: [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html) For a complete list of updatable resources and details about what to consider when updating a stack, see [AWS CloudFormation Stacks Updates](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks.html)\.  |  2010\-05\-15  | 
|  Restructured guide  |  February 2, 2012  |  Reorganized existing sections into new sections: [Working with AWS CloudFormation Templates](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/template-guide.html) and **Managing Stacks**\. Moved [Template Reference](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/template-reference.html) to the top level of the Table of Contents\. Moved [Estimating the Cost of Your AWS CloudFormation Stack](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-paying.html) to the Getting Started section\.  |  2010\-05\-15  | 
|  New content  |  February 2, 2012  |  Added three new sections: [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html)  |  2010\-05\-15  | 
|  New feature  |  May 26, 2011  |  AWS CloudFormation now provides the aws cloudformation list\-stacks command, which enables you to list stacks filtered by stack status\. Deleted stacks can be listed for up to 90 days after they have been deleted\.  For more information, see [Describing and Listing Your Stacks](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-describing-stacks.html)\.  |  2010\-05\-15  | 
|  New features  |  May 26, 2011  |  The aws cloudformation describe\-stack\-resources and aws cloudformation get\-template commands now enable you to get information from stacks that have been deleted for 90 days after they have been deleted\.  For more information, see [Listing Resources](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-listing-stack-resources.html) and [Retrieving a Template](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-get-template.html)\.  |  2010\-05\-15  | 
|  New link  |  March 1, 2011  |  AWS CloudFormation endpoint information is now located in the AWS General Reference\. For more information, go to Regions and Endpoints in [Amazon Web Services General Reference](http://docs.aws.amazon.com/general/latest/gr/index.html?rande.html)\.  |  2010\-05\-15  | 
|  Initial release  |  February 25, 2011  |  This is the initial public release of AWS CloudFormation\.  |  2010\-05\-15  | 