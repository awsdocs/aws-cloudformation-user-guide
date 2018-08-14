# AWS::Config::ConfigRule<a name="aws-resource-config-configrule"></a>

The `AWS::Config::ConfigRule` resource uses an AWS Lambda \(Lambda\) function that evaluates configuration items to assess whether your AWS resources comply with your specified configurations\. This function can run when AWS Config detects a configuration change or delivers a configuration snapshot\. The resources this function evaluates must be in the recording group\. For more information, see [Evaluating AWS Resource Configurations with AWS Config](http://docs.aws.amazon.com/config/latest/developerguide/evaluate-config.html) in the *AWS Config Developer Guide*\.

**Topics**
+ [Syntax](#aws-resource-config-configrule-syntax)
+ [Properties](#w3ab2c21c10d304b9)
+ [Return Values](#w3ab2c21c10d304c11)
+ [Examples](#w3ab2c21c10d304c13)

## Syntax<a name="aws-resource-config-configrule-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-config-configrule-syntax.json"></a>

```
{
  "Type" : "AWS::Config::ConfigRule",
  "Properties" : {
    "[ConfigRuleName](#cfn-config-configrule-configrulename)" : String,
    "[Description](#cfn-config-configrule-description)" : String,
    "[InputParameters](#cfn-config-configrule-inputparameters)" : { ParameterName : Value },
    "[MaximumExecutionFrequency](#cfn-config-configrule-maximumexecutionfrequency)" : String,
    "[Scope](#cfn-config-configrule-scope)" : Scope,
    "[Source](#cfn-config-configrule-source)" : Source
  }
}
```

### YAML<a name="aws-resource-config-configrule-syntax.yaml"></a>

```
Type: "AWS::Config::ConfigRule"
Properties:
  [ConfigRuleName](#cfn-config-configrule-configrulename): String
  [Description](#cfn-config-configrule-description): String
  [InputParameters](#cfn-config-configrule-inputparameters):
    ParameterName : Value
  [MaximumExecutionFrequency](#cfn-config-configrule-maximumexecutionfrequency): String
  [Scope](#cfn-config-configrule-scope):
    Scope
  [Source](#cfn-config-configrule-source):
    Source
```

## Properties<a name="w3ab2c21c10d304b9"></a>

`ConfigRuleName`  <a name="cfn-config-configrule-configrulename"></a>
A name for the AWS Config rule\. If you don't specify a name, AWS CloudFormation generates a unique physical ID and uses that ID for the rule name\. For more information, see [Name Type](aws-properties-name.md)\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`Description`  <a name="cfn-config-configrule-description"></a>
A description about this AWS Config rule\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`InputParameters`  <a name="cfn-config-configrule-inputparameters"></a>
Input parameter values that are passed to the AWS Config rule \(Lambda function\)\.  
*Required*: No  
*Type*: JSON object  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`MaximumExecutionFrequency`  <a name="cfn-config-configrule-maximumexecutionfrequency"></a>
The maximum frequency at which the AWS Config rule runs evaluations\. For valid values, see the [ConfigRule](http://docs.aws.amazon.com/config/latest/APIReference/API_ConfigRule.html) data type in the *AWS Config API Reference*\.  
If the rule runs an evaluation when AWS Config delivers a configuration snapshot, the rule cannot run more frequently than the snapshot delivery frequency\. Set an execution frequency value that is equal to or greater than the value of the snapshot delivery frequency, which is a property the [AWS::Config::DeliveryChannel](aws-resource-config-deliverychannel.md) resource\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`Scope`  <a name="cfn-config-configrule-scope"></a>
Defines which AWS resources will trigger an evaluation when their configurations change\. The scope can include one or more resource types, a combination of a tag key and value, or a combination of one resource type and one resource ID\. Specify a scope to constrain the resources that are evaluated\. If you don't specify a scope, the rule evaluates all resources in the recording group\.  
*Required*: No  
*Type*: [AWS Config ConfigRule Scope](aws-properties-config-configrule-scope.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`Source`  <a name="cfn-config-configrule-source"></a>
Specifies the rule owner, the rule identifier, and the events that cause the function to evaluate your AWS resources\.  
*Required*: Yes  
*Type*: [AWS Config ConfigRule Source](aws-properties-config-configrule-source.md)  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

## Return Values<a name="w3ab2c21c10d304c11"></a>

### Ref<a name="w3ab2c21c10d304c11b2"></a>

When you pass the logical ID of an `AWS::Config::ConfigRule` resource to the intrinsic `Ref` function, the function returns the rule name, such as `mystack-MyConfigRule-12ABCFPXHV4OV`\.

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\.

### Fn::GetAtt<a name="w3ab2c21c10d304c11b4"></a>

`Fn::GetAtt` returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

`Arn`  
The Amazon Resource Name \(ARN\) of the AWS Config rule, such as `arn:aws:config:us-east-1:123456789012:config-rule/config-rule-a1bzhi`\.

`ConfigRuleId`  
The ID of the AWS Config rule, such as `config-rule-a1bzhi`\.

`Compliance.Type`  
The compliance status of an AWS Config rule, such as `COMPLIANT` or `NON_COMPLIANT`\.

For more information about using `Fn::GetAtt`, see [Fn::GetAtt](intrinsic-function-reference-getatt.md)\.

## Examples<a name="w3ab2c21c10d304c13"></a>

### <a name="w3ab2c21c10d304c13b2"></a>

The following example uses an AWS managed rule that checks whether EC2 volumes resource types have a `CostCenter` tag\.

#### JSON<a name="aws-resource-config-configrule-example1.json"></a>

```
"ConfigRuleForVolumeTags": {
  "Type": "AWS::Config::ConfigRule",
  "Properties": {
    "InputParameters": {"tag1Key": "CostCenter"},
    "Scope": {
      "ComplianceResourceTypes": ["AWS::EC2::Volume"]
    },
    "Source": {
      "Owner": "AWS",
      "SourceIdentifier": "REQUIRED_TAGS"
    }
  }
}
```

#### YAML<a name="aws-resource-config-configrule-example1.yaml"></a>

```
ConfigRuleForVolumeTags: 
  Type: "AWS::Config::ConfigRule"
  Properties: 
    InputParameters: 
      tag1Key: CostCenter
    Scope: 
      ComplianceResourceTypes: 
        - "AWS::EC2::Volume"
    Source: 
      Owner: AWS
      SourceIdentifier: "REQUIRED_TAGS"
```

### Rule Using Lambda Function<a name="w3ab2c21c10d304c13b4"></a>

The following example creates a custom configuration rule that uses a Lambda function\. The function checks whether an EC2 volume has the `AutoEnableIO` property set to true\. Note that the configuration rule has a dependency on the Lambda policy so that the rule calls the function only after it's permitted to do so\.

#### JSON<a name="aws-resource-config-configrule-example2.json"></a>

```
"ConfigPermissionToCallLambda": {
  "Type": "AWS::Lambda::Permission",
  "Properties": {
    "FunctionName": {"Fn::GetAtt": ["VolumeAutoEnableIOComplianceCheck", "Arn"]},
    "Action": "lambda:InvokeFunction",
    "Principal": "config.amazonaws.com"
  }
},
"VolumeAutoEnableIOComplianceCheck": {
  "Type": "AWS::Lambda::Function",
  "Properties": {
    "Code": {
      "ZipFile":  {"Fn::Join": ["\n", [
        "var aws  = require('aws-sdk');",
        "var config = new aws.ConfigService();",
        "var ec2 = new aws.EC2();",

        "exports.handler = function(event, context) {",
        "    compliance = evaluateCompliance(event, function(compliance, event) {",
        "        var configurationItem = JSON.parse(event.invokingEvent).configurationItem;",

        "        var putEvaluationsRequest = {",
        "            Evaluations: [{",
        "                ComplianceResourceType: configurationItem.resourceType,",
        "                ComplianceResourceId: configurationItem.resourceId,",
        "                ComplianceType: compliance,",
        "                OrderingTimestamp: configurationItem.configurationItemCaptureTime",
        "            }],",
        "            ResultToken: event.resultToken",
        "        };",

        "        config.putEvaluations(putEvaluationsRequest, function(err, data) {",
        "            if (err) context.fail(err);",
        "            else context.succeed(data);",
        "        });",
        "    });",
        "};",

        "function evaluateCompliance(event, doReturn) {",
        "    var configurationItem = JSON.parse(event.invokingEvent).configurationItem;",
        "    var status = configurationItem.configurationItemStatus;",
        "    if (configurationItem.resourceType !== 'AWS::EC2::Volume' || event.eventLeftScope || (status !== 'OK' && status !== 'ResourceDiscovered'))",
        "        doReturn('NOT_APPLICABLE', event);",
        "    else ec2.describeVolumeAttribute({VolumeId: configurationItem.resourceId, Attribute: 'autoEnableIO'}, function(err, data) {",
        "        if (err) context.fail(err);",
        "        else if (data.AutoEnableIO.Value) doReturn('COMPLIANT', event);",
        "        else doReturn('NON_COMPLIANT', event);",
        "    });",
        "}"
      ]]}
    },
    "Handler": "index.handler",
    "Runtime": "nodejs4.3",
    "Timeout": "30",
    "Role": {"Fn::GetAtt": ["LambdaExecutionRole", "Arn"]}
  }
},
"ConfigRuleForVolumeAutoEnableIO": {
  "Type": "AWS::Config::ConfigRule",
  "Properties": {
    "ConfigRuleName": "ConfigRuleForVolumeAutoEnableIO",
    "Scope": {
      "ComplianceResourceId": {"Ref": "Ec2Volume"},
      "ComplianceResourceTypes": ["AWS::EC2::Volume"]
    },
    "Source": {
      "Owner": "CUSTOM_LAMBDA",
      "SourceDetails": [{
          "EventSource": "aws.config",
          "MessageType": "ConfigurationItemChangeNotification"
      }],
      "SourceIdentifier": {"Fn::GetAtt": ["VolumeAutoEnableIOComplianceCheck", "Arn"]}
    }
  },
  "DependsOn": "ConfigPermissionToCallLambda"
}
```

#### YAML<a name="aws-resource-config-configrule-example2.yaml"></a>

```
ConfigPermissionToCallLambda: 
  Type: "AWS::Lambda::Permission"
  Properties: 
    FunctionName: 
      Fn::GetAtt: 
        - VolumeAutoEnableIOComplianceCheck
        - Arn
    Action: "lambda:InvokeFunction"
    Principal: "config.amazonaws.com"
VolumeAutoEnableIOComplianceCheck: 
  Type: "AWS::Lambda::Function"
  Properties: 
    Code: 
      ZipFile: 
        !Sub |
          var aws  = require('aws-sdk');
          var config = new aws.ConfigService();
          var ec2 = new aws.EC2();
          exports.handler = function(event, context) {
              compliance = evaluateCompliance(event, function(compliance, event) {
                    var configurationItem = JSON.parse(event.invokingEvent).configurationItem;
                    var putEvaluationsRequest = {
                        Evaluations: [{
                            ComplianceResourceType: configurationItem.resourceType,
                            ComplianceResourceId: configurationItem.resourceId,
                            ComplianceType: compliance,
                            OrderingTimestamp: configurationItem.configurationItemCaptureTime
                        }],
                        ResultToken: event.resultToken
                    };
                    config.putEvaluations(putEvaluationsRequest, function(err, data) {
                        if (err) context.fail(err);
                        else context.succeed(data);
                    });
                });
            };
            function evaluateCompliance(event, doReturn) {
                var configurationItem = JSON.parse(event.invokingEvent).configurationItem;
                var status = configurationItem.configurationItemStatus;
                if (configurationItem.resourceType !== 'AWS::EC2::Volume' || event.eventLeftScope || (status !== 'OK' && status !== 'ResourceDiscovered'))
                    doReturn('NOT_APPLICABLE', event);
                else ec2.describeVolumeAttribute({VolumeId: configurationItem.resourceId, Attribute: 'autoEnableIO'}, function(err, data) {
                    if (err) context.fail(err);
                    else if (data.AutoEnableIO.Value) doReturn('COMPLIANT', event);
                    else doReturn('NON_COMPLIANT', event);
                });
            }
    Handler: "index.handler"
    Runtime: nodejs4.3
    Timeout: 30
    Role: 
      Fn::GetAtt: 
        - LambdaExecutionRole
        - Arn
ConfigRuleForVolumeAutoEnableIO: 
  Type: "AWS::Config::ConfigRule"
  Properties: 
    ConfigRuleName: ConfigRuleForVolumeAutoEnableIO
    Scope: 
      ComplianceResourceId: 
        Ref: Ec2Volume
      ComplianceResourceTypes: 
        - "AWS::EC2::Volume"
    Source: 
      Owner: "CUSTOM_LAMBDA"
      SourceDetails: 
        - 
          EventSource: "aws.config"
          MessageType: "ConfigurationItemChangeNotification"
      SourceIdentifier: 
        Fn::GetAtt: 
          - VolumeAutoEnableIOComplianceCheck
          - Arn
  DependsOn: ConfigPermissionToCallLambda
```