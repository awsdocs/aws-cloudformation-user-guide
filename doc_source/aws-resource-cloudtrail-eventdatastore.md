# AWS::CloudTrail::EventDataStore<a name="aws-resource-cloudtrail-eventdatastore"></a>

Creates a new event data store\.

## Syntax<a name="aws-resource-cloudtrail-eventdatastore-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-cloudtrail-eventdatastore-syntax.json"></a>

```
{
  "Type" : "AWS::CloudTrail::EventDataStore",
  "Properties" : {
      "[AdvancedEventSelectors](#cfn-cloudtrail-eventdatastore-advancedeventselectors)" : [ AdvancedEventSelector, ... ],
      "[KmsKeyId](#cfn-cloudtrail-eventdatastore-kmskeyid)" : String,
      "[MultiRegionEnabled](#cfn-cloudtrail-eventdatastore-multiregionenabled)" : Boolean,
      "[Name](#cfn-cloudtrail-eventdatastore-name)" : String,
      "[OrganizationEnabled](#cfn-cloudtrail-eventdatastore-organizationenabled)" : Boolean,
      "[RetentionPeriod](#cfn-cloudtrail-eventdatastore-retentionperiod)" : Integer,
      "[Tags](#cfn-cloudtrail-eventdatastore-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ],
      "[TerminationProtectionEnabled](#cfn-cloudtrail-eventdatastore-terminationprotectionenabled)" : Boolean
    }
}
```

### YAML<a name="aws-resource-cloudtrail-eventdatastore-syntax.yaml"></a>

```
Type: AWS::CloudTrail::EventDataStore
Properties: 
  [AdvancedEventSelectors](#cfn-cloudtrail-eventdatastore-advancedeventselectors): 
    - AdvancedEventSelector
  [KmsKeyId](#cfn-cloudtrail-eventdatastore-kmskeyid): String
  [MultiRegionEnabled](#cfn-cloudtrail-eventdatastore-multiregionenabled): Boolean
  [Name](#cfn-cloudtrail-eventdatastore-name): String
  [OrganizationEnabled](#cfn-cloudtrail-eventdatastore-organizationenabled): Boolean
  [RetentionPeriod](#cfn-cloudtrail-eventdatastore-retentionperiod): Integer
  [Tags](#cfn-cloudtrail-eventdatastore-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
  [TerminationProtectionEnabled](#cfn-cloudtrail-eventdatastore-terminationprotectionenabled): Boolean
```

## Properties<a name="aws-resource-cloudtrail-eventdatastore-properties"></a>

