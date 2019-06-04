# `Ref`<a name="intrinsic-function-reference-ref"></a>

The intrinsic function `Ref` returns the value of the specified *parameter* or *resource*\.
+ When you specify a parameter's logical name, it returns the value of the parameter\.
+ When you specify a resource's logical name, it returns a value that you can typically use to refer to that resource, such as a [physical ID](resources-section-structure.md)\.

When you are declaring a resource in a template and you need to specify another template resource by name, you can use the `Ref` to refer to that other resource\. In general, `Ref` returns the name of the resource\. For example, a reference to an [AWS::AutoScaling::AutoScalingGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-as-group.html) returns the name of that Auto Scaling group resource\.

For some resources, an identifier is returned that has another significant meaning in the context of the resource\. An [AWS::EC2::EIP](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ec2-eip.html) resource, for instance, returns the IP address, and an [AWS::EC2::Instance](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ec2-instance.html) returns the instance ID\. 

At the bottom of this topic, there is a table that lists the values returned for many common resource types\. More information about `Ref` return values for a particular resource or property can be found in the documentation for that resource or property\.

**Tip**  
You can also use `Ref` to add values to Output messages\.

## Declaration<a name="ref-declaration"></a>

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

## Parameters<a name="ref-parameters"></a>

logicalName  
The logical name of the resource or parameter you want to dereference\.

## Return Value<a name="ref-return-value"></a>

The physical ID of the resource or the value of the parameter\.

## Example<a name="ref-example"></a>

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

## Supported Functions<a name="ref-supported-functions"></a>

You cannot use any functions in the `Ref` function\. You must specify a string that is a resource logical ID\.

## Resource Return Examples<a name="ref-resource-return-examples"></a>

This section lists sample values returned by `Ref` for particular AWS CloudFormation resources\. For more information about `Ref` return values for a particular resource or property, refer to the documentation for that resource or property\.


