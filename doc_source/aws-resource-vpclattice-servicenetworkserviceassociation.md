# AWS::VpcLattice::ServiceNetworkServiceAssociation<a name="aws-resource-vpclattice-servicenetworkserviceassociation"></a>

Associates a service with a service network\.

You can't use this operation if the service and service network are already associated or if there is a disassociation or deletion in progress\. If the association fails, you can retry the operation by deleting the association and recreating it\.

You cannot associate a service and service network that are shared with a caller\. The caller must own either the service or the service network\.

As a result of this operation, the association is created in the service network account and the association owner account\.

## Syntax<a name="aws-resource-vpclattice-servicenetworkserviceassociation-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-vpclattice-servicenetworkserviceassociation-syntax.json"></a>

```
{
  "Type" : "AWS::VpcLattice::ServiceNetworkServiceAssociation",
  "Properties" : {
      "[DnsEntry](#cfn-vpclattice-servicenetworkserviceassociation-dnsentry)" : DnsEntry,
      "[ServiceIdentifier](#cfn-vpclattice-servicenetworkserviceassociation-serviceidentifier)" : String,
      "[ServiceNetworkIdentifier](#cfn-vpclattice-servicenetworkserviceassociation-servicenetworkidentifier)" : String,
      "[Tags](#cfn-vpclattice-servicenetworkserviceassociation-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ]
    }
}
```

### YAML<a name="aws-resource-vpclattice-servicenetworkserviceassociation-syntax.yaml"></a>

```
Type: AWS::VpcLattice::ServiceNetworkServiceAssociation
Properties: 
  [DnsEntry](#cfn-vpclattice-servicenetworkserviceassociation-dnsentry): 
    DnsEntry
  [ServiceIdentifier](#cfn-vpclattice-servicenetworkserviceassociation-serviceidentifier): String
  [ServiceNetworkIdentifier](#cfn-vpclattice-servicenetworkserviceassociation-servicenetworkidentifier): String
  [Tags](#cfn-vpclattice-servicenetworkserviceassociation-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
```

## Properties<a name="aws-resource-vpclattice-servicenetworkserviceassociation-properties"></a>

`DnsEntry`  <a name="cfn-vpclattice-servicenetworkserviceassociation-dnsentry"></a>
Property description not available\.  
*Required*: No  
*Type*: [DnsEntry](aws-properties-vpclattice-servicenetworkserviceassociation-dnsentry.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ServiceIdentifier`  <a name="cfn-vpclattice-servicenetworkserviceassociation-serviceidentifier"></a>
The ID or Amazon Resource Name \(ARN\) of the service\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ServiceNetworkIdentifier`  <a name="cfn-vpclattice-servicenetworkserviceassociation-servicenetworkidentifier"></a>
The ID or Amazon Resource Name \(ARN\) of the service network\. You must use the ARN if the resources specified in the operation are in different accounts\.  
*Required*: No  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-vpclattice-servicenetworkserviceassociation-tags"></a>
The tags for the association\.  
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-vpclattice-servicenetworkserviceassociation-return-values"></a>

### Ref<a name="aws-resource-vpclattice-servicenetworkserviceassociation-return-values-ref"></a>

When you pass the logical ID of this resource to the intrinsic `Ref` function, `Ref` returns the Amazon Resource Name \(ARN\) of the association\.

For more information about using the `Ref` function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-vpclattice-servicenetworkserviceassociation-return-values-fn--getatt"></a>

The `Fn::GetAtt` intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt` intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-vpclattice-servicenetworkserviceassociation-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the association between the service network and the service\.

`CreatedAt`  <a name="CreatedAt-fn::getatt"></a>
The date and time that the association was created, specified in ISO\-8601 format\.

`DnsEntry.DomainName`  <a name="DnsEntry.DomainName-fn::getatt"></a>
The domain name of the service\.

`DnsEntry.HostedZoneId`  <a name="DnsEntry.HostedZoneId-fn::getatt"></a>
The ID of the hosted zone\.

`Id`  <a name="Id-fn::getatt"></a>
The ID of the of the association between the service network and the service\.

`ServiceArn`  <a name="ServiceArn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the service\.

`ServiceId`  <a name="ServiceId-fn::getatt"></a>
The ID of the service\.

`ServiceName`  <a name="ServiceName-fn::getatt"></a>
The name of the service\.

`ServiceNetworkArn`  <a name="ServiceNetworkArn-fn::getatt"></a>
The Amazon Resource Name \(ARN\) of the service network

`ServiceNetworkId`  <a name="ServiceNetworkId-fn::getatt"></a>
The ID of the service network\.

`ServiceNetworkName`  <a name="ServiceNetworkName-fn::getatt"></a>
The name of the service network\.

`Status`  <a name="Status-fn::getatt"></a>
The status of the association between the service network and the service\.