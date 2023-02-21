# AWS::APS::Workspace<a name="aws-resource-aps-workspace"></a>

The `AWS::APS::Workspace` type specifies an Amazon Managed Service for Prometheus \(Amazon Managed Service for Prometheus\) workspace\. A *workspace* is a logical and isolated Prometheus server dedicated to Prometheus resources such as metrics\. You can have one or more workspaces in each Region in your account\.

## Syntax<a name="aws-resource-aps-workspace-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-aps-workspace-syntax.json"></a>

```
{
  "Type" : "AWS::APS::Workspace",
  "Properties" : {
      "[AlertManagerDefinition](#cfn-aps-workspace-alertmanagerdefinition)" : String,
      "[Alias](#cfn-aps-workspace-alias)" : String,
      "[LoggingConfiguration](#cfn-aps-workspace-loggingconfiguration)" : LoggingConfiguration,
      "[Tags](#cfn-aps-workspace-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-aps-workspace-syntax.yaml"></a>

```
Type: AWS::APS::Workspace
Properties: 
  [AlertManagerDefinition](#cfn-aps-workspace-alertmanagerdefinition): String
  [Alias](#cfn-aps-workspace-alias): String
  [LoggingConfiguration](#cfn-aps-workspace-loggingconfiguration): 
    LoggingConfiguration
  [Tags](#cfn-aps-workspace-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-aps-workspace-properties"></a>

`AlertManagerDefinition`  <a name="cfn-aps-workspace-alertmanagerdefinition"></a>
The alert manager definition for the workspace, as a string\. For more information, see [ Alert manager and templating](https://docs.aws.amazon.com/prometheus/latest/userguide/AMP-alert-manager.html)\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Alias`  <a name="cfn-aps-workspace-alias"></a>
An alias that you assign to this workspace to help you identify it\. It does not need to be unique\.  
 The alias can be as many as 100 characters and can include any type of characters\. Amazon Managed Service for Prometheus automatically strips any blank spaces from the beginning and end of the alias that you specify\.   
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LoggingConfiguration`  <a name="cfn-aps-workspace-loggingconfiguration"></a>
The LoggingConfiguration attribute is used to set the logging configuration for the workspace\.  
*Required*: No  
*Type*: [LoggingConfiguration](aws-properties-aps-workspace-loggingconfiguration.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-aps-workspace-tags"></a>
A list of tag keys and values to associate with the workspace\.   
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-aps-workspace-return-values"></a>

### Ref<a name="aws-resource-aps-workspace-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the ARN of the workspace\. For example, `arn:aws:aps:us-west-2:123456789012:workspace/ws-EXAMPLE-3687-4ac9-853c-EXAMPLEe8f`\. 

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-aps-workspace-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-aps-workspace-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The ARN of the workspace\. For example: `arn:aws:aps:us-west-2:123456789012:workspace/ws-EXAMPLE-3687-4ac9-853c-EXAMPLEe8f`\.

`PrometheusEndpoint`  <a name="PrometheusEndpoint-fn::getatt"></a>
The Prometheus endpoint attribute of the workspace\. This is the endpoint prefix without the remote\_write or query API appended\. For example: `https://aps-workspaces.us-west-2.amazonaws.com/workspaces/ws-EXAMPLE-3687-4ac9-853c-EXAMPLEe8f/`\.

`WorkspaceId`  <a name="WorkspaceId-fn::getatt"></a>
The workspace ID\. For example: `ws-EXAMPLE-3687-4ac9-853c-EXAMPLEe8f`\.

## Examples<a name="aws-resource-aps-workspace--examples"></a>

### Amazon Managed Service for Prometheus workspace example<a name="aws-resource-aps-workspace--examples--_workspace_example"></a>

The following example creates an Amazon Managed Service for Prometheus workspace with an alias and one tag\.

#### JSON<a name="aws-resource-aps-workspace--examples--_workspace_example--json"></a>

```
{
    "Resources": {
        "APSWorkspace": {
            "Type": "AWS::APS::Workspace",
            "Properties": {
                "Alias": "TestWorkspace"
                "Tags": [
                    {
                        "Key": "BusinessPurpose",
                        "Value": "LoadTesting"
                    }
                ]
            }
        }
    }
}
```

#### YAML<a name="aws-resource-aps-workspace--examples--_workspace_example--yaml"></a>

```
Resources:
  APSWorkspace:
    Type: AWS::APS::Workspace
    Properties:
      Alias: TestWorkspace
      Tags:
      - Key: BusinessPurpose
        Value: LoadTesting
```

### Amazon Managed Service for Prometheus logging configuration example<a name="aws-resource-aps-workspace--examples--_logging_configuration_example"></a>

The following example creates a new workspace and sets a new logging configuration\.

#### JSON<a name="aws-resource-aps-workspace--examples--_logging_configuration_example--json"></a>

```
{
    "Resources": {
        "APSWorkspace": {
            "Type": "AWS::APS::Workspace",
            "Properties": {
                "Alias": "TestWorkspace",
                "LoggingConfiguration": {
                    "LogGroupArn": "arn:aws:logs:{region}:{account}:log-group:test-log-group:*"
                },
                "Tags": [
                    {
                        "Key": "BusinessPurpose",
                        "Value": "LoadTesting"
                    }
                ]
            }
        }
    }
}
```

#### YAML<a name="aws-resource-aps-workspace--examples--_logging_configuration_example--yaml"></a>

```
Resources:
  APSWorkspace:
    Type: AWS::APS::Workspace
    Properties:
      Alias: TestWorkspace
      LoggingConfiguration:
        LogGroupArn: "arn:aws:logs:{region}:{account}:log-group:test-log-group:*"
      Tags:
        - Key: BusinessPurpose
          Value: LoadTesting
```