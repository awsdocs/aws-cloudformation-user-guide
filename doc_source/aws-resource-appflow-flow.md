# AWS::AppFlow::Flow<a name="aws-resource-appflow-flow"></a>

 The `AWS::AppFlow::Flow` resource is an Amazon AppFlow resource type that specifies a new flow\. 

**Note**  
If you want to use AWS CloudFormation to create a connector profile for connectors that implement OAuth \(such as Salesforce, Slack, Zendesk, and Google Analytics\), you must fetch the access and refresh tokens\. You can do this by implementing your own UI for OAuth, or by retrieving the tokens from elsewhere\. Alternatively, you can use the Amazon AppFlow console to create the connector profile, and then use that connector profile in the flow creation CloudFormation template\. 

## Syntax<a name="aws-resource-appflow-flow-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-appflow-flow-syntax.json"></a>

```
{
  "Type" : "AWS::AppFlow::Flow",
  "Properties" : {
      "[Description](#cfn-appflow-flow-description)" : String,
      "[DestinationFlowConfigList](#cfn-appflow-flow-destinationflowconfiglist)" : [ DestinationFlowConfig, ... ],
      "[FlowName](#cfn-appflow-flow-flowname)" : String,
      "[KMSArn](#cfn-appflow-flow-kmsarn)" : String,
      "[SourceFlowConfig](#cfn-appflow-flow-sourceflowconfig)" : SourceFlowConfig,
      "[Tags](#cfn-appflow-flow-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ],
      "[Tasks](#cfn-appflow-flow-tasks)" : [ Task, ... ],
      "[TriggerConfig](#cfn-appflow-flow-triggerconfig)" : TriggerConfig
    }
}
```

### YAML<a name="aws-resource-appflow-flow-syntax.yaml"></a>

```
Type: AWS::AppFlow::Flow
Properties: 
  [Description](#cfn-appflow-flow-description): String
  [DestinationFlowConfigList](#cfn-appflow-flow-destinationflowconfiglist): 
    - DestinationFlowConfig
  [FlowName](#cfn-appflow-flow-flowname): String
  [KMSArn](#cfn-appflow-flow-kmsarn): String
  [SourceFlowConfig](#cfn-appflow-flow-sourceflowconfig): 
    SourceFlowConfig
  [Tags](#cfn-appflow-flow-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
  [Tasks](#cfn-appflow-flow-tasks): 
    - Task
  [TriggerConfig](#cfn-appflow-flow-triggerconfig): 
    TriggerConfig
```

## Properties<a name="aws-resource-appflow-flow-properties"></a>

`Description`  <a name="cfn-appflow-flow-description"></a>
 A user\-entered description of the flow\.   
*Required*: No  
*Type*: String  
*Maximum*: `2048`  
*Pattern*: `[\w!@#\-.?,\s]*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`DestinationFlowConfigList`  <a name="cfn-appflow-flow-destinationflowconfiglist"></a>
 The configuration that controls how Amazon AppFlow places data in the destination connector\.   
*Required*: Yes  
*Type*: List of [DestinationFlowConfig](aws-properties-appflow-flow-destinationflowconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FlowName`  <a name="cfn-appflow-flow-flowname"></a>
 The specified name of the flow\. Spaces are not allowed\. Use underscores \(\_\) or hyphens \(\-\) only\.   
*Required*: Yes  
*Type*: String  
*Maximum*: `256`  
*Pattern*: `[a-zA-Z0-9][\w!@#.-]+`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`KMSArn`  <a name="cfn-appflow-flow-kmsarn"></a>
 The ARN \(Amazon Resource Name\) of the Key Management Service \(KMS\) key you provide for encryption\. This is required if you do not want to use the Amazon AppFlow\-managed KMS key\. If you don't provide anything here, Amazon AppFlow uses the Amazon AppFlow\-managed KMS key\.   
*Required*: No  
*Type*: String  
*Minimum*: `20`  
*Maximum*: `2048`  
*Pattern*: `arn:aws:kms:.*:[0-9]+:.*`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SourceFlowConfig`  <a name="cfn-appflow-flow-sourceflowconfig"></a>
 Contains information about the configuration of the source connector used in the flow\.   
*Required*: Yes  
*Type*: [SourceFlowConfig](aws-properties-appflow-flow-sourceflowconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-appflow-flow-tags"></a>
 The tags used to organize, track, or control access for your flow\.   
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tasks`  <a name="cfn-appflow-flow-tasks"></a>
 A list of tasks that Amazon AppFlow performs while transferring the data in the flow run\.   
