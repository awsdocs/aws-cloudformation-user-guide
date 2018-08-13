# AWS::Glue::Crawler<a name="aws-resource-glue-crawler"></a>

The `AWS::Glue::Crawler` resource specifies an AWS Glue crawler\. For more information, see [Cataloging Tables with a Crawler](http://docs.aws.amazon.com/glue/latest/dg/add-crawler.html) and [Crawler Structure](http://docs.aws.amazon.com/glue/latest/dg/aws-glue-api-crawler-crawling.html#aws-glue-api-crawler-crawling-Crawler) in the *AWS Glue Developer Guide*\. 

**Topics**
+ [Syntax](#aws-resource-glue-crawler-syntax)
+ [Properties](#aws-resource-glue-crawler-properties)
+ [Return Values](#aws-resource-glue-crawler-returnvalues)
+ [Examples](#aws-resource-glue-crawler-examples)

## Syntax<a name="aws-resource-glue-crawler-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-glue-crawler-syntax.json"></a>

```
{
  "Type" : "AWS::Glue::Crawler",
  "Properties" : {
    "[Role](#cfn-glue-crawler-role)" : String,
    "[Classifiers](#cfn-glue-crawler-classifiers)" : [ String, ... ],
    "[Description](#cfn-glue-crawler-description)" : String,
    "[SchemaChangePolicy](#cfn-glue-crawler-schemachangepolicy)" : [*SchemaChangePolicy*](aws-properties-glue-crawler-schemachangepolicy.md),
    "[Schedule](#cfn-glue-crawler-schedule)" : [*Schedule*](aws-properties-glue-crawler-schedule.md),
    "[DatabaseName](#cfn-glue-crawler-databasename)" : String,
    "[Targets](#cfn-glue-crawler-targets)" : [*Targets*](aws-properties-glue-crawler-targets.md),
    "[TablePrefix](#cfn-glue-crawler-tableprefix)" : String,
    "[Name](#cfn-glue-crawler-name)" : String
  }
}
```

### YAML<a name="aws-resource-glue-crawler-syntax.yaml"></a>

```
Type: "AWS::Glue::Crawler"
Properties:
  [Role](#cfn-glue-crawler-role): String
  [Classifiers](#cfn-glue-crawler-classifiers): 
    - String
  [Description](#cfn-glue-crawler-description): String
  [SchemaChangePolicy](#cfn-glue-crawler-schemachangepolicy): 
    [*SchemaChangePolicy*](aws-properties-glue-crawler-schemachangepolicy.md)
  [Schedule](#cfn-glue-crawler-schedule): 
    [*Schedule*](aws-properties-glue-crawler-schedule.md)
  [DatabaseName](#cfn-glue-crawler-databasename): String
  [Targets](#cfn-glue-crawler-targets): 
    [*Targets*](aws-properties-glue-crawler-targets.md)
  [TablePrefix](#cfn-glue-crawler-tableprefix): String
  [Name](#cfn-glue-crawler-name): String
```

## Properties<a name="aws-resource-glue-crawler-properties"></a>

`Role`  <a name="cfn-glue-crawler-role"></a>
The Amazon Resource Name \(ARN\) of an IAM role that's used to access customer resources, such as Amazon S3 data\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Classifiers`  <a name="cfn-glue-crawler-classifiers"></a>
A list of UTF\-8 strings that specify the custom classifiers that are associated with the crawler\.  
 *Required*: No  
 *Type*: List of String values  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Description`  <a name="cfn-glue-crawler-description"></a>
A description of the crawler and where it should be used\. It must match the URI address multi\-line string pattern: `[\u0020-\uD7FF\uE000-\uFFFD\uD800\uDC00-\uDBFF\uDFFF\r\n\t]*`  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`SchemaChangePolicy`  <a name="cfn-glue-crawler-schemachangepolicy"></a>
The policy that specifies update and delete behaviors for the crawler\.  
 *Required*: No  
 *Type*: [AWS Glue Crawler SchemaChangePolicy](aws-properties-glue-crawler-schemachangepolicy.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Schedule`  <a name="cfn-glue-crawler-schedule"></a>
The schedule for the crawler\.  
 *Required*: No  
 *Type*: [AWS Glue Crawler Schedule](aws-properties-glue-crawler-schedule.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`DatabaseName`  <a name="cfn-glue-crawler-databasename"></a>
The name of the database where the crawler's output is stored\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Targets`  <a name="cfn-glue-crawler-targets"></a>
The crawler targets\.  
 *Required*: Yes  
 *Type*: [AWS Glue Crawler Targets](aws-properties-glue-crawler-targets.md)  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`TablePrefix`  <a name="cfn-glue-crawler-tableprefix"></a>
The table prefix that's used for catalog tables that are created\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`Name`  <a name="cfn-glue-crawler-name"></a>
The name of the crawler\. Must match the single\-line string pattern: `[\u0020-\uD7FF\uE000-\uFFFD\uD800\uDC00-\uDBFF\uDFFF\t]*`  
 *Required*: No  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

## Return Values<a name="aws-resource-glue-crawler-returnvalues"></a>

### Ref<a name="w3ab2c21c10d704c10b3"></a>

When the logical ID of this resource is provided to the `Ref` intrinsic function, `Ref` returns the resource name\.

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\. 

## Examples<a name="aws-resource-glue-crawler-examples"></a>

### <a name="aws-resource-glue-crawler-example1"></a>

The following example creates a crawler for an Amazon S3 target\.

#### JSON<a name="aws-resource-glue-crawler-example1.json"></a>

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

#### YAML<a name="aws-resource-glue-crawler-example1.yaml"></a>

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