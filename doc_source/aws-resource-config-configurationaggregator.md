# AWS::Config::ConfigurationAggregator<a name="aws-resource-config-configurationaggregator"></a>

The `AWS::Config::ConfigurationAggregator` resource is an AWS Config resource type that collects AWS Config data from multiple accounts and regions\. Use an aggregator to view the resource configuration and compliance data recorded in AWS Config for multiple accounts and regions\. 

**Topics**
+ [Syntax](#aws-resource-config-configurationaggregator-syntax)
+ [Properties](#aws-resource-config-configurationaggregator-properties)
+ [Return Values](#aws-resource-config-configurationaggregator-returnvalues)
+ [Examples](#aws-resource-config-configurationaggregator-examples)

## Syntax<a name="aws-resource-config-configurationaggregator-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-config-configurationaggregator-syntax.json"></a>

```
{
  "Type" : "AWS::Config::ConfigurationAggregator",
  "Properties" : {
    "[AccountAggregationSources](#cfn-config-configurationaggregator-accountaggregationsources)" : [ [*AccountAggregationSource*](aws-properties-config-configurationaggregator-accountaggregationsource.md), ... ],
    "[OrganizationAggregationSource](#cfn-config-configurationaggregator-organizationaggregationsource)" : [*OrganizationAggregationSource*](aws-properties-config-configurationaggregator-organizationaggregationsource.md),
    "[ConfigurationAggregatorName](#cfn-config-configurationaggregator-configurationaggregatorname)" : String
  }
}
```

### YAML<a name="aws-resource-config-configurationaggregator-syntax.yaml"></a>

```
Type: "AWS::Config::ConfigurationAggregator"
Properties:
  [AccountAggregationSources](#cfn-config-configurationaggregator-accountaggregationsources): 
    - [*AccountAggregationSource*](aws-properties-config-configurationaggregator-accountaggregationsource.md)
 [OrganizationAggregationSource](#cfn-config-configurationaggregator-organizationaggregationsource): 
    [*OrganizationAggregationSource*](aws-properties-config-configurationaggregator-organizationaggregationsource.md)
  [ConfigurationAggregatorName](#cfn-config-configurationaggregator-configurationaggregatorname): String
```

## Properties<a name="aws-resource-config-configurationaggregator-properties"></a>

`AccountAggregationSources`  <a name="cfn-config-configurationaggregator-accountaggregationsources"></a>
A collection of accounts and regions\.  
 *Required*: No  
 *Type*: List of [AWS Config ConfigurationAggregator AccountAggregationSource](aws-properties-config-configurationaggregator-accountaggregationsource.md) property types  
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`OrganizationAggregationSource`  <a name="cfn-config-configurationaggregator-organizationaggregationsource"></a>
A collection of regions and IAM role to retrieve AWS Organizations details\.  
 *Required*: No  
 *Type*: [AWS Config ConfigurationAggregator OrganizationAggregationSource](aws-properties-config-configurationaggregator-organizationaggregationsource.md)   
 *Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt) 

`ConfigurationAggregatorName`  <a name="cfn-config-configurationaggregator-configurationaggregatorname"></a>
The name of the configuration aggregator\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

## Return Values<a name="aws-resource-config-configurationaggregator-returnvalues"></a>

### Ref<a name="aws-resource-config-configurationaggregator-ref"></a>

When you pass the logical ID of an `AWS::Config::ConfigurationAggregator` resource to the intrinsic `Ref` function, the function returns the ConfigurationAggregatorName, such as `myConfigurationAggregator`\. 

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\. 

## Examples<a name="aws-resource-config-configurationaggregator-examples"></a>

### ConfigurationAggregator with multiple accounts and multiple regions\.<a name="aws-resource-config-configurationaggregator-example1"></a>

The following example creates a ConfigurationAggregator 

#### JSON<a name="aws-resource-config-configurationaggregator-example1.json"></a>

```
"ConfigurationAggregator": {
    "Type": "AWS::Config::ConfigurationAggregator",
    "Properties": {
      "AccountAggregationSources": [
        {
          "AccountIds": [
            "123456789012",
            "987654321012"
          ],
          "AwsRegions": [
            "us-west-2",
            "us-east-1"
          ],
          "AllAwsRegions": false
        }
      ],
      "ConfigurationAggregatorName": "MyConfigurationAggregator"
    }
  }
```

#### YAML<a name="aws-resource-config-configurationaggregator-example1.yaml"></a>

```
ConfigurationAggregator: 
    Type: "AWS::Config::ConfigurationAggregator"
    Properties: 
      AccountAggregationSources: 
        - AccountIds: 
            - "123456789012"
            - "987654321012"
          AwsRegions:
            - "us-west-2"
            - "us-east-1"
          AllAwsRegions: false
      ConfigurationAggregatorName: MyConfigurationAggregator
```

### ConfigurationAggregator for organization\.<a name="aws-resource-config-configurationaggregator-example2"></a>

The following example creates a ConfigurationAggregator for an organization\.

#### JSON<a name="aws-resource-config-configurationaggregator-example2.json"></a>

```
"ConfigurationAggregator": {
    "Type": "AWS::Config::ConfigurationAggregator",
    "Properties": {
      "OrganizationAggregationSource": {
        "RoleArn": "arn:aws:iam::012345678912:role/aws-service-role/organizations.amazonaws.com/AWSServiceRoleForOrganizations",
        "AwsRegions": [
          "us-west-2",
          "us-east-1"
        ],
        "AllAwsRegions": false
      }
      "ConfigurationAggregatorName": "MyConfigurationAggregator"
    }
  }
```

#### YAML<a name="aws-resource-config-configurationaggregator-example2.yaml"></a>

```
ConfigurationAggregator: 
    Type: "AWS::Config::ConfigurationAggregator"
    Properties: 
      OrganizationAggregationSource: 
        RoleArn: "arn:aws:iam::012345678912:role/aws-service-role/organizations.amazonaws.com/AWSServiceRoleForOrganizations"
        AwsRegions:
          - "us-west-2"
          - "us-east-1"
        AllAwsRegions: false
      ConfigurationAggregatorName: MyConfigurationAggregator
```