*Required*: Yes  
*Type*: List of [Task](aws-properties-appflow-flow-task.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TriggerConfig`  <a name="cfn-appflow-flow-triggerconfig"></a>
 The trigger settings that determine how and when Amazon AppFlow runs the specified flow\.   
*Required*: Yes  
*Type*: [TriggerConfig](aws-properties-appflow-flow-triggerconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-appflow-flow-return-values"></a>

### Ref<a name="aws-resource-appflow-flow-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the flow name\. For example:

            `{ "Ref": "myFlowName" }`        

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-appflow-flow-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-appflow-flow-return-values-fn--getatt-fn--getatt"></a>

`FlowArn`  <a name="FlowArn-fn::getatt"></a>
The flow's Amazon Resource Name \(ARN\)\.

## Examples<a name="aws-resource-appflow-flow--examples"></a>



### Test flow for CloudFormation from Salesforce to Amazon S3<a name="aws-resource-appflow-flow--examples--Test_flow_for_CloudFormation_from_Salesforce_to_Amazon_S3"></a>

The following example shows a test event flow for CloudFormation using Salesforce as the source and Amazon S3 as the destination\.

#### JSON<a name="aws-resource-appflow-flow--examples--Test_flow_for_CloudFormation_from_Salesforce_to_Amazon_S3--json"></a>

```
{
    "AWSTemplateFormatVersion":"2010-09-09",
    "Resources": {
        "TestFlow": {
            "Type": "AWS::AppFlow::Flow",
            "Properties": {
                "flowName": "MyEventFlow",
                "description": "Test event flow for CloudFormation from salesforce to s3",
                "triggerConfig": {
                    "triggerType": "Event"
                 },
                "sourceFlowConfig": {
                    "connectorType": "Salesforce",
                    "connectorProfileName": "TestConnectorProfile",
                    "sourceConnectorProperties": {
                        "Salesforce": {
                            "object": "Account",
                            "enableDynamicFieldUpdate": false,
                            "includeDeletedRecords": true
                        }
                    }
                },
                "destinationFlowConfigList": [
                    {
                        "connectorType": "S3",
                        "destinationConnectorProperties": {
                            "S3": {
                                "bucketName": "TestOutputBucket",
                                "s3OutputFormatConfig": {
                                    "fileType": "JSON",
                                    "aggregationConfig": {
                                        "aggregationType": "None"
                                    }
                                }
                            }
                        }
                    }
                ],
                "tasks": [
                    {
                        "taskType": "Filter",
                        "sourceFields": [
                            "Id",
                            "Name"
                        ],
                        "connectorOperator": {
"Salesforce": "PROJECTION"
                            }
                     },
                    {
                        "taskType": "Map",
                        "sourceFields": [
                            "Id"
                        ],
                        "taskProperties": [
                            {
                                "Key": "SOURCE_DATA_TYPE",
                                "Value": "id"
                            },
                             {
                                "Key": "DESTINATION_DATA_TYPE",
                                "Value": "id"
                            }
                        ],
                        "destinationField": "Id",
                        "connectorOperator": {
                            "Salesforce": "NO_OP"
                        }
                    },
                    {
                        "taskType": "Map",
                        "sourceFields": [
                            "Name"
                        ],
                        "taskProperties": [
                            {
                                "Key": "SOURCE_DATA_TYPE",
                                "Value": "string"
                            },
                            {
                                "Key": "DESTINATION_DATA_TYPE",
                                "Value": "string"
                            }
                        ],
                        "destinationField": "Name",
                        "connectorOperator": {
                            "Salesforce": "NO_OP"
                        }
                    }
                ],
                "tags": [
                    {
                        "Key": "testKey",
                        "Value": "testValue"
                    }
                ]
            }
        }
    }
}
```

#### YAML<a name="aws-resource-appflow-flow--examples--Test_flow_for_CloudFormation_from_Salesforce_to_Amazon_S3--yaml"></a>

```
AWSTemplateFormatVersion: '2010-09-09'
Resources:
  TestFlow:
    Type: AWS::AppFlow::Flow
    Properties:
      FlowName: MyEventFlow
      Description: Test flow for CloudFormation from salesforce to s3
      TriggerConfig:
        TriggerType: Event
      SourceFlowConfig:
        ConnectorType: Salesforce
        ConnectorProfileName: TestConnectorProfile
        SourceConnectorProperties:
          Salesforce:
            Object: Account
            EnableDynamicFieldUpdate: false
            IncludeDeletedRecords: true
      DestinationFlowConfigList:
        - ConnectorType: S3
          DestinationConnectorProperties:
            S3:
              BucketName: TestOutputBucket
              S3OutputFormatConfig:
                 FileType: JSON
                AggregationConfig:
                AggregationType: None
      Tasks:
        - TaskType: Filter
          ConnectorOperator:
            Salesforce: PROJECTION
          SourceFields:
            - Id
        - TaskType: Map
          SourceFields:
            - Id
          TaskProperties:
            - Key: SOURCE_DATA_TYPE
              Value: id
            - Key: DESTINATION_DATA_TYPE
              Value: id
          DestinationField: Id
          ConnectorOperator:
            Salesforce: NO_OP
        - TaskType: Map
          SourceFields:
            - Name
          TaskProperties:
            - Key: SOURCE_DATA_TYPE
              Value: string
            - Key: DESTINATION_DATA_TYPE
              Value: string
          DestinationField: Name
          ConnectorOperator:
            Salesforce: NO_OP
```

## See also<a name="aws-resource-appflow-flow--seealso"></a>
+ [CreateFlow](https://docs.aws.amazon.com/appflow/1.0/APIReference/API_CreateFlow.html) in the *Amazon AppFlow API Reference*\.
+ [DescribeFlow](https://docs.aws.amazon.com/appflow/1.0/APIReference/API_DescribeFlow.html) in the *Amazon AppFlow API Reference*\.
+ [DeleteFlow](https://docs.aws.amazon.com/appflow/1.0/APIReference/API_DeleteFlow.html) in the *Amazon AppFlow API Reference*\.
+ [UpdateFlow](https://docs.aws.amazon.com/appflow/1.0/APIReference/API_UpdateFlow.html) in the *Amazon AppFlow API Reference*\.

