# AWS::Redshift::EndpointAuthorization<a name="aws-resource-redshift-endpointauthorization"></a>

Describes an endpoint authorization for authorizing Redshift\-managed VPC endpoint access to a cluster across AWS accounts\.

## Syntax<a name="aws-resource-redshift-endpointauthorization-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-redshift-endpointauthorization-syntax.json"></a>

```
{
  "Type" : "AWS::Redshift::EndpointAuthorization",
  "Properties" : {
      "[Account](#cfn-redshift-endpointauthorization-account)" : String,
      "[ClusterIdentifier](#cfn-redshift-endpointauthorization-clusteridentifier)" : String,
      "[Force](#cfn-redshift-endpointauthorization-force)" : Boolean,
      "[VpcIds](#cfn-redshift-endpointauthorization-vpcids)" : [ String, ... ]
    }
}
```

### YAML<a name="aws-resource-redshift-endpointauthorization-syntax.yaml"></a>

```
Type: AWS::Redshift::EndpointAuthorization
Properties: 
  [Account](#cfn-redshift-endpointauthorization-account): String
  [ClusterIdentifier](#cfn-redshift-endpointauthorization-clusteridentifier): String
  [Force](#cfn-redshift-endpointauthorization-force): Boolean
  [VpcIds](#cfn-redshift-endpointauthorization-vpcids): 
    - String
```

## Properties<a name="aws-resource-redshift-endpointauthorization-properties"></a>

`Account`  <a name="cfn-redshift-endpointauthorization-account"></a>
The AWS account ID of either the cluster owner \(grantor\) or grantee\. If `Grantee` parameter is true, then the `Account` value is of the grantor\.  
*Required*: Yes  
*Type*: String  
*Maximum*: `2147483647`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ClusterIdentifier`  <a name="cfn-redshift-endpointauthorization-clusteridentifier"></a>
The cluster identifier\.  
*Required*: Yes  
*Type*: String  
*Maximum*: `2147483647`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Force`  <a name="cfn-redshift-endpointauthorization-force"></a>
Indicates whether to force the revoke action\. If true, the Redshift\-managed VPC endpoints associated with the endpoint authorization are also deleted\.  
*Required*: No  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VpcIds`  <a name="cfn-redshift-endpointauthorization-vpcids"></a>
The virtual private cloud \(VPC\) identifiers to grant access to\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-redshift-endpointauthorization-return-values"></a>

### Fn::GetAtt<a name="aws-resource-redshift-endpointauthorization-return-values-fn--getatt"></a>

#### <a name="aws-resource-redshift-endpointauthorization-return-values-fn--getatt-fn--getatt"></a>

`AllowedAllVPCs`  <a name="AllowedAllVPCs-fn::getatt"></a>
Indicates whether all VPCs in the grantee account are allowed access to the cluster\.

`AllowedVPCs`  <a name="AllowedVPCs-fn::getatt"></a>
The VPCs allowed access to the cluster\.

`AuthorizeTime`  <a name="AuthorizeTime-fn::getatt"></a>
The time \(UTC\) when the authorization was created\.

`ClusterStatus`  <a name="ClusterStatus-fn::getatt"></a>
The status of the cluster\.

`EndpointCount`  <a name="EndpointCount-fn::getatt"></a>
The number of Redshift\-managed VPC endpoints created for the authorization\.

`Grantee`  <a name="Grantee-fn::getatt"></a>
The AWS account ID of the grantee of the cluster\.

`Grantor`  <a name="Grantor-fn::getatt"></a>
The AWS account ID of the cluster owner\.

`Status`  <a name="Status-fn::getatt"></a>
The status of the authorization action\.