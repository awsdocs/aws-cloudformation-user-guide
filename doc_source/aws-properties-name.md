# Name Type<a name="aws-properties-name"></a>

For some resources, you can specify a custom name\. By default, AWS CloudFormation generates a unique physical ID to name a resource\. For example, AWS CloudFormation might name an Amazon S3 bucket with the following physical ID `stack123123123123-s3bucket-abcdefghijk1`\. With custom names, you can specify a name that's easier to read and identify, such as `production-app-logs` or `business-metrics`\.

Resource names must be unique across all of your active stacks\. If you reuse templates to create multiple stacks, you must change or remove custom names from your template\. If you don't specify a name, AWS CloudFormation generates a unique physical ID to name the resource\. Names must begin with a letter; contain only ASCII letters, digits, and hyphens; and not end with a hyphen or contain two consecutive hyphens\.

Also, do not manage stack resources outside of AWS CloudFormation\. For example, if you rename a resource that's part of a stack without using AWS CloudFormation, you might get an error any time you try to update or delete that stack\.

**Important**  
You can't perform an update that causes a custom\-named resource to be replaced\. If you must replace the resource, specify a new name\.

## Example<a name="aws-properties-name-example"></a>

If you want to use a custom name, specify a name property for that resource in your AWS CloudFormation template\. Each resource that supports custom names has its own property that you specify\. For example, to name an DynamoDB table, you use the `TableName` property, as shown in the following sample:

### JSON<a name="aws-properties-name-example.json"></a>

```
"myDynamoDBTable" : {
   "Type" : "AWS::DynamoDB::Table",
   "Properties" : {
      "KeySchema" : {
         "HashKeyElement": {
            "AttributeName" : "AttributeName1",
            "AttributeType" : "S"
         },
         "RangeKeyElement" : {
            "AttributeName" : "AttributeName2",
            "AttributeType" : "N"
         }
      },
      "ProvisionedThroughput" : {
         "ReadCapacityUnits" : "5",
         "WriteCapacityUnits" : "10"
      },
      "TableName" : "SampleTable"
   }
}
```

### YAML<a name="aws-properties-name-example.yaml"></a>

```
myDynamoDBTable: 
  Type: "AWS::DynamoDB::Table"
  Properties: 
    KeySchema: 
      HashKeyElement: 
        AttributeName: "AttributeName1"
        AttributeType: "S"
      RangeKeyElement: 
        AttributeName: "AttributeName2"
        AttributeType: "N"
    ProvisionedThroughput: 
      ReadCapacityUnits: "5"
      WriteCapacityUnits: "10"
    TableName: "SampleTable"
```

## Supported Resources<a name="w3ab2c21c14e1541c13"></a>

The following resource types support custom names:
+ [AWS::ApiGateway::ApiKey](aws-resource-apigateway-apikey.md)
+ [AWS::ApiGateway::Model](aws-resource-apigateway-model.md)
+ [AWS::CloudWatch::Alarm](aws-properties-cw-alarm.md)
+ [AWS::DynamoDB::Table](aws-resource-dynamodb-table.md)
+ [AWS::ElasticBeanstalk::Application](aws-properties-beanstalk.md)
+ [AWS::ElasticBeanstalk::Environment](aws-properties-beanstalk-environment.md)
+ [AWS::CodeDeploy::Application](aws-resource-codedeploy-application.md)
+ [AWS::CodeDeploy::DeploymentConfig](aws-resource-codedeploy-deploymentconfig.md)
+ [AWS::CodeDeploy::DeploymentGroup](aws-resource-codedeploy-deploymentgroup.md)
+ [AWS::Config::ConfigRule](aws-resource-config-configrule.md)
+ [AWS::Config::DeliveryChannel](aws-resource-config-deliverychannel.md)
+ [AWS::Config::ConfigurationRecorder](aws-resource-config-configurationrecorder.md)
+ [AWS::ElasticLoadBalancing::LoadBalancer](aws-properties-ec2-elb.md)
+ [AWS::EC2::SecurityGroup](aws-properties-ec2-security-group.md)
+ [AWS::ElastiCache::CacheCluster](aws-properties-elasticache-cache-cluster.md)
+ [AWS::ECR::Repository](aws-resource-ecr-repository.md)
+ [AWS::ECS::Cluster](aws-resource-ecs-cluster.md)
+ [AWS::Elasticsearch::Domain](aws-resource-elasticsearch-domain.md)
+ [AWS::Events::Rule](aws-resource-events-rule.md)
+ [AWS::IAM::Group](aws-properties-iam-group.md)
+ [AWS::IAM::ManagedPolicy](aws-resource-iam-managedpolicy.md)
+ [AWS::IAM::Role](aws-resource-iam-role.md)
+ [AWS::IAM::User](aws-properties-iam-user.md)
+ [AWS::Lambda::Function](aws-resource-lambda-function.md)
+ [AWS::RDS::DBInstance](aws-properties-rds-database-instance.md)
+ [AWS::S3::Bucket](aws-properties-s3-bucket.md)
+ [AWS::SNS::Topic](aws-properties-sns-topic.md)
+ [AWS::SQS::Queue](aws-properties-sqs-queues.md)