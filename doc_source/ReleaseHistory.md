# Release History<a name="ReleaseHistory"></a>

The following table describes important changes in each release of the AWS CloudFormation User Guide after May 2018\. For notification about updates to this documentation, you can subscribe to an RSS feed\.

| Change | Description | Date | 
| --- |--- |--- |
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
Use the `VolumeSizeInGB` property to specify the size in GB of the persisted machine learning storage volume that is provisioned and attached to the Amazon SageMaker notebook instance\.  | February 28, 2019 | 
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
| [Stack instance operation limit](#ReleaseHistory) | For StackSets, you can have a maximum of 1500 stack instance operations running in a given region at the same time, per administrator account\.For more information, see [Limitations of StackSets](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/stacksets-limitations.html)\. | December 13, 2018 | 
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

 [AWS::CertificateManager::Certificate](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-certificatemanager-certificate.html)>   
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

## Earlier Updates<a name="release-history-earlier-updates"></a>

The following table describes important changes in each release of the AWS CloudFormation User Guide before May 2018\.


| Change | Release Date | Description | API Version | 
| --- | --- | --- | --- | 
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
|  Changed default `umask` value from version 1\.4\-22 onwards  |  September 14, 2017  |  The default `umask` parameter value for the cfn\-hup\.conf configuration file is now `022`\. For more information, see [cfn\-hup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/cfn-hup.html) \.  |   | 
| Updated resources | September 7, 2017 |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html)  | 2010\-05\-15 | 
|  Rollback triggers added to the AWS CloudFormation API  |  August 31, 2017  |  Rollback triggers enable you to have AWS CloudFormation monitor the state of your application during stack creation and updating, and to roll back that operation if the application breaches the threshold of any of the alarms you've specified\. For more information, see [ RollbackConfiguration](https://docs.aws.amazon.com/AWSCloudFormation/latest/APIReference/API_RollbackConfiguration.html) in the *AWS CloudFormation API Reference*\.  |  2010\-05\-15  | 
|  New `umask` parameter for cfn\-hup\.conf file  |  August 31, 2017  |  Use the `umask` parameter in the cfn\-hup\.conf configuration file to control file permissions used by the cfn\-hup daemon \(version 1\.4\-21\)\. For more information, see [cfn\-hup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/cfn-hup.html)\.  |   | 
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
|  Update stack enhancements  |  May 12, 2014  |  AWS CloudFormation supports additional features for updating stacks: [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html) For more information, see [AWS CloudFormation Stacks Updates](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks.html)>\.  |  2010\-05\-15  | 
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
|  New and updated documentation  |  August 27, 2012  |  Topics have been reorganized to more clearly provide specific information about using the AWS Management Console and using the AWS CloudFormation command\-line interface \(CLI\)\. Information about tagging AWS CloudFormation stacks has been added, including new guides and updated reference topics: [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html) New information about [working with Windows stacks](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/cfn-windows-stacks.html)>: [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html) New topic: [Using Regular Expressions in AWS CloudFormation Templates](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/cfn-regexes.html) />\.  |  2010\-05\-15  | 
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