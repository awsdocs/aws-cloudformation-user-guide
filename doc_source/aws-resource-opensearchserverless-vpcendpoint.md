# AWS::OpenSearchServerless::VpcEndpoint<a name="aws-resource-opensearchserverless-vpcendpoint"></a>

Creates an OpenSearch Serverless\-managed interface VPC endpoint\. For more information, see [Access Amazon OpenSearch Serverless using an interface endpoint](https://docs.aws.amazon.com/opensearch-service/latest/developerguide/serverless-vpc.html)\.

## Syntax<a name="aws-resource-opensearchserverless-vpcendpoint-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-opensearchserverless-vpcendpoint-syntax.json"></a>

```
{
  "Type" : "AWS::OpenSearchServerless::VpcEndpoint",
  "Properties" : {
      "[Name](#cfn-opensearchserverless-vpcendpoint-name)" : String,
      "[SecurityGroupIds](#cfn-opensearchserverless-vpcendpoint-securitygroupids)" : [ String, ... ],
      "[SubnetIds](#cfn-opensearchserverless-vpcendpoint-subnetids)" : [ String, ... ],
      "[VpcId](#cfn-opensearchserverless-vpcendpoint-vpcid)" : String
    }
}
```

### YAML<a name="aws-resource-opensearchserverless-vpcendpoint-syntax.yaml"></a>

```
Type: AWS::OpenSearchServerless::VpcEndpoint
Properties: 
  [Name](#cfn-opensearchserverless-vpcendpoint-name): String
  [SecurityGroupIds](#cfn-opensearchserverless-vpcendpoint-securitygroupids): 
    - String
  [SubnetIds](#cfn-opensearchserverless-vpcendpoint-subnetids): 
    - String
  [VpcId](#cfn-opensearchserverless-vpcendpoint-vpcid): String
```

## Properties<a name="aws-resource-opensearchserverless-vpcendpoint-properties"></a>

`Name`  <a name="cfn-opensearchserverless-vpcendpoint-name"></a>
The name of the endpoint\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`SecurityGroupIds`  <a name="cfn-opensearchserverless-vpcendpoint-securitygroupids"></a>
The unique identifiers of the security groups that define the ports, protocols, and sources for inbound traffic that you are authorizing into your endpoint\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SubnetIds`  <a name="cfn-opensearchserverless-vpcendpoint-subnetids"></a>
The ID of the subnets from which you access OpenSearch Serverless\.  
*Required*: Yes  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VpcId`  <a name="cfn-opensearchserverless-vpcendpoint-vpcid"></a>
The ID of the VPC from which you access OpenSearch Serverless\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-opensearchserverless-vpcendpoint-return-values"></a>

### Ref<a name="aws-resource-opensearchserverless-vpcendpoint-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the endpoint ID\. For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-opensearchserverless-vpcendpoint-return-values-fn--getatt"></a>

`GetAtt` returns a value for a specified attribute of this type\. For more information, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\. The following are the available attributes and sample return values\.

#### <a name="aws-resource-opensearchserverless-vpcendpoint-return-values-fn--getatt-fn--getatt"></a>

`Id`  <a name="Id-fn::getatt"></a>
The unique identifier of the endpoint\. For example, `vpce-050f79086ee71ac05`\.

## Examples<a name="aws-resource-opensearchserverless-vpcendpoint--examples"></a>

### Create a VPC endpoint<a name="aws-resource-opensearchserverless-vpcendpoint--examples--Create_a_VPC_endpoint"></a>

The following example specifies an OpenSearch Serverless\-managed interface VPC endpoint named `test-vpcendpoint`\. The endpoint has one subnet and one security group\.

#### JSON<a name="aws-resource-opensearchserverless-vpcendpoint--examples--Create_a_VPC_endpoint--json"></a>

```
{
  "AWSTemplateFormatVersion": "2010-09-09",
  "Description": "OpenSearch Serverless VPC endpoint template",
  "Resources": {
    "TestAOSSVpcEndpoint": {
      "Type": "AWS::OpenSearchServerless::VpcEndpoint",
      "Properties": {
        "Name": "test-vpcendpoint",
        "VpcId": "vpc-0d728b8430292b3f4",
        "SubnetIds": [
          "subnet-0e855f5722a9598ee"
        ],
        "SecurityGroupIds": [
          "sg-03843b03f369eb245"
        ]
      }
    }
  }
}
```

#### YAML<a name="aws-resource-opensearchserverless-vpcendpoint--examples--Create_a_VPC_endpoint--yaml"></a>

```
AWSTemplateFormatVersion: 2010-09-09
Description: 'OpenSearch Serverless VPC endpoint template'
Resources:
  TestAOSSVpcEndpoint:
    Type: 'AWS::OpenSearchServerless::VpcEndpoint'
    Properties:
      Name: test-vpcendpoint
      VpcId: vpc-0d728b8430292b3f4
      SubnetIds:
        - subnet-0e855f5722a9598ee
      SecurityGroupIds:
        - sg-03843b03f369eb245
```