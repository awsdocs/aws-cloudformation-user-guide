# AWS::ServiceDiscovery::HttpNamespace<a name="aws-resource-servicediscovery-httpnamespace"></a>

The `AWS::ServiceDiscovery::HttpNamespace` resource specifies values for an AWS Cloud Map HTTP namespace\. For more information, see [CreateHttpNamespace](https://docs.aws.amazon.com/cloud-map/latest/api/API_CreateHttpNamespace.html) in the *AWS Cloud Map API Reference*\. 

## Syntax<a name="aws-resource-servicediscovery-httpnamespace-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-servicediscovery-httpnamespace-syntax.json"></a>

```
{
  "Type" : "AWS::ServiceDiscovery::HttpNamespace",
  "Properties" : {
    "[Description](#cfn-servicediscovery-httpnamespace-description)" : String,
    "[Name](#cfn-servicediscovery-httpnamespace-name)" : String
  }
}
```

### YAML<a name="aws-resource-servicediscovery-httpnamespace-syntax.yaml"></a>

```
Type: "AWS::ServiceDiscovery::HttpNamespace"
Properties:
  [Description](#cfn-servicediscovery-httpnamespace-description): String
  [Name](#cfn-servicediscovery-httpnamespace-name): String
```

## Properties<a name="aws-resource-servicediscovery-httpnamespace-properties"></a>

`Description`  <a name="cfn-servicediscovery-httpnamespace-description"></a>
A description of the namespace\.  
 *Required*: No  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

`Name`  <a name="cfn-servicediscovery-httpnamespace-name"></a>
A name for the namespace\.  
 *Required*: Yes  
 *Type*: String  
 *Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement) 

## Return Values<a name="aws-resource-servicediscovery-httpnamespace-returnvalues"></a>

### Ref<a name="aws-resource-servicediscovery-httpnamespace-ref"></a>

When you pass the logical ID of an `AWS::ServiceDiscovery::HttpNamespace` resource to the intrinsic `Ref` function, the function returns the `Id` for the namespace\. 

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\. 

### Fn::GetAtt<a name="aws-resource-servicediscovery-httpnamespace-getatt"></a>

 `Fn::GetAtt` returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\. 

`Arn`  
The Amazon Resource Name \(ARN\) of the namespace, such as `arn:aws:service-discovery:us-east-1:123456789012:http-namespace/http-namespace-a1bzhi`\.

`Id`  
The ID of the namespace\.

For more information about using `Fn::GetAtt`, see [Fn::GetAtt](intrinsic-function-reference-getatt.md)\. 

## See Also<a name="aws-resource-servicediscovery-httpnamespace-seealso"></a>
+ [CreateHttpNamespace](https://docs.aws.amazon.com/cloud-map/latest/api/API_CreateHttpNamespace.html) in the *AWS Cloud Map API Reference*