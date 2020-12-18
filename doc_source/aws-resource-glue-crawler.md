# AWS::Glue::Crawler<a name="aws-resource-glue-crawler"></a>

The `AWS::Glue::Crawler` resource specifies an AWS Glue crawler\. For more information, see [Cataloging Tables with a Crawler](https://docs.aws.amazon.com/glue/latest/dg/add-crawler.html) and [Crawler Structure](https://docs.aws.amazon.com/glue/latest/dg/aws-glue-api-crawler-crawling.html#aws-glue-api-crawler-crawling-Crawler) in the *AWS Glue Developer Guide*\.

## Syntax<a name="aws-resource-glue-crawler-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-glue-crawler-syntax.json"></a>

```
{
  "Type" : "AWS::Glue::Crawler",
  "Properties" : {
      "[Classifiers](#cfn-glue-crawler-classifiers)" : [ String, ... ],
      "[Configuration](#cfn-glue-crawler-configuration)" : String,
      "[CrawlerSecurityConfiguration](#cfn-glue-crawler-crawlersecurityconfiguration)" : String,
      "[DatabaseName](#cfn-glue-crawler-databasename)" : String,
      "[Description](#cfn-glue-crawler-description)" : String,
      "[Name](#cfn-glue-crawler-name)" : String,
      "[Role](#cfn-glue-crawler-role)" : String,
      "[Schedule](#cfn-glue-crawler-schedule)" : Schedule,
      "[SchemaChangePolicy](#cfn-glue-crawler-schemachangepolicy)" : SchemaChangePolicy,
      "[TablePrefix](#cfn-glue-crawler-tableprefix)" : String,
      "[Tags](#cfn-glue-crawler-tags)" : Json,
      "[Targets](#cfn-glue-crawler-targets)" : Targets
    }
}
```

### YAML<a name="aws-resource-glue-crawler-syntax.yaml"></a>

```
Type: AWS::Glue::Crawler
Properties: 
  [Classifiers](#cfn-glue-crawler-classifiers): 
    - String
  [Configuration](#cfn-glue-crawler-configuration): String
  [CrawlerSecurityConfiguration](#cfn-glue-crawler-crawlersecurityconfiguration): String
  [DatabaseName](#cfn-glue-crawler-databasename): String
  [Description](#cfn-glue-crawler-description): String
  [Name](#cfn-glue-crawler-name): String
  [Role](#cfn-glue-crawler-role): String
  [Schedule](#cfn-glue-crawler-schedule): 
    Schedule
  [SchemaChangePolicy](#cfn-glue-crawler-schemachangepolicy): 
    SchemaChangePolicy
  [TablePrefix](#cfn-glue-crawler-tableprefix): String
  [Tags](#cfn-glue-crawler-tags): Json
  [Targets](#cfn-glue-crawler-targets): 
    Targets
```

## Properties<a name="aws-resource-glue-crawler-properties"></a>

`Classifiers`  <a name="cfn-glue-crawler-classifiers"></a>
A list of UTF\-8 strings that specify the custom classifiers that are associated with the crawler\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Configuration`  <a name="cfn-glue-crawler-configuration"></a>
Crawler configuration information\. This versioned JSON string allows users to specify aspects of a crawler's behavior\. For more information, see [Configuring a Crawler](https://docs.aws.amazon.com/glue/latest/dg/crawler-configuration.html)\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CrawlerSecurityConfiguration`  <a name="cfn-glue-crawler-crawlersecurityconfiguration"></a>
The name of the `SecurityConfiguration` structure to be used by this crawler\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DatabaseName`  <a name="cfn-glue-crawler-databasename"></a>
The name of the database in which the crawler's output is stored\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Description`  <a name="cfn-glue-crawler-description"></a>
A description of the crawler\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-glue-crawler-name"></a>
The name of the crawler\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Role`  <a name="cfn-glue-crawler-role"></a>
The Amazon Resource Name \(ARN\) of an IAM role that's used to access customer resources, such as Amazon Simple Storage Service \(Amazon S3\) data\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Schedule`  <a name="cfn-glue-crawler-schedule"></a>
For scheduled crawlers, the schedule when the crawler runs\.  
*Required*: No  
*Type*: [Schedule](aws-properties-glue-crawler-schedule.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SchemaChangePolicy`  <a name="cfn-glue-crawler-schemachangepolicy"></a>
The policy that specifies update and delete behaviors for the crawler\.  
*Required*: No  
*Type*: [SchemaChangePolicy](aws-properties-glue-crawler-schemachangepolicy.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TablePrefix`  <a name="cfn-glue-crawler-tableprefix"></a>
The prefix added to the names of tables that are created\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-glue-crawler-tags"></a>
The tags to use with this crawler\.  
*Required*: No  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Targets`  <a name="cfn-glue-crawler-targets"></a>
A collection of targets to crawl\.  
*Required*: Yes  
*Type*: [Targets](aws-properties-glue-crawler-targets.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-glue-crawler-return-values"></a>

### Ref<a name="aws-resource-glue-crawler-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the crawler name\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

## Examples<a name="aws-resource-glue-crawler--examples"></a>



### <a name="aws-resource-glue-crawler--examples--"></a>

The following example creates a crawler for an Amazon S3 target\. 

#### JSON<a name="aws-resource-glue-crawler--examples----json"></a>

```
{
    "Description": "AWS Glue Crawler Test",
    "Resources": {
        "MyRole": {
            "Type": "AWS::IAM::Role",
            "Properties": {
                "AssumeRolePolicyDocument": {
                    "Version": "2012-10-17",
                    "Statement": [
                        {
                            "Effect": "Allow",
                            "Principal": {
                                "Service": [
                                    "glue.amazonaws.com"
                                ]
                            },
                            "Action": [
                                "sts:AssumeRole"
                            ]
                        }
                    ]
                },
                "Path": "/",
                "Policies": [
                    {
                        "PolicyName": "root",
                        "PolicyDocument": {
                            "Version": "2012-10-17",
                            "Statement": [
                                {
                                    "Effect": "Allow",
                                    "Action": "*",
                                    "Resource": "*"
                                }
                            ]
                        }
                    }
                ]
            }
        },
        "MyDatabase": {
            "Type": "AWS::Glue::Database",
            "Properties": {
                "CatalogId": {
                    "Ref": "AWS::AccountId"
                },
                "DatabaseInput": {
                    "Name": "dbCrawler",
                    "Description": "TestDatabaseDescription",
                    "LocationUri": "TestLocationUri",
                    "Parameters": {
                        "key1": "value1",
                        "key2": "value2"
                    }
                }
            }
        },
        "MyClassifier": {
            "Type": "AWS::Glue::Classifier",
            "Properties": {
                "GrokClassifier": {
                    "Name": "CrawlerClassifier",
                    "Classification": "wikiData",
                    "GrokPattern": "%{NOTSPACE:language} %{NOTSPACE:page_title} %{NUMBER:hits:long} %{NUMBER:retrieved_size:long}"
                }
            }
        },
        "MyS3Bucket": {
            "Type": "AWS::S3::Bucket",
            "Properties": {
                "BucketName": "crawlertesttarget",
                "AccessControl": "BucketOwnerFullControl"
            }
        },
        "MyCrawler2": {
            "Type": "AWS::Glue::Crawler",
            "Properties": {
                "Name": "testcrawler1",
                "Role": {
                    "Fn::GetAtt": [
                        "MyRole",
                        "Arn"
                    ]
                },
                "DatabaseName": {
                    "Ref": "MyDatabase"
                },
                "Classifiers": [
                    {
                        "Ref": "MyClassifier"
                    }
                ],
                "Targets": {
                    "S3Targets": [
                        {
                            "Path": {
                                "Ref": "MyS3Bucket"
                            }
                        }
                    ]
                },
                "SchemaChangePolicy": {
                    "UpdateBehavior": "UPDATE_IN_DATABASE",
                    "DeleteBehavior": "LOG"
                },
                "Schedule": {
                    "ScheduleExpression": "cron(0/10 * ? * MON-FRI *)"
                }
            }
        }
    }
}
```

#### YAML<a name="aws-resource-glue-crawler--examples----yaml"></a>

```
Resources:
  MyRole:
    Type: AWS::IAM::Role
    Properties:
      AssumeRolePolicyDocument:
        Version: "2012-10-17"
        Statement:
          -
            Effect: "Allow"
            Principal:
              Service:
                - "glue.amazonaws.com"
            Action:
              - "sts:AssumeRole"
      Path: "/"
      Policies:
        -
          PolicyName: "root"
          PolicyDocument:
            Version: "2012-10-17"
            Statement:
              -
                Effect: "Allow"
                Action: "*"
                Resource: "*"
 
  MyDatabase:
    Type: AWS::Glue::Database
    Properties:
      CatalogId: !Ref AWS::AccountId
      DatabaseInput:
        Name: "dbCrawler"
        Description: "TestDatabaseDescription"
        LocationUri: "TestLocationUri"
        Parameters:
          key1 : "value1"
          key2 : "value2"
 
  MyClassifier:
    Type: AWS::Glue::Classifier
    Properties:
      GrokClassifier:
        Name: "CrawlerClassifier"
        Classification: "wikiData"
        GrokPattern: "%{NOTSPACE:language} %{NOTSPACE:page_title} %{NUMBER:hits:long} %{NUMBER:retrieved_size:long}"
 
  MyS3Bucket:
    Type: AWS::S3::Bucket
    Properties:
      BucketName: "crawlertesttarget"
      AccessControl: "BucketOwnerFullControl"
 
  MyCrawler2:
    Type: AWS::Glue::Crawler
    Properties:
      Name: "testcrawler1"
      Role: !GetAtt MyRole.Arn
      DatabaseName: !Ref MyDatabase
      Classifiers:
        - !Ref MyClassifier
      Targets:
        S3Targets:
          - Path: !Ref MyS3Bucket
      SchemaChangePolicy:
        UpdateBehavior: "UPDATE_IN_DATABASE"
        DeleteBehavior: "LOG"
      Schedule:
        ScheduleExpression: "cron(0/10 * ? * MON-FRI *)"
```

### Crawler Configuration<a name="aws-resource-glue-crawler--examples--Crawler_Configuration"></a>

The following example specifies a configuration that controls a crawler's behavior\. 

#### JSON<a name="aws-resource-glue-crawler--examples--Crawler_Configuration--json"></a>

```
{
    "Type": "AWS::Glue::Crawler",
    "Properties": {
        "Role": "role1",
        "Classifiers": [],
        "Description": "example classifier",
        "SchemaChangePolicy": "",
        "Schedule": "Schedule",
        "DatabaseName": "test",
        "Targets": [],
        "TablePrefix": "test-",
        "Name": "my-crawler",
        "Configuration": "{\"Version\":1.0,\"CrawlerOutput\":{\"Partitions\":{\"AddOrUpdateBehavior\":\"InheritFromTable\"},\"Tables\":{\"AddOrUpdateBehavior\":\"MergeNewColumns\"}}}"
    }
}
```

#### YAML<a name="aws-resource-glue-crawler--examples--Crawler_Configuration--yaml"></a>

```
Type: AWS::Glue::Crawler
Properties:
  Role: role1
  Classifiers:
    - ''
  Description: example classifier
  SchemaChangePolicy: ''
  Schedule: Schedule
  DatabaseName: test
  Targets:
    - ''
  TablePrefix: test-
  Name: my-crawler
  Configuration: "{\"Version\":1.0,\"CrawlerOutput\":{\"Partitions\":{\"AddOrUpdateBehavior\":\"InheritFromTable\"},\"Tables\":{\"AddOrUpdateBehavior\":\"MergeNewColumns\"}}}"
```