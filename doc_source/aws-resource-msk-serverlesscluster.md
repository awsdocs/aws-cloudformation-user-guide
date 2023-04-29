# AWS::MSK::ServerlessCluster<a name="aws-resource-msk-serverlesscluster"></a>

<a name="aws-resource-msk-serverlesscluster-description"></a>The `AWS::MSK::ServerlessCluster` resource Property description not available\. for MSK\.

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
Property description not available\.  
*Required*: Yes  
*Type*: [ClientAuthentication](aws-properties-msk-serverlesscluster-clientauthentication.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ClusterName`  <a name="cfn-msk-serverlesscluster-clustername"></a>
Property description not available\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-msk-serverlesscluster-tags"></a>
Property description not available\.  
*Required*: No  
*Type*: Map of String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`VpcConfigs`  <a name="cfn-msk-serverlesscluster-vpcconfigs"></a>
Property description not available\.  
*Required*: Yes  
*Type*: List of [VpcConfig](aws-properties-msk-serverlesscluster-vpcconfig.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-msk-serverlesscluster-return-values"></a>

### Ref<a name="aws-resource-msk-serverlesscluster-return-values-ref"></a>

### Fn::GetAtt<a name="aws-resource-msk-serverlesscluster-return-values-fn--getatt"></a>

#### <a name="aws-resource-msk-serverlesscluster-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
Property description not available\.