# Amazon EMR Cluster KerberosAttributes<a name="aws-properties-elasticmapreduce-cluster-kerberosattributes"></a>

<a name="aws-properties-elasticmapreduce-cluster-kerberosattributes-description"></a>The `KerberosAttributes` property type specifies attributes for Kerberos configuration when Kerberos authentication is enabled using a security configuration\.

<a name="aws-properties-elasticmapreduce-cluster-kerberosattributes-inheritance"></a> `KerberosAttributes` is a property of the [AWS::EMR::Cluster](aws-resource-emr-cluster.md) resource\.

## Syntax<a name="aws-properties-elasticmapreduce-cluster-kerberosattributes-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-elasticmapreduce-cluster-kerberosattributes-syntax.json"></a>

```
{
  "[ADDomainJoinPassword](#cfn-elasticmapreduce-cluster-kerberosattributes-addomainjoinpassword)" : String,
  "[ADDomainJoinUser](#cfn-elasticmapreduce-cluster-kerberosattributes-addomainjoinuser)" : String,
  "[CrossRealmTrustPrincipalPassword](#cfn-elasticmapreduce-cluster-kerberosattributes-crossrealmtrustprincipalpassword)" : String,
  "[KdcAdminPassword](#cfn-elasticmapreduce-cluster-kerberosattributes-kdcadminpassword)" : String,
  "[Realm](#cfn-elasticmapreduce-cluster-kerberosattributes-realm)" : String
}
```

### YAML<a name="aws-properties-elasticmapreduce-cluster-kerberosattributes-syntax.yaml"></a>

```
[ADDomainJoinPassword](#cfn-elasticmapreduce-cluster-kerberosattributes-addomainjoinpassword): String
[ADDomainJoinUser](#cfn-elasticmapreduce-cluster-kerberosattributes-addomainjoinuser): String
[CrossRealmTrustPrincipalPassword](#cfn-elasticmapreduce-cluster-kerberosattributes-crossrealmtrustprincipalpassword): String
[KdcAdminPassword](#cfn-elasticmapreduce-cluster-kerberosattributes-kdcadminpassword): String
[Realm](#cfn-elasticmapreduce-cluster-kerberosattributes-realm): String
```

## Properties<a name="aws-properties-elasticmapreduce-cluster-kerberosattributes-properties"></a>

`ADDomainJoinPassword`  <a name="cfn-elasticmapreduce-cluster-kerberosattributes-addomainjoinpassword"></a>
The Active Directory password for `ADDomainJoinUser`\.  
Length Constraints: Minimum length of 0\. Maximum length of 256\.  
Pattern: \[\\u0020\-\\uD7FF\\uE000\-\\uFFFD\\uD800\\uDC00\-\\uDBFF\\uDFFF\\r\\n\\t\]\*  
 *Required*: No  
 *Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`ADDomainJoinUser`  <a name="cfn-elasticmapreduce-cluster-kerberosattributes-addomainjoinuser"></a>
Required only when establishing a cross\-realm trust with an Active Directory domain\. A user with sufficient privileges to join resources to the domain\.  
Length Constraints: Minimum length of 0\. Maximum length of 256\.  
Pattern: \[\\u0020\-\\uD7FF\\uE000\-\\uFFFD\\uD800\\uDC00\-\\uDBFF\\uDFFF\\r\\n\\t\]\*  
 *Required*: No  
 *Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`CrossRealmTrustPrincipalPassword`  <a name="cfn-elasticmapreduce-cluster-kerberosattributes-crossrealmtrustprincipalpassword"></a>
Required only when establishing a cross\-realm trust with a KDC in a different realm\. The cross\-realm principal password, which must be identical across realms\.  
Length Constraints: Minimum length of 0\. Maximum length of 256\.  
Pattern: \[\\u0020\-\\uD7FF\\uE000\-\\uFFFD\\uD800\\uDC00\-\\uDBFF\\uDFFF\\r\\n\\t\]\*  
 *Required*: No  
 *Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`KdcAdminPassword`  <a name="cfn-elasticmapreduce-cluster-kerberosattributes-kdcadminpassword"></a>
The password used within the cluster for the kadmin service on the cluster\-dedicated KDC, which maintains Kerberos principals, password policies, and keytabs for the cluster\.  
Length Constraints: Minimum length of 0\. Maximum length of 256\.  
Pattern: \[\\u0020\-\\uD7FF\\uE000\-\\uFFFD\\uD800\\uDC00\-\\uDBFF\\uDFFF\\r\\n\\t\]\*  
 *Required*: Yes  
 *Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

`Realm`  <a name="cfn-elasticmapreduce-cluster-kerberosattributes-realm"></a>
The name of the Kerberos realm to which all nodes in a cluster belong\. For example, `EC2.INTERNAL`\.  
Length Constraints: Minimum length of 0\. Maximum length of 256\.  
Pattern: \[\\u0020\-\\uD7FF\\uE000\-\\uFFFD\\uD800\\uDC00\-\\uDBFF\\uDFFF\\r\\n\\t\]\*  
 *Required*: Yes  
 *Type*: String  
*Update requires*: [No interruption](using-cfn-updating-stacks-update-behaviors.md#update-no-interrupt)

## See Also<a name="aws-properties-elasticmapreduce-cluster-kerberosattributes-seealso"></a>
+ [KerberosAttributes](https://docs.aws.amazon.com/ElasticMapReduce/latest/API/API_KerberosAttributes.html) in the *Amazon EMR API Reference*
+ [Use Kerberos Authentication](https://docs.aws.amazon.com/emr/latest/ManagementGuide/emr-kerberos.html) in the *Amazon EMR Management Guide*