`AdvancedEventSelectors`  <a name="cfn-cloudtrail-eventdatastore-advancedeventselectors"></a>
The advanced event selectors to use to select the events for the data store\. You can configure up to five advanced event selectors for each event data store\.  
 For more information about how to use advanced event selectors to log CloudTrail events, see [Log events by using advanced event selectors](https://docs.aws.amazon.com/awscloudtrail/latest/userguide/logging-data-events-with-cloudtrail.html#creating-data-event-selectors-advanced) in the CloudTrail User Guide\.  
For more information about how to use advanced event selectors to include AWS Config configuration items in your event data store, see [Create an event data store for AWS Config configuration items](https://docs.aws.amazon.com/awscloudtrail/latest/userguide/query-lake-cli.html#lake-cli-create-eds-config) in the CloudTrail User Guide\.  
For more information about how to use advanced event selectors to include non\-AWS events in your event data store, see [Create an integration to log events from outside AWS](https://docs.aws.amazon.com/awscloudtrail/latest/userguide/query-lake-cli.html#lake-cli-create-integration) in the CloudTrail User Guide\.  
*Required*: No  
*Type*: List of [AdvancedEventSelector](aws-properties-cloudtrail-eventdatastore-advancedeventselector.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`KmsKeyId`  <a name="cfn-cloudtrail-eventdatastore-kmskeyid"></a>
Specifies the AWS KMS key ID to use to encrypt the events delivered by CloudTrail\. The value can be an alias name prefixed by `alias/`, a fully specified ARN to an alias, a fully specified ARN to a key, or a globally unique identifier\.  
Disabling or deleting the KMS key, or removing CloudTrail permissions on the key, prevents CloudTrail from logging events to the event data store, and prevents users from querying the data in the event data store that was encrypted with the key\. After you associate an event data store with a KMS key, the KMS key cannot be removed or changed\. Before you disable or delete a KMS key that you are using with an event data store, delete or back up your event data store\.
CloudTrail also supports AWS KMS multi\-Region keys\. For more information about multi\-Region keys, see [Using multi\-Region keys](https://docs.aws.amazon.com/kms/latest/developerguide/multi-region-keys-overview.html) in the * AWS Key Management Service Developer Guide*\.  
Examples:  
+  `alias/MyAliasName` 
+  `arn:aws:kms:us-east-2:123456789012:alias/MyAliasName` 
+  `arn:aws:kms:us-east-2:123456789012:key/12345678-1234-1234-1234-123456789012` 
+  `12345678-1234-1234-1234-123456789012` 
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `350`  
*Pattern*: `^[a-zA-Z0-9._/\-:]+$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`MultiRegionEnabled`  <a name="cfn-cloudtrail-eventdatastore-multiregionenabled"></a>
Specifies whether the event data store includes events from all regions, or only from the region in which the event data store is created\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-cloudtrail-eventdatastore-name"></a>
The name of the event data store\.  
*Required*: No  
*Type*: String  
*Minimum*: `3`  
*Maximum*: `128`  
*Pattern*: `^[a-zA-Z0-9._\-]+$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`OrganizationEnabled`  <a name="cfn-cloudtrail-eventdatastore-organizationenabled"></a>
Specifies whether an event data store collects events logged for an organization in AWS Organizations\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RetentionPeriod`  <a name="cfn-cloudtrail-eventdatastore-retentionperiod"></a>
The retention period of the event data store, in days\. You can set a retention period of up to 2557 days, the equivalent of seven years\.  
*Required*: No  
*Type*: Integer  
*Minimum*: `7`  
*Maximum*: `2557`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-cloudtrail-eventdatastore-tags"></a>
A list of tags\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Maximum*: `200`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TerminationProtectionEnabled`  <a name="cfn-cloudtrail-eventdatastore-terminationprotectionenabled"></a>
Specifies whether termination protection is enabled for the event data store\. If termination protection is enabled, you cannot delete the event data store until termination protection is disabled\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-cloudtrail-eventdatastore-return-values"></a>

### Ref<a name="aws-resource-cloudtrail-eventdatastore-return-values-ref"></a>

When the logical ID of this resource is provided to the Ref intrinsic function, `Ref` returns the resource name\. 

### Fn::GetAtt<a name="aws-resource-cloudtrail-eventdatastore-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-cloudtrail-eventdatastore-return-values-fn--getatt-fn--getatt"></a>

`CreatedTimestamp`  <a name="CreatedTimestamp-fn::getatt"></a>
When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the time stamp of the creation of the event data store, such as `1248496624`\.

`EventDataStoreArn`  <a name="EventDataStoreArn-fn::getatt"></a>
 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the ARN of the CloudTrail event data store, such as `arn:aws:cloudtrail:us-east-1:12345678910:eventdatastore/EXAMPLE-f852-4e8f-8bd1-bcf6cEXAMPLE`\.

`Status`  <a name="Status-fn::getatt"></a>
When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the status of the event data store, such as `ENABLED`\.

`UpdatedTimestamp`  <a name="UpdatedTimestamp-fn::getatt"></a>
When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the time stamp that updates were made to an event data store, such as `1598296624`\.

## Examples<a name="aws-resource-cloudtrail-eventdatastore--examples"></a>

### Example<a name="aws-resource-cloudtrail-eventdatastore--examples--Example"></a>

The following example creates an event data store that logs events in all regions\. For information about CloudTrail Lake event data stores, see [Working with CloudTrail Lake](https://docs.aws.amazon.com/awscloudtrail/latest/userguide/cloudtrail-lake.html) in the *AWS CloudTrail User Guide*\.

#### JSON<a name="aws-resource-cloudtrail-eventdatastore--examples--Example--json"></a>

```
{
    "Parameters": {
        "Name": {
            "Type": "String"
        }
    },
    "Conditions": {
        "IsOrganizationsSupported": {
            "Fn::Not": [
                {
                    "Fn::Equals": [
                        {
                            "Ref": "AWS::Partition"
                        },
                        "aws-cn"
                    ]
                }
            ]
        }
    },
    "Resources": {
        "myEventDataStore": {
            "Type": "AWS::CloudTrail::EventDataStore",
            "Properties": {
                "Name": {
                    "Ref": "Name"
                },
                "MultiRegionEnabled": true,
                "RetentionPeriod": 30,
                "OrganizationEnabled": {
                    "Fn::If": [
                        "IsOrganizationsSupported",
                        true,
                        {
                            "Ref": "AWS::NoValue"
                        }
                    ]
                },
                "TerminationProtectionEnabled": false,
                "KmsKeyId": {
                    "Fn::ImportValue": "EventDataStoreKeyTest"
                },
                "Tags": [
                    {
                        "Key": "TagKeyIntTest",
                        "Value": "TagValueIntTest"
                    },
                    {
                        "Key": "TagKeyIntTest2",
                        "Value": "TagValueIntTest2"
                    }
                ],
                "AdvancedEventSelectors": [
                    {
                        "Name": "AdvancedEventSelectors1",
                        "FieldSelectors": [
                            {
                                "Field": "eventCategory",
                                "Equals": [
                                    "Management"
                                ]
                            }
                        ]
                    }
                ]
            }
        }
    },
    "Outputs": {
        "myEventDataStoreArn": {
            "Description": "The event data store ARN",
            "Value": {
                "Fn::GetAtt": [
                    "myEventDataStore",
                    "EventDataStoreArn"
                ]
            }
        }
    }
}
```

#### YAML<a name="aws-resource-cloudtrail-eventdatastore--examples--Example--yaml"></a>

```
Parameters:
  Name:
    Type: String
Conditions:
  IsOrganizationsSupported:
    !Not [!Equals [Ref: "AWS::Partition", "aws-cn"]]
Resources:
  myEventDataStore:
    Type: AWS::CloudTrail::EventDataStore
    Properties:
      Name: !Ref Name
      
      MultiRegionEnabled: true
      RetentionPeriod: 30
      OrganizationEnabled:
        Fn::If:
          - IsOrganizationsSupported
          - true
          - !Ref "AWS::NoValue"
      TerminationProtectionEnabled: false
      KmsKeyId:
        Fn::ImportValue: EventDataStoreKeyTest
      Tags:
        - Key: "TagKeyIntTest"
          Value: "TagValueIntTest"
        - Key: "TagKeyIntTest2"
          Value: "TagValueIntTest2"
      AdvancedEventSelectors:
        - Name: "AdvancedEventSelectors1"
          FieldSelectors:
          - Field: "eventCategory"
            Equals: [ "Management" ]
Outputs:
  myEventDataStoreArn:
    Description: The eventdatastore ARN
    Value:
      'Fn::GetAtt':
        - myEventDataStore
        - EventDataStoreArn
```