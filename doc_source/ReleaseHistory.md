# Release history<a name="ReleaseHistory"></a>

The following table describes important changes in each release of the AWS CloudFormation User Guide after May 2018\. For notification about updates to this documentation, you can subscribe to an [RSS feed](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-cloudformation-release-notes.rss)\.

| Change | Description | Date | 
| --- |--- |--- |
| [Updated resource](AWS_Lambda.md) | The following resource was updated: AWS::Lambda::EventSourceMapping\. 

 [AWS::Lambda::EventSourceMapping](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-lambda-eventsourcemapping.html)   
 Use the `DocumentDBEventSourceConfig` property to define specific configuration settings for a DocumentDB event source, such as the database name\.   | March 2, 2023 | 
| [Updated resource](AWS_WAFv2.md) | The following resource was updated: AWS::WAFv2::WebACL\. 

 [AWS::WAFv2::WebACL](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-wafv2-webacl.html)   
Use the `AWSManagedRulesATPRuleSet` property to configure your use of the Fraud Control account takeover prevention \(ATP\) managed rule group in a managed rule group reference statement\. For protected CloudFront distributions, in addition to inspecting login requests, you can now use ATP to block new login attempts from clients that have recently submitted too many failed login attempts\.  | March 2, 2023 | 
| [New resources](AWS_IVSChat.md) | The following resources were added: AWS::IVSChat::Room and AWS::IVSChat::LoggingConfiguration 

 [AWS::IVSChat::Room](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ivschat-room.html)   
Use the `AWS::IVSChat::Room` resource to specify and Amazon IVS Chat Room\. 

 [AWS::IVSChat::LoggingConfiguration](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ivschat-loggingconfiguration.html)   
Use the `AWS::IVSChat::LoggingConfiguration` resource to specify and Amazon IVS Chat Logging Configuration, which stores configuration information related to loggin your chat session to a data store\.  | March 2, 2023 | 
| [New resource](AWS_SystemsManagerSAP.md) | The following resource was released: [https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-systemsmanagersap-application.html](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-systemsmanagersap-application.html)\.Use `AWS::SystemsManagerSAP::Application` to register an SAP application with AWS Systems Manager for SAP\. | March 2, 2023 | 
| [New resource](AWS_NetworkManager.md) | A new resource was added to Network Manager: AWS::NetworkManager::TransitGatewayRouteTableAttachment 

 [ AWS::NetworkManager::TransitGatewayRouteTableAttachment\.](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-networkmanager-transitgatewayroutetableattachment.html)   
Use `AWS::NetworkManager::TransitGatewayRouteTableAttachment` to create a transit gateway route table attachment\.  | February 23, 2023 | 
| [Updated resource](AWS_FMS.md) | The following resource was updated: AWS::FMS::Policy\. 

 [AWS::FMS::Policy](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-fms-policy.html)   
Use the `PolicyDescription` property to establish default actions to take on a packet that doesn't match any stateful rules when using strict rule ordering\.   
Use the `ResourceSetIds` property to configure the resources to include in a resource set\.   | February 17, 2023 | 
| [New resource](AWS_FMS.md) | The following resource was added: AWS::FMS::ResourceSet\. 

 [AWS::FMS::ResourceSet](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-fms-resourceset.html)   
Use the `AWS::FMS::ResourceSet` resource to import resources into your firewall policy from another AWS service\.  | February 17, 2023 | 
| [New resource](AWS_Organizations.md) | The following resource was added: `AWS::Organizations::ResourcePolicy.` 

 [AWS::Organizations::ResourcePolicy](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-organizations-resourcepolicy.html)   
Use the `AWS::Organizations::ResourcePolicy` resource to create or update a resource\-based delegation policy that delegates policy management for AWS Organizations to specified member accounts to perform policy actions that are by default available only to the organization management account\.  | February 16, 2023 | 
| [Updated resource](AWS_DataSync.md) | The following resource was updated: AWS::DataSync::LocationObjectStorage\. 

[AWS::DataSync::LocationObjectStorage](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-datasync-locationobjectstorage.html)  
Use the `ServerCertificate` property to specify a certificate for authenticating with an object storage system that uses a private or self\-signed certificate authority \(CA\)\.  | February 9, 2023 | 
| [Updated resource](AWS_SageMaker.md) | The following resource was added: AWS::SageMaker::Space\. 

 [AWS::SageMaker::Space](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-sagemaker-space.html)   
Use the `AWS::SageMaker::Space` resource to create a new shared space for use in a Domain\.  | February 9, 2023 | 
| [Updated resource](AWS_SNS.md) | The following resource was updated: AWS::SNS::Topic\. 

 [AWS::SNS::Topic](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-sns-topic.html)   
Use the `TracingConfig` property vend X\-Ray segment data to a topic owner account\. Only supported on standard topics\.  | February 8, 2023 | 
| [New resources](AWS_Omics.md) | The following resources were added: AWS::Omics::Workflow, AWS::Omics::RunGroup, AWS::Omics::AnnotationStore, AWS::Omics::ReferenceStore, AWS::Omics::VariantStore, and AWS::Omics::SequenceStore\. 

 [WS::Omics::Workflow](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-omics-workflow.html)   
Use the `AWS::Omics::Workflow` resource to specify a workflow in Amazon Omics\. 

 [AWS::Omics::RunGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-omics-rungroup.html)   
Use the `AWS::Omics::RunGroup` resource to specify a run group in Amazon Omics\. 

 [AWS::Omics::ReferenceStore](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-omics-referencestore.html)   
Use the `AWS::Omics::ReferenceStore` resource to specify a reference store in Amazon Omics\. 

 [AWS::Omics::RunGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-omics-sequencestore.html)   
Use the `AWS::Omics::SequenceStore` resource to specify a sequence store in Amazon Omics\. 

 [AWS::Omics::ReferenceStore](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-omics-referencestore.html)   
Use the `AWS::Omics::ReferenceStore` resource to specify a reference store in Amazon Omics\. 

 [AWS::Omics::RunGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-omics-sequencestore.html)   
Use the `AWS::Omics::SequenceStore` resource to specify a sequence store in Amazon Omics\.  | February 3, 2023 | 
| [Updated resource](AWS_AppSync.md) | The following resources were updated: AWS::AppSync::DataSource 

 [AWS::AppSync::DataSource](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-appsync-datasource.html#cfn-appsync-datasource-eventbridgeconfig)   
Use the `EventBridgeConfig` property to add custom events to your Amazon EventBridge bus\.   | February 2, 2023 | 
| [Updated resource](AWS_DataSync.md) | The following resource was updated: AWS::DataSync::LocationS3\. 

[AWS::DataSync::LocationS3](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-datasync-locations3.html)  
Use the `S3StorageClass` property to specify the S3 Glacier Instant Retrieval storage class \(`GLACIER_INSTANT_RETRIEVAL`\) for data transferred to your S3 bucket\.  | February 2, 2023 | 
| [Updated resource](AWS_RDS.md) | The following resource was updated: AWS::RDS::DBInstance 

 [AWS::RDS::DBInstance](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-rds-dbinstance.html)   
Use `CertificateDetails` property for the details of the DB instance's server certificate\.  | February 2, 2023 | 
| [Updated resource](AWS_SageMaker.md) | The following resource was added: AWS::SageMaker::ModelCard\. 

 [AWS::SageMaker::ModelCard](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-sagemaker-modelcard.html)   
Use the `AWS::SageMaker::ModelCard` resource to create an Amazon SageMaker Model Card\.  | February 2, 2023 | 
| [New resources](AWS_CloudTrail.md) | The following new resources were added: AWS::CloudTrail::Channel and AWS::CloudTrail::ResourcePolicy 

 [AWS::CloudTrail::Channel](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-cloudtrail-channel.html)   
Use the `Channel` resource to specify a channel for logging events from outside AWS in CloudTrail Lake\. Channels are used by partner event sources, or your custom event sources, to send events to CloudTrail Lake\. For more information, see [Working with CloudTrail Lake](https://docs.aws.amazon.com/awscloudtrail/latest/userguide/cloudtrail-lake.html) in the *AWS CloudTrail User Guide*\. 

 [AWS::CloudTrail::Channel\.Channel](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-cloudtrail-channel-channel.html)   
Use the `Channel` property to specify the name and ARN of a channel that you use with integrations in CloudTrail Lake\. For more information, see [Working with CloudTrail Lake](https://docs.aws.amazon.com/awscloudtrail/latest/userguide/cloudtrail-lake.html) in the *AWS CloudTrail User Guide*\. 

 [AWS::CloudTrail::Channel\.Destination](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-cloudtrail-channel-destination.html)   
Use the `Destination` property to specify destination event data stores for events that arrive over a channel in CloudTrail Lake\. For more information, see [Working with CloudTrail Lake](https://docs.aws.amazon.com/awscloudtrail/latest/userguide/cloudtrail-lake.html) in the *AWS CloudTrail User Guide*\. 

 [AWS::CloudTrail::ResourcePolicy](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-cloudtrail-resourcepolicy.html)   
Use the `ResourcePolicy` resource to attach a resource\-based permission policy to a CloudTrail channel that is used for an integration with an event source outside of AWS\. For more information about resource\-based policies, see [CloudTrail resource\-based policy examples](https://docs.aws.amazon.com/awscloudtrail/latest/userguide/security_iam_resource-based-policy-examples.html) in the *CloudTrail User Guide*\. 

 [AWS::CloudTrail::ResourcePolicy\.ResourceArn](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-cloudtrail-resourcepolicy-resourcearn.html)   
Use the `ResourceArn` property to specify the Amazon Resource Name \(ARN\) of the CloudTrail channel attached to the resource\-based policy\. The following is the format of a resource ARN: `arn:aws:cloudtrail:us-east-2:123456789012:channel/MyChannel`\. 

 [AWS::CloudTrail::ResourcePolicy\.ResourcePolicy](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-cloudtrail-resourcepolicy-resourcepolicy.html)   
Use the `ResourcePolicy` property to specify the JSON\-formatted string that contains the resource\-based policy to attach to the CloudTrail channel\.  | February 2, 2023 | 
| [New resource](AWS_Connect.md) | The following resource was added: AWS::Connect::IntegrationAssociation 

 [AWS::Connect::IntegrationAssociation](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-connect-integrationassociation.html)   
Use the `AWS::Connect::IntegrationAssociation` resource to associate Lex bots \(both v1 and v2\) and Lambda functions with an instance\.  | February 2, 2023 | 
| [New resource](AWS_Connect.md) | The following resource was added: AWS::Connect::ApprovedOrigin 

 [AWS::Connect::ApprovedOrigin](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-connect-approvedorigin.html)   
Use the `AWS::Connect::ApprovedOrigin` resource to associate Approved Origin with an instance\.  | February 2, 2023 | 
| [New resource](AWS_Connect.md) | The following resource was added: AWS::Connect::SecurityKey 

 [AWS::Connect::SecurityKey](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-connect-securitykey.html)   
Use the `AWS::Connect::SecurityKey` resource to associate Security Key with an instance\.  | February 2, 2023 | 
| [New resource](AWS_SimSpaceWeaver.md) | The following resource was added: AWS::SimSpaceWeaver::Simulation\. 

 [AWS::SimSpaceWeaver::Simulation](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-simspaceweaver-simulation.html)   
Use the `AWS::SimSpaceWeaver::Simulation` resource to specify a simulation in the AWS Cloud, in your AWS account\.  | February 2, 2023 | 
| [Updated resource](AWS_Lambda.md) | The following resource was updated: AWS::Lambda::Function\. 

 [AWS::Lambda::Function](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-lambda-function.html)   
 Use the `RuntimeManagementConfig` to define how your function gets runtime version updates\. Lambda releases new runtime versions that include security updates, bug fixes, and new features\. You can now control when your functions get updated to the new runtime versions\.   | January 26, 2023 | 
| [Updated resource](AWS_OpenSearchService.md) | The following resource was updated: AWS::OpenSearchService::Domain\. 

 [AWS::OpenSearchService::Domain](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-opensearchservice-domain.html)   
Use the `SAMLOptions` property within `AdvancedSecurityOptions` to configure SAML authentication for the domain\.  | January 26, 2023 | 
| [New resource](AWS_NetworkManager.md) | A new resource was added to Network Manager: AWS::NetworkManager::TransitGatewayPeering 

 [ AWS::NetworkManager::TransitGatewayPeering\.](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-networkmanager-transitgatewaypeering.html)   
Use `AWS::NetworkManager::TransitGatewayPeering` to create a transit gateway peering\.  | January 26, 2023 | 
| [Updated resource](AWS_KendraRanking.md) | The following resource was updated: AWS::KendraRanking::ExecutionPlan 

 [AWS::KendraRanking::ExecutionPlan](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-kendraranking-executionplan.html)   
Create a rescore execution plan, which is an Amazon Kendra Intelligent Ranking resource used for provisioning the `Rescore` API\. Amazon Kendra Intelligent Ranking rescores or re\-ranks a search service's results using semantic search\.  | January 20, 2023 | 
| [Updated resource](AWS_CloudWatch.md) | The following resource was updated: AWS::CloudWatch::MetricStream\. 

 [AWS::CloudWatch::MetricStream](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-metricstream.html)   
In the [MetricStream](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-cloudwatch-alarm-metricstream.html) resource, use `IncludeLinkedAccountsMetrics` to specify whether the metric stream should metric streams from source accounts, if the metric stream is created in a monitoring account\.  | January 19, 2023 | 
| [Updated resource](AWS_Lambda.md) | The following resource was updated: AWS::Lambda::EventSourceMapping\. 

 [AWS::Lambda::EventSourceMapping](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-lambda-eventsourcemapping.html)   
 Use the `ScalingConfig` property to specify a scaling configuration for an Amazon SQS event source\.   | January 19, 2023 | 
| [Updated resource](AWS_AuditManager.md) | The following resource was updated: AWS::AuditManager::Assessment 

 [AWS::AuditManager::Assessment](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-auditmanager-assessment.html)   
Use the `Delegations` property to specify a delegation for an assessment\.  | January 12, 2023 | 
| [Updated resource](AWS_RDS.md) | The following resource was updated: AWS::RDS::DBCluster 

 [AWS::RDS::DBCluster](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-rds-dbcluster.html)   
The `ManageMasterUserPassword` property indicates whether to manage the master user password with AWS Secrets Manager\.  
The `MasterUserSecret` property 4has the secret managed by RDS in AWS Secrets Manager for the master user password\.  | January 12, 2023 | 
| [Updated resource](AWS_RDS.md) | The following resource was updated: AWS::RDS::DBInstance 

 [AWS::RDS::DBInstance](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-rds-dbinstance.html)   
The `ManageMasterUserPassword` property indicates whether to manage the master user password with AWS Secrets Manager\.  
The `MasterUserSecret` property 4has the secret managed by RDS in AWS Secrets Manager for the master user password\.  | January 12, 2023 | 
| [Updated resource](AWS_CloudFront.md) | The following resource was updated: AWS::CloudFront::ResponseHeadersPolicy\. 

 [AWS::CloudFront::ResponseHeadersPolicy](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-cloudfront-responseheaderspolicy.html)   
In the [ResponseHeadersPolicyConfig](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-cloudfront-responseheaderspolicy-responseheaderspolicyconfig.html) use the `RemoveHeadersConfig` to specify a list of headers that CloudFront removes from HTTP responses that it sends to viewers\.  
For more information, see [Adding or removing response headers](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/modifying-response-headers.html) in the *Amazon CloudFront Developer Guide*\.  | January 5, 2023 | 
| [Updated resource](AWS_MWAA.md) | The following resource was updated: AWS::MWAA::Environment 

 [AirflowVersion](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-mwaa-environment.html#cfn-mwaa-environment-airflowversion)   
The `AirflowVersion` property has been updated to include a new valid value for Apache Airflow version 2\.4\.3\.  | January 5, 2023 | 
| [Updated resource](AWS_AppRunner.md) | The following resource was updated: AWS::AppRunner::Service 

 [AWS::AppRunner::Service\.ImageConfiguration\.RuntimeEnvironmentSecrets](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-apprunner-service.html#cfn-apprunner-service-imageconfiguration-runtimeenvironmentsecrets)   
New property\. To add runtime environment variables as secrets in Image Configuration in App Runner service\.  | December 30, 2022 | 
| [Updated resource](AWS_AppRunner.md) | The following resource was updated: AWS::AppRunner::Service 

 [AWS::AppRunner::Service\.CodeConfigurationValues\.RuntimeEnvironmentSecrets](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-apprunner-service.html#cfn-apprunner-service-codeconfigurationvalues-runtimeenvironmentsecrets)   
New property\. To add runtime environment variables as secrets in Code Configuration values in App Runner service\.  | December 30, 2022 | 
| [Updated resource](AWS_Lex.md) | The following property type was updated: AWS::Lex::Bot\. 

[AWS::Lex::Bot](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-lex-bot.html)  
Use the [ AllowedInputTypes](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-lex-bot-allowedinputtypes) property to specify the allowed input types\.  
Use the [ AudioSpecification](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-lex-bot-audiospecification) property to specify the audio input specifications\.  
Use the [ AudioAndDTMFInputSpecification](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-lex-bot-audioanddtmfinputspecification) property to specify the audio and DTMF input specification\.  
Use the [Condition](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-lex-bot-condition) property to provide an expression that evaluates to true or false\.  
Use the [ ConditionalBranch](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-lex-bot-conditionalbranch) property to configure a set of actions that Amazon Lex should run if the condition is matched\.  
Use the [ ConditionalSpecification](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-lex-bot-conditionalspecification) property to provide a list of conditional branches\.  
Use the [ DefaultConditionalBranch](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-lex-bot-defaultconditionalbranch) property to configure a set of actions that Amazon Lex should run if none of the other conditions are met\.  
Use the [ DialogAction](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-lex-bot-dialogaction) property to define the action that the bot executes at runtime\.  
Use the [ DialogCodeHookInvocationSetting](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-lex-bot-dialogcodehookinvocationsetting) property to specify the dialog code hook that is called by Amazon Lex at a step of the conversation\.  
Use the [ DialogState](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-lex-bot-dialogstate) property to configure the current state of the conversation with the user\.  
Use the [ DTMFSpecification](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-lex-bot-dtmfspecification) property to specify the DTMF input specifications\.  
Use the [ ElicitationCodeHookInvocationSetting](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-lex-bot-elicitationcodehookinvocationsetting) property to specify the dialog code hook that is called by Amazon Lex between eliciting slot values\.  
Use the [ InitialResponseSetting](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-lex-bot-initialresponsesetting) property to configure settings for a response sent to the user before Amazon Lex starts eliciting slots\.  
Use the [ Intent](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-lex-bot-intent) property to configure how Amazon Lex handles intents\.  
Use the [ IntentClosingSetting](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-lex-bot-intentclosingsetting) property to configure the statement that Amazon Lex conveys to the user when the intent is successfully fulfilled\.  
Use the [ IntentConfirmationSetting](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-lex-bot-intentconfirmationsetting.html) property to provide a prompt for making sure that the user is ready for the intent to be fulfilled\.  
Use the [ IntentOverride](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-lex-bot-intentoverride) property to override settings to configure the intent state\.  
Use the [ PostDialogCodeHookInvocationSpecification](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-lex-bot-postdialogcodehookinvocationspecification) property to specify next steps to run after the dialog code hook finishes\.  
Use the [ PostFulfillmentStatusSpecification](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-lex-bot-postfulfillmentstatusspecification) property to configure the settings of the post\-fulfillment response that is sent to the user\.  
Use the [ PromptAttemptSpecification](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-lex-bot-promptattemptspecification) property to specify the settings on a prompt attempt\.  
Use the [ PromptSpecification](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-lex-bot-promptspecification.html) property to specify a list of message groups that Amazon Lex sends to a user to elicit a response\.  
Use the [ SessionAttribute](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-lex-bot-sessionattribute) property to specify session\-specific context information\.  
Use the [ SlotCaptureSetting](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-lex-bot-slotcapturesetting) property to configure the settings that are used when Amazon Lex successfully captures a slot value from a user\.  
Use the [ SlotValue](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-lex-bot-slotvalue) property to set values in a slot\.  
Use the [ SlotValueElicitationSetting](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-lex-bot-slotvalueelicitationsetting) property to specify the settings for eliciting a slot value\.  
Use the [ SlotValueOverride](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-lex-bot-slotvalueoverride) property to set slot values in a dialog step\.  
Use the [ SlotValueOverrideMap](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-lex-bot-slotvalueoverridemap) property to map slot names to a SlotValueOVerride object\.  
Use the [ TextInputSpecification](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-lex-bot-textinputspecification) property to specify the text input specifications\.  
Use the [ VoiceSettings](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-lex-bot-voicesettings) property to specify the Amazon Polly voice used for audio interaction with the user\.  | December 30, 2022 | 
| [Updated resource](AWS_FSx.md) | The following resource was updated: AWS::FSx::Filesystem 

[AWS::FSx::Filesystem](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-fsx-filesystem.html)  
The `AWS::FSx::FileSystem` resource returns a file system's Amazon Resource Name \(ARN\)\.  | December 29, 2022 | 
| [Updated resource](AWS_FSx.md) | The following resource was updated: AWS::FSx::Volume 

[AWS::FSx::Volume](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-fsx-volume.html)  
Use the `CopyTagsToBackups` `AWS::FSx::Volume OntapConfiguration` property to specify whether an ONTAP volume's tags get copied to backups\.  | December 29, 2022 | 
| [Updated resource](AWS_FSx.md) | The following resource was updated: AWS::FSx::Volume 

[AWS::FSx::Volume](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-fsx-volume.html)  
Use the `OntapVolumeType` `AWS::FSx::Volume OntapConfiguration` property to specify the type of ONTAP volume to create\.  | December 29, 2022 | 
| [Updated resource](AWS_FSx.md) | The following resource was updated: AWS::FSx::Volume 

[AWS::FSx::Volume](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-fsx-volume.html)  
Use the `SnapshotPolicy` `AWS::FSx::Volume OntapConfiguration` property to specify the snapshot policy for the volume you are creating\.  | December 29, 2022 | 
| [Updated resources](AWS_NetworkFirewall.md) | The following resources were updated: AWS::NetworkFirewall::FirewallPolicy and AWS::NetworkFirewall::RuleGroup 

 [AWS::NetworkFirewall::FirewallPolicy](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-networkfirewall-firewallpolicy.html)   
Use the `StatefulDefaultActions` property to establish default actions to take on a packet that doesn't match any stateful rules when using strict rule ordering\.   
Use the `StatefulEngineOptions` property to govern how Network Firewall handles stateful rules\.  

 [AWS::NetworkFirewall::RuleGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-networkfirewall-rulegroup.html)   
The `StatefulRuleGroupReference` property now includes `Priority` and `StatefulRuleGroupOverride` fields\.  
Use the `StatefulRuleOptions` property to govern how Network Firewall handles stateful rules\.   
Use the `ReferenceSets` property to configure IP set references for your stateful rules\.   | December 22, 2022 | 
| [Updated resource](AWS_Grafana.md) | The following resource was updated: `AWS::Grafana::Workspace`\. 

 [AWS::Grafana::Workspace](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-grafana-workspace.html)   
Use the `vpcConfiguration` property of the `AWS::Grafana::Workspace` resource to configure a connection to a private VPC from your Amazon Managed Grafana workspace\.  | December 22, 2022 | 
| [Updated resource](AWS_RDS.md) | The following resource was updated: AWS::RDS::DBInstance 

 [AWS::RDS::DBInstance](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-rds-dbinstance.html)   
The `Endpoint` property specifies the connection endpoint\.  
The `DBSystemId` return value is the Oracle system ID \(Oracle SID\) for a container database \(CDB\)\.  | December 22, 2022 | 
| [Updated resource](AWS_SageMaker.md) | The following resource was added: AWS::SageMaker::Project\. 

 [AWS::SageMaker::FeatureGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-sagemaker-featuregroup.html)   
Use the `AWS::SageMaker::FeatureGroup` resource to create a new feature group using either an Apache Iceberg or Glue table format\.  | December 22, 2022 | 
| [Updated resources](AWS_M2.md) | The following resources were updated: AWS::M2::Application and AWS::M2::Environment\. 

 [AWS::M2::Application](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-m2-application.html)   
Use the `KmsKeyId` property to specify a customer managed key\. 

 [AWS::M2::Environment](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-m2-environment.html)   
Use the `KmsKeyId` property to specify a customer managed key\.  | December 15, 2022 | 
| [Updated resources](AWS_RefactorSpaces.md) | The following resources were updated: AWS::RefactorSpaces::Application, AWS::RefactorSpaces::Environment, AWS::RefactorSpaces::Route, AWS::RefactorSpaces::Service\. 

 [AWS::RefactorSpaces::Application](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-refactorspaces-application.html)   
The `EnvironmentIdentifier` property was changed to `Required: Yes`\.  
The `Name` property was changed to `Required: Yes`\.  
The `ProxyType` property was changed to `Required: Yes`\.  
The `VpcId` property was changed to `Required: Yes`\. 

 [AWS::RefactorSpaces::Environment](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-refactorspaces-environment.html)   
The `Name` property was changed to `Required: Yes`\.  
The `NetworkFabricType` property was changed to `Required: Yes`\. 

 [AWS::RefactorSpaces::Route](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-refactorspaces-route.html)   
The `RouteType` property was changed to `Required: Yes`\.  
In the [DefaultRouteInput](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-refactorspaces-route-defaultrouteinput.html) property type, the `ActivationState` property was changed to `Required: No`\.  
In the [UriPathRouteInput](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-refactorspaces-route-uripathrouteinput.html) property type, the `SourcePath` property was changed to `Required: Yes`\. 

 [AWS::RefactorSpaces::Service](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-refactorspaces-service.html)   
The `Name` property was changed to `Required: Yes`\.  
In the [LambdaEndpointInput](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-refactorspaces-service-lambdaendpointinput.html) property type, the `Arn` property description was updated\.  | December 15, 2022 | 
| [Updated resource](AWS_SSMIncidents.md) | The following resource was updated: AWS::SSMIncidents::AWS::SSMIncidents::ReplicationSet 

 [AWS::SSMIncidents::ReplicationSet](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ssmincidents-replicationset.html)   
Use the `Tags` resource to add a list of tags to the replication set\.  | December 15, 2022 | 
| [Updated resource](AWS_RDS.md) | The following resource was updated: AWS::RDS::DBInstance 

 [AWS::RDS::DBInstance](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-rds-dbinstance.html)   
Use the `DBClusterSnapshotIdentifier` property as the identifier for the RDS for MySQL Multi\-AZ DB cluster snapshot to restore from\.  
Use the `RestoreTime` property to specify the date and time to restore from\.  
Use the `SourceDbiResourceId` property to specify the resource ID of the source DB instance from which to restore\.  
Use the `SourceDBInstanceAutomatedBackupsArn` property to specify the Amazon Resource Name \(ARN\) of the replicated automated backups from which to restore\.  
Use the `UseLatestRestorableTime` property to specify a value that indicates whether the DB instance is restored from the latest backup time\.  | December 15, 2022 | 
| [Updated resource](AWS_RDS.md) | The following resource was updated: AWS::RDS::DBCluster 

 [AWS::RDS::DBCluster](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-rds-dbcluster.html)   
Use the `SecondsBeforeTimeout` value in `ScalingConfiguration` property syntax to define the amount of time \(seconds\) that Aurora Serverless v1 tries to find a scaling point to perform seamless scaling before enforcing the timeout action\.  
The `DBSystemId` property is reserved for future use\.  | December 15, 2022 | 
| [New resource](AWS_DocDBElastic.md) | The following resources were added: AWS::DocDBElastic::Cluster\. 

 [AWS::DocDBElastic::Cluster](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-docdbelastic-cluster.html)   
Use the `AWS::DocDBElastic::Cluster` resource to create an elastic cluster in the Amazon DocumentDB database service\.  | December 15, 2022 | 
| [New resources](AWS_NetworkManager.md) | A property was added to `VpcOptions` in Network Manager: AWS::NetworkManager::VpcAttachment VpcOptions 

 [ AWS::NetworkManager::VpcAttachment VpcOptions](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ec2-transitgatewayvpcattachment-options.html#cfn-ec2-transitgatewayvpcattachment-options-appliancemodesupport)   
You can enable or disable appliance mode for VPC attachments in `VpcOptions` by using the `ApplianceModeSupport` Boolean\.  | December 14, 2022 | 
| [New resource](AWS_Connect.md) | The following resource was added: AWS::Connect::Rule 

 [AWS::Connect::Rule](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-connect-rule.html)   
Use the `AWS::Connect::Rule` resource to create an instance\.  | December 12, 2022 | 
| [Updated resources](AWS_WAFv2.md) | The following resources were updated: AWS::WAFv2::WebACL and AWS::WAFv2::RuleGroup\. 

 [AWS::WAFv2::WebACL](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-wafv2-webacl.html)   
Use the `ChallengeConfig` property to configure request evaluations for rules that use the `Challenge` action\.   
Use the `TokenDomains` property to specify additional domains to accept in web request tokens\.   
Use the `RuleActionOverride` property in rule group reference statements to override individual rule actions to any valid action\. This replaces the `ExcludedRule` property, which only allows override to `Count`\.  
Use the `AWSManagedRulesBotControlRuleSet` property to configure your use of the Bot Control managed rule group in a managed rule group reference statement\.  

 [AWS::WAFv2::RuleGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-wafv2-rulegroup.html)   
Use the `ChallengeConfig` property to configure request evaluations for rules that use the `Challenge` action\.  | December 8, 2022 | 
| [New resources](AWS_Grafana.md) | The following resources were added: `AWS::Grafana::Workspace`\. 

 [AWS::Grafana::Workspace](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-grafana-workspace.html)   
Use the `AWS::Grafana::Workspace` resource to create an Amazon Managed Grafana workspace in your AWS account\. An Amazon Managed Grafana workspace allows you to view and monitor metrics and alerts for your system\.  | December 8, 2022 | 
| [New resource](AWS_OpenSearchServerless.md) | The following resources were added: AWS::OpenSearchServerless::AccessPolicy, AWS::OpenSearchServerless::Collection, AWS::OpenSearchServerless::SecurityConfig, AWS::OpenSearchServerless::SecurityPolicy, AWS::OpenSearchServerless::VpcEndpoint\. 

 [AWS::OpenSearchServerless::AccessPolicy](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-opensearchserverless-accesspolicy.html)   
Use the `AWS::OpenSearchServerless::AccessPolicy` resource to create data access policies for Amazon OpenSearch Serverless\. 

 [AWS::OpenSearchServerless::Collection](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-opensearchserverless-collection.html)   
Use the `AWS::OpenSearchServerless::Collection` resource to create collections in Amazon OpenSearch Serverless\. 

 [AWS::OpenSearchServerless::SecurityConfig](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-opensearchserverless-securityconfig.html)   
Use the `AWS::OpenSearchServerless::SecurityConfig` resource to specify SAML providers for Amazon OpenSearch Serverless\. 

 [AWS::OpenSearchServerless::SecurityPolicy](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-opensearchserverless-securitypolicy.html)   
Use the `AWS::OpenSearchServerless::SecurityPolicy` resource to specify network and encryption policies for Amazon OpenSearch Serverless\. 

 [AWS::OpenSearchServerless::VpcEndpoint](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-opensearchserverless-vpcendpoint.html)   
Use the `AWS::OpenSearchServerless::VpcEndpoint` resource to specify Amazon OpenSearch Serverless\-managed VPC endpoints\.  | December 8, 2022 | 
| [New resources ](AWS_IoTTwinMaker.md) | The following resource was added: AWS::IoTTwinMaker::SyncJob\. 

 [ AWS::IoTTwinMaker::SyncJob](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-iottwinmaker-syncjob.html)   
Use the `AWS::IoTTwinMaker::SyncJob` respurce to create a new sync job request\.  | December 6, 2022 | 
| [Updated resources](AWS_ECS.md) | The following resources were updated: AWS::ECS::TaskDefinition\. 

 [AWS::ECS::TaskDefinition PortMappings](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ecs-taskdefinition-portmappings.html)   
Use the `Name` property to specify the port mapping name\.  
Use the `AppProtocol` property to specify the port mapping's application protocol\.  | December 2, 2022 | 
| [Updated resource](AWS_Logs.md) | The following resource was updated: AWS::Logs::LogGroup\. 

 [AWS::Logs::LogGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-logs-loggroup.html)   
The AWS::Logs::LogGroup resource now supports the `DataProtectionPolicy` parameter, to support the masking of sensitive data in log events in the log group\. For more information, see [Protect sensitive log data with masking](https://docs.aws.amazon.com/AmazonCloudWatch/latest/logs/mask-sensitive-log-data.html)\.  | December 2, 2022 | 
| [Updated resource](AWS_SSMIncidents.md) | The following resource was updated: AWS::SSMIncidents::ResponsePlan 

 [AWS::SSMIncidents::ResponsePlan](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ssmincidents-responseplan.html)   
Use the `Integration` resource to specify information about third\-party services integrated into the response plan, such as PagerDuty\.  
Use the `PagerDuty` resource to provide details about the PagerDuty configuration for a response plan\.  | December 2, 2022 | 
| [Updated resource](AWS_Lambda.md) | The following resource was updated: AWS::Lambda::Function\. 

 [AWS::Lambda::Function](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-lambda-function.html)   
 Use the `SnapStart` property to specify the function's AWS Lambda SnapStart setting\. SnapStart creates a snapshot of the initialized execution environment when you publish a function version\.   | December 2, 2022 | 
| [New resources](AWS_ECS.md) | The following resources were added: AWS::ECS::Cluster ServiceConnectDefaults, AWS::ECS::Service ServiceConnectClientAlias, and AWS::ECS::Service ServiceConnectConfiguration\. 

 [AWS::ECS::Cluster ServiceConnectDefaults](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ecs-cluster-serviceconnectdefaults.html)  
Use the `AWS::ECS::Cluster ServiceConnectDefaults` resource to specify a default Service Connect namespace for new services in the cluster\. 

 [AWS::ECS::Service ServiceConnectClientAlias](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ecs-service-serviceconnectclientalias.html)  
Use the `AWS::ECS::Service ServiceConnectClientAlias` resource to specify an endpoint in the Service Connect configuration for the service\. 

 [AWS::ECS::Service ServiceConnectConfiguration](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ecs-taskdefinition-serviceconnectconfiguration.html)  
Use the `AWS::ECS::Service ServiceConnectConfiguration` resource to specify the Service Connect configuration for the service\.  | December 2, 2022 | 
| [New resources](AWS_Pipes.md) | The following resources were added: AWS::Pipes::Pipe\. 

 [AWS::Pipes::Pipe](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-pipes-pipe.html)   
Use the `AWS::Pipes::Pipe` resource to specify a new Amazon EventBridge Pipes pipe\.  | December 2, 2022 | 
| [New resource](AWS_EC2.md) | The following resource was added: AWS::EC2::NetworkPerformanceMetricSubscription\. 

 [ AWS::EC2::NetworkPerformanceMetricSubscription](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-networkperformancemetricsubscription.html)   
Returns a list of Infrastructure Performance subscriptions for AWS CloudWatch\.  | December 2, 2022 | 
| [New resource](AWS_IoT.md) | The following resource was added: AWS::IoT::TopicRule RepublishActionHeaders\. 

 [AWS::IoT::TopicRule RepublishActionHeaders](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-iot-topicrule-republishactionheaders.html)   
Use AWS::IoT::TopicRule RepublishActionHeaders to specify MQTT Version 5\.0 headers information\.  | December 2, 2022 | 
| [Updated resource](AWS_S3.md) | The following resource was updated: AWS::S3::AccessPoint\. 

 [AWS::S3::AccessPoint](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-s3-accesspoint.html)   
Use `AWS::S3::AccessPoint BucketAccountId` to specify which AWS account is associated with the S3 bucket associated with an access point\.  | November 30, 2022 | 
| [Updated resources ](AWS_IoTTwinMaker.md) | The following properties were added: AWS::IoTTwinMaker::ComponentType\.PropertyGroups, and Entity\.PropertyGroup\. 

 [ AWS::IoTTwinMaker::ComponentType\.PropertyGroups](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-iottwinmaker-componenttype-propertygroups.html)   
Use the `AWS::IoTTwinMaker::ComponentType.PropertyGroups` property to declare a ComponentType propertyGroup\. 

 [ Entity\.PropertyGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-iottwinmaker-entity-propertygroup.html.html)   
Use the `AWS::IoTTwinMaker::Entity.PropertyGroup` to declare an entity PropertyGroup\.  | November 17, 2022 | 
| [Updated resources](AWS_Amplify.md) | The following resources were updated: AWS::Amplify::App and AWS::Amplify::Branch 

 [AWS::Amplify::App](https://docs.aws.amazon.com/AWSCloudFormation/latest/userguide/aws-resource-amplify-app.html)   
Use the `Platform` property to specify the platform type for the Amplify app\. 

 [AWS::Amplify::Branch](https://docs.aws.amazon.com/AWSCloudFormation/latest/userguide/aws-resource-amplify-branch.html)   
Use the `Framework` property to specify the framework for the Amplify app\.  | November 17, 2022 | 
| [Updated resource](AWS_AppSync.md) | The following resources were updated: AWS::AppSync::Resolver and AWS::AppSync::FunctionConfiguration 

 [AWS::AppSync::Resolver](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-appsync-resolver.html#cfn-appsync-resolver-code)   
Use the `Code` property to specify the request and response functions\. 

 [AWS::AppSync::Resolver](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-appsync-resolver.html#cfn-appsync-resolver-runtime)   
Use the `Runtime` property to specify the runtime type to be used with a pipeline resolver or function 

 [AWS::AppSync::Resolver](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-appsync-resolver-appsyncruntime.html)   
Use the `AppSyncRuntime` to specify the name and version of your runtime property\. 

 [AWS::AppSync::FunctionConfiguration](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-appsync-functionconfiguration.html#cfn-appsync-functionconfiguration-code)   
Use the `Code` property to specify the request and response functions\. 

 [AWS::AppSync::FunctionConfiguration](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-appsync-functionconfiguration.html#cfn-appsync-functionconfiguration-runtime)   
Use the `Runtime` property to specify the runtime type to be used with a pipeline resolver or function 

 [AWS::AppSync::FunctionConfiguration](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-appsync-functionconfiguration-appsyncruntime.html)   
Use the `AppSyncRuntime` to specify the name and version of your runtime property\.  | November 17, 2022 | 
| [Updated resource](AWS_CloudFront.md) | The following resource was updated: AWS::CloudFront::Distribution\. 

 [AWS::CloudFront::Distribution](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-cloudfront-distribution.html)   
In the [DistributionConfig](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-cloudfront-distribution-distributionconfig.html) use the `ContinuousDeploymentPolicyId` to specify a continuous deployment policy to associate with the distribution\.  
For more information, see [Using CloudFront continuous deployment to safely test CDN configuration changes](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/continuous-deployment.html) in the *Amazon CloudFront Developer Guide*\.  | November 17, 2022 | 
| [Updated resource](AWS_CloudTrail.md) | The following resource was updated: AWS::CloudTrail::EventDataStore 

 [AWS::CloudTrail::EventDataStore](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-cloudtrail-eventdatastore.html)   
Use the `KmsKeyId` property to specify the AWS KMS key ID to use to encrypt the events delivered by CloudTrail\.  | November 17, 2022 | 
| [Updated resource](AWS_AutoScaling.md) | The following resource was updated: AWS::AutoScaling::AutoScalingGroup\. 

 [AWS::AutoScaling::AutoScalingGroup InstanceRequirements](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-autoscaling-autoscalinggroup-instancerequirements.html)   
Use the `AllowedInstanceTypes` and `NetworkBandwidthGbpsRequest` properties when using attribute\-based instance type selection\.  | November 17, 2022 | 
| [Updated resource](AWS_IVS.md) | The following resource was updated: AWS::IVS::RecordingConfiguration 

 [AWS::IVS::RecordingConfiguration](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ivs-recordingconfiguration.html)   
Use the `RecordingReconnectWindowSeconds` property to control when multiple streams from the same broadcast are merged together\.  | November 17, 2022 | 
| [Updated resource](AWS_S3.md) | The following resource was updated: AWS::S3::StorageLens\. 

 [AWS::S3::StorageLens AdvancedCostOptimizationMetrics](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-s3-storagelens-advancedcostoptimizationmetrics.html)   
Use `AWS::S3::StorageLens AdvancedCostOptimizationMetrics` to enable advanced cost optimization metrics for S3 Storage Lens\. 

 [AWS::S3::StorageLens AdvancedDataProtectionMetrics](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-s3-storagelens-advanceddataprotectionmetrics.html)   
Use `AWS::S3::StorageLens AdvancedDataProtectionMetrics` to enable advanced data protection metrics for S3 Storage Lens\. 

 [AWS::S3::StorageLens DetailedStatusCodesMetrics](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-s3-storagelens-detailedstatuscodesmetrics.html)   
Use `AWS::S3::StorageLens DetailedStatusCodesMetrics` to enable detailed status code metrics for S3 Storage Lens\.  | November 17, 2022 | 
| [New resources](AWS_Organizations.md) | The following resources were added: `AWS::Organizations::Account`, `AWS::Organizations::OrganizationalUnit`, and `AWS::Organizations::Policy`\. 

 [AWS::Organizations::Account](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-organizations-account.html)   
Use the `AWS::Organizations::Account` resource to create an AWS account that is automatically a member of the organization whose credentials made the request\. 

 [AWS::Organizations::OrganizationalUnit](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-organizations-organizationalunit.html)   
Use the `AWS::Organizations::OrganizationalUnit` resource to create an organizational unit \(OU\) within a root or parent OU in AWS Organizations\. 

 [AWS::Organizations::Policy](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-organizations-policy.html)   
Use the `AWS::Organizations::Policy` resource to create a policy of a specified type that you can attach to a root, an organizational unit \(OU\), or an individual AWS account in AWS Organizations\.  | November 17, 2022 | 
| [New resource](AWS_EMRServerless.md) | The following resource was added: AWS::EMRServerless::Application:Architecture\. 

 [AWS::EMRServerless::Application:Architecture](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-emrserverless-application.html)   
Use the `AWS::EMRServerless::Application:Architecture` resource to specify the CPU architecture type of the application\.  | November 17, 2022 | 
| [New Resource](AWS_CloudFront.md) | The following resource was added: AWS::CloudFront::ContinuousDeploymentPolicy\. 

 [AWS::CloudFront::ContinuousDeploymentPolicy](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-cloudfront-continuousdeploymentpolicy.html)   
Use the `AWS::CloudFront::ContinuousDeploymentPolicy` resource in a CloudFront continuous deployment workflow\.  
For more information, see [Using CloudFront continuous deployment to safely test CDN configuration changes](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/continuous-deployment.html) in the *Amazon CloudFront Developer Guide*\.  | November 17, 2022 | 
| [New property](AWS_GreengrassV2.md) | The following property was added: AWS::GreengrassV2::Deployment\.ParentTargetArn\. 

 [AWS::GreengrassV2::Deployment](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-greengrassv2-deployment.html)   
Use the `AWS::GreengrassV2::Deployment.ParentTargetArn` property to set the parent deployment of a subdeployment\.  | November 15, 2022 | 
| [Updated resources](AWS_AppStream.md) | The following resources were updated: `AWS::AppStream::DirectoryConfig` 

 [AWS::AppStream::DirectoryConfig RSS ](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-appstream-directoryconfig.html)   
Use the `CertificateBasedAuthProperties` property to specify the certificate\-based authentication properties used to authenticate SAML 2\.0 Identity Provider \(IdP\) user identities to Active Directory domain\-joined streaming instances\.  | November 10, 2022 | 
| [Updated resources](AWS_Batch.md) | The following resources were updated: [AWS::Batch::ComputeEnvironment](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-batch-computeenvironment.html) and [AWS::Batch::JobDefinition](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-batch-jobdefinition.html) 

 [AWS::Batch::ComputeEnvironment](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-batch-computeenvironment.html)   
Use the `EksConfiguration` property to specify the details for the EKS cluster that supports the compute environment\. 

 [AWS::Batch::JobDefinition](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-batch-jobdefinition.html)   
Use the `EksProperty` property to specify properties for Amazon EKS based jobs\.  | November 10, 2022 | 
| [Updated resources](AWS_EC2.md) | The following resources were updated: AWS::EC2::SpotFleet, AWS::EC2::EC2Fleet, and AWS::EC2::LaunchTemplate\. 

 [AWS::EC2::SpotFleet InstanceRequirementsRequest](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ec2-spotfleet-instancerequirementsrequest.html)   
Use the `AllowedInstanceTypes` and `NetworkBandwidthGbps` properties when using attribute\-based instance type selection\. 

 [AWS::EC2::EC2Fleet InstanceRequirementsRequest](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ec2-ec2fleet-instancerequirementsrequest.html)   
Use the `AllowedInstanceTypes` and `NetworkBandwidthGbps` properties when using attribute\-based instance type selection\. 

 [AWS::EC2::LaunchTemplate InstanceRequirements](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ec2-launchtemplate-launchtemplatedata-instancerequirements.html)   
Use the `AllowedInstanceTypes` and `NetworkBandwidthGbps` properties when using attribute\-based instance type selection\.  | November 10, 2022 | 
| [Updated resources](AWS_EC2.md) | The following resource was updated: AWS::EC2::LaunchTemplate\. 

 [AWS::EC2::LaunchTemplate MaintenanceOptions](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ec2-launchtemplate-launchtemplatedata-maintenanceoptions.html)   
Use the `AutoRecovery` property to disable the automatic recovery of your instance or set it to default\. 

 [AWS::EC2::LaunchTemplate Placement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ec2-launchtemplate-launchtemplatedata-placement.html)   
Use the `GroupId` property to launch an instance in a shared placement group\.  | November 10, 2022 | 
| [Updated resource](AWS_AutoScaling.md) | The following resource was updated: AWS::AutoScaling::AutoScalingGroup\. 

 [AWS::AutoScaling::AutoScalingGroup MixedInstancesPolicy](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-autoscaling-autoscalinggroup-mixedinstancespolicy.html)   
Use the `SpotAllocationStrategy` property to specify `price-capacity-optimized` as the allocation strategy for your Spot capacity\.  | November 10, 2022 | 
| [Updated resource](AWS_RDS.md) | The following resource was updated: AWS::RDS::DBInstance 

 [AWS::RDS::DBInstance](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-rds-dbinstance.html)   
Use the `StorageThroughput` property to specify the storage throughput value for the DB instance\. This setting is applicable only for `gp3` storage type\.  | November 10, 2022 | 
| [New resources](AWS_MemoryDB.md) | The following resources were added: AWS::MemoryDB::Cluster\.DataTiering 

 [AWS::MemoryDB::Cluster\.DataTiering](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-memorydb-cluster.html)   
The `data-tiering-enabled` parameter enables data tiering\. Data tiering is only supported for clusters using the r6gd node type\. For more information, see [Data tiering](https://docs.aws.amazon.com/memorydb/latest/devguide/data-tiering.html)\. | November 10, 2022 | 
| [Launch of Resource Explorer](AWS_ResourceExplorer2.md) | Initially added the resources for AWS Resource Explorer\. 

 [AWS::ResourceExplorer2::Index](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-resource-explorer-index.html)   
Use the `AWS::ResourceExplorer2::Index` resource to turn on Resource Explorer in an AWS Region by creating an index\. 

 [AWS::ResourceExplorer2::View](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-resource-explorer-view.html)   
Use the `AWS::ResourceExplorer2::View` resource to create a view that your users can use to search\. 

 [AWS::ResourceExplorer2::DefaultViewAssociation](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-resource-explorer-defaultviewassociation.html)   
Use the `AWS::ResourceExplorer2::DefaultViewAssociation` resource to designate a view as the default for its AWS Region in the account\.  | November 7, 2022 | 
| [Updated resource](AWS_RDS.md) | The following resource was updated: AWS::RDS::DBCluster 

 [AWS::RDS::DBCluster](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-rds-dbcluster.html)   
Use the `TimeoutAction` value in `ScalingConfiguration` property syntax to define the action to take when the timeout is reached\.   
The `DBClusterArn` return value is the Amazon Resource Name \(ARN\) for the DB cluster\.  
The `DBClusterResourceId` return value is the AWS Region\-unique, immutable identifier for the DB cluster\.  | November 3, 2022 | 
| [Updated resource](AWS_RDS.md) | The following resource was updated: AWS::RDS::DBInstance 

 [AWS::RDS::DBInstance](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-rds-dbinstance.html)   
Use the `ReplicaMode` property to define the open mode of an Oracle read replica\.  
The `DBInstanceArn` return value is the Amazon Resource Name \(ARN\) for the your instance\.  
The `DbiResourceId` return value is the AWS Region\-unique, immutable identifier for the DB instance\.   | November 3, 2022 | 
| [Updated resource](AWS_RDS.md) | The following resource was updated: AWS::RDS::DBClusterParameterGroup 

 [AWS::RDS::DBClusterParameterGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-rds-dbparametergroup.html)   
Use the `DBClusterParameterGroupName` property to specify the name of the DB cluster parameter group\.  | November 3, 2022 | 
| [Updated resource](AWS_RDS.md) | The following resource was updated: AWS::RDS::OptionGroup 

 [AWS::RDS::OptionGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-rds-optiongroup.html)   
Use the `OptionGroupName` property to specify the name of the new option group\.  | November 3, 2022 | 
| [Updated resource](AWS_RDS.md) | The following resource was updated: AWS::RDS::DBInstance 

 [AWS::RDS::DBParameterGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-rds-dbparametergroup.html)   
Use the `DBParameterGroupName` property to specify the name of the DB parameter group\.  | November 3, 2022 | 
| [New resource](AWS_SES.md) | The following resource and properties were added: AWS::SES::VdmAttributes, AWS::SES::ConfigurationSet VdmOptions \. 

 [AWS::SES::VdmAttributes](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ses-vdmattributes.html)   
Use the `VdmAttributes` resource to specify the Virtual Deliverability Manager \(VDM\) attributes that apply to your Amazon SES account\. 

 [AWS::SES::ConfigurationSet VdmOptions](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ses-configurationset-vdmoptions.html)   
Use the `VdmOptions` property to specify the VDM properties that apply to a configuration set\.  | November 3, 2022 | 
| [New resource](AWS_SupportApp.md) | The following resource was added: AWS::SupportApp::SlackWorkspaceConfiguration\. 

 [AWS::SupportApp::SlackWorkspaceConfiguration](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-supportapp-slackworkspaceconfiguration.html)   
Use the `AWS::SupportApp::SlackWorkspaceConfiguration` resource to specify your configuration for the AWS Support App in Slack\.  | November 3, 2022 | 
| [Updated resource](AWS_AutoScaling.md) | The following resource was updated: AWS::AutoScaling::AutoScalingGroup\. 

 [AWS::AutoScaling::AutoScalingGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-as-group.html)   
Use the `DefaultInstanceWarmup` property to unify all the warm\-up and cooldown settings for an Auto Scaling group and optimize the performance of scaling policies that scale continuously, such as target tracking and step scaling policies\.  | November 2, 2022 | 
| [Updated resource](AWS_AppRunner.md) | The following resource was updated: AWS::AppRunner::Service 

 [AWS::AppRunner::Service\.IngressConfiguration](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-apprunner-service.html#cfn-apprunner-service-IngressConfiguration)   
New property\. The ingress configuration of the App Runner service\.  | October 31, 2022 | 
| [New resource](AWS_AppRunner.md) | The following resource was added: AWS::AppRunner::VpcIngressConnection 

 [AWS::AppRunner::VpcIngressConnection](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-apprunner-vpcingressconnection.html)   
Use the `AWS::AppRunner::VpcIngressConnection` resource to create or update an AWS App Runner VPC Ingress Connection\.  | October 31, 2022 | 
| [New resource](AWS_IoT.md) | The following resource was added: AWS::IoT::TopicRule LocationAction\. 

 [AWS::IoT::TopicRule LocationAction](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-iot-topicrule-locationaction.html)   
The AWS::IoT::TopicRule LocationAction resource to specify a Location Action\.  | October 31, 2022 | 
| [Updated resource](AWS_Connect.md) | The following resource was updated: AWS::Connect::User UserIdentityInfo 

 [AWS::Connect::User UserIdentityInfo](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-connect-user-useridentityinfo.html)   
Use the `Mobile` property to specify the user's mobile number\.   
Use the `SecondaryEmail` property to specify the user's secondary email address\.   | October 27, 2022 | 
| [Updated resource](AWS_RUM.md) | The following resource was updated: AWS::RUM::AppMonitor\. 

 [AWS::RUM::AppMonitor](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-rum-appmonitor.html)   
The `MetricDestination` and `MetricDefinition` properties were added to the `AWS::RUM::AppMonitor` resource to support Amazon CloudWatch extended metrics\. For more information, see [ Extended metrics that you can send to CloudWatch and CloudWatch Evidently](https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/CloudWatch-RUM-vended-metrics.html)\.  | October 27, 2022 | 
| [Updated resource](AWS_Cognito.md) | The following resource was updated: AWS::Cognito::UserPoolClient 

 [AWS::Cognito::UserPool](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-cognito-userpool.html)   
The `DeletionProtection` property of a user pool prevents accidental deletion of user pools\.  | October 24, 2022 | 
| [Updated resource](AWS_SES.md) | The following property was added to the AWS::SES::DedicatedIpPool resource: 

 [AWS::SES::DedicatedIpPool](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ses-dedicatedippool.html)   
Use the `ScalingMode` property to specify the scaling mode of a dedicated IP pool\.  | October 20, 2022 | 
| [New resource](AWS_FSx.md) | The following new resource was added: AWS::FSx::DataRepositoryAssociation 

[AWS::FSx::DataRepositoryAssociation](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-fsx-datarepositoryassociation.html)  
Use the `DataRepositoryAssociation` resource to link an FSx for Lustre file system to an Amazon S3 data repository\.  | October 20, 2022 | 
| [Updated resource](AWS_RDS.md) | The following resource was updated: AWS::RDS::DBCluster 

 [AWS::RDS::DBCluster](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-rds-dbcluster.html)   
Use the `Domain` property to specify the directory ID of the Active Directory to create the DB cluster\.  
Use the `DomainIAMRoleName` property to specify the name of the IAM role to use when making API calls to the Directory Service\.  
Use the `NetworkType` property to indicate the network type of the DB cluster\.  
The following properties now supported for Multi\-AZ DB clusters: AllocatedStorage, AutoMinorVersionUpgrade, BackupRetentionPeriod, CopyTagsToSnapshot, DatabaseName, DBClusterIdentifier, DBClusterInstanceClass, DBClusterParameterGroupName, DBSubnetGroupName, DeletionProtection, EnableCloudwatchLogsExports, Engine, EngineVersion, Iops, KmsKeyId, MasterUsername, MasterUserPassword, MonitoringInterval, MonitoringRoleArn, PerformanceInsightsEnabled, PerformanceInsightsKmsKeyId, PerformanceInsightsRetentionPeriod, Port, PreferredBackupWindow, PreferredMaintenanceWindow, PubliclyAccessible, StorageEncrypted, StorageType, Tags, and VpcSecurityGroupIds   | October 13, 2022 | 
| [Updated resource](AWS_RDS.md) | The following resource was updated: AWS::RDS::DBInstance 

 [AWS::RDS::DBInstance](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-rds-dbinstance.html)   
Use the `NetworkType` property to indicate the network type of the DB cluster\.  | October 13, 2022 | 
| [Updated resource](AWS_Connect.md) | The following resource was updated: AWS::Connect::PhoneNumber 

 [AWS::Connect::PhoneNumber](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-connect-phonenumber.html)   
Use the `AWS::Connect::PhoneNumber` resource to claim a phone number to an Amazon Connect instance or traffic distribution group\.  | October 10, 2022 | 
| [New resource](AWS_GreengrassV2.md) | The following resources were added: AWS::GreengrassV2::Deployment\. 

 [AWS::GreengrassV2::Deployment](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-greengrassv2-deployment.html)   
Use the `AWS::GreengrassV2::Deployment` resource to create a new deployment to your core devices in AWS IoT Greengrass\.  | October 6, 2022 | 
| [New and updated resources](AWS_Transfer.md) | The following resources were added: AWS::Transfer::Agreement, AWS::Transfer::Connector, AWS::Transfer::Certificate, and AWS::Transfer::Profile\. The following resource was updated: AWS::Transfer::Server WorkflowDetails 

 [AWS::Transfer::Agreement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-transfer-agreement.html)   
Use the `Agreement` resource to specify an agreement between trading partners in AWS Transfer Family\. 

 [AWS::Transfer::Certificate](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-transfer-certificate.html)   
Use the `Certificate` resource to import signing and encryption certificates for AS2 in AWS Transfer Family\. 

 [AWS::Transfer::Connector](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-transfer-connector.html)   
Use the `Connector` resource to create an entity that captures the parameters for an outbound AS2 connection in AWS Transfer Family\. 

 [AWS::Transfer::Profile](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-transfer-profile.html)   
Use the `Profile` resource to specify local and partner profiles for servers in AWS Transfer Family that use the AS2 protocol\. 

 [AWS::Transfer::Server WorkflowDetails](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-transfer-server.html)   
Use the `OnPartialUpload` parameter to trigger a workflow in the case a transfer is interrupted and does not complete\.  | October 6, 2022 | 
| [Updated resource](AWS_KMS.md) | The following resource was updated: `AWS::KMS::Key`\. 

 [AWS::KMS::Key](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-kms-key.html)   
If you change the value of an immutable property of an existing `AWS::KMS::Key` resource, the request to update the resource fails\. Previously, changing the value of an immutable property caused the existing `AWS::KMS::Key` to be deleted and replaced\.   
This change does not affect the `AWS::KMS::Alias` or `AWS::KMS::ReplicaKey` resources\. If you change an immutable property of these resources, the resource is deleted and replaced\.  | September 30, 2022 | 
| [Updated resource](AWS_RDS.md) | The following resource was updated: AWS::RDS::DBCluster 

 [AWS::RDS::DBCluster](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-rds-dbcluster.html)   
Use the `ServerlessV2ScalingConfiguration` property to specify the scaling configuration of an Aurora Serverless V2 DB cluster\.  
The `DBClusterResourceId` return value is the AWS Region\-unique, immutable identifier for the DB cluster\.  
Use the `DBInstanceParameterGroupName` property to specify the name of the DB parameter group to apply to all instances of the DB cluster\.  | September 29, 2022 | 
| [Updated resource](AWS_RDS.md) | The following resource was updated: AWS::RDS::DBInstance 

 [AWS::RDS::DBInstance](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-rds-dbinstance.html)   
Use the `NcharCharacterSetName` property to specify the name of the NCHAR character set for the Oracle DB instance\.  
Use the `CustomIAMInstanceProfile` property to specify the instance profile associated with the underlying Amazon EC2 instance of an RDS Custom DB instance\.  | September 29, 2022 | 
| [New resources](AWS_IdentityStore.md) | The following resources were added: AWS::IdentityStore::Group and AWS::IdentityStore::GroupMembership\. 

 [AWS::IdentityStore::Group](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-identitystore-group.html)   
Use the `AWS::IdentityStore::Group` resource to manage groups in an identity store\. 

 [AWS::IdentityStore::GroupMembership](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-identitystore-groupmembership.html)   
Use the `AWS::IdentityStore::GroupMembership` resource to manage group membership in an identity store\.  | September 29, 2022 | 
| [New resource](AWS_CloudFront.md) | The following resource was added: AWS::CloudFront::MonitoringSubscription\. 

 [AWS::CloudFront::MonitoringSubscription](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-cloudfront-monitoringsubscription.html)   
Use the `AWS::CloudFront::MonitoringSubscription` resource to enable additional CloudWatch metrics for the specified Amazon CloudFront distribution\.  
For more information, see [Viewing additional CloudFront distribution metrics](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/viewing-cloudfront-metrics.html#monitoring-console.distributions-additional) in the *Amazon CloudFront Developer Guide*\.  | September 29, 2022 | 
| [Updated resource](AWS_IoT.md) | The following resource was updated: AWS::IoT::CACertificate\. 

 [AWS::IoT::CACertificate](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-iot-cacertificate.html)   
The AWS::IoT::CACertificate resource adds RemoveAutoRegistration property\.  | September 22, 2022 | 
| [New resource](AWS_IoTFleetWise.md) | The following resource was added: AWS::IoTFleetWise::Campaign 

 [AWS::IoTFleetWise::Campaign](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-iotfleetwise-campaign.html)   
Use the `AWS::IoTFleetWise::Campaign` resource to specify a campaign in \.  | September 22, 2022 | 
| [New resource](AWS_IoTFleetWise.md) | The following resource was added: AWS::IoTFleetWise::DecoderManifest 

 [AWS::IoTFleetWise::DecoderManifest](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-iotfleetwise-decodermanifest.html)   
Use the `AWS::IoTFleetWise::DecoderManifest` resource to specify a decoder manifest in \.  | September 22, 2022 | 
| [New resource](AWS_IoTFleetWise.md) | The following resource was added: AWS::IoTFleetWise::Fleet 

 [AWS::IoTFleetWise::Fleet](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-iotfleetwise-fleet.html)   
Use the `AWS::IoTFleetWise::Fleet` resource to specify a fleet in \.  | September 22, 2022 | 
| [New resource](AWS_IoTFleetWise.md) | The following resource was added: AWS::IoTFleetWise::ModelManifest 

 [AWS::IoTFleetWise::ModelManifest](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-iotfleetwise-modelmanifest.html)   
Use the `AWS::IoTFleetWise::ModelManifest` resource to specify a model manifest in \.  | September 22, 2022 | 
| [New resource](AWS_IoTFleetWise.md) | The following resource was added: AWS::IoTFleetWise::SignalCatalog 

 [AWS::IoTFleetWise::SignalCatalog](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-iotfleetwise-signalcatalog.html)   
Use the `AWS::IoTFleetWise::SignalCatalog` resource to specify a signal catalog in \.  | September 22, 2022 | 
| [New resource](AWS_IoTFleetWise.md) | The following resource was added: AWS::IoTFleetWise::Vehicle 

 [AWS::IoTFleetWise::Vehicle](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-iotfleetwise-vehicle.html)   
Use the `AWS::IoTFleetWise::Vehicle` resource to specify a vehicle in \.  | September 22, 2022 | 
| [Updated resource](AWS_Cognito.md) | The following resource was updated: AWS::Cognito::UserPoolClient 

 [AWS::Cognito::UserPoolClient](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-cognito-userpoolclient.html)   
The `AuthSessionValidity` property of a user pool client makes it possible to increase the duration of a prompt for authentication input like a password or MFA code\.  | September 15, 2022 | 
| [Updated resource](AWS_EKS.md) | The following property was updated: `AWS::EKS::Cluster` 

 [https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-eks-cluster.html](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-eks-cluster.html)   
Use the `OutpostConfig` property to specify the configuration of your local Amazon EKS cluster on an Outpost\.   | September 15, 2022 | 
| [New resource](AWS_Evidently.md) | A new parameter was added to the AWS::Evidently::Project\. 

 [Evidently resource type reference](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/AWS_Evidently.html)   
The `AppConfigResource` property was added to the `AWS::Evidently::Project` resource to enable you to use Client\-side evaluation \- powered by AWS AppConfig in your projects\.  
For more information, see [ Use client\-side evaluation \- powered by AWS AppConfig](https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/CloudWatch-Evidently-client-side-evaluation.html)\.  | September 15, 2022 | 
| [Updated resources](AWS_EC2.md) | The following resource was updated: AWS::EC2::LaunchTemplate\. 

 [ AWS::EC2::LaunchTemplate](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-launchtemplate.html#cfn-ec2-launchtemplate-versiondescription)   
A description for the first version of the launch template\.  | September 8, 2022 | 
| [Updated resource](AWS_KMS.md) | The following resource was updated: `AWS::KMS::Key`\. 

 [AWS::KMS::Key](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-kms-key.html)   
Add full `AWS::KMS::Key` support to Middle East \(UAE\) Region \(me\-central\-1\), including support for using a CloudFormation template to create and manage asymmetric KMS keys and multi\-Region KMS keys \(primary or replica\)\.  | September 8, 2022 | 
| [Updated resource](AWS_OpenSearchService.md) | The following resource was updated: AWS::OpenSearchService::Domain\. 

 [AWS::OpenSearchService::Domain](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-opensearchservice-domain.html)   
Use the `Throughput` property to specify the throughput of the EBS volumes attached to data nodes\. This propertly applies only to the `gp3` volume type\.  | September 8, 2022 | 
| [Updated resource](AWS_SNS.md) | The following resource was updated: AWS::SNS::Topic\. 

 [AWS::SNS::Topic](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-sns-topic.html)   
Use the `DataProtectionPolicy` property to attach a DataProtectionPolicy to an SNS topic\.  | September 8, 2022 | 
| [New resource](AWS_CloudFront.md) | The following resource was added: AWS::CloudFront::OriginAccessControl\. 

 [AWS::CloudFront::OriginAccessControl](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-cloudfront-originaccesscontrol.html)   
Use the `AWS::CloudFront::OriginAccessControl` resource to create a new origin access control in Amazon CloudFront\.  
For more information, see [Restricting access to an Amazon S3 origin](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/private-content-restricting-access-to-s3.html) in the *Amazon CloudFront Developer Guide*\.  | September 8, 2022 | 
| [New resource](AWS_Connect.md) | The following resource was added: AWS::Connect::InstanceStorageConfig 

 [AWS::Connect::InstanceStorageConfig](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-connect-instancestorageconfig.html)   
Use the `AWS::Connect::InstanceStorageConfig` resource to configure instance storage\.  | September 1, 2022 | 
| [New resource](AWS_ControlTower.md) | The following resource was added: AWS::ControlTower::EnabledControl\. 

 [AWS::ControlTower::EnabledControl](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-controltower-enabledcontrol.html)   
Use the `AWS::ControlTower::EnabledControl` resource to specify an asynchronous operation that manages a control\.  | September 1, 2022 | 
| [New resource](AWS_Macie.md) | The following resource was added: `AWS::Macie::AllowList`\. 

 [AWS::Macie::AllowList](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-macie-allowlist.html)   
Use the `AWS::Macie::AllowList` resource to specify text or a text pattern for Amazon Macie to ignore when it inspects data sources for sensitive data\.  | September 1, 2022 | 
| [Updated resources](AWS_AppMesh.md) | The following resources were updated: AWS::AppMesh::VirtualNode, AWS::AppMesh::VirtualGateway, AWS::AppMesh::GatewayRoute and AWS::AppMesh::Route 

 [AWS::AppMesh::VirtualNode](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-appmesh-virtualnode.html)   
Use the `Format` property to represent the specified format for the logs\. The format is either `json_format` or `text_format`\.  
Use the `JsonFormatRef` resource to represent object that represents the key value pairs for the JSON\.  
Use the `LoggingFormat` resource to represent object that represents the format for the logs\. 

 [AWS::AppMesh::VirtualGateway](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-appmesh-virtualgateway.html)   
Use the `VirtualGatewayFileAccessLogFormat` property to represent the specified format for the logs\. The format is either `json_format` or `text_format`\.  
Use the `JsonFormatRef` resource to represent object that represents the key value pairs for the JSON\.  
Use the `LoggingFormat` resource to represent object that represents the format for the logs\. 

 [AWS::AppMesh::GatewayRoute](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-appmesh-gatewayroute.html)   
Use the `Port` property to represent the port number of the gateway route target\. 

 [AWS::AppMesh::Route](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-appmesh-route.html)   
Use the `Port` property to represent the port number of the gateway route target\.  
Use the `Port` property to represent an object that is the criteria for determining a request match\.  
Use the `TcpRouteMatch` resource to represent an object that is the TCP route to match\.  | August 25, 2022 | 
| [Updated resource](AWS_MediaPackage.md) | The following resource was updated: AWS::MediaPackage::OriginEndpoint\. 

 [AWS::MediaPackage::OriginEndpoint\.](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-mediapackage-originendpoint.html)>   
Use the `DVB_DASH_2014` property to select the DVB\_DASH\_2014 profile for the output\.  | August 25, 2022 | 
| [New resource](AWS_Connect.md) | The following resource was added: AWS::Connect::Instance 

 [AWS::Connect::Instance](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-connect-instance.html)   
Use the `AWS::Connect::Instance` resource to create an instance\.  | August 25, 2022 | 
| [New resource](AWS_SupportApp.md) | The following resource was added: AWS::SupportApp::SlackChannelConfiguration\. 

 [AWS::SupportApp::SlackChannelConfiguration](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-supportapp-slackchannelconfiguration.html)   
Use the `AWS::SupportApp::SlackChannelConfiguration` resource to specify your configuration for the AWS Support App in Slack\.  | August 25, 2022 | 
| [New resource](AWS_SupportApp.md) | The following resource was added: AWS::SupportApp::AccountAlias\. 

 [AWS::SupportApp::AccountAlias](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-supportapp-accountalias.html)   
Use the `AWS::SupportApp::AccountAlias` resource to specify your alias name\. You can use this alias to identify your AWS account in the AWS Support App\.  | August 25, 2022 | 
| [Fn::ToJsonString intrinsic function](#ReleaseHistory) | The Fn::ToJsonString intrinsic function converts an object or array to its corresponding JSON string\.For more information, see [Fn::ToJsonString](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-tojsonstring.html)\. | August 24, 2022 | 
| [Fn::Length intrinsic function](#ReleaseHistory) | The Fn::Length intrinsic function returns the number of elements within an array or an intrinsic function that returns an array\.For more information, see [Fn::Length](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-length.html)\. | August 24, 2022 | 
| [AWS::LanguageExtensions transform](#ReleaseHistory) | The AWS::LanguageExtensions transform is a macro hosted by AWS CloudFormation that lets you use intrinsic functions and other functionalities not included by default in AWS CloudFormation\.For more information, see [AWS::LanguageExtensions transform](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/transform-aws-languageextensions.html)\. | August 24, 2022 | 
| [Updated resources](AWS_WAFv2.md) | The following resource was updated: AWS::WAFv2::WebACLAssociation\. 

 [AWS::WAFv2::WebACLAssociation](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-wafv2-webaclassociation.html)   
The `ResourceArn` property now accepts `AWS::Cognito::UserPool` ARNs\.   | August 23, 2022 | 
| [Updated resource](AWS_FMS.md) | The following resource was updated: AWS::FMS::Policy\. 

 [AWS::FMS::Policy](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-fms-policy.html)   
The `AWS::FMS::Policy` resource now allows you to manage third\-party firewalls, as well as AWS Network Firewall policies that use centralized or distributed deployment models\.  | August 18, 2022 | 
| [Updated resource](AWS_Lambda.md) | The following resource was updated: AWS::Lambda::EventSourceMapping\. 

 [AWS::Lambda::EventSourceMapping](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-lambda-eventsourcemapping.html)   
 Use the `SelfManagedKafkaEventSourceConfig` property to define specific configuration settings for a self\-managed Kafka event source, such as the consumer group ID\. Use the `AmazonManagedKafkaEventSourceConfig` property to define specific configuration settings for an MSK event source, such as the consumer group ID\.   | August 18, 2022 | 
| [New resource](AWS_DynamoDB.md) | The following resource was added: AWS::DynamoDB::Table\.ImportSourceSpecification 

 [AWS::DynamoDB::Table\.ImportSourceSpecification](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-dynamodb-table.html)   
Use the `AWS::DynamoDB::Table.ImportSourceSpecification` resource to import from S3 into DynamoDB\.  | August 18, 2022 | 
| [Updated resource](AWS_CloudFront.md) | The following resource was updated: AWS::CloudFront::Distribution\. 

 [AWS::CloudFront::Distribution](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-cloudfront-distribution.html)   
In the [HttpVersion](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-cloudfront-distribution-distributionconfig.html#cfn-cloudfront-distribution-distributionconfig-httpversion) property, use the `http2and3` and `http3` values to specify the maximum HTTP version\(s\) that you want viewers to use to communicate with Amazon CloudFront\.  
For more information, see [Supported HTTP versions](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/distribution-web-values-specify.html#DownloadDistValuesSupportedHTTPVersions) in the *Amazon CloudFront Developer Guide*\.  | August 15, 2022 | 
| [Updated resource](AWS_GuardDuty.md) | The following resources were updated: AWS::GuardDuty::Filter, AWS::GuardDuty::IPSet, and AWS::GuardDuty::ThreatIntelSet 

 [AWS::GuardDuty::Filter](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-guardduty-filter.html)   
Use `Tags` property to specify metadata to add to a new filter resource\.  
Use `Rank` property to specify position of the filter in the list of the current filters\. 

 [AWS::GuardDuty::IPSet](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-guardduty-ipset.html)   
Use `Tags` property to specify metadata to add to a new IP set resource\. 

 [AWS::GuardDuty::ThreatIntelSet](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-guardduty-threatintelset.html)   
Use `Tags` property to specify metadata to add to a new threat list resource\.  | August 15, 2022 | 
| [New resources](AWS_M2.md) | The following resources were added: AWS::M2::Application and AWS::M2::Environment\. 

 [AWS::M2::Application](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-m2-application.html)   
Use the `AWS::M2::Application` resource to specify an application in the AWS Mainframe Modernization service\. 

 [AWS::M2::Environment](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-m2-environment.html)   
Use the `AWS::M2::Environment` resource to specify a runtime environment in the AWS Mainframe Modernization service\.  | August 11, 2022 | 
| [New resource](AWS_MSK.md) | The following resource was added: AWS::MSK::ServerlessCluster 

 [AWS::MSK::ServerlessCluster](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-msk-serverlesscluster.html)   
This resource represents an Amazon MSK Serverless cluster\.  | August 11, 2022 | 
| [Updated resources](AWS_WAFv2.md) | The following resources were updated: AWS::WAFv2::WebACL and AWS::WAFv2::RuleGroup\. 

 [AWS::WAFv2::WebACL](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-wafv2-webacl.html)   
In the [SqliMatchStatement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-wafv2-webacl-sqlimatchstatement.html) property type, use the `SensitivityLevel` property to specify the sensitivity that you want to use to inspect for SQL injection attacks\.  

 [AWS::WAFv2::RuleGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-wafv2-rulegroup.html)   
In the [SqliMatchStatement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-wafv2-rulegroup-sqlimatchstatement.html) property type, use the `SensitivityLevel` property to specify the sensitivity that you want to use to inspect for SQL injection attacks\.   | August 4, 2022 | 
| [Updated resource](AWS_GuardDuty.md) | The following resource was updated: AWS::GuardDuty::Detector 

 [AWS::GuardDuty::Detector](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-guardduty-detector.html)   
Use the `CFNDataSourceConfigurations` property to specify the data source when detector is created\.  
Use the `CFNMalwareProtectionConfiguration` property to specify enabling Malware Protection data source\.  
Use the `CFNScanEc2InstanceWithFindingsConfiguration` property to specify enabling data source as Malware Protection for EC2 findings\.  | August 4, 2022 | 
| [Updated resource](AWS_IoT.md) | The following resource was updated: AWS::IoT::CACertificate\. 

 [AWS::IoT::CACertificate](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-iot-cacertificate.html)   
The AWS::IoT::CACertificate resource adds RegistrationConfig type in RegistrationConfig property\.  | August 4, 2022 | 
| [Updated resource](AWS_IoT.md) | The following resource was updated: AWS::IoT::ProvisioningTemplate\. 

 [AWS::IoT::ProvisioningTemplate](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-iot-provisioningtemplate.html)   
The AWS::IoT::ProvisioningTemplate resource now supports TemplateType property\.  | August 4, 2022 | 
| [Updated resource](AWS_RedshiftServerless.md) | The following resource was updated: AWS::RedshiftServerless::Workgroup 

 [AWS::RedshiftServerless::Workgroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-redshiftserverless-workgroup.html)   
The `additionalinfo` parameter was removed from `AWS::RedshiftServerless::Workgroup`\.  | July 28, 2022 | 
| [Updated resource](AWS_Transfer.md) | The following resource was updated: 

 [AWS::Transfer::Server ProtocolDetails ](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-transfer-server-protocoldetails.html)   
Use the `As2Transports` property to indicate the transport method for the AS2 messages\.  | July 28, 2022 | 
| [Updates to resource](AWS_SSO.md) | The following resource was updated: `AWS::SSO::PermissionSet`\.  

 [https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-sso-permissionset.html](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-sso-permissionset.html)   
Use the `CustomerManagedPolicyReferences` and `PermissionsBoundary` properties of the `AWS::SSO::PermissionSet` resource to assign customer managed policies and permissions boundaries in IAM Identity Center\.  | July 21, 2022 | 
| [Updated resources](AWS_EC2.md) | The following resource was updated: AWS::EC2::PlacementGroup\. 

 [ AWS::EC2::PlacementGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-placementgroup.html#aws-resource-ec2-placementgroup-properties)   
Use the `SpreadLevel` parameter to determine how placement groups spread instances\.  | July 21, 2022 | 
| [New resource](AWS_Synthetics.md) | The following resource was added: AWS::Synthetics::Group\. 

 [AWS::Synthetics::Group](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-synthetics-group.html)   
Use the `AWS::Synthetics::Group` resource to create a group\. You can use groups to associate canaries with each other, including cross\-Region canaries\. Using groups can help you with managing and automating your canaries, and you can also view aggregated run results and statistics for all canaries in a group\.  | July 21, 2022 | 
| [New resource](AWS_Evidently.md) | The AWS::Evidently::Segment resource was added\. 

 [Evidently resource type reference](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/AWS_Evidently.html)   
Use a segment to define a portion of your audience that share one or more characteristics\.  
For more information, see [ Use segments to focus your audience](https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/CloudWatch-Evidently-segments.html)\.  | July 21, 2022 | 
| [Managing events with AWS CloudFormation and Amazon EventBridge](#ReleaseHistory) | Receive notifications when specific AWS CloudFormation events such as object creation or deletion occur in an AWS CloudFormation with EventBridge\.For more information, see [Managing events with Amazon EventBridge](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/stacks-event-bridge.html)\. | July 20, 2022 | 
| [Updated resource](AWS_KMS.md) | The following resource was updated: `AWS::KMS::Key`\. 

 [AWS::KMS::Key](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-kms-key.html)   
Added support for SM2 key pairs \(China Regions only\), including the SM2 value for the `KeySpec` property\.  | July 14, 2022 | 
| [Updated resource](AWS_SageMaker.md) | The following resource was updated: AWS::SageMaker::NotebookInstance 

 [AWS::SageMaker::NotebookInstance](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-sagemaker-notebookinstance.html)   
Use the `InstanceMetadataServiceConfiguration` property to specify information about the IMDS configuration of the notebook instance\.  
Use the `InstanceMetadataServiceConfiguration.MinimumInstanceMetadataServiceVersion` property to specify the minimum IMDS version that the notebook instance supports\.  | July 14, 2022 | 
| [New resources](AWS_RedshiftServerless.md) | Use these resources to manage your Amazon Redshift Serverless instance\. 

 [AWS::RedshiftServerless::Workgroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-redshiftserverless-workgroup.html)   
Use the `AWS::RedshiftServerless::Workgroup` resource to manage compute resources in Amazon Redshift Serverless\. 

 [AWS::RedshiftServerless::Namespace](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-redshiftserverless-namespace.html)   
Use the `AWS::RedshiftServerless::Namespace` resource to manage database objects and users in Amazon Redshift Serverless\.  | July 12, 2022 | 
| [Account level](#ReleaseHistory) | AWS CloudFormation announces the general availability of *account filter type*, a feature that allows customers to limit deployment targets to individual accounts or include additional accounts with provided OUs\.For more information, see [Account level targets](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/account-level-targets.html)\. | July 7, 2022 | 
| [Updated resource](AWS_RefactorSpaces.md) | The following resource was updated: AWS::RefactorSpaces::Route\. 

 [AWS::RefactorSpaces::Route](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-refactorspaces-route.html)   
In the [DefaultRouteInput](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-refactorspaces-route-defaultrouteinput.html) property type, use the `ActivationState` property to specify the activation state of the route\.  
In the [UriPathRouteInput](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-refactorspaces-route-uripathrouteinput.html) property type, use the `ActivationState` property to specify the activation state of the route\.  | June 30, 2022 | 
| [New resources](AWS_LakeFormation.md) | The following resources were added: AWS::LakeFormation::DataCellsFilter, AWS::LakeFormation::TagAssociation, documentation target="AWS::LakeFormation::Tag, AWS::LakeFormation::PrincipalPermissions 

 [AWS::LakeFormation::DataCellsfilter](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-lakeformation-datacellsfilter.html)   
Use the `DataCellsFilter` resource to specify a structure for a data cell filter\. 

 [AWS::LakeFormation::PrincipalPermissions](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-lakeformation-PrincipalPermissions.html)   
Use the `AWS::LakeFormation::PrincipalPermissions` resource to specify the permissions that a principal has on an resource\. 

 [AWS::LakeFormation::Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-lakeformation-tag.html)   
Use the `AWS::LakeFormation::Tag` resource to specify an LF\-tag, which consists of a key and one or more possible values for the key\. 

 [AWS::LakeFormation::TagAssociation](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-lakeformation-tagassociation.html)   
Use the `AWS::LakeFormation::TagAssociation` resource to assign an LF\-tag to a Data Catalog resource\.  | June 30, 2022 | 
| [New resource](AWS_DataSync.md) | The following resource was added: AWS::DataSync::LocationFSxONTAP\. 

[AWS::DataSync::LocationFSxONTAP](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-datasync-locationfsxontap.html)  
Use the `AWS::DataSync::LocationFSxONTAP` resource to create a location for an Amazon FSx for ONTAP file system\.  | June 30, 2022 | 
| [New resource](AWS_IoT.md) | The following resource was added: AWS::IoT::CACertificate 

 [AWS::IoT::CACertificate](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-iot-cacertificate.html)   
Use the `AWS::IoT::CACertificate`to specify a CA certificate\.  | June 30, 2022 | 
| [New resource](AWS_SES.md) | The following resource was added: AWS::SES::DedicatedIpPool\. 

 [AWS::SES::DedicatedIpPool](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ses-dedicatedippool.html)   
Use the `DedicatedIpPool` resource to create a new pool of dedicated IP addresses\.  | June 30, 2022 | 
| [New resource](AWS_SES.md) | The following resource and properties were added: AWS::SES::EmailIdentity, AWS::SES::EmailIdentity ConfigurationSetAttributes, AWS::SES::EmailIdentity DkimAttributes, AWS::SES::EmailIdentity DkimSigningAttributes, AWS::SES::EmailIdentity FeedbackAttributes, and AWS::SES::EmailIdentity MailFromAttributes\. 

 [AWS::SES::EmailIdentity](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ses-emailidentity.html)   
Use the `EmailIdentity` resource to specify an identity, such as an email address or domain, for using within SES\. 

 [AWS::SES::EmailIdentity ConfigurationSetAttributes](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ses-emailidentity-configurationsetattributes.html)   
Use the `ConfigurationSetAttributes` property to associate a configuration set with an email identity\. 

 [AWS::SES::EmailIdentity DkimAttributes](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ses-emailidentity-dkimattributes.html)   
Use the `DkimAttributes` property to enable or disable DKIM authentication for an email identity\. 

 [AWS::SES::EmailIdentity DkimSigningAttributes](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ses-emailidentity-dkimsigningattributes.html)   
Use the `DkimSigningAttributes` property to configure or change the DKIM authentication settings for an email domain identity\. 

 [AWS::SES::EmailIdentity FeedbackAttributes](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ses-emailidentity-feedbackattributes.html)   
Use the `FeedbackAttributes` property to enable or disable feedback forwarding for an identity\. 

 [AWS::SES::EmailIdentity MailFromAttributes](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ses-emailidentity-mailfromattributes.html)   
Use the `MailFromAttributes` property to enable or disable the custom Mail\-From domain configuration for an email identity\.  | June 30, 2022 | 
| [Updated resources](AWS_AppStream.md) | The following resources were updated: `AWS::AppStream::Stack` 

 [AWS::AppStream::Stack](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-appstream-stack.html)   
Use the `StreamingExperienceSettings` property to specify the streaming protocol you want your stack to prefer\. This can be UDP or TCP\. Currently, UDP is only supported in the Windows native client\.  | June 28, 2022 | 
| [New resource](AWS_CloudTrail.md) | The following resource was added: AWS::CloudTrail::EventDataStore 

 [AWS::CloudTrail::EventDataStore](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-cloudtrail-eventdatastore.html)   
Use the `EventDataStore` resource to specify an event data store in CloudTrail Lake\. Event data stores are immutable collections of events based on criteria that you select by applying advanced event selectors\. For more information, see [Working with CloudTrail Lake](https://docs.aws.amazon.com/awscloudtrail/latest/userguide/cloudtrail-lake.html) in the *AWS CloudTrail User Guide*\. 

 [AWS::CloudTrail::EventDataStore\.AdvancedEventSelector](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-cloudtrail-eventdatastore-advancedeventselector.html)   
Use the `AdvancedEventSelector` property to specify fine\-grained event properties for data events that you want to log to an event data store\. For more information, see [Data events](https://docs.aws.amazon.com/awscloudtrail/latest/userguide/logging-data-events-with-cloudtrail.html#logging-data-events) in the *AWS CloudTrail User Guide*\. 

 [AWS::CloudTrail::EventDataStore\.AdvancedFieldSelector](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-cloudtrail-eventdatastore-advancedfieldselector.html)   
Use the `AdvancedFieldSelector` property to specify fine\-grained event properties for data events that you want to log to an event data store\. An `AdvancedFieldSelector` is a single selector statement within an advanced event selector\. For more information, see [Data events](https://docs.aws.amazon.com/awscloudtrail/latest/userguide/logging-data-events-with-cloudtrail.html#logging-data-events) in the *AWS CloudTrail User Guide*\.  | June 23, 2022 | 
| [New resource](AWS_ConnectCampaigns.md) | The following resources were added: AWS::ConnectCampaigns::Campaign 

 [AWS::ConnectCampaigns::Campaign](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/AWS_ConnectCampaigns.html)   
Use the `AWS::ConnectCampaigns::Campaign` resource to create a high\-volume outbound campaign\.  | June 23, 2022 | 
| [Updated resources](AWS_MediaTailor.md) | The following resource updated: AWS::MediaTailor::PlaybackConfiguration\. 

 [AWS::MediaTailor::PlaybackConfiguration](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-mediatailor-playbackconfiguration.html)   
Added `DashConfiguration.ManifestEndpointPrefix`, `HlsConfiguration.ManifestEndpointPrefix`, `PlaybackConfigurationArn`, `PlaybackEndpointPrefix`, and `SessionInitializationEndpointPrefix` return values\.  | June 16, 2022 | 
| [New resources](AWS_Route53.md) | The following resource and properties were added: AWS::Route53::CidrCollection, AWS::Route53::RecordSet\.CidrRoutingConfig, and AWS::Route53::RecordSetGroup CidrRoutingConfig 

 [AWS::Route53::CidrCollection](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-route53-cidrcollection.html)   
Use the `AWS::Route53::CidrCollection` resource to create a CIDR collection for IP\-based DNS routing\.  

 [AWS::Route53::RecordSet\.CidrRoutingConfig](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-route53-cidrroutingconfig.html)   
Use the `AWS::Route53::RecordSet.CidrRoutingConfig` property to update IP\-routing information for the DNS record that you want to create\. 

 [AWS::Route53::RecordSetGroup CidrRoutingConfig](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-route53-cidrroutingconfig.html)   
Use the `AWS::Route53::RecordSetGroup CidrRoutingConfig` property to link a resource record set to a CIDR location\.  | June 16, 2022 | 
| [Updated resources](AWS_EC2.md) | The following resource was updated: AWS::EC2::LaunchTemplate\. 

 [ AWS::EC2::LaunchTemplate LaunchTemplateData](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ec2-launchtemplate-launchtemplatedata.html#cfn-ec2-launchtemplate-launchtemplatedata-disableapistop)   
Use the `DisableApiStop` parameter to enable or disable an instance for stop protection\.  | June 9, 2022 | 
| [Updated resource](AWS_DataSync.md) | The following resource was updated: AWS::DataSync::LocationEFS\. 

[AWS::DataSync::LocationEFS](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-datasync-locationefs.html)  
Use the `AccessPointArn` property to specify an access point for your Amazon EFS file system\.  
Use the `FileSystemAccessRoleArn` property to specify an IAM role that DataSync assumes when mounting your file system\.  
Use the `InTransitEncryption` property to specify whether you want DataSync to use Transport Layer Security \(TLS\) 1\.2 encryption when it copies data to or from your file system\.  | June 9, 2022 | 
| [Updated resource](AWS_SES.md) | The following property was added to the AWS::SES::ConfigurationSetEventDestination resource: 

 [AWS::SES::ConfigurationSetEventDestination SnsDestination](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ses-configurationseteventdestination-snsdestination.html)   
Use the `SnsDestination` property to specify an Amazon Simple Notification Service \(Amazon SNS\) event destination to publish email sending events\.  | June 9, 2022 | 
| [Updated resource](AWS_SES.md) | The following properties were updated to SES API v2 for the AWS::SES::ConfigurationSet resource: 

 [AWS::SES::ConfigurationSet DeliveryOptions](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ses-configurationset-deliveryoptions.html)   
Use the `DeliveryOptions` property to assign a dedicated IP pool to this configuration set\. 

 [AWS::SES::ConfigurationSet ReputationOptions](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ses-configurationset-reputationoptions.html)   
Use the `ReputationOptions` property to enable or disable collection of reputation metrics for emails sent with this configuration set\. 

 [AWS::SES::ConfigurationSet SendingOptions](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ses-configurationset-sendingoptions.html)   
Use the `SendingOptions` property to enable or disable email sending for messages that use this configuration set\. 

 [AWS::SES::ConfigurationSet SuppressionOptions](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ses-configurationset-suppressionoptions.html)   
Use the `SuppressionOptions` property to specify a list that contains the reasons that email addresses are automatically added to the suppression list\. 

 [AWS::SES::ConfigurationSet TrackingOptions](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ses-configurationset-trackingoptions.html)   
Use the `TrackingOptions` property to specify a custom domain to use for open and click tracking elements in emails that you send from this configuration set\.  | June 9, 2022 | 
| [New resource](AWS_Connect.md) | The following resources were added: AWS::Connect::TaskTemplate 

 [AWS::Connect::TaskTemplate](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-connect-tasktemplate.html)   
Use the `AWS::Connect::TaskTemplate` resource to create a task template\.  | June 9, 2022 | 
| [Updated resource](AWS_IoTEvents.md) | The following property was updated: AWS::IoTEvents::AlarmModel\.IotSiteWise\. 

 [ AWS::IoTEvents::AlarmModel\.IotSiteWise](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-iotevents-alarmmodel-iotsitewise.html)   
The following property is no longer required: `PropertyValue`\.  | May 26, 2022 | 
| [Updated resource](AWS_Transfer.md) | The following resource was updated: 

 [AWS::Transfer::Server ProtocolDetails](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-transfer-server-protocoldetails.html)   
Use the `SetStatOption` to ignore the error that is generated when the client attempts to use SETSTAT on a file you are uploading to an S3 bucket\.  | May 26, 2022 | 
| [New resource](AWS_EMRServerless.md) | The following resource was added: AWS::EMRServerless::Application\. 

 [AWS::EMRServerless::Application](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-emrserverless-application.html)   
Use the `AWS::EMRServerless::Application` resource to specify an EMR Serverless application\.  | May 26, 2022 | 
| [New resources](AWS_IoTWireless.md) | The following resources were added: AWS::IoTWireless::NetworkAnalyzerConfiguration 

 [AWS::IoTWireless::NetworkAnalyzerConfiguration](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-iotwireless-networkanalyzerconfiguration.html)   
 Gets information about a network analyzer configuration\.   | May 25, 2022 | 
| [Updated resource](AWS_Cognito.md) | The following resource was updated: AWS::Cognito::UserPoolClient 

 [AWS::Cognito::UserPoolClient](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-cognito-userpoolclient.html)   
The `EnablePropagateAdditionalUserContextData` property of a user pool client makes it possible to pass IP address information to advanced security features with unauthenticated API requests\.  | May 20, 2022 | 
| [Updated resources](AWS_AppMesh.md) | The following resources were updated: AWS::AppMesh::VirtualNode and AWS::AppMesh::Mesh 

 [AWS::AppMesh::VirtualNode](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-appmesh-virtualnode.html)   
Use the `DnsServiceDiscovery` property to represent the DNS service discovery information for your virtual node\.  
Use the `AwsCloudMapServiceDiscovery` property to represent the AWS Cloud Map service discovery information for your virtual node\. 

 [AWS::AppMesh::Mesh](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-appmesh-mesh.html)   
Use the `MeshServiceDiscovery` resource to represent the service discovery information for a service mesh\.  | May 19, 2022 | 
| [Updated resources](AWS_Lightsail.md) | The following resources were updated: AWS::Lightsail::LoadBalancer and AWS::Lightsail::LoadBalancerTlsCertificate 

 [AWS::Lightsail::LoadBalancer](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-lightsail-loadbalancer.html)   
Use the `tlsPolicyName` property to specify a TLS security policy for the load balancer\. 

 [AWS::Lightsail::LoadBalancerTlsCertificate](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-lightsail-loadbalancertlscertificate.html)   
Use the `httpsRedirectionEnabled` property to indicate whether HTTPS redirection is enabled for the load balancer that the TLS certificate is attached to\.  | May 19, 2022 | 
| [Updated resource](AWS_Synthetics.md) | The following resource was updated: AWS::Synthetics::Canary\. 

 [AWS::Synthetics::Canary](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-synthetics-canary.html)   
The `DeleteLambdaResourcesOnCanaryDeletion` parameter was added\. You can specify this parameter when you create or update a canary to have the canary's Lambda resources deleted when the canary is deleted\.  | May 12, 2022 | 
| [Updated resource](AWS_DataSync.md) | The following resource was updated: AWS::DataSync::Task\. 

[AWS::DataSync::Task](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-datasync-task-options.html)  
In the `Options` property type, use the `ObjectTags` property to specify whether object tags are maintained when transferring between object storage systems\.  | May 12, 2022 | 
| [New resource](AWS_IoT.md) | The following resource was added: AWS::IoT::RoleAlias 

 [AWS::IoT::RoleAlias](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-iot-rolealias.html)   
Use the `AWS::IoT::RoleAlias`to specify a role alias\.  | May 12, 2022 | 
| [New resources](AWS_NetworkManager.md) | New resources were added to Network Manager: AWS::NetworkManager::CoreNetwork, AWS::NetworkManager::ConnectAttachment, AWS::NetworkManager::ConnectPeer, AWS::NetworkManager::SiteToSiteVpnAttachment, and AWS::NetworkManager::VpcAttachment\.  

 [AWS::NetworkManager::CoreNetwork](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-networkmanager-corenetwork.html)   
Use the `AWS::NetworkManager::CoreNetwork` to create a core network\. 

 [AWS::NetworkManager::ConnectAttachment](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-networkmanager-connectattachment.html)   
Use the `AWS::NetworkManager::CoreNetwork.ConnectAttachment` to create a Connect attachment\. 

 [AWS::NetworkManager::ConnectPeer](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-networkmanager-connectpeer.html)   
Use the `AWS::NetworkManager::ConnectPeer` to create a Connect peer attachment\. 

 [AWS::NetworkManager::SiteToSiteVpnAttachment](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-networkmanager-sitetositevpnattachment.html)   
Use the `AWS::NetworkManager::SiteToSiteVpnAttachment` to create a site\-to\-site VPN attachment\. 

 [AWS::NetworkManager::VpcAttachment](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-networkmanager-vpcattachment.html)   
Use the `AWS::NetworkManager::VpcAttachment` to create a VPC attachment\.  | May 11, 2022 | 
| [Updated resources](AWS_WAFv2.md) | The following resources were updated: AWS::WAFv2::WebACL and AWS::WAFv2::RuleGroup\. 

 [AWS::WAFv2::WebACL](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-wafv2-webacl.html)   
Use the `Cookies` property to specify that a rule statement should inspect the cookies in web requests\.   
Use the `CookieMatchPattern` property to specify a subset of all cookies for inspection\.   
Use the `Headers` property to specify that a rule statement should inspect the headers in web requests\.   
Use the `HeaderMatchPattern` property to specify a subset of all headers for inspection\.   
In the [Body](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-wafv2-webacl-body.html) property type, use the `OversizeHandling` property to specify how to handle web requests that have oversize body contents\.   
In the [JsonBody](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-wafv2-webacl-jsonbody.html) property type, use the `OversizeHandling` property to specify how to handle web requests that have oversize body contents\.  

 [AWS::WAFv2::RuleGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-wafv2-rulegroup.html)   
Use the `Cookies` property to specify that a rule statement should inspect the cookies in web requests\.   
Use the `CookieMatchPattern` property to specify a subset of all cookies for inspection\.   
Use the `Headers` property to specify that a rule statement should inspect the headers in web requests\.   
Use the `HeaderMatchPattern` property to specify a subset of all headers for inspection\.   
In the [Body](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-wafv2-rulegroup-body.html) property type, use the `OversizeHandling` property to specify how to handle web requests that have oversize body contents\.   
In the [JsonBody](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-wafv2-rulegroup-jsonbody.html) property type, use the `OversizeHandling` property to specify how to handle web requests that have oversize body contents\.   | May 5, 2022 | 
| [New resource](AWS_Rekognition.md) | The following resource was added: AWS::Rekognition::StreamProcessor\. 

 [AWS::Rekognition::StreamProcessor](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/AWS_Rekognition.html)   
The `AWS::Rekognition::StreamProcessor` type creates a stream processor used to detect and recognize faces or to detect connected home labels in a streaming video\.  | May 5, 2022 | 
| [New resource](AWS_VoiceID.md) | The following resources were added: AWS::VoiceID::Domain 

 [AWS::VoiceID::Domain](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-voiceid-domain.html)   
Use the `AWS::VoiceID::Domain` resource to create a Voice ID domain\.  | May 5, 2022 | 
| [New resource](AWS_EC2.md) | The following resource was added: AWS::EC2::KeyPair\. 

 [AWS::EC2::KeyPair](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-keypair.html)   
Use the `KeyPair` resource to create or import a key pair\.  | April 28, 2022 | 
| [Updated resources](AWS_Batch.md) | The following resource was updated: [AWS::Batch::ComputeEnvironment](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-batch-computeenvironment.html) 

 [AWS::Batch::ComputeEnvironment](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-batch-computeenvironment.html)   
Use the `ReplaceComputeEnvironment` property to specify whether the compute environment should be replaced if an update is made that requires replacing the instances in the compute environment\.  
Use the `UpdatePolicy` property to specify the infrastructure update policy for the compute environment\. 

 [AWS::Batch::JobDefinition](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-batch-jobdefinition.html)   
Added a `JobQueueArn` attribute to the [return values](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-batch-jobqueue.html#aws-resource-batch-jobqueue-return-values)\.  | April 21, 2022 | 
| [Updated resource](AWS_Evidently.md) | New parameters were added to AWS::Evidently::Experiment and AWS::Evidently::Launch 

 [Evidently resource type reference](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/AWS_Evidently.html)   
New parameters were added to [ AWS::Evidently::Experiment](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-evidently-experiment.html) and [ AWS::Evidently::Launch](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-evidently-launch.html) to allow you to use AWS CloudFormation to start and stop experiments and launches\.  | April 21, 2022 | 
| [New resources ](AWS_IoTTwinMaker.md) | The following resources were added: AWS::IoTTwinMaker::ComponentType, AWS::IoTTwinMaker::Entity, AWS::IoTTwinMaker::Scene, and AWS::IoTTwinMaker::Workspace 

 [ AWS::IoTTwinMaker::ComponentType](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-iottwinmaker-componenttype.html)   
Use the `AWS::IoTTwinMaker::ComponentType` resource to declare a component type\. 

 [ AWS::IoTTwinMaker::Entity](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-iottwinmaker-entity.html)   
Use the `AWS::IoTTwinMaker::Entity` resource to declare an entity\. 

 [AWS::IoTTwinMaker::Scene](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-iottwinmaker-scene.html)   
Use the `AWS::IoTTwinMaker::Scene` resource to declare a scene\. 

 [CFNResource](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-iottwinmaker-workspace.html)   
Use the `AWS::IoTTwinMaker::Workspace` resource to declare a workspace\.  | April 21, 2022 | 
| [New resource](AWS_Connect.md) | The following resources were added: AWS::Connect::PhoneNumber 

 [AWS::Connect::PhoneNumber](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-connect-phonenumber.html)   
Use the `AWS::Connect::PhoneNumber` resource to create a phone number\.  | April 21, 2022 | 
| [Updated resource](AWS_KMS.md) | The following resource was updated: `AWS::KMS::Key`\. 

 [AWS::KMS::Key](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-kms-key.html)   
Added support for HMAC KMS keys, including new HMAC values for the `KeySpec` property and the `GENERATE_VERIFY_MAC` value for the `KeyUsage` property\. You can also use the `AWS::KMS::ReplicaKey` resource to create a replica of a multi\-Region HMAC key\. However, the properties of this resource did not change\. | April 19, 2022 | 
| [Updated resources](AWS_AppStream.md) | The following resources were updated: `AWS::AppStream::Fleet` 

 [AWS::AppStream::Fleet](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-appstream-fleet.html)   
Use the `SessionScriptS3Location` property to specify the S3 location of the session scripts configuration zip file\. This only applies to Elastic fleets\.  | April 14, 2022 | 
| [Updated resource](AWS_CloudWatch.md) | The following resource was updated: AWS::CloudWatch::MetricStream\. 

 [AWS::CloudWatch::MetricStream](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-metricstream.html)   
In the [MetricStream](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-cloudwatch-alarm-metricstream.html) resource, use the `MetricStreamStatisticsConfiguration` to have the metric stream include additional statistics such as percentile statistics in the stream\.  | April 14, 2022 | 
| [Updated resource](AWS_AppRunner.md) | The following resource was updated: AWS::AppRunner::Service 

 [AWS::AppRunner::Service\.ObservabilityConfiguration](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-apprunner-service.html#cfn-apprunner-service-observabilityconfiguration)   
New property\. The observability configuration of the App Runner service\.  | April 12, 2022 | 
| [New resource](AWS_AppRunner.md) | The following resource was added: AWS::AppRunner::ObservabilityConfiguration 

 [AWS::AppRunner::ObservabilityConfiguration](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-apprunner-observabilityconfiguration.html)   
Use the `AWS::AppRunner::ObservabilityConfiguration` resource to create or update an AWS App Runner observability configuration\.  | April 12, 2022 | 
| [Updated resources](AWS_EC2.md) | The following resource was updated: AWS::EC2::LaunchTemplate\. 

 [AWS::EC2::LaunchTemplate NetworkInterface](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ec2-launchtemplate-networkinterface.html)   
Use the `Ipv4PrefixCount` or `Ipv4Prefixes` properties to assign IPv4 prefixes to a network interface\.  
Use the `Ipv6PrefixCount` or `Ipv6Prefixes` properties to assign IPv6 prefixes to a network interface\.  | April 7, 2022 | 
| [New resource](AWS_Events.md) | The following resource was added: [AWS::Events::Endpoint](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-events-endpoint.html)\. 

 [AWS::Events::Endpoint](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-events-endpoint.html)   
Use the `AWS::Events::Endpoint` resource to create a Amazon EventBridge global endpoint and mae your application Regional\-fault tolerant\.  | April 7, 2022 | 
| [New resource](AWS_Lambda.md) | The following resource was added: AWS::Lambda::Url\. 

 [AWS::Lambda::Url](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-lambda-url.html)   
 Use the `Url` resource to add a function URL endpoint to your Lambda function\.   | April 7, 2022 | 
| [Updated resource](AWS_SageMaker.md) | The following resources were updated: AWS::SageMaker::Domain, AWS::SageMaker::UserProfile 

 [AWS::SageMaker::Domain](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-sagemaker-domain.html)   
Use the `UserSettings.RStudioServerProAppSettings` property to configure user interaction with the `RStudioServerPro` app\.  
Use the `RStudioServerProAppSettings` property to configure user interaction with the `RStudioServerPro` app\.  
Use the `RStudioServerProAppSettings.AccessStatus` property to indicate whether the current user has access to the `RStudioServerPro` app\.  
Use the `RStudioServerProAppSettings.UserGroup` property to indicate the level of permissions that the user has within the `RStudioServerPro` app\.  
Use the `RStudioServerProDomainSettings` property to configure the `RStudioServerPro` Domain\-level app\.  
Use the `RStudioServerProDomainSettings.DefaultResourceSpec` property to define the default `InstanceType`, `SageMakerImageArn` and `SageMakerImageVersionArn` for the Domain\.  
Use the `RStudioServerProDomainSettings.DomainExecutionRoleArn` property to indicate the ARN of the execution role for the `RStudioServerPro` Domain\-level app\.  
Use the `RStudioServerProDomainSettings.RStudioConnectUrl` property to indicate a URL pointing to an RStudio Connect server\.  
Use the `RStudioServerProDomainSettings.RStudioPackageManagerUrl` property to indicate a URL pointing to an RStudio Package Manager server\.  
Use the `DomainSettings` property to indicate a collection of settings that apply to the `SageMaker Domain`\.  
Use the `DomainSettings.RStudioServerProDomainSettings` property to configure the `RStudioServerPro` Domain\-level app\.  
Use the `DomainSettings.SecurityGroupIds` property to indicate security groups for the Amazon Virtual Private Cloud \(Amazon VPC\) that the `Domain` uses for communication between Domain\-level apps and user apps\. 

 [AWS::SageMaker::UserProfile](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-sagemaker-userprofile.html.html)   
Use the `UserSettings.RStudioServerProAppSettings` property to configure user interaction with the `RStudioServerPro` app\.  
Use the `RStudioServerProAppSettings` property to configure user interaction with the `RStudioServerPro` app\.  
Use the `RStudioServerProAppSettings.AccessStatus` property to indicate whether the current user has access to the `RStudioServerPro` app\.  
Use the `RStudioServerProAppSettings.UserGroup` property to indicate the level of permissions that the user has within the `RStudioServerPro` app\.  | March 31, 2022 | 
| [New resource](AWS_DataSync.md) | The following resource was added: AWS::DataSync::LocationFSxOpenZFS\. 

[AWS::DataSync::LocationFSxOpenZFS](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-datasync-locationfsxopenzfs.html)  
Use the `AWS::DataSync::LocationFSxOpenZFS` resource to specify an Amazon FSx for OpenZFS file system\.  | March 31, 2022 | 
| [Updated resource](AWS_Lambda.md) | The following resource was updated: AWS::Lambda::Function\. 

 [AWS::Lambda::Function](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-lambda-function.html)   
Use the `EphemeralStorage` property to set the function's ephemeral \(/tmp\) storage to any any whole number between 512 and 10240 MB\.  | March 24, 2022 | 
| [Updated resource](AWS_Lex.md) | The following property type was updated: AWS::Lex::Bot\. 

[AWS::Lex::Bot](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-lex-bot.html)  
Use the [AudioLogSetting](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-lex-bot-audiologsetting.html) property to configure logging of audio conversation with your users\.  
Use the [AudioLogSetting](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-lex-bot-botaliaslocalesettings.html) property to configure the Lambda functions used for each of your bot's locales\.  
Use the [ConversationLogsSettings](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-lex-bot-conversationlogsettings.html) property to manage logging that saves audio, text, and metadata of the conversations with your users\.  
Use the [CustomVocabulary](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-lex-bot-customvocabulary.html) property to define custom vocabularies for your slot types\.  
Use the [LambdaCodeHook](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-lex-bot-lambdacodehook.html) property to specify a Lambda function that verifies requests to the bot or fulfills the user's request\.  
Use the [S3BucketLogDestination](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-lex-bot-s3bucketlogdestination.html) property to configure the Amazon S3 bucket to hold audio conversation logs\.  
Use the [SlotValueSelectionSetting](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-lex-bot-slotvalueselectionsetting.html) property to configure advanced settings for recognizing slot values\.  
Use the [TestBotAliasSettings](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-lex-bot-testbotaliassettings.html) property to configure the alias used for testing a bot\.  
Use the [TextLogSetting](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-lex-bot-textlogsetting.html) property to configure text logs for conversations\.  | March 24, 2022 | 
| [New resource](AWS_IoTEvents.md) | The following resource was added: AWS::IoTEvents::AlarmModel\. 

 [ AWS::IoTEvents::AlarmModel](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-iotevents-alarmmodel.html)   
Use the `AlarmModel` resource to monitor an AWS IoT Events input attribute\.  | March 24, 2022 | 
| [Updated resource](AWS_ACMPCA.md) | The following resources were updated: AWS::ACMPCA::Certificate and AWS::ACMPCA::CertificateAuthority\. 

 [AWS::ACMPCA::Certificate](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-acmpca-certificate.html)   
Use the `CustomAttribute` object to \.  
Use the `CustomExtension` object to \. 

 [AWS::ACMPCA::CertificateAuthority](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-acmpca-certificateauthority.html)   
Use the `CustomAttribute` object to \.  | March 17, 2022 | 
| [Updated resource](AWS_FSx.md) | The following resource was updated: AWS::FSx::Filesystem 

[AWS::FSx::Filesystem](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-fsx-filesystem.html)  
FSx for OpenZFS file system root volumes now support the LZ4 `DataCompressionType`\.  | March 17, 2022 | 
| [Updated resource](AWS_FSx.md) | The following resource was updated: AWS::FSx::Volume 

[AWS::FSx::Volume](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-fsx-volume.html)  
FSx for OpenZFS volumes now support the LZ4 `DataCompressionType`\.  | March 17, 2022 | 
| [Updated resource](AWS_FSx.md) | The following resource was updated: AWS::FSx::Volume 

[AWS::FSx::Volume](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-fsx-volume.html)  
FSx for OpenZFS volumes now support using the value `0` to un\-set the `StorageCapacityQuotaGiB` for a volume\.  | March 17, 2022 | 
| [Updated resource](AWS_FSx.md) | The following resource was updated: AWS::FSx::Volume 

[AWS::FSx::Volume](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-fsx-volume.html)  
FSx for OpenZFS volumes now support using the value `0` to un\-set the `StorageCapacityReservationGiB` for a volume\.  | March 17, 2022 | 
| [Updated resource](AWS_FSx.md) | The following resource was updated: AWS::FSx::Volume 

[AWS::FSx::Volume](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-fsx-volume.html)  
FSx for OpenZFS volumes now support setting the suggested block size for a volume\.  | March 17, 2022 | 
| [Updated resource](AWS_FSx.md) | The following resource was updated: AWS::FSx::Filesystem 

[AWS::FSx::FileSystem](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-fsx-filesystem.html)  
FSx for ONTAP file systems now support lower ThroughputCapacity settings\.  | March 17, 2022 | 
| [Updated resource](AWS_FIS.md) | The following resource was updated: AWS::FIS::ExperimentTemplate\. 

 [AWS::FIS::ExperimentTemplate](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-fis-experimenttemplate.html)   
Use the `LogConfiguration` property to configure experiment logging\.  
Use the `Parameters` property to specify criteria used to identify target resources\.  | March 11, 2022 | 
| [Updated resource](AWS_AutoScaling.md) | The following resource was updated: AWS::AutoScaling::ScalingPolicy\. 

 [AWS::AutoScaling::ScalingPolicy](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-as-policy.html)   
Use the `AWS::AutoScaling::ScalingPolicy` property to specify custom metrics when you create predictive scaling policies\. You can also use metric math to further customize the metrics that you include in your policy\.  | March 10, 2022 | 
| [New resources](AWS_Personalize.md) | The following resources were added: `AWS::Personalize::Dataset`, `AWS::Personalize::Dataset DatasetImportJob`, `AWS::Personalize::DatasetGroup`, `AWS::Personalize::Schema`, `AWS::Personalize::Solution`, and `AWS::Personalize::Solution SolutionConfig`\. 

 [AWS::Personalize::Dataset](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-personalize-dataset.html)   
Use the `AWS::Personalize::Dataset` resource to specify a dataset in Amazon Personalize\. 

 [AWS::Personalize::Dataset DatasetImportJob](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-personalize-dataset-datasetimportjob.html)   
Use the `AWS::Personalize::Dataset DatasetImportJob` resource to specify a dataset import job in Amazon Personalize\. 

 [AWS::Personalize::DatasetGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-personalize-datasetgroup.html)   
Use the `AWS::Personalize::DatasetGroup` resource to specify a dataset group in Amazon Personalize\. 

 [AWS::Personalize::Schema](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-personalize-schema.html)   
Use the `AWS::Personalize::Schema` resource to specify a schema in Amazon Personalize\. 

 [AWS::Personalize::Solution](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-personalize-solution.html)   
Use the `AWS::Personalize::Solution` resource to specify a solution in Amazon Personalize\. 

 [AWS::Personalize::Solution SolutionConfig](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-personalize-solution-solutionconfig.html)   
Use the `AWS::Personalize::Solution SolutionConfig` resource to specify a solution configuration in Amazon Personalize\.  | March 10, 2022 | 
| [New resource](AWS_EKS.md) | The following resource was added: `AWS::EKS::IdentityProviderConfig` 

 [https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-eks-identityproviderconfig.html](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-eks-identityproviderconfig.html)   
Use the `OidcIdentityProviderConfig` property to specify an identity provider config and `RequiredClaim` to specify required claims\.  | March 7, 2022 | 
| [Updated resources](AWS_DataBrew.md) | The following resources were updated: AWS::DataBrew::Job 

 [AWS::DataBrew::Job](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-databrew-job-output.html)   
Add MaxOutputFiles parameter to the Output data type to specify the maximum number of files to be generated by a profile job and written to the output folder\.  | March 3, 2022 | 
| [Added resource](AWS_ManagedBlockchain.md) | The following resource was added: AWS::ManagedBlockchain::Accessor 

 [AWS::ManagedBlockchain::Accessor](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-managedblockchain-accessor.html)   
Use the `Accessor` to create a new accessor for use with Managed Blockchain Ethereum nodes\.  | March 2, 2022 | 
| [Updated resources](AWS_Batch.md) | The following resources were updated: [AWS::Batch::ComputeEnvironment](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-batch-computeenvironment.html), and [AWS::Batch::JobQueue](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-batch-jobqueue.html) 

 [AWS::Batch::ComputeEnvironment](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-batch-computeenvironment.html)   
Added a `ComputeEnvironmentArn` attribute to the [return values](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-batch-computeenvironment.html#aws-resource-batch-computeenvironment-return-values)\. 

 [AWS::Batch::JobQueue](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-batch-jobqueue.html)   
Added a `JobQueueArn` attribute to the [return values](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-batch-jobqueue.html#aws-resource-batch-jobqueue-return-values)\.  | February 24, 2022 | 
| [Updated resource](AWS_AutoScaling.md) | The following resource was updated: AWS::AutoScaling::WarmPool\. 

 [AWS::AutoScaling::WarmPool](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-autoscaling-warmpool.html)   
Use the `PoolState` property to specify `Hibernated` to stop instances in a warm pool without deleting their RAM contents\. Use the `InstanceReusePolicy` property to return instances to the warm pool on scale in, instead of always terminating instance capacity that you will need later\.  | February 24, 2022 | 
| [Updated resource](AWS_Transfer.md) | The following resource was updated: 

 [AWS::Transfer::Server](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-transfer-server.html)   
Use the `PreAuthenticationLoginBanner` property to specify a string to display when users connect to a server, before they authenticate\.  
Use the `PostAuthenticationLoginBanner` property to specify a string to display when users connect to a server, after they authenticate\.  | February 24, 2022 | 
| [New resource](AWS_DataSync.md) | The following resource was added: AWS::DataSync::LocationFSxLustre\. 

[AWS::DataSync::LocationFSxLustre](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-datasync-locationfsxlustre.html)  
Use the `AWS::DataSync::LocationFSxLustre` resource to specify an Amazon FSx for Lustre file system\.  | February 24, 2022 | 
| [New resource](AWS_MSK.md) | The following resource was added: AWS::MSK::BatchScramSecret 

 [AWS::MSK::BatchScramSecret](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-msk-batchscramsecret.html)   
This resource represents a secret stored in the Amazon Secrets Manager that can be used to authenticate with a cluster using a user name and a password\.  | February 24, 2022 | 
| [New resource](AWS_MSK.md) | The following resource was added: AWS::MSK::Configuration 

 [AWS::MSK::Configuration](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-msk-configuration.html)   
Represents an MSK configuration\.  | February 24, 2022 | 
| [Updated resource](AWS_WAFv2.md) | The following resource was updated: AWS::WAFv2::WebACL\. 

 [AWS::WAFv2::WebACL](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-wafv2-webacl.html)   
You can now define `ManagedRuleGroupConfigs` for a `ManagedRuleGroupStatement`, to provide configuration specific to the managed rule group\. This is required to use the managed rule group, `AWSManagedRulesATPRuleSet`\.  | February 17, 2022 | 
| [New resources](AWS_NetworkManager.md) | The following new resources were added to Network Manager: AWS::NetworkManager::ConnectAttachment, AWS::NetworkManager::ConnectPeer, AWS::NetworkManager::CoreNetwork, AWS::NetworkManager::SiteToSiteVPNAttachment, and AWS::NetworkManager::VPCAttachment\. 

 [AWS::NetworkManager::ConnectAttachment](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-networkmanager-connectattachment.html)   
Use the `AWS::NetworkManager::ConnectAttachment` to create a core network Connect attachment\. 

 [AWS::NetworkManager::ConnectPeer](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-networkmanager-connectpeer.html)   
Use the `AWS::NetworkManager::ConnectPeer` create a core network Connect Peer attachment\. 

 [AWS::NetworkManager::CoreNetwork](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-networkmanager-corenetwork.html)   
Use the `AWS::NetworkManager::CoreNetwork` to create a core network\. 

 [AWS::NetworkManager::SiteToSiteVPNAttachment](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-networkmanager-sitetositevpnattachment.html)   
Use the `AWS::NetworkManager::SiteToSiteVPNAttachment` create a core network site\-to\-site VPN attachment\. 

 [AWS::NetworkManager::VPCAttachment](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-networkmanager-vpcattachment.html)   
Use the `AWS::NetworkManager::VPCAttachment` create a core network VPC attachment\.  | February 17, 2022 | 
| [Updated resources](AWS_EC2.md) | The following resource was updated: AWS::EC2::LaunchTemplate\. 

 [AWS::EC2::LaunchTemplate PrivateDnsNameOptions](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ec2-launchtemplate-launchtemplatedata-privatednsnameoptions.html)   
Use the `PrivateDnsNameOptions` property to set options for instance hostnames\. 

 [AWS::EC2::LaunchTemplate MetadataOptions](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ec2-launchtemplate-launchtemplatedata-metadataoptions.html#cfn-ec2-launchtemplate-launchtemplatedata-metadataoptions-instancemetadatatags)   
Use the `InstanceMetadataTags` property to allow access to instance tags from the instance metadata\.  | February 10, 2022 | 
| [New resources](AWS_CloudFormation.md) | The following resources were added: AWS::CloudFormation::HookDefaultVersion, AWS::CloudFormation::HookTypeConfig, and AWS::CloudFormation::HookVersion\. 

 [AWS::CloudFormation::HookDefaultVersion](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-cloudformation-hookdefaultversion.html)   
Use the `AWS::CloudFormation::HookDefaultVersion` resource to specify the default version of the hook\. 

 [AWS::CloudFormation::HookTypeConfig](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-cloudformation-hooktypeconfig.html)   
Use the `AWS::CloudFormation::HookTypeConfig` resource to specify the configuration of a hook\. 

 [AWS::CloudFormation::HookVersion](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-cloudformation-hookversion.html)   
Use the `AWS::CloudFormation::HookVersion` resource to publish the hook version in the AWS CloudFormation registry\.  | February 10, 2022 | 
| [New resources](AWS_ECR.md) | The following resources were added: AWS::ECR::PullThroughCacheRule 

 [AWS::ECR::PullThroughCacheRule](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ecr-pullthroughcacherule.html)   
Use the `AWS::ECR::PullThroughCacheRule` property to create a pull through cache rule for your private registry\. Pull through cache rules provide a way to cache images from an external public registry in your private registry  | February 10, 2022 | 
| [CloudFormation registry](#ReleaseHistory) | AWS CloudFormation announces the general availability of *hooks*, a feature that allows customers to invoke custom logic to automate actions or inspect resource configurations prior to a create, update or delete stack operation\.For more information, see [Developing hooks](https://docs.aws.amazon.com/cloudformation-cli/latest/userguide/hooks.html) in the *User Guide for Extension Development*\. | February 10, 2022 | 
| [Updated resource](AWS_AppRunner.md) | The following resource was updated: AWS::AppRunner::Service 

 [AWS::AppRunner::Service\.NetworkConfiguration](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-apprunner-service.html#cfn-apprunner-service-networkconfiguration)   
New property\. Configuration settings related to network traffic of the web application that the App Runner service runs\.  | February 8, 2022 | 
| [New resource](AWS_AppRunner.md) | The following resource was added: AWS::AppRunner::VpcConnector 

 [AWS::AppRunner::VpcConnector](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-apprunner-vpcconnector.html)   
Use the `AWS::AppRunner::VpcConnector` resource to create or update an AWS App Runner VPC connector\.  | February 8, 2022 | 
| [Updated resource](AWS_Events.md) | The following resource was updated: [AWS::Events::Rule](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-events-rule.html)\. 

 [AWS::Events::Rule](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-events-rule.html)   
The [Rule\.SageMakerPipelineParameter\.PipelineParameterList](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-events-rule-sagemakerpipelineparameter.html#cfn-events-rule-sagemakerpipelineparameters-pipelineparameterlist) is a list of parameter names and values for SageMaker Model Building Pipeline execution\.  
The [Rule\.SageMakerPipelineParameter\.Name](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-events-rule-sagemakerpipelineparameters.html#cfn-events-rule-sagemakerpipelineparameter-name) is the name of parameter to start execution of a SageMaker Model Building Pipeline\.  
The [Rule\.SageMakerPipelineParameter\.Value](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-events-rule-sagemakerpipelineparameters.html#cfn-events-rule-sagemakerpipelineparameter-value) is the value of parameter to start execution of a SageMaker Model Building Pipeline\.  | February 3, 2022 | 
| [New properties](AWS_ApplicationInsights.md) | The following properties were added under [AWS::ApplicationInsights::Application\.ConfigurationDetails](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-applicationinsights-application-configurationdetails.html):  

 [HANAPrometheusExporter](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-applicationinsights-application-configurationdetails.html#aws-properties-applicationinsights-application-configurationdetails-properties)   
Use the `HANAPrometheusExporter` property of the `AWS::ApplicationInsights::Application` resource to define the HANA DB Prometheus Exporter settings\. 

[HAClusterPrometheusExporter](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-applicationinsights-application-configurationdetails.html#aws-properties-applicationinsights-application-configurationdetails-properties)  
Use the `HAClusterPrometheusExporter` property of the `AWS::ApplicationInsights::Application` resource to define the HA Cluster Prometheus Exporter settings\.  | February 3, 2022 | 
| [Updated resource](AWS_SecretsManager.md) | The following resource was updated: `RotationRules` 

[AWS::SecretsManager::RotationSchedule RotationRules](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-secretsmanager-rotationschedule-rotationrules.html)  
Use `RotationRules` to set a detailed schedule to rotate your secret\.   | January 31, 2022 | 
| [Updated resources](AWS_CustomerProfiles.md) | The following resource was updated: AWS::CustomerProfiles::Integration\. 

 [AWS::CustomerProfiles::Integration](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-customerprofiles-integration.html)  
Use the `AWS::CustomerProfiles::Integration` resource to create a new integration in Amazon Connect Customer Profiles Service\.  | January 27, 2022 | 
| [Updated resources](AWS_Location.md) | The following resources were updated: `AWS::Location::GeofenceCollection`, `AWS::Location::Map`, `AWS::Location::PlaceIndex`, `AWS::Location::RouteCalculator`, and `AWS::Location::Tracker`\. 

 [AWS::Location::GeofenceCollection](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-location-geofencecollection.html)   
Updated the `AWS::Location::GeofenceCollection` resource to no longer use `PricingPlan` or `PricingPlanDataSource`\. 

 [AWS::Location::Map](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-location-map.html)   
Updated the `AWS::Location::Map` resource to no longer use `PricingPlan`\. 

 [AWS::Location::PlaceIndex](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-location-placeindex.html)   
Updated the `AWS::Location::PlaceIndex` resource to no longer use `PricingPlan`\. 

 [AWS::Location::RouteCalculator](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-location-routecalculator.html)   
Update the `AWS::Location::RouteCalculator` resource to no longer use `PricingPlan`\. 

 [AWS::Location::Tracker](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-location-tracker.html)   
Update the `AWS::Location::Tracker` resource to no longer use `PricingPlan` or `PricingPlanDataSource`\.  | January 27, 2022 | 
| [Updated resource](AWS_IVS.md) | The following resource was updated: AWS::IVS::RecordingConfiguration 

 [AWS::IVS::RecordingConfiguration](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ivs-recordingconfiguration.html)   
Use the `ThumbnailConfiguration` property to specify an Amazon IVS ThumbnailConfiguration, which stores configuration information related to generating thumbnail images for your live stream\.  | January 27, 2022 | 
| [New resource](AWS_AppIntegrations.md) | The following resource was added: AWS::AppIntegrations::DataIntegration 

 [AWS::AppIntegrations::DataIntegration](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-appintegrations-dataintegration.html)   
Use the `AWS::AppIntegrations::DataIntegration` resource to create a DataIntegration\.  | January 27, 2022 | 
| [New collection resource](AWS_Rekognition.md) | The following resource was added: AWS::Rekognition::Collection\. 

 [AWS::Rekognition::Collection](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/AWS_Rekognition.html)   
The `AWS::Rekognition::Collection` type creates a server\-side container called a collection\. You can use a collection to store information about detected faces and search for known faces in images, stored videos, and streaming videos\.  | January 27, 2022 | 
| [New resources](AWS_Forecast.md) | The following resources were added: AWS::Forecast::Dataset and AWS::Forecast::DatasetGroup\. 

 [AWS::Forecast::Dataset](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-forecast-dataset.html)   
Use the `AWS::Forecast::Dataset` resource to import a new or updated dataset in Amazon Forecast\. 

 [AWS::Forecast::DatasetGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-forecast-datasetgroup.html)   
Use the `AWS::Forecast::DatasetGroup` resource to create a Dataset Group in Amazon Forecast\.  | January 23, 2022 | 
| [Updated resources](AWS_DataBrew.md) | The following resources were updated: AWS::DataBrew::Job 

 [AWS::DataBrew::Job](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-databrew-job-s3location.html)   
Add BucketOwner parameter to the S3Location data type to define the owner of the specified S3 bucket\.  | January 20, 2022 | 
| [Updated resource](AWS_Location.md) | The following resources were updated: `AWS::Location::Tracker`, 

 [AWS::Location::Tracker](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-location-tracker.html)   
Added `AccuracyBased` as a new value for `PositionFiltering` for trackers\.  | January 20, 2022 | 
| [New resources](AWS_Lightsail.md) | The following resources were added: AWS::Lightsail::Certificate, AWS::Lightsail::Container, and AWS::Lightsail::Distribution 

 [AWS::Lightsail::Certificate](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-lightsail-certificate.html)   
Use the `AWS::Lightsail::Certificate` resource to specify an Amazon Lightsail certificate that you can use with a Lightsail content delivery network \(CDN\) distribution and a container service\. 

 [AWS::Lightsail::Container](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-lightsail-container.html)   
Use the `AWS::Lightsail::Container` resource to specify an Amazon Lightsail container service\. 

 [AWS::Lightsail::Distribution](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-lightsail-distribution.html)   
Use the `AWS::Lightsail::Distribution` resource to specify an Amazon Lightsail CDN distribution\.  | January 20, 2022 | 
| [New resource](AWS_KafkaConnect.md) | The following resource was added: AWS::KafkaConnect::Connector 

 [AWS::KafkaConnect::Connector](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-kafkaconnect-connector.html)   
Creates an MSK Connect connector\.  | January 20, 2022 | 
| [Updated resource](AWS_AppSync.md) | The following resources were updated: AWS::AppSync::Resolver and AWS::AppSync::FunctionConfiguration 

 [AWS::AppSync::Resolver](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-appsync-resolver.html#cfn-appsync-resolver-maxbatchsize)   
Use the `MaxBatchSize` property to specify the maximum number of resolver request inputs that will be sent to a single AWS Lambda function in a `BatchInvoke` operation\.  

 [AWS::AppSync::FunctionConfiguration](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-appsync-functionconfiguration.html#cfn-appsync-functionconfiguration-maxbatchsize)   
Use the `MaxBatchSize` property to specify the maximum number of resolver request inputs that will be sent to a single AWS Lambda function in a `BatchInvoke` operation\.   | January 13, 2022 | 
| [Updated resource](AWS_FMS.md) | The following resource was updated: AWS::FMS::Policy\. 

 [AWS::FMS::Policy](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-fms-policy.html)   
The `AWS::FMS::Policy` resource now allows you to manage Shield Advanced automatic application layer DDoS mitigation for Shield Advanced policies that you use for Amazon CloudFront distributions\.   | January 7, 2022 | 
| [Updated resource](AWS_EKS.md) | The following property was updated: `AWS::EKS::Cluster KubernetesNetworkConfig` 

 [https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-eks-cluster-kubernetesnetworkconfig.html](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-eks-cluster-kubernetesnetworkconfig.html)   
Use the `IpFamily` property to specify whether you want your version 1\.21 or later cluster to assign IPv4 or IPv6 addresses to pods and services\.  | January 6, 2022 | 
| [Updated resource](AWS_Lex.md) | The following property type was updated: AWS::Lex::Bot\. 

[AWS::Lex::Bot](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-lex-bot.html)  
In the [ExternalSourceSetting](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-lex-bot-externalsourcesetting.html) property type, use the `GrammarSlotTypeSetting` property to specify that the slot type is defined by an external grammar\.  
In the [GrammarSlotTypeSetting](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-lex-bot-grammarslottypesetting.html) property type, use the `Source` property to specify the location of a file that contains a grammar defining the slot type\.  
In the [GrammarSlotTypeSource](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-lex-bot-grammarslottypesource.html) property type, use the `KmsKeyArn`, `S3BucketName`, and `S3ObjectKey` properties to specify the S3 bucket location of a file that contains a grammar defining the slot type\.  | January 6, 2022 | 
| [New resources](AWS_Lightsail.md) | The following resources were added: AWS::Lightsail::Alarm, AWS::Lightsail::Bucket, AWS::Lightsail::LoadBalancer, and AWS::Lightsail::LoadBalancerTlsCertificate 

 [AWS::Lightsail::Alarm](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-lightsail-alarm.html)   
Use the `AWS::Lightsail::Alarm` resource to specify an Amazon Lightsail alarm\. 

 [AWS::Lightsail::Bucket](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-lightsail-bucket.html)   
Use the `AWS::Lightsail::Bucket` resource to specify an Amazon Lightsail bucket\. 

 [AWS::Lightsail::LoadBalancer](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-lightsail-loadbalancer.html)   
Use the `AWS::Lightsail::LoadBalancer` resource to specify an Amazon Lightsail load balancer\. 

 [AWS::Lightsail::LoadBalancerTlsCertificate](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-lightsail-loadbalancertlscertificate.html)   
Use the `AWS::Lightsail::LoadBalancerTlsCertificate` resource to specify a certificate that you can use with an Amazon Lightsail load balancer that is in the same AWS Region and Availability Zone\.  | January 6, 2022 | 
| [New resource](AWS_InspectorV2.md) | The following resource was added: AWS::InspectorV2::Filter\. 

 [AWS::InspectorV2::Filter](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-inspectorv2-filter.html)   
Use the `AWS::InspectorV2::Filter` resource to specify a filter\.  | January 6, 2022 | 
| [New resource](AWS_IoT.md) | The following resource is new: AWS::IoT::JobTemplate 

 [AWS::IoT::JobTemplate](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-iot-jobtemplate.html)   
Use the `AWS::IoT::JobTemplate` resource to specify a job template\.  | January 6, 2022 | 
| [New resources](AWS_AppStream.md) | The following resources were added: `AWS::AppStream::ApplicationEntitlementAssociation` and `AWS::AppStream::Entitlement` 

 [AWS::AppStream::ApplicationEntitlementAssociation](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-appstream-applicationentitlementassociation.html)   
Use the `AWS::AppStream::ApplicationEntitlementAssociation` resource to specify an association between an application and entitlement\. 

 [AWS::AppStream::Entitlement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-appstream-entitlement.html)   
Use the `AWS::AppStream::Entitlement` resource to specify an entitlement\.  | January 5, 2022 | 
| [Updated resources](AWS_WAFv2.md) | The following resources were updated: AWS::WAFv2::WebACL and AWS::WAFv2::RuleGroup\. 

 [AWS::WAFv2::WebACL](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-wafv2-webacl.html)   
You can now use single regular expression \(regex\) match statements with `RegexMatchStatement`\. You can now specify a `CAPTCHA` rule action\. 

 [AWS::WAFv2::RuleGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-wafv2-rulegroup.html)   
You can now use single regular expression \(regex\) match statements with `RegexMatchStatement`\. You can now specify a `CAPTCHA` rule action\.  | December 9, 2021 | 
| [Updated resource](AWS_Kinesis.md) | The following resource was updated: AWS::Kinesis::Stream\. 

 [AWS::Kinesis::Stream](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-kinesis-stream.html)   
Use the `StreamModeDetails` property to specify the capacity mode to which you want to set your data stream\. Currently, in Kinesis Data Streams, you can choose between an **on\-demand** capacity mode and a **provisioned** capacity mode for your data streams\.  | December 9, 2021 | 
| [Properties updated](AWS_Chatbot.md) | For the `AWS::Chatbot::SlackChannelConfiguration` resource, the GuardrailPolicies property was updated and the UserRoleRequired property was added\. 

 [AWS::Chatbot::SlackChannelConfiguration](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/AWS_Chatbot.html)   
Use the `GuardrailPolicies` property to list policy ARNs applied as channel guardrails for AWS Chatbot\. 

 [AWS::Chatbot::SlackChannelConfiguration](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/AWS_Chatbot.html)   
Use the `UserRoleRequired` property to enable the use of a user role requirement in AWS Chatbot configurations\.  | December 9, 2021 | 
| [New resources](AWS_Lex.md) | The following resources were added: AWS::Lex:Bot, AWS::Lex::BotAlias, AWS::Lex::BotVersion, and AWS::Lex::ResourcePolicy\. 

 [AWS::Lex::Bot](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-lex-bot.html)   
Use the `AWS::Lex::Bot` resource to specify an Amazon Lex chatbot\. 

 [AWS::Lex::BotAlias](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-lex-botalias.html)   
Use the `AWS::Lex::BotAlias` resource to specify an alias for an Amazon Lex chatbot\. 

 [AWS::Lex::BotVersion](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-lex-botversion.html)   
Use the `AWS::Lex::BotVersion` resource to specify a version of an Amazon Lex chatbot\. 

 [AWS::Lex::ResourcePolicy](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-lex-resourcepolicy.html)   
Use the `AWS::Lex::ResourcePolicy` resource to specify a new resource policy for an Amazon Lex chatbot\.  | December 9, 2021 | 
| [Updated resource](AWS_GameLift.md) | The following resources were updated: AWS::GameLift::GameSessionQueue, AWS::GameLift::MatchmakingConfiguration, AWS::GameLift::MatchmakingRuleSet, AWS::GameLift::Script 

 [AWS::GameLift::GameSessionQueue](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-gamelift-gamesessionqueue.html)   
Use the `Tags` property to add a list of labels to new game session queue resources\. 

 [AWS::GameLift::MatchmakingConfiguration](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-gamelift-matchmakingconfiguration.html)   
Use the `Tags` property to add a list of labels to new matchmaking configurations\. 

 [AWS::GameLift::MatchmakingRuleSet](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-gamelift-matchmakingruleset.html)   
Use the `Tags` property to add a list of labels to new matchmaking rule sets\. 

 [AWS::GameLift::Script](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-gamelift-script.html)   
Use the `Tags` property to add a list of labels to new scripts\.  | December 8, 2021 | 
| [New resources](AWS_AppSync.md) | The following resources were added: AWS::AppSync::DomainName and AWS::AppSync::DomainNameApiAssociation 

 [AWS::AppSync::DomainName](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-appsync-domainname.html)   
Use the `AWS::AppSync::DomainName` resource to specify the configuration for a custom domain\.  

 [AWS::AppSync::DomainNameApiAssociation](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-appsync-domainnameapiassociation.html)   
Use the `AWS::AppSync::DomainNameApiAssociation` property to specify the mapping of a custom domain name to an assigned API URL\.   | December 6, 2021 | 
| [Updated resources](AWS_WAFv2.md) | The following resource was updated: AWS::WAFv2::LoggingConfiguration\. 

 [AWS::WAFv2::LoggingConfiguration](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-wafv2-loggingconfiguration.html)   
You can now log web ACL traffic to an Amazon CloudWatch Logs log group or an Amazon Simple Storage Service \(Amazon S3\) bucket\. These options are in addition to the existing option of logging to an Amazon Kinesis Data Firehose\.  | December 3, 2021 | 
| [Updated resource](AWS_S3.md) | The following resource was updated: AWS::S3::StorageLens\. 

 [AWS::S3::StorageLens CloudWatchMetrics](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-s3-storagelens-cloudwatchmetrics.html)   
Use the `AWS::S3::StorageLens CloudWatchMetrics` resource to enable the Amazon CloudWatch publishing option for S3 Storage Lens metrics\.  | December 3, 2021 | 
| [Updated resource](AWS_S3.md) | The following resource was updated: AWS::S3::Bucket OwnershipControlsRule\. 

 [AWS::S3::Bucket OwnershipControlsRule](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-s3-bucket-ownershipcontrolsrule.html)   
Updated `ObjectOwnership` property to add a new allowed value: `BucketOwnerEnforced`\. You can apply this S3 Object Ownership setting to disable access control lists \(ACLs\) and take ownership of all the objects in your bucket\.  | December 3, 2021 | 
| [Updated resource](AWS_SageMaker.md) | The following resource was updated: AWS::SageMaker::EndpointConfig 

 [AWS::SageMaker::EndpointConfig](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-sagemaker-endpointconfig.html)   
Use the `ServerlessConfig` property to specify a serverless configuration for a serverless endpoint\.  
Use the `MaxConcurrency` property to specify the maximum concurrent invocations for a serverless endpoint\.  
Use the `MemorySizeInMB` property to specify the memory size \(in MB\) for a serverless endpoint\.  | December 3, 2021 | 
| [New resources](AWS_AmplifyUIBuilder.md) | The following resources were added: AWS::AmplifyUIBuilder::Component and AWS::AmplifyUIBuilder::Theme\. 

 [AWS::AmplifyUIBuilder::Component](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-amplifyuibuilder-component.html)   
Use the `AWS::AmplifyUIBuilder::Component` resource to specify a component within an Amplify app\. 

 [AWS::AmplifyUIBuilder::Theme](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-amplifyuibuilder-theme.html)   
Use the `AWS::AmplifyUIBuilder::Theme` resource to specify a collection of style settings to apply globally to the components in an Amplify app\.  | December 3, 2021 | 
| [New resources](AWS_ResilienceHub.md) | The following resources were added: 

[AWS::ResilienceHub::App](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-resiliencehub-app.html)  
Creates an AWS Resilience Hub application\. 

[AWS::ResilienceHub::ResiliencyPolicy](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-resiliencehub-resiliencypolicy.html)  
Defines a resiliency policy\.  | December 3, 2021 | 
| [New resource](AWS_Connect.md) | The following resources were added: AWS::Connect::ContactFlow and AWS::Connect::ContactFlowModule 

 [AWS::Connect::ContactFlow](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-connect-contactflow.html)   
Use the `AWS::Connect::ContactFlow` resource to create a flow\. 

 [AWS::Connect::ContactFlowModule](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-connect-contactflowmodule.html)   
Use the `AWS::Connect::ContactFlowModule` resource to create a flow module\.  | December 3, 2021 | 
| [New resource](AWS_Evidently.md) | The following resources were added: AWS::Evidently::Experiment, AWS::Evidently::Feature, AWS::Evidently::Launch, and AWS::Evidently::Project 

 [Evidently resource type reference](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/AWS_Evidently.html)   
Use Amazon CloudWatch Evidently to safely validate new features by serving them to a specified percentage of your users while you roll out the feature\. You can monitor the performance of the new feature to help you decide when to ramp up traffic to your users\. This helps you reduce risk and identify unintended consequences before you fully launch the feature\. You can also conduct A/B experiments to make feature design decisions based on evidence and data\.  
For more information, see [ Perform launches and A/B experiments with CloudWatch Evidently](https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/CloudWatch-Evidently.html)\.  | December 3, 2021 | 
| [New resource](AWS_FSx.md) | The following new resource was added: AWS::FSx::Snapshot 

[AWS::FSx::Snapshot](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-fsx-snapshot.html)  
Use the `Snapshot` resource to create a snapshot of an FSx for ONTAP or Amazon FSx for OpenZFS volume\.  | December 3, 2021 | 
| [New resource](AWS_FSx.md) | The following new resource was added: AWS::FSx::StorageVirtualMachine 

[AWS::FSx::StorageVirtualMachine](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-fsx-storagevirtualmachine.html)  
Use the `StorageVirtualMachine` resource to create an FSx for ONTAP storage virtual machine\.  | December 3, 2021 | 
| [New resource](AWS_FSx.md) | The following new resource was added: AWS::FSx::Volume 

[AWS::FSx::Volume](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-fsx-volume.html)  
Use the `Volume` resource to create an FSx for ONTAP or Amazon FSx for OpenZFS volume\.  | December 3, 2021 | 
| [New resource](AWS_RUM.md) | The following resource was added: AWS::RUM::AppMonitor\. 

 [AWS::RUM::AppMonitor](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-rum-appmonitor.html)   
Use the AWS::RUM::AppMonitor resource to create or update an Amazon CloudWatch RUM app monitor\. For more information, see [ Set up an application to use CloudWatch RUM](https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/CloudWatch-RUM-get-started.html)\.  | December 3, 2021 | 
| [New resource](AWS_Timestream.md) | The following resource was added: AWS::Timestream::ScheduledQuery\. 

 [AWS::Timestream::ScheduledQuery](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-timestream-scheduledquery.html)   
Use the `AWS::Timestream::ScheduledQuery` resource to create a new scheduled query for an existing table in Amazon Timestream\.  | December 3, 2021 | 
| [Updated resource](AWS_SES.md) | The following resource was updated: AWS::SES::ConfigurationSetEventDestination 

 [AWS::SES::ConfigurationSetEventDestination](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ses-configurationseteventdestination.html)   
Use the new property [SnsDestination](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ses-configurationseteventdestination-snsdestination.html) with the `ConfigurationSetEventDestination` resource as an event destination associated with a configuration set which enables you to publish email sending events\.  
In the property type [EventDestination](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ses-configurationseteventdestination-eventdestination.html), new property `SnsDestination` specifies the topic ARN associated with an Amazon Simple Notification Service \(Amazon SNS\) event destination\.  | November 25, 2021 | 
| [Updated resources](AWS_ElastiCache.md) | AWS::ElastiCache::ReplicationGroup\. 

 [AWS::ElastiCache::ReplicationGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-elasticache-replicationgroup.html)   
The `data-tiering-enabled` parameter enables data tiering\. Data tiering is only supported for replication groups using the r6gd node type\. If you elect not to use data\-tiering, set the parameter to `no-data-tiering-enabled.` For more information, see [Data tiering](https://docs.aws.amazon.com/AmazonElastiCache/latest/red-ug/data-tiering.html)\.  | November 23, 2021 | 
| [Updated resource](AWS_Logs.md) | The following resource was updated: AWS::Logs::LogGroup\. 

 [AWS::Logs::LogGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-logs-loggroup.html)   
The AWS::Logs::LogGroup resource now supports tags\.  | November 22, 2021 | 
| [Updated resources](AWS_AppStream.md) | The following resources were updated: `AWS::AppStream::Fleet` 

 [AWS::AppStream::Fleet](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-appstream-fleet.html)   
Use the `FleetType` property to specify an ELASTIC fleet\.  
Use the `Platform` property to specify platform of the fleet\.  
Use the `MaxConcurrentSessions` property to specify the maximum concurrent sessions of an Elastic fleet\.  
Use the `UsbDeviceFilterStrings` property to specify the USB device filter strings for an Elastic fleet\.\.  | November 18, 2021 | 
| [Updated resources](AWS_DataBrew.md) | The following resources were updated: AWS::DataBrew::Job, AWS::DataBrew::Ruleset 

 [AWS::DataBrew::Job](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-databrew-job-datacatalogoutput.html)   
Updates to support the following features: handling personally identifiable information \(PII\), data quality rules, and custom SQL queries\.   | November 18, 2021 | 
| [Updated resources](AWS_Transfer.md) | The following resources were updated: 

 [AWS::Transfer::Server](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-transfer-server.html#cfn-transfer-server-identityprovidertype)   
Use the `IdentityProviderType` resource to specify a the identity provider to use with your AWS Transfer Family server\. A new type, `LAMBDA`, was added\.  | November 18, 2021 | 
| [Updated resource](AWS_FinSpace.md) | The following resource was updated: AWS::FinSpace::Environment 

 [AWS::FinSpace::Environment](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-finspace-environment.html)   
Use the `DataBundles` property to specify a list of data bundles to install\.  
Use the `SuperuserParameters` property to specify configuration information of the superuser\.  | November 18, 2021 | 
| [Updated resource](AWS_FSx.md) | The following resource was updated: AWS::FSx::FileSystem 

[AWS::FSx::FileSystem](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-fsx-filesystem.html)  
Use ONTAP for the FileSystemType, to use an ONTAP file system\. Use `OntapConfiguration` parameter to configure an Amazon FSx ONTAP file system\.  | November 18, 2021 | 
| [Updated resource](AWS_MSK.md) | The following resource was updated: AWS::MSK::Cluster 

 [AWS::MSK::Cluster](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-msk-cluster.html)   
You can now turn on public access to an MSK cluster's brokers\.  | November 18, 2021 | 
| [New resources](AWS_AppStream.md) | The following resources were added: `AWS::AppStream::Application`, `AWS::AppStream::AppBlock`, and `AWS::AppStream::ApplicationFleetAssociation` 

 [AWS::AppStream::Application](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-appstream-application.html)   
Use the `AWS::AppStream::Application` resource to specify an application\. 

 [AWS::AppStream::AppBlock](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-appstream-appblock.html)   
Use the `AWS::AppStream::AppBlock` resource to specify an app block\. 

 [AWS::AppStream::ApplicationFleetAssociation](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-appstream-applicationfleetassociation.html)   
Use the `AWS::AppStream::ApplicationFleetAssociation` resource to specify an association between an application and fleet\.  | November 18, 2021 | 
| [New resource](AWS_FSx.md) | The following resource was updated: AWS::FSx::FileSystem 

[AWS::FSx::FileSystem](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-fsx-filesystem.html)  
Use the `FileSystemTypeVersion` attribute to specify the file system version of an Amazon FSx for Lustre file system\.  | November 18, 2021 | 
| [New resource](AWS_Transfer.md) | The following resource was added: 

 [AWS::Transfer::Workflow](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-transfer-workflow.html)   
Use the `Workflow` resource to specify a managed workflow for file processing using AWS Transfer Family\.  | November 18, 2021 | 
| [New resource](AWS_SSM.md) | The following resource was added: AWS::SSM::ResourcePolicy 

 [AWS::SSM::ResourcePolicy](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ssm-document.html)   
Creates or updates a Systems Manager resource policy\. A resource policy helps you to define the IAM entity \(for example, an AWS account\) that can manage your Systems Manager resources\. Currently, `OpsItemGroup` is the only resource that supports Systems Manager resource policies\. The resource policy for `OpsItemGroup` enables AWS accounts to view and interact with OpsCenter operational work items \(OpsItems\)\. OpsCenter is a capability of Systems Manager\. For more information about OpsCenter, see [Systems Manager OpsCenter](https://docs.aws.amazon.com/systems-manager/latest/userguide/OpsCenter.html) in the Systems Manager User Guide\.   | November 17, 2021 | 
| [Updated resource](AWS_Location.md) | The following resource was updated: AWS::Location::Tracker 

 [AWS::Location::Tracker](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-location-tracker.html)   
Use the `PositionFiltering` property to specify how you want positions in your tracker to be filtered\.  | November 12, 2021 | 
| [Updated resources](AWS_Batch.md) | The following resources were updated: [AWS::Batch::ComputeEnvironment](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-batch-computeenvironment.html), [AWS::Batch::JobDefinition](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-batch-jobdefinition.html), and [AWS::Batch::JobQueue](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-batch-jobqueue.html) 

 [AWS::Batch::ComputeEnvironment](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-batch-computeenvironment.html)   
Use the `UnmanagedvCpus` property to specify the maximum number of vCPUs for an unmanaged compute environment\. 

 [AWS::Batch::JobDefinition](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-batch-jobdefinition.html)   
Use the `SchedulingPriority` property to specify the scheduling priority for job definition\. 

 [AWS::Batch::JobQueue](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-batch-jobqueue.html)   
Use the `SchedulingPolicyArn` property to specify the scheduling policy for a job queue\.  | November 11, 2021 | 
| [Updated resources](AWS_SageMaker.md) | The following resource was updated: AWS::SageMaker::Endpoint 

 [AWS::SageMaker::Endpoint](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-sagemaker-endpoint.html)   
Use the `DeploymentConfig` property to specify the deployment configuration for an endpoint, which contains the desired deployment strategy and rollback configurations\.  
Use the `AutoRollbackConfig` property to specify the the automatic rollback configuration for handling endpoint deployment failures and recovery\.  
Use the `Alarm` property to specify a list of CloudWatch alarms that are configured to monitor metrics on an endpoint\.  
Use the `AlarmName` property to specify the name of a CloudWatch alarm in your account\.  
Use the `BlueGreenUpdatePolicy` property to specify the update policy for a blue/green deployment\.  
Use the `MaximumExecutionTimeoutInSeconds` property to specify the maximum execution timeout for a blue/green deployment\.  
Use the `TerminationWaitInSeconds` property to specify additional waiting time in seconds after the completion of an endpoint deployment before terminating the old endpoint fleet  
Use the `TrafficRoutingConfig` property to specify the traffic routing strategy during a blue/green endpoint deployment\.  
Use the `CanarySize` property to specify the batch size for the first step to turn on traffic on the new endpoint fleet\.  
Use the `LinearStepSize` property to specify the batch size for each step to turn on traffic on the new endpoint fleet  
Use the `Type` property to specify the traffic routing strategy type \(all at once, canary, or linear\)\.  
Use the `WaitIntervalInSeconds` property to specify the waiting time \(in seconds\) between incremental steps to turn on traffic on the new endpoint fleet\.  
Use the `CapacitySize` property to specify the endpoint capacity to activate for production\.  
Use the `Type` property to specify the endpoint capacity type to use \(instance count or capacity percent\)\.  
Use the `Value` property to specify the capacity size, either as a number of instances or a capacity percentage\.  
Use the `RetainDeploymentConfig` property to specify whether to reuse the last deployment configuration\. The default value is false \(the configuration is not reused\)  | November 11, 2021 | 
| [New resources](AWS_Batch.md) | The following resource was added: [AWS::Batch::SchedulingPolicy](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-batch-schedulingpolicy.html) 

 [AWS::Batch::SchedulingPolicy](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-batch-schedulingpolicy.html)   
Use the `AWS::Batch::SchedulingPriority` resource to specify a scheduling policy\.  | November 11, 2021 | 
| [New resources](AWS_IoTWireless.md) | The following resources were added: AWS::IoTWireless::FuotaTask, AWS::IoTWireless::MulticastGroup 

 [AWS::IoTWireless::FuotaTask](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-iotwireless-fuotatask.html)   
 Gets information about a FUOTA task\.  

 [AWS::IoTWireless::MulticastGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-iotwireless-taskdefinition.html)   
 Gets information about a multicast group\.   | November 11, 2021 | 
| [Updated resource](AWS_Backup.md) | The following resource was updated: AWS::Backup::BackupSelection 

 [AWS::Backup::BackupSelection](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-backup-backupselection.html)   
The `BackupSelection` resource type supports a number of new resource assignment options, including `StringLike` and the ability to exclude resources from your backup plans\.  | November 10, 2021 | 
| [Updated resource](AWS_EKS.md) | The following resource was updated: `AWS::EKS::Cluster` 

 [https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-eks-cluster-clusterlogging.html](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-eks-cluster-clusterlogging.html)   
Use the `ClusterLogging` property to specify the cluster control plane configuration for your cluster\. 

 [https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-eks-cluster-logging.html](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-eks-cluster-logging.html)   
Use the `Logging` property to enable or disable exporting the Kubernetes control plane logs for your cluster to CloudWatch Log\. 

 [https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-eks-cluster-loggingtypeconfig.html](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-eks-cluster-loggingtypeconfig.html)   
Use the `LoggingTypeConfig` property to specify the enabled logging type\. 

 [https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-eks-cluster-resourcesvpcconfig.html](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-eks-cluster-resourcesvpcconfig.html)   
Use the `EndpointPrivateAccess` property to enable or disable private access for your cluster's Kubernetes API server endpoint\.  
Use the `EndpointPublicAccess` property to enable or disable public access to your cluster's Kubernetes API server endpoint\.  
Use the `PublicAccessCidrs` property to specify the CIDR blocks that are allowed access to your cluster's public Kubernetes API server endpoint\.  | November 10, 2021 | 
| [Updated resources](AWS_EC2.md) | The following resources were updated: AWS::EC2::SpotFleet and AWS::EC2::EC2Fleet\. 

 [AWS::EC2::SpotFleet\.SpotCapacityRebalance](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ec2-spotfleet-spotcapacityrebalance.html)   
Use the `TerminationDelay` property type to specify a delay in termination of your Spot Instances that receive a rebalance notification\. 

 [AWS::EC2::EC2Fleet\.SpotOptionsRequest](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ec2-ec2fleet-spotoptionsrequest.html#cfn-ec2-ec2fleet-spotoptionsrequest-maintenancestrategies)   
Use the `MaintenanceStrategies` property type to manage your Spot Instances that are at an elevated risk of being interrupted\. 

 [AWS::EC2::EC2Fleet\.CapacityRebalance](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ec2-ec2fleet-capacityrebalance.html)   
Use the `CapacityRebalance` property to proactively augment your fleet with a new Spot Instance before a running Spot Instance is interrupted by Amazon EC2\.  | November 4, 2021 | 
| [Updated resources](AWS_NetworkFirewall.md) | The following resources were updated: AWS::NetworkFirewall::FirewallPolicy and AWS::NetworkFirewall::RuleGroup 

 [AWS::NetworkFirewall::FirewallPolicy](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-networkfirewall-firewallpolicy.html)   
Use the `StatefulDefaultActions` property to establish default actions to take on a packet that doesn't match any stateful rules when using strict rule ordering\.   
Use the `StatefulEngineOptions` property to govern how Network Firewall handles stateful rules\.  

 [AWS::NetworkFirewall::RuleGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-networkfirewall-rulegroup.html)   
Use the `StatefulRuleOptions` property to govern how Network Firewall handles stateful rules\.   | November 4, 2021 | 
| [Updated resources](AWS_Pinpoint.md) | The following resource was updated: AWS::Pinpoint::Campaign\. 

[AWS::Pinpoint::Campaign InAppMessageBodyConfig](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-pinpoint-campaign-inappmessagebodyconfig.html)  
Specifies the configuration of main body text of the in\-app message\. 

[AWS::Pinpoint::Campaign InAppMessageButton](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-pinpoint-campaign-inappmessagebutton.html)  
Specifies the configuration of a button that appears in an in\-app message\. 

[AWS::Pinpoint::Campaign InAppMessageContent](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-pinpoint-campaign-inappmessagecontent.html)  
Specifies the configuration and contents of an in\-app message\. 

[AWS::Pinpoint::Campaign InAppMessageHeaderConfig](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-pinpoint-campaign-inappmessageheaderconfig.html)  
Specifies the configuration and content of the header or title text of the in\-app message\.  | November 4, 2021 | 
| [Updated resource](AWS_CloudFront.md) | The following resource was updated: AWS::CloudFront::Distribution\. 

 [AWS::CloudFront::Distribution](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-cloudfront-distribution.html)   
In the [CacheBehavior](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-cloudfront-distribution-cachebehavior.html) and [DefaultCacheBehavior](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-cloudfront-distribution-defaultcachebehavior.html) property types, use the `ResponseHeadersPolicyId` property to specify a response headers policy to associate with the cache behavior\.  
For more information, see [Adding HTTP headers to CloudFront responses](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/adding-response-headers.html) in the *Amazon CloudFront Developer Guide*\.  | November 4, 2021 | 
| [Updated resource](AWS_MWAA.md) | The following resource was updated: AWS::MWAA::Environment 

 TagMap   
The `TagMap` property has been removed the service resource specification\.  | November 4, 2021 | 
| [Updated resource](AWS_Redshift.md) | The following resource was updated: AWS::Redshift\. 

 [Amazon Redshift resource type reference](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/AWS_Redshift.html)   
AWS::Redshift::EndpointAccess to create a Amazon Redshift\-managed VPC endpoint\. 

 [Amazon Redshift resource type reference](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/AWS_Redshift.html)   
AWS::Redshift::EndpointAuthorization to describe an endpoint authorization for authorizing Amazon Redshift\-managed VPC endpoint access to a cluster across AWS accounts\. 

 [Amazon Redshift resource type reference](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/AWS_Redshift.html)   
AWS::Redshift::EventSubscription to create an event notification subscription\. 

 [Amazon Redshift resource type reference](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/AWS_Redshift.html)   
AWS::Redshift::ScheduledAction to create a scheduled action to run an API operation\.  | November 4, 2021 | 
| [New resources](AWS_Pinpoint.md) | The following resource was added: AWS::Pinpoint::InAppTemplate\. 

[AWS::Pinpoint::InAppTemplate](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-pinpoint-inapptemplate.html)  
Creates a message template that you can use to send in\-app messages\.  | November 4, 2021 | 
| [New resource](AWS_CloudFront.md) | The following resource was added: AWS::CloudFront::ResponseHeadersPolicy\. 

 [AWS::CloudFront::ResponseHeadersPolicy](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-cloudfront-responseheaderspolicy.html)   
Use the `AWS::CloudFront::ResponseHeadersPolicy` resource to create a new response headers policy in Amazon CloudFront\.  
For more information, see [Adding HTTP headers to CloudFront responses](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/adding-response-headers.html) in the *Amazon CloudFront Developer Guide*\.  | November 4, 2021 | 
| [New resource](AWS_DataSync.md) | The following resource was added: AWS::DataSync::LocationHDFS\. 

 [AWS::DataSync::LocationHDFS](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-datasync-locationhdfs.html)   
Use the `AWS::DataSync::LocationHDFS` resource to specify an endpoint for a Hadoop Distributed File System \(HDFS\)\.  | November 4, 2021 | 
| [New resource](AWS_EC2.md) | The following resource was added: AWS::EC2::CapacityReservationFleet\. 

 [AWS::EC2::CapacityReservationFleet](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-capacityreservationfleet.html)   
Use the `CapacityReservationFleet` property to create a Capacity Reservation Fleet\.  | November 4, 2021 | 
| [Updated resource](AWS_EC2.md) | The following resource was updated: AWS::EC2::EC2Fleet\. 

 [InstanceRequirementsRequest](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ec2-ec2fleet-instancerequirementsrequest.html)   
Use the `InstanceRequirementsRequest` property to specify instance attributes, which Amazon EC2 uses to identify instance types\.  | October 28, 2021 | 
| [Updated resource](AWS_EC2.md) | The following resource was updated: AWS::EC2::SpotFleet\. 

 [InstanceRequirementsRequest](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ec2-spotfleet-instancerequirementsrequest.html)   
Use the `InstanceRequirementsRequest` property to specify instance attributes, which Amazon EC2 uses to identify instance types\.  | October 28, 2021 | 
| [Updated resource](AWS_AutoScaling.md) | The following resource was updated: AWS::AutoScaling::AutoScalingGroup\. 

 [AWS::AutoScaling::AutoScalingGroup MixedInstancesPolicy](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-autoscaling-autoscalinggroup-mixedinstancespolicy.html)   
Use the `OnDemandAllocationStrategy` property to specify `lowest-price` as the allocation strategy for your On\-Demand capacity\. 

 [AWS::AutoScaling::AutoScalingGroup MixedInstancesPolicy](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-autoscaling-autoscalinggroup-mixedinstancespolicy.html)   
Use the `InstanceRequirements` property to specify the instance attributes that Amazon EC2 Auto Scaling uses for selecting instance types to fulfill your On\-Demand and Spot capacities\.  | October 28, 2021 | 
| [New resources](AWS_Lightsail.md) | The following resources were added: AWS::Lightsail::Database and AWS::Lightsail::StaticIp  

 [AWS::Lightsail::Database](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-lightsail-database.html)   
Use the `AWS::Lightsail::Database` resource to specify an Amazon Lightsail database\. 

 [AWS::Lightsail::StaticIp](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-lightsail-staticip.html)   
Use the `AWS::Lightsail::StaticIp` resource to specify a static IP that can be attached to an Amazon Lightsail instance that is in the same AWS Region and Availability Zone\.  | October 28, 2021 | 
| [Updated resource](AWS_MediaConnect.md) | The following resources were updated: `AWS::MediaConnect::Flow.Source`, `AWS::MediaConnect::FlowOutput` 

 [AWS::MediaConnect::Flow Source](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-mediaconnect-flow-source.html)   
Use the `AWS::MediaConnect::Flow.Source` resource to specify the details of the sources of the flow\. 

 [AWS::MediaConnect::FlowOutput](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-mediaconnect-flowoutput.html)   
Use the `AWS::MediaConnect::FlowOutput` resource to specify the destination address, protocol, and port to send the ingested video to\.  | October 27, 2021 | 
| [Updated resource](AWS_FMS.md) | The following resource was updated: AWS::FMS::Policy\. 

 [AWS::FMS::Policy](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-fms-policy.html)   
The `AWS::FMS::Policy` resource now allows you to automatically remove protections from resources that leave policy scope\.  | October 21, 2021 | 
| [Updated resource](AWS_Cassandra.md) | The following resource was updated: `AWS::Cassandra::Table`\. 

 [AWS::Cassandra::Table](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-cassandra-table.html)   
Use the `DefaultTimeToLive` property to set a default Time to Live \(TTL\) value for a table in Amazon Keyspaces \(for Apache Cassandra\)\.  | October 21, 2021 | 
| [Updated resource](AWS_SageMaker.md) | The following resource was updated: AWS::SageMaker::NotebookInstance 

 [AWS::SageMaker::NotebookInstance](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-sagemaker-notebookinstance.html)   
Use the `PlatformIdentifier` property to set the platform identifier of the notebook instance runtime environment\.  | October 21, 2021 | 
| [New resources](AWS_Panorama.md) | Use these resources to deploy computer vision applications to an AWS Panorama Appliance\. 

 [AWS::Panorama::ApplicationInstance](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-panorama-applicationinstance.html)   
Creates and deploys an application instance\. 

 [AWS::Panorama::Package](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-panorama-package.html)   
Creates an application package\. 

 [AWS::Panorama::PackageVersion](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-panorama-packageversion.html)   
Registers an application version\.  | October 21, 2021 | 
| [New resource](AWS_Rekognition.md) | The following resource was added: AWS::Rekognition:Project\. 

 [AWS::Rekognition:Project](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/AWS_Rekognition.html)   
 Use the `Project` resource to create an Amazon Rekognition Custom Labels project\.   | October 21, 2021 | 
| [New resources](AWS_DeviceFarm.md) | The following resources were added: AWS::DeviceFarm::DevicePool, AWS::DeviceFarm::InstanceProfile, AWS::DeviceFarm::NetworkProfile, AWS::DeviceFarm::Project AWS::DeviceFarm::TestGridProject, and AWS::DeviceFarm::VPCEConfiguration\. 

 [AWS::DeviceFarm::DevicePool](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-devicefarm-devicepool.html)   
Use the `AWS::DeviceFarm::DevicePool` resource to specify a device pool operation\. 

 [AWS::DeviceFarm::InstanceProfile](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-devicefarm-instanceprofile.html)   
Use the `AWS::DeviceFarm::InstanceProfile` resource to specify a profile that can be applied to one or more private fleet device instances\.  

 [AWS::DeviceFarm::NetworkProfile](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-devicefarm-networkprofile.html)   
Use the `AWS::DeviceFarm::NetworkProfile` resource to specify a network profile\.  

 [AWS::DeviceFarm::Project](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-devicefarm-project.html)   
Use the `AWS::DeviceFarm::Project` resource to specify a project\.  

 [AWS::DeviceFarm::TestGridProject](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-devicefarm-testgridproject.html)   
Use the `AWS::DeviceFarm::TestGridProject` resource to specify a Selenium testing project\.  

 [AWS::DeviceFarm::VPCEConfiguration](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-devicefarm-vpceconfiguration.html)   
Use the `AWS::DeviceFarm::VPCEConfiguration` resource to specify a configuration record in Device Farm for your Amazon Virtual Private Cloud \(VPC\) endpoint service\.   | October 14, 2021 | 
| [New resource](AWS_Wisdom.md) | The following resources were added: AWS::Wisdom::Assistant, AWS::Wisdom::AssistantAssociation, and AWS::Wisdom::KnowledgeBase 

 [AWS::Wisdom::Assistant](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-wisdom-assistant.html)   
Use the `AWS::Wisdom::Assistant` resource to specify an Amazon Connect Wisdom assistant\. 

 [AWS::Wisdom::AssistantAssociation](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-wisdom-assistantassociation.html)   
Use the `AWS::Wisdom::AssistantAssociation` resource to specify an association between an Amazon Connect Wisdom assistant and another resource\. 

 [AWS::Wisdom::KnowledgeBase](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-wisdom-knowledgebase.html)   
Use the `AWS::Wisdom::KnowledgeBase` resource to specify a knowledge base\.  | October 14, 2021 | 
| [Updated resource](AWS_CodeBuild.md) | The following resource was updated: AWS::CodeBuild::Project ProjectBuildBatchConfig 

 [AWS::CodeBuild::Project ProjectBuildBatchConfig](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-codebuild-project-projectbuildbatchconfig.html)   
The `BatchReportMode` property was added to specify the how batch build reports are sent to the source provider\.  | October 13, 2021 | 
| [New resource](AWS_Connect.md) | The following resources were added: AWS::Connect::HoursOfOperation, AWS::Connect::User, AWS::Connect::UserHierarchyGroup 

 [AWS::Connect::HoursOfOperation](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-connect-hoursofoperation.html)   
Use the `AWS::Connect::HoursOfOperation` resource to create an hours of operation\. 

 [AWS::Connect::User](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-connect-user.html)   
Use the `AWS::Connect::User` resource to create a user\. 

 [AWS::Connect::UserHierarchyGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-connect-userhierarchygroup.html)   
Use the `AWS::Connect::UserHierarchyGroup` resource to create a user hierarchy group\.  | October 12, 2021 | 
| [Updated resource](AWS_Backup.md) | The following resource was updated: AWS::Backup::BackupVault 

 [AWS::Backup::BackupVault](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-backup-backupvault.html)   
Use the `LockConfiguration` property to specify the configuration of AWS Backup; Vault Lock\. 

 [AWS::Backup::Framework](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-backup-framework.html)   
Use the `Framework` property to specify the configuration of an AWS Backup; Audit Manager framework\. 

 [AWS::Backup::ReportPlan](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-backup-reportplan.html)   
Use the `Report Plan` property to specify the configuration of an AWS Backup; Audit Manager report plan\.  | October 7, 2021 | 
| [New resources](AWS_Lightsail.md) | The following resources were added: AWS::Lightsail::Disk and AWS::Lightsail::Instance  

 [AWS::Lightsail::Instance](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-lightsail-instance.html)   
Use the `AWS::Lightsail::Instance` resource to specify an Amazon Lightsail instance\. 

 [AWS::Lightsail::Disk](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-lightsail-disk.html)   
Use the `AWS::Lightsail::Disk` resource to specify a disk that can be attached to an Amazon Lightsail instance that is in the same AWS Region and Availability Zone\.  | October 7, 2021 | 
| [New resource](AWS_IoT.md) | The following resource was added: AWS::IoT::JobTemplate\. 

 [AWS::IoT::JobTemplate](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-iot-jobtemplate.html)   
Use the `AWS::IoT::DomainConfJobTemplateiguration` resource to specify a job template in AWS IoT Core\.  | October 7, 2021 | 
| [New resource](AWS_Route53Resolver.md) | The following resource was added: `AWS::Route53Resolver::ResolverConfig` 

[AWS::Route53Resolver::ResolverConfig](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-route53resolver-resolverconfig.html)  
Use the `AWS::Route53Resolver::ResolverConfig` resource to specify information about a Route 53 Resolver configuration for a VPC\.\.  | October 7, 2021 | 
| [Updated resources](AWS_ECR.md) | The following resources were updated: AWS::ECR::ReplicationConfiguration 

 [AWS::ECR::ReplicationConfiguration](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ecr-replicationconfiguration.html)   
Use the `AWS::ECR::ReplicationConfiguration` property to configure replication for the contents of a private repository\. Support has been added to specify repository filters on a replication rule\.  | September 30, 2021 | 
| [Updated resource](AWS_KinesisFirehose.md) | The following resource was updated: AWS::KinesisFirehose::DeliveryStream\. 

 [AWS::KinesisFirehose::DeliveryStream](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-kinesisfirehose-deliverystream.html)   
Use the `AmazonopensearchserviceDestinationConfiguration` property type to specify the destination in Amazon OpenSearch Service\. You can specify only one destination\.  | September 30, 2021 | 
| [Updated resource](AWS_Lambda.md) | The following resources were updated: AWS::Lambda::LayerVersion and AWS::Lambda::Function\. 

 [AWS::Lambda::Function](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-lambda-function.html)   
Use the `Architectures` property to set the instruction set architecture for the function\.  | September 30, 2021 | 
| [Updated resource](AWS_APS.md) | The following resource was updated: AWS::APS::Workspace\. 

 [AWS::APS::Workspace](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-aps-workspace.html)   
Use the AWS::APS::Workspace resource was updated to include the `AlertManagerDefinition` property\. For more information, see [ Alert manager and templating](https://docs.aws.amazon.com/prometheus/latest/userguide/AMP-alert-manager.html)\.  | September 30, 2021 | 
| [New resource](AWS_APS.md) | The following resource was added: AWS::APS::RuleGroupsNamespace\. 

 [AWS::APS::RuleGroupsNamespace](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-aps-rulegroupsnamespace.html)   
Use the AWS::APS::RuleGroupsNamespace resource to create or update an Amazon Managed Service for Prometheus rule groups namespace\. A rule groups namespace contains Prometheus recording rules and alerting rules\. For more information, see [ Recording rules and alerting rules](https://docs.aws.amazon.com/prometheus/latest/userguide/AMP-Ruler.html)\.  | September 30, 2021 | 
| [Updated resource](AWS_AppSync.md) | The following resource was updated: AWS::AppSync::DataSource 

 [AWS::AppSync::DataSource](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-appsync-datasource.html)   
Use the `OpenSearchServiceConfig` property to specify the configuration for an Amazon OpenSearch Service domain for an AWS AppSync data source\.   | September 23, 2021 | 
| [New resources](AWS_MemoryDB.md) | The following resources were added: AWS::MemoryDB::Cluster, AWS::MemoryDB::ACL, AWS::MemoryDB::ParameterGroup, AWS::MemoryDB::SubnetGroup, and AWS::MemoryDB::User\. 

 [AWS::MemoryDB::Cluster](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-memorydb-cluster.html)   
Use the `Cluster` resource to specify a MemoryDB cluster\. 

 [AWS::MemoryDB::ACL](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-memorydb-acl.html)   
Use the `ACL` resource to specify a MemoryDB access control list and associate it with a cluster\. 

 [AWS::MemoryDB::ParameterGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-memorydb-parametergroup.html)   
Use the `ParameterGroup` resource to specify a MemoryDB parameter group and associate it with a cluster\. 

 [AWS::MemoryDB::SubnetGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-memorydb-subnetgroup.html)   
Use the `SubnetGroup` resource to specify a MemoryDB subnet group and associate it with a cluster\. 

 [AWS::MemoryDB::User](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-memorydb-user.html)   
Use the `User` resource to specify a MemoryDB user and add it to an access control list\.  | September 23, 2021 | 
| [Updated resources](AWS_EMR.md) | The following resource was updated: AWS::EMR::Studio\. 

 [AWS::EMR::Studio](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-emr-studio.html)   
Use the `IdpAuthUrl` property to specify the authentication endpoint of your identity provider \(IdP\) when you use IAM authentication and want to let federated users log in to an Amazon EMR Studio with the Studio URL and credentials from your IdP\.  
Use the `IdpRelayStateParameterName` property to specify the name that your identity provider uses for its RelayState parameter\.  
Use the `UserRole` property only when you set `AuthMode` to `SSO`\.  | September 17, 2021 | 
| [Updated resource](AWS_S3.md) | The following resource was updated: AWS::S3::Bucket\. 

 [Monitoring metrics with Amazon CloudWatch](https://docs.aws.amazon.com/AmazonS3/latest/userguide/cloudwatch-monitoring.html)   
Use the `AccessPointArn` property in `AWS::S3::Bucket MetricsConfiguration` to filter CloudWatch request metrics by access point\.  | September 17, 2021 | 
| [Updated resource](AWS_ACMPCA.md) | The following resource was added: AWS::ACMPCA::Permission\. 

 [AWS::ACMPCA::Permission](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aaws-resource-acmpca-permission.html)   
Use the `AWS::ACMPCA::Permission` object to grant permissions on a private CA to the AWS Certificate Manager \(ACM\) service principal \(acm\.amazonaws\.com\)\. These permissions allow ACM to issue and renew ACM certificates that reside in the same AWS account as the CA\.  | September 16, 2021 | 
| [Updated resource](AWS_MSK.md) | The following resource was updated: AWS::MSK::Cluster 

 [AWS::MSK::Cluster](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-msk-cluster.html)   
You can now update the authentication and encryption settings for an existing MSK cluster\.  | September 16, 2021 | 
| [New resources](AWS_OpenSearchService.md) | The following resource was added: AWS::OpenSearchService::Domain\. 

 [AWS::OpenSearchService::Domain](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-opensearchservice-domain.html)   
Use the `AWS::OpenSearchService::Domain` resource to create an Amazon OpenSearch Service domain\.  | September 16, 2021 | 
| [New resource](AWS_APS.md) | The following resource was added: AWS::APS::Workspace\. 

 [AWS::APS::Workspace](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-aps-workspace.html)   
Use the AWS::APS::Workspace resource to create an Amazon Managed Service for Prometheus workspace\. For more information, see [ Create a workspace](https://docs.aws.amazon.com/prometheus/latest/userguide/AMP-onboard-create-workspace.html)\.  | September 16, 2021 | 
| [Updated resource](AWS_Cassandra.md) | The following resource was updated: `AWS::Cassandra::Table`\. 

 [AWS::Cassandra::Table](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-cassandra-table.html)   
Use the `AWS::Cassandra::Table` resource to add new regular columns to existing tables in Amazon Keyspaces \(for Apache Cassandra\)\.  | September 3, 2021 | 
| [Updated resources](AWS_Transfer.md) | The following resource was updated: AWS::Transfer::Server 

[AWS::Transfer::Server WorkflowDetail](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-transfer-server.html#cfn-transfer-server-workflowdetail)  
Use the `WorkflowDetail` property to specify the steps and other details for a workflow\. 

[AWS::Transfer::Server WorkflowDetails](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-transfer-server.html#cfn-transfer-server-workflowdetails)  
Use the `WorkflowDetails` property as a container for the `WorkflowDetails` property\.  | September 2, 2021 | 
| [Updated resource](AWS_ACMPCA.md) | The following resource was added: AWS::ACMPCA::CertificateAuthority OcspConfiguration\. The following resource was updated: AWS::ACMPCA::CertificateAuthority RevocationConfiguration\. 

 [AWS::ACMPCA::CertificateAuthority OcspConfiguration](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-acmpca-certificateauthority-ocspconfiguration.html)   
Use the `AWS::ACMPCA::CertificateAuthority OcspConfiguration` object to configure Online Certificate Status Protocol \(OCSP\) support on a CA\.  | September 2, 2021 | 
| [Updated resource](AWS_DataSync.md) | The following resource was updated: AWS::DataSync::Task\. 

 [AWS::DataSync::Task](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-datasync-task.html)   
Use the `Includes` property to specify files to include in a task\.  | September 2, 2021 | 
| [Updated resource](AWS_EventSchemas.md) | The following resource was Updated: `AWS::EventSchemas::Discoverer`\. 

 [AWS::EventSchemas::Discoverer](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-eventschemas-discoverer.html)   
Use the `CrossAccount` property to allow event schemas from other accounts to be discovered\.   | September 2, 2021 | 
| [Updated resource](AWS_KinesisFirehose.md) | The following resource was updated: AWS::KinesisFirehose::DeliveryStream\. 

 [AWS::KinesisFirehose::DeliveryStream](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-kinesisfirehose-deliverystream.html)   
DynamicPartitioningConfiguration property type is now supported for the delivery streams in CloudFormation\.  | September 2, 2021 | 
| [New resource](AWS_IoT.md) | The following resource is new: AWS::IoT::FleetMetric 

 [AWS::IoT::FleetMetric](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-iot-fleetmetric.html)   
Use the `AWS::IoT::FleetMetric` resource to specify a fleet metric\.  | September 2, 2021 | 
| [New resource](AWS_S3.md) | The following resources were added: AWS::S3::MultiRegionAccessPoint and AWS::S3::MultiRegionAccessPointPolicy\. 

 [AWS::S3::MultiRegionAccessPoint](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-s3-multiregionaccesspoint.html)   
Use the `AWS::S3::MultiRegionAccessPoint` resource to create an S3 Multi\-Region Access Point configuration\. 

 [AWS::S3::MultiRegionAccessPointPolicy](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-s3-multiregionaccesspointpolicy.html)   
Use the `AWS::S3::MultiRegionAccessPointPolicy` resource to create an S3 Multi\-Region Access Point Policy configuration\.  | September 2, 2021 | 
| [Terminology change](AWS_KMS.md) | AWS KMS is replacing the term *customer master key \(CMK\)* with *AWS KMS key* and *KMS key*\. The concept has not changed\. To prevent breaking changes, AWS KMS is keeping some variations of this term\. | August 30, 2021 | 
| [Stack failure options](#ReleaseHistory) | You can iteratively develop your applications when provisioning failures are encountered by starting from the point of failure without rolling back successfully provisioned resources\. By specifying stack failure options, you can troubleshoot resources in a `CREATE_FAILED` or `UPDATE_FAILED` status\. You can provision failure options for all stack deployments and change set operations\.For more information, see [Stack failure options](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/stack-failure-options.html)\. | August 30, 2021 | 
| [Updated resource](AWS_CodeBuild.md) | The following resource was updated: AWS::CodeBuild::Project 

 [AWS::CodeBuild::Project](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-codebuild-project.html)   
The `ResourceAccessRole` and `Visibility` properties were added to support public builds\.  | August 19, 2021 | 
| [Updated resource](AWS_AutoScaling.md) | The following resource was updated: AWS::AutoScaling::ScalingPolicy\. 

 [AWS::AutoScaling::ScalingPolicy](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-as-policy.html)   
Use the `PredictiveScalingConfiguration` property to specify a predictive scaling policy configuration for an Auto Scaling group\.  | August 19, 2021 | 
| [Updated resource](AWS_SageMaker.md) | The following resource was updated: AWS::SageMaker::EndpointConfig 

 [AWS::SageMaker::EndpointConfig](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-sagemaker-endpointconfig.html)   
In the [AsyncInferenceClientConfig](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-sagemaker-endpointconfig-asyncinferenceclientconfig.html) property type, use the `MaxConcurrentInvocationsPerInstance` property to set the maximum number of concurent requests\.  
In the [AsyncInferenceConfig](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-sagemaker-endpointconfig-asyncinferenceconfig.html) property type, use the `ClientConfig` to configure the behavior of the client SageMaker uses\. Use `OutputConfig` to spcify invocation outputs\.  
In the [AsyncInferenceNotificationConfig](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-sagemaker-endpointconfig-asyncinferencenotificationconfig.html) property, use the `ErrorTopic` and `SuccessTopic` to define Amazon SNS topics to post a notification if the inference fails or completes successfully, respectively\.  
In the [OutputConfig](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-sagemaker-endpointconfig-asyncinferenceoutputconfig.html) property type use the `KmsKeyId` to encrypt the asynchronous inference output\. Use `NotificationConfig` to specify the notification configuration and `S3OutputPath` to specify the output location in S3\.  | August 19, 2021 | 
| [Updated resource](AWS_Elasticsearch.md) | The following resource was updated: AWS::Elasticsearch::Domain\. 

 [AWS::Elasticsearch::Domain](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-elasticsearch-domain.html)   
Use the `ColdStorageOptions` property to specify whether to enable cold storage for the cluster\.  | August 17, 2021 | 
| [Updated resources](AWS_WAFv2.md) | The following resource was updated: AWS::WAFv2::WebACL\. 

 [AWS::WAFv2::WebACL](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-wafv2-webacl.html)   
You can now specify the version to use for managed rule groups\. For information, see `ManagedRuleGroupStatement`\.  | August 12, 2021 | 
| [Updated resource](AWS_ApiGateway.md) | The following resource was updated: AWS::ApiGateway::DomainName\. 

 [AWS::ApiGateway::DomainName](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-apigateway-domainname.html)   
Use the `OwnershipVerificationCertificateArn` property to specify the certificate ARN used to verify ownership of the domain using mutual TLS\.  | August 12, 2021 | 
| [Updated resource](AWS_LookoutEquipment.md) | The following resource was updated: AWS::LookoutEquipment::InferenceScheduler 

 [AWS::LookoutEquipment::InferenceScheduler](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-lookoutequipment-inferencescheduler.html)   
The ModelName property has changed so that an update requires replacement\.  
The ServerSideKmsKeyId property has changed so that an update requires replacement\.  | August 12, 2021 | 
| [Updated resource](AWS_SageMaker.md) | The following resource was updated: AWS::SageMaker::Model\. 

 [AWS::SageMaker::Model](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-sagemaker-model.html)   
In the [ImageConfig](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-sagemaker-model-containerdefinition-imageconfig.html) property type, use the `RepositoryAuthConfig` property to specify an authentication configuration for the private docker registry where your model image is hosted\.  | August 12, 2021 | 
| [Updated resource](AWS_WAFv2.md) | The following resource was added: AWS::WAFv2::LoggingConfiguration\. 

 [AWS::WAFv2::LoggingConfiguration](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-wafv2-loggingconfiguration.html)   
You can now define an association between Amazon Kinesis Data Firehose destinations and a web ACL resource, for logging\.   | August 12, 2021 | 
| [Updated resource](AWS_AppSync.md) | The following resource was updated: AWS::AppSync::GraphQLApi 

 [AWS::AppSync::GraphQLApi](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-appsync-graphqlapi.html)   
Use the `LambdaAuthorizerConfig` property to specify the configuration for AWS Lambda function authorization\.  | August 5, 2021 | 
| [Updated resource](AWS_FSx.md) | The following resource was updated: AWS::FSx::FileSystem 

 [AWS::FSx::FileSystem](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-fsx-filesystem.html)   
In the [WindowsConfiguration](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-fsx-filesystem-windowsconfiguration.html) property type, use the `AuditLogConfiguration` property to enable audit event logging of end\-user accesses of files, folders, and file shares on an Amazon FSx Windows File Server instance\.  | August 5, 2021 | 
| [New resource](AWS_Athena.md) | The following resource was added: AWS::Athena::PreparedStatement 

 [AWS::Athena::PreparedStatement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-athena-preparedstatement.html)   
Use the `AWS::Athena::PreparedStatement` resource to specify a prepared statement for use with SQL queries in Athena\. Use prepared statements for repeated execution of the same query with different query parameters\. A prepared statement contains parameter placeholders whose values are supplied at execution time\.  | August 5, 2021 | 
| [Updated resource](AWS_DataBrew.md) | The following resource was updated: AWS::DataBrew::Job 

 [AWS::DataBrew::Job](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-databrew-job-databaseoutput.html)   
Use the `AWS::DataBrew::Job.DatabaseOutputs` property type to define the output destination for a DataBrew job to be written into\.  
Use the `AWS::DataBrew::Job.ProfileConfiguration` property type to configure which statistics to include when running DataBrew profile jobs\.  | July 29, 2021 | 
| [Updated resource](AWS_S3Outposts.md) | The following resource was updated: AWS::S3Outposts::EndPoint 

 [AWS::S3Outposts::EndPoint](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-s3outposts-endpoint.html)   
Use the `AWS::S3Outposts::EndPoint.AccessType` property to create an endpoint using [customer owned IP \(CoIP\) addresses](https://docs.aws.amazon.com/outposts/latest/userguide/outposts-networking-components.html) and access your Amazon S3 on AWS Outposts objects by creating a [ local gateway](https://docs.aws.amazon.com/outposts/latest/userguide/outposts-networking-components.html) from your on\-premises network\.  | July 29, 2021 | 
| [New resource](AWS_Route53RecoveryControl.md) | The following resources were released: AWS::Route53RecoveryControl::Cluster, AWS::Route53RecoveryControl::ControlPanel, AWS::Route53RecoveryControl::RoutingControl, AWS::Route53RecoveryControl::SafetyRule 

 [AWS::Route53RecoveryControl::Cluster](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-route53recoverycontrol-cluster.html)   
Use the `AWS::Route53RecoveryControl::Cluster` to host routing controls, which are simple on/off switches for routing traffic\. 

 [AWS::Route53RecoveryControl::ControlPanel](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-route53recoverycontrol-controlpanel.html)   
Use the `AWS::Route53RecoveryControl::ControlPanel` to define a group of routing controls that can be updated together in a single transaction\. 

 [AWS::Route53RecoveryControl::RoutingControl](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-route53recoverycontrol-routingcontrol.html)   
Use the `AWS::Route53RecoveryControl::RoutingControl` to fail over traffic to an application replica, to recover your application across Availability Zones or Regions\. 

 [AWS::Route53RecoveryControl::SafetyRule](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-route53recoverycontrol-safetyrule.html)   
Use the `AWS::Route53RecoveryControl::SafetyRule` to configure safeguards for routing controls, to avoid a scenario like stopping all traffic flow by setting all routing controls to off\.   | July 29, 2021 | 
| [New resource](AWS_Route53RecoveryReadiness.md) | The following resources were released: AWS::Route53RecoveryReadiness::Cell, AWS::Route53RecoveryReadiness::ReadinessCheck, AWS::Route53RecoveryReadiness::RecoveryGroup, AWS::Route53RecoveryReadiness::ResourceSet 

 [AWS::Route53RecoveryReadiness::Cell](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-route53recoveryreadiness-cell.html)   
Use the `AWS::Route53RecoveryReadiness::Cell` to define a single cell for an application\. 

 [AWS::Route53RecoveryReadiness::ReadinessCheck](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-route53recoveryreadiness-readinesscheck.html)   
Use the `AWS::Route53RecoveryReadiness::ReadinessCheck` to check application readiness for failover\. Amazon Route 53 Application Recovery Controller uses readiness checks to determine the readiness of the resources in a resource set\. 

 [AWS::Route53RecoveryReadiness::RecoveryGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-route53recoveryreadiness-recoverygroup.html)   
Use the `AWS::Route53RecoveryReadiness::RecoveryGroup` to define a recovery group for an application\. A recovery group models an application and includes cells that represent application replicas\. 

 [AWS::Route53RecoveryReadiness::ResourceSet](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-route53recoveryreadiness-resourceset.html)   
Use the `AWS::Route53RecoveryReadiness::ResourceSet` to define a group of resources of a single type that you can associate with a readiness check\.  | July 29, 2021 | 
| [Import stacks to stack set](#ReleaseHistory) | The AWS CloudFormation *stack import* operation can import existing stacks into new or existing stack sets, so that you can migrate existing stacks to a stack set in one operation\.For more information, see [Importing stacks into a stack set](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/stacksets-import.html)\. | July 28, 2021 | 
| [Updated resource](AWS_CloudWatch.md) | The following resource was updated: AWS::CloudWatch::Alarm\. 

 [AWS::CloudWatch::Alarm](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-cw-alarm.html)   
In the [MetricDataQuery](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-cloudwatch-alarm-metricdataquery.html) property type, use the `AccountId` property to specify the ID of the account where the metrics are located, if this is a cross\-account alarm\.  | July 22, 2021 | 
| [Updated resource](AWS_QLDB.md) | The following resource was updated: AWS::QLDB::Ledger 

 [AWS::QLDB::Ledger](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-qldb-ledger.html)   
Use the `KmsKey` property to specify a customer managed AWS KMS key to use for encryption at rest in the ledger\.  | July 22, 2021 | 
| [New resources](AWS_LookoutEquipment.md) | The following resources were added: AWS::LookoutEquipment::InferenceScheduler 

 [AWS::LookoutEquipment::InferenceScheduler](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-lookoutequipment-inferencescheduler.html)   
Use the `AWS::LookoutEquipment::InferenceScheduler` resource to set up a continuous real\-time inference plan to analyze new measurement data\.  | July 22, 2021 | 
| [Updated resource](AWS_EC2.md) | The following resource was updated: AWS::EC2::VPCCidrBlock\. 

 [AWS::EC2::VPCCidrBlock](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-vpccidrblock.html)   
Use the `Ipv6CidrBlock` property to specify an IPv6 CIDR block from the IPv6 address pool\.  
Use the `Ipv6Pool` property to specify the ID of an IPv6 address pool from which to allocate the IPv6 CIDR block\.  | July 21, 2021 | 
| [Updated resource](AWS_Cassandra.md) | The following resource was updated: `AWS::Cassandra::Table`\. 

 [AWS::Cassandra::Table\.EncryptionSpecification](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-cassandra-table.html)   
Use the `AWS::Cassandra::Table.EncryptionSpecification` property to choose the encryption option for new or existing tables in Amazon Keyspaces \(for Apache Cassandra\)\.  | July 21, 2021 | 
| [New resource](AWS_Logs.md) | The following resource was added : AWS::Logs::ResourcePolicy 

 [AWS::Logs::ResourcePolicy](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-logs-resourcepolicy.html)   
Use the `AWS::Logs::ResourcePolicy` resource to create a IAM policy that allows other AWS services to write log events to this account\. For more information, see [ Logs sent to CloudWatch Logs](https://docs.aws.amazon.com/AmazonCloudWatch/latest/logs/AWS-logs-and-resource-policy.html#AWS-logs-infrastructure-CWL)\.  | July 15, 2021 | 
| [Increased quota](#ReleaseHistory) | The following AWS CloudFormation quota has been updated\.  You can now declare a defaulted maximum of `2000` stacks in your AWS CloudFormation account\. For more information, see [AWS CloudFormation quotas](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/cloudformation-limits.html)\.   | July 15, 2021 | 
| [Updated resource](AWS_DataBrew.md) | The following resource was updated: AWS::DataBrew::Job 

 [AWS::DataBrew::Job](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-databrew-job-datacatalogoutput.html)   
Use the `AWS::DataBrew::Job.DataCatalogOutput` property type to define outputs from DataBrew recipe jobs to the AWS Glue Data Catalog\.  | July 9, 2021 | 
| [Updated resources](AWS_ServiceDiscovery.md) | The following resources were updated: `AWS::ServiceDiscovery::PrivateDnsNamespace` and `AWS::ServiceDiscovery::PublicDnsNamespace`\. 

[AWS::ServiceDiscovery::PrivateDnsNamespace](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-servicediscovery-privatednsnamespace.html)   
Use the `Properties` property to specify DNS properties for an AWS Cloud Map private DNS namespace\. 

[AWS::ServiceDiscovery::PublicDnsNamespace](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-servicediscovery-publicdnsnamespace.html)   
Use the `Properties` property to specify DNS properties for an AWS Cloud Map public DNS namespace\.  | July 8, 2021 | 
| [Updated resources](AWS_CodeDeploy.md) | The following resources were updated: AWS::CodeDeploy::Application, AWS::CodeDeploy::DeploymentConfig, and AWS::CodeDeploy::DeploymentGroup 

 [AWS::CodeDeploy::Application](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-codedeploy-application.html)   
Use the `Tags` property to specify metadata to add to CodeDeploy applications\. 

 [AWS::CodeDeploy::DeploymentConfig](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-codedeploy-deploymentconfig.html)   
Use the `TrafficRoutingConfig` property to specify how deployment traffic is routed\.  
Use the `ComputePlatform` property to specify the destination platform type for the deployment \(`Lambda`, `Server`, or `ECS`\)\. 

 [AWS::CodeDeploy::DeploymentGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-codedeploy-deploymentgroup.html)   
Use the `BlueGreenDeploymentConfiguration` property to specify information about blue/green deployment options for a deployment group\.  
Use the `ECSServices` property to specify the target Amazon ECS services in the deployment group\.  | July 8, 2021 | 
| [Updated resource](AWS_AutoScaling.md) | The following resource was updated: AWS::AutoScaling::LaunchConfiguration\. 

 [AWS::AutoScaling::LaunchConfiguration](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-as-launchconfig.html)   
Use the `BlockDevice` property to specify GP3 volumes in the block device mappings for launch configurations\.  | July 8, 2021 | 
| [Updated resources](AWS_ImageBuilder.md) | The following resources were updated: AWS::ImageBuilder::ContainerRecipe and AWS::ImageBuilder::DistributionConfiguration\. 

 [AWS::ImageBuilder::DistributionConfiguration](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-imagebuilder-distributionconfiguration.html)   
Use the `LaunchTemplateConfiguration` property to use an Amazon EC2 launch template for specified accounts where you distribute your Image Builder image\. 

 [AWS::ImageBuilder::ContainerRecipe](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-imagebuilder-containerrecipe.html)   
+ Retrieve the container recipe `Name` attribute with the `GN::GetAtt` function\.
+ Use the `InstanceBlockDeviceMapping` property to define block device mappings for the build instance used to configure your image\.  | July 1, 2021 | 
| [China Rebrand Update](AWS_Chatbot.md) | China rebrand updates | June 29, 2021 | 
| [Updated resources](AWS_Transfer.md) | The following resource was updated: AWS::Transfer::Server ProtocolDetails 

 [AWS::Transfer::Server ProtocolDetails](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-transfer-server.html#cfn-transfer-server-protocoldetails)   
Use the `ProtocolDetails` property to specify the `PassiveIp` address for FTP and FTPS protocols\.  | June 24, 2021 | 
| [Updated resource](AWS_DAX.md) | The following resource was updated: AWS::DAX::Cluster 

 [AWS::DAX::Cluster](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-dax-cluster.html)   
Use the `ClusterEndpointEncryptionType` to specify the encryption type of the cluster's endpoint\.  | June 24, 2021 | 
| [New resources](AWS_CloudFormation.md) | The following resources were added: AWS::CloudFormation::PublicTypeVersion, AWS::CloudFormation::Publisher, and AWS::CloudFormation::TypeActivation\. 

 [AWS::CloudFormation::PublicTypeVersion](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-cloudformation-publictypeversion.html)  
Use the `AWS::CloudFormation::PublicTypeVersion` resource to test and publish a registered extension as a public, third\-party extension\. 

 [AWS::CloudFormation::Publisher](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-cloudformation-publisher.html)  
Use the `AWS::CloudFormation::Publisher` resource to register your account as a publisher of public extensions in the CloudFormation registry\. 

 [AWS::CloudFormation::TypeActivation](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-cloudformation-typeactivation.html)  
Use the `AWS::CloudFormation::TypeActivation` resource to activate a public third\-party extension, making it available for use in CloudFormation operations\.  | June 24, 2021 | 
| [New resource](AWS_Connect.md) | The following resource was added: AWS::Connect::QuickConnect 

 [AWS::Connect::QuickConnect](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-connect-quickconnect.html)   
Use the `AWS::Connect::QuickConnect` resource to create a quick connect\.  | June 24, 2021 | 
| [Updated resource](AWS_MWAA.md) | The following resource was updated: AWS::MWAA::Environment 

 [Schedulers](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-mwaa-environment.html#cfn-mwaa-environment-schedulers)   
Use the `Schedulers` property to specify the number of Apache Airflow schedulers that run in an environment\.  | June 21, 2021 | 
| [Publish public third\-party extensions](#ReleaseHistory) | Use public extensions provided by third\-party publishers, just as you would extensions from AWS\.For more information, see [Using public extensions](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/registry-public.html)\. For information about publishing third\-party public extensions, see [Publishing extensions](https://docs.aws.amazon.com/cloudformation-cli/latest/userguide/publish.html) in the *CloudFormation CLI User Guide*\. | June 21, 2021 | 
| [Updated resource](AWS_AutoScaling.md) | The following resource was updated: AWS::AutoScaling::ScheduledAction\. 

 [AWS::AutoScaling::ScheduledAction](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-as-scheduledaction.html)   
Use the `TimeZone` property to create recurring scheduled actions in the local time zone\. If your time zone observes Daylight Saving Time \(DST\), the recurring action automatically adjusts for Daylight Saving Time\.  | June 18, 2021 | 
| [Updated resources](AWS_AppMesh.md) | The following resources were updated: AWS::AppMesh::VirtualNode, AWS::AppMesh::GatewayRoute, and AWS::AppMesh::Route 

 [AWS::AppMesh::VirtualNode](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-appmesh-virtualnode.html)   
Use the `DnsServiceDiscovery` property to represent the DNS service discovery information for your virtual node\. 

 [AWS::AppMesh::GatewayRoute](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-appmesh-gatewayroute.html)   
Use the `GatewayRouteHostnameMatch` property to represent the gateway route hostname to match\.  
Use the `GatewayRouteHostnameRewrite ` property to represent the gateway route host name to rewrite\.  
Use the `GrpcGatewayRouteMetadata` property to represent the metadata of the gateway route\.  
Use the `GrpcGatewayRouteRewrite` property to represent the the gateway route to rewrite\.  
Use the `GrpcMetadataMatchMethod` property to represent the method header to be matched\.  
Use the `HttpGatewayRouteHeader` property to represent the HTTP header in the gateway route\.  
Use the `HttpGatewayRoutePathRewrite` property to represent the path to rewrite\.  
Use the `HttpGatewayRoutePrefixRewrite` property to represent the beginning characters of the route to rewrite\.  
Use the `HttpGatewayRouteRewrite` property to represent the beginning characters of the route to rewrite\.  
Use the `HttpGatewayRoutePathRewrite` property to represent the beginning characters of the route to rewrite\. 

 [AWS::AppMesh::Route](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-appmesh-route.html)   
Use the `HttpQueryParameter` property to represent the query parameter in the request\.  | June 17, 2021 | 
| [Updated resource](AWS_KMS.md) | The following resource was updated: AWS::KMS::Key\. 

 [AWS::KMS::Key](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-kms-key.html)   
Use the `MultiRegionKey` property to specify multi\-Region primary keys\.  | June 17, 2021 | 
| [New resource](AWS_KMS.md) | The following resource was added: AWS::KMS::ReplicaKey\. 

 [AWS::KMS::ReplicaKey](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-kms-replicakey.html)   
Use the `AWS::KMS::ReplicaKey` resource to specify a replica of a specified multi\-Region primary key\.  | June 17, 2021 | 
| [Parallel Node Upgrade and Scale to Zero](AWS_EKS.md) | In the NodegroupUpdateConfig, use either the MaxUnavailable and MaxUnavailablePercentage values to define the number of nodes to upgrade in parallel\. In the scalingconfig, the minsize and desiredsize values can both be set to zero\. | June 16, 2021 | 
| [Updated resource](AWS_EC2.md) | The following resource was updated: AWS::EC2::NatGateway 

 [AWS::EC2::NatGateway](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-natgateway.html)   
Use the `ConnectivityType` property to indicate whether the NAT gateway supports public or private connectivity\.  | June 11, 2021 | 
| [Updated resources](AWS_RAM.md) | The following resource was updated: `AWS::RAM:ResourceShare` 

 [AWS::RAM::ResourceShare](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ram-resourceshare.html)   
Use the `PermissionArns` property to specify the Amazon Resource Names \(ARNs\) of the permissions to associate with the resource share\.  | June 10, 2021 | 
| [Updated resource](AWS_KinesisAnalyticsV2.md) | The following resource was updated: AWS::KinesisAnalyticsV2::Application 

 [AWS::KinesisAnalyticsV2::Application ApplicationConfiguration](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-kinesisanalyticsv2-application-applicationconfiguration.html)   
You can use the ZeppelinApplicationConfiguration property to create Studio notebook applications that use Apache Zeppelin\. You can use the notebook interactively, and you can deploy it as a continuously running streaming application with durable state and autoscaling features\.  | June 10, 2021 | 
| [Updated resource](AWS_SQS.md) | The following resource was updated: AWS::SQS::Queue 

 [AWS::SQS::Queue](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-sqs-queues.html)   
You can now use the `DeduplicationScope` and `FifoThroughputLimit`properties to enable higher throughput for FIFO queues\.  | June 10, 2021 | 
| [Updated resource](AWS_SSM.md) | The following resource was updated: AWS::SSM::Document 

 [AWS::SSM::Document](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ssm-document.html)   
Use the `Attachments` property to specify a list of key and value pairs that describe attachments to a version of a document\. Use the `Requires` property to specify a list of SSM documents required by a document\. This parameter is used exclusively by AWS AppConfig\. When a user creates an AWS AppConfig configuration in an SSM document, the user must also specify a required document for validation purposes\. In this case, an ApplicationConfiguration document requires an ApplicationConfigurationSchema document for validation purposes\. For more information, see [Creating a configuration and a configuration profile ](https://docs.aws.amazon.com/appconfig/latest/userguide/appconfig-creating-configuration-and-profile.html) in the *AWS AppConfig User Guide*\.  | June 10, 2021 | 
| [Updated resource](AWS_FSx.md) | The following resource was updated: AWS::FSx::FileSystem 

[AWS::FSx::FileSystem](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-fsx-filesystem.html)  
Use the `DNSName` attribute to access the DNS name of your Amazon FSx file system\.  | June 7, 2021 | 
| [New resource](AWS_Location.md) | The following resources were added: `AWS::Location::GeofenceCollection`, `AWS::Location::Map`, `AWS::Location::PlaceIndex`, `AWS::Location::RouteCalculator`, `AWS::Location::Tracker`, and `AWS::Location::TrackerConsumer`\. 

 [AWS::Location::GeofenceCollection](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-location-geofencecollection.html)   
Use the `AWS::Location::GeofenceCollection` resource to specify the ability to detect and act when a tracked device enters or exits a defined geographical boundary\. 

 [AWS::Location::Map](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-location-map.html)   
Use the `AWS::Location::Map` resource to specify a map resource in your AWS account, which provides map tiles of different styles sourced from available data providers\. 

 [AWS::Location::PlaceIndex](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-location-placeindex.html)   
Use the `AWS::Location::PlaceIndex` resource to specify a place index resource in your AWS account, which supports Places functions with geospatial data sourced from your chosen data provider\. 

 [AWS::Location::RouteCalculator](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-location-routecalculator.html)   
Use the `AWS::Location::RouteCalculator` resource to specify a route calculator resource in your AWS account\. 

 [AWS::Location::Tracker](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-location-tracker.html)   
Use the `AWS::Location::Tracker` resource to specify a tracker resource in your AWS account, which lets you receive current and historical location of devices\. 

 [AWS::Location::TrackerConsumer](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-location-trackerconsumer.html)   
Use the `AWS::Location::TrackerConsumer` resource to specify an association between a geofence collection and a tracker resource\.  | June 7, 2021 | 
| [Updated resources](AWS_MediaPackage.md) | The following resources were updated: AWS::MediaPackage::Channel, AWS::MediaPackage::OriginEndpoint, AWS::MediaPackage::PackagingConfiguration, and AWS::MediaPackage::PackagingGroup\. 

 [AWS::MediaPackage::Channel\.](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-mediapackage-channel.html)   
Use the `EgressAccessLogs` property to specify egress access logs for your channel\.  
Use the `IngressAccessLogs` property to specify ingress access logs for your channel\. 

 [AWS::MediaPackage::OriginEndpoint\.](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-mediapackage-originendpoint.html)   
Use the `CmafEncryption.ConstantInitializationVector` property to specify an optional 128\-bit, 16\-byte hex value represented by a 32\-character string, used in conjunction with the key for encrypting blocks\. If you don't specify a value, then AWS Elemental MediaPackage creates the constant initialization vector \(IV\)\. 

 [AWS::MediaPackage::PackagingConfiguration\.](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-mediapackage-packagingconfiguration.html)   
Use the `CmafPackage.IncludeEncoderConfigurationInSegments` property to place your encoder's metadata into every video segment instead of the init fragment, which is the default behavior\. This lets you use different SPS/PPS/VPS settings for your assets during content playback\. 

 [AWS::MediaPackage::PackagingGroup\.](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-mediapackage-packaginggroup.html)   
Use the `EgressAccessLogs` property to configure egress access logs for your packaging group\.  | May 27, 2021 | 
| [Updated resources](AWS_WAFv2.md) | The following resources were updated: AWS::WAFv2::WebACL and AWS::WAFv2::RuleGroup\. 

 [AWS::WAFv2::WebACL](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-wafv2-webacl.html)   
You now have additional text transformation options\. 

 [AWS::WAFv2::RuleGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-wafv2-rulegroup.html)   
You now have additional text transformation options\.  | May 27, 2021 | 
| [Updated resource](AWS_ACMPCA.md) | The following resource was updated: AWS::ACMPCA::CertificateAuthority\. 

 [AWS::ACMPCA::CertificateAuthority](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-acmpca-certificateauthority.html)   
Use the `S3ObjectAcl` property to restrict public access to your CRLs\.  | May 27, 2021 | 
| [Updated resource](AWS_FraudDetector.md) | The following resource was updated: AWS::FraudDetector::Detector\. 

 [AWS::FraudDetector::Detector](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-frauddetector-detector.html)   
Use the `AssociatedModels` property to associate models with the detector\.  | May 27, 2021 | 
| [Updated resource](AWS_FSx.md) | The following resource was updated: AWS::FSx::FileSystem 

[AWS::FSx::FileSystem](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-fsx-filesystem.html)  
In the [LustreConfiguration](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-fsx-filesystem-lustreconfiguration.html) property type, use `DataCompressionType` to specify the type of data compression used by an Amazon FSx for Lustre file system\.  | May 27, 2021 | 
| [Updated resource](AWS_MWAA.md) | The following resource was updated: AWS::MWAA::Environment 

 [ModuleLoggingConfiguration](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-mwaa-environment-moduleloggingconfiguration.html)   
In the `ModuleLoggingConfiguration` property type, the `CloudWatchLogGroupArn` response property type for the CloudWatch Logs ARN where Apache Airflow DAG logs are published was removed from the request to enable logs, and is being returned in the response\. 

 [AirflowConfigurationOptions](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-mwaa-environment.html)   
In the `AirflowConfigurationOptions` property type, use a `PrimitiveType` of `Json` to add an Apache Airflow configuration option\. 

 [MinWorkers](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-mwaa-environment.html#cfn-mwaa-environment-minworkers)   
Use the `MinWorkers` property to specify the minimum number of Apache Airflow workers that run in an environment\.  | May 27, 2021 | 
| [Updated resource](AWS_QLDB.md) | The following resource was updated: AWS::QLDB::Ledger 

 [AWS::QLDB::Ledger](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-qldb-ledger.html)   
The `PermissionsMode` property has changed so that an update requires no interruption\.  | May 27, 2021 | 
| [New resource](AWS_CUR.md) | The following resource was added: AWS::CUR::ReportDefinition 

 [AWS::CUR::ReportDefinition](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-cur-reportdefinition.html)   
Use the `AWS::CUR::ReportDefinition` resource to define AWS Cost and Usage Report\.  | May 27, 2021 | 
| [Region availability](AWS_AmazonMQ.md) | The following resources were updated: AWS::AmazonMQ::Broker 

 [AWS::AmazonMQ::Broker](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-amazonmq-broker.html)   
Amazon MQ for RabbitMQ is now available in the Amazon Web Services China \(Bejing\) and the Amazon Web Services China \(Ningxia\) Regions\.  | May 26, 2021 | 
| [New resources](AWS_EC2.md) | The following resource was added: AWS::EC2::TransitGatewayPeeringAttachment\. 

 [AWS::EC2::TransitGatewayPeeringAttachment](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-transitgatewaypeeringattachment.html)   
Use the `TransitGatewayPeeringAttachment` resource to request transit gateway peering attachment between the specified transit gateway \(requester\) and a peer transit gateway \(accepter\)\.  | May 20, 2021 | 
| [New resource](AWS_AppRunner.md) | The following resource was added: AWS::AppRunner::Service 

 [AWS::AppRunner::Service](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-apprunner-service.html)   
Use the `AWS::AppRunner::Service` resource to create or update an AWS App Runner service\.  | May 20, 2021 | 
| [New resource](AWS_IoTCoreDeviceAdvisor.md) | The following resource was added: AWS::IoTCoreDeviceAdvisor::SuiteDefinition 

 [SuiteDefinition](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-iotcoredeviceadvisor-suitedefinition.htm)   
Use the `SuiteDefinition` resource to create a new test suite configuration for Device Advisor\.  | May 20, 2021 | 
| [Updated resources](AWS_CloudFormation.md) | The following resource was updated: AWS::CloudFormation::StackSet\. 

 [AWS::CloudFormation::StackSet](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-cloudformation-stackset.html)  
Use the `CallAs` property type to specify whether you are acting as an account administrator in the organization's management account or as a delegated administrator in a member account\.  | May 14, 2021 | 
| [Updated resource](AWS_ECS.md) | The following resource was updated: AWS::ECS::TaskDefinition\. 

 [AWS::ECS::TaskDefinition EphemeralStorage](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ecs-taskdefinition-ephemeralstorage.html)   
Use the `AWS::ECS::TaskDefinition EphemeralStorage` resource to define a custom ephemeral storage setting for your Amazon ECS tasks that are hosted on AWS Fargate\.  | May 14, 2021 | 
| [Updated resource](AWS_ECS.md) | The following resource was updated: AWS::ECS::CapacityProvider\. 

 [AWS::ECS::CapacityProvider ManagedScaling](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ecs-capacityprovider-managedscaling.html)   
Use the `AWS::ECS::CapacityProvider ManagedScaling.InstanceWarmupPeriod` resource to set an instance warmup period for newly launched Amazon EC2 instances\.  | May 14, 2021 | 
| [Updated resource](AWS_EKS.md) | The following resource was updated: `AWS::EKS::Nodegroup` 

 [https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-eks-nodegroup.html](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-eks-nodegroup.html)   
Use the `Taints` property to specify whether you want to have the effect of `No_Schedule`, `Prefer_No_Schedule`, or `No_Execute` applied to your node group\.  | May 14, 2021 | 
| [Updated resource](AWS_Elasticsearch.md) | The following resource was updated: AWS::Elasticsearch::Domain\. 

 [AWS::Elasticsearch::Domain](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-elasticsearch-domain.html)   
Use the `EncryptionAtRestOptions` property to specify whether the domain should encrypt data at rest, and if so, the AWS Key Management Service \(KMS\) key to use\.  
Use the `NodeToNodeEncryptionOptions` property to specify whether node\-to\-node encryption is enabled\.  | May 14, 2021 | 
| [New resources](AWS_SSMContacts.md) | The following resources were added: AWS::SSMContacts::Contact and AWS::SSMContacts::ContactChannel 

 [AWS::SSMContacts::Contact](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ssmcontacts-contact.html)   
Use the `AWS::SSMContacts::Contact` resource to specify an Incident Manager contact or escalation plan\. 

 [AWS::SSMContacts::ContactChannel](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ssmcontacts-contactchannel.html)   
Use the `AWS::SSMContacts::ContactChannel` resource to specify a contact channel as the method that Incident Manager uses to engage your contact\.  | May 14, 2021 | 
| [New resource](AWS_DynamoDB.md) | The following resource was added: AWS::DynamoDB::GlobalTable 

 [AWS::DynamoDB::GlobalTable](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-dynamodb-globaltable.html)   
Use the `AWS::DynamoDB::GlobalTable` resource to create DynamoDB global tables\.  | May 14, 2021 | 
| [New resource](AWS_SSMIncidents.md) | The following resources were added: AWS::SSMIncidents::ReplicationSet and AWS::SSMIncidents::ResponsePlan 

 [AWS::SSMIncidents::ReplicationSet](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ssmincidents-replicationset.html)   
Use the `ReplicationSet` resource to specify a set of Regions that Incident Manager data is replicated to and the KMS key used to encrypt the data\. 

 [AWS::SSMIncidents::ResponsePlan](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ssmincidents-responseplan.html)   
Use the `ResponsePlan` resource to specify the details of the response plan that are used when creating an incident\.  | May 14, 2021 | 
| [Updated resources](AWS_ECR.md) | The following resources were updated: AWS::ECR::Repository 

 [AWS::ECR::Repository](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ecr-repository.html)   
Use the `AWS::ECR::Repository.EncryptionConfiguration` property to configure encryption for the contents of a private repository\.  | May 13, 2021 | 
| [Updated resource](AWS_S3.md) | The following resource was updated: AWS::S3::Bucket\. 

 [AWS::S3::Bucket](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-s3-bucket.html)   
Use the `ExpiredObjectDeleteMarker` property to specify whether Amazon S3 will remove a delete marker with no noncurrent versions\.  | May 13, 2021 | 
| [Updated resource](AWS_ACMPCA.md) | The following resource was updated: AWS::ACMPCA::CertificateAuthority\. 

 [AWS::ACMPCA::CertificateAuthority](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-acmpca-certificateauthority.html)   
Use the `KeyStorageSecurityStandard` property to specify the minimum FIPS key security standard\.  | May 6, 2021 | 
| [Updated resource](AWS_CloudFront.md) | The following resource was updated: AWS::CloudFront::Distribution\. 

 [AWS::CloudFront::Distribution](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-cloudfront-distribution.html)   
In the [CacheBehavior](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-cloudfront-distribution-cachebehavior.html) and [DefaultCacheBehavior](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-cloudfront-distribution-defaultcachebehavior.html) property types, use the `FunctionAssociations` property to specify the CloudFront functions associated with the cache behavior\.  
For more information, see [Customizing with CloudFront Functions](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/cloudfront-functions.html) in the *Amazon CloudFront Developer Guide*\.  | May 6, 2021 | 
| [Updated resource](AWS_GameLift.md) | The following resources were updated: AWS::GameLift:Fleet, AWS::GameLift::GameSessionQueue\. 

 [AWS::GameLift::Fleet](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-gamelift-fleet.html)   
In the `LocationCapacity` property type, use `DesiredEc2Instance` to specify the number of desired EC2 instance and `MinSize` and `MaxSize` to specify the minimum and maximum capacity size\.   
In the `LocationConfiguration` property type, use location `Location` to specify an AWS Region code and `LocationConfiguration` to specify resource capacity settings in a specified fleet\.  

 [AWS::GameLift::GameSessionQueue](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-gamelift-gamesessionqueue.html)   
Use the `PriorityConfiguration` property to specify priority destinations and locations for game session placements\.  
Use the `FilterConfiguration` property to specify a list of locations where a queue is allowed to place new game sessions\.  | May 6, 2021 | 
| [Updated resource](AWS_IoT.md) | The following resource was updated: AWS::IoT::TopicRule 

 [AWS::IoT::TopicRule](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-iot-topicrule.html)   
Use the `CloudwatchLogsAction` property to specify a Cloudwatch logs action\.  
Use the `TimestreamAction` property to specify a timestream action\.  
Use the `KafkaAction` property to specify a kafka action\.  
In the `S3Action` property, use the `CannedAcl` value to specify a canned ACL action\.  | May 6, 2021 | 
| [Updated resource](AWS_MSK.md) | The following resource was updated: AWS::MSK::Cluster 

 [AWS::MSK::Cluster](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-msk-cluster.html)   
You can now create clusters with IAM access control\. This enables you to authenticate clients, as well as to authorize Apache Kafka actions\.  | May 6, 2021 | 
| [New resources](AWS_FraudDetector.md) | The following resources were added: AWS::FraudDetector::Detector, AWS::FraudDetector::EntityType, AWS::FraudDetector::EventType, AWS::FraudDetector::Label, AWS::FraudDetector::Outcome, and AWS::FraudDetector::Variable 

 [AWS::FraudDetector::Detector](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-frauddetector-detector.html)   
Use the `AWS::FraudDetector::Detector` resource to manage a detector or associated detector versions in Amazon Fraud Detector\. 

 [AWS::FraudDetector::EntityType](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-frauddetector-entitytype.html)   
Use the `AWS::FraudDetector::EntityType` resource to create or update an entity type in Amazon Fraud Detector\. 

 [AWS::FraudDetector::EventType](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-frauddetector-eventtype.html)   
Use the `AWS::FraudDetector::EventType` resource to create or update an event type in Amazon Fraud Detector\. 

 [AWS::FraudDetector::Label](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-frauddetector-label.html)   
Use the `AWS::FraudDetector::Label` resource to create or update label in Amazon Fraud Detector\. 

 [AWS::FraudDetector::Outcome](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-frauddetector-outcome.html)   
Use the `AWS::FraudDetector::Outcome` resource to create or update an outcome in Amazon Fraud Detector\. 

 [AWS::FraudDetector::Variable](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-frauddetector-variable.html)   
Use the `AWS::FraudDetector::Variable` resource to create a variable in Amazon Fraud Detector\.  | May 6, 2021 | 
| [New resources](AWS_XRay.md) | The following resources were added: AWS::XRay::Group and AWS::XRay::SamplingRule\. 

 [AWS::XRay::Group](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-xray-group.html)   
Use the `AWS::XRay::Group` resource to specify an X\-Ray group\. 

 [AWS::XRay::SamplingRule](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-xray-samplingrule.html)   
Use the `AWS::XRay::SamplingRule` resource to specify an X\-Ray sampling rule\.  | May 6, 2021 | 
| [New resource](AWS_CloudFront.md) | The following resource was added: AWS::CloudFront::Function\. 

 [AWS::CloudFront::Function](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-cloudfront-function.html)   
Use the `AWS::CloudFront::Function` resource to create a function in CloudFront Functions\.  
For more information, see [Customizing with CloudFront Functions](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/cloudfront-functions.html) in the *Amazon CloudFront Developer Guide*\.  | May 6, 2021 | 
| [New resource](AWS_FinSpace.md) | The following resource was added: AWS::FinSpace::Environment 

 [AWS::FinSpace::Environment](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-finspace-environment.html)   
Use the `AWS::FinSpace::Environment` resource to specify an Amazon FinSpace environment\.  | May 6, 2021 | 
| [Updated resource](AWS_Detective.md) | The following resource was updated: AWS::Detective::Graph 

[AWS::Detective::Graph](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-detective-graph.html)  
Use the `Tags` property to assign tag values to the behavior graph\.  | April 29, 2021 | 
| [New resource](AWS_IoTFleetHub.md) | The following resource was added: AWS::IoTFleetHub::Application 

 [AWS::IoTFleetHub::Application](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-iotfleethub-application.html)   
Use the `AWS::IoTFleetHub::Application` resource to create a Fleet Hub for AWS IoT Device Management web application\.  | April 29, 2021 | 
| [New resource](AWS_SES.md) | The following resource was added: AWS::SES::ContactList 

 [AWS::SES::ContactList](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ses-contactlist.html)   
Use the `AWS::SES::ContactList` resource to create a list that contains contacts that have subscribed to a particular topic or topics\.  | April 29, 2021 | 
| [Updated resource](AWS_IAM.md) | The following resources were updated: AWS::IAM::InstanceProfile and AWS::IAM::ManagedPolicy\. 

 [AWS::IAM::InstanceProfile](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-iam-instanceprofile.html)   
Use the `Tags` property to specify a list of tags that you want to attach to the newly created instance profile\. 

 [AWS::IAM::ManagedPolicy](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-iam-managedpolicy.html)   
Use the `Tags` property to specify a list of tags that you want to attach to the newly created managed policy\.  | April 27, 2021 | 
| [New resources](AWS_IoTWireless.md) | The following resources were added: AWS::IoTWireless::PartnerAccount, AWS::IoTWireless::TaskDefinition 

 [AWS::IoTWireless::PartnerAccount](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-iotwireless-partneraccount.html)   
 Gets information about a partner account\. If `PartnerAccountId` and `PartnerType` are `null`, returns all partner accounts\.  

 [AWS::IoTWireless::TaskDefinition](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-iotwireless-taskdefinition.html)   
 Gets information about the gateway task definition for a wireless gateway\.   | April 26, 2021 | 
| [New resources](AWS_NimbleStudio.md) | The following resources were added: AWS::NimbleStudio::Studio, AWS::NimbleStudio::StudioComponent, AWS::NimbleStudio::StreamingImage, and AWS::NimbleStudio::LaunchProfile\. 

 [AWS::NimbleStudio::Studio](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-nimblestudio-studio.html)   
Use the `AWS::NimbleStudio::Studio` resource to specify a studio resource\. 

 [AWS::NimbleStudio::StudioComponent](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-nimblestudio-studiocomponent.html)   
Use the `AWS::NimbleStudio::StudioComponent` resource to configure studio components, including types of workstations, render farms, license servers, and shared file systems\. 

 [AWS::NimbleStudio::StreamingImage](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-nimblestudio-streamingimage.html)   
Use the `AWS::NimbleStudio::StreamingImage` resource to configure a machine image, including operating system and software, that can be launched as a virtual workstation in a streaming session\. 

 [AWS::NimbleStudio::LaunchProfile](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-nimblestudio-launchprofile.html)   
Use the `AWS::NimbleStudio::LaunchProfile` resource to specify user access permissions to studio components\.  | April 26, 2021 | 
| [Updated resources](AWS_ElastiCache.md) | AWS::ElastiCache::CacheCluster, AWS::ElastiCache::ReplicationGroup\. 

 [AWS::ElastiCache::CacheCluster](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-elasticache-cache-cluster.html)   
You can now specify log delivery to a CloudWatch Logs or Kinesis Data Firehose destination\.  

 [AWS::ElastiCache::ReplicationGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-elasticache-replicationgroup.html)   
You can now specify log delivery to a CloudWatch Logs or Kinesis Data Firehose destination\.   | April 22, 2021 | 
| [Updated resources](AWS_WAFv2.md) | The following resources were updated: AWS::WAFv2::WebACL and AWS::WAFv2::RuleGroup\. 

 [AWS::WAFv2::WebACL](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-wafv2-webacl.html)   
You can now nest rule statements without using different names for statements at different levels\. For example, instead of using `AndStatementOne` and `AndStatementTwo` to nest an `AND` rule statement inside another `AND` rule statement, you can use `AndStatement` for both\. The new statement properties are `AndStatement`, `NotStatement`, `OrStatement`, `RateBasedStatement`, and `Statement`\.  

 [AWS::WAFv2::RuleGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-wafv2-rulegroup.html)   
You can now nest rule statements without using different names for statements at different levels\. For example, instead of using `AndStatementOne` and `AndStatementTwo` to nest an `AND` rule statement inside another `AND` rule statement, you can use `AndStatement` for both\. The new statement properties are `AndStatement`, `NotStatement`, `OrStatement`, `RateBasedStatement`, and `Statement`\.   | April 22, 2021 | 
| [Updated resource](AWS_ResourceGroups.md) | The following resource was updated: AWS::ResourceGroups::Group 

 [AWS::ResourceGroups::Group](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-resourcegroups-group.html)   
Use the `Configuration` property to specify settings for an AWS service that automatically apply to members of the resource group\.  | April 22, 2021 | 
| [New resource](AWS_AutoScaling.md) | The following resource was added: AWS::AutoScaling::WarmPool\. 

 [AWS::AutoScaling::WarmPool](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-autoscaling-warmpool.html)   
Use the `AWS::AutoScaling::WarmPool` resource to specify a warm pool for an Auto Scaling group\.   | April 22, 2021 | 
| [Updated resources](AWS_CloudFormation.md) | The following resource was updated: AWS::CloudFormation::StackSet\. 

 [AWS::CloudFormation::StackSet](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-cloudformation-stackset.html)  
Use the `RegionConcurrencyType` property type to specify the concurrency type of deploying StackSets operations in Regions\.  | April 15, 2021 | 
| [Updated resource](AWS_ApiGateway.md) | The following resource was updated: AWS::ApiGateway::RestApi\. 

 [AWS::ApiGateway::RestApi](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-apigateway-restapi.html)   
Use the `Mode` property to specify how API Gateway handles resource updates when you use OpenAPI to define your REST API\.  | April 15, 2021 | 
| [Updated resource](AWS_IVS.md) | The following resource was updated: AWS::IVS::Channel 

 [AWS::IVS::Channel](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ivs-channel.html)   
Use the `RecordingConfiguration` property to specify an Amazon IVS RecordingConfiguration, which stores configuration information related to recording your live stream to a data store\.  | April 15, 2021 | 
| [New resources](AWS_EC2.md) | The following resource was added: AWS::EC2::EnclaveCertificateIamRoleAssociation\. 

 [AWS::EC2::EnclaveCertificateIamRoleAssociation](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-enclavecertificateiamroleassociation.html)   
Use the `EnclaveCertificateIamRoleAssociation` resource to associate an AWS Identity and Access Management \(IAM\) role with an AWS Certificate Manager \(ACM\) certificate\.  | April 15, 2021 | 
| [New resource](AWS_IVS.md) | The following resource was added: AWS::IVS::RecordingConfiguration 

 [AWS::IVS::RecordingConfiguration](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ivs-recordingconfiguration.html)   
Use the `AWS::IVS::RecordingConfiguration` resource to specify an Amazon IVS RecordingConfiguration, which stores configuration information related to recording your live stream to a data store\.  | April 15, 2021 | 
| [Reference macros in stack set templates](#ReleaseHistory) | StackSets now supports creating or updating stack sets with self\-managed permissions from templates that reference macros\.For more information about macros, see [Using AWS CloudFormation macros to perform custom processing on templates](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/template-macros.html)\. | April 14, 2021 | 
| [Use the latest value of an SSM parameter in a dynamic reference\.](#ReleaseHistory) | When using dynamic references, you can now have CloudFormation use the latest version of an SSM parameter whenever you create or update a stack\. You are no longer required to specify a specific version\.For more details, see [SSM parameters](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/dynamic-references.html#dynamic-references-ssm)\. | April 13, 2021 | 
| [Updated resources](AWS_ElastiCache.md) | AWS::ElastiCache::ParameterGroup, AWS::ElastiCache::SecurityGroup, AWS::ElastiCache::SubnetGroup\. 

 [AWS::ElastiCache::ParameterGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-elasticache-parameter-group.html)   
You can now add tags to the AWS::ElastiCache::ParameterGroup type\.  

 [AWS::ElastiCache::SecurityGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-elasticache-security-group.html)   
You can now add tags to the AWS::ElastiCache::SecurityGroup resource\.  

 [AWS::ElastiCache::SubnetGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-elasticache-subnet-group.html)   
You can now add tags to the AWS::ElastiCache::SubnetGroup resource\.   | April 8, 2021 | 
| [Updated resource](AWS_DynamoDB.md) | The following resource was updated: AWS::DynamoDB::Table\. 

 [AWS::DynamoDB::Table](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-dynamodb-table.html)   
Use the `KinesisStreamSpecification` property to specify the Kinesis Data Streams configuration for a table\.  | April 8, 2021 | 
| [Modules support using period delimiters in resource names](#ReleaseHistory) | You can now use a period as a delimiter in specifying the fully\-qualified logical name for a resource contained in a module\.For more information, see [Referencing resources in a module](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/modules.html#module-ref-resources)\. | April 8, 2021 | 
| [AWS CloudFormation StackSets now supports parallel region deployment](#ReleaseHistory) | You can now choose to deploy StackSets into Regions sequentially or in parallel\.For more information, see [Stack set operation options](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/stacksets-concepts.html#stackset-ops-options)\. | April 6, 2021 | 
| [Updated resources](AWS_DataBrew.md) | The following resources were updated: AWS::DataBrew::Dataset and AWS::DataBrew::Job 

 [AWS::DataBrew::Dataset](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-databrew-dataset.html)   
Use the `CsvOptions` property to define how DataBrew will read a comma\-separated value \(CSV\) file when creating a dataset from that file\.  
Use the `DatabaseInputDefinition` property to define connection information for dataset input files stored in a database\.   
Use the `DataCatalogInputDefinition` property to define how metadata stored in the AWS Glue Data Catalog is defined in a DataBrew dataset\.   
Use the `DatasetParameter` property to define the type and conditions for a parameter in the Amazon S3 path of the dataset\.  
Use the `DatetimeOptions` property to define the correct interpretation of datetime parameters used in the Amazon S3 path of a dataset\.   
Use the `ExcelOptions` property to define how DataBrew will interpret a Microsoft Excel file when creating a dataset from that file\.   
Use the `FilesLimit` property to limit the number of Amazon S3 files that should be selected for a dataset from a connected Amazon S3 path\.  
Use the `FilterExpression` property to define parameter conditions\.  
Use the `FilterValue` property to define a single entry in the `ValuesMap` of a `FilterExpression`\.  
Use the `FormatOptions` property to define the structure of either comma\-separated value \(CSV\), Excel, or JSON input\.   
Use the `Input` property to define how DataBrew can find data, in either the AWS Glue Data Catalog or Amazon S3\.   
Use the `JsonOptions` property to define how input is to be interpreted by AWS Glue DataBrew\.   
Use the `PathOptions` property to define how DataBrew selects files for a given Amazon S3 path in a dataset\.   
Use the `PathParameter` property to define the file format of a dataset\.  
Use the `S3Location` property to define a single entry in the path parameters of a dataset\. 

 [AWS::DataBrew::Job](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-databrew-job.html)  
Use the `JobSample` property to define the number of rows on which a profile job is run\.  
Use the `OutputLocation` property to define the location in Amazon S3 where the job writes its output\.   
Use the `Recipe` property to define the actions to be performed on a dataset\.  | April 1, 2021 | 
| [Updated resources](AWS_WAFv2.md) | The following resources were updated: AWS::WAFv2::WebACL and AWS::WAFv2::RuleGroup\. 

 [AWS::WAFv2::WebACL](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-wafv2-webacl.html)   
You can now inspect a web request body as JSON\. You can now add custom request and response handling to web ACL default action and rule action settings\. You can now define labels for rules, which are added automatically to matching requests and that persist with requests during web ACL evaluation\. You can match against labels using the new rule `LabelMatchStatement`\. You can now add a scope\-down statement to managed rule group statements\. 

 [AWS::WAFv2::RuleGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-wafv2-rulegroup.html)   
You can now inspect a web request body as JSON\. You can now add custom request and response handling to rule action settings\. You can now define labels for rules, which are added automatically to matching requests and that persist with requests during web ACL evaluation\. You can match against labels using the new rule `LabelMatchStatement`\.   | April 1, 2021 | 
| [Updated resource ](AWS_Config.md) | The following resource was updated: AWS::Config::DeliveryChannel\. 

 [ AWS::Config::DeliveryChannel](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-config-deliverychannel.html)   
Use the `S3KmsKeyArn` property to specify the Amazon Resource Name \(ARN\) of the AWS Key Management Service \(KMS\) customer managed key \(CMK\) used to encrypt objects delivered by AWS Config\.  | April 1, 2021 | 
| [Updated resource](AWS_ApiGateway.md) | The following resource was updated: AWS::ApiGateway::RestApi\. 

 [AWS::ApiGateway::RestApi](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-apigateway-restapi.html)   
Use the `DisableExecuteApiEndpoint` property to disable the default endpoint for a REST API\.  | April 1, 2021 | 
| [Updated resource](AWS_Budgets.md) | The following resource was updated: AWS::Budgets::BudgetsAction 

 [AWS::Budgets::BudgetsAction](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-budgets-budgetsaction.html)   
Use the `AWS::Budgets::BudgetsAction` resource to take predefined actions that are initiated when a budget threshold has been exceeded\.  | April 1, 2021 | 
| [Updated resource](AWS_Cloud9.md) | The following resource was updated: AWS::Cloud9::EnvironmentEC2 

 [AWS::Cloud9::EnvironmentEC2](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ws-resource-cloud9-environmentec2.html.html)   
Use the `ImageId` property to specify the Amazon Machine Image \(AMI\) that's used to create the EC2 instance\.  | April 1, 2021 | 
| [Updated resource](AWS_EC2.md) | The following resource was updated: AWS::EC2::LaunchTemplate\. 

 [AWS::EC2::LaunchTemplate](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-launchtemplate.html)   
Use the `TagSpecifications` property to tag a launch template on creation\.  | April 1, 2021 | 
| [Updated resource](AWS_ElasticBeanstalk.md) | The following resource was updated: AWS::ElasticBeanstalk::Environment\. 

 [AWS::ElasticBeanstalk::Environment](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-beanstalk-environment.html)   
Use the `OperationsRole` property to specify the Amazon Resource Name \(ARN\) of an existing IAM role to be used as the environment's operations role\.  | April 1, 2021 | 
| [Updated resource](AWS_Events.md) | The following resource was updated: [AWS::Events::Rule](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-events-rule.html)\. 

 [AWS::Events::Rule](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-events-rule.html)   
The [SageMakerPipelineParameter](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-events-rule-sagemakerpipelineparameter.html) property is a Name / Value pair of a parameter to start execution of a SageMaker Model Building Pipeline to create an API destination\. An API destination defines an HTTP invocation endpoint to use as the target of a rule\.  
The [SageMakerPipelineParameters](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-events-rule-sagemakerpipelineparameters.html) contains the SageMaker Model Building Pipeline parameters to start execution of a SageMaker Model Building Pipeline\.  | April 1, 2021 | 
| [Updated resource](AWS_FMS.md) | The following resource was updated: AWS::FMS::Policy\. 

 [AWS::FMS::Policy](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-fms-policy.html)   
The `AWS::FMS::Policy` resource now allows you to manage DNS Firewall policies for Amazon Route 53 Resolver DNS Firewall\.   | April 1, 2021 | 
| [Updated resource](AWS_GameLift.md) | The following resource was updated: AWS::GameLift::GameSessionQueue\. 

 [AWS::GameLift::GameSessionQueue](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-gamelift-gamesessionqueue.html)   
Use the `NotificationTarget` property to specify an SNS topic ARN to publish game session placement events that are emitted by the queue\.  
Use the `CustomEventData` property to specify a string value to add to all game session placement events that are emitted by the queue\.  | April 1, 2021 | 
| [New resources](AWS_Route53Resolver.md) | The following resources were added: `AWS::Route53Resolver::FirewallDomainList`, `AWS::Route53Resolver::FirewallRuleGroup`, `AWS::Route53Resolver::FirewallRuleGroupAssociation` 

[AWS::Route53Resolver::FirewallDomainList](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-route53resolver-firewalldomainlist.html)  
Use the `AWS::Route53Resolver::FirewallDomainList` resource to specify a domain list configuration for Route 53 Resolver DNS Firewall\. 

[AWS::Route53Resolver::FirewallRuleGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-route53resolver-firewallrulegroup.html)  
Use the `AWS::Route53Resolver::FirewallRuleGroup` resource to specify a rule group configuration for Route 53 Resolver DNS Firewall\. 

[AWS::Route53Resolver::FirewallRuleGroupAssociation](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-route53resolver-firewallrulegroupassociation.html)  
Use the `AWS::Route53Resolver::FirewallRuleGroupAssociation` resource to specify an association between a firewall rule group and a VPC\.  | April 1, 2021 | 
| [New resource](AWS_CloudWatch.md) | The following resource was added: AWS::CloudWatch::MetricStream\. 

 [AWS::CloudWatch::MetricStream](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-cloudwatch-metricstream.html)   
Use the AWS::CloudWatch::MetricStream resource to create a metric stream of CloudWatch metric data to a destination of your choice\. For more information, see [ Metric streams](https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/CloudWatch-Metric-Streams.html)\.  | April 1, 2021 | 
| [New resource](AWS_Logs.md) | The following resource was added : AWS::Logs::QueryDefinition 

 [AWS::Logs::QueryDefinition](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-logs-querydefinition.html)   
Use the `AWS::Logs::QueryDefinition` resource to create a CloudWatch Logs Insights query definition\. For more information, see [ Analyzing Log Data with CloudWatch Logs Insights](https://docs.aws.amazon.com/AmazonCloudWatch/latest/logs/AnalyzingLogData.html)\.  | April 1, 2021 | 
| [Updated resource](AWS_Batch.md) | The following resource was updated: [AWS::Batch::JobDefinition](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-batch-jobdefinition.html) 

[AWS::Batch::JobDefinition](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-batch-jobdefinition.html)  
In the [Volumes](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-batch-jobdefinition-volumes.html) property type, use the [EfsVolumeConfiguration](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-batch-jobdefinition-volumes.html#cfn-batch-jobdefinition-volumes-efsvolumeconfiguration) property to specify the Amazon EFS configuration for a job definition\.  | March 31, 2021 | 
| [New resources](AWS_LookoutMetrics.md) | The following resources were added: AWS::LookoutMetrics::Alert 

 [AWS::LookoutMetrics::Alert](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-lookoutmetrics-alert.html)   
Use the `AWS::LookoutMetrics::Alert` resource to specify an alert for an anomaly detector\. 

 [AWS::LookoutMetrics::AnomalyDetector](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-lookoutmetrics-anomalydetector.html)   
Use the `AWS::LookoutMetrics::AnomalyDetector` resource to specify an anomaly detector\.  | March 25, 2021 | 
| [New resource](AWS_AppIntegrations.md) | The following resource was added: AWS::AppIntegrations::EventIntegration 

 [AWS::AppIntegrations::EventIntegration](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-appintegrations-eventintegration.html)   
Use the `AWS::AppIntegrations::EventIntegration` resource to create an EventIntegration\.  | March 25, 2021 | 
| [New resources](AWS_CustomerProfiles.md) | The following resources were added: AWS::CustomerProfiles::Domain, AWS::CustomerProfiles::Integration and AWS::CustomerProfiles::ObjectType\. 

 [AWS::CustomerProfiles::Domain](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-customerprofiles-domain.html)   
Use the `AWS::CustomerProfiles::Domain` resource to create a new domain in Amazon Connect Customer Profiles Service\. 

 [AWS::CustomerProfiles::Integration](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-customerprofiles-integration.html)   
Use the `AWS::CustomerProfiles::Integration` resource to create a new integration in Amazon Connect Customer Profiles Service\. 

 [AWS::CustomerProfiles::ObjectType](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-customerprofiles-objecttype.html)   
Use the `AWS::CustomerProfiles::ObjectType` resource to create a new object type in Amazon Connect Customer Profiles Service\.  | March 24, 2021 | 
| [Updated resource](AWS_ServiceDiscovery.md) | The following resource was updated: `AWS::ServiceDiscovery::Service`\. 

[AWS::ServiceDiscovery::Service](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-servicediscovery-service.html)   
Use the `Type` property to allow service instances in a service in a public or private DNS namespace to only be discovered with the `DiscoverInstances` API operation\.  | March 18, 2021 | 
| [New resource](AWS_FIS.md) | The following resource was added: AWS::FIS::ExperimentTemplate\. 

 [AWS::FIS::ExperimentTemplate](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-fis-experimenttemplate.html)   
Use the `AWS::FIS::ExperimentTemplate` resource to create an experiment template in AWS Fault Injection Simulator\.  | March 18, 2021 | 
| [New resource](AWS_S3ObjectLambda.md) | The following resources were added: AWS::S3ObjectLambda::AccessPoint and AWS::S3ObjectLambda::AccessPointPolicy 

 [AWS::S3ObjectLambda::AccessPoint](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-s3objectlambda-accesspoint.html)   
Use the `AWS::S3ObjectLambda::AccessPoint` resource to create a S3 Object Lambda access point\. 

 [AWS::S3ObjectLambda::AccessPointPolicy](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-s3objectlambda-accesspointpolicy.html)   
Use the `AWS::S3ObjectLambda::AccessPointPolicy` resource to create a policy for your S3 Object Lambda access point\.  | March 18, 2021 | 
| [New resources](AWS_ECS.md) | The following resources were updated: AWS::ECS::Service\. 

 [AWS::ECS::Service](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ecs-service.html)   
Use the `AWS::ECS::Service` resource and the `EnableExecuteCommand` property to turn on ECS Exec for the tasks in a service\.  | March 16, 2021 | 
| [New resources](AWS_ECS.md) | The following resources were updated: AWS::ECS::Cluster ExecuteCommandLogConfiguration\. 

 [AWS::ECS::Cluster ExecuteCommandLogConfiguration](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ecs-cluster-executecommandlogconfiguration.html)   
Use the `AWS::ECS::Cluster ExecuteCommandLogConfiguration` resource to define a logging configuration for the ECS Exec actions on the tasks in a cluster\.  | March 16, 2021 | 
| [New resources](AWS_ECS.md) | The following resources were updated: AWS::ECS::Cluster ExecuteCommandConfiguration\. 

 [AWS::ECS::Cluster ExecuteCommandConfiguration](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ecs-cluster-executecommandconfiguration.html)   
Use the `AWS::ECS::Cluster ExecuteCommandConfiguration` resource to turn on ECS Exec for a cluster\.  | March 16, 2021 | 
| [Updated resource](AWS_Detective.md) | The following resource was updated: AWS::Detective::MemberInvitation 

[AWS::Detective::MemberInvitation](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-detective-memberinvitation.html)  
Use the `DisableEmailNotification` property to prevent the sending of invitation emails to member accounts\.  
The term "master account" is changed to "administrator account\."  | March 15, 2021 | 
| [Updated resources](AWS_ECR.md) | The following resources were updated: AWS::ECR::PublicRepository 

 [AWS::ECR::PublicRepository](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ecr-replicationconfiguration.html)   
Use the `AWS::ECR::PublicRepository.Tags` property to add tags to your public repositories\.  | March 11, 2021 | 
| [Updated resource](AWS_CertificateManager.md) | The following resource was updated: AWS::CertificateManager::Account 

 [AWS::CertificateManager::Account](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-certificatemanager-account.html)   
Use the `ExpiryEventsConfiguration` property to specify options for certificate expiration events associated with an AWS account\.  | March 11, 2021 | 
| [Updated resource](AWS_EFS.md) | The following resource was updated: AWS::EFS::FileSystem 

[AWS::EFS::FileSystem](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-efs-filesystem.html#cfn-efs-filesystem-availabilityzonename)  
Use the `AvailabilityZoneName` property to create a file system that uses EFS One Zone storage classes, which store data redundantly within a single Availability Zone within an AWS Region\.  | March 11, 2021 | 
| [New resources](AWS_CE.md) | The following resources were added: AWS::CE::AnomalySubscription and AWS::CE::AnomalyMonitor\. 

 [AWS::CE::AnomalySubscription](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ce-anomalysubscription.html)   
Use the `AWS::CE::AnomalySubscription` resource to deliver notifications about anomalies detected by a monitor that exceeds a threshold\.  

 [AWS::CE::AnomalyMonitor](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ce-anomalymonitor.html)   
Use the `AWS::CE::AnomalyMonitor` resource to continuously inspect your account's cost data for anomalies, based on `MonitorType` and `MonitorSpecification`\.  | March 11, 2021 | 
| [New resources](AWS_ECS.md) | The following resources were updated: AWS::ECS::ClusterCapacityProviderAssociations\. 

 [AWS::ECS::ClusterCapacityProviderAssociations](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ecs-clustercapacityproviderassociations.html)   
Use the `AWS::ECS::ClusterCapacityProviderAssociations` resource to associate capacity providers with a cluster\.  | March 11, 2021 | 
| [New resource](AWS_RDS.md) | The following resource was added: AWS::RDS::DBProxyEndpoint\. 

 [AWS::RDS::DBProxyEndpoint](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-rds-dbproxyendpoint.html)   
Use the `AWS::RDS::DBProxyEndpoint` resource to create or update a custom DB proxy endpoint\.  | March 11, 2021 | 
| [Updated resource](AWS_StepFunctions.md) | The following resource was updated: `AWS::StepFunctions::StateMachine`\. 

 [AWS::StepFunctions::StateMachine](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-stepfunctions-statemachine.html)   
The `AWS::StepFunctions::StateMachine` has a new `Definition` property that lets you define your state machine in the language of your template file\.   | March 10, 2021 | 
| [Updated resource](AWS_AutoScaling.md) | The following resource was updated: AWS::AutoScaling::AutoScalingGroup\. 

 [AWS::AutoScaling::AutoScalingGroup MixedInstancesPolicy](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-autoscaling-autoscalinggroup-mixedinstancespolicy.html)   
Use the `SpotAllocationStrategy` property to specify `capacity-optimized-prioritized` as the allocation strategy for your Spot capacity when you use a mixed instances policy\.  | March 8, 2021 | 
| [Updated resource](AWS_SecretsManager.md) | The following new resource was updated: `AWS::SecretsManager::Secret` 

[AWS::SecretsManager::Secret](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-secretsmanager-secret.html)  
Use the `ReplicaRegions` property to replicate secrets into additional Regions for resiliency and disaster recovery\.  | March 4, 2021 | 
| [New resource](AWS_Events.md) | The following resource was added: AWS::Events::ApiDestination\. 

 [AWS::Events::ApiDestination](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-events-apidestination.html)   
Use the `ApiDestination` resource to create an API destination\. An API destination defines an HTTP invocation endpoint to use as the target of a rule\.  | March 4, 2021 | 
| [New resource](AWS_Events.md) | The following resource was added: AWS::Events::Connection\. 

 [AWS::Events::Connection](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-events-connection.html)   
Use the `Connection` resource to create a connection to use with Api destinations\. A connection defines the authorization method and parameters to use to connect to the HTTP invocation endpoint for an Api destination\.  | March 4, 2021 | 
| [New resource](AWS_IoT.md) | The following resources were added: AWS::IoT::AccountAuditConfiguration,AWS::IoT::CustomMetric, AWS::IoT::Dimension, AWS::IoT::MitigationAction, AWS::IoT::ScheduledAudit, AWS::IoT::SecurityProfile\. 

 [AWS::IoT::AccountAuditConfiguration](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-iot-accountauditconfiguration.html)   
Use the `AWS::IoT::AccountAuditConfiguration` resource to specify an account audit configuration in AWS IoT Core\. 

 [AWS::IoT::CustomMetric](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-iot-custommetric.html)   
Use the `AWS::IoT::CustomMetric` resource to specify a custom metric in AWS IoT Core\. 

 [AWS::IoT::Dimension](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-iot-dimension.html)   
Use the `AWS::IoT::Dimension` resource to specify a dimension in AWS IoT Core\. 

 [AWS::IoT::MitigationAction](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-iot-mitigationaction.html)   
Use the `AWS::IoT::MitigationAction` resource to specify a mitigation action in AWS IoT Core\. 

 [AWS::IoT::ScheduledAudit](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-iot-scheduledaudit.html)   
Use the `AWS::IoT::ScheduledAudit` resource to specify a Scheduled Audit in AWS IoT Core\. 

 [AWS::IoT::SecurityProfile](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-iot-securityprofile.html)   
Use the `AWS::IoT::SecurityProfile` resource to specify a security profile in AWS IoT Core\.  | March 4, 2021 | 
| [New resource](AWS_S3Outposts.md) | The following resources were added: AWS::S3Outposts::Bucket, AWS::S3Outposts::BucketPolicy, AWS::S3Outposts::AccessPoint, and AWS::S3Outposts::EndPoint 

 [AWS::S3Outposts::Bucket](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-s3outposts-bucket.html)   
Use the `AWS::S3Outposts::Bucket` resource to create an S3 on Outposts bucket\. 

 [AWS::S3Outposts::BucketPolicy](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-s3outposts-bucketpolicy.html)   
Use the `AWS::S3Outposts::BucketPolicy` resource to create a bucket policy for your S3 on Outposts bucket\. 

 [AWS::S3Outposts::AccessPoint](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-s3outposts-accesspoint.html)   
Use the `AWS::S3Outposts::AccessPoint` resource to create an access point for your S3 on Outposts bucket\. 

 [AWS::S3Outposts::EndPoint](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-s3outposts-endpoint.html)   
Use the `AWS::S3Outposts::EndPoint` resource to create an endpoint for Amazon S3 on AWS Outposts\.  | March 4, 2021 | 
| [Updated resource](AWS_IoTSiteWise.md) | The following resources were updated: AWS::IoTSiteWise::AccessPolicy and AWS::IoTSiteWise::Portal\. 

 [ AWS::IoTSiteWise::AccessPolicy](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-iotsitewise-accesspolicy.html)   
Added the following properties: `IamRole` and `IamUser`\. 

 [AWS::IoTSiteWise::Portal](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-iotsitewise-portal.html)   
Added the following property: `PortalAuthMode`\.  | March 2, 2021 | 
| [Updated resource](AWS_IoTSiteWise.md) | The following resource was updated: AWS::IoTSiteWise::AssetModel\. 

 [ AWS::IoTSiteWise::AssetModel](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-iotsitewise-assetmodel.html)   
Added the following property: `AssetModelCompositeModel`\.  
You can use this property to define an alarm in AWS IoT SiteWise\.  
For more information, see [Monitoring data with alarms](https://docs.aws.amazon.com/iot-sitewise/latest/userguide/industrial-alarms.html) in the *AWS IoT SiteWise User Guide*\.  | March 1, 2021 | 
| [Updated resource](AWS_DataBrew.md) | The following resource was updated: AWS::DataBrew::Dataset Format\. 

 [AWS::DataBrew::Dataset Format](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-databrew-dataset.html#cfn-databrew-dataset-format)   
Use the `Format` property to define the file format of a dataset\.  | February 25, 2021 | 
| [Updated resource](AWS_ManagedBlockchain.md) | The following resource was updated: AWS::ManagedBlockchain::Node 

 [AWS::ManagedBlockchain::Node](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-managedblockchain-node.html)   
Use the `NodeConfiguration` property to create a node on an Ethereum network\.  | February 25, 2021 | 
| [Updated resource](AWS_SageMaker.md) | The following resource was updated: AWS::SageMaker::Model 

 [AWS::SageMaker::Model](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-sagemaker-model.html)   
Use the `InferenceExecutionConfig` property to specify details of how containers in a multi\-container endpoint are called\.  | February 25, 2021 | 
| [New resources](AWS_EC2.md) | The following resource was added: AWS::EC2::TransitGatewayConnect\. 

 [AWS::EC2::TransitGatewayConnect](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-transitgatewayconnect.html)   
Use the `TransitGatewayConnect` resource to create a Connect attachment from a specified transit gateway attachment\.  | February 25, 2021 | 
| [New resources](AWS_EMR.md) | The following resources were added: AWS::EMR::Studio and AWS::EMR::StudioSessionMapping\. 

 [AWS::EMR::Studio](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-emr-studio.html)   
Use the `AWS::EMR::Studio` resource to create a new Amazon EMR Studio\. 

 [AWS::EMR::StudioSessionMapping](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-emr-studiosessionmapping.html)   
Use the `AWS::EMR::StudioSessionMapping` resource to assign a user or group to an Amazon EMR Studio, and apply an IAM session policy to refine Studio permissions for that user or group\.  | February 25, 2021 | 
| [New resources](AWS_SageMaker.md) | The following resources were added: AWS::SageMaker::Image, AWS::SageMaker::ImageVersion\. 

 [AWS::SageMaker::Image](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-sagemaker-image.html)   
Use the `AWS::SageMaker::Image` resource to create a new Image in Amazon SageMaker\. 

 [AWS::SageMaker::ImageVersion](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-sagemaker-imageversion.html)   
Use the `AWS::SageMaker::ImageVersion` resource to create a new ImageVersion in Amazon SageMaker\.  | February 25, 2021 | 
| [New resource](AWS_EKS.md) | The following resource was added: `AWS::EKS::Addon`\. 

 [https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-eks-addon.html](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-eks-addon.html)   
Use the `AWS::EKS::Addon` resource to create an Amazon EKS add\-on\.  | February 25, 2021 | 
| [New resource](AWS_IAM.md) | The following resources were added: AWS::IAM::OIDCProvider, AWS::IAM::SAMLProvider, AWS::IAM::ServerCertificate, and AWS::IAM::VirtualMFADevice\. 

 [AWS::IAM::OIDCProvider](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-iam-oidcprovider.html)   
Use the `AWS::IAM::OIDCProvider` resource to create an IAM entity to describe an identity provider \(IdP\) that supports OpenID Connect \(OIDC\)\. 

 [AWS::IAM::SAMLProvider](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-iam-samlprovider.html)   
Use the `AWS::IAM::SAMLProvider` resource to create an IAM resource that describes an identity provider \(IdP\) that supports SAML 2\.0\. 

 [AWS::IAM::ServerCertificate](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-iam-servercertificate.html)   
Use the `AWS::IAM::ServerCertificate` resource to retrieve information about the specified server certificate stored in IAM\. 

 [AWS::IAM::VirtualMFADevice](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-iam-virtualmfadevice.html)   
Use the `AWS::IAM::VirtualMFADevice` resource to create a new virtual MFA device for the AWS account\.  | February 25, 2021 | 
| [New attributes](AWS_Pinpoint.md) | The following parameters were added for 10DLC support: EntityId, TemplateId, OriginationNumber\. 

 [AWS::Pinpoint::Campaign CampaignSmsMessage](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-pinpoint-campaign-campaignsmsmessage.html)   
Specifies the content and settings for an SMS message that's sent to recipients of a campaign\.   | February 24, 2021 | 
| [Updated resource](AWS_DynamoDB.md) | The following resource was updated: AWS::DynamoDB::Table 

 [AWS::DynamoDB::Table](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-dynamodb-table.html)   
Use the `ContributorInsightsSpecification` property to enable or disable CloudWatch Contributor Insights on a table or global secondary index\.  | February 22, 2021 | 
| [Updated resource](AWS_CodeCommit.md) | The following resource was updated: AWS::CodeCommit::Repository Code 

 [AWS::CodeCommit::Repository Code](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-codecommit-repository-code.html)   
The behavior of the `BranchName` property on update has changed to be consistent with all other aspects of `AWS:CodeCommit:Repository Code`\. All properties of `AWS:CodeCommit:Repository Code` are ignored on update, as they only apply to initial resource creation\.  | February 19, 2021 | 
| [Updated resources](AWS_AppMesh.md) | The following resources were updated: AWS::AppMesh::VirtualNode and AWS::AppMesh::VirtualGateway 

 [AWS::AppMesh::VirtualNode](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-appmesh-virtualnode.html)   
Use the `ClientTlsCertificate` property to represent the client's certificate\.  
Use the `SubjectAlternativeNames` property to represent the subject alternative names secured by the certificate\.  
Use the `TlsValidationContextSdsTrust` property to represent a Transport Layer Security \(TLS\) Secret Discovery Service validation context trust\.  
Use the `ListenerTlsValidationContextTrust` property to represent a listener's Transport Layer Security \(TLS\) validation context trust\.  
Use the `SubjectAlternativeNameMatchers` property to represent the methods by which a subject alternative name on a peer Transport Layer Security \(TLS\) certificate can be matched\.  
Use the `ListenerTlsSdsCertificate` property to represent the listener's Secret Discovery Service certificate\.  
Use the `ListenerTlsValidationContext` property to represent a listener's Transport Layer Security \(TLS\) validation context\. 

 [AWS::AppMesh::VirtualGateway](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-appmesh-virtualgateway.html)   
Use the `VirtualGatewayListenerTlsValidationContextTrust` property to specify validation context trust\.  
Use the `VirtualGatewayTlsValidationContextSdsTrust ` property to represent a virtual gateway's listener's Transport Layer Security \(TLS\) Secret Discovery Service validation context trust\.  
Use the `SubjectAlternativeNames` property represents the subject alternative names secured by the certificate\.  
Use the `VirtualGatewayListenerTlsSdsCertificate` property to represent the virtual gateway's listener's Secret Discovery Service certificate\.  
Use the `VirtualGatewayClientTlsCertificate` property to represent the virtual gateway's client's Transport Layer Security \(TLS\) certificate\.  
Use the `VirtualGatewayListenerTlsValidationContext` property to represent a virtual gateway's listener's Transport Layer Security \(TLS\) validation context\.  
Use the `SubjectAlternativeNameMatchers` property to represent the methods by which a subject alternative name on a peer Transport Layer Security \(TLS\) certificate can be matched\.  | February 18, 2021 | 
| [Updated resources](AWS_IoTWireless.md) | The following resource was updated: AWS::IoTWireless::ServiceProfile 

 [AWS::IoTWireless::ServiceProfile](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-iotwireless-serviceprofile.html)   
 Use the attributes of `LoRaWANGetServiceProfileInfo` with `LoRaWANServiceProfile` instead as `ReadOnly` properties that you can return using `Fn::GetAtt`\.   | February 18, 2021 | 
| [Updated resources](AWS_Kendra.md) | The following resources were updated: AWS::Kendra::DataSource, AWS::Kendra::Index\. 

[AWS::Kendra::DataSource](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-kendra-datasource.html)  
Use the `ConfluenceConfiguration` property of the resource to specify configuration information for indexing a Confluence data source\. 

[AWS::Kendra::DataSource](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-kendra-datasource.html)  
Use the `GoogleDriveConfiguration` property of the resource to specify configuration information for indexing a Google Drive data source\. 

[AWS::Kendra::Index](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-kendra-index.html)  
Use the `UserContextPolicy` and `UserTokenConfiguration` properties of the resource to specify how Amazon Kendra uses user tokens for access to the index\.  | February 18, 2021 | 
| [Updated resource](AWS_DataBrew.md) | The following resource was updated: AWS::DataBrew::Job JobSample\. 

 [AWS::DataBrew::Job JobSample](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-databrew-job.html#cfn-databrew-job-jobsample)   
Use the `JobSample` property to define the sample configuration for profile jobs\.  | February 18, 2021 | 
| [Updated resource](AWS_FSx.md) | The following resource was updated: AWS::FSx::FileSystem 

[AWS::FSx::FileSystem](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-fsx-filesystem.html)  
In the [WindowsConfiguration](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-fsx-filesystem-windowsconfiguration.html) property type, use `Aliases` to specify one or more DNS alias names that you want to associate with the Amazon FSx file system\.  | February 18, 2021 | 
| [Updated resource](AWS_IoTAnalytics.md) | The following resource was updated: AWS::IoTAnalytics::Dataset\. 

 [ AWS::IoTAnalytics::Dataset](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-iotanalytics-dataset.html)   
Added the following properties: `LateDataRule` and `LateDataRuleConfiguration`\.  
You can use these properties to specify a late data rule for your dataset\. The late data rule enables AWS IoT Analytics to send notifications through Amazon CloudWatch when late data arrives\.  
For more information, see [Getting late data notifications](https://docs.aws.amazon.com/iotanalytics/latest/userguide/late-data-notification.html) in the *AWS IoT Analytics User Guide*\.  | February 18, 2021 | 
| [AWS CloudFormation StackSets now supports delegated administrator with AWS Organizations](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/stacksets-orgs-delegated-admin.html) | In addition to the organization's management account, delegated administrator accounts can create and manage stack sets with service\-managed permissions for their organization\.For more information, see [Register a delegated administrator](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/stacksets-orgs-delegated-admin) and [Create a stack set with service\-managed permissions](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/stacksets-getting-started-create.html#stacksets-orgs-associate-stackset-with-org)\. | February 18, 2021 | 
| [New resources](AWS_EC2.md) | The following resources were added: AWS::EC2::TransitGatewayMulticastDomain, AWS::EC2::TransitGatewayMulticastDomainAssociation, AWS::EC2::TransitGatewayMulticastGroupMembers and AWS::EC2::TransitGatewayMulticastGroupSource\. 

 [AWS::EC2::TransitGatewayMulticastDomain](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-transitgatewaymulticastdomain.html)   
Use the `TransitGatewayMulticastDomain` resource to create a transit gateway multicast domain\. 

 [AWS::EC2::TransitGatewayMulticastDomainAssociation](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-transitgatewaymulticastdomainassociation.html)   
Use the `TransitGatewayMulticastDomainAssociation` resource to associate the specified subnets and transit gateway attachments with the specified transit gateway multicast domain\. 

 [AWS::EC2::TransitGatewayMulticastGroupMember](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-transitgatewaymulticastgroupmember.html)   
Use the `TransitGatewayMulticastGroupMembers` resource to register members \(network interfaces\) with the transit gateway multicast group\. 

 [AWS::EC2::TransitGatewayMulticastGroupSource](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-transitgatewaymulticastgroupsource.html)   
Use the `TransitGatewayMulticastGroupSource` resource to register sources \(network interfaces\) with the specified transit gateway multicast group\.  | February 12, 2021 | 
| [Updated resources](AWS_IoTWireless.md) | The following resources were updated: AWS::IoTWireless::Destination, AWS::IoTWireless::DeviceProfile, AWS::IoTWireless::ServiceProfile, AWS::IoTWireless::WirelessDevice, and AWS::IoTWireless::WirelessGateway\. 

 [AWS::IoTWireless::Destination](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-iotwireless-destination.html)   
 Use the `ExpressionType` property of the resource to specify whether to use a new value `MqttTopic` or to use `RuleName`\. In addition, the property descriptions now list any maximum values, minimum values, and patterns\.  

 [AWS::IoTWireless::DeviceProfile](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-iotwireless-deviceprofile.html)   
 Use the new `LoRaWAN` property which is a renaming of the `LoRaWANDeviceProfile` property\. The property type has not changed from `LoRaWANDeviceProfile`\. In addition, the property descriptions now list any maximum values, minimum values, and patterns\.  

 [AWS::IoTWireless::ServiceProfile](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-iotwireless-serviceprofile.html)   
 Use the new `LoRaWAN` property which is a renaming of the `LoRaWANServiceProfile` property\. The property type has not changed from `LoRaWANServiceProfile`\. In addition, the property descriptions now list any maximum values, minimum values, and patterns\.  

 [AWS::IoTWireless::WirelessDevice](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-iotwireless-wirelessdevice.html)   
 Use the new `LoRaWAN` property which is a renaming of the `LoRaWANDevice` property\. The property type has not changed from `LoRaWANDevice`\. In addition, the property descriptions now list any maximum values, minimum values, and patterns\.  

 [AWS::IoTWireless::WirelessGateway](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-iotwireless-wirelessgateway.html)   
 Use the new `LoRaWAN` property which is a renaming of the `LoRaWANGateway` property\. The property type has not changed from `LoRaWANGateway`\. In addition, the property descriptions now list any maximum values, minimum values, and patterns\.   | February 11, 2021 | 
| [Updated resource](AWS_DMS.md) | The following resource was updated: `AWS::DMS::Endpoint`\. 

 [AWS::DMS::Endpoint\.MongoDbSettings](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-dms-endpoint-mongodbsettings.html)   
Added `SecretsManager` attributes to `MongoDbSettings`\. 

 [AWS::DMS::Endpoint\.MySqlSettings](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-dms-endpoint-mysqlsettings.html)   
Added `SecretsManager` attributes to `MySqlSettings`\. 

 [AWS::DMS::Endpoint\.RedshiftSettings](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-dms-endpoint-redshiftsettings.html)   
Added `SecretsManager` attributes to `RedshiftSettings`\. 

 [AWS::DMS::Endpoint\.SybaseSettings](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-dms-endpoint-sybasesettings.html)   
Added `SecretsManager` attributes to `SybaseSettings`\. 

 [AWS::DMS::Endpoint\.PostgreSqlSettings](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-dms-endpoint-postgresqlsettings.html)   
Added `SecretsManager` attributes to `PostgreSqlSettings`\. 

 [AWS::DMS::Endpoint\.MicrosoftSqlServerSettings](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-dms-endpoint-microsoftsqlserversettings.html)   
Added `SecretsManager` attributes to `MicorsoftSqlServerSettings`\. 

 [AWS::DMS::Endpoint\.IbmDb2Settings](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-dms-endpoint-ibmdb2settings.html)   
Added `SecretsManager` attributes to `IbmDb2Settings`\. 

 [AWS::DMS::Endpoint\.DocDbSettings](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-dms-endpoint-docdbsettings.html)   
Added `SecretsManager` attributes to `DocDbSettings`\. 

 [AWS::DMS::Endpoint\.OracleSettings](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-dms-endpoint-oraclesettings.html)   
Added `SecretsManager` attributes to `OracleSettings`\.  | February 11, 2021 | 
| [Updated resource](AWS_GroundStation.md) | The following resource was updated: AWS::GroundStation::Config\. 

 [AWS::GroundStation::Config S3RecordingConfig CloudFormation property](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-groundstation-config-s3recordingconfig.html)   
The `S3RecordingConfig` property sets the information for a S3 recording config object\.  | February 11, 2021 | 
| [New resources](AWS_CloudFormation.md) | The following resources were added: AWS::CloudFormation::ResourceDefaultVersion and AWS::CloudFormation::ResourceVersion\. 

 [AWS::CloudFormation::ResourceDefaultVersion](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-cloudformation-resourcedefaultversion.html)  
Use the `AWS::CloudFormation::ResourceDefaultVersion` resource to specify the default resource version to be used in CloudFormation operations\. 

 [AWS::CloudFormation::ResourceVersion](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-cloudformation-resourceversion.html)   
Use the `AWS::CloudFormation::ResourceVersion` resource to specify a resource version with the CloudFormation service, making it available for use in CloudFormation operations\.  | February 11, 2021 | 
| [New resources](AWS_SageMaker.md) | The following resources were added: AWS::SageMaker::App, AWS::SageMaker::AppImageConfig, AWS::SageMaker::Domain, AWS::SageMaker::UserProfile\. 

 [AWS::SageMaker::App](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-sagemaker-app.html)   
Use the `AWS::SageMaker::App` resource to create a running app for a user profile in SageMaker Studio\. 

 [AWS::SageMaker::AppImageConfig](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-sagemaker-appimageconfig.html)   
Use the `AWS::SageMaker::AppImageConfig` resource to create a configuration for running a SageMaker image as a KernelGateway app in SageMaker Studio\. 

 [AWS::SageMaker::Domain](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-sagemaker-domain.html)   
Use the `AWS::SageMaker::Domain` resource to create a Domain used by SageMaker Studio\. 

 [AWS::SageMaker::UserProfile](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-sagemaker-userprofile.html)   
Use the `AWS::SageMaker::UserProfile` resource to create a user profile used by SageMaker Studio\.  | February 11, 2021 | 
| [New resources](AWS_ServiceCatalog.md) | The following resources were added: AWS::ServiceCatalog::ServiceAction and AWS::ServiceCatalog::ServiceActionAssociation\. 

 [ AWS::ServiceCatalog::ServiceAction](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-servicecatalog-serviceaction.html)   
Use this self\-service action feature to create CloudFormation templates that create Service Actions\.  

 [ AWS::ServiceCatalog::ServiceActionAssociation](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-servicecatalog-serviceactionassociation.html)   
Use this self\-service action association feature to create AWS CloudFormation templates that create Service Actions\.  | February 11, 2021 | 
| [AWS CloudFormation StackSets Region availability](#ReleaseHistory) | AWS CloudFormation StackSets is now available in the Asia Pacific \(Osaka\) Region\.For more information, see [Working with AWS CloudFormation StackSets](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/what-is-cfnstacksets.html)\. | February 10, 2021 | 
| [Updated resource](AWS_IoTAnalytics.md) | The following resource was updated: AWS::IoTAnalytics::Datastore\. 

 [ AWS::IoTAnalytics::Datastore](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-iotanalytics-datastore.html)   
Added the following properties: `Column`, `FileFormatConfiguration`, `JsonConfiguration`, `ParquetConfiguration`, and `SchemaDefinition`\.  
You can use these properties to specify JSON or Parquet file format for your data store\.  
For more information, see [File formats](https://docs.aws.amazon.com/iotanalytics/latest/userguide/iotanalytics-schema.html) in the *AWS IoT Analytics User Guide*\.  | February 5, 2021 | 
| [Updated resources](AWS_ECR.md) | The following resources were updated: AWS::ECR::ReplicationConfiguration 

 [AWS::ECR::ReplicationConfiguration](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ecr-replicationconfiguration.html)   
Use the `ReplicationConfiguration` property to create or update the replication configuration for a private repository\.  | February 4, 2021 | 
| [Updated resources](AWS_IoTWireless.md) | The following resources were updated: AWS::IoTWireless::DeviceProfile, AWS::IoTWireless::ServiceProfile, AWS::IoTWireless::WirelessDevice, and AWS::IoTWireless::WirelessGateway\. 

 [AWS::IoTWireless::DeviceProfile](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-iotwireless-deviceprofile.html)   
 Use the `DeviceProfile` resource to specify a device profile for a wireless device to use\.  

 [AWS::IoTWireless::ServiceProfile](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-iotwireless-serviceprofile.html)   
 Use the `ServiceProfile` resource to specify a service profile for a wireless device to use\.  

 [AWS::IoTWireless::WirelessDevice](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-iotwireless-wirelessdevice.html)   
 Use the `WirelessDevice` resource to specify a wireless device in an AWS IoT Core for LoRaWAN solution\.  

 [AWS::IoTWireless::WirelessGateway](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-iotwireless-wirelessgateway.html)   
 Use the `WirelessGateway` resource to specify a wireless gateway in an AWS IoT Core for LoRaWAN solution\.   | February 4, 2021 | 
| [Updated resources](AWS_Cassandra.md) | The following resources were updated: `AWS::Cassandra::Keyspace` and `AWS::Cassandra::Table`\. 

 [AWS::Cassandra::Keyspace\.Tags](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-cassandra-keyspace.html)   
Use the `AWS::Cassandra::Keyspace.Tags` property to add tags to new or existing keyspaces in Amazon Keyspaces \(for Apache Cassandra\)\. 

 [AWS::Cassandra::Table\.Tags](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-cassandra-table.html)   
Use the `AWS::Cassandra::Table.Tags` property to create and add tags to new or existing tables in Amazon Keyspaces \(for Apache Cassandra\)\. 

 [AWS::Cassandra::Table\.PointInTimeRecoveryEnabled](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-cassandra-table.html)   
Use the `AWS::Cassandra::Table.PointInTimeRecoveryEnabled` property to enable point\-in\-time recovery in Amazon Keyspaces \(for Apache Cassandra\)\.  | February 4, 2021 | 
| [Updated resource](AWS_DataBrew.md) | The following resource was updated: AWS::DataBrew::Job\. 

 [AWS::DataBrew::Job](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-databrew-job.html)   
Use the `CsvOutputOptions` property to define how DataBrew will write a CSV file\.  
Use the `OutputFormatOptions` property to define the structure of CSV job output\.  | February 4, 2021 | 
| [Updated resource](AWS_ElastiCache.md) | The following resource was updated: AWS::ElastiCache::GlobalReplicationGroup\. 

 [AWS::ElastiCache::GlobalReplicationGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-elasticache-globalreplicationgroup.html)   
Consists of a primary cluster that accepts writes and an associated secondary cluster that resides in a different Region\. The secondary cluster accepts only reads\. The primary cluster automatically replicates updates to the secondary cluster\.   | February 4, 2021 | 
| [New resource](AWS_ImageBuilder.md) | Added the following resource: AWS::ImageBuilder::ContainerRecipe\. 

 [AWS::ImageBuilder::ContainerRecipe](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-imagebuilder-containerrecipe.html)   
Use the `AWS::ImageBuilder::ContainerRecipe` resource to create a container recipe in the Image Builder service\.  | February 4, 2021 | 
| [Updated resource](AWS_ApiGatewayV2.md) | The following resource was updated: `AWS::ApiGatewayV2::Stage`\. 

 [AWS::ApiGatewayV2::Stage](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-apigatewayv2-stage.html)   
Added the attribute `AccessPolicyId` for internal use only\.  | January 28, 2021 | 
| [New resource](AWS_LookoutVision.md) | The following resource was added: AWS::LookoutVision:Project\. 

 [AWS::LookoutVision:Project](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/AWS_LookoutVision.html)   
Use the `Project` resource to create an Amazon Lookout for Vision project\.  | January 28, 2021 | 
| [Updated resource](AWS_ACMPCA.md) | The following resource was updated: AWS::ACMPCA::Certificate\. 

 [AWS::ACMPCA::Certificate](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-acmpca-certificate.html)   
Use the `ApiPassthrough` property to include parameters in certificates during issuance\.  
Use the `ValidityNotBefore` property to customize the start of certificate validity\.  | January 21, 2021 | 
| [Updated resource](AWS_MediaConnect.md) | The following resource was updated: `AWS::MediaConnect::FlowVpcInterface`\. 

 [AWS::MediaConnect::FlowVpcInterface](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-mediaconnect-flowvpcinterface.html)   
Use the `FlowArn` property to specify the ARN of the flow\.  
Use the `Name` property to specify the name of the VPC Interface\.  | January 21, 2021 | 
| [Updated resource](AWS_SageMaker.md) | The following resources were updated: AWS::SageMaker::Device, AWS::SageMaker::DeviceFleet, and AWS::SageMaker::Model\. 

 [AWS::SageMaker::Device](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-sagemaker-device.html)   
Use the `DeviceFleetName` property to get the name of the fleet the device belongs to\.  
Use the `Device` property to make the edge device you want to create\.  
Use the `Tags` property to get the tags registered to a specific device\.  
Use the `Device.Device` property/resource to get information about a particular device\.  
Use the `Device.Device.Description` property/resource to get a description of the device\.  
Use the `Device.Device.DeviceName` property/resource to get the device name\.  
Use the `Device.Device.IotThingName` property/resource to get the IoT object name\. 

 [AWS::SageMaker::DeviceFleet](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-sagemaker-devicefleet.html)   
Use the `DeviceFleet.Description` property to get information about a fleet\.  
Use the `OutputConfig` property to get the output configuration for the fleet\.  
Use the `RoleArn` property to get the ARN of the IoT thing\.  
Use the `Tags` property to get the tags registered to a specific fleet\.  
Use the `EdgeOutputConfig.KmsKeyId` property/resource to set the KMS key ID\.  
Use the `EdgeOutputConfig.S3OutputLocation` property/resource to set the S3 bucket URI\. 

 [AWS::SageMaker::Model](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-sagemaker-model.html)   
Use the `MultiModelConfiguration` property to specify configuration details for a multi\-model endpoint\.  | January 21, 2021 | 
| [New resources](AWS_SageMaker.md) | The following resource was added: AWS::SageMaker::Project\. 

 [AWS::SageMaker::Project](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-sagemaker-project.html)   
Use the `AWS::SageMaker::Project` resource to create a new project in Amazon SageMaker\.  | January 21, 2021 | 
| [Updated resource](AWS_S3.md) | The following resource was updated with examples: AWS::S3::AccessPoint 

 [Access Points](https://docs.aws.amazon.com/AmazonS3/latest/userguide/access-points.html)   
Use the `AWS::S3::AccessPoint` resource to specify an S3 access point\.  | January 20, 2021 | 
| [Updated resource](AWS_MSK.md) | The following resource was updated: AWS::MSK::Cluster 

 [AWS::MSK::Cluster](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-msk-cluster.html)   
You can now change the broker type for an existing cluster\.  | January 15, 2021 | 
| [New resource](AWS_EMRContainers.md) | The AWS::EMRContainers::VirtualCluster resource was added\. 

 [AWS::EMRContainers::VirtualCluster](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-emrcontainers-virtualcluster.html)   
The `AWS::EMRContainers::VirtualCluster` resource specifies a virtual cluster\.  | January 14, 2021 | 
| [New resource](AWS_QuickSight.md) | The following resource was added: AWS::QuickSight::DataSet and AWS::QuickSight::DataSource\. 

 [ AWS::QuickSight::DataSet](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-quicksight-dataset.html)   
Use the `AWS::QuickSight::DataSet` resource to create a dataset in Amazon QuickSight\. 

 [ AWS::QuickSight::DataSource](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-quicksight-datasource.html)   
Use the `AWS::QuickSight::DataSource` resource to create a data source in Amazon QuickSight\.  | January 14, 2021 | 
| [New resource](AWS_QuickSight.md) | The following resource was added: AWS::QuickSight::Analysis, AWS::QuickSight::Dashboard, AWS::QuickSight::Template, and AWS::QuickSight::Theme\. 

 [ AWS::QuickSight::Analysis](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-quicksight-analysis.html)   
Use the `AWS::QuickSight::Analysis` resource to create an analysis in Amazon QuickSight\. 

 [ AWS::QuickSight::Dashboard](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-quicksight-dashboard.html)   
Use the `AWS::QuickSight::Dashboard` resource to create a dashboard from a template in Amazon QuickSight\. 

 [ AWS::QuickSight::Template](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-quicksight-template.html)   
Use the `AWS::QuickSight::Template` resource to create a template from an existing Amazon QuickSight analysis or template\. 

 [ AWS::QuickSight::Theme](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-quicksight-theme.html)   
Use the `AWS::QuickSight::Theme` resource to create a theme in Amazon QuickSight\.  | January 14, 2021 | 
| [New resource](AWS_ServiceCatalogAppRegistry.md) | The following new resources were added: AWS::ServiceCatalogAppRegistry::Application, AWS::ServiceCatalogAppRegistry::AttributeGroup, AWS::ServiceCatalogAppRegistry::AttributeGroupAssociation, AWS::ServiceCatalogAppRegistry::ResourceAssociation 

 [AWS::ServiceCatalogAppRegistry::Application](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-servicecatalogappregistry-application.html)   
Use the `AWS::ServiceCatalogAppRegistry::Application` resource to represent a Service Catalog AppRegistry application at the top\-level node in a hierarchy of related cloud resource abstractions\. 

 [AWS::ServiceCatalogAppRegistry::AttributeGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-servicecatalogappregistry-attributegroup.html)   
Use the `AWS::ServiceCatalogAppRegistry::AttributeGroup` resource to create a new attribute group as a container for user\-defined attributes\. 

 [AWS::ServiceCatalogAppRegistry::AttributeGroupAssociation](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-servicecatalogappregistry-attributegroupassociation.html)   
Use the `AWS::ServiceCatalogAppRegistry::AttributeGroupAssociation` as the attribute group to associate ServiceCatalogAppRegistry\. 

 [AWS::ServiceCatalogAppRegistry::ResourceAssociation](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-servicecatalogappregistry-resourceassociation.html)   
Use the `AWS::ServiceCatalogAppRegistry::ResourceAssociation` as the resource association for ServiceCatalogAppRegistry\.  | January 14, 2021 | 
| [Updates to resource](AWS_SSO.md) | The following resource was updated: `AWS::SSO::InstanceAccessControlAttributeConfiguration`\.  

 [https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-sso-instanceaccesscontrolattributeconfiguration.html](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-sso-instanceaccesscontrolattributeconfiguration.html)   
Use the `AWS::SSO::InstanceAccessControlAttributeConfiguration` resource to configure attribute\-based access control \(ABAC\) in IAM Identity Center\.  | January 7, 2021 | 
| [Updated resources](AWS_IoTWireless.md) | The following resources were updated: AWS::IoTWireless::Destination, AWS::IoTWireless::DeviceProfile, AWS::IoTWireless::ServiceProfile, AWS::IoTWireless::WirelessDevice, and AWS::IoTWireless::WirelessGateway\. 

 [AWS::IoTWireless::Destination](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-iotwireless-destination.html)   
 Use the `Destination` resource to specify a destination for a wireless device to use\.  

 [AWS::IoTWireless::DeviceProfile](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-iotwireless-deviceprofile.html)   
 Use the `DeviceProfile` resource to specify a device profile for a wireless device to use\.  

 [AWS::IoTWireless::ServiceProfile](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-iotwireless-serviceprofile.html)   
 Use the `ServiceProfile` resource to specify a service profile for a wireless device to use\.  

 [AWS::IoTWireless::WirelessDevice](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-iotwireless-wirelessdevice.html)   
 Use the `WirelessDevice` resource to specify a wireless device in an AWS IoT Core for LoRaWAN solution\.  

 [AWS::IoTWireless::WirelessGateway](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-iotwireless-wirelessgateway.html)   
 Use the `WirelessGateway` resource to specify a wireless gateway in an AWS IoT Core for LoRaWAN solution\.   | January 7, 2021 | 
| [Updated resource](AWS_ApiGatewayV2.md) | The following resource was updated: `AWS::ApiGatewayV2::Integration`\. 

 [AWS::ApiGatewayV2::Integration](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-apigatewayv2-integration.html)   
Use the `AWS::ApiGatewayV2::Integration` resource to configure request and response parameter mapping for an HTTP API\.  | January 7, 2021 | 
| [Updated resource](AWS_EC2.md) | The following resource was updated: AWS::EC2::LaunchTemplate 

 [AWS::EC2::LaunchTemplate](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-launchtemplate.html)   
Use the `Throughput` property to specify the throughput to provision for gp3 volumes\.  | January 7, 2021 | 
| [Updated resource](AWS_FMS.md) | The following resources were updated: AWS::FMS::Policy\. 

 [AWS::FMS::Policy](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-fms-policy.html)   
The `AWS::FMS::Policy` resource now allows you to manage AWS Network Firewall policies\.   | January 7, 2021 | 
| [New resources](AWS_MediaConnect.md) | The following resources were added: `AWS::MediaConnect::Flow`, `AWS::MediaConnect::FlowEntitlement`, `AWS::MediaConnect::FlowOutput`, `AWS::MediaConnect::FlowSource`, and `AWS::MediaConnect::FlowVpcInterface`\. 

 [AWS::MediaConnect::Flow](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-mediaconnect-flow.html)   
Use the `AWS::MediaConnect::Flow` resource to create a connection between one or more video sources and one or more outputs\. 

 [AWS::MediaConnect::FlowEntitlement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-mediaconnect-flowentitlement.html)   
Use the `AWS::MediaConnect::FlowEntitlement` resource to grant permission to another AWS account to allow access to the content in a specific AWS Elemental MediaConnect flow\. 

 [AWS::MediaConnect::FlowOutput](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-mediaconnect-flowoutput.html)   
Use the `AWS::MediaConnect::FlowOutput` resource to define the destination address, protocol, and port that you want MediaConnect to send the ingested video to\. 

 [AWS::MediaConnect::FlowSource](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-mediaconnect-flowsource.html)   
Use the `AWS::MediaConnect::FlowSource` resource to define where the external video content comes from\. 

 [AWS::MediaConnect::FlowVpcInterface](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-mediaconnect-flowvpcinterface.html)   
Use the `AWS::MediaConnect::FlowVpcInterface` resource to create a connection between your MediaConnect flow and a virtual private cloud \(VPC\) that you created using the Amazon Virtual Private Cloud service\.  | January 7, 2021 | 
| [New resources](AWS_Route53.md) | The following resources were added: AWS::Route53::DNSSEC and AWS::Route53::KeySigningKey\. 

 [AWS::Route53::DNSSEC](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-route53-dnssec.html)   
Use the `AWS::Route53::DNSSEC` resource to enable DNSSEC signing for a hosted zone\.  

 [AWS::Route53::KeySigningKey](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-route53-keysigningkey.html)   
Use the `AWS::Route53::KeySigningKey` resource to specify configuration settings for a key\-signing key \(KSK\) that's associated with a hosted zone\.  | January 7, 2021 | 
| [New resource](AWS_Route53Resolver.md) | The following resource was added: `AWS::Route53Resolver::ResolverDNSSECConfig`\. 

 [AWS::Route53Resolver::ResolverDNSSECConfig](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-route53resolver-resolverdnssecconfig.html)   
Use the `AWS::Route53Resolver::ResolverDNSSECConfig` resource to specify configuration for DNSSEC validation\.  | January 7, 2021 | 
| [New Resources](AWS_DataSync.md) | The following resources were added: AWS::DataSync::Agent, AWS::DataSync::LocationEFS, AWS::DataSync::LocationFSxWindows, AWS::DataSync::LocationNFS, AWS::DataSync::LocationObjectStorage, AWS::DataSync::LocationS3, AWS::DataSync::LocationSMB, and AWS::DataSync::Task\.  

 [AWS::DataSync::Agent](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-datasync-agent.html)   
Use the `AWS::DataSync::Agent` resource to specify an AWS DataSync agent\. 

 [AWS::DataSync::LocationEFS](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-datasync-locationefs.html)   
Use the `AWS::DataSync::LocationEFS` resource to specify a location for an Amazon EFS location\. 

 [AWS::DataSync::LocationFSxWindows](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-datasync-locationfsxwindows.html)   
Use the `AWS::DataSync::LocationFSxWindows` resource to specify an Amazon FSx for Windows Server file system\. 

 [AWS::DataSync::LocationNFS](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-datasync-locationnfs.html)   
Use the `AWS::DataSync::LocationNFS` resource to specify a file system on a Network File System \(NFS\) server\. 

 [AWS::DataSync::LocationObjectStorage](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-datasync-locationobjectstorage.html)   
Use the `AWS::DataSync::LocationObjectStorage` resource to specify an endpoint for a self\-managed object storage bucket\. 

 [AWS::DataSync::LocationS3](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-datasync-locations3.html)   
Use the `AWS::DataSync::LocationS3` resource to specify an endpoint for an Amazon S3 bucket\. 

 [AWS::DataSync::LocationSMB](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-datasync-locationsmb.html)   
Use the `AWS::DataSync::LocationSMB` resource to specify a Server Message Block \(SMB\) location\. 

 [AWS::DataSync::Task](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-datasync-task.html)   
Use the `AWS::DataSync::Task` resource to specify a task\.  | January 7, 2021 | 
| [Updated resource](AWS_Glue.md) | The following resource was updated: AWS::Glue::Table 

 [AWS::Glue::Table](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-glue-table.html)   
Use the `SchemaReference` property to specify an object that references a schema stored in the AWS Glue Schema Registry\.  
Use the `TableInput.TargetTable` property to specify a `TableIdentifier` structure that describes a target table for resource linking\.  
Use the `Table.TableIdentifier` property to specify a target table for resource linking\.  | December 22, 2020 | 
| [Updated resource](AWS_Glue.md) | The following resource was updated: AWS::Glue::Partition 

 [AWS::Glue::Partition](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-glue-partition.html)   
Use the `SchemaReference` property to specify an object that references a schema stored in the AWS Glue Schema Registry\.  | December 22, 2020 | 
| [Updated resource](AWS_Glue.md) | The following resource was updated: AWS::Glue::Database 

 [AWS::Glue::Database](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-glue-database.html)   
Use the `DatabaseInput.TargetDatabase` property to specify a `TableIdentifier` structure that describes a target table for resource linking\.  
Use the `Database.DatabaseIdentifier` property to specify a target database for resource linking\.  | December 22, 2020 | 
| [Updated resource](AWS_Glue.md) | The following resource was updated: AWS::Glue::MLTransform 

 [AWS::Glue::MLTransform](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-glue-mltransform.html)   
Use the `TransformEncryption` property to specify the encryption\-at\-rest settings of the transform that apply to accessing user data\.  
Use the `MLUserDataEncryption` property to specify the encryption mode and customer\-provided KMS key ID\.  | December 22, 2020 | 
| [Updated resource](AWS_NimbleStudio.md) | The following resource was updated: AWS::NimbleStudio::LaunchProfile\. 

 [AWS::NimbleStudio::LaunchProfile](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-nimblestudio-launchprofile.html)   
In the [StreamConfiguration](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-nimblestudio-launchprofile-streamconfiguration.html) property type, use the `MaxStoppedSessionLengthInMinutes` property to specify if you can stop your sessions, and use the `SessionStorage` property to specify the upload storage for a streaming session\.  
Use the `StreamConfigurationSessionStorage` property to specify a configuration for a streaming session’s upload storage\.  
Use the `StreamingSessionStorageRoot` property to specify the upload storage root location that is a folder on streaming workstations where files are uploaded\.  | December 22, 2020 | 
| [New resource](AWS_MWAA.md) | The following resource was added: AWS::MWAA::Environment 

 [AWS::MWAA::Environment](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-mwaa-environment.html)   
Use the `AWS::MWAA::Environment` resource to create an Amazon Managed Workflows for Apache Airflow \(MWAA\) environment\.  | December 21, 2020 | 
| [Updated resources](AWS_EC2.md) | The following resources were updated: AWS::EC2::Instance, AWS::EC2::SpotFleet, AWS::EC2::Volume\. 

 [AWS::EC2::Instance](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ec2-instance.html)   
Use the `EnclaveOptions` property to indicate whether the instance is enabled for AWS Nitro Enclaves\. 

 [AWS::EC2::SpotFleet SpotCapacityRebalance](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ec2-spotfleet-spotcapacityrebalance.html)   
Use the `SpotCapacityRebalance` property when Amazon EC2 emits a signal that your Spot Instance is at an elevated risk of being interrupted\. 

 [AWS::EC2::SpotFleet SpotMaintenanceStrategies](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ec2-spotfleet-spotmaintenancestrategies.html)   
Use the `SpotMaintenanceStrategies` property to manage your Spot Instances that are at an elevated risk of being interrupted\. \. 

 [AWS::EC2::Volume](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ec2-ebs-volume.html)   
Use the `Throughput` property to specify the throughput that the volume supports, in MiB/s\.  | December 18, 2020 | 
| [Updated resources](AWS_ECS.md) | The following resources were updated: AWS::ECS::Service\. 

 [AWS::ECS::Service](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ecs-service.html)   
Use the `DeploymentCircuitBreaker` property to turn on the deployment circuit breaker for a service\.  | December 18, 2020 | 
| [Updated resources](AWS_ElastiCache.md) | The following resources were updated: AWS::ElastiCache::User AWS::ElastiCache::UserGroup and AWS::ElastiCache::ReplicationGroup\. 

 [AWS::ElastiCache::User](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-elasticache-user.html)   
For Redis engine version 6\.0 onwards: Creates a Redis user\. For more information, see [Using Role Based Access Control \(RBAC\)](AmazonElastiCache/latest/red-ug/Clusters.RBAC.html)  

 [AWS::ElastiCache::UserGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-elasticache-usergroup.html)   
For Redis engine version 6\.0 onwards: Creates a Redis user group\. For more information, see [Using Role Based Access Control \(RBAC\)](AmazonElastiCache/latest/red-ug/Clusters.RBAC.html) 

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
| [New resources](AWS_CloudFormation.md) | The following resources were added: AWS::CloudFormation::ModuleDefaultVersion and AWS::CloudFormation::ModuleVersion\. 

 [AWS::CloudFormation::ModuleDefaultVersion](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-cloudformation-moduledefaultversion.html)   
Use the `AWS::CloudFormation::ModuleDefaultVersion` resource to specify the default version of a module, which will be used in CloudFormation operations for this account and Region\. 

 [AWS::CloudFormation::ModuleVersion](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-cloudformation-moduleversion.html)   
Use the `AWS::CloudFormation::ModuleVersion` resource to register the specified version of the module with the CloudFormation service, making it available for use in CloudFormation templates in this account and Region\.  | December 18, 2020 | 
| [New resources](AWS_DevOpsGuru.md) | The following resources were added: `AWS::DevOpsGuru::NotificationChannel`, `AWS::DevOpsGuru::ResourceCollection` 

 [AWS::DevOpsGuru::NotificationChannel](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-devopsguru-notificationchannel.html)   
Use the `AWS::DevOpsGuru::NotificationChannel` resource to add a notification channel to Amazon DevOps Guru\. The notification channel is used to notify you about important events\. For example, the creation of an insight or a change in an insight's severity\. 

 [AWS::DevOpsGuru::ResourceCollection](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-devopsguru-resourcecollection.html)   
Use the `AWS::DevOpsGuru::ResourceCollection` resource to specify a collection of resources in your account that you want Amazon DevOps Guru to analyze\. The specified resources are analyzed to generate insights that contain recommendations, related metrics, and operational data to help you improve the performance of your operational solutions\.  | December 18, 2020 | 
| [New resources](AWS_EC2.md) | The following resources were added: AWS::EC2::NetworkInsightsPath and AWS::EC2::NetworkInsightsAnalysis\. 

 [AWS::EC2::NetworkInsightsPath](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-networkinsightspath.html)   
Use the `NetworkInsightsPath` property to specify a path to analyze for reachability\. 

 [AWS::EC2::NetworkInsightsAnalysis](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-networkinsightsanalysis.html)   
Use the `NetworkInsightsAnalysis` property to specify a network insights analysis\.  | December 18, 2020 | 
| [New resources](AWS_ECR.md) | The following resources were added: AWS::ECR::PublicRepository 

 [AWS::ECR::PublicRepository](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ecr-publicrepository.html)   
Use the `PublicRepository` property to create or update a public repository\.  | December 18, 2020 | 
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
Use the `AWS::SageMaker::ModelPackageGroup` resource to create a group of related models\. 

 [AWS::SageMaker::Pipeline](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-sagemaker-pipeline.html)   
Use the `AWS::SageMaker::Pipeline` resource to specify shell scripts that run when you create and/or start a SageMaker Pipeline\. For information about SageMaker Pipelines, see [SageMaker Pipelines](https://docs.aws.amazon.com/sagemaker/latest/dg/pipelines.html) in the *Amazon SageMaker Developer Guide*\.  | December 18, 2020 | 
| [New resource](AWS_AuditManager.md) | The following resource was added: AWS::AuditManager::Assessment 

 [AWS::AuditManager::Assessment](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-auditmanager-assessment.html)   
Use the `AWS::AuditManager::Assessment` resource to specify a new assessment in AWS Audit Manager\.  | December 18, 2020 | 
| [New resource](AWS_GreengrassV2.md) | The following resources were added: AWS::GreengrassV2::ComponentVersion\. 

 [AWS::GreengrassV2::ComponentVersion](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-greengrassv2-componentversion.html)   
Use the `AWS::GreengrassV2::ComponentVersion` resource to create a new component version in AWS IoT Greengrass\.  | December 18, 2020 | 
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
| [New resource](AWS_SSO.md) | The following resource was added: `AWS::SSO::InstanceAccessControlAttributeConfiguration`\.  

 [https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-sso-instanceaccesscontrolattributeconfiguration.html](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-sso-instanceaccesscontrolattributeconfiguration.html)   
Use the `AWS::SSO::InstanceAccessControlAttributeConfiguration` resource to configure attribute\-based access control \(ABAC\) in IAM Identity Center\.  | December 18, 2020 | 
| [Updated resource](AWS_EKS.md) | The following resource was updated to support specifying a capacity type for a node group: `AWS::EKS::Nodegroup`\. 

 [https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-eks-nodegroup.html](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-eks-nodegroup.html)   
Use the `CapacityType` property to specify whether you want to use Spot or On\-Demand instance types for your node group\.  | December 17, 2020 | 
| [Updated resource](AWS_GameLift.md) | The following resource was updated: AWS::GameLift::MatchmakingConfiguration\. 

 [AWS::GameLift::MatchmakingConfiguration](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-gamelift-matchmakingconfiguration.html)   
Use the `FlexMatchMode` property to specify that the matchmaker is for a standalone FlexMatch solution or for matchmaking with GameLift managed hosting\.  | November 24, 2020 | 
| [Updated resource](AWS_Lambda.md) | The following resource was updated: AWS::Lambda::CreateEventSourceMapping\. 

 [AWS::Lambda::EventSourceMapping\.BatchSize](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-lambda-eventsourcemapping.html#cfn-lambda-eventsourcemapping-batchsize)   
The `BatchSize` has been increased for standard SQS queues, and allows for the use of a `MaximumBatchingWindowInSeconds`\.  | November 24, 2020 | 
| [Modules](#ReleaseHistory) | Modules are a way for you to package resource configurations for inclusion across stack templates, in a transparent, manageable, and repeatable way\. Modules can encapsulate common service configurations and best practices as modular, customizable building blocks for you to include in your stack templates\.For more information, see [Using modules to encapsulate and reuse resource configurations](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/modules.html)\. | November 24, 2020 | 
| [New resource](AWS_Lambda.md) | The following resource was added: AWS::Lambda::CodeSigningConfig\. 

 [AWS::Lambda::CodeSigningConfig](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-lambda-codesigningconfig.html)   
Use the `CodeSigningConfig` resource to specify code\-signing capability to your Lambda functions\.  | November 23, 2020 | 
| [Updated resource](AWS_CloudFront.md) | The following resource was updated: AWS::CloudFront::Distribution\. 

 [AWS::CloudFront::Distribution](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-cloudfront-distribution.html)   
In the [CacheBehavior](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-cloudfront-distribution-cachebehavior.html) and [DefaultCacheBehavior](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-cloudfront-distribution-defaultcachebehavior.html) property types, use the `TrustedKeyGroups` property to specify a list of the key groups that CloudFront can use to verify signed URLs or signed cookies\.  
For more information, see [Serving private content](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/PrivateContent.html) in the *Amazon CloudFront Developer Guide*\.  | November 19, 2020 | 
| [Updated resource](AWS_EC2.md) | The following resources were updated: AWS::EC2::LaunchTemplate and AWS::EC2::ClientVpnEndpoint\. 

 [AWS::EC2::ClientVpnEndpoint](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-clientvpnendpoint.html)   
Use the `ClientConnectOptions` property to indicate whether client connect options are used for Client VPN\. 

 [AWS::EC2::LaunchTemplate](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-launchtemplate.html)   
Use the `AssociateCarrierIpAddress` property to indicates whether to associate a Carrier IP address with eth0 for a new network interface\. 

 [AWS::EC2::LaunchTemplate](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-launchtemplate.html)   
Use the `EnclaveOptions` property to indicate whether the instance is enabled for AWS Nitro Enclaves\. 

 [AWS::EC2::LaunchTemplate](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-launchtemplate.html)   
Use the `NetworkCardIndex` property to specify the network card index\.  | November 19, 2020 | 
| [Updated resource](AWS_Events.md) | The following resource was updated: AWS::Events::EventBusPolicy\. 

 [AWS::Events::EventBusPolicy](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-events-eventbuspolicy.html)   
Added the `Statement` property\. Use the `Statement` property to add a statement to the policy attached to an event bus\.  | November 19, 2020 | 
| [Updated resource](AWS_KMS.md) | The following resource was updated: AWS::KMS::Key\. 

 [AWS::KMS::Key](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-kms-key.html)   
Added support for asymmetric KMS keys, including the `KeySpec` property and the SIGN\_VERIFY value for the `KeyUsage` property\.  | November 19, 2020 | 
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
| [New resource](AWS_IoT.md) | The following resource is new: AWS::IoT::TopicRuleDestination 

 [AWS::IoT::TopicRuleDestination](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-iot-topicruledestination.html)   
Use the `AWS::IoT::TopicRuleDestination` to specify a topic rule destination\.  | November 19, 2020 | 
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
| [Change sets for nested stacks](#ReleaseHistory) | With change sets for nested stacks you can preview the changes to your application and infrastructure resources across the entire nested stack hierarchy and proceed with updates when you've confirmed that all the changes are as intended\.For more information, see [Change sets for nested stacks](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/change-sets-for-nested-stacks.html)\. | November 18, 2020 | 
| [Updated resources](AWS_AppMesh.md) | The following resources were updated: AWS::AppMesh::VirtualNode and AWS::AppMesh::VirtualGateway 

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
| [Updated resource](AWS_EC2.md) | The following resources were updated: AWS::EC2::Route and AWS::EC2::VPCEndpointService\. 

 [AWS::EC2::Route](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-route.html)   
Use the `VpcEndpointId` property to create a route to a Gateway Load Balancer endpoint\. 

 [AWS::EC2::VPCEndpointService](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-vpcendpointservice.html)   
Use the `GatewayLoadBalancerArns` property to specify a Gateway Load Balancer for your VPC endpoint service\.  | November 12, 2020 | 
| [Updated resource](AWS_Kendra.md) | The following resource was updated: AWS::Kendra::DataSource\. 

 [AWS::Kendra::DataSource](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-kendra-datasource.html)   
Use the new `CUSTOM` value to specify the custom data sources\.  | November 12, 2020 | 
| [New resources:](AWS_DataBrew.md) | This is the first release of [AWS Glue DataBrew](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/AWS_DataBrew.html)\. | November 12, 2020 | 
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
| [Updated resource](AWS_Batch.md) | The following resource was updated: [AWS::Batch::JobDefinition](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-batch-jobdefinition.html) 

[AWS::Batch::JobDefinition](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-batch-jobdefinition.html)  
In the [RetryStrategy](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-batch-jobdefinition-retrystrategy.html) property type, use the [EvaluateOnExit](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-batch-jobdefinition-retrystrategy.html#cfn-batch-jobdefinition-retrystrategy-evaluateonexit) property to specify a set of conditions to be met, and an action to take \(`RETRY` or `EXIT`\) if all conditions are met\.  | November 5, 2020 | 
| [Updated resource](AWS_EC2.md) | The following resource was updated: AWS::EC2::Route\. 

 [AWS::EC2::Route](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-route.html)   
Use the `CarrierGatewayId` property to create a route to a carrier gateway\.  | November 5, 2020 | 
| [Updated resource](AWS_AutoScaling.md) | The following resource was updated: AWS::AutoScaling::AutoScalingGroup\. 

 [CapacityRebalance](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-as-group.html#cfn-as-group-capacityrebalance)   
Use the `CapacityRebalance` property to indicate whether Capacity Rebalancing is enabled\.  | November 5, 2020 | 
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
| [Updated resource](AWS_AmazonMQ.md) | The following resources were updated: AWS::AmazonMQ::Broker, AWS::AmazonMQ::Configuration, AWS::AmazonMQ::ConfigurationAssociation 

 [AWS::AmazonMQ::Broker](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-amazonmq-broker.html)   
Amazon MQ now supports RabbitMQ broker engine\.  | November 4, 2020 | 
| [Updated resource](AWS_GlobalAccelerator.md) | The following resource was updated: AWS::GlobalAccelerator::EndpointGroup\. 

 [ AWS::GlobalAccelerator::EndpointGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-globalaccelerator-endpointgroup.html)   
Use the `PortOverride` property to override the listener port used for routing traffic to endpoints\.  | October 29, 2020 | 
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
| [Updated resources](AWS_Batch.md) | The following resources were updated: [AWS::Batch::ComputeEnvironment](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-batch-computeenvironment.html), [AWS::Batch::JobDefinition](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-batch-jobdefinition.html), and [AWS::Batch::JobQueue](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-batch-jobqueue.html)\. 

[AWS::Batch::ComputeEnvironment](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-batch-computeenvironment.html)  
Use the `Tags` property to specify tags for the compute environment\. 

[AWS::Batch::JobDefinition](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-batch-jobdefinition.html)  
Use the `Tags` property to specify tags for the job definition\. 

[AWS::Batch::JobQueue](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-batch-jobqueue.html)  
Use the `Tags` property to specify tags for the job queue\.  | October 22, 2020 | 
| [Updated resource](AWS_AppSync.md) | The following resource was updated: AWS::AppSync::ApiKey\. 

 [AWS::AppSync::ApiKey](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-appsync-apikey.html)   
Use the `ApiKeyId` property to specify the API key ID\.  | October 22, 2020 | 
| [Updated resource](AWS_CloudFront.md) | The following resource was updated: AWS::CloudFront::Distribution\. 

[AWS::CloudFront::Distribution](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-cloudfront-distribution.html)  
In the [Origin](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-cloudfront-distribution-origin.html) property type, use the `OriginShield` property to enable CloudFront Origin Shield\.  
For more information, see [Using Origin Shield](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/origin-shield.html) in the *Amazon CloudFront Developer Guide*\.  | October 22, 2020 | 
| [Updated resource](AWS_EMR.md) | The following resource was updated: AWS::EMR::Cluster\. 

 [AWS::EMR::Cluster](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-elasticmapreduce-cluster.html)   
Use the `LogEncryptionKmsKeyId` property to specify the AWS KMS key used for encrypting log files\.  
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
| [Updated resource](AWS_KinesisFirehose.md) | The following resource was updated: AWS::KinesisFirehose::DeliveryStream\. 

 [AWS::KinesisFirehose::DeliveryStream](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-kinesisfirehose-deliverystream.html)   
DeliveryStreamEncryptionConfigurationInput property type is now supported for the delivery streams in CloudFormation\.  | October 22, 2020 | 
| [Updated resource](AWS_Elasticsearch.md) | The following resource was updated: AWS::Elasticsearch::Domain\. 

 [AWS::Elasticsearch::Domain](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-elasticsearch-domain.html)   
In the [ElasticsearchClusterConfig](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-elasticsearch-domain-elasticsearchclusterconfig.html) property type:  
+ Use the `WarmCount` property to specify the number of warm nodes in the cluster\.
+ Use the `WarmEnabled` property to specify whether to enable warm storage for the cluster\.
+ Use the `WarmType` property to specify the instance type for the cluster's warm nodes\.  | October 22, 2020 | 
| [New resources](AWS_MediaPackage.md) | The following resources were added: AWS::MediaPackage::Asset, AWS::MediaPackage::Channel, AWS::MediaPackage::OriginEndpoint, AWS::MediaPackage::PackagingConfiguration, and AWS::MediaPackage::PackagingGroup\. 

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
| [New resource](AWS_SecretsManager.md) | The following updated resource was added: `BlockPublicPolicy` 

 [AWS::SecretsManager::Resource Policies\.BlockPublicPolicy](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-secretsmanager-resourcepolicy.html)   
Use the `BlockPublicPolicy` when adding resource policies to Secrets Manager\.  | October 22, 2020 | 
| [Increased quotas](#ReleaseHistory) | The following AWS CloudFormation quotas have been updated\.  You can now declare a maximum of `200` mappings in your AWS CloudFormation template\.   You can now declare a maximum of `200` mapping attributes for each mapping in your AWS CloudFormation template\.   You can now declare a maximum of `200` outputs in your AWS CloudFormation template\.   You can now declare a maximum of `200` parameters in your AWS CloudFormation template\.   You can now declare a maximum of `500` resources in your AWS CloudFormation template\.   You can now pass a template body with a maximum size of `1 MB` in an Amazon S3 object\.   | October 22, 2020 | 
| [Updated resource](AWS_Synthetics.md) | The following resource was updated: AWS::Synthetics::Canary\. 

 [AWS::Synthetics::Canary](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-synthetics-canary.html)   
The ArtifactConfig and S3Encryption parameters were added\.  | October 21, 2020 | 
| [Updated resource](AWS_AmazonMQ.md) | The following resource was updated: AWS::AmazonMQ::Broker\. 

 [AWS::AmazonMQ::Broker](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-amazonmq-broker.html)   
Use the `LdapServerMetadata` property to to authenticate and authorize connections to a broker\.  | October 9, 2020 | 
| [New resources](AWS_CodeArtifact.md) | The following resources were added: AWS::CodeArtifact::Domain and AWS::CodeArtifact::Repository\. 

 [AWS::CodeArtifact::Domain](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-codeartifact-domain.html)   
Use the `AWS::CodeArtifact::Domain` resource to create an AWS CodeArtifact domain\. 

 [AWS::CodeArtifact::Repository](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-codeartifact-repository.html)   
Use the `AWS::CodeArtifact::Repository` resource to create an AWS CodeArtifact repository\.  | October 8, 2020 | 
| [New resources](AWS_Timestream.md) | The following resources were added: AWS::Timestream::Table and AWS::Timestream::Database\. 

 [AWS::Timestream::Table](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-timestream-table.html)   
Use the `AWS::Timestream::Table` resource to create a new table in an existing database in Amazon Timestream\. 

 [AWS::Timestream::Database](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-timestream-database.html)   
Use the `AWS::Timestream::Database` resource to create a new database in Amazon Timestream\.  | October 8, 2020 | 
| [Updated resources](AWS_ECS.md) | The following resources were updated: AWS::ECS::Service\. 

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
| [Updated resource](AWS_EKS.md) | The following resource was updated to support specifying a custom CIDR for Kubernetes service IP address assignment: `AWS::EKS::Cluster`\. 

 [https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-eks-cluster.html](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-eks-cluster.html)   
Use the `KubernetesNetworkConfig` property to specify a Kubernetes network configuration\. 

 [https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-eks-cluster-kubernetesnetworkconfig.html](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-eks-cluster-kubernetesnetworkconfig.html)   
Use the `ServiceIpv4Cidr` property to specify the CIDR block that you want Kubernetes to assign service IP addresses from\.  | October 1, 2020 | 
| [New resource](AWS_WorkSpaces.md) | The following resource was added: `AWS::WorkSpaces::ConnectionAlias` 

 [AWS::WorkSpaces::ConnectionAlias](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-workspaces-connectionalias.html)   
Use the `AWS::WorkSpaces::ConnectionAlias` resource to specify a connection alias\. Connection aliases are used for cross\-Region redirection\.   | October 1, 2020 | 
| [Drift detection for private resources](#ReleaseHistory) | CloudFormation supports drift detection operations on an expanded list of AWS resources, as well as private resources that are defined as provisonable\.In addition to the resources that previously supported drift detection, CloudFormation now supports drift detection on all resources defined as provisionable in the CloudFormation registry\. For more information, see [Resources that support import and drift detection operations](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/resource-import-supported-resources.html)\. | October 1, 2020 | 
| [Updated resource](AWS_MSK.md) | The following resource was updated: AWS::MSK::Cluster 

 [AWS::MSK::Cluster](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-msk-cluster.html)   
Adding support for SASL/Scram \(sign\-in credentials client authentication\.\)  | September 24, 2020 | 
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
| [New resource](AWS_CloudFormation.md) | The following resource was added: AWS::CloudFormation::StackSet\. 

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
| [New resources](AWS_SSO.md) | The following resources were added: `AWS::SSO::Assignment`, `AWS::SSO::PermissionSet`\.  

 [https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-sso-assignment.html](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-sso-assignment.html)   
Use the `AWS::SSO::Assignment` resource to assign access to a principal for a specified AWS account using a specified permission set\. 

 [https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-sso-permissionset.html](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-sso-permissionset.html)   
Use the `AWS::SSO::PermissionSet` resource to create a permission set within a specified IAM Identity Center instance\.  | September 10, 2020 | 
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
| [New resource](AWS_EKS.md) | The following resource was added: `AWS::EKS::FargateProfile`\. 

 [https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-eks-fargateprofile.html](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-eks-fargateprofile.html)   
Use the `AWS::EKS::FargateProfile` resource to create an AWS Fargate profile\.  | September 3, 2020 | 
| [Updated resource](AWS_CodeCommit.md) | The following resource was updated: `AWS::CodeCommit::Repository Code` 

 [AWS::CodeCommit::Repository Code](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-codecommit-repository-code.html)   
Use the `BranchName` property to specify a branch name to be used as the default branch when importing code into a repository\.  | August 31, 2020 | 
| [Updated resource](AWS_ServiceCatalog.md) | The following resource was updated: AWS::ServiceCatalog::CloudFormationProvisionedProduct\. 

 [AWS::ServiceCatalog::CloudFormationProvisionedProduct](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-servicecatalog-cloudformationprovisionedproduct.html)   
The `PathName` property is now available as an alternative to `PathId`\.  | August 27, 2020 | 
| [New resources](AWS_GameLift.md) | The following resources were added: AWS::GameLift::GameServerGroup 

 [AWS::GameLift::GameServerGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-gamelift-gameservergroup.html)   
Use the `AWS::GameLift::GameServerGroup` resource to create a GameLift FleetIQ game server group to run low\-cost game hosting on your Amazon EC2 instances\.  | August 27, 2020 | 
| [New resources](AWS_Route53Resolver.md) | The following resources were added: `AWS::Route53Resolver::ResolverQueryLoggingConfig` and `AWS::Route53Resolver::ResolverQueryLoggingConfigAssociation`\. 

 [AWS::Route53Resolver::ResolverQueryLoggingConfig](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-route53resolver-resolverqueryloggingconfig.html)   
Use the `AWS::Route53Resolver::ResolverQueryLoggingConfig` resource to specify settings for a query logging configuration\. 

 [AWS::Route53Resolver::ResolverQueryLoggingConfigAssociation](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-route53resolver-resolverqueryloggingconfigassociation.html)   
Use the `AWS::Route53Resolver::ResolverQueryLoggingConfigAssociation` resource to configure DNS query logging\.  | August 27, 2020 | 
| [Updated resource](AWS_KMS.md) | The following resource was updated: AWS::KMS::Key\. 

 [AWS::KMS::Key](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-kms-key.html)   
Added a `KeyId` attribute to the [return values](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-kms-key.html#aws-resource-kms-key-return-values)\.  | August 26, 2020 | 
| [Updated resource](AWS_EKS.md) | The following resource was updated to support use of a launch template: `AWS::EKS::Nodegroup`\. 

 [https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-eks-nodegroup.html](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-eks-nodegroup.html)   
Use the `LaunchTemplate` property to specify a launch template specification that can be used to deploy or update a managed node group\. If you use a launch template to deploy a node group, some settings that you normally set for a node group must be moved into the launch template\. The text for affected settings has been updated to note that\.  | August 20, 2020 | 
| [Updated resources](AWS_ECS.md) | The following resources were updated: AWS::ECS::TaskDefinition\. 

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
| [Updated resources](AWS_ECS.md) | The following resources were updated: AWS::ECS::TaskDefinition\. 

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
| [Updated resources](AWS_WAFv2.md) | The following resources were updated: AWS::WAFv2::WebACL and AWS::WAFv2::RuleGroup\. 

 [AWS::WAFv2::WebACL](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-wafv2-webacl.html)   
Rule statements that use IP addresses now support using IP addresses that are forwarded in an HTTP header in the web request, instead of using the IP address that's reported by the web request origin\. This option is available for all rule statements that use an IP address: `GeoMatchStatement`, `RateBasedStatement`, and `IPSetReferenceStatement`\. The following new properties support this functionality: `IPSetForwardedIPConfiguration` and `ForwardedIPConfiguration`\. 

 [AWS::WAFv2::RuleGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-wafv2-rulegroup.html)   
Rule statements that use IP addresses now support using IP addresses that are forwarded in an HTTP header in the web request, instead of using the IP address that's reported by the web request origin\. This option is available for all rule statements that use an IP address: `GeoMatchStatement`, `RateBasedStatement`, and `IPSetReferenceStatement`\. The following new properties support this functionality: `IPSetForwardedIPConfiguration` and `ForwardedIPConfiguration`\.  | July 23, 2020 | 
| [Updated resource ](AWS_EFS.md) | The following resource was updated: AWS::EFS::FileSystem 

[AWS::EFS::FileSystem](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-efs-filesystem-backuppolicy.html)  
Use the `BackupPolicy` property to turn automatic backups on or off for your Amazon EFS file system\.  | July 23, 2020 | 
| [Updated resource](AWS_CloudFront.md) | The following resource was updated: AWS::CloudFront::Distribution\. 

 [AWS::CloudFront::Distribution](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-cloudfront-distribution.html)   
In the [CacheBehavior](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-cloudfront-distribution-cachebehavior.html) and [DefaultCacheBehavior](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-cloudfront-distribution-defaultcachebehavior.html) property types:  
+ Use the `CachePolicyId` property to specify the ID of the cache policy for the cache behavior\.
+ Use the `OriginRequestPolicyId` property to specify the ID of the origin request policy for the cache behavior\.
For more information, see [Working with policies](https://docs.aws.amazon.com/AmazonCloudFront/latest/DeveloperGuide/working-with-policies.html) in the *Amazon CloudFront Developer Guide*\.  | July 23, 2020 | 
| [Updated resource](AWS_CodeStarConnections.md) | The following resource was updated: AWS::CodeStarConnections::Connection 

 [AWS::CodeStarConnections::Connection](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-codestarconnections-connection.html)   
Use the `HostArn` property to specify the host associated with connections you want to make to an installed provider\.  | July 23, 2020 | 
| [Updated resource](AWS_FSx.md) | The following resource was updated: AWS::FSx::FileSystem 

[AWS::FSx::FileSystem](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-fsx-filesystem.html)  
In the [LustreConfiguration](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-fsx-filesystem-lustreconfiguration.html) property type, use `AutoImportPolicyType` to configure how FSx imports new files and file changes in the linked data repository into the file system\.  | July 23, 2020 | 
| [Updated resource](AWS_SageMaker.md) | The following resource was updated: EndpointConfig 

 [AWS::SageMaker::EndpointConfig](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-sagemaker-endpointconfig.html)   
Use the `CaptureContentTypeHeader` property to specify content types \(JSON and/or CSV\) to capture\.  
Use the `CaptureOption` property to specify whether to capture input data, output data, or both\.  
Use the `DataCaptureConfig` resource/property to configure how the endpoint captures data\.  | July 23, 2020 | 
| [New resource](AWS_SecretsManager.md) | The following resource was added: AWS::SecretsManager::RotationSchedule\.HostedRotationLambda\. 

[AWS::SecretsManager::RotationSchedule](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-secretsmanager-rotationschedule.html)  
Use the `HostedRotationLambda` property type to create a rotation Lambda\.  | July 23, 2020 | 
| [Updated resource](AWS_Amplify.md) | The following resource was updated: AWS::Amplify::App 

 [AWS::Amplify::App](https://docs.aws.amazon.com/AWSCloudFormation/latest/userguide/aws-resource-amplify-app.html)   
Use the `EnableBranchAutoDeletion` property to automatically disconnect a branch in the Amplify Console when you delete a branch from your Git repository\.  | July 9, 2020 | 
| [Updated resource](AWS_Amplify.md) | The following resource was updated: AWS::Amplify::Domain 

 [AWS::Amplify::Domain](https://docs.aws.amazon.com/AWSCloudFormation/latest/userguide/aws-resource-amplify-domain.html)   
Use the `AutoSubDomainCreationPatterns` property to set branch patterns for automatic subdomain creation\.  
Use the `AutoSubDomainIAMRole` property to specify the required AWS Identity and Access Management \(IAM\) service role for the Amazon Resource Name \(ARN\) for automatically creating subdomains\.  
Use the `EnableAutoSubDomain` property to enable the automated creation of subdomains for branches\.  | July 9, 2020 | 
| [Updated resource](AWS_Synthetics.md) | The following resource was updated: AWS::Synthetics::Canary\. 

 [AWS::Synthetics::Canary](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-synthetics-canary.html)   
The MemoryInMB parameter was added\. Also, the RunConfig parameter is no longer required, and DurationInSeconds is no longer required\.   | July 9, 2020 | 
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
| [Updated resource](AWS_ApplicationAutoScaling.md) | The following resource was updated: AWS::ApplicationAutoScaling::ScalableTarget\. 

 [AWS::ApplicationAutoScaling::ScalableTarget](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-applicationautoscaling-scalabletarget.html)   
In the [ScheduledAction](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-applicationautoscaling-scalabletarget-scheduledaction.html) property type, use the `Timezone` property to create scheduled actions in the local time zone\. If your time zone observes Daylight Saving Time \(DST\), it automatically adjusts for Daylight Saving Time\.  | July 1, 2020 | 
| [New resource](AWS_AppConfig.md) | The following resource was added: AWS::AppConfig::HostedConfigurationVersion 

 [AWS::AppConfig::HostedConfigurationVersion](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-appconfig-hostedconfigurationversion.html)   
This resource lets you create a new configuration in the AWS AppConfig hosted configuration store\.  | June 25, 2020 | 
| [Updated resources](AWS_ServiceDiscovery.md) | The following resources were updated: `AWS::ServiceDiscovery::HttpNamespace`, `AWS::ServiceDiscovery::PrivateDnsNamespace`, `AWS::ServiceDiscovery::PublicDnsNamespace`, `AWS::ServiceDiscovery::Service`\. 

[AWS::ServiceDiscovery::HttpNamespace](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-servicediscovery-httpnamespace.html)   
Use the `Tags` property to add tag keys and values to an AWS Cloud Map HTTP namespace\. 

[AWS::ServiceDiscovery::PrivateDnsNamespace](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-servicediscovery-privatednsnamespace.html)   
Use the `Tags` property to add tag keys and values to an AWS Cloud Map private DNS namespace\. 

[AWS::ServiceDiscovery::PublicDnsNamespace](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-servicediscovery-publicdnsnamespace.html)   
Use the `Tags` property to add tag keys and values to an AWS Cloud Map public DNS namespace\. 

[AWS::ServiceDiscovery::Service](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-servicediscovery-service.html)   
Use the `Tags` property to add tag keys and values to an AWS Cloud Map service\.  | June 22, 2020 | 
| [Updated resources](AWS_ECS.md) | The following resources were updated: AWS::ECS::Cluster\. 

 [AWS::ECS::Cluster](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ecs-cluster.html)   
Use the `CapacityProviderStrategyItem` property to specify the capacity provider strategy when creating a cluster\.  | June 18, 2020 | 
| [Updated resource](AWS_FMS.md) | The following resources were updated: AWS::FMS::Policy IEMap\. 

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
| [Updated resource](AWS_ElasticLoadBalancingV2.md) | The following resource was updated: AWS::ElasticLoadBalancingV2::LoadBalancer\. 

 [AWS::ElasticLoadBalancingV2::LoadBalancer](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-elasticloadbalancingv2-loadbalancer-subnetmapping.html)   
Use the `SubnetMapping` attribute to specify a subnet to attach to a load balancer\.  | June 11, 2020 | 
| [Updated resource](AWS_ElastiCache.md) | The following resource was updated: AWS::ElastiCache::ReplicationGroup\. 

 [AWS::ElastiCache::ReplicationGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-elasticache-replicationgroup.html)   
Use the `MultiAZEnabled` attribute to indicate if you have Multi\-AZ enabled\.  | June 11, 2020 | 
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
| [Updated resource](AWS_Synthetics.md) | The following resource was updated: AWS::Synthetics::Canary\. 

 [AWS::Synthetics::Canary](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-synthetics-canary.html)   
The RunConfig parameter is required\.  | May 14, 2020 | 
| [Updated resource](AWS_CodeStarConnections.md) | The following resource was updated: AWS::CodeStarConnections::Connection 

 [AWS::CodeStarConnections::Connection](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-codestarconnections-connection.html)   
Use the `Tags` property to specify the tags applied to your connections resource\.  | May 14, 2020 | 
| [Updated resource](AWS_ServiceCatalog.md) | The following resource was updated: AWS::ServiceCatalog::CloudFormationProduct\. 

 [AWS::ServiceCatalog::CloudFormationProduct](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-servicecatalog-cloudformationproduct.html)   
Use the `ReplaceProvisioningArtifacts` property to choose whether provisioning artifact identifiers are replaced when you update a product\.  | May 14, 2020 | 
| [New resources](AWS_GlobalAccelerator.md) | The following resources were added: AWS::GlobalAccelerator::Accelerator, AWS::GlobalAccelerator::EndpointGroup, and AWS::GlobalAccelerator::Listener 

 [ AWS::GlobalAccelerator::Accelerator](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-globalaccelerator-accelerator.html)   
Use the `AWS::GlobalAccelerator::Accelerator` resource to create or update an accelerator for AWS Global Accelerator\. 

 [ AWS::GlobalAccelerator::EndpointGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-globalaccelerator-endpointgroup.html)   
Use the `AWS::GlobalAccelerator::EndpointGroup` resource to create or update an endpoint group for AWS Global Accelerator\. 

 [ AWS::GlobalAccelerator::Listener](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-globalaccelerator-listener.html)   
Use the `AWS::GlobalAccelerator::Listener` resource to create or update a listener for AWS Global Accelerator\.  | May 14, 2020 | 
| [New resources](AWS_Macie.md) | The following resources were added: `AWS::Macie::CustomDataIdentifier`, `AWS::Macie::FindingsFilter`, and `AWS::Macie::Session` 

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
Use the `AWS::ImageBuilder::Image` resource to create an image in the Image Builder service\.  | May 7, 2020 | 
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
Use the `AWS::ImageBuilder::Component` resource to create a component in the Image Builder service\. 

 [AWS::ImageBuilder::DistributionConfiguration](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-imagebuilder-distributionconfiguration.html)   
Use the `AWS::ImageBuilder::DistributionConfiguration` resource to create a distribution configuration in the Image Builder service\. 

 [AWS::ImageBuilder::ImagePipeline](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-imagebuilder-imagepipeline.html)   
Use the `AWS::ImageBuilder::ImagePipeline` resource to create an image pipeline in the Image Builder service\. 

 [AWS::ImageBuilder::ImageRecipe](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-imagebuilder-imagerecipe.html)   
Use the `AWS::ImageBuilder::ImageRecipe` resource to create an image recipe in the Image Builder service\.  

 [AWS::ImageBuilder::InfrastructureConfiguration](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-imagebuilder-infrastructureconfiguration.html)   
Use the `AWS::ImageBuilder::InfrastructureConfiguration` resource to create an infrastructure configuration in the Image Builder service\.  | April 23, 2020 | 
| [New resource](AWS_Synthetics.md) | The following resource was added: AWS::Synthetics::Canary\. 

 [AWS::Synthetics::Canary](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-synthetics-canary.html)   
Use the `AWS::Synthetics::Canary` resource to create a canary\. Canaries are configurable scripts that run on a schedule and monitor your endpoints and APIs\. By using canaries, you can discover issues before your customers do\.  | April 23, 2020 | 
| [New resource](AWS_CE.md) | The following resource was added: AWS::CE::CostCategory 

 [AWS::CE::CostCategory](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/AWS_CE.html)   
Use the `AWS::CE::CostCategory` resource to create groupings of costs that you can use across products in the AWS Billing and Cost Management console\.  | April 23, 2020 | 
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
| [Updated resource](AWS_Cognito.md) | The following resource was updated: AWS::Cognito::UserPool 

 [AWS::Cognito::UserPool](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-cognito-userpool.html)   
Use the `UsernameConfiguration` property to set case sensitivity on the username input for the selected sign\-in option\.  | March 26, 2020 | 
| [Updated resource](AWS_EC2.md) | The following resource was updated: AWS::EC2::Volume 

 [AWS::EC2::Volume](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ec2-ebs-volume.html)   
Use the `MultiAttachEnabled` property to indicate whether Amazon EBS Multi\-Attach is enabled\.  | March 26, 2020 | 
| [Updated resource](AWS_AutoScaling.md) | The following resource was updated: AWS::AutoScaling::AutoScalingGroup\. 

 [AWS::AutoScaling::AutoScalingGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-as-group.html)   
Use the `MaxInstanceLifetime` property to specify the maximum amount of time, in seconds, that an instance can be in service\.  | March 26, 2020 | 
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
Use `LoggingInfo` to stream broker logs to one or more of the following destination types: Amazon CloudWatch Logs, Amazon S3, Kinesis Data Firehose\.  | March 12, 2020 | 
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
| [Updated resource](AWS_EKS.md) | The following resource was updated to support envelope encryption of secrets with AWS Key Management Service: `AWS::EKS::Cluster` 

 [https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-eks-cluster-encryptionconfig.html](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-eks-cluster-encryptionconfig.html)   
Use the `AWS::EKS::Cluster EncryptionConfig` property to specify the encryption configuration for an Amazon EKS cluster\. 

 [https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-eks-cluster-provider.html](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-eks-cluster-provider.html)   
Use the `AWS::EKS::Cluster Provider` property to specify the AWS Key Management Service customer master key \(CMK\) used to encrypt the secrets for an Amazon EKS cluster\.  | March 5, 2020 | 
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
Use the `AWS::CloudWatch::CompositeAlarm` property to create a composite alarm\. Composite alarms evaluate their alarm state based on the alarm states of other CloudWatchrules\.  | March 2, 2020 | 
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
| [New resource ](AWS_Config.md) | The following resource was added: AWS::Config::ConformancePack 

 [ AWS::Config::ConformancePack](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-config-conformancepack.html)   
Use the `AWS::Config::ConformancePack` resource to create a Conformance Pack that is a collection of AWS rules that can be easily deployed in an account and a region and across AWS Organizations\.  | February 13, 2020 | 
| [New resource ](AWS_Config.md) | The following resource was added: AWS::Config::OrganizationConformancePack 

 [ AWS::Config::OrganizationConformancePack](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-config-organizationconformancepack.html)   
Use the `AWS::Config::OrganizationConformancePack` resource to create an OrganizationConformancePack that has information about conformance packs that AWS Config creates in the member accounts\.  | February 13, 2020 | 
| [New resource](AWS_FMS.md) | The following resources were added: AWS::FMS::NotificationChannel and AWS::FMS::Policy\. 

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
When the property `XrayEnabled` is set to `TRUE`, X\-Ray tracing is enabled for this `GraphqlApi`\.  | February 6, 2020 | 
| [Updated resource](AWS_Cognito.md) | The following resource was updated: AWS::Cognito::UserPool 

 [AWS::Cognito::UserPool](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-cognito-userpool.html)   
Added `AccountRecoverySetting` parameter to define which verified available method a user can use to recover their password\.  | February 6, 2020 | 
| [Updated resource](AWS_OpsWorksCM.md) | The following resource was updated: `AWS::OpsWorksCM::Server` 

 [https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-opsworkscm-server.html](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-opsworkscm-server.html)   
Use the `Tags` property to add tag keys and values to an AWS OpsWorks for Chef Automate or OpsWorks for Puppet Enterprise server\.  | February 6, 2020 | 
| [New resource](AWS_WAFv2.md) | The following resource was added: AWS::WAFv2::WebACLAssociation\. 

 [AWS WAFv2](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/AWS_WAFv2.html)   
Use the web ACL association to define an association between a web ACL and a regional application resource, to protect the resource\. A regional application can be an Application Load Balancer \(ALB\), Amazon API Gateway REST API, an AWS AppSync GraphQL API, or an Amazon Cognito user pool\. For Amazon CloudFront distributions, you use AWS::CloudFront::Distribution to manage the association\.   | February 6, 2020 | 
| [New resources](AWS_ACMPCA.md) | The following resources were added: AWS::ACMPCA::Certificate, AWS::ACMPCA::CertificateAuthority, AWS::ACMPCA::CertificateAuthorityActivation\. 

 [AWS::ACMPCA::Certificate](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-acmpca-certificate.html)   
The `AWS::ACMPCA::Certificate` resource is used to issue a certificate using your private certificate authority\. 

 [AWS::ACMPCA::CertificateAuthority](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-acmpca-certificateauthority.html)   
Use the `AWS::ACMPCA::CertificateAuthority` resource to create a private CA\. 

 [AWS::ACMPCA::CertificateAuthorityActivation](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-acmpca-certificateauthorityactivation.html)   
The `AWS::ACMPCA::CertificateAuthorityActivation` resource creates and installs a CA certificate on a CA\.  | January 23, 2020 | 
| [New resource](AWS_AppConfig.md) | The following resources were added: AWS::AppConfig::Application, AWS::AppConfig::ConfigurationProfile, AWS::AppConfig::Deployment, AWS::AppConfig::Environment, and AWS::AppConfig::DeploymentStrategy 

 [AWS::AppConfig::Application](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-appconfig-application.html)   
The `AWS::AppConfig::Application` resource creates an application, which is a logical unit of code that provides capabilities for your customers\. 

 [AWS::AppConfig::ConfigurationProfile](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-appconfig-configurationprofile.html)   
The `AWS::AppConfig::ConfigurationProfile` resource creates a configuration profile that enables AWS AppConfig to access the configuration source\.  

 [AWS::AppConfig::Deployment](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-appconfig-deployment.html)   
The `AWS::AppConfig::Deployment` resource starts a deployment\.  

 [AWS::AppConfig::Environment](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-appconfig-environment.html)   
The `AWS::AppConfig::Environment` resource creates an environment, which is a logical deployment group of AWS AppConfig targets, such as applications in a `Beta` or `Production` environment\. 

 [AWS::AppConfig::DeploymentStrategy](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-appconfig-deploymentstrategy.html)   
The `AWS::AppConfig::DeploymentStrategy` resource creates an AWS AppConfig deployment strategy\.   | January 23, 2020 | 
| [Updated resource](AWS_Glue.md) | The following resource was updated: AWS::Glue::Crawler 

 [AWS::Glue::Crawler](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-glue-table.html)   
Use the `MongoDBTarget` property to specify an Amazon DocumentDB or MongoDB data store to crawl\.  
Use the `RecrawlPolicy.RecrawlBehavior` property to specify a new `CRAWL_EVENT_MODE` that specifies crawling only the changes identified by Amazon S3 events\.  
Use the `S3Target.SampleSize` property to specify the number of files in each leaf folder to be crawled when crawling sample files in a dataset\.  
Use the `S3Target.EventQueueArn` property to specify a valid Amazon SQS ARN\.  
Use the `S3Target.DlqEventQueueArn` property to specify a valid Amazon dead\-letter SQS ARN\.  | January 20, 2020 | 
| [Updated resources](AWS_Lambda.md) | The following resource was updated: AWS::Lambda::Function\. 

 [AWS::Lambda::Function](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-lambda-function.html)   
In the [Code](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-lambda-function-code.html) property type, `ZipFile` supports `nodejs12.x` for `RunTime`\.  | January 16, 2020 | 
| [Updated resource](AWS_EC2.md) | The following resource was updated: AWS::EC2::Instance\. 

 [AWS::EC2::Instance](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ec2-instance.html)   
Use the `HibernationOptions` property to indicate whether the instance is enabled for hibernation\.  
Use the `HostResourceGroupArn` property to specify the ARN of the host resource group in which to launch the instances\.  | January 16, 2020 | 
| [Updated resource](AWS_AutoScaling.md) | The following resource was updated: AWS::AutoScaling::AutoScalingGroup\. 

 [AWS::AutoScaling::AutoScalingGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-as-group.html)   
Use the `WeightedCapacity` property to specify the number of capacity units, which gives the instance type a proportional weight to other instance types\.  | January 16, 2020 | 
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
| [New resource](AWS_WAFv2.md) | The following resource was added: AWS WAFv2\. 

 [AWS WAFv2](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/AWS_WAFv2.html)   
This is the latest version of AWS WAF, a web application firewall that lets you monitor HTTP\(S\) requests that are forwarded to an Amazon API Gateway REST API, Amazon CloudFront, Application Load Balancer, an AWS AppSync GraphQL API, or an Amazon Cognito user pool\. AWS WAF also lets you control access to your content\.  | November 25, 2019 | 
| [Updated resources](AWS_AppSync.md) | The following resources were updated: AWS::AppSync::Resolver, AWS::AppSync::DataSource\. 

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
Use the `ClusterSettings` property to specify the setting to use when creating a cluster\. This parameter is used to use CloudWatch Container Insights for a cluster\. 

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
Use the `PrivateCertificateAuthorityArn` property to specify a private certificate authority \(CA\) from AWS Private CA as certificate issuer\.  
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
| [Updated resource](AWS_Glue.md) | The following resource was updated: AWS::Glue::MLTransform 

 [AWS::Glue::MLTransform](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-glue-mltransform.html)   
Use the `GlueVersion` property to specify which version of AWS Glue this machine learning transform is compatible with\.  | November 21, 2019 | 
| [Updated resource](AWS_IAM.md) | The following resource was updated: AWS::IAM::User\. 

 [AWS::IAM::User](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-iam-user.html)   
Use the `Tags` property to specify a list of tags that you want to attach to the newly created user\.  | November 21, 2019 | 
| [Updated resource](AWS_Elasticsearch.md) | The following resource was updated: AWS::Elasticsearch::Domain\. 

 [AWS::Elasticsearch::Domain](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-elasticsearch-domain.html)   
Use the `CognitoOptions` property to configure OpenSearch Service to use Amazon Cognito authentication for OpenSearch Dashboards\.  
Use the [EnableVersionUpgrade](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-attribute-updatepolicy.html#cfn-attributes-updatepolicy-upgradeelasticsearchversion) update policy to update the `ElasticsearchVersion` property without replacing the `AWS::Elasticsearch::Domain` resource\.  | November 21, 2019 | 
| [Updated resource](AWS_OpsWorksCM.md) | The following resource was updated: `AWS::OpsWorksCM::Server` 

 [https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-opsworkscm-server.html](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-opsworkscm-server.html)   
Use the `CustomDomain` property to specify a custom domain on an AWS OpsWorks for Chef Automate Server running Chef Automate 2\.0\.  
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
| [Drift Detection for Stack Sets](#ReleaseHistory) | You can now run drift detection on a stack set and all the stack instances it includes\.When CloudFormation performs drift detection on a stack set, it performs drift detection on the stack associated with each stack instance in the stack set\. For more details, see [Detecting Unmanaged Configuration Changes in Stack Sets](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/stacksets-drift.html)\. | November 19, 2019 | 
| [Updated resource](AWS_EKS.md) | The following resource was updated to support Amazon EKS managed node groups: `AWS::EKS::Cluster` 

 [https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-eks-cluster.html](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-eks-cluster.html)   
Use the `AWS::EKS::Cluster` resource to create a new Amazon EKS cluster\.  | November 18, 2019 | 
| [New resource](AWS_EKS.md) | The following resource was added: `AWS::EKS::Nodegroup` 

 [https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-eks-nodegroup.html](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-eks-nodegroup.html)   
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

 [AWS::Amplify::App](https://docs.aws.amazon.com/AWSCloudFormation/latest/userguide/aws-resource-amplify-app.html)   
Use the `EnablePullRequestPreview` property to specify whether pull request previews are enabled for each branch that Amplify Console automatically creates for your app\.  
Use the `PullRequestEnvironmentName` property to specify a dedicated backend environment for your pull request previews\.  | October 31, 2019 | 
| [Updated resource](AWS_ECS.md) | The following resource was updated: AWS::ECS::TaskDefinition\. 

 [AWS::ECS::TaskDefinition](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ecs-taskdefinition.html)   
Use the `InferenceAccelerator` property to specify the Elastic Inference accelerators to use for the containers in the task\.  | October 31, 2019 | 
| [Updated resource](AWS_Events.md) | The following resource was updated: AWS::Events::Rule\. 

 [AWS::Events::Rule](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-events-rule.html)   
In the [Target](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-events-rule-target.html) property type, use the `BatchParameters` property to specify the job definition, job name, and other parameters, if the event target is an AWS Batch job\.  | October 31, 2019 | 
| [Updated resource](AWS_Elasticsearch.md) | The following resource was updated: AWS::Elasticsearch::Domain\. 

 [AWS::Elasticsearch::Domain](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-elasticsearch-domain.html)   
Use the `LogPublishingOptions` property to configure slow log publishing\.  | October 31, 2019 | 
| [New resources](AWS_Pinpoint.md) | The following resources were added: AWS::Pinpoint::EmailTemplate, AWS::Pinpoint::PushTemplate, and AWS::Pinpoint::SmsTemplate\. 

 [AWS::Pinpoint::EmailTemplate](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-pinpoint-emailtemplate.html)   
Use the `AWS::Pinpoint::EmailTemplate` resource to create a message template that you can use in messages that are sent through the email channel\. 

 [AWS::Pinpoint::PushTemplate](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-pinpoint-pushtemplate.html)   
Use the `AWS::Pinpoint::PushTemplate` resource to create a message template that you can use in messages that are sent through a push notification channel\. 

 [AWS::Pinpoint::SmsTemplate](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-pinpoint-smstemplate.html)   
Use the `AWS::Pinpoint::SmsTemplate` resource to create a message template that you can use in messages that are sent through the SMS channel\.  | October 31, 2019 | 
| [Updated resource](AWS_Amplify.md) | The following resource was updated: AWS::Amplify::Branch 

 [AWS::Amplify::Branch](https://docs.aws.amazon.com/AWSCloudFormation/latest/userguide/aws-resource-amplify-branch.html)   
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
| [Updated resources](AWS_Pinpoint.md) | The following resource was updated: AWS::Pinpoint::App, AWS::Pinpoint::Campaign, and AWS::Pinpoint::Segment\. 

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
Use the AWS::Glue::Workflow resource to manage AWS Glue workflows\.  | September 26, 2019 | 
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
In the [Ebs](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ec2-blockdev-template.html) property type, use the `KmsKeyId` property to specify an identifier \(key ID, key alias, ID ARN, or alias ARN\) for a customer managed key under which the EBS volume is encrypted\. 

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
Use the `AWS::LakeFormation:Permissions` resource to grant or revoke Lake Formation permissions\.  | August 8, 2019 | 
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
For the `NumberofWorkers` property, when you specify a Python shell job \(`JobCommand.Name`="pythonshell"\), you can allocate either 0\.0625 or 1 DPU\. The default is 0\.0625 DPU\. When you specify an Apache Spark ETL job \(`JobCommand.Name`="glueetl"\), you can allocate from 2 to 100 DPUs\. The default is 10 DPUs\. This job type can't have a fractional DPU allocation\.  
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
Use the `encryptionOptions` property to specify an AWS owned key or a customer managed key\.  | July 22, 2019 | 
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
The `AWS::MediaLive::InputSecurityGroup` resource creates an input security group\. A MediaLive input security group is associated with a MediaLive input\. The input security group is an "allow list" of IP addresses that controls whether an external IP address can push content to the associated MediaLive input\.  | June 27, 2019 | 
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
Use `ServiceDiscovery` to specify whether to use `AWSCloudMap` or `DNS` for service discovery\. If using AWS Cloud Map for service discovery, use `AwsCloudMapServiceDiscovery` to specify `ServiceName`, `NamespaceName`, and `Attributes` properties\. Use `AwsCloudMapInstanceAttribute` to specify key\-value pairs for `AwsCloudMapServiceDiscovery`\. 

 [AWS::CodeBuild::Project](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-codebuild-project.html)   
Use the `SecondarySourceVersions` property to specify an array of `ProjectSourceVersion` objects\. If `secondarySourceVersions` is specified at the build level, then they take over these `secondarySourceVersions` \(at the project level\)\. 

 [AWS::DLM::LifecyclePolicy](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-dlm-lifecyclepolicy.html)   
In the [PolicyDetails](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-dlm-lifecyclepolicy-policydetails.html) property type:  
+ Use the `PolicyType` property to determine the valid target resource types and actions a policy can manage\. This field defaults to EBS\_SNAPSHOT\_MANAGEMENT if not present\.
+ Use the `Parameters` property to specify a set of optional parameters that can be provided by the policy\.
In the [Schedule](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-dlm-lifecyclepolicy-schedule.html) property type, use the `VariableTags` property to specify a collection of key\-value pairs with values determined dynamically when the policy is executed\. Keys may be any valid Amazon EC2 tag key\. Values must be in one of the two following formats: `$(instance-id)` or `$(timestamp)`\. Variable tags are only valid for EBS Snapshot Management Instance policies\. 

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
+ Use the `ErrorOutputPrefix` property to specify a prefix that Amazon Kinesis Data Firehose evaluates and adds to failed records before writing them to S3\.
+ The `Prefix` property is no longer required\.
In the [S3DestinationConfiguration](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-kinesisfirehose-deliverystream-s3destinationconfiguration.html) property type, use the `ErrorOutputPrefix` property to specify a prefix that Amazon Kinesis Data Firehose evaluates and adds to failed records before writing them to S3\. 

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

 [AWS::EC2::ClientVpnAuthorizationRule](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-clientvpnauthorizationrule.html)   
Specifies an ingress authorization rule to add to a Client VPN endpoint\. Ingress authorization rules act as firewall rules that grant access to networks\. 

 [AWS::EC2::ClientVpnEndpoint](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-clientvpnendpoint.html)   
Specifies a Client VPN endpoint\. A Client VPN endpoint is the resource you create and configure to enable and manage Client VPN sessions\. It is the destination endpoint at which all Client VPN sessions are terminated\. 

 [AWS::EC2::ClientVpnRoute](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-clientvpnroute.html)  
Specifies a network route to add to a Client VPN endpoint\. Each Client VPN endpoint has a route table that describes the available destination network routes\. Each route in the route table specifies the path for traﬃc to speciﬁc resources or networks\. 

 [AWS::EC2::ClientVpnTargetNetworkAssociation](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-clientvpntargetnetworkassociation.html)   
Specifies a target network to associate with a Client VPN endpoint\. A target network is a subnet in a VPC\. You can associate multiple subnets from the same VPC with a Client VPN endpoint\. 

 [AWS::MSK::Cluster](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-msk-cluster.html)   
Use the `AWS::MSK::Cluster` resource to create an Amazon MSK cluster\.  | June 13, 2019 | 
| [Updated resources](#ReleaseHistory) | The following resource was updated: AWS::SageMaker::NotebookInstance\. 

 [AWS::SageMaker::NotebookInstance](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-sagemaker-notebookinstance.html)   
Use the `AcceleratorTypes` property to specify a list of Amazon Elastic Inference \(EI\) instance types to associate with this notebook instance\.  
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
The `AWS::WAFRegional::RateBasedRule` resource is identical to a regular Rule, with one addition: a RateBasedRule counts the number of requests that arrive from a specified IP address every 5 minutes\. 

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
In the [ProvisioningArtifactProperties](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-servicecatalog-cloudformationproduct-provisioningartifactproperties.html) property type, if `DisableTemplateValidation` is set to `true`, Service Catalog stops validating the specified provisioning artifact even if it is invalid\.  | May 3, 2019 | 
| [New resources](#ReleaseHistory) | The following resources were added: AWS::ApiGatewayV2::ApiMapping and AWS::ApiGatewayV2::DomainName\. 

 [AWS::ApiGatewayV2::ApiMapping](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-apigatewayv2-apimapping.html)   
The AWS CloudFormation `AWS::ApiGatewayV2::ApiMapping` resource contains an API mapping\. 

 [AWS::ApiGatewayV2::DomainName](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-apigatewayv2-domainname.html)   
Use the AWS CloudFormation `AWS::ApiGatewayV2::DomainName` resource to specify a custom, friendly URL for your API in API Gateway\.  | May 3, 2019 | 
| [Limit for resources in concurrent stack operations ](#ReleaseHistory) | AWS CloudFormation now enforces an account limit for the number of resources in concurrent stack operations\. This limit is determined by region\.For more information, see [AWS CloudFormation quotas](cloudformation-limits.md) | April 30, 2019 | 
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
Use the `AWS::ServiceCatalog::ResourceUpdateConstraint` resource to create a RESOURCE\_UPDATE constraint for AWS Service Catalog\.  | April 4, 2019 | 
| [Updated resources](#ReleaseHistory) | The following resources were updated: AWS::AppStream::Fleet, AWS::AppStream::ImageBuilder, AWS::AppStream::Stack, and AWS::EKS::Cluster\. 

 [AWS::AppStream::Fleet](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-appstream-fleet.html), [AWS::AppStream::ImageBuilder](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-appstream-imagebuilder.html), and [AWS::AppStream::Stack](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-appstream-stack.html)   
Use the `Tags` property to add or overwrite one or more tags for an Amazon AppStream 2\.0 fleet, stack, or image builder\. 

 [AWS::EKS::Cluster](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-eks-cluster.html)   
Updates to the `Version` property no longer require replacement\.  | March 28, 2019 | 
| [New resources](#ReleaseHistory) | The following resources were added: AWS::AppMesh::Mesh, AWS::AppMesh::Route, AWS::AppMesh::VirtualNode, AWS::AppMesh::VirtualRouter, and AWS::AppMesh::VirtualService\. 

 [AWS::AppMesh::Mesh](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-appmesh-mesh.html)   
The `AWS::AppMesh::Mesh` resource to specify a service mesh\. A service mesh is a logical boundary for network traffic between the services that reside within it\. 

 [AWS::AppMesh::Route](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-appmesh-route.html)   
Use the `AWS::AppMesh::Route` resource to specify a route that's associated with a virtual router\. 

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
Use the `AWS::RoboMaker::Fleet` resource to create an AWS RoboMaker fleet\. 

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
In the [ProjectTriggers](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-codebuild-project-projecttriggers.html) property type, you can use the `WebhookFilters` property to specify the webhook events that trigger a new AWS CodeBuild build\.  | February 15, 2019 | 
| [New resources](#ReleaseHistory) | The following resources were added: AWS::FSx::FileSystem, AWS::KinesisAnalyticsv2::Application, AWS::KinesisAnalyticsv2::ApplicationCloudWatchLoggingOption, AWS::KinesisAnalyticsv2::ApplicationOutput, and AWS::KinesisAnalyticsv2::ApplicationReferenceDataSource\. 

 [AWS::FSx::FileSystem](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-fsx-filesystem.html)   
Use the `AWS::FSx::FileSystem` resource to create a new FSx for Lustre or FSx for Windows File Server file system\. 

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
| [New resources](#ReleaseHistory) | The following resources were added: AWS::ApiGatewayV2::Api, AWS::ApiGatewayV2::Authorizer, AWS::ApiGatewayV2::Deployment, AWS::ApiGatewayV2::Integration, AWS::ApiGatewayV2::IntegrationResponse, AWS::ApiGatewayV2::Model, AWS::ApiGatewayV2::Route, AWS::ApiGatewayV2::RouteResponse, and AWS::ApiGatewayV2::Stage\. 

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
| [UpdateReplacePolicy attribute added](#ReleaseHistory) | Use the UpdateReplacePolicy attribute to retain or \(in some cases\) backup the existing physical instance of a resource when it is replaced during a stack update operation\.For more information, see [UpdateReplacePolicy Attribute](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-attribute-updatereplacepolicy.html)\. | January 23, 2019 | 
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
| [The `CAPABILITY_AUTO_EXPAND` capability is now available\.](#ReleaseHistory) | Use the `CAPABILITY_AUTO_EXPAND` capability to create or update a stack directly from a stack template that contains macros, without first reviewing the resulting changes in a change set first\.For more information, see [CreateStack](https://docs.aws.amazon.com/AWSCloudFormation/latest/APIReference/API_CreateStack.html) or [UpdateStack](https://docs.aws.amazon.com/AWSCloudFormation/latest/APIReference/API_UpdateStack.html) in *AWS CloudFormation API Reference*\. | December 7, 2018 | 
| [Updated resource](#ReleaseHistory) | The following resource was updated: AWS::CodeBuild::Project\. 

 [AWS::CodeBuild::Project](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-codebuild-project.html)   
+ In the [Environment](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-codebuild-project-environment.html) property type, you can use the `Certificate` property to specify a certificate to use with your build project\.
+ In the [Artifacts](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-codebuild-project-artifacts.html) property type, you can use the `ArtifactIdentifier` property to identify the project artifact\.
+ In the [Source](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-codebuild-project-source.html) property type, you can use the `SourceIdentifier` property to identify the project source\.  | December 6, 2018 | 
| [Updated resource](#ReleaseHistory) | The following resource was updated: AWS::Lambda::Function 

 [AWS::Lambda::Function](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-lambda-function.html)   
Use the `Layers` property to specify a list of Amazon Resource Names \(ARNs\) for the function layers to add to the function's execution environment\.  | November 29, 2018 | 
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
Use the `AWS::Kinesis::StreamConsumer` resource to register a consumer with a Kinesis data stream\. 

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
In the [Actions](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-codepipeline-pipeline-stages-actions.html) property type, use the `Region` property to specify the action's AWS Region, such as `us-east-1`\.  | November 13, 2018 | 
| [Stack drift detection added](#ReleaseHistory) | Drift detection enables you to detect whether a stack's actual configuration differs, or has *drifted*, from its expected template configuration as defined within AWS CloudFormation\. You can have AWS CloudFormation detect drift on an entire stack, or individual stack resources\.For more information, see [Detecting Unmanaged Configuration Changes to Stacks and Resources](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-stack-drift.html)\. | November 13, 2018 | 
| [Updated resources](#ReleaseHistory) | The following resources have been updated: AWS::ApiGateway::Deployment, AWS::ApiGateway::Stage, AWS::CloudWatch::Alarm, AWS::EC2::SecurityGroupIngress, AWS::IAM::Role, AWS::IAM::User, AWS::IoT::TopicRule, AWS::KMS::Key, AWS::RDS::DBCluster, AWS::RDS::DBInstance, AWS::Route53::RecordSet, AWS::S3::Bucket, and AWS::Workspaces::Workspace\. 

 [AWS::ApiGateway::Deployment](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-apigateway-deployment.html)   
In the [StageDescription](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-apigateway-deployment-stagedescription.html) property type, use the `TracingEnabled` property to specify whether active tracing with X\-Ray is enabled for this stage\. 

 [AWS::ApiGateway::Stage](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-apigateway-stage.html)   
Use the `TracingEnabled` property to specify whether active tracing with X\-Ray is enabled for this stage\. 

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
Use the `PendingWindowInDays` property to specify the waiting period, specified in number of days, after which AWS Key Management Service deletes the AWS KMS key\. 

 [AWS::RDS::DBInstance](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-rds-database-instance.html)   
Use the `EnableCloudwatchLogsExports` property to specify the list of log types that need to be enabled for exporting to CloudWatch Logs\.  
Use the `EnableIAMDatabaseAuthentication` property to enable mapping of AWS Identity and Access Management \(IAM\) accounts to database accounts\.  
Use the `EnablePerformanceInsights` property to enable Performance Insights for the DB instance\.  
Use the `PerformanceInsightsKMSKeyId` property to specify the KMS key identifier for encryption of Performance Insights data\. The KMS key ID is the Amazon Resource Name \(ARN\), KMS key identifier, or the KMS key alias for the AWS KMS encryption key\.  
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
| [The `secretsmanager` dynamic reference is now available\.](#ReleaseHistory) | Use the `secretsmanager` dynamic reference to retrieve entire secrets or secret values that are stored in AWS Secrets Manager for use in your templates\. *Secrets* can be database credentials, passwords, third\-party API keys, and even arbitrary text\. Using the `secretsmanager` dynamic reference guarantees that neither Secrets Manager nor CloudFormation logs or persists any resolved secret value\.For more information, see [Using Dynamic References to Specify Template Values](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/dynamic-references.html)\. | November 9, 2018 | 
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
Use the `AWS::AppStream::User` resource to create a new user in the user pool for Amazon AppStream 2\.0\.  | October 25, 2018 | 
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
| [UseOnlineResharding update policy now available\.](#ReleaseHistory) | To modify a replication group's shards by adding or removing shards, rather than replacing the entire `AWS::ElastiCache::ReplicationGroup` resource, use the `UseOnlineResharding` update policy\.For more information, see [UseOnlineResharding Policy](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-attribute-updatepolicy.html#cfn-attributes-updatepolicy-useonlineresharding)\. | September 20, 2018 | 
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
Use the `LogDestinationType` property to specify the type of destination to which the flow log data is to be published\. Flow log data can be published to Amazon CloudWatch Logs or Amazon S3\. 

 [AWS::EC2::SpotFleet](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-spotfleet.html)   
In the `SpotFleetRequestConfigData` property type, use the `InstanceInterruptionBehavior` property to specify the behavior when a Spot Instance is interrupted\.  
In the `SpotFleetRequestConfigData` property type, use the `LoadBalancersConfig` property to specify one or more Classic Load Balancers and target groups to attach to the Spot Fleet request\. Spot Fleet registers the running Spot Instances with the specified Classic Load Balancers and target groups\.  
In the `Placement` property type, use the `Tenancy` property to specify the tenancy of the instance \(if the instance is running in a VPC\)\. An instance with a tenancy of dedicated runs on single\-tenant hardware\. The host tenancy isn't supported for Spot Instances\. 

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
| [Macros now available](#ReleaseHistory) | Use macros to perform custom processing on templates, from simple actions like find\-and\-replace operations to extensive transformations of entire templates\.See [Using AWS CloudFormation Macros to Perform Custom Processing on Templates](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/template-macros.html) for more information\. | September 6, 2018 | 
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
| [AWS CloudFormation now supports VPC endpoints powered by PrivateLink\.](#ReleaseHistory) | You can use a VPC endpoint to create a private connection between your VPC and AWS CloudFormation without requiring access over the Internet, through a NAT instance, a VPN connection, or AWS Direct Connect\.For more information, see [Setting Up VPC Endpoints for AWS CloudFormation](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/cfn-vpce-bucketnames.html)\. | August 22, 2018 | 
| [Dynamic references support secure strings](#ReleaseHistory) | Use new dynamic references to specify values that are stored and managed in other services, including Systems Manager Parameter Store SecureString type parameters, in your stack templates\.For more information, see [Using Dynamic References to Specify Template Values](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/dynamic-references.html)\. | August 16, 2018 | 
| [Updated resources](#ReleaseHistory) | The following resources were updated: AWS::ApiGateway::DomainName, AWS::CertificateManager::Certificate, AWS::EC2::VPCPeeringConnection, AWS::EFS::FileSystem, AWS::EMR::Cluster, AWS::RDS::DBClusterParameterGroup, AWS::SNS::Subscription, and AWS::SQS::Queue\. 

 [AWS::ApiGateway::DomainName](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-apigateway-domainname.html)   

Use the following attributes with the `Fn::GetAtt` intrinsic function:
+ The `DistributionHostedZoneId` attribute returns the region\-agnostic Route 53 Hosted Zone ID of the edge\-optimized endpoint\.
+ The `RegionalDomainName` attribute returns the domain name associated with the regional endpoint for this custom domain name\.
+ The `RegionalHostedZoneId` attribute returns the region\-specific Route 53 Hosted Zone ID of the regional endpoint\. 

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
Use the `SSESpecification` property to specify the settings to enable server\-side encryption\.  | August 9, 2018 | 
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
Use the `VpcEndpointType` property to specify the type of endpoint\.  | June 21, 2018 | 
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
Use the `AWS::AmazonMQ::Configuration` resource to create a configuration, update the specified configuration, or return information about the specified configuration\.  | June 14, 2018 | 
| [New resource](#ReleaseHistory) | The following resource was added: AWS::SSM::ResourceDataSync\. 

 [AWS::SSM::ResourceDataSync](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ssm-resourcedatasync.html)   
Use the `AWS::SSM::ResourceDataSync` resource to create or delete a Resource Data Sync for Systems Manager Inventory\. You can use Resource Data Sync to send Inventory data collected from all your Systems Manager managed instances to a single Amazon S3 bucket\.  | June 11, 2018 | 
| [New resource](#ReleaseHistory) | The following resource was released: AWS::EKS::Cluster\. 

 [AWS::EKS::Cluster](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-eks-cluster.html)   
Use the `AWS::EKS::Cluster` resource to create Amazon EKS clusters\.  | June 5, 2018 | 
| [Updated resource](#ReleaseHistory) | For the AWS::GuardDuty::Master resource, the InvitationId property is now optional\. 

 [AWS::GuardDuty::Master](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-guardduty-master.html)   
The `InvitationId` property is now optional\.  | May 31, 2018 | 
| [New resources](#ReleaseHistory) | The following new resources were released: AWS::SageMaker::Endpoint, AWS::SageMaker::EndpointConfig, AWS::SageMaker::Model, AWS::SageMaker::NotebookInstance, and AWS::SageMaker::NotebookInstanceLifecycleConfig\. 

 [AWS::SageMaker::Endpoint](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-sagemaker-endpoint.html)   
Use the `AWS::SageMaker::Endpoint` resource to create a Amazon SageMaker endpoint to host trained models\. 

 [AWS::SageMaker::EndpointConfig](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-sagemaker-endpointconfig.html)   
Use the `AWS::SageMaker::EndpointConfig` resource to create a configuration for an endpoint\. 

 [AWS::SageMaker::Model](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-sagemaker-model.html)   
Use the `AWS::SageMaker::Model` resource to create a model to host at an Amazon SageMaker endpoint\. 

 [AWS::SageMaker::NotebookInstance](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-sagemaker-notebookinstance.html)   
Use the `AWS::SageMaker::NotebookInstance` resource to create an Amazon SageMaker notebook instance\. 

 [AWS::SageMaker::NotebookInstanceLifecycleConfig](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-sagemaker-notebookinstancelifecycleconfig.html)   
Use the `AWS::SageMaker::NotebookInstanceLifecycleConfig` resource to specify shell scripts that run when you create or start a notebook instance\.  | May 31, 2018 | 
| [Stack sets now support customized execution roles](#ReleaseHistory) | Use customized execution roles in target accounts to control the stack resources that users or groups can include in their stack sets\.For more information, see [Granting Permissions for Stack Set Operations](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/stacksets-prereqs.html)\. | May 30, 2018 | 
| [Selective updates of stack instances](#ReleaseHistory) | Use the optional Accounts and Regions parameters to specify the accounts and regions in which to update stack instances during a stack set update operation\.For more information, see [UpdateStackSet](https://docs.aws.amazon.com/AWSCloudFormation/latest/APIReference/API_UpdateStackSet.html) in the *AWS CloudFormation API Reference*\. | May 30, 2018 | 
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
Use the `EncryptionAtRestOptions` property type to specify whether the domain should encrypt data at rest, and if so, the AWS Key Management Service key to use\. 

 [AWS::IAM::Role](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-iam-role.html)   
Use the `RoleId` attribute to have `Fn::GetAtt` return the stable and unique string identifying the role\.  
Use the `MaxSessionDuration` property to specify the maximum session duration \(in seconds\) for the specified role\. 

 [AWS::KinesisFirehose::DeliveryStream](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-kinesisfirehose-deliverystream.html)   
Use the `SplunkDestinationConfiguration` property to specify the configuration of a destination in Splunk for a Kinesis Data Firehose delivery stream\. 

 [AWS::Lambda::EventSourceMapping](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-lambda-eventsourcemapping.html)   
The `StartingPosition` property is no longer required\. 

 [AWS::Logs::MetricFilter](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-logs-metricfilter.html)   
In the [MetricTransformation](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-logs-metricfilter-metrictransformation.html) property type, use the `DefaultValue` property to specify the value to emit when a filter pattern doesn't match a log event\. 

 [AWS::SSM::Association](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ssm-association.html)   
Use the `OutputLocation` property to specify an Amazon S3 bucket where you want to store the results of an association request\.  | May 24, 2018 | 
| [New resources](#ReleaseHistory) | The following new resources were released: AWS::ServiceCatalog::AcceptedPortfolioShare, AWS::ServiceCatalog::CloudFormationProduct, AWS::ServiceCatalog::LaunchNotificationConstraint, AWS::ServiceCatalog::LaunchRoleConstraint, AWS::ServiceCatalog::LaunchTemplateConstraint, AWS::ServiceCatalog::Portfolio, AWS::ServiceCatalog::PortfolioPrincipalAssociation, AWS::ServiceCatalog::PortfolioProductAssociation, AWS::ServiceCatalog::PortfolioShare, AWS::ServiceCatalog::TagOption, and AWS::ServiceCatalog::TagOptionAssociation\. 

 [AWS::ServiceCatalog::AcceptedPortfolioShare](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-servicecatalog-acceptedportfolioshare.html)   
Use the `AWS::ServiceCatalog::AcceptedPortfolioShare` resource to accept an offer to share the specified portfolio for Service Catalog\. 

 [AWS::ServiceCatalog::CloudFormationProduct](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-servicecatalog-cloudformationproduct.html)   
Use the `AWS::ServiceCatalog::CloudFormationProduct` resource to create a product for Service Catalog\. 

 [AWS::ServiceCatalog::LaunchNotificationConstraint](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-servicecatalog-launchnotificationconstraint.html)   
Use the `AWS::ServiceCatalog::LaunchNotificationConstraint` resource to create a notification constraint for Service Catalog\. 

 [AWS::ServiceCatalog::LaunchRoleConstraint](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-servicecatalog-launchroleconstraint.html)   
Use the `AWS::ServiceCatalog::LaunchRoleConstraint` resource to create a launch constraint for Service Catalog\. 

 [AWS::ServiceCatalog::LaunchTemplateConstraint](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-servicecatalog-launchtemplateconstraint.html)   
Use the `AWS::ServiceCatalog::LaunchTemplateConstraint` resource to create a template constraint for Service Catalog\. 

 [AWS::ServiceCatalog::Portfolio](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-servicecatalog-portfolio.html)   
Use the `AWS::ServiceCatalog::Portfolio` resource to create a portfolio for Service Catalog\. 

 [AWS::ServiceCatalog::PortfolioPrincipalAssociation](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-servicecatalog-portfolioprincipalassociation.html)   
Use the `AWS::ServiceCatalog::PortfolioPrincipalAssociation` resource to associate a principal with a portfolio for Service Catalog\. 

 [AWS::ServiceCatalog::PortfolioProductAssociation](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-servicecatalog-portfolioproductassociation.html)   
Use the `AWS::ServiceCatalog::PortfolioProductAssociation` resource to associate a product with a portfolio for Service Catalog\. 

 [AWS::ServiceCatalog::PortfolioShare](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-servicecatalog-portfolioshare.html)   
Use the `AWS::ServiceCatalog::PortfolioShare` resource to share a portfolio for Service Catalog\. 

 [AWS::ServiceCatalog::TagOption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-servicecatalog-tagoption.html)   
Use the `AWS::ServiceCatalog::TagOption` resource to create a TagOption\. 

 [AWS::ServiceCatalog::TagOptionAssociation](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-servicecatalog-tagoptionassociation.html)   
Use the `AWS::ServiceCatalog::TagOptionAssociation` resource to associate a TagOption with a resource for Service Catalog\.  | May 24, 2018 | 
| [AWS CloudFormation now creates S3 buckets with encryption enabled](#ReleaseHistory) | For Amazon S3 buckets that AWS CloudFormation creates to store uploaded stack templates, server\-side encryption is now enabled by default, thereby encrypting all objects stored in those buckets\.For more information, see [Selecting a Stack Template](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/cfn-using-console-create-stack-template.html)\. | May 24, 2018 | 
| [New resource](#ReleaseHistory) | The following resource was released: AWS::Budgets::Budget\. 

 [AWS::Budgets::Budget](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-budgets-budget.html)   
Use the `AWS::Budgets::Budget` resource to create a budget\.  | May 22, 2018 | 
| [FIPS endpoints added](#ReleaseHistory) | AWS CloudFormation now offers new endpoints which use FIPS 140\-2 validated cryptographic modules in the following public US regions: US\-East\-1, US\-East\-2, US\-West\-1, and US\-West\-2\.See [Regions and Endpoints](https://docs.aws.amazon.com/general/latest/gr/rande.html#cfn_region) in the *[Amazon Web Services General Reference](https://docs.aws.amazon.com/general/latest/gr/)* for the new FIPS\-compliant endpoint URLs\. | May 17, 2018 | 
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
Use the `AWS::ServiceCatalog::CloudFormationProvisionedProduct` resource to provision the specified product for Service Catalog\.  | May 1, 2018 | 

## Earlier updates<a name="release-history-earlier-updates"></a>

The following table describes important changes in each release of the AWS CloudFormation User Guide before May 2018\.


| Change | Release Date | Description | API Version | 
| --- | --- | --- | --- | 
|  Updated resources  |  July 22, 2019  |  Use the `encryptionOptions` property to specify an AWS owned key or a customer managed key for Amazon MQ brokers\.  |  2010\-05\-15  | 
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
|  StackSets now supports a maximum of 500 stack instances per stack set\.  |  November 6, 2017  |  You can now create up to a maximum of 500 stack instances per stack set\. For more information about AWS CloudFormation limits, see [AWS CloudFormation Limits](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/cloudformation-limits.html)\.  |  2010\-05\-15  | 
|  New resources  |  November 2, 2017  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html)  |  2010\-05\-15  | 
| Updated resources | November 2, 2017 |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html)  | 2010\-05\-15 | 
|  New resources  |  October 24, 2017  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html)  |  2010\-05\-15  | 
|  New resources  |  October 11, 2017  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html)  |  2010\-05\-15  | 
|  New resource  |  October 10, 2017  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html)  |  2010\-05\-15  | 
|  New resource  |  September 27, 2017  |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html)  |  2010\-05\-15  | 
| Updated resources | September 27, 2017 |  [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html)  | 2010\-05\-15 | 
| Termination protection added for stacks\. | September 26, 2017 | Enabling termination protection on a stack prevents it from being accidentally deleted\. A user can't delete a stack with termination protection enabled\. For more information, see [Protecting a Stack From Being Deleted](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-protect-stacks.html)\. | 2010\-05\-15 | 
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
|  Transforms  |  November 17, 2016  |  Specify the AWS Serverless Application Model \(AWS SAM\) that AWS CloudFormation uses to process AWS SAM syntax for serverless applications\. For more information, see [Transform](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/transform-section-structure.html)\.  |  2010\-05\-15  | 
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
|  Resource update  |  November 4, 2015  |  For the [AWS::EC2::Volume](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ec2-ebs-volume.html) resource, use the `AutoEnableIO` property to automatically resume I/O operations if a volume's data becomes inconsistent\.  |  2010\-05\-15  | 
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
|  New AWS\-specific parameter types  |  November 6, 2014  |  You can specify AWS\-specific parameter types in your AWS CloudFormation templates\. In the AWS CloudFormation console, these parameter types provide a drop\-down list of valid values\. With the API or AWS CLI, AWS CloudFormation can quickly validate values for these parameter types before creating or updating a stack\. For more information, see [Parameters](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/parameters-section-structure.html)\.  |  2010\-05\-15  | 
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
|  API logging with AWS CloudTrail  |  April 2, 2014  |  You can use AWS CloudTrail \(CloudTrail\) to log AWS CloudFormation requests\. With CloudTrail you can get a history of AWS CloudFormation API calls for your account\. For more information, see [Logging AWS CloudFormation API Calls with AWS CloudTrail](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/cfn-api-logging-cloudtrail.html)\.  |  2010\-05\-15  | 
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
|  Amazon RDS read replica support  |  September 24, 2013  |  You can now create Amazon RDS read replicas from a source DB instance\. For more information, see the `SourceDBInstanceIdentifier` property in the [AWS::RDS::DBInstance](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-rds-database-instance.html) resource\.  |  2010\-05\-15  | 
|  Associate public IP address with instances in an Auto Scaling group  |  September 19, 2013  |  You can now associate public IP addresses with instances in an Auto Scaling group\. For more information, see [AWS::AutoScaling::LaunchConfiguration](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-as-launchconfig.html)\.  |  2010\-05\-15  | 
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
|  New and updated documentation  |  August 27, 2012  |  Topics have been reorganized to more clearly provide specific information about using the AWS Management Console and using the AWS CloudFormation command line interface \(CLI\)\. Information about tagging AWS CloudFormation stacks has been added, including new guides and updated reference topics: [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html) New information about [working with Windows stacks](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/cfn-windows-stacks.html): [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html) New topic: [Using Regular Expressions in AWS CloudFormation Templates](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/cfn-regexes.html)\.  |  2010\-05\-15  | 
|  New feature  |  April 25, 2012  |  AWS CloudFormation now provides full support for Virtual Private Cloud \(VPC\) security with Amazon EC2\. You can now create and populate an entire VPC with every type of VPC resource \(subnets, gateways, network ACLs, route tables, and so forth\) using a single AWS CloudFormation template\.  Documentation for the following resource types has been updated: [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html) New resource types have been added to the documentation: [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html)  |  2010\-05\-15  | 
|  New feature  |  April 13, 2012  |  AWS CloudFormation now allows you to add or remove elements from a stack when updating it\. [AWS CloudFormation Stacks Updates](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks.html) has been updated, and a new section has been added to the walkthrough: [Change the Stack's Resources](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/updating.stacks.walkthrough.html#update.walkthrough.change.resources), which describes how to add and remove resources when updating the stack\.  |  2010\-05\-15  | 
|  New feature  |  February 2, 2012  |  AWS CloudFormation now provides support for resources in an existing Amazon Virtual Private Cloud \(Amazon VPC\)\. With this release, you can: [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html)  |  2010\-05\-15  | 
|  New feature  |  February 2, 2012  |  You can now update properties for the following resources in an existing stack: [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html) For a complete list of updatable resources and details about what to consider when updating a stack, see [AWS CloudFormation Stacks Updates](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks.html)\.  |  2010\-05\-15  | 
|  Restructured guide  |  February 2, 2012  |  Reorganized existing sections into new sections: [Working with AWS CloudFormation Templates](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/template-guide.html) and **Managing Stacks**\. Moved [Template Reference](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/template-reference.html) to the top level of the Table of Contents\. Moved [Estimating the Cost of Your AWS CloudFormation Stack](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-paying.html) to the Getting Started section\.  |  2010\-05\-15  | 
|  New content  |  February 2, 2012  |  Added three new sections: [\[See the AWS documentation website for more details\]](http://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/ReleaseHistory.html)  |  2010\-05\-15  | 
|  New feature  |  May 26, 2011  |  AWS CloudFormation now provides the `aws cloudformation list-stacks` command, which enables you to list stacks filtered by stack status\. Deleted stacks can be listed for up to 90 days after they have been deleted\.  For more information, see [Describing and Listing Your Stacks](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-describing-stacks.html)\.  |  2010\-05\-15  | 
|  New features  |  May 26, 2011  |  The `aws cloudformation describe-stack-resources` and `aws cloudformation get-template` commands now enable you to get information from stacks that have been deleted for 90 days after they have been deleted\.  For more information, see [Listing Resources](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-listing-stack-resources.html) and [Retrieving a Template](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-get-template.html)\.  |  2010\-05\-15  | 
|  New link  |  March 1, 2011  |  AWS CloudFormation endpoint information is now located in the AWS General Reference\. For more information, go to Regions and Endpoints in [Amazon Web Services General Reference](http://docs.aws.amazon.com/general/latest/gr/index.html?rande.html)\.  |  2010\-05\-15  | 
|  Initial release  |  February 25, 2011  |  The initial public release of AWS CloudFormation\.  |  2010\-05\-15  | 