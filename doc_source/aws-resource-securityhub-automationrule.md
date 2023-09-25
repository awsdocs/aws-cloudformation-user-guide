# AWS::SecurityHub::AutomationRule<a name="aws-resource-securityhub-automationrule"></a>

 The `AWS::SecurityHub::AutomationRule` resource specifies an automation rule based on input parameters\. For more information, see [Automation rules](https://docs.aws.amazon.com/securityhub/latest/userguide/automation-rules.html) in the *AWS Security Hub User Guide*\.

## Syntax<a name="aws-resource-securityhub-automationrule-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-securityhub-automationrule-syntax.json"></a>

```
{
  "Type" : "AWS::SecurityHub::AutomationRule",
  "Properties" : {
      "[Actions](#cfn-securityhub-automationrule-actions)" : [ AutomationRulesAction, ... ],
      "[Criteria](#cfn-securityhub-automationrule-criteria)" : AutomationRulesFindingFilters,
      "[Description](#cfn-securityhub-automationrule-description)" : String,
      "[IsTerminal](#cfn-securityhub-automationrule-isterminal)" : Boolean,
      "[RuleName](#cfn-securityhub-automationrule-rulename)" : String,
      "[RuleOrder](#cfn-securityhub-automationrule-ruleorder)" : Integer,
      "[RuleStatus](#cfn-securityhub-automationrule-rulestatus)" : String,
      "[Tags](#cfn-securityhub-automationrule-tags)" : {Key: Value, ...}
    }
}
```

### YAML<a name="aws-resource-securityhub-automationrule-syntax.yaml"></a>

```
Type: AWS::SecurityHub::AutomationRule
Properties:
  [Actions](#cfn-securityhub-automationrule-actions):
    - AutomationRulesAction
  [Criteria](#cfn-securityhub-automationrule-criteria):
    AutomationRulesFindingFilters
  [Description](#cfn-securityhub-automationrule-description): String
  [IsTerminal](#cfn-securityhub-automationrule-isterminal): Boolean
  [RuleName](#cfn-securityhub-automationrule-rulename): String
  [RuleOrder](#cfn-securityhub-automationrule-ruleorder): Integer
  [RuleStatus](#cfn-securityhub-automationrule-rulestatus): String
  [Tags](#cfn-securityhub-automationrule-tags):
    Key: Value
```

## Properties<a name="aws-resource-securityhub-automationrule-properties"></a>

`Actions`  <a name="cfn-securityhub-automationrule-actions"></a>
 One or more actions to update finding fields if a finding matches the conditions specified in `Criteria`\.
*Required*: Yes
*Type*: List of [AutomationRulesAction](aws-properties-securityhub-automationrule-automationrulesaction.md)
*Maximum*: `1`
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Criteria`  <a name="cfn-securityhub-automationrule-criteria"></a>
 A set of [AWS Security Finding Format \(ASFF\)](https://docs.aws.amazon.com/securityhub/latest/userguide/securityhub-findings-format.html) finding field attributes and corresponding expected values that Security Hub uses to filter findings\. If a rule is enabled and a finding matches the criteria specified in this parameter, Security Hub applies the rule action to the finding\.
*Required*: Yes
*Type*: [AutomationRulesFindingFilters](aws-properties-securityhub-automationrule-automationrulesfindingfilters.md)
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Description`  <a name="cfn-securityhub-automationrule-description"></a>
 A description of the rule\.
*Required*: Yes
*Type*: String
*Pattern*: `.*\S.*`
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IsTerminal`  <a name="cfn-securityhub-automationrule-isterminal"></a>
Specifies whether a rule is the last to be applied with respect to a finding that matches the rule criteria\. This is useful when a finding matches the criteria for multiple rules, and each rule has different actions\. If a rule is terminal, Security Hub applies the rule action to a finding that matches the rule criteria and doesn't evaluate other rules for the finding\. By default, a rule isn't terminal\.
*Required*: No
*Type*: Boolean
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RuleName`  <a name="cfn-securityhub-automationrule-rulename"></a>
 The name of the rule\.
*Required*: Yes
*Type*: String
*Pattern*: `.*\S.*`
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RuleOrder`  <a name="cfn-securityhub-automationrule-ruleorder"></a>
An integer ranging from 1 to 1000 that represents the order in which the rule action is applied to findings\. Security Hub applies rules with lower values for this parameter first\.
*Required*: Yes
*Type*: Integer
*Minimum*: `1`
*Maximum*: `1000`
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RuleStatus`  <a name="cfn-securityhub-automationrule-rulestatus"></a>
 Whether the rule is active after it is created\. If this parameter is equal to `ENABLED`, Security Hub applies the rule to findings and finding updates after the rule is created\.
*Required*: No
*Type*: String
*Allowed values*: `DISABLED | ENABLED`
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Tags`  <a name="cfn-securityhub-automationrule-tags"></a>
 User\-defined tags that help you label the purpose of a rule\.
*Required*: No
*Type*: Map of String
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-securityhub-automationrule-return-values"></a>

### Ref<a name="aws-resource-securityhub-automationrule-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref`function, `Ref`returns `RuleArn`\. For example, `arn:aws:securityhub:us-east-1:123456789012:automation-rule/a1b2c3d4-5678-90ab-cdef-EXAMPLE11111`\.

For more information about using the `Ref`function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-securityhub-automationrule-return-values-fn--getatt"></a>

The `Fn::GetAtt`intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt`intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-securityhub-automationrule-return-values-fn--getatt-fn--getatt"></a>

`CreatedAt`  <a name="CreatedAt-fn::getatt"></a>
 A timestamp that indicates when the rule was created\.
Uses the `date-time` format specified in [RFC 3339 section 5\.6, Internet Date/Time Format](https://tools.ietf.org/html/rfc3339#section-5.6)\. The value cannot contain spaces\. For example, `2020-03-22T13:22:13.933Z`\.

`CreatedBy`  <a name="CreatedBy-fn::getatt"></a>
 The principal that created the rule\. For example, `arn:aws:sts::123456789012:assumed-role/Developer-Role/JaneDoe`\.

`RuleArn`  <a name="RuleArn-fn::getatt"></a>
 The Amazon Resource Name \(ARN\) of the automation rule that you create\. For example, `arn:aws:securityhub:us-east-1:123456789012:automation-rule/a1b2c3d4-5678-90ab-cdef-EXAMPLE11111`\.

`UpdatedAt`  <a name="UpdatedAt-fn::getatt"></a>
 A timestamp that indicates when the rule was most recently updated\.
Uses the `date-time` format specified in [RFC 3339 section 5\.6, Internet Date/Time Format](https://tools.ietf.org/html/rfc3339#section-5.6)\. The value cannot contain spaces\. For example, `2020-03-22T13:22:13.933Z`\.

## Examples<a name="aws-resource-securityhub-automationrule--examples"></a>

The following examples demonstrate how to declare an `AWS::SecurityHub::AutomationRule` resource\.

### Creating an automation rule<a name="aws-resource-securityhub-automationrule--examples--Creating_an_automation_rule"></a>

This example creates a Security Hub automation rule\. This example contains all available fields for `Actions` and `Criteria` for demonstration purposes\.

#### JSON<a name="aws-resource-securityhub-automationrule--examples--Creating_an_automation_rule--json"></a>

```
{
  "Description": "Example template to create Security Hub automation rule",
  "Resources": {
    "RuleWithCriteriaActionsTags": {
      "Type": "AWS::SecurityHub::AutomationRule",
      "Properties": {
        "RuleName": "Example rule name",
        "RuleOrder": 5,
        "Description": "Example rule description.",
        "IsTerminal": false,
        "RuleStatus": "ENABLED",
        "Criteria": {
          "ProductName": [
            {
              "Comparison": "EQUALS",
              "Value": "GuardDuty"
            },
            {
              "Comparison": "PREFIX",
              "Value": "SecurityHub"
            }
          ],
          "CompanyName": [
            {
              "Comparison": "EQUALS",
              "Value": "AWS"
            },
            {
              "Comparison": "PREFIX",
              "Value": "Private"
            }
          ],
          "ProductArn": [
            {
              "Comparison": "EQUALS",
              "Value": "arn:aws:securityhub:us-west-2:123456789012:product/123456789012/default"
            },
            {
              "Comparison": "PREFIX",
              "Value": "arn:aws:securityhub:us-west-2:123456789012:product/aws"
            }
          ],
          "AwsAccountId": [
            {
              "Comparison": "EQUALS",
              "Value": 123456789012
            }
          ],
          "Id": [
            {
              "Comparison": "EQUALS",
              "Value": "example-finding-id"
            }
          ],
          "GeneratorId": [
            {
              "Comparison": "EQUALS",
              "Value": "example-generator-id"
            }
          ],
          "Type": [
            {
              "Comparison": "EQUALS",
              "Value": "type-1"
            },
            {
              "Comparison": "EQUALS",
              "Value": "type-2"
            }
          ],
          "Description": [
            {
              "Comparison": "EQUALS",
              "Value": "description1"
            },
            {
              "Comparison": "EQUALS",
              "Value": "description2"
            }
          ],
          "SourceUrl": [
            {
              "Comparison": "PREFIX",
              "Value": "https"
            },
            {
              "Comparison": "PREFIX",
              "Value": "ftp"
            }
          ],
          "Title": [
            {
              "Comparison": "EQUALS",
              "Value": "title-1"
            },
            {
              "Comparison": "PREFIX",
              "Value": "title-2"
            }
          ],
          "SeverityLabel": [
            {
              "Comparison": "EQUALS",
              "Value": "LOW"
            },
            {
              "Comparison": "EQUALS",
              "Value": "HIGH"
            }
          ],
          "ResourceType": [
            {
              "Comparison": "EQUALS",
              "Value": "AwsEc2Instance"
            }
          ],
          "ResourcePartition": [
            {
              "Comparison": "EQUALS",
              "Value": "aws"
            }
          ],
          "ResourceId": [
            {
              "Comparison": "PREFIX",
              "Value": "i-1234567890"
            }
          ],
          "ResourceRegion": [
            {
              "Comparison": "PREFIX",
              "Value": "us-west"
            }
          ],
          "ComplianceStatus": [
            {
              "Comparison": "EQUALS",
              "Value": "FAILED"
            }
          ],
          "ComplianceSecurityControlId": [
            {
              "Comparison": "EQUALS",
              "Value": "EC2.3"
            }
          ],
          "ComplianceAssociatedStandardsId": [
            {
              "Comparison": "EQUALS",
              "Value": "ruleset/cis-aws-foundations-benchmark/v/1.2.0"
            }
          ],
          "VerificationState": [
            {
              "Comparison": "EQUALS",
              "Value": "BENIGN_POSITIVE"
            }
          ],
          "RecordState": [
            {
              "Comparison": "EQUALS",
              "Value": "ACTIVE"
            }
          ],
          "RelatedFindingsProductArn": [
            {
              "Comparison": "EQUALS",
              "Value": "arn:aws:securityhub:eu-central-1::product/aws/securityhub"
            }
          ],
          "RelatedFindingsId": [
            {
              "Comparison": "EQUALS",
              "Value": "example-finding-id-2"
            }
          ],
          "NoteText": [
            {
              "Comparison": "EQUALS",
              "Value": "example-note-text"
            }
          ],
          "NoteUpdatedAt": [
            {
              "DateRange": {
                "Unit": "DAYS",
                "Value": 5
              }
            }
          ],
          "NoteUpdatedBy": [
            {
              "Comparison": "PREFIX",
              "Value": "sechub"
            }
          ],
          "WorkflowStatus": [
            {
              "Comparison": "EQUALS",
              "Value": "NEW"
            }
          ],
          "FirstObservedAt": [
            {
              "DateRange": {
                "Unit": "DAYS",
                "Value": 5
              }
            }
          ],
          "LastObservedAt": [
            {
              "DateRange": {
                "Unit": "DAYS",
                "Value": 5
              }
            }
          ],
          "CreatedAt": [
            {
              "DateRange": {
                "Unit": "DAYS",
                "Value": 5
              }
            }
          ],
          "UpdatedAt": [
            {
              "Start": "2023-04-25T17:05:54.832Z",
              "End": "2023-05-25T17:05:54.832Z"
            }
          ],
          "ResourceTags": [
            {
              "Comparison": "NOT_EQUALS",
              "Key": "department",
              "Value": "security"
            },
            {
              "Comparison": "NOT_EQUALS",
              "Key": "department",
              "Value": "operations"
            }
          ],
          "UserDefinedFields": [
            {
              "Comparison": "EQUALS",
              "Key": "key1",
              "Value": "security"
            },
            {
              "Comparison": "EQUALS",
              "Key": "key2",
              "Value": "operations"
            }
          ],
          "ResourceDetailsOther": [
            {
              "Comparison": "NOT_EQUALS",
              "Key": "area",
              "Value": "na"
            },
            {
              "Comparison": "NOT_EQUALS",
              "Key": "department",
              "Value": "sales"
            }
          ],
          "Confidence": [
            {
              "Gte": 50,
              "Lte": 95
            }
          ],
          "Criticality": [
            {
              "Gte": 50,
              "Lte": 95
            }
          ]
        },
        "Actions": [
          {
            "Type": "FINDING_FIELDS_UPDATE",
            "FindingFieldsUpdate": {
              "Severity": {
                "Product": 50,
                "Label": "MEDIUM",
                "Normalized": 60
              },
              "Types": [
                "Software and Configuration Checks/Industry and Regulatory Standards/AWS-Foundational-Security-Best-Practices",
                "Industry Compliance"
              ],
              "Confidence": 98,
              "Criticality": 95,
              "UserDefinedFields": {
                "key1": "value1",
                "key2": "value2"
              },
              "RelatedFindings": [
                {
                  "ProductArn": "arn:aws:securityhub:us-west-2:123456789012:product/123456789012/default",
                  "Id": "sample-finding-id-1"
                },
                {
                  "ProductArn": "arn:aws:securityhub:us-west-2:123456789012:product/123456789012/default",
                  "Id": "sample-finding-id-2"
                }
              ],
              "Note": {
                "Text": "sample-note-text",
                "UpdatedBy": "sechub"
              },
              "VerificationState": "TRUE_POSITIVE",
              "Workflow": {
                "Status": "NOTIFIED"
              }
            }
          }
        ],
        "Tags": {
          "sampleTag": "sampleValue",
          "organizationUnit": "pnw"
        }
      }
    }
  }
}
```

#### YAML<a name="aws-resource-securityhub-automationrule--examples--Creating_an_automation_rule--yaml"></a>

```
---
Description: Example template to create Security Hub automation rule
Resources:
  RuleWithCriteriaActionsTags:
    Type: "AWS::SecurityHub::AutomationRule"
    Properties:
      RuleName: "Example rule name"
      RuleOrder: 5
      Description: "Example rule description."
      IsTerminal: false
      RuleStatus: "ENABLED"
      Criteria:
        ProductName:
          - Comparison: EQUALS
            Value: GuardDuty
          - Comparison: PREFIX
            Value: SecurityHub
        CompanyName:
          - Comparison: EQUALS
            Value: AWS
          - Comparison: PREFIX
            Value: Private
        ProductArn:
          - Comparison: EQUALS
            Value: arn:aws:securityhub:us-west-2:123456789012:product/123456789012/default
          - Comparison: PREFIX
            Value: arn:aws:securityhub:us-west-2:123456789012:product/aws
        AwsAccountId:
          - Comparison: EQUALS
            Value: 123456789012
        Id:
          - Comparison: EQUALS
            Value: example-finding-id
        GeneratorId:
          - Comparison: EQUALS
            Value: example-generator-id
        Type:
          - Comparison: EQUALS
            Value: type-1
          - Comparison: EQUALS
            Value: type-2
        Description:
          - Comparison: EQUALS
            Value: description1
          - Comparison: EQUALS
            Value: description2
        SourceUrl:
          - Comparison: PREFIX
            Value: https
          - Comparison: PREFIX
            Value: ftp
        Title:
          - Comparison: EQUALS
            Value: title-1
          - Comparison: PREFIX
            Value: title-2
        SeverityLabel:
          - Comparison: EQUALS
            Value: LOW
          - Comparison: EQUALS
            Value: HIGH
        ResourceType:
          - Comparison: EQUALS
            Value: AwsEc2Instance
        ResourcePartition:
          - Comparison: EQUALS
            Value: aws
        ResourceId:
          - Comparison: PREFIX
            Value: i-1234567890
        ResourceRegion:
          - Comparison: PREFIX
            Value: us-west
        ComplianceStatus:
          - Comparison: EQUALS
            Value: FAILED
        ComplianceSecurityControlId:
          - Comparison: EQUALS
            Value: EC2.3
        ComplianceAssociatedStandardsId:
          - Comparison: EQUALS
            Value: ruleset/cis-aws-foundations-benchmark/v/1.2.0
        VerificationState:
          - Comparison: EQUALS
            Value: BENIGN_POSITIVE
        RecordState:
          - Comparison: EQUALS
            Value: ACTIVE
        RelatedFindingsProductArn:
          - Comparison: EQUALS
            Value: arn:aws:securityhub:eu-central-1::product/aws/securityhub
        RelatedFindingsId:
          - Comparison: EQUALS
            Value: example-finding-id-2
        NoteText:
          - Comparison: EQUALS
            Value: example-note-text
        NoteUpdatedAt:
          - DateRange:
              Unit: DAYS
              Value: 5
        NoteUpdatedBy:
          - Comparison: PREFIX
            Value: sechub
        WorkflowStatus:
          - Comparison: EQUALS
            Value: NEW
        FirstObservedAt:
          - DateRange:
              Unit: DAYS
              Value: 5
        LastObservedAt:
          - DateRange:
              Unit: DAYS
              Value: 5
        CreatedAt:
          - DateRange:
              Unit: DAYS
              Value: 5
        UpdatedAt:
          - Start: "2023-04-25T17:05:54.832Z"
            End: "2023-05-25T17:05:54.832Z"
        ResourceTags:
          - Comparison: NOT_EQUALS
            Key: department
            Value: security
          - Comparison: NOT_EQUALS
            Key: department
            Value: operations
        UserDefinedFields:
          - Comparison: EQUALS
            Key: key1
            Value: security
          - Comparison: EQUALS
            Key: key2
            Value: operations
        ResourceDetailsOther:
          - Comparison: NOT_EQUALS
            Key: area
            Value: na
          - Comparison: NOT_EQUALS
            Key: department
            Value: sales
        Confidence:
          - Gte: 50
            Lte: 95
        Criticality:
          - Gte: 50
            Lte: 95
      Actions:
        - Type: FINDING_FIELDS_UPDATE
          FindingFieldsUpdate:
            Severity:
              Product: 50
              Label: MEDIUM
              Normalized: 60
            Types:
              - Software and Configuration Checks/Industry and Regulatory Standards/AWS-Foundational-Security-Best-Practices
              - Industry Compliance
            Confidence: 98
            Criticality: 95
            UserDefinedFields:
              key1: value1
              key2: value2
            RelatedFindings:
              - ProductArn: arn:aws:securityhub:us-west-2:123456789012:product/123456789012/default
                Id: sample-finding-id-1
              - ProductArn: arn:aws:securityhub:us-west-2:123456789012:product/123456789012/default
                Id: sample-finding-id-2
            Note:
              Text: sample-note-text
              UpdatedBy: sechub
            VerificationState: TRUE_POSITIVE
            Workflow:
              Status: NOTIFIED
      Tags:
        sampleTag: sampleValue
        organizationUnit: pnw
```