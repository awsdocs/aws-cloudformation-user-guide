# AWS::MSK::ServerlessCluster<a name="aws-resource-msk-serverlesscluster"></a>

The `AWS::MSK::ServerlessCluster` resource creates an Amazon MSK Serverless cluster\. For more information, see [MSK Serverless](https://docs.aws.amazon.com/msk/latest/developerguide/serverless.html) in the *Amazon MSK Developer Guide*

## Syntax<a name="aws-resource-msk-serverlesscluster-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-msk-serverlesscluster-syntax.json"></a>

```
{
  "Type" : "AWS::MSK::ServerlessCluster",
  "Properties" : {
      "[ClientAuthentication](#cfn-msk-serverlesscluster-clientauthentication)" : ClientAuthentication,
      "[ClusterName](#cfn-msk-serverlesscluster-clustername)" : String,
      "[Tags](#cfn-msk-serverlesscluster-tags)" : {Key : Value, ...},
      "[VpcConfigs](#cfn-msk-serverlesscluster-vpcconfigs)" : [ VpcConfig, ... ]
    }
}
```

### YAML<a name="aws-resource-msk-serverlesscluster-syntax.yaml"></a>

```
Type: AWS::MSK::ServerlessCluster
Properties: 
  [ClientAuthentication](#cfn-msk-serverlesscluster-clientauthentication): 
    ClientAuthentication
  [ClusterName](#cfn-msk-serverlesscluster-clustername): String
  [Tags](#cfn-msk-serverlesscluster-tags): 
    Key : Value
  [VpcConfigs](#cfn-msk-serverlesscluster-vpcconfigs): 
    - VpcConfig
```

## Properties<a name="aws-resource-msk-serverlesscluster-properties"></a>

`ClientAuthentication`  <a name="cfn-msk-serverlesscluster-clientauthentication"></a>
Specifies client authentication information for the serverless cluster\.  
*Required*: Yes  
*Type*: [ClientAuthentication](aws-properties-msk-serverlesscluster-clientauthentication.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ClusterName`  <a name="cfn-msk-serverlesscluster-clustername"></a>
The name of the serverless cluster\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-msk-serverlesscluster-tags"></a>
A map of key:value pairs to apply to this serverless cluster\.  
*Required*: No  
*Type*: Map of String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`VpcConfigs`  <a name="cfn-msk-serverlesscluster-vpcconfigs"></a>
VPC configuration information\.  
*Required*: Yes  
*Type*: List of [VpcConfig](aws-properties-msk-serverlesscluster-vpcconfig.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-msk-serverlesscluster-return-values"></a>

### Ref<a name="aws-resource-msk-serverlesscluster-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the Amazon MSK Serverless cluster ARN\.



For example, the expresesion `REF MyTestCluster` returns the ARN of the Amazon MSK Serverless cluster whose logical ID is `MyTestCluster`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-msk-serverlesscluster-return-values-fn--getatt"></a>

Not currently supported by AWS CloudFormation\.

#### <a name="aws-resource-msk-serverlesscluster-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The ARN of the serverless cluster\.