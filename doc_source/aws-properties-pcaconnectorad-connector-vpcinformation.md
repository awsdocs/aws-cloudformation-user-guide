# AWS::PCAConnectorAD::Connector VpcInformation<a name="aws-properties-pcaconnectorad-connector-vpcinformation"></a>

Information about your VPC and security groups used with the connector\.

## Syntax<a name="aws-properties-pcaconnectorad-connector-vpcinformation-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-pcaconnectorad-connector-vpcinformation-syntax.json"></a>

```
{
  "[SecurityGroupIds](#cfn-pcaconnectorad-connector-vpcinformation-securitygroupids)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-pcaconnectorad-connector-vpcinformation-syntax.yaml"></a>

```
  [SecurityGroupIds](#cfn-pcaconnectorad-connector-vpcinformation-securitygroupids): 
    - String
```

## Properties<a name="aws-properties-pcaconnectorad-connector-vpcinformation-properties"></a>

`SecurityGroupIds`  <a name="cfn-pcaconnectorad-connector-vpcinformation-securitygroupids"></a>
The security groups used with the connector\. You can use a maximum of 4 security groups with a connector\.  
*Required*: Yes  
*Type*: List of String  
*Maximum*: `4`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)