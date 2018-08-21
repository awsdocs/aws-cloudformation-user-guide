# AWS::DynamoDB::Table<a name="aws-resource-dynamodb-table"></a>

The `AWS::DynamoDB::Table` resource creates a DynamoDB table\. For more information, see [CreateTable](http://docs.aws.amazon.com/amazondynamodb/latest/APIReference/API_CreateTable.html) in the *Amazon DynamoDB API Reference*\.

You should be aware of the following behaviors when working with DynamoDB tables:
+ AWS CloudFormation typically creates DynamoDB tables in parallel\. However, if your template includes multiple DynamoDB tables with indexes, you must declare dependencies so that the tables are created sequentially\. Amazon DynamoDB limits the number of tables with secondary indexes that are in the creating state\. If you create multiple tables with indexes at the same time, DynamoDB returns an error and the stack operation fails\. For an example, see [DynamoDB Table with a DependsOn Attribute](#cfn-dynamodb-table-examples-dependson)\.
+ Updates to `AWS::DynamoDB::Table` resources that are associated with `AWS::ApplicationAutoScaling::ScalableTarget` resources will always result in an update failure and then an update rollback failure\. The following `ScalableDimension` attributes cause this problem when associated with the table:
  + dynamodb:table:ReadCapacityUnits
  + dynamodb:table:WriteCapacityUnits
  + dynamodb:index:ReadCapacityUnits
  + dynamodb:index:WriteCapacityUnits

  As a workaround, please deregister scalable targets before performing updates to `AWS::DynamoDB::Table` resources\.

**Topics**
+ [Syntax](#aws-resource-dynamodb-table-syntax)
+ [Properties](#w3ab2c21c10d373c13)
+ [Return Values](#w3ab2c21c10d373c15)
+ [Examples](#cfn-dynamodb-table-examples)

## Syntax<a name="aws-resource-dynamodb-table-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-dynamodb-table-syntax.json"></a>

```
{
  "Type" : "AWS::DynamoDB::Table",
  "Properties" : {
    "[AttributeDefinitions](#cfn-dynamodb-table-attributedef)" : [ AttributeDefinition, ... ],
    "[GlobalSecondaryIndexes](#cfn-dynamodb-table-gsi)" : [ GlobalSecondaryIndexes, ... ],
    "[KeySchema](#cfn-dynamodb-table-keyschema)" : [ KeySchema, ... ],
    "[LocalSecondaryIndexes](#cfn-dynamodb-table-lsi)" : [ LocalSecondaryIndexes, ... ],
    "[PointInTimeRecoverySpecification](#cfn-dynamodb-table-pointintimerecoveryspecification)" : [PointInTimeRecoverySpecification](aws-properties-dynamodb-table-pointintimerecoveryspecification.md),
    "[ProvisionedThroughput](#cfn-dynamodb-table-provisionedthroughput)" : ProvisionedThroughput,
    "[SSESpecification](#cfn-dynamodb-table-ssespecification)" : SSESpecification,
    "[StreamSpecification](#cfn-dynamodb-table-streamspecification)" : StreamSpecification,
    "[TableName](#cfn-dynamodb-table-tablename)" : String,
    "[Tags](#cfn-dynamodb-table-tags)" : [ Resource Tag, ... ],
    "[TimeToLiveSpecification](#cfn-dynamodb-table-timetolivespecification)" : [TimeToLiveSpecification](aws-properties-dynamodb-table-timetolivespecification.md)
  }
}
```

### YAML<a name="aws-resource-dynamodb-table-syntax.yaml"></a>

```
Type: "AWS::DynamoDB::Table"
Properties:
  [AttributeDefinitions](#cfn-dynamodb-table-attributedef):
    - AttributeDefinition
  [GlobalSecondaryIndexes](#cfn-dynamodb-table-gsi):
    - GlobalSecondaryIndexes
  [KeySchema](#cfn-dynamodb-table-keyschema):
    - KeySchema
  [LocalSecondaryIndexes](#cfn-dynamodb-table-lsi):
    - LocalSecondaryIndexes
  [PointInTimeRecoverySpecification](#cfn-dynamodb-table-pointintimerecoveryspecification): 
    [PointInTimeRecoverySpecification](aws-properties-dynamodb-table-pointintimerecoveryspecification.md)
  [ProvisionedThroughput](#cfn-dynamodb-table-provisionedthroughput):
    ProvisionedThroughput
  [SSESpecification](#cfn-dynamodb-table-ssespecification):
    SSESpecification
  [StreamSpecification](#cfn-dynamodb-table-streamspecification):
    StreamSpecification
  [TableName](#cfn-dynamodb-table-tablename): String
  [Tags](#cfn-dynamodb-table-tags): 
    - Resource Tag
  [TimeToLiveSpecification](#cfn-dynamodb-table-timetolivespecification): 
    [TimeToLiveSpecification](aws-properties-dynamodb-table-timetolivespecification.md)
```

## Properties<a name="w3ab2c21c10d373c13"></a>

`AttributeDefinitions`  <a name="cfn-dynamodb-table-attributedef"></a>
A list of attributes that describe the key schema for the table and indexes\. Duplicates are allowed\.  
*Required*: Yes  
*Type*: List of [DynamoDB Table AttributeDefinition](aws-properties-dynamodb-attributedef.md)  
*Update requires*: [Some interruptions](using-cfn-updating-stacks-update-behaviors.md#update-some-interrupt)\. Replacement if you edit an existing `AttributeDefinition`\.

`GlobalSecondaryIndexes`  <a name="cfn-dynamodb-table-gsi"></a>
Global secondary indexes to be created on the table\. You can create up to 5 global secondary indexes\.  
If you update a table to include a new global secondary index, AWS CloudFormation initiates the index creation and then proceeds with the stack update\. AWS CloudFormation doesn't wait for the index to complete creation because the backfilling phase can take a long time, depending on the size of the table\. You can't use the index or update the table until the index's status is `ACTIVE`\. You can track its status by using the DynamoDB [http://docs.aws.amazon.com/cli/latest/reference/dynamodb/describe-table.html](http://docs.aws.amazon.com/cli/latest/reference/dynamodb/describe-table.html) command\.  
If you add or delete an index during an update, we recommend that you don't update any other resources\. If your stack fails to update and is rolled back while adding a new index, you must manually delete the index\.
*Required*: No  
*Type*: List of [DynamoDB Table GlobalSecondaryIndex](aws-properties-dynamodb-gsi.md)  
*Update requires*: Updates are not supported\. The following are exceptions:  
+ If you update only the provisioned throughput values of global secondary indexes, you can update the table [without interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)\.
+ You can delete or add one global secondary index [without interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)\. If you do both in the same update \(for example, by changing the index's logical ID\), the update fails\.

`KeySchema`  <a name="cfn-dynamodb-table-keyschema"></a>
Specifies the attributes that make up the primary key for the table\. The attributes in the `KeySchema` property must also be defined in the `AttributeDefinitions` property\.  
*Required*: Yes  
*Type*: List of [DynamoDB Table KeySchema](aws-properties-dynamodb-keyschema.md)  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`LocalSecondaryIndexes`  <a name="cfn-dynamodb-table-lsi"></a>
Local secondary indexes to be created on the table\. You can create up to 5 local secondary indexes\. Each index is scoped to a given hash key value\. The size of each hash key can be up to 10 gigabytes\.  
*Required*: No  
*Type*: List of [DynamoDB Table LocalSecondaryIndex](aws-properties-dynamodb-lsi.md)  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`PointInTimeRecoverySpecification`  <a name="cfn-dynamodb-table-pointintimerecoveryspecification"></a>
The settings used to enable point in time recovery\.  
*Required*: No  
*Type*: [DynamoDB Table PointInTimeRecoverySpecification](aws-properties-dynamodb-table-pointintimerecoveryspecification.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`ProvisionedThroughput`  <a name="cfn-dynamodb-table-provisionedthroughput"></a>
Throughput for the specified table, which consists of values for `ReadCapacityUnits` and `WriteCapacityUnits`\. For more information about the contents of a provisioned throughput structure, see [Amazon DynamoDB Table ProvisionedThroughput](aws-properties-dynamodb-provisionedthroughput.md)\.  
*Required*: Yes  
*Type*: [DynamoDB Table ProvisionedThroughput](aws-properties-dynamodb-provisionedthroughput.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`SSESpecification`  <a name="cfn-dynamodb-table-ssespecification"></a>
Specifies the settings to enable server\-side encryption\.  
*Required*: No  
*Type*: [DynamoDB SSESpecification](aws-properties-dynamodb-table-ssespecification.md)  
*Update requires*: [Some interruptions](using-cfn-updating-stacks-update-behaviors.md#update-some-interrupt)

`StreamSpecification`  <a name="cfn-dynamodb-table-streamspecification"></a>
The settings for the DynamoDB table stream, which capture changes to items stored in the table\.  
*Required*: No  
*Type*: [DynamoDB Table StreamSpecification](aws-properties-dynamodb-streamspecification.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) to the table\. However, the stream is replaced\.

`TableName`  <a name="cfn-dynamodb-table-tablename"></a>
A name for the table\. If you don't specify a name, AWS CloudFormation generates a unique physical ID and uses that ID for the table name\. For more information, see [Name Type](aws-properties-name.md)\.  
If you specify a name, you cannot perform updates that require replacement of this resource\. You can perform updates that require no or some interruption\. If you must replace the resource, specify a new name\.
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`Tags`  <a name="cfn-dynamodb-table-tags"></a>
Specifies an arbitrary set of tags \(key–value pairs\) to associate with this table\. Use tags to manage your resources\.  
*Required*: No  
*Type*: [AWS CloudFormation Resource Tags](aws-properties-resource-tags.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`TimeToLiveSpecification`  <a name="cfn-dynamodb-table-timetolivespecification"></a>
Specifies the Time to Live \(TTL\) settings for the table\.  
*Required*: No  
*Type*: [DynamoDB Table TimeToLiveSpecification](aws-properties-dynamodb-table-timetolivespecification.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

**Note**  
For detailed information about the limits in DynamoDB, see [Limits in Amazon DynamoDB](http://docs.aws.amazon.com/amazondynamodb/latest/developerguide/Limits.html) in the *Amazon DynamoDB Developer Guide*\.

## Return Values<a name="w3ab2c21c10d373c15"></a>

### Ref<a name="w3ab2c21c10d373c15b2"></a>

When the logical ID of this resource is provided to the `Ref` intrinsic function, `Ref` returns the resource name\. For example:

```
{ "Ref": "MyResource" }
```

For the resource with the logical ID `myDynamoDBTable`, `Ref` will return the DynamoDB table name\.

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\.

### Fn::GetAtt<a name="w3ab2c21c10d373c15b4"></a>

`Fn::GetAtt` returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

`Arn`  
The Amazon Resource Name \(ARN\) of the DynamoDB table, such as `arn:aws:dynamodb:us-east-2:123456789012:table/myDynamoDBTable`\.

`StreamArn`  
The ARN of the DynamoDB stream, such as `arn:aws:dynamodb:us-east-1:123456789012:table/testddbstack-myDynamoDBTable-012A1SL7SMP5Q/stream/2015-11-30T20:10:00.000`\.  
You must specify the `StreamSpecification` property to use this attribute\.

For more information about using `Fn::GetAtt`, see [Fn::GetAtt](intrinsic-function-reference-getatt.md)\.

## Examples<a name="cfn-dynamodb-table-examples"></a>

### DynamoDB Table with Local and Secondary Indexes<a name="cfn-dynamodb-table-example1"></a>

The following sample creates an DynamoDB table with `Album`, `Artist`, `Sales`, `NumberOfSongs` as attributes\. The primary key includes the `Album` attribute as the hash key and `Artist` attribute as the range key\. The table also includes two global and one secondary index\. For querying the number of sales for a given artist, the global secondary index uses the `Sales` attribute as the hash key and the `Artist` attribute as the range key\.

For querying the sales based on the number of songs, the global secondary index uses the `NumberOfSongs` attribute as the hash key and the `Sales` attribute as the range key\.

For querying the sales of an album, the local secondary index uses the same hash key as the table but uses the `Sales` attribute as the range key\.

#### JSON<a name="aws-resource-dynamodb-table-example1.json"></a>

```
{
  "AWSTemplateFormatVersion" : "2010-09-09",
  "Resources" : {
    "myDynamoDBTable" : {
      "Type" : "AWS::DynamoDB::Table",
      "Properties" : {
        "AttributeDefinitions" : [
          {
            "AttributeName" : "Album",
            "AttributeType" : "S"   
          },
          {
            "AttributeName" : "Artist",
            "AttributeType" : "S"
          },
          {
            "AttributeName" : "Sales",
            "AttributeType" : "N"
          },
          {
            "AttributeName" : "NumberOfSongs",
            "AttributeType" : "N"
          }
        ],
        "KeySchema" : [
          {
            "AttributeName" : "Album",
            "KeyType" : "HASH"
          },
          {
            "AttributeName" : "Artist",
            "KeyType" : "RANGE"
          }
        ],
        "ProvisionedThroughput" : {
          "ReadCapacityUnits" : "5",
          "WriteCapacityUnits" : "5"
        },
        "TableName" : "myTableName",
        "GlobalSecondaryIndexes" : [{
          "IndexName" : "myGSI",
          "KeySchema" : [
            {
              "AttributeName" : "Sales",
              "KeyType" : "HASH"
            },
            {
              "AttributeName" : "Artist",
              "KeyType" : "RANGE"
            }
          ],                         
          "Projection" : {
            "NonKeyAttributes" : ["Album","NumberOfSongs"],
            "ProjectionType" : "INCLUDE"
          },
          "ProvisionedThroughput" : {
            "ReadCapacityUnits" : "5",
            "WriteCapacityUnits" : "5"
          }
        },
        {
          "IndexName" : "myGSI2",
          "KeySchema" : [
            {
              "AttributeName" : "NumberOfSongs",
              "KeyType" : "HASH"
            },
            {
              "AttributeName" : "Sales",
              "KeyType" : "RANGE"
            }
          ],                         
          "Projection" : {
            "NonKeyAttributes" : ["Album","Artist"],
            "ProjectionType" : "INCLUDE"
          },
          "ProvisionedThroughput" : {
            "ReadCapacityUnits" : "5",
            "WriteCapacityUnits" : "5"
          }
        }],
        "LocalSecondaryIndexes" :[{
          "IndexName" : "myLSI",
          "KeySchema" : [
            {
              "AttributeName" : "Album",
              "KeyType" : "HASH"
            },
            {
              "AttributeName" : "Sales",
              "KeyType" : "RANGE"
            }
          ],                           
          "Projection" : {
            "NonKeyAttributes" : ["Artist","NumberOfSongs"],
            "ProjectionType" : "INCLUDE"
          }
        }]
      }
    }
  }
}
```

#### YAML<a name="aws-resource-dynamodb-table-example1.yaml"></a>

```
AWSTemplateFormatVersion: "2010-09-09"
Resources: 
  myDynamoDBTable: 
    Type: "AWS::DynamoDB::Table"
    Properties: 
      AttributeDefinitions: 
        - 
          AttributeName: "Album"
          AttributeType: "S"
        - 
          AttributeName: "Artist"
          AttributeType: "S"
        - 
          AttributeName: "Sales"
          AttributeType: "N"
        - 
          AttributeName: "NumberOfSongs"
          AttributeType: "N"
      KeySchema: 
        - 
          AttributeName: "Album"
          KeyType: "HASH"
        - 
          AttributeName: "Artist"
          KeyType: "RANGE"
      ProvisionedThroughput: 
        ReadCapacityUnits: "5"
        WriteCapacityUnits: "5"
      TableName: "myTableName"
      GlobalSecondaryIndexes: 
        - 
          IndexName: "myGSI"
          KeySchema: 
            - 
              AttributeName: "Sales"
              KeyType: "HASH"
            - 
              AttributeName: "Artist"
              KeyType: "RANGE"
          Projection: 
            NonKeyAttributes: 
              - "Album"
              - "NumberOfSongs"
            ProjectionType: "INCLUDE"
          ProvisionedThroughput: 
            ReadCapacityUnits: "5"
            WriteCapacityUnits: "5"
        - 
          IndexName: "myGSI2"
          KeySchema: 
            - 
              AttributeName: "NumberOfSongs"
              KeyType: "HASH"
            - 
              AttributeName: "Sales"
              KeyType: "RANGE"
          Projection: 
            NonKeyAttributes: 
              - "Album"
              - "Artist"
            ProjectionType: "INCLUDE"
          ProvisionedThroughput: 
            ReadCapacityUnits: "5"
            WriteCapacityUnits: "5"
      LocalSecondaryIndexes: 
        - 
          IndexName: "myLSI"
          KeySchema: 
            - 
              AttributeName: "Album"
              KeyType: "HASH"
            - 
              AttributeName: "Sales"
              KeyType: "RANGE"
          Projection: 
            NonKeyAttributes: 
              - "Artist"
              - "NumberOfSongs"
            ProjectionType: "INCLUDE"
```

### DynamoDB Table with a DependsOn Attribute<a name="cfn-dynamodb-table-examples-dependson"></a>

If you include multiple DynamoDB tables with indexes in a single template, you must include dependencies so that the tables are created sequentially\. DynamoDB limits the number of tables with secondary indexes that are in the creating state\. If you create multiple tables with indexes at the same time, DynamoDB returns an error and the stack operation fails\.

The following sample assumes that the `myFirstDDBTable` table is declared in the same template as the `mySecondDDBTable` table, and both tables include a secondary index\. The `mySecondDDBTable` table includes a dependency on the `myFirstDDBTable` table so that AWS CloudFormation creates the tables one at a time\.

#### JSON<a name="aws-resource-dynamodb-table-example2.json"></a>

```
"mySecondDDBTable" : {
  "Type" : "AWS::DynamoDB::Table",
  "DependsOn" : "myFirstDDBTable" ,
  "Properties" : {
    "AttributeDefinitions" : [
      {
        "AttributeName" : "ArtistId",
        "AttributeType" : "S"        
      },
      {
        "AttributeName" : "Concert",
        "AttributeType" : "S"        
      },
      {
        "AttributeName" : "TicketSales",
        "AttributeType" : "S"        
      }
    ],
    "KeySchema" : [
      {
        "AttributeName" : "ArtistId",
        "KeyType" : "HASH"
      },
      {
        "AttributeName" : "Concert",
        "KeyType" : "RANGE"
      }
    ],
    "ProvisionedThroughput" : {
      "ReadCapacityUnits" : {"Ref" : "ReadCapacityUnits"},
      "WriteCapacityUnits" : {"Ref" : "WriteCapacityUnits"}
    },
    "GlobalSecondaryIndexes" : [{
      "IndexName" : "myGSI",
      "KeySchema" : [
        {
          "AttributeName" : "TicketSales",
          "KeyType" : "HASH"
        }
      ],                           
      "Projection" : {
        "ProjectionType" : "KEYS_ONLY"
      },    
      "ProvisionedThroughput" : {
        "ReadCapacityUnits" : {"Ref" : "ReadCapacityUnits"},
        "WriteCapacityUnits" : {"Ref" : "WriteCapacityUnits"}
      }
    }],    
    "Tags": [
      {
        "Key": "foo",
        "Value": "bar"
      }
    ]
  }
}
```

#### YAML<a name="aws-resource-dynamodb-table-example2.yaml"></a>

```
mySecondDDBTable: 
  Type: "AWS::DynamoDB::Table"
  DependsOn: "myFirstDDBTable"
  Properties: 
    AttributeDefinitions: 
      - 
        AttributeName: "ArtistId"
        AttributeType: "S"
      - 
        AttributeName: "Concert"
        AttributeType: "S"
      - 
        AttributeName: "TicketSales"
        AttributeType: "S"
    KeySchema: 
      - 
        AttributeName: "ArtistId"
        KeyType: "HASH"
      - 
        AttributeName: "Concert"
        KeyType: "RANGE"
    ProvisionedThroughput: 
      ReadCapacityUnits: 
        Ref: "ReadCapacityUnits"
      WriteCapacityUnits: 
        Ref: "WriteCapacityUnits"
    GlobalSecondaryIndexes: 
      - 
        IndexName: "myGSI"
        KeySchema: 
          - 
            AttributeName: "TicketSales"
            KeyType: "HASH"
        Projection: 
          ProjectionType: "KEYS_ONLY"
        ProvisionedThroughput: 
          ReadCapacityUnits: 
            Ref: "ReadCapacityUnits"
          WriteCapacityUnits: 
            Ref: "WriteCapacityUnits"
    Tags:
      - Key: foo
        Value: bar
```

### DynamoDB Table with Application Auto Scaling<a name="cfn-dynamodb-table-examples-application-autoscaling"></a>

This example sets up Application Auto Scaling for a `AWS::DynamoDB::Table` resource\. The template defines a `TargetTrackingScaling` scaling policy that scales up the `WriteCapacityUnits` throughput for the table\.

#### JSON<a name="cfn-dynamodb-table-examples-application-autoscaling.json"></a>

```
{
  "Resources": {
    "DDBTable": {
      "Type": "AWS::DynamoDB::Table",
      "Properties": {
        "AttributeDefinitions": [
          {
            "AttributeName": "ArtistId",
            "AttributeType": "S"
          },
          {
            "AttributeName": "Concert",
            "AttributeType": "S"
          },
          {
            "AttributeName": "TicketSales",
            "AttributeType": "S"
          }
        ],
        "KeySchema": [
          {
            "AttributeName": "ArtistId",
            "KeyType": "HASH"
          },
          {
            "AttributeName": "Concert",
            "KeyType": "RANGE"
          }
        ],
        "GlobalSecondaryIndexes": [
          {
            "IndexName": "GSI",
            "KeySchema": [
              {
                "AttributeName": "TicketSales",
                "KeyType": "HASH"
              }
            ],
            "Projection": {
              "ProjectionType": "KEYS_ONLY"
            },
            "ProvisionedThroughput": {
              "ReadCapacityUnits": 5,
              "WriteCapacityUnits": 5
            }
          }
        ],
        "ProvisionedThroughput": {
          "ReadCapacityUnits": 5,
          "WriteCapacityUnits": 5
        }
      }
    },
    "WriteCapacityScalableTarget": {
      "Type": "AWS::ApplicationAutoScaling::ScalableTarget",
      "Properties": {
        "MaxCapacity": 15,
        "MinCapacity": 5,
        "ResourceId": { "Fn::Join": [
          "/",
          [
            "table",
            { "Ref": "DDBTable" }
          ]
        ] },
        "RoleARN": {
          "Fn::GetAtt": ["ScalingRole", "Arn"]
        },
        "ScalableDimension": "dynamodb:table:WriteCapacityUnits",
        "ServiceNamespace": "dynamodb"
      }
    },
    "ScalingRole": {
      "Type": "AWS::IAM::Role",
      "Properties": {
        "AssumeRolePolicyDocument": {
          "Version": "2012-10-17",
          "Statement": [
            {
              "Effect": "Allow",
              "Principal": {
                "Service": [
                  "application-autoscaling.amazonaws.com"
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
                  "Action": [
                    "dynamodb:DescribeTable",
                    "dynamodb:UpdateTable",
                    "cloudwatch:PutMetricAlarm",
                    "cloudwatch:DescribeAlarms",
                    "cloudwatch:GetMetricStatistics",
                    "cloudwatch:SetAlarmState",
                    "cloudwatch:DeleteAlarms"
                  ],
                  "Resource": "*"
                }
              ]
            }
          }
        ]
      }
    },
    "WriteScalingPolicy": {
      "Type": "AWS::ApplicationAutoScaling::ScalingPolicy",
      "Properties": {
        "PolicyName": "WriteAutoScalingPolicy",
        "PolicyType": "TargetTrackingScaling",
        "ScalingTargetId": {
          "Ref": "WriteCapacityScalableTarget"
        },
        "TargetTrackingScalingPolicyConfiguration": {
          "TargetValue": 50.0,
          "ScaleInCooldown": 60,
          "ScaleOutCooldown": 60,
          "PredefinedMetricSpecification": {
            "PredefinedMetricType": "DynamoDBWriteCapacityUtilization"
          }
        }
      }
    }
  }
}
```

#### YAML<a name="cfn-dynamodb-table-examples-application-autoscaling.yaml"></a>

```
Resources:
  DDBTable:
    Type: "AWS::DynamoDB::Table"
    Properties:
      AttributeDefinitions:
        -
          AttributeName: "ArtistId"
          AttributeType: "S"
        -
          AttributeName: "Concert"
          AttributeType: "S"
        -
          AttributeName: "TicketSales"
          AttributeType: "S"
      KeySchema:
        -
          AttributeName: "ArtistId"
          KeyType: "HASH"
        -
          AttributeName: "Concert"
          KeyType: "RANGE"
      GlobalSecondaryIndexes:
        -
          IndexName: "GSI"
          KeySchema:
            -
              AttributeName: "TicketSales"
              KeyType: "HASH"
          Projection:
            ProjectionType: "KEYS_ONLY"
          ProvisionedThroughput:
            ReadCapacityUnits: 5
            WriteCapacityUnits: 5
      ProvisionedThroughput:
        ReadCapacityUnits: 5
        WriteCapacityUnits: 5
  WriteCapacityScalableTarget:
    Type: "AWS::ApplicationAutoScaling::ScalableTarget"
    Properties:
      MaxCapacity: 15
      MinCapacity: 5
      ResourceId: !Join
        - /
        - - table
          - !Ref DDBTable
      RoleARN: !GetAtt ScalingRole.Arn
      ScalableDimension: dynamodb:table:WriteCapacityUnits
      ServiceNamespace: dynamodb
  ScalingRole:
    Type: "AWS::IAM::Role"
    Properties:
      AssumeRolePolicyDocument:
        Version: "2012-10-17"
        Statement:
          -
            Effect: "Allow"
            Principal:
              Service:
                - application-autoscaling.amazonaws.com
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
                Action:
                  - "dynamodb:DescribeTable"
                  - "dynamodb:UpdateTable"
                  - "cloudwatch:PutMetricAlarm"
                  - "cloudwatch:DescribeAlarms"
                  - "cloudwatch:GetMetricStatistics"
                  - "cloudwatch:SetAlarmState"
                  - "cloudwatch:DeleteAlarms"
                Resource: "*"
  WriteScalingPolicy:
    Type: "AWS::ApplicationAutoScaling::ScalingPolicy"
    Properties:
      PolicyName: WriteAutoScalingPolicy
      PolicyType: TargetTrackingScaling
      ScalingTargetId: !Ref WriteCapacityScalableTarget
      TargetTrackingScalingPolicyConfiguration:
        TargetValue: 50.0
        ScaleInCooldown: 60
        ScaleOutCooldown: 60
        PredefinedMetricSpecification:
          PredefinedMetricType: DynamoDBWriteCapacityUtilization
```