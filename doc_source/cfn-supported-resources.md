# Supported AWS Services<a name="cfn-supported-resources"></a>

AWS CloudFormation supports the following AWS services and features through the listed resources\.

**Topics**
+ [Analytics](#w3ab2c27c11b7)
+ [Application Services](#w3ab2c27c11b9)
+ [Compute](#w3ab2c27c11c11)
+ [Customer Engagement](#w3ab2c27c11c13)
+ [Database](#w3ab2c27c11c15)
+ [Developer Tools](#w3ab2c27c11c17)
+ [Enterprise Applications](#w3ab2c27c11c19)
+ [Game Development](#w3ab2c27c11c21)
+ [Internet of Things](#w3ab2c27c11c23)
+ [Machine Learning](#w3ab2c27c11c25)
+ [Management Tools](#w3ab2c27c11c27)
+ [Mobile Services](#w3ab2c27c11c29)
+ [Networking](#w3ab2c27c11c31)
+ [Security and Identity](#w3ab2c27c11c33)
+ [Storage and Content Delivery](#w3ab2c27c11c35)
+ [Additional Software and Services](#w3ab2c27c11c37)

## Analytics<a name="w3ab2c27c11b7"></a>

**Amazon Athena** \(Added in September 2017\)  
[AWS::Athena::NamedQuery](aws-resource-athena-namedquery.md)

**Amazon EMR \(Amazon EMR\)** \(Updated in November 2017\)  
 [AWS::EMR::Cluster](aws-resource-emr-cluster.md)  
 [AWS::EMR::InstanceFleetConfig](aws-resource-elasticmapreduce-instancefleetconfig.md)  
 [AWS::EMR::InstanceGroupConfig](aws-resource-emr-instancegroupconfig.md)  
[AWS::EMR::SecurityConfiguration](aws-resource-emr-securityconfiguration.md)  
 [AWS::EMR::Step](aws-resource-emr-step.md)

**AWS Data Pipeline** \(Added in June 2015\)  
 [AWS::DataPipeline::Pipeline](aws-resource-datapipeline-pipeline.md)

**Amazon Elasticsearch Service \(Amazon ES\)** \(Updated in September 2016\)  
 [AWS::Elasticsearch::Domain](aws-resource-elasticsearch-domain.md)

**AWS Glue** \(Added in October 2017\)  
[AWS::Glue::Classifier](aws-resource-glue-classifier.md)  
[AWS::Glue::Connection](aws-resource-glue-connection.md)  
[AWS::Glue::Crawler](aws-resource-glue-crawler.md)  
[AWS::Glue::Database](aws-resource-glue-database.md)  
[AWS::Glue::DevEndpoint](aws-resource-glue-devendpoint.md)  
[AWS::Glue::Job](aws-resource-glue-job.md)  
[AWS::Glue::Trigger](aws-resource-glue-trigger.md)  
[AWS::Glue::Partition](aws-resource-glue-partition.md)  
[AWS::Glue::Table](aws-resource-glue-table.md)

**Amazon Kinesis** \(Updated in November 2017\)  
[AWS::Kinesis::Stream](aws-resource-kinesis-stream.md)  
[AWS::KinesisFirehose::DeliveryStream](aws-resource-kinesisfirehose-deliverystream.md)  
[AWS::KinesisAnalytics::Application](aws-resource-kinesisanalytics-application.md)  
[AWS::KinesisAnalytics::ApplicationOutput](aws-resource-kinesisanalytics-applicationoutput.md)  
[AWS::KinesisAnalytics::ApplicationReferenceDataSource](aws-resource-kinesisanalytics-applicationreferencedatasource.md)

## Application Services<a name="w3ab2c27c11b9"></a>

**Amazon API Gateway \(API Gateway\)** \(Updated in February 2018\)  
[AWS::ApiGateway::Account](aws-resource-apigateway-account.md)  
[AWS::ApiGateway::ApiKey](aws-resource-apigateway-apikey.md)  
[AWS::ApiGateway::Authorizer](aws-resource-apigateway-authorizer.md)  
[AWS::ApiGateway::BasePathMapping](aws-resource-apigateway-basepathmapping.md)  
[AWS::ApiGateway::ClientCertificate](aws-resource-apigateway-clientcertificate.md)  
[AWS::ApiGateway::Deployment](aws-resource-apigateway-deployment.md)  
[AWS::ApiGateway::DocumentationPart](aws-resource-apigateway-documentationpart.md)  
[AWS::ApiGateway::DocumentationVersion](aws-resource-apigateway-documentationversion.md)  
[AWS::ApiGateway::DomainName](aws-resource-apigateway-domainname.md)  
[AWS::ApiGateway::GatewayResponse](aws-resource-apigateway-gatewayresponse.md)  
[AWS::ApiGateway::Method](aws-resource-apigateway-method.md)  
[AWS::ApiGateway::Model](aws-resource-apigateway-model.md)  
[AWS::ApiGateway::RequestValidator](aws-resource-apigateway-requestvalidator.md)  
[AWS::ApiGateway::Resource](aws-resource-apigateway-resource.md)  
[AWS::ApiGateway::RestApi](aws-resource-apigateway-restapi.md)  
[AWS::ApiGateway::Stage](aws-resource-apigateway-stage.md)  
[AWS::ApiGateway::UsagePlan](aws-resource-apigateway-usageplan.md)  
[AWS::ApiGateway::UsagePlanKey](aws-resource-apigateway-usageplankey.md)  
[AWS::ApiGateway::VpcLink](aws-resource-apigateway-vpclink.md)

**Amazon Simple Queue Service \(Amazon SQS\)** \(Updated in August 2017\)  
[AWS::SQS::Queue](aws-properties-sqs-queues.md)  
[AWS::SQS::QueuePolicy](aws-properties-sqs-policy.md)

**AWS Step Functions \(Step Functions\)** \(Updated in February 2017\)  
[AWS::StepFunctions::Activity](aws-resource-stepfunctions-activity.md)  
[AWS::StepFunctions::StateMachine](aws-resource-stepfunctions-statemachine.md)

## Compute<a name="w3ab2c27c11c11"></a>

**Application Auto Scaling** \(Added in July 2017\)  
[AWS::ApplicationAutoScaling::ScalableTarget](aws-resource-applicationautoscaling-scalabletarget.md)  
[AWS::ApplicationAutoScaling::ScalingPolicy](aws-resource-applicationautoscaling-scalingpolicy.md)

**Amazon EC2 Auto Scaling** \(Updated in November 2017\)  
[AWS::AutoScaling::AutoScalingGroup](aws-properties-as-group.md)  
[AWS::AutoScaling::LaunchConfiguration](aws-properties-as-launchconfig.md)  
[AWS::AutoScaling::LifecycleHook](aws-resource-as-lifecyclehook.md)  
[AWS::AutoScaling::ScalingPolicy](aws-properties-as-policy.md)  
[AWS::AutoScaling::ScheduledAction](aws-resource-as-scheduledaction.md)

**Amazon Elastic Compute Cloud \(Amazon EC2\)** \(Updated in March 2018\)  
[AWS::EC2::Host](aws-resource-ec2-host.md)  
[AWS::EC2::Instance](aws-properties-ec2-instance.md)  
[AWS::EC2::LaunchTemplate](aws-resource-ec2-launchtemplate.md)  
[AWS::EC2::PlacementGroup](aws-resource-ec2-placementgroup.md)  
[AWS::EC2::SpotFleet](aws-resource-ec2-spotfleet.md)  
[AWS::EC2::VPCPeeringConnection](aws-resource-ec2-vpcpeeringconnection.md)

**Amazon Elastic Container Registry \(Amazon ECR\)** \(Added in February 2016\)  
[AWS::ECR::Repository](aws-resource-ecr-repository.md)

**Amazon Elastic Container Service \(Amazon ECS\)** \(Updated in April 2017\)  
[AWS::ECS::Cluster](aws-resource-ecs-cluster.md)  
[AWS::ECS::Service](aws-resource-ecs-service.md)  
 [AWS::ECS::TaskDefinition](aws-resource-ecs-taskdefinition.md) 

**Amazon Elastic Container Service for Kubernetes** \(Added in June 2018\)  
[AWS::EKS::Cluster](aws-resource-eks-cluster.md)

**Amazon EC2 Systems Manager \(SSM\)** \(Updated in June 2018\)  
[AWS::SSM::Association](aws-resource-ssm-association.md)  
[AWS::SSM::Document](aws-resource-ssm-document.md)  
[AWS::SSM::MaintenanceWindow](aws-resource-ssm-maintenancewindow.md)  
[AWS::SSM::MaintenanceWindowTarget](aws-resource-ssm-maintenancewindowtarget.md)  
[AWS::SSM::MaintenanceWindowTask](aws-resource-ssm-maintenancewindowtask.md)  
[AWS::SSM::Parameter](aws-resource-ssm-parameter.md)  
[AWS::SSM::PatchBaseline](aws-resource-ssm-patchbaseline.md)  
[AWS::SSM::ResourceDataSync](aws-resource-ssm-resourcedatasync.md)

**AWS Batch **\(Added in August 2017\)  
[AWS::Batch::ComputeEnvironment](aws-resource-batch-computeenvironment.md)  
[AWS::Batch::JobDefinition](aws-resource-batch-jobdefinition.md)  
[AWS::Batch::JobQueue](aws-resource-batch-jobqueue.md)

**AWS Elastic Beanstalk \(Elastic Beanstalk\)** \(Updated in November 2017\)  
[AWS::ElasticBeanstalk::Application](aws-properties-beanstalk.md)  
[AWS::ElasticBeanstalk::ApplicationVersion](aws-properties-beanstalk-version.md)  
[AWS::ElasticBeanstalk::ConfigurationTemplate](aws-resource-beanstalk-configurationtemplate.md)  
[AWS::ElasticBeanstalk::Environment](aws-properties-beanstalk-environment.md)

**Elastic Load Balancing** \(Updated in November 2017\)  
[AWS::ElasticLoadBalancing::LoadBalancer](aws-properties-ec2-elb.md)  
[AWS::ElasticLoadBalancingV2::Listener](aws-resource-elasticloadbalancingv2-listener.md)  
[AWS::ElasticLoadBalancingV2::ListenerCertificate](aws-resource-elasticloadbalancingv2-listenercertificate.md)  
[AWS::ElasticLoadBalancingV2::ListenerRule](aws-resource-elasticloadbalancingv2-listenerrule.md)  
[AWS::ElasticLoadBalancingV2::LoadBalancer](aws-resource-elasticloadbalancingv2-loadbalancer.md)  
[AWS::ElasticLoadBalancingV2::TargetGroup](aws-resource-elasticloadbalancingv2-targetgroup.md)

**AWS Lambda \(Lambda\)** \(Updated in April 2017\)  
[AWS::Lambda::Alias](aws-resource-lambda-alias.md)  
[AWS::Lambda::EventSourceMapping](aws-resource-lambda-eventsourcemapping.md)  
[AWS::Lambda::Function](aws-resource-lambda-function.md)  
[AWS::Lambda::Permission](aws-resource-lambda-permission.md)  
[AWS::Lambda::Version](aws-resource-lambda-version.md)

## Customer Engagement<a name="w3ab2c27c11c13"></a>

**Amazon Simple Email Service \(Amazon SES\)** \(Added in March 2018\)  
[AWS::SES::ConfigurationSet](aws-resource-ses-configurationset.md)  
[AWS::SES::ConfigurationSetEventDestination](aws-resource-ses-configurationseteventdestination.md)  
[AWS::SES::ReceiptFilter](aws-resource-ses-receiptfilter.md)  
[AWS::SES::ReceiptRule](aws-resource-ses-receiptrule.md)  
[AWS::SES::ReceiptRuleSet](aws-resource-ses-receiptruleset.md)  
[AWS::SES::Template](aws-resource-ses-template.md)

## Database<a name="w3ab2c27c11c15"></a>

**Amazon DynamoDB \(DynamoDB\)** \(Updated in August 2017\)  
[AWS::DynamoDB::Table](aws-resource-dynamodb-table.md)

**Amazon DynamoDB Accelerator \(DAX\)** \(Added in August 2017\)  
[AWS::DAX::Cluster](aws-resource-dax-cluster.md)  
[AWS::DAX::ParameterGroup](aws-resource-dax-parametergroup.md)  
[AWS::DAX::SubnetGroup](aws-resource-dax-subnetgroup.md)

**Amazon ElastiCache \(ElastiCache\)** \(Updated in August 2017\)  
[AWS::ElastiCache::CacheCluster](aws-properties-elasticache-cache-cluster.md)  
[AWS::ElastiCache::ParameterGroup](aws-properties-elasticache-parameter-group.md)  
[AWS::ElastiCache::ReplicationGroup](aws-resource-elasticache-replicationgroup.md)  
[AWS::ElastiCache::SecurityGroup](aws-properties-elasticache-security-group.md)  
[AWS::ElastiCache::SecurityGroupIngress](aws-properties-elasticache-security-group-ingress.md)  
[AWS::ElastiCache::SubnetGroup ](aws-properties-elasticache-subnetgroup.md)

**Amazon Neptune \(Neptune\)** \(Added in May 2018\)  
[AWS::Neptune::DBCluster](aws-resource-neptune-dbcluster.md)  
[AWS::Neptune::DBClusterParameterGroup](aws-resource-neptune-dbclusterparametergroup.md)  
[AWS::Neptune::DBInstance](aws-resource-neptune-dbinstance.md)  
[AWS::Neptune::DBParameterGroup](aws-resource-neptune-dbparametergroup.md)  
[AWS::Neptune::DBSubnetGroup](aws-resource-neptune-dbsubnetgroup.md)

**Amazon Relational Database Service \(Amazon RDS\)** \(Updated in October 2017\)  
[AWS::RDS::DBCluster](aws-resource-rds-dbcluster.md)  
[AWS::RDS::DBClusterParameterGroup](aws-resource-rds-dbclusterparametergroup.md)  
[AWS::RDS::DBInstance](aws-properties-rds-database-instance.md)  
[AWS::RDS::DBParameterGroup](aws-properties-rds-dbparametergroup.md)  
[AWS::RDS::DBSecurityGroup](aws-properties-rds-security-group.md)  
[AWS::RDS::DBSecurityGroupIngress](aws-resource-rds-security-group-ingress.md)  
[AWS::RDS::DBSubnetGroup](aws-resource-rds-dbsubnet-group.md)  
[AWS::RDS::EventSubscription](aws-resource-rds-eventsubscription.md)  
[AWS::RDS::OptionGroup](aws-resource-rds-optiongroup.md)

**Amazon Redshift** \(Updated in July 2017\)  
[AWS::Redshift::Cluster](aws-resource-redshift-cluster.md)  
[AWS::Redshift::ClusterParameterGroup](aws-resource-redshift-clusterparametergroup.md)  
[AWS::Redshift::ClusterSecurityGroup](aws-resource-redshift-clustersecuritygroup.md)  
[AWS::Redshift::ClusterSecurityGroupIngress](aws-resource-redshift-clustersecuritygroupingress.md)  
[AWS::Redshift::ClusterSubnetGroup](aws-resource-redshift-clustersubnetgroup.md)

**Amazon SimpleDB** \(Added in February 2011\)  
[AWS::SDB::Domain](aws-properties-simpledb.md)

**AWS Database Migration Service** \(Added in July 2017\)  
[AWS::DMS::Certificate](aws-resource-dms-certificate.md)  
[AWS::DMS::Endpoint](aws-resource-dms-endpoint.md)  
[AWS::DMS::EventSubscription](aws-resource-dms-eventsubscription.md)  
[AWS::DMS::ReplicationInstance](aws-resource-dms-replicationinstance.md)  
[AWS::DMS::ReplicationSubnetGroup](aws-resource-dms-replicationsubnet-group.md)  
[AWS::DMS::ReplicationTask](aws-resource-dms-replicationtask.md)

## Developer Tools<a name="w3ab2c27c11c17"></a>

**AWS Cloud9** \(Added in November 2017\)  
[AWS::Cloud9::EnvironmentEC2](aws-resource-cloud9-environmentec2.md)

**AWS CodeBuild** \(Added in December 2016\)  
[AWS::CodeBuild::Project](aws-resource-codebuild-project.md)

**AWS CodeCommit** \(Added in October 2016\)  
[AWS::CodeCommit::Repository](aws-resource-codecommit-repository.md)

**AWS CodeDeploy** \(Updated in November 2017\)  
[AWS::CodeDeploy::Application](aws-resource-codedeploy-application.md)  
[AWS::CodeDeploy::DeploymentConfig](aws-resource-codedeploy-deploymentconfig.md)  
[AWS::CodeDeploy::DeploymentGroup](aws-resource-codedeploy-deploymentgroup.md)

**AWS CodePipeline** \(Added in December 2015\)  
[AWS::CodePipeline::CustomActionType](aws-resource-codepipeline-customactiontype.md)  
[AWS::CodePipeline::Pipeline](aws-resource-codepipeline-pipeline.md)

## Enterprise Applications<a name="w3ab2c27c11c19"></a>

**Amazon WorkSpaces** \(Updated in December 2015\)  
[AWS::WorkSpaces::Workspace](aws-resource-workspaces-workspace.md)

## Game Development<a name="w3ab2c27c11c21"></a>

**Amazon GameLift \(GameLift\)** \(Updated in April 2016\)  
[AWS::GameLift::Alias](aws-resource-gamelift-alias.md)  
[AWS::GameLift::Build](aws-resource-gamelift-build.md)  
[AWS::GameLift::Fleet](aws-resource-gamelift-fleet.md)

## Internet of Things<a name="w3ab2c27c11c23"></a>

**AWS IoT** \(Updated in August 2017\)  
[AWS::IoT::Certificate](aws-resource-iot-certificate.md)  
[AWS::IoT::Policy](aws-resource-iot-policy.md)  
[AWS::IoT::PolicyPrincipalAttachment](aws-resource-iot-policyprincipalattachment.md)  
[AWS::IoT::Thing](aws-resource-iot-thing.md)  
[AWS::IoT::ThingPrincipalAttachment](aws-resource-iot-thingprincipalattachment.md)  
[AWS::IoT::TopicRule](aws-resource-iot-topicrule.md)

## Machine Learning<a name="w3ab2c27c11c25"></a>

**Amazon SageMaker ** \(Added in May 2018\)  
[AWS::SageMaker::Endpoint](aws-resource-sagemaker-endpoint.md)  
[AWS::SageMaker::EndpointConfig](aws-resource-sagemaker-endpointconfig.md)  
[AWS::SageMaker::Model](aws-resource-sagemaker-model.md)  
[AWS::SageMaker::NotebookInstance](aws-resource-sagemaker-notebookinstance.md)  
[AWS::SageMaker::NotebookInstanceLifecycleConfig](aws-resource-sagemaker-notebookinstancelifecycleconfig.md)

## Management Tools<a name="w3ab2c27c11c27"></a>

**AWS Auto Scaling ** \(Added in May 2018\)  
[AWS::AutoScalingPlans::ScalingPlan](aws-resource-autoscalingplans-scalingplan.md)

**AWS CloudFormation \(AWS CloudFormation\)** \(Updated in April 2015\)  
[AWS::CloudFormation::Authentication](aws-resource-authentication.md)  
[AWS::CloudFormation::CustomResource](aws-resource-cfn-customresource.md)  
[AWS::CloudFormation::Init](aws-resource-init.md)  
[AWS::CloudFormation::Stack](aws-properties-stack.md)  
[AWS::CloudFormation::WaitCondition](aws-properties-waitcondition.md)  
[AWS::CloudFormation::WaitConditionHandle](aws-properties-waitconditionhandle.md)

**AWS CloudTrail \(CloudTrail\)** \(Updated in August 2017\)  
[AWS::CloudTrail::Trail](aws-resource-cloudtrail-trail.md)

**Amazon CloudWatch \(CloudWatch\)** \(Updated in September 2017\)  
[AWS::CloudWatch::Alarm](aws-properties-cw-alarm.md)  
[AWS::CloudWatch::Dashboard](aws-properties-cw-dashboard.md)  
[AWS::Events::Rule](aws-resource-events-rule.md)  
[AWS::Logs::Destination](aws-resource-logs-destination.md)  
[AWS::Logs::LogGroup](aws-resource-logs-loggroup.md)  
[AWS::Logs::LogStream](aws-resource-logs-logstream.md)  
[AWS::Logs::MetricFilter](aws-resource-logs-metricfilter.md)  
[AWS::Logs::SubscriptionFilter](aws-resource-logs-subscriptionfilter.md)

**AWS Config** \(Updated in April 2018\)  
[AWS::Config::AggregationAuthorization](aws-resource-config-aggregationauthorization.md)  
[AWS::Config::ConfigRule](aws-resource-config-configrule.md)  
[AWS::Config::ConfigurationAggregator](aws-resource-config-configurationaggregator.md)  
[AWS::Config::ConfigurationRecorder](aws-resource-config-configurationrecorder.md)  
[AWS::Config::DeliveryChannel](aws-resource-config-deliverychannel.md)

**AWS OpsWorks** \(Updated in November 2017\)  
[AWS::OpsWorks::App](aws-resource-opsworks-app.md)  
[AWS::OpsWorks::ElasticLoadBalancerAttachment](aws-resource-opsworks-elbattachment.md)  
[AWS::OpsWorks::Instance](aws-resource-opsworks-instance.md)  
[AWS::OpsWorks::Layer](aws-resource-opsworks-layer.md)  
[AWS::OpsWorks::Stack](aws-resource-opsworks-stack.md)  
[AWS::OpsWorks::UserProfile](aws-resource-opsworks-userprofile.md)  
[AWS::OpsWorks::Volume](aws-resource-opsworks-volume.md)

**AWS Service Catalog** \(Updated in May 2018\)  
[AWS::ServiceCatalog::AcceptedPortfolioShare](aws-resource-servicecatalog-acceptedportfolioshare.md)  
[AWS::ServiceCatalog::CloudFormationProduct](aws-resource-servicecatalog-cloudformationproduct.md)  
[AWS::ServiceCatalog::CloudFormationProvisionedProduct](aws-resource-servicecatalog-cloudformationprovisionedproduct.md)  
[AWS::ServiceCatalog::LaunchNotificationConstraint](aws-resource-servicecatalog-launchnotificationconstraint.md)  
[AWS::ServiceCatalog::LaunchRoleConstraint](aws-resource-servicecatalog-launchroleconstraint.md)  
[AWS::ServiceCatalog::LaunchTemplateConstraint](aws-resource-servicecatalog-launchtemplateconstraint.md)  
[AWS::ServiceCatalog::Portfolio](aws-resource-servicecatalog-portfolio.md)  
[AWS::ServiceCatalog::PortfolioPrincipalAssociation](aws-resource-servicecatalog-portfolioprincipalassociation.md)  
[AWS::ServiceCatalog::PortfolioProductAssociation](aws-resource-servicecatalog-portfolioproductassociation.md)  
[AWS::ServiceCatalog::PortfolioShare](aws-resource-servicecatalog-portfolioshare.md)  
[AWS::ServiceCatalog::TagOption](aws-resource-servicecatalog-tagoption.md)  
[AWS::ServiceCatalog::TagOptionAssociation](aws-resource-servicecatalog-tagoptionassociation.md)

**AWS Systems Manager** \(Updated in May 2018\)  
[AWS::SSM::Association](aws-resource-ssm-association.md)  
[AWS::SSM::Document](aws-resource-ssm-document.md)  
[AWS::SSM::MaintenanceWindow](aws-resource-ssm-maintenancewindow.md)  
[AWS::SSM::MaintenanceWindowTarget](aws-resource-ssm-maintenancewindowtarget.md)  
[AWS::SSM::MaintenanceWindowTask](aws-resource-ssm-maintenancewindowtask.md)  
[AWS::SSM::Parameter](aws-resource-ssm-parameter.md)  
[AWS::SSM::PatchBaseline](aws-resource-ssm-patchbaseline.md)  
[AWS::SSM::ResourceDataSync](aws-resource-ssm-resourcedatasync.md)

## Mobile Services<a name="w3ab2c27c11c29"></a>

**AWS AppSync** \(Added in April 2018\)  
[AWS::AppSync::ApiKey](aws-resource-appsync-apikey.md)  
[AWS::AppSync::DataSource](aws-resource-appsync-datasource.md)  
[AWS::AppSync::GraphQLApi](aws-resource-appsync-graphqlapi.md)  
[AWS::AppSync::GraphQLSchema](aws-resource-appsync-graphqlschema.md)  
[AWS::AppSync::Resolver](aws-resource-appsync-resolver.md)

**Amazon Cognito** \(Added in April 2017\)  
[AWS::Cognito::IdentityPool](aws-resource-cognito-identitypool.md)  
[AWS::Cognito::IdentityPoolRoleAttachment](aws-resource-cognito-identitypoolroleattachment.md)  
[AWS::Cognito::UserPool](aws-resource-cognito-userpool.md)  
[AWS::Cognito::UserPoolClient](aws-resource-cognito-userpoolclient.md)  
[AWS::Cognito::UserPoolGroup](aws-resource-cognito-userpoolgroup.md)  
[AWS::Cognito::UserPoolUser](aws-resource-cognito-userpooluser.md)  
[AWS::Cognito::UserPoolUserToGroupAttachment](aws-resource-cognito-userpoolusertogroupattachment.md)

**Amazon Simple Notification Service \(Amazon SNS\)** \(Updated in November 2016\)  
[AWS::SNS::Subscription](aws-resource-sns-subscription.md)  
[AWS::SNS::Topic](aws-properties-sns-topic.md)  
[AWS::SNS::TopicPolicy](aws-properties-sns-policy.md)

## Networking<a name="w3ab2c27c11c31"></a>

**Amazon Route 53** \(Updated in March 2017\)  
[AWS::Route53::HealthCheck](aws-resource-route53-healthcheck.md)  
[AWS::Route53::HostedZone](aws-resource-route53-hostedzone.md)  
[AWS::Route53::RecordSet](aws-properties-route53-recordset.md)  
[AWS::Route53::RecordSetGroup](aws-properties-route53-recordsetgroup.md)

**Service Discovery** \(Added in December 2017\)  
[AWS::ServiceDiscovery::Instance](aws-resource-servicediscovery-instance.md)  
[AWS::ServiceDiscovery::PrivateDnsNamespace](aws-resource-servicediscovery-privatednsnamespace.md)  
[AWS::ServiceDiscovery::PublicDnsNamespace](aws-resource-servicediscovery-publicdnsnamespace.md)  
[AWS::ServiceDiscovery::Service](aws-resource-servicediscovery-service.md)

**Amazon Virtual Private Cloud \(Amazon VPC\)** \(Updated in November 2017\)  
[AWS::EC2::CustomerGateway](aws-resource-ec2-customer-gateway.md)  
[AWS::EC2::DHCPOptions](aws-resource-ec2-dhcp-options.md)  
[AWS::EC2::EgressOnlyInternetGateway](aws-resource-ec2-egressonlyinternetgateway.md)  
[AWS::EC2::EIP](aws-properties-ec2-eip.md)  
[AWS::EC2::EIPAssociation](aws-properties-ec2-eip-association.md)  
[AWS::EC2::FlowLog](aws-resource-ec2-flowlog.md)  
[AWS::EC2::InternetGateway](aws-resource-ec2-internetgateway.md)  
[AWS::EC2::NatGateway](aws-resource-ec2-natgateway.md)  
[AWS::EC2::NetworkAcl](aws-resource-ec2-network-acl.md)  
[AWS::EC2::NetworkAclEntry](aws-resource-ec2-network-acl-entry.md)  
[AWS::EC2::NetworkInterface](aws-resource-ec2-network-interface.md)  
[AWS::EC2::NetworkInterfaceAttachment](aws-resource-ec2-network-interface-attachment.md)  
[AWS::EC2::NetworkInterfacePermission](aws-resource-ec2-networkinterfacepermission.md)  
[AWS::EC2::Route](aws-resource-ec2-route.md)  
[AWS::EC2::RouteTable](aws-resource-ec2-route-table.md)  
[AWS::EC2::SecurityGroup](aws-properties-ec2-security-group.md)  
[AWS::EC2::SecurityGroupEgress](aws-resource-ec2-security-group-egress.md)  
[AWS::EC2::SecurityGroupIngress](aws-properties-ec2-security-group-ingress.md)  
[AWS::EC2::Subnet](aws-resource-ec2-subnet.md)  
[AWS::EC2::SubnetCidrBlock](aws-resource-ec2-subnetcidrblock.md)  
[AWS::EC2::SubnetNetworkAclAssociation](aws-resource-ec2-subnet-network-acl-assoc.md)  
[AWS::EC2::SubnetRouteTableAssociation](aws-resource-ec2-subnet-route-table-assoc.md)  
[AWS::EC2::VPC](aws-resource-ec2-vpc.md)  
[AWS::EC2::VPCCidrBlock](aws-resource-ec2-vpccidrblock.md)  
[AWS::EC2::VPCDHCPOptionsAssociation](aws-resource-ec2-vpc-dhcp-options-assoc.md)  
[AWS::EC2::VPCEndpoint](aws-resource-ec2-vpcendpoint.md)  
[AWS::EC2::VPCGatewayAttachment](aws-resource-ec2-vpc-gateway-attachment.md)  
[AWS::EC2::VPCPeeringConnection](aws-resource-ec2-vpcpeeringconnection.md)  
[AWS::EC2::VPNConnection](aws-resource-ec2-vpn-connection.md)  
[AWS::EC2::VPNConnectionRoute](aws-resource-ec2-vpn-connection-route.md)  
[AWS::EC2::VPNGateway](aws-resource-ec2-vpn-gateway.md)  
[AWS::EC2::VPNGatewayRoutePropagation](aws-resource-ec2-vpn-gatewayrouteprop.md)

## Security and Identity<a name="w3ab2c27c11c33"></a>

**AWS Certificate Manager \(ACM\)** \(Added in August 2016\)  
[AWS::CertificateManager::Certificate](aws-resource-certificatemanager-certificate.md)

**AWS Directory Service** \(Updated in December 2015\)  
[AWS::DirectoryService::MicrosoftAD](aws-resource-directoryservice-microsoftad.md)  
[AWS::DirectoryService::SimpleAD](aws-resource-directoryservice-simplead.md)

**Amazon Inspector** \(Added in December 2017\)  
[AWS::Inspector::AssessmentTarget](aws-resource-inspector-assessmenttarget.md)  
[AWS::Inspector::AssessmentTemplate](aws-resource-inspector-assessmenttemplate.md)  
[AWS::Inspector::ResourceGroup](aws-resource-inspector-resourcegroup.md)

**Amazon GuardDuty** \(Updated in May 2018\)  
[AWS::GuardDuty::Detector](aws-resource-guardduty-detector.md)  
[AWS::GuardDuty::Filter](aws-resource-guardduty-filter.md)  
[AWS::GuardDuty::IPSet](aws-resource-guardduty-ipset.md)  
[AWS::GuardDuty::Master](aws-resource-guardduty-master.md)  
[AWS::GuardDuty::Member](aws-resource-guardduty-member.md)  
[AWS::GuardDuty::ThreatIntelSet](aws-resource-guardduty-threatintelset.md)

**AWS Identity and Access Management \(IAM\)** \(Updated in April 2017\)  
[AWS::IAM::AccessKey](aws-properties-iam-accesskey.md)  
[AWS::IAM::Group](aws-properties-iam-group.md)  
[AWS::IAM::InstanceProfile](aws-resource-iam-instanceprofile.md)  
[AWS::IAM::ManagedPolicy](aws-resource-iam-managedpolicy.md)  
[AWS::IAM::Policy](aws-resource-iam-policy.md)  
[AWS::IAM::Role](aws-resource-iam-role.md)  
[AWS::IAM::User](aws-properties-iam-user.md)  
[AWS::IAM::UserToGroupAddition](aws-properties-iam-addusertogroup.md)

**AWS Key Management Service \(AWS KMS\)** \(Updated in October 2017\)  
[AWS::KMS::Alias](aws-resource-kms-alias.md)  
[AWS::KMS::Key](aws-resource-kms-key.md)

**AWS WAF** \(Updated in May 2017\)  
[AWS::WAF::ByteMatchSet](aws-resource-waf-bytematchset.md)  
[AWS::WAF::IPSet](aws-resource-waf-ipset.md)  
[AWS::WAF::Rule](aws-resource-waf-rule.md)  
[AWS::WAF::SizeConstraintSet](aws-resource-waf-sizeconstraintset.md)  
[AWS::WAF::SqlInjectionMatchSet](aws-resource-waf-sqlinjectionmatchset.md)  
[AWS::WAF::WebACL](aws-resource-waf-webacl.md)  
[AWS::WAF::XssMatchSet](aws-resource-waf-xssmatchset.md)  
[AWS::WAFRegional::ByteMatchSet](aws-resource-wafregional-bytematchset.md)  
[AWS::WAFRegional::IPSet](aws-resource-wafregional-ipset.md)  
[AWS::WAFRegional::Rule](aws-resource-wafregional-rule.md)  
[AWS::WAFRegional::SizeConstraintSet](aws-resource-wafregional-sizeconstraintset.md)  
[AWS::WAFRegional::SqlInjectionMatchSet](aws-resource-wafregional-sqlinjectionmatchset.md)  
[AWS::WAFRegional::WebACL](aws-resource-wafregional-webacl.md)  
[AWS::WAFRegional::WebACLAssociation](aws-resource-wafregional-webaclassociation.md)  
[AWS::WAFRegional::XssMatchSet](aws-resource-wafregional-xssmatchset.md)

## Storage and Content Delivery<a name="w3ab2c27c11c35"></a>

**Amazon CloudFront \(CloudFront\)** \(Updated in November 2017\)  
[AWS::CloudFront::CloudFrontOriginAccessIdentity](aws-resource-cloudfront-cloudfrontoriginaccessidentity.md)  
[AWS::CloudFront::Distribution](aws-resource-cloudfront-distribution.md)  
[AWS::CloudFront::StreamingDistribution](aws-resource-cloudfront-streamingdistribution.md)

**Amazon Elastic Block Store \(Amazon EBS\)** \(Updated in April 2017\)  
 [AWS::EC2::Volume](aws-properties-ec2-ebs-volume.md)   
[AWS::EC2::VolumeAttachment](aws-properties-ec2-ebs-volumeattachment.md)

**Amazon Elastic File System \(Amazon EFS\)** \(Updated in August 2017\)  
[AWS::EFS::FileSystem](aws-resource-efs-filesystem.md)  
[AWS::EFS::MountTarget](aws-resource-efs-mounttarget.md)

**Amazon Simple Storage Service \(Amazon S3\)** \(Updated in November 2017\)  
[AWS::S3::Bucket](aws-properties-s3-bucket.md)  
[AWS::S3::BucketPolicy](aws-properties-s3-policy.md)

## Additional Software and Services<a name="w3ab2c27c11c37"></a>

**AWS Billing and Cost Management \(Billing and Cost Management\)** \(Added in May 2018\)  
[AWS::Budgets::Budget](aws-resource-budgets-budget.md)