| Resource Type | Reference Value | Example Return Value | 
| --- | --- | --- | 
| [Alexa::ASK::Skill](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ask-skill.html) | Alexa skill ID | amzn1\.ask\.skill\.a3103cee\-c48c\-40a0\-a2c9\-251141888863 | 
| [AWS::AmazonMQ::Broker](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-amazonmq-broker.html) | Amazon MQ broker ID | b\-1234a5b6\-78cd\-901e\-2fgh\-3i45j6k178l9 | 
| [AWS::AmazonMQ::Configuration](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-amazonmq-configuration.html) | Amazon MQ configuration ID | c\-1234a5b6\-78cd\-901e\-2fgh\-3i45j6k178l9 | 
| [AWS::AmazonMQ::ConfigurationAssociation](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-amazonmq-configurationassociation.html) | Amazon MQ configurationassociation ID | c\-1234a5b6\-78cd\-901e\-2fgh\-3i45j6k178l9 | 
|  [AWS::ApiGateway::Account](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-apigateway-account.html)  |  API Gateway account resource ID  |  `mysta-accou-01234b567890example`  | 
|  [AWS::ApiGateway::ApiKey](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-apigateway-apikey.html)  |  API key  |  `m2m1k7sybf`  | 
|  [AWS::ApiGateway::Authorizer](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-apigateway-authorizer.html)  |  Authorizer resource ID  |  `abcde1`  | 
|  [AWS::ApiGateway::ClientCertificate](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-apigateway-clientcertificate.html)  |  Client certificate name  |  `abc123`  | 
|  [AWS::ApiGateway::Deployment](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-apigateway-deployment.html)  |  Deployment resource ID  |  `abc123`  | 
|  [AWS::ApiGateway::DocumentationPart](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-apigateway-documentationpart.html)  |  Documentation part ID  |  `abc123`  | 
|  [AWS::ApiGateway::DomainName](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-apigateway-domainname.html)  |  Domain name  |  `example.mydomain.com`  | 
|  [AWS::ApiGateway::Method](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-apigateway-method.html)  |  Method resource ID  |  `mysta-metho-01234b567890example`  | 
|  [AWS::ApiGateway::Model](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-apigateway-model.html)  |  Model name  |  `myModel`  | 
|  [AWS::ApiGateway::RequestValidator](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-apigateway-requestvalidator.html)  |  Request validator ID  |  `abc123`  | 
|  [AWS::ApiGateway::Resource](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-apigateway-resource.html)  |  API Gateway resource ID  |  `abc123`  | 
|  [AWS::ApiGateway::RestApi](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-apigateway-restapi.html)  |  Rest API resource ID  |  `a1bcdef2gh`  | 
|  [AWS::ApiGateway::Stage](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-apigateway-stage.html)   |  Stage name  |  `MyTestStage`  | 
|  [AWS::ApiGateway::VpcLink](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-apigateway-vpclink.html)  |  VPC link ID  |  `gim7c3`   | 
|  [AWS::ApiGatewayV2::Api](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-apigatewayv2-api.html)  |  API resource ID  |  `a1bcdef2gh`  | 
|  [AWS::ApiGatewayV2::ApiMapping](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-apigatewayv2-apimapping.html)  |  API mapping resource ID  |  `abc123`  | 
|  [AWS::ApiGatewayV2::Authorizer](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-apigatewayv2-authorizer.html)  |  Authorizer resource ID  |  `abc123`  | 
|  [AWS::ApiGatewayV2::Deployment](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-apigatewayv2-deployment.html)  |  Deployment resource ID  |  `abc123`  | 
|  [AWS::ApiGatewayV2::DomainName](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-apigatewayv2-domainname.html)  |  Domain name  |  `example.mydomain.com`  | 
|  [AWS::ApiGatewayV2::Integration](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-apigatewayv2-integration.html)  |  Integration resource ID  |  `abcd123`  | 
|  [AWS::ApiGatewayV2::IntegrationResponse](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-apigatewayv2-integrationresponse.html)  |  Integration response resource ID  |  `abcd123`  | 
|  [AWS::ApiGatewayV2::Model](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-apigatewayv2-model.html)  |  Model resource ID  |  `abc123`  | 
|  [AWS::ApiGatewayV2::Route](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-apigatewayv2-route.html)  |  Route resource ID  |  `abcd123`  | 
|  [AWS::ApiGatewayV2::RouteResponse](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-apigatewayv2-routeresponse.html)  |  Route response resource ID  |  `abc123`  | 
|  [AWS::ApiGatewayV2::Stage](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-apigatewayv2-stage.html)  |  Stage name  |  `MyTestStage`  | 
| [AWS::ApplicationAutoScaling::ScalableTarget](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-applicationautoscaling-scalabletarget.html) |  Scalable Target ID  |  `service/ecsStack-MyECSCluster-AB12CDE3F4GH/ecsStack-MyECSService-AB12CDE3F4GH\|ecs:service:DesiredCount\|ecs`  | 
| [AWS::ApplicationAutoScaling::ScalingPolicy](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-applicationautoscaling-scalingpolicy.html) |  Application Auto Scaling policy Amazon Resource Name \(ARN\)  | arn:aws:autoscaling:us\-east\-1:123456789012:scalingPolicy:12ab3c4d\-56789\-0ef1\-2345\-6ghi7jk8lm90:resource/ecs/service/ecsStack\-MyECSCluster\-AB12CDE3F4GH/ecsStack\-MyECSService\-AB12CDE3F4GH:policyName/MyStepPolicy | 
| [AWS::AppMesh::Mesh](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-appmesh-mesh.html) | Mesh ARN | arn:aws:appmesh:us\-east\-1:555555555555:mesh/myMesh | 
| [AWS::AppMesh::Route](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-appmesh-route.html) | Route ARN | arn:aws:appmesh:us\-east\-1:555555555555:route/myRoute | 
| [AWS::AppMesh::VirtualNode](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-appmesh-virtualnode.html) | Virtual node ARN | arn:aws:appmesh:us\-east\-1:555555555555:virtualNode/myVirtualNode | 
| [AWS::AppMesh::VirtualRouter](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-appmesh-virtualrouter.html) | Virtual router ARN | arn:aws:appmesh:us\-east\-1:555555555555:virtualRouter/myVirtualRouter | 
| [AWS::AppMesh::VirtualService](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-appmesh-virtualservice.html) | Virtual service ARN | arn:aws:appmesh:us\-east\-1:555555555555:virtualService/myVirtualService | 
|  [AWS::AppSync::ApiKey](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-appsync-apikey.html)  |  ARN of the API Key  |  `arn:aws:appsync:us-east-1:123456789012:apis/graphqlapiid/apikey/apikeya1bzhi`  | 
|  [AWS::AppSync::DataSource](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-appsync-datasource.html)  |  ARN of the Data Source  |  `arn:aws:appsync:us-east-1:123456789012:apis/graphqlapiid/datasources/datasourcename`  | 
|  [AWS::AppSync::FunctionConfiguration](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-appsync-functionconfiguration.html)  |  ARN of the FunctionConfiguration  |  `arn:aws:appsync:us-east-1:123456789012:apis/graphqlapiid/functions/functionid`  | 
|  [AWS::AppSync::GraphQLApi](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-appsync-graphqlapi.html)  |  ARN of the GraphQL API  |  `arn:aws:appsync:us-east-1:123456789012:apis/graphqlapiid`  | 
|  [AWS::AppSync::GraphQLSchema](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-appsync-graphqlschema.html)  |  GraphQL API id with the literal String GraphQLSchema attached to it  |   | 
|  [AWS::AppSync::Resolver](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-appsync-resolver.html)  |  ARN of the Resolver  |  `arn:aws:appsync:us-east-1:123456789012:apis/graphqlapiid/types/typename/resolvers/resolvername`  | 
|  [AWS::Athena::NamedQuery](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-athena-namedquery.html)  |  Named query name  |  `abc123`  | 
|  [AWS::AutoScalingPlans::ScalingPlan](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-autoscalingplans-scalingplan.html)  |  Amazon Resource Name \(ARN\) of the scaling plan  |  `arn:aws:autoscaling:region:123456789012:scalingPlan:scalingPlanName/plan-name:scalingPlanVersion/plan-version`  | 
|  [AWS::AutoScaling::AutoScalingGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-as-group.html)  |  Name  |  `mystack-myasgroup-NT5EUXTNTXXD`  | 
|  [AWS::AutoScaling::LaunchConfiguration](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-as-launchconfig.html)  |  Name  |  `mystack-mylaunchconfig-1DDYF1E3B3I`  | 
|  [AWS::AutoScaling::LifecycleHook](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-as-lifecyclehook.html)  |  Name  |  `mylifecyclehookname`  | 
|  [AWS::AutoScaling::ScalingPolicy](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-as-policy.html)  |  Scaling policy Amazon Resource Name \(ARN\)  |  `arn:aws:autoscaling:us-east-1:123456789012:scalingPolicy:ab12c4d5-a1b2-a1b2-a1b2-ab12c4d56789:autoScalingGroupName/myStack-AutoScalingGroup-AB12C4D5E6:policyName/myStack-myScalingPolicy-AB12C4D5E6`  | 
|  [AWS::AutoScaling::ScheduledAction](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-as-scheduledaction.html)  |  Name  |  `mystack-myscheduledaction-NT5EUXTNTXXD`  | 
| [AWS::Backup::BackupPlan](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-backup-backupplan.html) |  `BackupPlanId`  |  `a1b2c3d4-0123-4567-8901-a1b2c3d4e5f6`  | 
| [AWS::Backup::BackupSelection](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-backup-backupselection.html) |  `BackupSelectionId`  |  `a1b2c3d4-0123-4567-8901-a1b2c3d4e5f6`  | 
| [AWS::Backup::BackupVault](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-backup-backupvault.html) |  `BackupVaultName`  |  `Default`  | 
| [AWS::Batch::ComputeEnvironment](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-batch-computeenvironment.html) |  AWS Batch Compute Environment Amazon Resource Name \(ARN\)  |  `arn:aws:batch:us-east-1:555555555555:compute-environment/M4OnDemand`  | 
| [AWS::Batch::JobDefinition](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-batch-jobdefinition.html) |  AWS Batch Job Definition Amazon Resource Name \(ARN\)  |  `arn:aws:batch:us-east-1:111122223333:job-definition/test-gpu:2`  | 
| [AWS::Batch::JobQueue](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-batch-jobqueue.html) |  AWS Batch Job Queue Amazon Resource Name \(ARN\)  |  `arn:aws:batch:us-east-1:111122223333:job-queue/HighPriority`  | 
| [AWS::Budgets::Budget](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-budgets-budget.html) |  Budget name  |  `my-budget`   | 
| [AWS::CertificateManager::Certificate](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-certificatemanager-certificate.html) |  Certificate Amazon Resource Name \(ARN\)  |  `arn:aws:acm:us-east-1:123456789012:certificate/12ab3c4d-56789-0ef1-2345-3dab6fa3ee50`  | 
|  [AWS::Cloud9::EnvironmentEC2](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-cloud9-environmentec2.html)  |  Development environment ID  |  `2bc3642873c342e485f7e0c56example`  | 
|  [AWS::CloudFormation::Stack](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-stack.html)  |  Stack ID  |  `arn:aws:cloudformation:``us-east-2``:803981987763:stack/mystack-mynestedstack-sggfrhxhum7w/f449b250-b969-11e0-a185-5081d0136786`  | 
|  [AWS::CloudFormation::WaitCondition](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-waitcondition.html)  |  Name  |  `arn:aws:cloudformation:``us-east-2``:803981987763:stack/mystack/c325e210-bdf2-11e0-9638-50690880c386/mywaithandle`  | 
|  [AWS::CloudFormation::WaitConditionHandle](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-waitconditionhandle.html)  |  Wait Condition Signal URL  |  `https://cloudformation-waitcondition-``us-east-2``.s3.amazonaws.com/arn%3Aaws%3Acloudformation%3A``us-east-2``%3A803981987763%3Astack%2Fwaittest%2F054a33d0-bdee-11e0-8816-5081c490a786%2FmyWaitHandle?Expires=1312475488&AWSAccessKeyId=AKIAIOSFODNN7EXAMPLE&Signature=tUsrW3WvWVT46K69zMmgbEkwVGo%3D`  | 
|  [AWS::CloudFront::Distribution](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-cloudfront-distribution.html)  |  Distribution ID  |  `E27LVI50CSW06W`  | 
|  [AWS::CloudFront::CloudFrontOriginAccessIdentity](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-cloudfront-cloudfrontoriginaccessidentity.html)  |  Origin access identity  |  `E15MNIMTCFKK4C`  | 
|  [AWS::CloudFront::StreamingDistribution](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-cloudfront-streamingdistribution.html)  |  Streaming distribution ID  |  `E1E7FEN9T35R9W`  | 
|  [AWS::CloudTrail::Trail](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-cloudtrail-trail.html)  |  Trail name  |  `awscloudtrail-example`  | 
|  [AWS::CloudWatch::Alarm](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-cw-alarm.html)  |  Name  |  `mystack-myalarm-3AOHFRGOXR5T`  | 
|  [AWS::CloudWatch::Dashboard](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-cw-dashboard.html)  |  Name  |   | 
|  [AWS::CodeBuild::Project](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-codebuild-project.html)  |  Project name  |  `myProjectName`  | 
|  [AWS::CodeCommit::Repository](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-codecommit-repository.html)  |  Repository ID  |  `12a345b6-bbb7-4bb6-90b0-8c9577a2d2b9`  | 
| [AWS::CodeDeploy::Application](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-codedeploy-application.html) |  Application name  |  `myapplication-a123d0d1`  | 
| [AWS::CodeDeploy::DeploymentConfig](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-codedeploy-deploymentconfig.html) |  Deployment configuration name  |  `mydeploymentconfig-a123d0d1`  | 
| [AWS::CodeDeploy::DeploymentGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-codedeploy-deploymentgroup.html) |  Deployment group name  |  `mydeploymentgroup-a123d0d1`  | 
| [AWS::CodePipeline::CustomActionType](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-codepipeline-customactiontype.html) |  Custom action name  |  `mysta-MyCus-A1BCDEFGHIJ2`  | 
| [AWS::CodePipeline::Pipeline](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-codepipeline-pipeline.html) |  Pipeline name  |  `mysta-MyPipeline-A1BCDEFGHIJ2`  | 
| [AWS::CodePipeline::Webhook](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-codepipeline-webhook.html) |  Webhook name  |  `MyFirstPipeline-SourceAction1-Webhook-utb9LrOl24Kk`  | 
| [AWS::Cognito::IdentityPool](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-cognito-identitypool.html) |  `IdentityPoolId`  |  `us-east-2:0d01f4d7-1305-4408-b437-12345EXAMPLE`  | 
| [AWS::Cognito::IdentityPoolRoleAttachment](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-cognito-identitypoolroleattachment.html) |  ID  |  `IdentityPoolRoleAttachment-EXAMPLEwnOR3n`  | 
| [AWS::Cognito::UserPool](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-cognito-userpool.html) |  ID  |  `us-east-2_zgaEXAMPLE`  | 
| [AWS::Cognito::UserPoolClient](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-cognito-userpoolclient.html) |  Amazon Cognito user pool client ID  |  `1h57kf5cpq17m0eml12EXAMPLE`  | 
| [AWS::Cognito::UserPoolGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-cognito-userpoolgroup.html) |  Name of the user pool group  |  `Admins`  | 
| [AWS::Cognito::UserPoolUser](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-cognito-userpooluser.html) |  Name of the user  |  `admin`  | 
| [AWS::Cognito::UserPoolUserToGroupAttachment](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-cognito-userpoolusertogroupattachment.html) |  ID  |  `UserToGroupAttachment-YejJvzrEXAMPLE`  | 
| [AWS::Config::AggregationAuthorization](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-config-aggregationauthorization.html) |  ARN of the AggregationAuthorization  |  `arn:aws:config:us-east-1:123456789012:aggregation-authorization/987654321012/us-west-2`  | 
| [AWS::Config::ConfigRule](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-config-configrule.html) |  Configuration rule name  |  `mystack-MyConfigRule-12ABCFPXHV4OV`  | 
| [AWS::Config::ConfigurationAggregator](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-config-configurationaggregator.html) |  `ConfigurationAggregatorName`  |  `myConfigurationAggregator`  | 
| [AWS::Config::ConfigurationRecorder](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-config-configurationrecorder.html) |  Configuration recorder name  |  `default`  | 
| [AWS::Config::DeliveryChannel](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-config-deliverychannel.html) |  Delivery channel name  |  `default`  | 
| [AWS::DataPipeline::Pipeline](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-datapipeline-pipeline.html) |  Pipeline ID  |  `df-sample322HVPGK130TOD`  | 
|  [AWS::DAX::Cluster](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-dax-cluster.html)  |  `Name`  |  `MyDAXCluster`  | 
|  [AWS::DAX::ParameterGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-dax-parametergroup.html)  |  ARN of the created parameter group  |  `my-dax-parameter-group`  | 
|  [AWS::DAX::SubnetGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-dax-subnetgroup.html)  |  ARN of the created activity  |  `my-dax-subnet-group`  | 
| [AWS::DirectoryService::MicrosoftAD](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-directoryservice-microsoftad.html) |  Microsoft directory ID  |  `d-12345ab592`  | 
| [AWS::DirectoryService::SimpleAD](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-directoryservice-simplead.html) |  Directory ID  |  `d-12345ab592`  | 
| [AWS::DLM::LifecyclePolicy](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-dlm-lifecyclepolicy.html) | Policy ID |  `policy-0123456789abcdef0`  | 
| [AWS::DMS::Certificate](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-dms-certificate.html) |  Amazon Resource Name \(ARN\) of the certificate  |   | 
| [AWS::DMS::Endpoint](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-dms-endpoint.html) |  ARN of the endpoint  |   | 
| [AWS::DMS::EventSubscription](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-dms-eventsubscription.html) |  Event subscription name  |  `mystack-myEventSubscription-1DDYF1E3B3I`  | 
| [AWS::DMS::ReplicationInstance](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-dms-replicationinstance.html) |  Replication instance ARN  |   | 
| [AWS::DMS::ReplicationSubnetGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-dms-replicationsubnet-group.html) |  Name of the replication subnet group  |  `mystack-myrepsubnetgroup-0a12bc456789de0fg`  | 
| [AWS::DMS::ReplicationTask](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-dms-replicationtask.html) |  Replication task ARN  |   | 
| [AWS::DocDB::Cluster](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-docdb-dbcluster.html) |  DB cluster name  |  `sample-cluster`  | 
| [AWS::DocDB::DBClusterParameterGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-docdb-dbclusterparametergroup.html) |  DB cluster parameter group name  |  `default.docdb3.6`  | 
| [AWS::DocDB::DBInstance](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-docdb-dbinstance.html) |  DB instance name  |  `sample-instance`  | 
| [AWS::DocDB::DBSubnetGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-docdb-dbsubnetgroup.html) |  DB subnet group name  |  `default`  | 
| [AWS::DynamoDB::Table](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-dynamodb-table.html) |  Table Name  |  `MyDDBTable`  | 
| [AWS::EC2::CapacityReservation](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-capacityreservation.html)  |  Capacity Reservation ID  |  `cr-1234ab5cd6789e0f1`  | 
|  [AWS::EC2::CustomerGateway](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-customer-gateway.html)  |  Name  |   | 
|  [AWS::EC2::DHCPOptions](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-dhcp-options.html)  |  Name  |   | 
|  [AWS::EC2::EC2Fleet](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-ec2fleet.html)  |  Fleet ID  |  `fleet-12a34b55-67cd-8ef9-ba9b-9208dEXAMPLE`  | 
|  [AWS::EC2::EgressOnlyInternetGateway](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-egressonlyinternetgateway.html)  |  ID of the egress\-only Internet gateway  |   | 
|  [AWS::EC2::EIP](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ec2-eip.html)  |  Elastic IP Address  |  `192.0.2.0`  | 
|  [AWS::EC2::EPIAssociation](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ec2-eip-association.html)  |  Name  |  `mystack-myeipa-1NU3IL8LJ313N`  | 
|  [AWS::EC2::FlowLog](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-flowlog.html)  |  Flow log ID  |  `fl-1a23b456`  | 
|  [AWS::EC2::Host](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-host.html)  |  Host ID  |  `h-0ab123c45d67ef89`  | 
|  [AWS::EC2::Instance](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ec2-instance.html)  |  Instance ID  |  `i-1234567890abcdef0`  | 
|  [AWS::EC2::InternetGateway](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-internetgateway.html)  |  Name  |   | 
|  [AWS::EC2::LaunchTemplate](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-launchtemplate.html)  |  Launch template ID  |  `lt-01238c059e3466abc`  | 
|  [AWS::EC2::NatGateway](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-natgateway.html)  |  NAT gateway ID  |  `nat-0a12bc456789de0fg`  | 
|  [AWS::EC2::NetworkAcl](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-network-acl.html)  |  Name  |   | 
|  [AWS::EC2::NetworkAclEntry](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-network-acl-entry.html)  |  Name  |   | 
|  [AWS::EC2::NetworkInterface](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-network-interface.html)  |  Name  |   | 
|  [AWS::EC2::NetworkInterfaceAttachment](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-network-interface-attachment.html)  |  Name  |   | 
|  [AWS::EC2::NetworkInterfacePermission](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-networkinterfacepermission.html)  |  Network interface permission ID  |  `eni-perm-055663b682ea24b48`  | 
|  [AWS::EC2::PlacementGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-placementgroup.html)  |  Placement group name  |  `mystack-myplacementgroup-CU6107MRVLR7`  | 
|  [AWS::EC2::Route](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-route.html)  |  Name  |   | 
|  [AWS::EC2::RouteTable](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-route-table.html)  |  Route table ID  | rtb\-12a34567 | 
|  [AWS::EC2::SecurityGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ec2-security-group.html)  |  Name or security group ID \(for VPC security groups that are not in a default VPC\)  |  `mystack-mysecuritygroup-QQB406M8FISX or sg-94b3a1f6`  | 
|  [AWS::EC2::SecurityGroupEgress](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-security-group-egress.html)  |  Name  |  `mysecuritygroupegress`  | 
|  [AWS::EC2::SecurityGroupIngress](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ec2-security-group-ingress.html)  |  Name  |  `mysecuritygroupingress`  | 
|  [AWS::EC2::SpotFleet](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-spotfleet.html)  |  Name  |  `sfr-73fbd2ce-aa30-494c-8788-1cee4EXAMPLE`  | 
|  [AWS::EC2::Subnet](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-subnet.html)  |  Subnet ID  |  `subnet-e19f0178`  | 
|  [AWS::EC2::SubnetNetworkAclAssociation](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-subnet-network-acl-assoc.html)  |  Name  |   | 
|  [AWS::EC2::SubnetRouteTableAssociation](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-subnet-route-table-assoc.html)  |  Name  |   | 
|  [AWS::EC2::TransitGateway](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-transitgateway.html)  |  Transit gateway ID  |  `tgw-1234567891234567`  | 
|  [AWS::EC2::TransitGatewayAttachment](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-transitgatewayattachment.html)  |  Attachment ID  |  `tgw-attach-vpc-0d39e0d39e0d39e`  | 
|  [AWS::EC2::TransitGatewayRoute](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-transitgatewayroute.html)  |  ID of the route table and destination CIDR, separated by an underscore  |  `tgw-rtb-0ea209e5dcc99f3a3_0.0.0.0/0`  | 
|  [AWS::EC2::TransitGatewayRouteTable](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-transitgatewayroutetable.html)  |  ID of the transit gateway route table  |  `tgw-rtb-020b99a6568edc33a`  | 
|  [AWS::EC2::TransitGatewayRouteTableAssociation](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-transitgatewayroutetableassociation.html)  |  ID of the attachment and ID of the transit gateway route table, separated by an underscore  |  `tgw-attach-0bbfdd70ef7d35f5d_tgw-rtb-020b99a6568edc33a`  | 
|  [AWS::EC2::TransitGatewayRouteTablePropagation](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-transitgatewayroutetablepropagation.html)  |  ID of the attachment and ID of the propagation route table, separated by an underscore  |  `tgw-attach-0bbfdd70ef7d35f5d_tgw-rtb-020b99a6568edc33a`  | 
|  [AWS::EC2::Volume](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ec2-ebs-volume.html)  |  Volume ID  |  `vol-3cdd3f56`  | 
|  [AWS::EC2::VolumeAttachment](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ec2-ebs-volumeattachment.html)  |  Name  |  `mystack-myvola-ERXHJITXMRLT`  | 
|  [AWS::EC2::VPC](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-vpc.html)  |  VPC ID  |  `vpc-18ac277d`  | 
|  [AWS::EC2::VPCDHCPOptionsAssociation](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-vpc-dhcp-options-assoc.html)  |  Name  |   | 
|  [AWS::EC2::VPCEndpoint](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-vpcendpoint.html)  |  Endpoint ID  |  `vpce-a123d0d1`  | 
|  [AWS::EC2::VPCEndpointConnectionNotification](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-vpcendpointconnectionnotification.html)  |  ID of the connection notification  |   | 
|  [AWS::EC2::VPCEndpointService](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-vpcendpointservice.html)  |  ID of the VPC endpoint service configuration  |   | 
|  [AWS::EC2::VPCEndpointServicePermissions](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-vpcendpointservicepermissions.html)  |  ID of the VPC endpoint service  |   | 
|  [AWS::EC2::VPCGatewayAttachment](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-vpc-gateway-attachment.html)  |  Name  |   | 
| [AWS::EC2::VPCPeeringConnection](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-vpcpeeringconnection.html) |  VPC peering connection ID  |  `pcx-75de3e1d`  | 
|  [AWS::EC2::VPNConnection](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-vpn-connection.html)  |  Name  |   | 
|  [AWS::EC2::VPNConnectionRoute](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-vpn-connection-route.html)  |  Name  |   | 
|  [AWS::EC2::VPNGateway](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-vpn-gateway.html)  |  Name  |   | 
|  [AWS::EC2::VPNGatewayRoutePropagation](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ec2-vpn-gatewayrouteprop.html)  |  Name  |   | 
|  [AWS::ECR::Repository](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ecr-repository.html)  |  Repository name  |  `test-repository`  | 
|  [AWS::ECS::Cluster](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ecs-cluster.html)  |  Name  |  `MyStack-MyECSCluster-NT5EUXTNTXXD`  | 
|  [AWS::ECS::Service](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ecs-service.html)  |  Service ARN  |  `arn:aws:ecs:us-west-2:123456789012:service/sample-webapp`  | 
|  [AWS::ECS::TaskDefinition](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ecs-taskdefinition.html)  |  Task definition ARN  |  `arn:aws:ecs:us-west-2:123456789012:task-definition/TaskDefinitionFamily:1`  | 
|  [AWS::EFS::FileSystem](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-efs-filesystem.html)  |  File system ID  |  `fs-47a2c22e`  | 
|  [AWS::EFS::MountTarget](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-efs-mounttarget.html)  |  Mount target ID  |  `fsmt-55a4413c`  | 
|  [AWS::EKS::Cluster](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-eks-cluster.html)  |  Cluster name  |  `EKSCluster-NT5EUXTNTXXD`  | 
|  [AWS::ElastiCache::CacheCluster](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-elasticache-cache-cluster.html)  |  Name  |   | 
|  [AWS::ElastiCache::ParameterGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-elasticache-parameter-group.html)  |  Name  |   | 
|  [AWS::ElastiCache::ReplicationGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-elasticache-replicationgroup.html)  |  Name  |  `abc12xmy3d1w3hv6`  | 
|  [AWS::ElastiCache::SecurityGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-elasticache-security-group.html)   |  `CacheSecurityGroupName`  |   | 
|  [AWS::ElastiCache::SubnetGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-elasticache-subnetgroup.html)  |  Name  |  `myCachesubnetgroup`  | 
|  [AWS::Elasticsearch::Domain](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-elasticsearch-domain.html)  |  Domain name  |  `mystack-elasticsea-abc1d2efg3h4`  | 
|  [AWS::ElasticBeanstalk::Application](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-beanstalk.html)  |  Name  |  `mystack-myapplication-FM6BIXY7U8PK`  | 
|  [AWS::ElasticBeanstalk::ApplicationVersion](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-beanstalk-version.html)  |  Name  |  `mystack-myapplicationversion-iy8ptveuxjly`  | 
|  [AWS::ElasticBeanstalk::ConfigurationTemplate](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-beanstalk-configurationtemplate.html)  |  Name  |  `mystack-myconfigurationtemplate-108RPH64J195`  | 
|  [AWS::ElasticBeanstalk::Environment](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-beanstalk-environment.html)  |  Name  |  `mystack-myenv-LKGNQSFHO1DB`  | 
|  [AWS::ElasticLoadBalancing::LoadBalancer](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-ec2-elb.html)  |  Name  |  `mystack-myelb-1WQN7BJGDB5YQ`  | 
|  [AWS::ElasticLoadBalancingV2::Listener](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-elasticloadbalancingv2-listener.html)  |  Listener's Amazon Resource Name \(ARN\)  |  `arn:aws:elasticloadbalancing:us-west-2:123456789012:listener/app/my-load-balancer/50dc6c495c0c9188/f2f7dc8efc522ab2`  | 
|  [AWS::ElasticLoadBalancingV2::ListenerRule](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-elasticloadbalancingv2-listener.html)  |  Listener rule's Amazon Resource Name \(ARN\)  |  `arn:aws:elasticloadbalancing:us-west-2:123456789012:listener-rule/app/my-load-balancer/50dc6c495c0c9188/f2f7dc8efc522ab2/9683b2d02a6cabee`  | 
|  [AWS::ElasticLoadBalancingV2::LoadBalancer](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-elasticloadbalancingv2-loadbalancer.html)  |  Application load balancer's Amazon Resource Name \(ARN\)  |  `arn:aws:elasticloadbalancing:us-west-2:123456789012:loadbalancer/app/my-internal-load-balancer/50dc6c495c0c9188`  | 
|  [AWS::ElasticLoadBalancingV2::TargetGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-elasticloadbalancingv2-targetgroup.html)  |  Target group's Amazon Resource Name \(ARN\)  |  `arn:aws:elasticloadbalancing:us-west-2:123456789012:targetgroup/my-targets/73e2d6bc24d8a067`  | 
|  [AWS::EMR::Cluster](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-emr-cluster.html)  |  Cluster ID  |  `j-1ABCD123AB1A`  | 
|  [AWS::EMR::InstanceGroupConfig](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-emr-instancegroupconfig.html)  |  Instance group ID  |  `ig-ABC12DEF3456`  | 
|  [AWS::EMR::SecurityConfiguration](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-emr-securityconfiguration.html)  |  Name  |  `mySecurityConfiguration`  | 
|  [AWS::EMR::Step](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-emr-step.html)  |  Step ID  |  `s-1A2BC3D4EFG56`  | 
|  [AWS::Events::EventBusPolicy](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-events-eventbuspolicy.html)  |  Event bus policy ID  |  `EventBusPolicy-1aBCdeFGh2J3`  | 
|  [AWS::Events::Rule](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-events-rule.html)  |  Event rule ID  |  `mystack-ScheduledRule-ABCDEFGHIJK`  | 
|  [AWS::FSx::FileSystem](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-fsx-filesystem.html)  |  File system resource ID  |  `fs-0d33333e999a7c66g`  | 
|  [AWS::GameLift::Alias](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-gamelift-alias.html)  |  Alias ID  |  `myalias-a01234b56-7890-1de2-f345-g67h8i901j2k`  | 
|  [AWS::GameLift::Build](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-gamelift-build.html)  |  Build ID  |  `mybuild-a01234b56-7890-1de2-f345-g67h8i901j2k`  | 
|  [AWS::GameLift::Fleet](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-gamelift-fleet.html)  |  Fleet ID  |  `myfleet-a01234b56-7890-1de2-f345-g67h8i901j2k`  | 
|  [AWS::Glue::Classifier](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-glue-classifier.html)  |  Name  |  `abc123`  | 
|  [AWS::Glue::Connection](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-glue-connection.html)  |  `ConnectionInput` name  |  `abc123`  | 
|  [AWS::Glue::Crawler](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-glue-crawler.html)  |  Name  |  `abc123`  | 
|  [AWS::Glue::Database](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-glue-database.html)  |  `DatabaseInput` name  |  `abc123`  | 
|  [AWS::Glue::Job](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-glue-job.html)  |  Name  |  `abc123`  | 
|  [AWS::Glue::SecurityConfiguration](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-glue-securityconfiguration.html)  |  Name  |   | 
|  [AWS::Glue::Table](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-glue-table.html)  |  `TableInput` name  |  `abc123`  | 
|  [AWS::Glue::Trigger](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-glue-trigger.html)  |  Name  |  `abc123`  | 
|  [AWS::Greengrass::ConnectorDefinition](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-greengrass-connectordefinition.html)  |  ID  |  `1234a5b6-78cd-901e-2fgh-3i45j6k178l9`  | 
|  [AWS::Greengrass::ConnectorDefinitionVersion](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-greengrass-connectordefinitionversion.html)  |  ARN  |  `arn:aws:greengrass:us-east-1:123456789012:/greengrass/definition/connectors/1234a5b6-78cd-901e-2fgh-3i45j6k178l9/versions/9876ac30-4bdb-4f9d-95af-b5fdb66be1a2`  | 
|  [AWS::Greengrass::CoreDefinition](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-greengrass-coredefinition.html)  |  ID  |  `1234a5b6-78cd-901e-2fgh-3i45j6k178l9`  | 
|  [AWS::Greengrass::CoreDefinitionVersion](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-greengrass-coredefinitionversion.html)  |  ARN  |  `arn:aws:greengrass:us-east-1:123456789012:/greengrass/definition/cores/1234a5b6-78cd-901e-2fgh-3i45j6k178l9/versions/9876ac30-4bdb-4f9d-95af-b5fdb66be1a2`  | 
|  [AWS::Greengrass::DeviceDefinition](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-greengrass-devicedefinition.html)  |  ID  |  `1234a5b6-78cd-901e-2fgh-3i45j6k178l9`  | 
|  [AWS::Greengrass::DeviceDefinitionVersion](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-greengrass-devicedefinitionversion.html)  |  ARN  |  `arn:aws:greengrass:us-east-1:123456789012:/greengrass/definition/devices/1234a5b6-78cd-901e-2fgh-3i45j6k178l9/versions/9876ac30-4bdb-4f9d-95af-b5fdb66be1a2`  | 
|  [AWS::Greengrass::FunctionDefinition](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-greengrass-functiondefinition.html)  |  ID  |  `1234a5b6-78cd-901e-2fgh-3i45j6k178l9`  | 
|  [AWS::Greengrass::FunctionDefinitionVersion](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-greengrass-functiondefinitionversion.html)  |  ARN  |  `arn:aws:greengrass:us-east-1:123456789012:/greengrass/definition/functions/1234a5b6-78cd-901e-2fgh-3i45j6k178l9/versions/9876ac30-4bdb-4f9d-95af-b5fdb66be1a2`  | 
|  [AWS::Greengrass::Group](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-greengrass-group.html)  |  ID  |  `1234a5b6-78cd-901e-2fgh-3i45j6k178l9`  | 
|  [AWS::Greengrass::GroupVersion](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-greengrass-groupversion.html)  |  ARN  |  `arn:aws:greengrass:us-east-1:123456789012:/greengrass/definition/groups/1234a5b6-78cd-901e-2fgh-3i45j6k178l9/versions/9876ac30-4bdb-4f9d-95af-b5fdb66be1a2`  | 
|  [AWS::Greengras::LoggerDefinition](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-greengrass-loggerdefinition.html)  |  ID  |  `1234a5b6-78cd-901e-2fgh-3i45j6k178l9`  | 
|  [AWS::Greengrass::LoggerDefinitionVersion](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-greengrass-loggerdefinitionversion.html)  |  ARN  |  `arn:aws:greengrass:us-east-1:123456789012:/greengrass/definition/loggers/1234a5b6-78cd-901e-2fgh-3i45j6k178l9/versions/9876ac30-4bdb-4f9d-95af-b5fdb66be1a2`  | 
|  [AWS::Greengrass::ResourceDefinition](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-greengrass-resourcedefinition.html)  |  ID  |  `1234a5b6-78cd-901e-2fgh-3i45j6k178l9`  | 
|  [AWS::Greengrass::ResourceDefinitionVersion](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-greengrass-resourcedefinitionversion.html)  |  ARN  |  `arn:aws:greengrass:us-east-1:123456789012:/greengrass/definition/resources/1234a5b6-78cd-901e-2fgh-3i45j6k178l9/versions/9876ac30-4bdb-4f9d-95af-b5fdb66be1a2`  | 
|  [AWS::Greengrass::SubscriptionDefinition](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-greengrass-subscriptiondefinition.html)  |  ID  |  `1234a5b6-78cd-901e-2fgh-3i45j6k178l9`  | 
|  [AWS::Greengrass::SubscriptionDefinitionVersion](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-greengrass-subscriptiondefinitionversion.html)  |  ARN  |  `arn:aws:greengrass:us-east-1:123456789012:/greengrass/definition/subscriptions/1234a5b6-78cd-901e-2fgh-3i45j6k178l9/versions/9876ac30-4bdb-4f9d-95af-b5fdb66be1a2`  | 
|  [AWS::GuardDuty::Detector](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-guardduty-detector.html)  |  Detector ID  |  `12abc34d567e8fa901bc2d34e56789f0`  | 
|  [AWS::GuardDuty::Filter](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-guardduty-filter.html)  |  Name  |  `SampleFilter`  | 
|  [AWS::GuardDuty::IPSet](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-guardduty-ipset.html)  |  IPSet ID  |  `0cb0141ab9fbde177613ab9436212e90`  | 
|  [AWS::GuardDuty::Master](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-guardduty-master.html)  |  Master ID  |  `012345678901`  | 
|  [AWS::GuardDuty::Member](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-guardduty-member.html)  |  Member ID  |  `012345678901`  | 
|  [AWS::GuardDuty::ThreatIntelSet](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-guardduty-threatintelset.html)  |  ThreatIntel Set ID  |  `12a34567890bc1de2345f67ab8901234`  | 
|  [AWS::IAM::AccessKey](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-iam-accesskey.html)  |  AccessKeyId  |  `AKIAIOSFODNN7EXAMPLE`  | 
|  [AWS::IAM::Group](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-iam-group.html)  |  Group name  |  `mystack-mygroup-1DZETITOWEKVO`  | 
|  [AWS::IAM::InstanceProfile](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-iam-instanceprofile.html)  |  Name  |   | 
|  [AWS::IAM::ManagedPolicy](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-iam-managedpolicy.html)  |  Policy ARN  |  `arn:aws:iam::123456789012:policy/teststack-CreateTestDBPolicy-16M23YE3CS700`  | 
|  [AWS::IAM::Policy](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-iam-policy.html)  |  Name  |   | 
|  [AWS::IAM::Role](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-iam-role.html)  |  Name  |  `MyRole`  | 
|  [AWS::IAM::User](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-iam-user.html)  |  User name  |  `mystack-myuser-1CCXAFG2H2U4D`  | 
|  [AWS::IAM::UserToGroupAddition](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-iam-addusertogroup.html)  |  Name  |   | 
| [AWS::IoT::Certificate](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-iot-certificate.html) | Certificate ID | a1234567b89c012d3e4fg567hij8k9l01mno1p23q45678901rs234567890t1u2 | 
| [AWS::IoT::Policy](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-iot-policy.html) | Policy name | MyPolicyName | 
| [AWS::IoT::Thing](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-iot-thing.html) | Thing name | MyStack\-MyThing\-AB1CDEFGHIJK | 
| [AWS::IoT::TopicRule](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-iot-topicrule.html) | Topic rule name | MyStackMyTopicRule12ABC3D456EFG | 
| [AWS::IoT1Click::Device](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-iot1click-device.html) | The device ARN | arn:aws:iot1click:us\-west\-2:123456789012:devices/G030PX0312744DWM | 
| [AWS::IoT1Click::Placement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-iot1click-placement.html) | The placement name \(associated with a project\) | region3 | 
| [AWS::IoT1Click::Project](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-iot1click-project.html) | The project ARN | arn:aws:iot1click:us\-west\-2:0123456789012:projects/seattle\-region | 
|  [AWS::Kinesis::Stream](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-kinesis-stream.html)  |  Name  |  `mystack-mystream-1NAOH4L1RIQ7I`  | 
|  [AWS::Kinesis::StreamConsumer](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-kinesis-streamconsumer.html)  |  Consumer ARN  |  `arn:aws:kinesis:region:account-id:stream/stream-name/consumer/consumer-name:consumer-creation-timestamp`  | 
|  [AWS::KinesisFirehose::DeliveryStream](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-kinesisfirehose-deliverystream.html)  |  Delivery stream name  |  `mystack-deliverystream-1ABCD2EF3GHIJ`  | 
|  [AWS::KMS::Alias](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-kms-alias.html)  |  Alias name  |  `alias/myAlias`  | 
|  [AWS::KMS::Key](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-kms-key.html)  |  Key ID  |  `123ab456-a4c2-44cb-95fd-b781f32fbb37`  | 
|  [AWS::Lambda::Alias](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-lambda-alias.html)  |  Amazon Resource Name of the AWS Lambda alias  | arn:aws:lambda:us\-west\-2:123456789012:function:helloworld:BETA | 
|  [AWS::Lambda::EventSourceMapping](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-lambda-eventsourcemapping.html)  |  Name  |  `MyStack-lambdaeventsourcemapping-CU6107MRVLR7`  | 
|  [AWS::Lambda::Function](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-lambda-function.html)  |  Name  |  `MyStack-AMILookUp-NT5EUXTNTXXD`  | 
|  [AWS::Lambda::LayerVersion](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-lambda-layerversion.html)  |  Layer version ARN  |  `arn:aws:lambda:us-west-2:123456789012:layer:my-layer:1`  | 
|  [AWS::Lambda::LayerVersionPermission](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-lambda-layerversionpermission.html)  |  Layer version ARN with statement ID  |  `arn:aws:lambda:us-west-2:123456789012:layer:my-layer:1#engineering-org`  | 
|  [AWS::Lambda::Version](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-lambda-version.html)  |  Amazon Resource Name of the AWS Lambda version  | arn:aws:lambda:us\-west\-2:123456789012:function:helloworld:1 | 
|  [AWS::Logs::Destination](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-logs-destination.html)  |  Destination name  |  `TestDestination`  | 
|  [AWS::Logs::LogGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-logs-loggroup.html)  |  Name  |  `mystack-myLogGroup-1341JS4M96031`  | 
|  [AWS::Logs::LogStream](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-logs-logstream.html)  |  Log stream name  |  `MyAppLogStream`  | 
|  [AWS::Logs::SubscriptionFilter](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-logs-subscriptionfilter.html)  |  Subscription filter name  |   | 
|  [AWS::MediaStore::Container](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-mediastore-container.html)  |  Container name  |   | 
|  [AWS::Neptune::DBCluster](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-neptune-dbcluster.html)  |  Name  |   | 
|  [AWS::Neptune::DBClusterParameterGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-neptune-dbclusterparametergroup.html)  |  Name  |   | 
|  [AWS::Neptune::DBInstance](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-neptune-dbinstance.html)  |  `DBInstanceIdentifier`  |  `mystack-mydb-ea5ugmfvuaxg`  | 
|  [AWS::Neptune::DBParameterGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-neptune-dbparametergroup.html)  |  Name  |   | 
|  [AWS::Neptune::DBSubnetGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-neptune-dbsubnetgroup.html)  |  Name  |  `mystack-mydbsubnetgroup-0a12bc456789de0fg`  | 
|  [AWS::OpsWorks::App](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-opsworks-app.html)  |  AWS OpsWorks Application ID  |  `4fee5b96-0d10-4af1-bcc5-25f92e3c6acf`  | 
|  [AWS::OpsWorks::Instance](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-opsworks-instance.html)  |  AWS OpsWorks Instance ID  |  `aa2e9ae2-2b4b-491c-aeb6-8bf3ce9400fe`  | 
|  [AWS::OpsWorks::Layer](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-opsworks-layer.html)  |  AWS OpsWorks Layer ID  |  `730b238b-f7c4-461d-b7c0-3feb7ef1152a`  | 
|  [AWS::OpsWorks::Stack](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-opsworks-stack.html)  |  AWS OpsWorks Stack ID  |  `5c9f04e8-370e-4bd3-ae09-a4bbcc2998bb`  | 
|  [AWS::OpsWorks::UserProfile](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-opsworks-userprofile.html)  |  IAM user Amazon Resource Name  |  `arn:aws:iam::123456789012:user/opsworksuser`  | 
|  [AWS::OpsWorks::Volume](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-opsworks-volume.html)  |  AWS OpsWorks Volume ID  |  `1ab23cd4-92ff-4501-b37c-example`  | 
|  [AWS::OpsWorksCM::Server](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-opsworkscm-server.html)  |  AWS OpsWorks CM server Amazon Resource Name  |  `arn:aws:OpsWorksCM:us-east-1:123456789012:server/server-a1bzhi`  | 
|  [AWS::PinpointEmail::ConfigurationSet](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-pinpointemail-configurationset.html)  |  The name of an Amazon Pinpoint Email API configuration set  |  `myConfigurationSet`  | 
|  [AWS::PinpointEmail::ConfigurationSetEventDestination](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-pinpointemail-configurationseteventdestination.html)  |  The name of an event destination in an Amazon Pinpoint Email API configuration set  |  `myConfigurationSetEventDestination`  | 
|  [AWS::PinpointEmail::DedicatedIpPool](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-pinpointemail-dedicatedippool.html)  |  The name of a dedicated IP pool used to send email through the Amazon Pinpoint Email API  |  `myIpPool`  | 
|  [AWS::PinpointEmail::Identity](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-pinpointemail-dedicatedippool.html)  |  The name \(email address or domain name\) of an identity used to send email by using the Amazon Pinpoint Email API\.  |  `sender@example.com`  | 
|  [AWS::RAM::ResourceShare](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ram-resourceshare.html)  |  Resource share ARN  |  `arn:aws:ram:us-east-1:123456789012:resource-share/12345678-1234-1234-1234-12345678`  | 
|  [AWS::RDS::DBCluster](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-rds-dbcluster.html)  |  Cluster name  |  `test-rdscluster-pdedtss0mfqr`  | 
|  [AWS::RDS::DBClusterParameterGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-rds-dbclusterparametergroup.html)  |  Parameter group name  |  `test-dbparamgroup-4l8qqx46vjby`  | 
|  [AWS::RDS::DBInstance](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-rds-database-instance.html)  |  Name  |  `mystack-mydb-ea5ugmfvuaxg`  | 
|  [AWS::RDS::DBParameterGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-rds-dbparametergroup.html)  |  Name  |   | 
|  [AWS::RDS::DBSecurityGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-rds-security-group.html)  |  Name  |  `mystack-mydbsecuritygroup-1k5u5dxjb0nxs`  | 
|  [AWS::RDS::DBSecurityGroupIngress](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-rds-security-group-ingress.html)  |  Name  |   | 
|  [AWS::RDS::DBSubnetGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-rds-dbsubnet-group.html)  |  DB subnet group name  |  `mystack-mydbsubnetgroup-1k5u5dxjb0nxs`  | 
|  [AWS::RDS::EventSubscription](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-rds-eventsubscription.html)  |  Name  |  `mystack-myEventSubscription-1DDYF1E3B3I`  | 
|  [AWS::RDS::OptionGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-rds-optiongroup.html)  |  Name  |  `mystack-myoptiongroup-1qmfawfea4vmz`  | 
|  [AWS::Redshift::Cluster](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-redshift-cluster.html)  |  Name  |  `mystack-myredshiftcluster-ranmiv3f0mad`  | 
|  [AWS::Redshift::ClusterParameterGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-redshift-clusterparametergroup.html)  |  Name  |  `mysta-mypar-1AJYM1FL3WQBW`  | 
|  [AWS::Redshift::ClusterSecurityGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-redshift-clustersecuritygroup.html)  |  Name  |  `mystack-myredshiftclustersecuritygroup-bjy2afmhy3ee`  | 
|  [AWS::Redshift::ClusterSubnetGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-redshift-clustersubnetgroup.html)  |  Name  |  `mystack-myredshiftclustersubnetgroup-aq6rsdq8rp71`  | 
|  [AWS::RoboMaker::Fleet](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-robomaker-fleet.html)  | Amazon Resource Name \(ARN\) of the fleet |  `arn:aws:robomaker:us-west-2:123456789012:deployment-fleet/MyFleet/1539894765711`  | 
|  [AWS::RoboMaker::Robot](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-robomaker-robot.html)  |  Amazon Resource Name \(ARN\) of the robot  |  `arn:aws:robomaker:us-west-2:123456789012:robot/MyRobot/1544035373264`  | 
|  [AWS::RoboMaker::RobotApplication](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-robomaker-robotapplication.html)  |  Amazon Resource Name \(ARN\) of the robot application  |  `arn:aws:robomaker:us-west-2:123456789012:robot-application/MyRobotApplication/1546541208251`  | 
|  [AWS::RoboMaker::RobotApplicationVersion](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-robomaker-robotapplicationversion.html)  |  Amazon Resource Name \(ARN\) of the robot application version  |  `arn:aws:robomaker:us-west-2:123456789012:robot-application/MyRobotApplication/1546541208251`  | 
|  [AWS::RoboMaker::SimulationApplication](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-robomaker-simulationapplication.html)  |  Amazon Resource Name \(ARN\) of the simulation application  |  `arn:aws:robomaker:us-west-2:123456789012:simulation-application/MySimulationApplication/1546541201334`  | 
|  [AWS::RoboMaker::SimulationApplicationVersion](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-robomaker-simulationapplicationversion.html)  |  Amazon Resource Name \(ARN\) of the simulation application version  |  `arn:aws:robomaker:us-west-2:123456789012:simulation-application/MySimulationApplication/1546541201334`  | 
|  [AWS::Route53::HealthCheck](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-route53-healthcheck.html)  |  Amazon Route 53 health check ID  |  `e0a123b4-4dba-4650-935e-example`  | 
|  [AWS::Route53::HostedZone](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-route53-hostedzone.html)  | Hosted zone ID |  `Z23ABC4XYZL05B`  | 
|  [AWS::Route53::RecordSet](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-route53-recordset.html)  |  Name  |   | 
|  [AWS::Route53::RecordSetGroup](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-route53-recordsetgroup.html)  |  Name  |   | 
|  [AWS::Route53Resolver::ResolverEndpoint](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-route53resolver-resolverendpoint.html)  | Endpoint ID |  `rslvr-out-fdc049932dexample`  | 
|  [AWS::Route53Resolver::ResolverRule](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-route53resolver-resolverrule.html)  | Rule ID |  `rslvr-rr-5328a0899aexample`  | 
|  [AWS::Route53Resolver::ResolverRuleAssociation](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-route53resolver-resolverruleassociation.html)  | Resolver rule association ID |  `rslvr-rrassoc-97242eaf88example`  | 
|  [AWS::S3::Bucket](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-s3-bucket.html)  |  Name  |  `mystack-mys3bucket-1hbsmonr9mytq`  | 
|  [AWS::SageMaker::Endpoint](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-sagemaker-endpoint.html)  |  Amazon Resource Name \(ARN\) of the endpoint  |  `arn:aws:sagemaker:us-west-2:012345678901:endpoint/myendpoint`  | 
|  [AWS::SageMaker::EndpointConfig](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-sagemaker-endpointconfig.html)  |  Amazon Resource Name \(ARN\) of the endpoint configuration  |  `arn:aws:sagemaker:us-west-2:012345678901:endpoint-config/myendpointconfig`  | 
|  [AWS::SageMaker::Model](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-sagemaker-model.html)  |  Amazon Resource Name \(ARN\) of the model  |  `arn:aws:sagemaker:us-west-2:012345678901:model/mymodel`  | 
|  [AWS::SageMaker::NotebookInstance](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-sagemaker-notebookinstance.html)  |  Amazon Resource Name \(ARN\) of the notebook instance  |  `arn:aws:sagemaker:us-west-2:012345678901:notebook-instance/mynotebookinstance`  | 
|  [AWS::SageMaker::NotebookInstanceLifecycleConfig](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-sagemaker-notebookinstancelifecycleconfig.html)  |  Amazon Resource Name \(ARN\) of the lifecycle configuration  |  `arn:aws:sagemaker:us-west-2:012345678901:notebook-instance-lifecycle-config/mylifecycleconfig`  | 
|  [AWS::SecretsManager::ResourcePolicy](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-secretsmanager-resourcepolicy.html)  |  ARN of the secret  |  `arn:aws:secretsmanager:us-west-2:123456789012:secret:my-path/my-secret-name-1a2b3c`  | 
|  [AWS::SecretsManager::RotationSchedule](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-secretsmanager-rotationschedule.html)  |  ARN of the secret  |  `arn:aws:secretsmanager:us-west-2:123456789012:secret:my-path/my-secret-name-1a2b3c`  | 
| [AWS::SecretsManager::Secret](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-secretsmanager-secret.html) | Secret ARN | arn:aws:secretsmanager:us\-east\-2:123456789012:secret:MyPath/MySecretName\-a1b2c3 | 
|  [AWS::SecretsManager::SecretTargetAttachment](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-secretsmanager-secrettargetattachment.html)  |  Secret ARN  |  `arn:aws:secretsmanager:us-west-2:123456789012:secret:my-path/my-secret-name-1a2b3c`  | 
|  [AWS::ServiceCatalog::AcceptedPortfolioShare](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-servicecatalog-acceptedportfolioshare.html)  |  Id  |   | 
|  [AWS::ServiceCatalog::CloudFormationProduct](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-servicecatalog-cloudformationproduct.html)  |  Provisioning artifact ID  |  `prod-nd24wbqkm4pju`  | 
|  [AWS::ServiceCatalog::CloudFormationProvisionedProduct](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-servicecatalog-cloudformationprovisionedproduct.html)  |  Provisioned product ID  |  `pp-hfyszaotincww`  | 
|  [AWS::ServiceCatalog::LaunchNotificationConstraint](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-servicecatalog-launchnotificationconstraint.html)  |  Constraint ID  |   | 
|  [AWS::ServiceCatalog::LaunchRoleConstraint](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-servicecatalog-launchroleconstraint.html)  |  Constraint ID  |   | 
|  [AWS::ServiceCatalog::LaunchTemplateConstraint](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-servicecatalog-launchtemplateconstraint.html)  |  Constraint ID  |   | 
|  [AWS::ServiceCatalog::Portfolio](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-servicecatalog-portfolio.html)  |  Portfolio ID  |   | 
|  [AWS::ServiceCatalog::PortfolioPrincipalAssociation](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-servicecatalog-portfolioprincipalassociation.html)  |  Association ID  |   | 
|  [AWS::ServiceCatalog::PortfolioProductAssociation](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-servicecatalog-portfolioproductassociation.html)  |  Association ID  |   | 
|  [AWS::ServiceCatalog::PortfolioShare](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-servicecatalog-portfolioshare.html)  |  Portfolio share ID  |   | 
|  [AWS::ServiceCatalog::ResourceUpdateConstraint](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-servicecatalog-resourceupdateconstraint.html)  |  Constraint ID  |   | 
|  [AWS::ServiceCatalog::TagOption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-servicecatalog-tagoption.html)  |  Tag option ID  |   | 
|  [AWS::ServiceCatalog::TagOptionAssociation](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-servicecatalog-tagoptionassociation.html)  |  Association ID  |   | 
|  [AWS::ServiceDiscovery::HttpNamespace](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-servicediscovery-httpnamespace.html)  |  Id  |  `ns-d6wz3hq6kexample`  | 
|  [AWS::ServiceDiscovery::Instance](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-servicediscovery-instance.html)  |  `Id`  |   | 
|  [AWS::ServiceDiscovery::PrivateDnsNamespace](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-servicediscovery-privatednsnamespace.html)  |  `Id`  |   | 
|  [AWS::ServiceDiscovery::PublicDnsNamespace](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-servicediscovery-publicdnsnamespace.html)  |  `Id`  |   | 
|  [AWS::ServiceDiscovery::Service](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-servicediscovery-service.html)  |  `Id`  |   | 
|  [AWS::SES::ConfigurationSet](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ses-configurationset.html)  |  Name  |   | 
|  [AWS::SES::ReceiptRule](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ses-receiptrule.html)  |  Name  |  `my-receipt-rule`  | 
|  [AWS::SES::ReceiptRuleSet](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ses-receiptruleset.html)  |  Name  |  `my-receipt-rule-set`  | 
|  [AWS::SDB::Domain](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-simpledb.html)  |  Name  |  `mystack-mysdbdomain-IVNAOZTDFVXL`  | 
|  [AWS::SNS::Topic](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-sns-topic.html)  |  Topic ARN  |  `arn:aws:sns:``us-east-2``:123456789012:mystack-mytopic-NZJ5JSMVGFIE`  | 
|  [AWS::SQS::Queue](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-sqs-queues.html)  |  Queue URL  |  `https://sqs.``us-east-2``.amazonaws.com/803981987763/aa4-MyQueue-Z5NOSZO2PZE9`  | 
|  [AWS::SSM::Document](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ssm-document.html)  |  SSM document name  |  `ssm-myinstanceconfig-ABCNPH3XCAO6`  | 
|  [AWS::SSM::MaintenanceWindow](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ssm-maintenancewindow.html)  |  Maintenance window ID  |  `mw-abcde1234567890yz`  | 
|  [AWS::SSM::MaintenanceWindowTarget](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ssm-maintenancewindowtarget.html)  |  Maintenance window target ID  |  `12a345b6-bbb7-4bb6-90b0-8c9577a2d2b9`  | 
|  [AWS::SSM::MaintenanceWindowTask](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ssm-maintenancewindowtask.html)  |  Maintenance window task ID  |  `12a345b6-bbb7-4bb6-90b0-8c9577a2d2b9`  | 
|  [AWS::SSM::PatchBaseline](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ssm-patchbaseline.html)  |  Patch baseline ID  |  `pb-abcde1234567890yz` The ID of the default patch baseline provided by AWS is an ARN—for example `arn:aws:ssm:us-west-2:123456789012:patchbaseline/abcde1234567890yz`\.  | 
|  [AWS::SSM::ResourceDataSync](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-ssm-resourcedatasync.html)  |  Name  |  `TestResourceDataSync`  | 
| [AWS::StepFunctions::Activity](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-stepfunctions-activity.html) | Amazon Resource Name \(ARN\) of the AWS Step Functions activity | arn:aws:states:us\-east\-1:111122223333:activity:myActivity | 
| [AWS::StepFunctions::StateMachine](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-stepfunctions-statemachine.html) | ARN of the created Step Functions state machine | arn:aws:states:us\-east\-1:111122223333:stateMachine:MyStateMachine\-ABCDEFGHIJ1K | 
|  [AWS::WAF::ByteMatchSet](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-waf-bytematchset.html)  |  Byte match ID  |  `aabc123a-fb4f-4fc6-becb-2b00831cadcf`  | 
|  [AWS::WAF::IPSet](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-waf-ipset.html)  |  IP set ID  |  `aabc123a-fb4f-4fc6-becb-2b00831cadcf`  | 
|  [AWS::WAF::Rule](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-waf-rule.html)  |  Rule ID  |  `aabc123a-fb4f-4fc6-becb-2b00831cadcf`  | 
|  [AWS::WAF::SizeConstraintSet](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-waf-sizeconstraintset.html)  |  Size constraint set ID  |  `aabc123a-fb4f-4fc6-becb-2b00831cadcf`  | 
|  [AWS::WAF::SqlInjectionMatchSet](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-waf-sqlinjectionmatchset.html)  |  SQL match set ID  |  `aabc123a-fb4f-4fc6-becb-2b00831cadcf`  | 
|  [AWS::WAF::WebACL](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-waf-webacl.html)  |  Web ACL ID  |  `aabc123a-fb4f-4fc6-becb-2b00831cadcf`  | 
|  [AWS::WAF::XssMatchSet](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-waf-xssmatchset.html)  |  XSS match set ID  |  `aabc123a-fb4f-4fc6-becb-2b00831cadcf`  | 
|  [AWS::WAFRegional::ByteMatchSet](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-wafregional-bytematchset.html)  |  Byte match ID  |  `aabc123a-fb4f-4fc6-becb-2b00831cadcf`  | 
|  [AWS::WAFRegional::IPSet](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-wafregional-ipset.html)  |  IP set ID  |  `aabc123a-fb4f-4fc6-becb-2b00831cadcf`  | 
|  [AWS::WAFRegional::Rule](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-wafregional-rule.html)  |  Rule ID  |  `aabc123a-fb4f-4fc6-becb-2b00831cadcf`  | 
|  [AWS::WAFRegional::SizeConstraintSet](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-wafregional-sizeconstraintset.html)  |  Size constraint set ID  |  `aabc123a-fb4f-4fc6-becb-2b00831cadcf`  | 
|  [AWS::WAFRegional::SqlInjectionMatchSet](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-wafregional-sqlinjectionmatchset.html)  |  SQL match set ID  |  `aabc123a-fb4f-4fc6-becb-2b00831cadcf`  | 
|  [AWS::WAFRegional::WebACL](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-wafregional-webacl.html)  |  Web ACL ID  |  `aabc123a-fb4f-4fc6-becb-2b00831cadcf`  | 
|  [AWS::WAFRegional::XssMatchSet](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-wafregional-xssmatchset.html)  |  XSS match set ID  |  `aabc123a-fb4f-4fc6-becb-2b00831cadcf`  | 
|  [AWS::WorkSpaces::Workspace](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-workspaces-workspace.html)  |  Workspace ID  |  `ws-cdd1gggh7`  | 
|  [Pseudo parameter](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/pseudo-parameter-reference.html#cfn-pseudo-param-accountid)  |  AWS::AccountId  |  `123456789012`  | 
|  [Pseudo parameter](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/pseudo-parameter-reference.html#cfn-pseudo-param-notificationarns)  |  AWS::NotificationARNs  |  `[arn:aws:sns:us-east-1:123456789012:MyTopic]`  | 
|  [Pseudo parameter](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/pseudo-parameter-reference.html#cfn-pseudo-param-novalue)  |  AWS::NoValue  |  Does not return a value\.  | 
|  [Pseudo parameter](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/pseudo-parameter-reference.html#cfn-pseudo-param-partition)  |  AWS::Partition  |  `aws`  | 
|  [Pseudo parameter](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/pseudo-parameter-reference.html#cfn-pseudo-param-region)  |  AWS::Region  |  `us-east-2`  | 
|  [Pseudo parameter](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/pseudo-parameter-reference.html#cfn-pseudo-param-stackid)  |  AWS::StackId  |  `arn:aws:cloudformation:us-east-1:123456789012:stack/MyStack/1c2fa620-982a-11e3-aff7-50e2416294e0`  | 
|  [Pseudo parameter](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/pseudo-parameter-reference.html#cfn-pseudo-param-stackname)  |  AWS::StackName  |  `MyStack`  | 
|  [Pseudo parameter](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/pseudo-parameter-reference.html#cfn-pseudo-param-urlsuffix)  |  AWS::URLSuffix  |  `amazonaws.com`  | 