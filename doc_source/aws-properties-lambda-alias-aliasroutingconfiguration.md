# AWS::Lambda::Alias AliasRoutingConfiguration<a name="aws-properties-lambda-alias-aliasroutingconfiguration"></a>

The [traffic\-shifting](https://docs.aws.amazon.com/lambda/latest/dg/lambda-traffic-shifting-using-aliases.html) configuration of a Lambda function alias\.

## Syntax<a name="aws-properties-lambda-alias-aliasroutingconfiguration-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-lambda-alias-aliasroutingconfiguration-syntax.json"></a>

```
{
  "[AdditionalVersionWeights](#cfn-lambda-alias-aliasroutingconfiguration-additionalversionweights)" : [ VersionWeight, ... ]
}
```

### YAML<a name="aws-properties-lambda-alias-aliasroutingconfiguration-syntax.yaml"></a>

```
  [AdditionalVersionWeights](#cfn-lambda-alias-aliasroutingconfiguration-additionalversionweights): 
    - VersionWeight
```

## Properties<a name="aws-properties-lambda-alias-aliasroutingconfiguration-properties"></a>

`AdditionalVersionWeights`  <a name="cfn-lambda-alias-aliasroutingconfiguration-additionalversionweights"></a>
The second version, and the percentage of traffic that's routed to it\.  
*Required*: Yes  
*Type*: List of [VersionWeight](aws-properties-lambda-alias-versionweight.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Examples<a name="aws-properties-lambda-alias-aliasroutingconfiguration--examples"></a>



### Routing Configuration<a name="aws-properties-lambda-alias-aliasroutingconfiguration--examples--Routing_Configuration"></a>

An alias that routes half of incoming requests to a second version\.

#### YAML<a name="aws-properties-lambda-alias-aliasroutingconfiguration--examples--Routing_Configuration--yaml"></a>

```
  alias:
    Type: AWS::Lambda::Alias
    Properties:
      FunctionName: !Ref function
      FunctionVersion: !GetAtt newVersion.Version
      Name: BLUE
      RoutingConfig:
        AdditionalVersionWeights:
          - FunctionVersion: !GetAtt version.Version
            FunctionWeight: 0.5
```