# AWS::AppMesh::VirtualNode AwsCloudMapServiceDiscovery<a name="aws-properties-appmesh-virtualnode-awscloudmapservicediscovery"></a>

An object that represents the AWS Cloud Map service discovery information for your virtual node\.

**Note**  
AWS Cloud Map is not available in the eu\-south\-1 Region\.

## Syntax<a name="aws-properties-appmesh-virtualnode-awscloudmapservicediscovery-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-appmesh-virtualnode-awscloudmapservicediscovery-syntax.json"></a>

```
{
  "[Attributes](#cfn-appmesh-virtualnode-awscloudmapservicediscovery-attributes)" : [ AwsCloudMapInstanceAttribute, ... ],
  "[NamespaceName](#cfn-appmesh-virtualnode-awscloudmapservicediscovery-namespacename)" : String,
  "[ServiceName](#cfn-appmesh-virtualnode-awscloudmapservicediscovery-servicename)" : String
}
```

### YAML<a name="aws-properties-appmesh-virtualnode-awscloudmapservicediscovery-syntax.yaml"></a>

```
  [Attributes](#cfn-appmesh-virtualnode-awscloudmapservicediscovery-attributes): 
    - AwsCloudMapInstanceAttribute
  [NamespaceName](#cfn-appmesh-virtualnode-awscloudmapservicediscovery-namespacename): String
  [ServiceName](#cfn-appmesh-virtualnode-awscloudmapservicediscovery-servicename): String
```

## Properties<a name="aws-properties-appmesh-virtualnode-awscloudmapservicediscovery-properties"></a>

`Attributes`  <a name="cfn-appmesh-virtualnode-awscloudmapservicediscovery-attributes"></a>
A string map that contains attributes with values that you can use to filter instances by any custom attribute that you specified when you registered the instance\. Only instances that match all of the specified key/value pairs will be returned\.  
*Required*: No  
*Type*: List of [AwsCloudMapInstanceAttribute](aws-properties-appmesh-virtualnode-awscloudmapinstanceattribute.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NamespaceName`  <a name="cfn-appmesh-virtualnode-awscloudmapservicediscovery-namespacename"></a>
The name of the AWS Cloud Map namespace to use\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ServiceName`  <a name="cfn-appmesh-virtualnode-awscloudmapservicediscovery-servicename"></a>
The name of the AWS Cloud Map service to use\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)