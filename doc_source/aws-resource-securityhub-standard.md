# AWS::SecurityHub::Standard<a name="aws-resource-securityhub-standard"></a>

The `AWS::SecurityHub::Standard` resource specifies the enablement of a security standard\. The standard is identified by the `StandardsArn` property\. To view a list of Security Hub standards and their Amazon Resource Names \(ARNs\), use the [https://docs.aws.amazon.com/securityhub/1.0/APIReference/API_DescribeStandards.html](https://docs.aws.amazon.com/securityhub/1.0/APIReference/API_DescribeStandards.html) API operation\.

You must create a separate `AWS::SecurityHub::Standard` resource for each standard that you want to enable\.

For more information about Security Hub standards, see [Security Hub standards reference](https://docs.aws.amazon.com/securityhub/latest/userguide/standards-reference.html) in the *AWS Security Hub User Guide*\.

## Syntax<a name="aws-resource-securityhub-standard-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-securityhub-standard-syntax.json"></a>

```
{
  "Type" : "AWS::SecurityHub::Standard",
  "Properties" : {
      "[DisabledStandardsControls](#cfn-securityhub-standard-disabledstandardscontrols)" : [ StandardsControl, ... ],
      "[StandardsArn](#cfn-securityhub-standard-standardsarn)" : String
    }
}
```

### YAML<a name="aws-resource-securityhub-standard-syntax.yaml"></a>

```
Type: AWS::SecurityHub::Standard
Properties: 
  [DisabledStandardsControls](#cfn-securityhub-standard-disabledstandardscontrols): 
    - StandardsControl
  [StandardsArn](#cfn-securityhub-standard-standardsarn): String
```

## Properties<a name="aws-resource-securityhub-standard-properties"></a>

`DisabledStandardsControls`  <a name="cfn-securityhub-standard-disabledstandardscontrols"></a>
 Specifies which controls are to be disabled in a standard\.   
*Maximum*: `100`  
*Required*: No  
*Type*: List of [StandardsControl](aws-properties-securityhub-standard-standardscontrol.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StandardsArn`  <a name="cfn-securityhub-standard-standardsarn"></a>
The ARN of the standard that you want to enable\. To view a list of available Security Hub standards and their ARNs, use the [https://docs.aws.amazon.com/securityhub/1.0/APIReference/API_DescribeStandards.html](https://docs.aws.amazon.com/securityhub/1.0/APIReference/API_DescribeStandards.html) API operation\.  
*Required*: Yes  
*Type*: String  
*Pattern*: `.*\S.*`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-securityhub-standard-return-values"></a>

### Ref<a name="aws-resource-securityhub-standard-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref`function, `Ref`returns `StandardsSubscriptionArn` for the standard that you enable, such as `arn:aws:securityhub:us-east-1:123456789012:subscription/aws-foundational-security-best-practices/v/1.0.0`\.

For more information about using the `Ref`function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-securityhub-standard-return-values-fn--getatt"></a>

The `Fn::GetAtt`intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt`intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-securityhub-standard-return-values-fn--getatt-fn--getatt"></a>

`StandardsSubscriptionArn`  <a name="StandardsSubscriptionArn-fn::getatt"></a>
The ARN of a resource that represents your subscription to a supported standard\.

## Examples<a name="aws-resource-securityhub-standard--examples"></a>

The following examples show how to declare an `AWS::SecurityHub::Standard` resource\. 

### Enabling a standard with all controls enabled<a name="aws-resource-securityhub-standard--examples--Enabling_a_standard_with_all_controls_enabled"></a>

The following example enables the AWS Foundational Security Best Practices \(FSBP\) standard and all controls that apply to it\.

#### JSON<a name="aws-resource-securityhub-standard--examples--Enabling_a_standard_with_all_controls_enabled--json"></a>

```
{
    "Description": "Example Standard",
    "Resources": {
        "ExampleStandard": {
            "Type": "AWS::SecurityHub::Standard",
            "Properties": {
                "StandardsArn": {
                   "Fn::Sub": "arn:${AWS::Partition}:securityhub:${AWS::Region}::standards/aws-foundational-security-best-practices/v/1.0.0"
                }
            }
        }
    },
    "Outputs": {
        "StandardsSubscriptionArn": {
            "Value": {
                "Ref": "ExampleStandard"
            }
        }
    }
}
```

#### YAML<a name="aws-resource-securityhub-standard--examples--Enabling_a_standard_with_all_controls_enabled--yaml"></a>

```
---
Description: Example Standard
Resources:
  ExampleStandard:
    Type: 'AWS::SecurityHub::Standard'
    Properties:
      StandardsArn: !Sub 'arn:${AWS::Partition}:securityhub:${AWS::Region}::standards/aws-foundational-security-best-practices/v/1.0.0'
Outputs:
  StandardsSubscriptionArn:
    Value: !Ref ExampleStandard
```

### Enabling a standard with some controls disabled<a name="aws-resource-securityhub-standard--examples--Enabling_a_standard_with_some_controls_disabled"></a>

The following example enables the FSBP standard\. The controls specified in the example are disabled in this standard, and all other controls are enabled in this standard\.

#### JSON<a name="aws-resource-securityhub-standard--examples--Enabling_a_standard_with_some_controls_disabled--json"></a>

```
{
    "Description": "Example Standard",
    "Resources": {
        "ExampleStandardWithDisabledControls": {
            "Type": "AWS::SecurityHub::Standard",
            "Properties": {
                "StandardsArn": {
                    "Fn::Sub": "arn:${AWS::Partition}:securityhub:${AWS::Region}::standards/aws-foundational-security-best-practices/v/1.0.0"
                },
                "DisabledStandardsControls": [
                    {
                        "StandardsControlArn": {
                            "Fn::Sub": "arn:${AWS::Partition}:securityhub:${AWS::Region}:${AWS::AccountId}:control/aws-foundational-security-best-practices/v/1.0.0/APIGateway.1"
                        },
                        "Reason": "Disabled reason text"
                    },
                    {
                        "StandardsControlArn": {
                            "Fn::Sub": "arn:${AWS::Partition}:securityhub:${AWS::Region}:${AWS::AccountId}:control/aws-foundational-security-best-practices/v/1.0.0/APIGateway.2"
                        },
                        "Reason": "Disabled reason text"
                    }
                ]
            }
        }
    },
    "Outputs": {
        "StandardsSubscriptionArn": {
            "Value": {
                "Ref": "ExampleStandardWithDisabledControls"
            }
        }
    }
}
```

#### YAML<a name="aws-resource-securityhub-standard--examples--Enabling_a_standard_with_some_controls_disabled--yaml"></a>

```
---
Description: Example Standard
Resources:
  ExampleStandardWithDisabledControls:
    Type: 'AWS::SecurityHub::Standard'
    Properties:
      StandardsArn: !Sub 'arn:${AWS::Partition}:securityhub:${AWS::Region}::standards/aws-foundational-security-best-practices/v/1.0.0'
      DisabledStandardsControls:
        - StandardsControlArn: !Sub 'arn:${AWS::Partition}:securityhub:${AWS::Region}:${AWS::AccountId}:control/aws-foundational-security-best-practices/v/1.0.0/APIGateway.1'
          Reason: 'Disabled reason text'
        - StandardsControlArn: !Sub 'arn:${AWS::Partition}:securityhub:${AWS::Region}:${AWS::AccountId}:control/aws-foundational-security-best-practices/v/1.0.0/APIGateway.2'
          Reason: 'Disabled reason text'
Outputs:
  StandardsSubscriptionArn:
    Value: !Ref ExampleStandardWithDisabledControls
```