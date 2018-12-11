# Resources that Support Drift Detection<a name="using-cfn-stack-drift-resource-list"></a>

The following resource types support drift detection\.


| Service | Resource | 
| --- | --- | 
| API Gateway |  [AWS::ApiGateway::Authorizer](aws-resource-apigateway-authorizer.md) [AWS::ApiGateway::Deployment](aws-resource-apigateway-deployment.md) [AWS::ApiGateway::Method](aws-resource-apigateway-method.md) [AWS::ApiGateway::Model](aws-resource-apigateway-model.md) [AWS::ApiGateway::Resource](aws-resource-apigateway-resource.md) [AWS::ApiGateway::RestApi](aws-resource-apigateway-restapi.md) [AWS::ApiGateway::RequestValidator](aws-resource-apigateway-requestvalidator.md) [AWS::ApiGateway::Stage](aws-resource-apigateway-stage.md)  | 
| Auto Scaling |  [AWS::AutoScaling::AutoScalingGroup](aws-properties-as-group.md) [AWS::AutoScaling::LaunchConfiguration](aws-properties-as-launchconfig.md) [AWS::AutoScaling::LifecycleHook](aws-resource-as-lifecyclehook.md) [AWS::AutoScaling::ScalingPolicy](aws-properties-as-policy.md) [AWS::AutoScaling::ScheduledAction](aws-resource-as-scheduledaction.md)  | 
| CloudTrail |  [AWS::CloudTrail::Trail](aws-resource-cloudtrail-trail.md)  | 
| CloudWatch |  [AWS::CloudWatch::Alarm](aws-properties-cw-alarm.md) [AWS::Events::Rule](aws-resource-events-rule.md) [AWS::Logs::LogGroup](aws-resource-logs-loggroup.md) [AWS::Logs::MetricFilter](aws-resource-logs-metricfilter.md) [AWS::Logs::SubscriptionFilter](aws-resource-logs-subscriptionfilter.md)  | 
| DynamoDB |  [AWS::DynamoDB::Table](aws-resource-dynamodb-table.md)  | 
| Amazon EC2 |  [AWS::EC2::EIP](aws-properties-ec2-eip.md) [AWS::EC2::Instance](aws-properties-ec2-instance.md) [AWS::EC2::InternetGateway](aws-resource-ec2-internetgateway.md) [AWS::EC2::NatGateway](aws-resource-ec2-natgateway.md) [AWS::EC2::NetworkAcl](aws-resource-ec2-network-acl.md) [AWS::EC2::NetworkInterface](aws-resource-ec2-network-interface.md) [AWS::EC2::RouteTable](aws-resource-ec2-route-table.md) [AWS::EC2::SecurityGroup](aws-properties-ec2-security-group.md) [AWS::EC2::Subnet](aws-resource-ec2-subnet.md) [AWS::EC2::Volume](aws-properties-ec2-ebs-volume.md) [AWS::EC2::VPC](aws-resource-ec2-vpc.md)  | 
| Amazon ECS |  [AWS::ECS::Cluster](aws-resource-ecs-cluster.md) [AWS::ECS::Service](aws-resource-ecs-service.md) [AWS::ECS::TaskDefinition](aws-resource-ecs-taskdefinition.md)  | 
| Elastic Load Balancing |  [AWS::ElasticLoadBalancing::LoadBalancer](aws-properties-ec2-elb.md) [AWS::ElasticLoadBalancingV2::Listener](aws-resource-elasticloadbalancingv2-listener.md) [AWS::ElasticLoadBalancingV2::ListenerRule](aws-resource-elasticloadbalancingv2-listenerrule.md) [AWS::ElasticLoadBalancingV2::LoadBalancer](aws-resource-elasticloadbalancingv2-loadbalancer.md)  | 
| IAM |  [AWS::IAM::Group](aws-properties-iam-group.md) [AWS::IAM::InstanceProfile](aws-resource-iam-instanceprofile.md) [AWS::IAM::ManagedPolicy](aws-resource-iam-managedpolicy.md) [AWS::IAM::Role](aws-resource-iam-role.md) [AWS::IAM::User](aws-properties-iam-user.md)  | 
| AWS IoT |  [AWS::IoT::Thing](aws-resource-iot-thing.md)  | 
| Lambda |  [AWS::Lambda::Alias](aws-resource-lambda-alias.md) [AWS::Lambda::Function](aws-resource-lambda-function.md) [AWS::Lambda::Version](aws-resource-lambda-version.md)  | 
| Amazon RDS |  [AWS::RDS::DBCluster](aws-resource-rds-dbcluster.md) [AWS::RDS::DBInstance](aws-properties-rds-database-instance.md)  | 
| Route 53 |  [AWS::Route53::HostedZone](aws-resource-route53-hostedzone.md)  | 
| Amazon S3 |  [AWS::S3::Bucket](aws-properties-s3-bucket.md)  | 
| Amazon SNS |  [AWS::SNS::Topic](aws-properties-sns-topic.md)  | 
| Amazon SQS |  [AWS::SQS::Queue](aws-properties-sqs-queues.md)  | 