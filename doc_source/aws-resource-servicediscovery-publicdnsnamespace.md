# AWS::ServiceDiscovery::PublicDnsNamespace<a name="aws-resource-servicediscovery-publicdnsnamespace"></a>

Creates a public namespace based on DNS, which will be visible on the internet\. The namespace defines your service naming scheme\. For example, if you name your namespace `example.com` and name your service `backend`, the resulting DNS name for the service will be `backend.example.com`\. For the current quota on the number of namespaces that you can create using the same AWS account, see [AWS Cloud Map Limits](https://docs.aws.amazon.com/cloud-map/latest/dg/cloud-map-limits.html) in the *AWS Cloud Map Developer Guide*\.

## Syntax<a name="aws-resource-servicediscovery-publicdnsnamespace-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-servicediscovery-publicdnsnamespace-syntax.json"></a>

```
{
  "Type" : "AWS::ServiceDiscovery::PublicDnsNamespace",
  "Properties" : {
      "[Description](#cfn-servicediscovery-publicdnsnamespace-description)" : String,
      "[Name](#cfn-servicediscovery-publicdnsnamespace-name)" : String,
      "[Tags](#cfn-servicediscovery-publicdnsnamespace-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-servicediscovery-publicdnsnamespace-syntax.yaml"></a>

```
Type: AWS::ServiceDiscovery::PublicDnsNamespace
Properties: 
  [Description](#cfn-servicediscovery-publicdnsnamespace-description): String
  [Name](#cfn-servicediscovery-publicdnsnamespace-name): String
  [Tags](#cfn-servicediscovery-publicdnsnamespace-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-servicediscovery-publicdnsnamespace-properties"></a>

`Description`  <a name="cfn-servicediscovery-publicdnsnamespace-description"></a>
A description for the namespace\.  
*Required*: No  
*Type*: String  
*Maximum*: `1024`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Name`  <a name="cfn-servicediscovery-publicdnsnamespace-name"></a>
The name that you want to assign to this namespace\.  
*Required*: Yes  
*Type*: String  
*Maximum*: `1024`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-servicediscovery-publicdnsnamespace-tags"></a>
The tags for the namespace\. Each tag consists of a key and an optional value, both of which you define\. Tag keys can have a maximum character length of 128 characters, and tag values can have a maximum length of 256 characters\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Maximum*: `200`  
*Update requires*: Updates are not supported\.

## Return values<a name="aws-resource-servicediscovery-publicdnsnamespace-return-values"></a>

### Ref<a name="aws-resource-servicediscovery-publicdnsnamespace-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the value of `Id` for the namespace, such as `ns-e4anhexample0004`\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-servicediscovery-publicdnsnamespace-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-servicediscovery-publicdnsnamespace-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the public namespace\.

`Id`  <a name="Id-fn::getatt"></a>
The ID of the public namespace\.

## Examples<a name="aws-resource-servicediscovery-publicdnsnamespace--examples"></a>



### Create a public DNS namespace<a name="aws-resource-servicediscovery-publicdnsnamespace--examples--Create_a_public_DNS_namespace"></a>

The following example creates a public DNS namespace named `example.com`\.

#### JSON<a name="aws-resource-servicediscovery-publicdnsnamespace--examples--Create_a_public_DNS_namespace--json"></a>

```
{
"Type" : "AWS::ServiceDiscovery::PublicDnsNamespace",
"Properties" : {
  "Description" : "AWS Cloud Map public DNS namespace for example.com website",
  "Name" : "example.com"
  }
}
```

#### YAML<a name="aws-resource-servicediscovery-publicdnsnamespace--examples--Create_a_public_DNS_namespace--yaml"></a>

```
Type: 'AWS::ServiceDiscovery::PublicDnsNamespace'
Properties:
  Description: AWS Cloud Map public DNS namespace for example.com website
  Name: example.com
```

## See also<a name="aws-resource-servicediscovery-publicdnsnamespace--seealso"></a>
+  [CreatePublicDnsNamespace](https://docs.aws.amazon.com/cloud-map/latest/api/API_CreatePublicDnsNamespace.html) in the *AWS Cloud Map API Reference* 

