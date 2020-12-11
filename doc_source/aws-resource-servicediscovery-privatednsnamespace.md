# AWS::ServiceDiscovery::PrivateDnsNamespace<a name="aws-resource-servicediscovery-privatednsnamespace"></a>

Creates a private namespace based on DNS, which will be visible only inside a specified Amazon VPC\. The namespace defines your service naming scheme\. For example, if you name your namespace `example.com` and name your service `backend`, the resulting DNS name for the service will be `backend.example.com`\. For the current quota on the number of namespaces that you can create using the same AWS account, see [AWS Cloud Map Limits](https://docs.aws.amazon.com/cloud-map/latest/dg/cloud-map-limits.html) in the *AWS Cloud Map Developer Guide*\.

## Syntax<a name="aws-resource-servicediscovery-privatednsnamespace-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-servicediscovery-privatednsnamespace-syntax.json"></a>

```
{
  "Type" : "AWS::ServiceDiscovery::PrivateDnsNamespace",
  "Properties" : {
      "[Description](#cfn-servicediscovery-privatednsnamespace-description)" : String,
      "[Name](#cfn-servicediscovery-privatednsnamespace-name)" : String,
      "[Tags](#cfn-servicediscovery-privatednsnamespace-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ],
      "[Vpc](#cfn-servicediscovery-privatednsnamespace-vpc)" : String
    }
}
```

### YAML<a name="aws-resource-servicediscovery-privatednsnamespace-syntax.yaml"></a>

```
Type: AWS::ServiceDiscovery::PrivateDnsNamespace
Properties: 
  [Description](#cfn-servicediscovery-privatednsnamespace-description): String
  [Name](#cfn-servicediscovery-privatednsnamespace-name): String
  [Tags](#cfn-servicediscovery-privatednsnamespace-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
  [Vpc](#cfn-servicediscovery-privatednsnamespace-vpc): String
```

## Properties<a name="aws-resource-servicediscovery-privatednsnamespace-properties"></a>

`Description`  <a name="cfn-servicediscovery-privatednsnamespace-description"></a>
A description for the namespace\.  
*Required*: No  
*Type*: String  
*Maximum*: `1024`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Name`  <a name="cfn-servicediscovery-privatednsnamespace-name"></a>
The name that you want to assign to this namespace\. When you create a private DNS namespace, AWS Cloud Map automatically creates an Amazon Route 53 private hosted zone that has the same name as the namespace\.  
*Required*: Yes  
*Type*: String  
*Maximum*: `1024`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-servicediscovery-privatednsnamespace-tags"></a>
The tags for the namespace\. Each tag consists of a key and an optional value, both of which you define\. Tag keys can have a maximum character length of 128 characters, and tag values can have a maximum length of 256 characters\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Maximum*: `200`  
*Update requires*: Updates are not supported\.

`Vpc`  <a name="cfn-servicediscovery-privatednsnamespace-vpc"></a>
The ID of the Amazon VPC that you want to associate the namespace with\.  
*Required*: Yes  
*Type*: String  
*Maximum*: `64`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

## Return values<a name="aws-resource-servicediscovery-privatednsnamespace-return-values"></a>

### Ref<a name="aws-resource-servicediscovery-privatednsnamespace-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the value of `Id` for the namespace, such as `ns-e4anhexample0004`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-servicediscovery-privatednsnamespace-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-servicediscovery-privatednsnamespace-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the private namespace\.

`Id`  <a name="Id-fn::getatt"></a>
The ID of the private namespace\.

## Examples<a name="aws-resource-servicediscovery-privatednsnamespace--examples"></a>



### Create a private DNS namespace<a name="aws-resource-servicediscovery-privatednsnamespace--examples--Create_a_private_DNS_namespace"></a>

The following example creates a private DNS namespace named `private-example.com`\.

#### JSON<a name="aws-resource-servicediscovery-privatednsnamespace--examples--Create_a_private_DNS_namespace--json"></a>

```
{
  "Type" : "AWS::ServiceDiscovery::PrivateDnsNamespace",
  "Properties" : {
    "Description" : "AWS Cloud Map private DNS namespace for resources for example.com website",
    "Vpc" : "vpc-12345678",
    "Name" : "private-example.com"
  }
}
```

#### YAML<a name="aws-resource-servicediscovery-privatednsnamespace--examples--Create_a_private_DNS_namespace--yaml"></a>

```
Type: 'AWS::ServiceDiscovery::PrivateDnsNamespace'
Properties:
  Description: AWS Cloud Map private DNS namespace for resources for example.com website
  Vpc: vpc-12345678
  Name: private-example.com
```

## See also<a name="aws-resource-servicediscovery-privatednsnamespace--seealso"></a>
+  [CreatePrivateDnsNamespace](https://docs.aws.amazon.com/cloud-map/latest/api/API_CreatePrivateDnsNamespace.html) in the *AWS Cloud Map API Reference* 

