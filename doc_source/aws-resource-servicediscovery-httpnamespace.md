# AWS::ServiceDiscovery::HttpNamespace<a name="aws-resource-servicediscovery-httpnamespace"></a>

The `HttpNamespace` resource is an AWS Cloud Map resource type that contains information about an HTTP namespace\. Service instances that you register using an HTTP namespace can be discovered using a `DiscoverInstances` request but can't be discovered using DNS\. 

For the current quota on the number of namespaces that you can create using the same AWS account, see [AWS Cloud Map quotas](https://docs.aws.amazon.com/cloud-map/latest/dg/cloud-map-limits.html) in the *AWS Cloud Map Developer Guide*\.

## Syntax<a name="aws-resource-servicediscovery-httpnamespace-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-servicediscovery-httpnamespace-syntax.json"></a>

```
{
  "Type" : "AWS::ServiceDiscovery::HttpNamespace",
  "Properties" : {
      "[Description](#cfn-servicediscovery-httpnamespace-description)" : String,
      "[Name](#cfn-servicediscovery-httpnamespace-name)" : String,
      "[Tags](#cfn-servicediscovery-httpnamespace-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-servicediscovery-httpnamespace-syntax.yaml"></a>

```
Type: AWS::ServiceDiscovery::HttpNamespace
Properties: 
  [Description](#cfn-servicediscovery-httpnamespace-description): String
  [Name](#cfn-servicediscovery-httpnamespace-name): String
  [Tags](#cfn-servicediscovery-httpnamespace-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-servicediscovery-httpnamespace-properties"></a>

`Description`  <a name="cfn-servicediscovery-httpnamespace-description"></a>
A description for the namespace\.  
*Required*: No  
*Type*: String  
*Maximum*: `1024`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Name`  <a name="cfn-servicediscovery-httpnamespace-name"></a>
The name that you want to assign to this namespace\.  
*Required*: Yes  
*Type*: String  
*Maximum*: `1024`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-servicediscovery-httpnamespace-tags"></a>
The tags for the namespace\. Each tag consists of a key and an optional value, both of which you define\. Tag keys can have a maximum character length of 128 characters, and tag values can have a maximum length of 256 characters\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Maximum*: `200`  
*Update requires*: Updates are not supported\.

## Return values<a name="aws-resource-servicediscovery-httpnamespace-return-values"></a>

### Ref<a name="aws-resource-servicediscovery-httpnamespace-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the `Id` for the namespace, such as `ns-e4anhexample0004`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-servicediscovery-httpnamespace-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-servicediscovery-httpnamespace-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the namespace, such as `arn:aws:service-discovery:us-east-1:123456789012:http-namespace/http-namespace-a1bzhi`\.

`Id`  <a name="Id-fn::getatt"></a>
The ID of the namespace\.

## Examples<a name="aws-resource-servicediscovery-httpnamespace--examples"></a>



### Create an HTTP namespace<a name="aws-resource-servicediscovery-httpnamespace--examples--Create_an_HTTP_namespace"></a>

The following example creates an HTTP namespace named `example-namespace`\.

#### JSON<a name="aws-resource-servicediscovery-httpnamespace--examples--Create_an_HTTP_namespace--json"></a>

```
{
  "Type" : "AWS::ServiceDiscovery::HttpNamespace",
  "Properties" : {
    "Description" : "AWS Cloud Map HTTP namespace for resources for example.com website",
    "Name" : "example-namespace"
  }
}
```

#### YAML<a name="aws-resource-servicediscovery-httpnamespace--examples--Create_an_HTTP_namespace--yaml"></a>

```
Type: 'AWS::ServiceDiscovery::HttpNamespace'
Properties:
  Description: AWS Cloud Map HTTP namespace for resources for example.com website
  Name: example-namespace
```

## See also<a name="aws-resource-servicediscovery-httpnamespace--seealso"></a>
+  [CreateHttpNamespace](https://docs.aws.amazon.com/cloud-map/latest/api/API_CreateHttpNamespace.html) in the *AWS Cloud Map API Reference* 

