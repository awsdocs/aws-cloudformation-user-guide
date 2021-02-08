# AWS::DynamoDB::Table<a name="aws-resource-dynamodb-table"></a>

The `AWS::DynamoDB::Table` resource creates a DynamoDB table\. For more information, see [CreateTable](https://docs.aws.amazon.com/amazondynamodb/latest/APIReference/API_CreateTable.html) in the *Amazon DynamoDB API Reference*\.

You should be aware of the following behaviors when working with DynamoDB tables:
+ AWS CloudFormation typically creates DynamoDB tables in parallel\. However, if your template includes multiple DynamoDB tables with indexes, you must declare dependencies so that the tables are created sequentially\. Amazon DynamoDB limits the number of tables with secondary indexes that are in the creating state\. If you create multiple tables with indexes at the same time, DynamoDB returns an error and the stack operation fails\. For an example, see [DynamoDB Table with a DependsOn Attribute](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-dynamodb-table.html#cfn-dynamodb-table-examples-dependson)\.

## Syntax<a name="aws-resource-dynamodb-table-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-dynamodb-table-syntax.json"></a>

```
{
  "Type" : "AWS::DynamoDB::Table",
  "Properties" : {
      "[AttributeDefinitions](#cfn-dynamodb-table-attributedef)" : [ AttributeDefinition, ... ],
      "[BillingMode](#cfn-dynamodb-table-billingmode)" : String,
      "[GlobalSecondaryIndexes](#cfn-dynamodb-table-gsi)" : [ GlobalSecondaryIndex, ... ],
      "[KeySchema](#cfn-dynamodb-table-keyschema)" : [ KeySchema, ... ],
      "[LocalSecondaryIndexes](#cfn-dynamodb-table-lsi)" : [ LocalSecondaryIndex, ... ],
      "[PointInTimeRecoverySpecification](#cfn-dynamodb-table-pointintimerecoveryspecification)" : PointInTimeRecoverySpecification,
      "[ProvisionedThroughput](#cfn-dynamodb-table-provisionedthroughput)" : ProvisionedThroughput,
      "[SSESpecification](#cfn-dynamodb-table-ssespecification)" : SSESpecification,
      "[StreamSpecification](#cfn-dynamodb-table-streamspecification)" : StreamSpecification,
      "[TableName](#cfn-dynamodb-table-tablename)" : String,
      "[Tags](#cfn-dynamodb-table-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ],
      "[TimeToLiveSpecification](#cfn-dynamodb-table-timetolivespecification)" : TimeToLiveSpecification
    }
}
```

### YAML<a name="aws-resource-dynamodb-table-syntax.yaml"></a>

```
Type: AWS::DynamoDB::Table
Properties: 
  [AttributeDefinitions](#cfn-dynamodb-table-attributedef): 
    - AttributeDefinition
  [BillingMode](#cfn-dynamodb-table-billingmode): String
  [GlobalSecondaryIndexes](#cfn-dynamodb-table-gsi): 
    - GlobalSecondaryIndex
  [KeySchema](#cfn-dynamodb-table-keyschema): 
    - KeySchema
  [LocalSecondaryIndexes](#cfn-dynamodb-table-lsi): 
    - LocalSecondaryIndex
  [PointInTimeRecoverySpecification](#cfn-dynamodb-table-pointintimerecoveryspecification): 
    PointInTimeRecoverySpecification
  [ProvisionedThroughput](#cfn-dynamodb-table-provisionedthroughput): 
    ProvisionedThroughput
  [SSESpecification](#cfn-dynamodb-table-ssespecification): 
    SSESpecification
  [StreamSpecification](#cfn-dynamodb-table-streamspecification): 
    StreamSpecification
  [TableName](#cfn-dynamodb-table-tablename): String
  [Tags](#cfn-dynamodb-table-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
  [TimeToLiveSpecification](#cfn-dynamodb-table-timetolivespecification): 
    TimeToLiveSpecification
```

## Properties<a name="aws-resource-dynamodb-table-properties"></a>

`AttributeDefinitions`  <a name="cfn-dynamodb-table-attributedef"></a>
A list of attributes that describe the key schema for the table and indexes\.  
This property is required to create a DynamoDB table\.  
Update requires: [Some interruptions](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-some-interrupt)\. Replacement if you edit an existing AttributeDefinition\.   
*Required*: Conditional  
*Type*: List of [AttributeDefinition](aws-properties-dynamodb-attributedef.md)  
*Update requires*: [Some interruptions](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-some-interrupt)

`BillingMode`  <a name="cfn-dynamodb-table-billingmode"></a>
Specify how you are charged for read and write throughput and how you manage capacity\.  
Valid values include:  
+  `PROVISIONED` \- We recommend using `PROVISIONED` for predictable workloads\. `PROVISIONED` sets the billing mode to [Provisioned Mode](https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/HowItWorks.ReadWriteCapacityMode.html#HowItWorks.ProvisionedThroughput.Manual)\.
+  `PAY_PER_REQUEST` \- We recommend using `PAY_PER_REQUEST` for unpredictable workloads\. `PAY_PER_REQUEST` sets the billing mode to [On\-Demand Mode](https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/HowItWorks.ReadWriteCapacityMode.html#HowItWorks.OnDemand)\. 
If not specified, the default is `PROVISIONED`\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`GlobalSecondaryIndexes`  <a name="cfn-dynamodb-table-gsi"></a>
Global secondary indexes to be created on the table\. You can create up to 20 global secondary indexes\.  
If you update a table to include a new global secondary index, AWS CloudFormation initiates the index creation and then proceeds with the stack update\. AWS CloudFormation doesn't wait for the index to complete creation because the backfilling phase can take a long time, depending on the size of the table\. You can't use the index or update the table until the index's status is `ACTIVE`\. You can track its status by using the DynamoDB [DescribeTable](https://docs.aws.amazon.com/cli/latest/reference/dynamodb/describe-table.html) command\.  
If you add or delete an index during an update, we recommend that you don't update any other resources\. If your stack fails to update and is rolled back while adding a new index, you must manually delete the index\.   
 Updates are not supported\. The following are exceptions:  
+ If you update only the provisioned throughput values of global secondary indexes, you can update the table without interruption\.
+ You can delete or add one global secondary index without interruption\. If you do both in the same update \(for example, by changing the index's logical ID\), the update fails\.
*Required*: No  
*Type*: List of [GlobalSecondaryIndex](aws-properties-dynamodb-gsi.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`KeySchema`  <a name="cfn-dynamodb-table-keyschema"></a>
Specifies the attributes that make up the primary key for the table\. The attributes in the `KeySchema` property must also be defined in the `AttributeDefinitions` property\.  
*Required*: Yes  
*Type*: [List](aws-properties-dynamodb-keyschema.md) of [KeySchema](aws-properties-dynamodb-keyschema.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`LocalSecondaryIndexes`  <a name="cfn-dynamodb-table-lsi"></a>
Local secondary indexes to be created on the table\. You can create up to 5 local secondary indexes\. Each index is scoped to a given hash key value\. The size of each hash key can be up to 10 gigabytes\.  
*Required*: No  
*Type*: List of [LocalSecondaryIndex](aws-properties-dynamodb-lsi.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`PointInTimeRecoverySpecification`  <a name="cfn-dynamodb-table-pointintimerecoveryspecification"></a>
The settings used to enable point in time recover\.  
*Required*: No  
*Type*: [PointInTimeRecoverySpecification](aws-properties-dynamodb-table-pointintimerecoveryspecification.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ProvisionedThroughput`  <a name="cfn-dynamodb-table-provisionedthroughput"></a>
Throughput for the specified table, which consists of values for `ReadCapacityUnits` and `WriteCapacityUnits`\. For more information about the contents of a provisioned throughput structure, see [Amazon DynamoDB Table ProvisionedThroughput](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-dynamodb-provisionedthroughput.html)\.   
If you set `BillingMode` as `PROVISIONED`, you must specify this property\. If you set `BillingMode` as `PAY_PER_REQUEST`, you cannot specify this property\.  
*Required*: Conditional  
*Type*: [ProvisionedThroughput](aws-properties-dynamodb-provisionedthroughput.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SSESpecification`  <a name="cfn-dynamodb-table-ssespecification"></a>
Specifies the settings to enable server\-side encryption\.  
*Required*: No  
*Type*: [SSESpecification](aws-properties-dynamodb-table-ssespecification.md)  
*Update requires*: [Some interruptions](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-some-interrupt)

`StreamSpecification`  <a name="cfn-dynamodb-table-streamspecification"></a>
The settings for the DynamoDB table stream, which capture changes to items stored in the table\.  
*Required*: No  
*Type*: [StreamSpecification](aws-properties-dynamodb-streamspecification.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TableName`  <a name="cfn-dynamodb-table-tablename"></a>
A name for the table\. If you don't specify a name, AWS CloudFormation generates a unique physical ID and uses that ID for the table name\. For more information, see [Name Type](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-name.html)\.  
If you specify a name, you cannot perform updates that require replacement of this resource\. You can perform updates that require no or some interruption\. If you must replace the resource, specify a new name\. 
*Required*: No  
*Type*: String  
*Minimum*: `3`  
*Maximum*: `255`  
*Pattern*: `[a-zA-Z0-9_.-]+`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-dynamodb-table-tags"></a>
An array of key\-value pairs to apply to this resource\.  
For more information, see [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TimeToLiveSpecification`  <a name="cfn-dynamodb-table-timetolivespecification"></a>
Specifies the Time to Live \(TTL\) settings for the table\.  
For detailed information about the limits in DynamoDB, see [Limits in Amazon DynamoDB](https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/Limits.html) in the Amazon DynamoDB Developer Guide\. 
*Required*: No  
*Type*: [TimeToLiveSpecification](aws-properties-dynamodb-timetolivespecification.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-dynamodb-table-return-values"></a>

### Ref<a name="aws-resource-dynamodb-table-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the resource name\. For example:

```
{ "Ref": "MyResource" }
```

For the resource with the logical ID `myDynamoDBTable`, `Ref` will return the DynamoDB table name\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-dynamodb-table-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-dynamodb-table-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the DynamoDB table, such as `arn:aws:dynamodb:us-east-2:123456789012:table/myDynamoDBTable`\.

`StreamArn`  <a name="StreamArn-fn::getatt"></a>
The ARN of the DynamoDB stream, such as `arn:aws:dynamodb:us-east-1:123456789012:table/testddbstack-myDynamoDBTable-012A1SL7SMP5Q/stream/2015-11-30T20:10:00.000`\.   
You must specify the `StreamSpecification` property to use this attribute\.

## Examples<a name="aws-resource-dynamodb-table--examples"></a>

### DynamoDB Table with Local and Secondary Indexes<a name="aws-resource-dynamodb-table--examples--DynamoDB_Table_with_Local_and_Secondary_Indexes"></a>

The following sample creates a DynamoDB table with `Album`, `Artist`, `Sales`, `NumberOfSongs` as attributes\. The primary key includes the `Album` attribute as the hash key and `Artist` attribute as the range key\. The table also includes two global and one secondary index\. For querying the number of sales for a given artist, the global secondary index uses the `Sales` attribute as the hash key and the `Artist` attribute as the range key\.

For querying the sales based on the number of songs, the global secondary index uses the `NumberOfSongs` attribute as the hash key and the `Sales` attribute as the range key\.

For querying the sales of an album, the local secondary index uses the same hash key as the table but uses the `Sales` attribute as the range key\.

#### JSON<a name="aws-resource-dynamodb-table--examples--DynamoDB_Table_with_Local_and_Secondary_Indexes--json"></a>

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

#### YAML<a name="aws-resource-dynamodb-table--examples--DynamoDB_Table_with_Local_and_Secondary_Indexes--yaml"></a>

```
AWSTemplateFormatVersion: "2010-09-09"
Resources: 
  myDynamoDBTable: 
    Type: AWS::DynamoDB::Table
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

### DynamoDB Table with a DependsOn Attribute<a name="aws-resource-dynamodb-table--examples--DynamoDB_Table_with_a_DependsOn_Attribute"></a>

If you include multiple DynamoDB tables with indexes in a single template, you must include dependencies so that the tables are created sequentially\. DynamoDB limits the number of tables with secondary indexes that are in the creating state\. If you create multiple tables with indexes at the same time, DynamoDB returns an error and the stack operation fails\.

The following sample assumes that the `myFirstDDBTable` table is declared in the same template as the `mySecondDDBTable` table, and both tables include a secondary index\. The `mySecondDDBTable` table includes a dependency on the `myFirstDDBTable` table so that AWS CloudFormation creates the tables one at a time\. 

#### JSON<a name="aws-resource-dynamodb-table--examples--DynamoDB_Table_with_a_DependsOn_Attribute--json"></a>

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

#### YAML<a name="aws-resource-dynamodb-table--examples--DynamoDB_Table_with_a_DependsOn_Attribute--yaml"></a>

```
mySecondDDBTable: 
  Type: AWS::DynamoDB::Table
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

### DynamoDB Table with Application Auto Scaling<a name="aws-resource-dynamodb-table--examples--DynamoDB_Table_with_Application_Auto_Scaling"></a>

This example sets up Application Auto Scaling for a `AWS::DynamoDB::Table` resource\. The template defines a `TargetTrackingScaling` scaling policy that scales up the `WriteCapacityUnits` throughput for the table\. 

#### JSON<a name="aws-resource-dynamodb-table--examples--DynamoDB_Table_with_Application_Auto_Scaling--json"></a>

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

#### YAML<a name="aws-resource-dynamodb-table--examples--DynamoDB_Table_with_Application_Auto_Scaling--yaml"></a>

```
Resources:
  DDBTable:
    Type: AWS::DynamoDB::Table
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
    Type: AWS::ApplicationAutoScaling::ScalableTarget
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
    Type: AWS::IAM::Role
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
    Type: AWS::ApplicationAutoScaling::ScalingPolicy
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