# AWS::Athena::WorkGroup<a name="aws-resource-athena-workgroup"></a>

The AWS::Athena::WorkGroup resource specifies an Amazon Athena workgroup, which contains a name, description, creation time, state, and other configuration, listed under [WorkGroupConfiguration](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-athena-workgroup.html#cfn-athena-workgroup-workgroupconfiguration)\. Each workgroup enables you to isolate queries for you or your group from other queries in the same account\. For more information, see [CreateWorkGroup](https://docs.aws.amazon.com/athena/latest/APIReference/API_CreateWorkGroup.html) in the *Amazon Athena API Reference*\.

## Syntax<a name="aws-resource-athena-workgroup-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-athena-workgroup-syntax.json"></a>

```
{
  "Type" : "AWS::Athena::WorkGroup",
  "Properties" : {
      "[Description](#cfn-athena-workgroup-description)" : String,
      "[Name](#cfn-athena-workgroup-name)" : String,
      "[RecursiveDeleteOption](#cfn-athena-workgroup-recursivedeleteoption)" : Boolean,
      "[State](#cfn-athena-workgroup-state)" : String,
      "[Tags](#cfn-athena-workgroup-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ],
      "[WorkGroupConfiguration](#cfn-athena-workgroup-workgroupconfiguration)" : WorkGroupConfiguration
    }
}
```

### YAML<a name="aws-resource-athena-workgroup-syntax.yaml"></a>

```
Type: AWS::Athena::WorkGroup
Properties: 
  [Description](#cfn-athena-workgroup-description): String
  [Name](#cfn-athena-workgroup-name): String
  [RecursiveDeleteOption](#cfn-athena-workgroup-recursivedeleteoption): Boolean
  [State](#cfn-athena-workgroup-state): String
  [Tags](#cfn-athena-workgroup-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
  [WorkGroupConfiguration](#cfn-athena-workgroup-workgroupconfiguration): 
    WorkGroupConfiguration
```

## Properties<a name="aws-resource-athena-workgroup-properties"></a>

`Description`  <a name="cfn-athena-workgroup-description"></a>
The workgroup description\.  
*Required*: No  
*Type*: String  
*Minimum*: `0`  
*Maximum*: `1024`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-athena-workgroup-name"></a>
The workgroup name\.  
*Required*: Yes  
*Type*: String  
*Pattern*: `[a-zA-Z0-9._-]{1,128}`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`RecursiveDeleteOption`  <a name="cfn-athena-workgroup-recursivedeleteoption"></a>
The option to delete a workgroup and its contents even if the workgroup contains any named queries\. The default is false\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`State`  <a name="cfn-athena-workgroup-state"></a>
The state of the workgroup: ENABLED or DISABLED\.  
*Required*: No  
*Type*: String  
*Allowed values*: `DISABLED | ENABLED`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-athena-workgroup-tags"></a>
The tags \(key\-value pairs\) to associate with this resource\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`WorkGroupConfiguration`  <a name="cfn-athena-workgroup-workgroupconfiguration"></a>
The configuration of the workgroup, which includes the location in Amazon S3 where query results are stored, the encryption option, if any, used for query results, whether Amazon CloudWatch Metrics are enabled for the workgroup, and the limit for the amount of bytes scanned \(cutoff\) per query, if it is specified\. The [EnforceWorkGroupConfiguration](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-athena-workgroup-workgroupconfiguration.html#cfn-athena-workgroup-workgroupconfiguration-enforceworkgroupconfiguration) option determines whether workgroup settings override client\-side query settings\.  
*Required*: No  
*Type*: [WorkGroupConfiguration](aws-properties-athena-workgroup-workgroupconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-athena-workgroup-return-values"></a>

### Ref<a name="aws-resource-athena-workgroup-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the name of the WorkGroup\. For example:

 `{ "Ref": "myWorkGroup" }` 

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-athena-workgroup-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-athena-workgroup-return-values-fn--getatt-fn--getatt"></a>

`CreationTime`  <a name="CreationTime-fn::getatt"></a>
The date and time the workgroup was created, as a UNIX timestamp in seconds\. For example: `1582761016`\.

`WorkGroupConfiguration.EngineVersion.EffectiveEngineVersion`  <a name="WorkGroupConfiguration.EngineVersion.EffectiveEngineVersion-fn::getatt"></a>
Property description not available\.

## Examples<a name="aws-resource-athena-workgroup--examples"></a>

### Creating an Athena WorkGroup<a name="aws-resource-athena-workgroup--examples--Creating_an_Athena_WorkGroup"></a>

The following example template creates the Athena WorkGroup `MyCustomWorkGroup`\. Note the use of `WorkGroupConfiguration` to specify the configuration for the WorkGroup\.

#### YAML<a name="aws-resource-athena-workgroup--examples--Creating_an_Athena_WorkGroup--yaml"></a>

```
Resources:
  MyAthenaWorkGroup:
    Type: AWS::Athena::WorkGroup
    Properties:
      Name: MyCustomWorkGroup
      Description: My WorkGroup
      State: ENABLED
      Tags:
        - Key: "key1"
          Value: "value1"
        - Key: "key2"
          Value: "value2"
      WorkGroupConfiguration:
        BytesScannedCutoffPerQuery: 200000000
        EnforceWorkGroupConfiguration: false
        PublishCloudWatchMetricsEnabled: false
        RequesterPaysEnabled: true
        ResultConfiguration:
          OutputLocation: s3://path/to/my/bucket/
```

#### JSON<a name="aws-resource-athena-workgroup--examples--Creating_an_Athena_WorkGroup--json"></a>

```
{
    "Resources":{
        "MyAthenaWorkGroup":{
            "Type":"AWS::Athena::WorkGroup",
            "Properties":{
                "Name":"MyCustomWorkGroup",
                "Description":"My WorkGroup",
                "State":"ENABLED",
                "Tags":[
                    {
                        "Key":"key1",
                        "Value":"value1"
                    },
                    {
                        "Key":"key2",
                        "Value":"value2"
                    }
                ],
                "WorkGroupConfiguration":{
                    "BytesScannedCutoffPerQuery":200000000,
                    "EnforceWorkGroupConfiguration":false,
                    "PublishCloudWatchMetricsEnabled":false,
                    "RequesterPaysEnabled":true,
                    "ResultConfiguration":{
                        "OutputLocation":"s3://path/to/my/bucket/"
                    }
                }
            }
        }
    }
}
```

### Updating an Athena WorkGroup<a name="aws-resource-athena-workgroup--examples--Updating_an_Athena_WorkGroup"></a>

The following example template updates the Athena WorkGroup `MyCustomWorkGroup`\. Note the use of `WorkGroupConfigurationUpdates` instead of `WorkGroupConfiguration`\.

#### YAML<a name="aws-resource-athena-workgroup--examples--Updating_an_Athena_WorkGroup--yaml"></a>

```
Resources:
  MyAthenaWorkGroup:
    Type: AWS::Athena::WorkGroup
    Properties:
      Name: MyCustomWorkGroup
      Description: My WorkGroup Updated
      State: DISABLED
      Tags:
        - Key: "key1"
          Value: "value1"
        - Key: "key2"
          Value: "value2"
      WorkGroupConfigurationUpdates:
        BytesScannedCutoffPerQuery: 10000000
        EnforceWorkGroupConfiguration: true
        PublishCloudWatchMetricsEnabled: true
        RequesterPaysEnabled: false
        ResultConfigurationUpdates:
          EncryptionConfiguration:
            EncryptionOption: SSE_S3
          OutputLocation: s3://path/to/my/bucket/updated/
```

#### JSON<a name="aws-resource-athena-workgroup--examples--Updating_an_Athena_WorkGroup--json"></a>

```
{
    "Resources":{
        "MyAthenaWorkGroup":{
            "Type":"AWS::Athena::WorkGroup",
            "Properties":{
                "Name":"MyCustomWorkGroup",
                "Description":"My WorkGroup Updated",
                "State":"DISABLED",
                "Tags":[
                    {
                        "Key":"key1",
                        "Value":"value1"
                    },
                    {
                        "Key":"key2",
                        "Value":"value2"
                    }
                ],
                "WorkGroupConfigurationUpdates":{
                    "BytesScannedCutoffPerQuery":10000000,
                    "EnforceWorkGroupConfiguration":true,
                    "PublishCloudWatchMetricsEnabled":true,
                    "RequesterPaysEnabled":false,
                    "ResultConfigurationUpdates":{
                        "EncryptionConfiguration":{
                            "EncryptionOption":"SSE_S3"
                        },
                        "OutputLocation":"s3://path/to/my/bucket/updated/"
                    }
                }
            }
        }
    }
}
```