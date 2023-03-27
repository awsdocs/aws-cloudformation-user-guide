# AWS::EC2::NetworkInsightsAnalysis AdditionalDetail<a name="aws-properties-ec2-networkinsightsanalysis-additionaldetail"></a>

Describes an additional detail for a path analysis\.

## Syntax<a name="aws-properties-ec2-networkinsightsanalysis-additionaldetail-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-ec2-networkinsightsanalysis-additionaldetail-syntax.json"></a>

```
{
  "[AdditionalDetailType](#cfn-ec2-networkinsightsanalysis-additionaldetail-additionaldetailtype)" : String,
  "[Component](#cfn-ec2-networkinsightsanalysis-additionaldetail-component)" : AnalysisComponent,
  "[LoadBalancers](#cfn-ec2-networkinsightsanalysis-additionaldetail-loadbalancers)" : [ AnalysisComponent, ... ],
  "[ServiceName](#cfn-ec2-networkinsightsanalysis-additionaldetail-servicename)" : String
}
```

### YAML<a name="aws-properties-ec2-networkinsightsanalysis-additionaldetail-syntax.yaml"></a>

```
  [AdditionalDetailType](#cfn-ec2-networkinsightsanalysis-additionaldetail-additionaldetailtype): String
  [Component](#cfn-ec2-networkinsightsanalysis-additionaldetail-component): 
    AnalysisComponent
  [LoadBalancers](#cfn-ec2-networkinsightsanalysis-additionaldetail-loadbalancers): 
    - AnalysisComponent
  [ServiceName](#cfn-ec2-networkinsightsanalysis-additionaldetail-servicename): String
```

## Properties<a name="aws-properties-ec2-networkinsightsanalysis-additionaldetail-properties"></a>

`AdditionalDetailType`  <a name="cfn-ec2-networkinsightsanalysis-additionaldetail-additionaldetailtype"></a>
The information type\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Component`  <a name="cfn-ec2-networkinsightsanalysis-additionaldetail-component"></a>
The path component\.  
*Required*: No  
*Type*: [AnalysisComponent](aws-properties-ec2-networkinsightsanalysis-analysiscomponent.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LoadBalancers`  <a name="cfn-ec2-networkinsightsanalysis-additionaldetail-loadbalancers"></a>
Property description not available\.  
*Required*: No  
*Type*: List of [AnalysisComponent](aws-properties-ec2-networkinsightsanalysis-analysiscomponent.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ServiceName`  <a name="cfn-ec2-networkinsightsanalysis-additionaldetail-servicename"></a>
Property description not available\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)