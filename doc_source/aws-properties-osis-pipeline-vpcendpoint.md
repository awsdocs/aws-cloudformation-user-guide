# AWS::OSIS::Pipeline VpcEndpoint<a name="aws-properties-osis-pipeline-vpcendpoint"></a>

An OpenSearch Ingestion\-managed VPC endpoint that will access one or more pipelines\.

## Syntax<a name="aws-properties-osis-pipeline-vpcendpoint-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-osis-pipeline-vpcendpoint-syntax.json"></a>

```
{
  "[VpcEndpointId](#cfn-osis-pipeline-vpcendpoint-vpcendpointid)" : String,
  "[VpcId](#cfn-osis-pipeline-vpcendpoint-vpcid)" : String,
  "[VpcOptions](#cfn-osis-pipeline-vpcendpoint-vpcoptions)" : VpcOptions
}
```

### YAML<a name="aws-properties-osis-pipeline-vpcendpoint-syntax.yaml"></a>

```
  [VpcEndpointId](#cfn-osis-pipeline-vpcendpoint-vpcendpointid): String
  [VpcId](#cfn-osis-pipeline-vpcendpoint-vpcid): String
  [VpcOptions](#cfn-osis-pipeline-vpcendpoint-vpcoptions): 
    VpcOptions
```

## Properties<a name="aws-properties-osis-pipeline-vpcendpoint-properties"></a>

`VpcEndpointId`  <a name="cfn-osis-pipeline-vpcendpoint-vpcendpointid"></a>
The unique identifier of the endpoint\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VpcId`  <a name="cfn-osis-pipeline-vpcendpoint-vpcid"></a>
The ID for your VPC\. AWS PrivateLink generates this value when you create a VPC\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VpcOptions`  <a name="cfn-osis-pipeline-vpcendpoint-vpcoptions"></a>
Information about the VPC, including associated subnets and security groups\.  
*Required*: No  
*Type*: [VpcOptions](aws-properties-osis-pipeline-vpcoptions.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)