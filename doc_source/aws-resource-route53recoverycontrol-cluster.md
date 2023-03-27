# AWS::Route53RecoveryControl::Cluster<a name="aws-resource-route53recoverycontrol-cluster"></a>

Returns an array of all the clusters in an account\.

## Syntax<a name="aws-resource-route53recoverycontrol-cluster-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-route53recoverycontrol-cluster-syntax.json"></a>

```
{
  "Type" : "AWS::Route53RecoveryControl::Cluster",
  "Properties" : {
      "[Name](#cfn-route53recoverycontrol-cluster-name)" : String,
      "[Tags](#cfn-route53recoverycontrol-cluster-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-route53recoverycontrol-cluster-syntax.yaml"></a>

```
Type: AWS::Route53RecoveryControl::Cluster
Properties: 
  [Name](#cfn-route53recoverycontrol-cluster-name): String
  [Tags](#cfn-route53recoverycontrol-cluster-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-route53recoverycontrol-cluster-properties"></a>

`Name`  <a name="cfn-route53recoverycontrol-cluster-name"></a>
Name of the cluster\. You can use any non\-white space character in the name\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-route53recoverycontrol-cluster-tags"></a>
The value for a tag\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-route53recoverycontrol-cluster-return-values"></a>

### Ref<a name="aws-resource-route53recoverycontrol-cluster-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the `ClusterArn` object\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-route53recoverycontrol-cluster-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-route53recoverycontrol-cluster-return-values-fn--getatt-fn--getatt"></a>

`ClusterArn`  <a name="ClusterArn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the cluster\.

`ClusterEndpoints`  <a name="ClusterEndpoints-fn::getatt"></a>
Endpoints for the cluster\. 

`Status`  <a name="Status-fn::getatt"></a>
Deployment status of a resource\. Status can be one of the following: PENDING, DEPLOYED, PENDING\_DELETION\.