# AWS::ApplicationInsights::Application<a name="aws-resource-applicationinsights-application"></a>

The `AWS::ApplicationInsights::Application` resource adds an application that is created from a resource group\.

## Syntax<a name="aws-resource-applicationinsights-application-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-applicationinsights-application-syntax.json"></a>

```
{
  "Type" : "AWS::ApplicationInsights::Application",
  "Properties" : {
      "[AutoConfigurationEnabled](#cfn-applicationinsights-application-autoconfigurationenabled)" : Boolean,
      "[ComponentMonitoringSettings](#cfn-applicationinsights-application-componentmonitoringsettings)" : [ ComponentMonitoringSetting, ... ],
      "[CustomComponents](#cfn-applicationinsights-application-customcomponents)" : [ CustomComponent, ... ],
      "[CWEMonitorEnabled](#cfn-applicationinsights-application-cwemonitorenabled)" : Boolean,
      "[LogPatternSets](#cfn-applicationinsights-application-logpatternsets)" : [ LogPatternSet, ... ],
      "[OpsCenterEnabled](#cfn-applicationinsights-application-opscenterenabled)" : Boolean,
      "[OpsItemSNSTopicArn](#cfn-applicationinsights-application-opsitemsnstopicarn)" : String,
      "[ResourceGroupName](#cfn-applicationinsights-application-resourcegroupname)" : String,
      "[Tags](#cfn-applicationinsights-application-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-applicationinsights-application-syntax.yaml"></a>

```
Type: AWS::ApplicationInsights::Application
Properties: 
  [AutoConfigurationEnabled](#cfn-applicationinsights-application-autoconfigurationenabled): Boolean
  [ComponentMonitoringSettings](#cfn-applicationinsights-application-componentmonitoringsettings): 
    - ComponentMonitoringSetting
  [CustomComponents](#cfn-applicationinsights-application-customcomponents): 
    - CustomComponent
  [CWEMonitorEnabled](#cfn-applicationinsights-application-cwemonitorenabled): Boolean
  [LogPatternSets](#cfn-applicationinsights-application-logpatternsets): 
    - LogPatternSet
  [OpsCenterEnabled](#cfn-applicationinsights-application-opscenterenabled): Boolean
  [OpsItemSNSTopicArn](#cfn-applicationinsights-application-opsitemsnstopicarn): String
  [ResourceGroupName](#cfn-applicationinsights-application-resourcegroupname): String
  [Tags](#cfn-applicationinsights-application-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-applicationinsights-application-properties"></a>

`AutoConfigurationEnabled`  <a name="cfn-applicationinsights-application-autoconfigurationenabled"></a>
If set to `true`, the application components will be configured with the monitoring configuration recommended by Application Insights\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ComponentMonitoringSettings`  <a name="cfn-applicationinsights-application-componentmonitoringsettings"></a>
The monitoring settings of the components\.  
*Required*: No  
*Type*: List of [ComponentMonitoringSetting](aws-properties-applicationinsights-application-componentmonitoringsetting.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CustomComponents`  <a name="cfn-applicationinsights-application-customcomponents"></a>
Describes a custom component by grouping similar standalone instances to monitor\.  
*Required*: No  
*Type*: List of [CustomComponent](aws-properties-applicationinsights-application-customcomponent.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`CWEMonitorEnabled`  <a name="cfn-applicationinsights-application-cwemonitorenabled"></a>
 Indicates whether Application Insights can listen to CloudWatch events for the application resources, such as `instance terminated`, `failed deployment`, and others\.   
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LogPatternSets`  <a name="cfn-applicationinsights-application-logpatternsets"></a>
The log pattern sets\.  
*Required*: No  
*Type*: List of [LogPatternSet](aws-properties-applicationinsights-application-logpatternset.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`OpsCenterEnabled`  <a name="cfn-applicationinsights-application-opscenterenabled"></a>
 Indicates whether Application Insights will create OpsItems for any problem that is detected by Application Insights for an application\.   
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`OpsItemSNSTopicArn`  <a name="cfn-applicationinsights-application-opsitemsnstopicarn"></a>
 The SNS topic provided to Application Insights that is associated with the created OpsItems to receive SNS notifications for opsItem updates\.   
*Required*: No  
*Type*: String  
*Minimum*: `20`  
*Maximum*: `300`  
*Pattern*: `^arn:aws(-\w+)?:[\w\d-]+:([\w\d-]*)?:[\w\d_-]*([:/].+)*$`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ResourceGroupName`  <a name="cfn-applicationinsights-application-resourcegroupname"></a>
The name of the resource group used for the application\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `256`  
*Pattern*: `[a-zA-Z0-9\.\-_]*`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-applicationinsights-application-tags"></a>
An array of `Tags`\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-applicationinsights-application-return-values"></a>

### Ref<a name="aws-resource-applicationinsights-application-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the Amazon Resource Name \(ARN\) of the application, such as `arn:aws:applicationinsights:us-east-1:123456789012:application/resource-group/my_resource_group`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-applicationinsights-application-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-applicationinsights-application-return-values-fn--getatt-fn--getatt"></a>

`ApplicationARN`  <a name="ApplicationARN-fn::getatt"></a>
Returns the Amazon Resource Name \(ARN\) of the application, such as ` arn:aws:applicationinsights:us-east-1:123456789012:application/resource-group/my_resource_group`\.

## Examples<a name="aws-resource-applicationinsights-application--examples"></a>



### The following example template creates an Application Insights application with all components configured with recommended monitoring settings<a name="aws-resource-applicationinsights-application--examples--The_following_example_template_creates_an_Application_Insights_application_with_all_components_configured_with_recommended_monitoring_settings"></a>

The following example template performs the following actions:
+ Creates an Application Insights application\. For more information, see [CreateApplication](https://docs.aws.amazon.com/appinsights/latest/APIReference/API_CreateApplication.html) in the *Amazon CloudWatch Application Insights API Reference*\.
+ Sets `AutoConfigurationEnabled` to `true`, which configures all components of the application with the recommended monitoring settings for the `DEFAULT` tier\. For more information, see [DescribeComponentConfigurationRecommendation](https://docs.aws.amazon.com/appinsights/latest/APIReference/API_DescribeComponentConfigurationRecommendation.html) in the *Amazon CloudWatch Application Insights API Reference*\.

#### YAML<a name="aws-resource-applicationinsights-application--examples--The_following_example_template_creates_an_Application_Insights_application_with_all_components_configured_with_recommended_monitoring_settings--yaml"></a>

```
---
Type: AWS::ApplicationInsights::Application
Properties:
  ResourceGroupName: my_resource_group
  AutoConfigurationEnabled: true
```

#### JSON<a name="aws-resource-applicationinsights-application--examples--The_following_example_template_creates_an_Application_Insights_application_with_all_components_configured_with_recommended_monitoring_settings--json"></a>

```
{
    "Type": "AWS::ApplicationInsights::Application",
    "Properties": {
        "ResourceGroupName": "my_resource_group",
        "AutoConfigurationEnabled": true
    }
}
```

### The following example template creates an Application Insights application with detailed settings<a name="aws-resource-applicationinsights-application--examples--The_following_example_template_creates_an_Application_Insights_application_with_detailed_settings"></a>

The following example template performs the following actions:
+ Creates an Application Insights application with CloudWatch Events notification and OpsCenter enabled\. For more information, see [CreateApplication](https://docs.aws.amazon.com/appinsights/latest/APIReference/API_CreateApplication.html) in the *Amazon CloudWatch Application Insights API Reference*\.
+ Tags the application with two tags, one of which has no tag values\. For more information, see [TagResource](https://docs.aws.amazon.com/appinsights/latest/APIReference/API_TagResource.html) in the *Amazon CloudWatch Application Insights API Reference*\.
+ Creates two custom instance group components\. For more information, see [CreateComponent](https://docs.aws.amazon.com/appinsights/latest/APIReference/API_CreateComponent.html) in the *Amazon CloudWatch Application Insights API Reference*\.
+ Creates two log pattern sets\. For more information, see [CreateLogPattern](https://docs.aws.amazon.com/appinsights/latest/APIReference/API_CreateLogPattern.html) in the *Amazon CloudWatch Application Insights API Reference*\.
+ Sets `AutoConfigurationEnabled` to `true`, which configures all components of the application with the recommended monitoring settings for the `DEFAULT` tier\. For more information, see [DescribeComponentConfigurationRecommendation](https://docs.aws.amazon.com/appinsights/latest/APIReference/API_DescribeComponentConfigurationRecommendation.html) in the *Amazon CloudWatch Application Insights API Reference*\.

#### YAML<a name="aws-resource-applicationinsights-application--examples--The_following_example_template_creates_an_Application_Insights_application_with_detailed_settings--yaml"></a>

```
---
Type: AWS::ApplicationInsights::Application
Properties:
  ResourceGroupName: my_resource_group
  CWEMonitorEnabled: true
  OpsCenterEnabled: true
  OpsItemSNSTopicArn: arn:aws:sns:us-east-1:123456789012:my_topic
  AutoConfigurationEnabled: true
  Tags:
  - Key: key1
    Value: value1
  - Key: key2
    Value: ''
  CustomComponents:
  - ComponentName: test_component_1
    ResourceList:
    - arn:aws:ec2:us-east-1:123456789012:instance/i-XXXXX
  - ComponentName: test_component_2
    ResourceList:
    - arn:aws:ec2:us-east-1:123456789012:instance/i-YYYYY
    - arn:aws:ec2:us-east-1:123456789012:instance/i-ZZZZZ
  LogPatternSets:
  - PatternSetName: pattern_set_1
    LogPatterns:
    - PatternName: deadlock_pattern
      Pattern: ".*\\sDeadlocked\\sSchedulers(([^\\w].*)|($))"
      Rank: 1
  - PatternSetName: pattern_set_2
    LogPatterns:
    - PatternName: error_pattern
      Pattern: ".*[\\s\\[]ERROR[\\s\\]].*"
      Rank: 1
    - PatternName: warning_pattern
      Pattern: ".*[\\s\\[]WARN(ING)?[\\s\\]].*"
      Rank: 10
```

#### JSON<a name="aws-resource-applicationinsights-application--examples--The_following_example_template_creates_an_Application_Insights_application_with_detailed_settings--json"></a>

```
{
    "Type": "AWS::ApplicationInsights::Application",
    "Properties": {
        "ResourceGroupName": "my_resource_group",
        "CWEMonitorEnabled": true,
        "OpsCenterEnabled": true,
        "OpsItemSNSTopicArn": "arn:aws:sns:us-east-1:123456789012:my_topic",
        "AutoConfigurationEnabled": true,
        "Tags": [
            {
                "Key": "key1",
                "Value": "value1"
            },
            {
                "Key": "key2",
                "Value": ""
            }
        ],
        "CustomComponents": [
            {
                "ComponentName": "test_component_1",
                "ResourceList": [
                    "arn:aws:ec2:us-east-1:123456789012:instance/i-XXXXX"
                ]
            },
            {
                "ComponentName": "test_component_2",
                "ResourceList": [
                    "arn:aws:ec2:us-east-1:123456789012:instance/i-YYYYY",
                    "arn:aws:ec2:us-east-1:123456789012:instance/i-ZZZZZ"
                ]
            }
        ],
        "LogPatternSets": [
            {
                "PatternSetName": "pattern_set_1",
                "LogPatterns": [
                    {
                        "PatternName": "deadlock_pattern",
                        "Pattern": ".*\\sDeadlocked\\sSchedulers(([^\\w].*)|($))",
                        "Rank": 1
                    }
                ]    
            },
            {
                "PatternSetName": "pattern_set_2",
                "LogPatterns": [
                    {
                        "PatternName": "error_pattern",
                        "Pattern": ".*[\\s\\[]ERROR[\\s\\]].*",
                        "Rank": 1
                    },
                    {
                        "PatternName": "warning_pattern",
                        "Pattern": ".*[\\s\\[]WARN(ING)?[\\s\\]].*",
                        "Rank": 10
                    }
                ]
            }
        ]
    }
}
```

### The following example template creates an Application Insights application with CUSTOM mode component configuration<a name="aws-resource-applicationinsights-application--examples--The_following_example_template_creates_an_Application_Insights_application_with_CUSTOM_mode_component_configuration"></a>

The following example template performs the following actions:
+ Creates an Application Insights application\. For more information, see [CreateApplication](https://docs.aws.amazon.com/appinsights/latest/APIReference/API_CreateApplication.html) in the *Amazon CloudWatch Application Insights API Reference*\.
+ Component `my_component` sets `ComponentConfigurationMode` to `CUSTOM`, which causes this component to be configured as specified in `CustomComponentConfiguration`\. For more information, see [UpdateComponentConfiguration](https://docs.aws.amazon.com/appinsights/latest/APIReference/API_UpdateComponentConfiguration.html) in the *Amazon CloudWatch Application Insights API Reference*\.

#### YAML<a name="aws-resource-applicationinsights-application--examples--The_following_example_template_creates_an_Application_Insights_application_with_CUSTOM_mode_component_configuration--yaml"></a>

```
---
Type: AWS::ApplicationInsights::Application
Properties:
  ResourceGroupName: my_resource_group
  ComponentMonitoringSettings:
  - ComponentARN: my_component
    Tier: SQL_SERVER
    ComponentConfigurationMode: CUSTOM
    CustomComponentConfiguration:
      ConfigurationDetails:
        AlarmMetrics:
        - AlarmMetricName: StatusCheckFailed
        ...
        Logs:
        - LogGroupName: my_log_group_1
          LogPath: C:\LogFolder_1\*
          LogType: DOT_NET_CORE
          Encoding: utf-8
          PatternSet: my_pattern_set_1
        ...
        WindowsEvents:
        - LogGroupName: my_windows_event_log_group_1
          EventName: Application
          EventLevels:
          - ERROR
          - WARNING
          ...
          Encoding: utf-8
          PatternSet: my_pattern_set_2
        ...
        Alarms:
        - AlarmName: my_alarm_name
          Severity: HIGH
        ...
      SubComponentTypeConfigurations:
      - SubComponentType: EC2_INSTANCE
        SubComponentConfigurationDetails:
          AlarmMetrics:
          - AlarmMetricName: DiskReadOps
          ...
          Logs:
          - LogGroupName: my_log_group_2
            LogPath: C:\LogFolder_2\*
            LogType: IIS
            Encoding: utf-8
            PatternSet: my_pattern_set_3
          ...
          WindowsEvents:
          - LogGroupName: my_windows_event_log_group_2
            EventName: Application
            EventLevels:
            - ERROR
            - WARNING
            ...
            Encoding: utf-8
            PatternSet: my_pattern_set_4
          ...
```

#### JSON<a name="aws-resource-applicationinsights-application--examples--The_following_example_template_creates_an_Application_Insights_application_with_CUSTOM_mode_component_configuration--json"></a>

```
{
    "Type": "AWS::ApplicationInsights::Application",
    "Properties": {
        "ResourceGroupName": "my_resource_group",
        "ComponentMonitoringSettings": [
            {
                "ComponentARN": "my_component",
                "Tier": "SQL_SERVER",
                "ComponentConfigurationMode": "CUSTOM",
                "CustomComponentConfiguration": {
                    "ConfigurationDetails": {
                        "AlarmMetrics": [
                            {
                                "AlarmMetricName": "StatusCheckFailed"
                            },
                            ...
                        ],
                        "Logs": [
                            {       
                                "LogGroupName": "my_log_group_1",
                                "LogPath": "C:\\LogFolder_1\\*",
                                "LogType": "DOT_NET_CORE",
                                "Encoding": "utf-8",
                                "PatternSet": "my_pattern_set_1"
                            },      
                            ...     
                        ],      
                        "WindowsEvents": [
                            {       
                                "LogGroupName": "my_windows_event_log_group_1",
                                "EventName": "Application",
                                "EventLevels": [
                                    "ERROR",
                                    "WARNING",
                                    ...     
                                ],       
                                "Encoding": "utf-8",
                                "PatternSet": "my_pattern_set_2"
                            },      
                            ...     
                        ],
                        "Alarms": [
                            {
                                "AlarmName": "my_alarm_name",
                                "Severity": "HIGH"
                            },
                            ...
                        ]
                    },
                    "SubComponentTypeConfigurations": [
                        {
                            "SubComponentType": "EC2_INSTANCE",
                            "SubComponentConfigurationDetails": {
                                "AlarmMetrics": [
                                    {
                                        "AlarmMetricName": "DiskReadOps"
                                    },
                                    ...
                                ],
                                "Logs": [
                                    {
                                        "LogGroupName": "my_log_group_2",
                                        "LogPath": "C:\\LogFolder_2\\*",
                                        "LogType": "IIS",
                                        "Encoding": "utf-8",
                                        "PatternSet": "my_pattern_set_3"
                                    },
                                    ...
                                ],
                                "WindowsEvents": [
                                    {
                                        "LogGroupName": "my_windows_event_log_group_2",
                                        "EventName": "Application",
                                        "EventLevels": [
                                            "ERROR",
                                            "WARNING",
                                            ...
                                        ],
                                        "Encoding": "utf-8",
                                        "PatternSet": "my_pattern_set_4"
                                    },
                                    ...
                                ]
                            }
                        }   
                    ]
                }
            }
        ]
    }
}
```

### The following example template creates an Application Insights application with DEFAULT mode component configuration<a name="aws-resource-applicationinsights-application--examples--The_following_example_template_creates_an_Application_Insights_application_with_DEFAULT_mode_component_configuration"></a>

The following example template performs the following actions:
+ Creates an Application Insights application\. For more information, see [CreateApplication](https://docs.aws.amazon.com/appinsights/latest/APIReference/API_CreateApplication.html) in the *Amazon CloudWatch Application Insights API Reference*\.
+ Component `my_component` sets `ComponentConfigurationMode` to `DEFAULT` and `Tier` to `SQL_SERVER`, which causes this component to be configured with the configuration settings that Application Insights recommends for the `SQL_Server` tier\. For more information, see [DescribeComponentConfiguration](https://docs.aws.amazon.com/appinsights/latest/APIReference/API_DescribeComponentConfiguration.html) and [UpdateComponentConfiguration](https://docs.aws.amazon.com/appinsights/latest/APIReference/API_UpdateComponentConfiguration.html) in the *Amazon CloudWatch Application Insights API Reference*\.

#### YAML<a name="aws-resource-applicationinsights-application--examples--The_following_example_template_creates_an_Application_Insights_application_with_DEFAULT_mode_component_configuration--yaml"></a>

```
---
Type: AWS::ApplicationInsights::Application
Properties:
  ResourceGroupName: my_resource_group
  ComponentMonitoringSettings:
  - ComponentARN: my_component
    Tier: SQL_SERVER
    ComponentConfigurationMode: DEFAULT
```

#### JSON<a name="aws-resource-applicationinsights-application--examples--The_following_example_template_creates_an_Application_Insights_application_with_DEFAULT_mode_component_configuration--json"></a>

```
{
    "Type": "AWS::ApplicationInsights::Application",
    "Properties": {
        "ResourceGroupName": "my_resource_group",
        "ComponentMonitoringSettings": [
            {
                "ComponentARN": "my_component",
                "Tier": "SQL_SERVER",
                "ComponentConfigurationMode": "DEFAULT"
            }
        ]
    }
}
```

### The following example template creates an Application Insights application with DEFAULT\_WITH\_OVERWRITE mode component configuration<a name="aws-resource-applicationinsights-application--examples--The_following_example_template_creates_an_Application_Insights_application_with_DEFAULT_WITH_OVERWRITE_mode_component_configuration"></a>

The following example template performs the following actions:
+ Creates an Application Insights application\. For more information, see [CreateApplication](https://docs.aws.amazon.com/appinsights/latest/APIReference/API_CreateApplication.html) in the *Amazon CloudWatch Application Insights API Reference*\.
+ Component `my_component` sets `ComponentConfigurationMode` to `DEFAULT_WITH_OVERWRITE` and `tier` to `DOT_NET_CORE`, which causes this component to be configured with the configuration settings that Application Insights recommends for the `DOT_NET_CORE` tier\. Overwritten configuration settings are specified in the `DefaultOverwriteComponentConfiguration`: 
  + At the component level, `AlarmMetrics` settings are overwritten\.
  + At the sub\-component level, for the `EC2_Instance` type sub\-components, `Logs` settings are overwritten\.

  For more information, see [UpdateComponentConfiguration](https://docs.aws.amazon.com/appinsights/latest/APIReference/API_UpdateComponentConfiguration.html) in the *Amazon CloudWatch Application Insights API Reference*\.

#### YAML<a name="aws-resource-applicationinsights-application--examples--The_following_example_template_creates_an_Application_Insights_application_with_DEFAULT_WITH_OVERWRITE_mode_component_configuration--yaml"></a>

```
---
Type: AWS::ApplicationInsights::Application
Properties:
  ResourceGroupName: my_resource_group
  ComponentMonitoringSettings:
  - ComponentName: my_component
    Tier: DOT_NET_CORE
    ComponentConfigurationMode: DEFAULT_WITH_OVERWRITE
    DefaultOverwriteComponentConfiguration:
      ConfigurationDetails:
        AlarmMetrics:
        - AlarmMetricName: StatusCheckFailed
      SubComponentTypeConfigurations:
      - SubComponentType: EC2_INSTANCE
        SubComponentConfigurationDetails:
          Logs:
          - LogGroupName: my_log_group
            LogPath: C:\LogFolder\*
            LogType: IIS
            Encoding: utf-8
            PatternSet: my_pattern_set
```

#### JSON<a name="aws-resource-applicationinsights-application--examples--The_following_example_template_creates_an_Application_Insights_application_with_DEFAULT_WITH_OVERWRITE_mode_component_configuration--json"></a>

```
{
    "Type": "AWS::ApplicationInsights::Application",
    "Properties": {
        "ResourceGroupName": "my_resource_group",
        "ComponentMonitoringSettings": [
            {
                "ComponentName": "my_component",
                "Tier": "DOT_NET_CORE",
                "ComponentConfigurationMode": "DEFAULT_WITH_OVERWRITE",
                "DefaultOverwriteComponentConfiguration": {
                    "ConfigurationDetails": {
                        "AlarmMetrics": [
                            {
                                "AlarmMetricName": "StatusCheckFailed"
                            }
                        ]
                    },
                    "SubComponentTypeConfigurations": [
                        {
                            "SubComponentType": "EC2_INSTANCE",
                            "SubComponentConfigurationDetails": {
                                "Logs": [
                                    {
                                        "LogGroupName": "my_log_group",
                                        "LogPath": "C:\\LogFolder\\*",
                                        "LogType": "IIS",
                                        "Encoding": "utf-8",
                                        "PatternSet": "my_pattern_set"
                                    }
                                ]
                            }
                        }   
                    ] 
                } 
            }
        ]
    }
}
```