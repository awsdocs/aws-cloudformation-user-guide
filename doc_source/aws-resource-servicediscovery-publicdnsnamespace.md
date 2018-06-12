# AWS::ServiceDiscovery::PublicDnsNamespace<a name="aws-resource-servicediscovery-publicdnsnamespace"></a>

The `AWS::ServiceDiscovery::PublicDnsNamespace` resource specifies information about a public namespace for Amazon Route 53\. Use a public namespace when you want to route internet traffic to your resources\. For more information, see [CreatePublicDnsNamespace](http://docs.aws.amazon.com/Route53/latest/APIReference/API_autonaming_CreatePublicDnsNamespace.html) in the *Amazon Route 53 API Reference*\.

**Topics**
+ [Syntax](#aws-resource-servicediscovery-publicdnsnamespace-syntax)
+ [Properties](#aws-resource-servicediscovery-publicdnsnamespace-properties)
+ [Return Values](#aws-resource-servicediscovery-publicdnsnamespace-returnvalues)
+ [See Also](#aws-resource-servicediscovery-publicdnsnamespace-seealso)

## Syntax<a name="aws-resource-servicediscovery-publicdnsnamespace-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-servicediscovery-publicdnsnamespace-syntax.json"></a>

```
{
  "Type" : "AWS::ServiceDiscovery::PublicDnsNamespace",
  "Properties" : {
    "[Description](#cfn-servicediscovery-publicdnsnamespace-description)" : String,
    "[Name](#cfn-servicediscovery-publicdnsnamespace-name)" : String
  }
}
```

### YAML<a name="aws-resource-servicediscovery-publicdnsnamespace-syntax.yaml"></a>

```
Type: "AWS::ServiceDiscovery::PublicDnsNamespace"
Properties:
  [Description](#cfn-servicediscovery-publicdnsnamespace-description): String
  [Name](#cfn-servicediscovery-publicdnsnamespace-name): String
```

## Properties<a name="aws-resource-servicediscovery-publicdnsnamespace-properties"></a>

`Description`  <a name="cfn-servicediscovery-publicdnsnamespace-description"></a>
A description for the namespace\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

`Name`  <a name="cfn-servicediscovery-publicdnsnamespace-name"></a>
The name that you want to assign to this namespace\. When you create a namespace, Route 53 automatically creates a hosted zone that has the same name as the namespace\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](using-cfn-updating-stacks-update-behaviors.md#update-replacement)

## Return Values<a name="aws-resource-servicediscovery-publicdnsnamespace-returnvalues"></a>

### Ref<a name="aws-resource-servicediscovery-publicdnsnamespace-ref"></a>

When you pass the logical ID of an `AWS::ServiceDiscovery::PublicDnsNamespace` resource to the intrinsic `Ref` function, the function returns the value of `Id` for the namespace\.

For more information about using the `Ref` function, see [Ref](intrinsic-function-reference-ref.md)\.

### Fn::GetAtt<a name="aws-resource-servicediscovery-publicdnsnamespace-getatt"></a>

 `Fn::GetAtt` returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

`Id`  
The ID of the public namespace\.

`Arn`  
The Amazon Resource Name \(ARN\) of the public namespace\.

For more information about using `Fn::GetAtt`, see [Fn::GetAtt](intrinsic-function-reference-getatt.md)\. 

## See Also<a name="aws-resource-servicediscovery-publicdnsnamespace-seealso"></a>
+ [Using Autonaming for Service Discovery](http://docs.aws.amazon.com/Route53/latest/APIReference/overview-service-discovery.html) in the *Amazon Route 53 API Reference*
+ [CreatePublicDnsNamespace](http://docs.aws.amazon.com/Route53/latest/APIReference/API_autonaming_CreatePublicDnsNamespace.html) in the *Amazon Route 53 API Reference*