# AWS::EKS::Cluster<a name="aws-resource-eks-cluster"></a>

Creates an Amazon EKS control plane\. 

The Amazon EKS control plane consists of control plane instances that run the Kubernetes software, such as `etcd` and the API server\. The control plane runs in an account managed by AWS, and the Kubernetes API is exposed by the Amazon EKS API server endpoint\. Each Amazon EKS cluster control plane is single tenant and unique\. It runs on its own set of Amazon EC2 instances\.

The cluster control plane is provisioned across multiple Availability Zones and fronted by an Elastic Load Balancing Network Load Balancer\. Amazon EKS also provisions elastic network interfaces in your VPC subnets to provide connectivity from the control plane instances to the nodes \(for example, to support `kubectl exec`, `logs`, and `proxy` data flows\)\.

Amazon EKS nodes run in your AWS account and connect to your cluster's control plane over the Kubernetes API server endpoint and a certificate file that is created for your cluster\.

In most cases, it takes several minutes to create a cluster\. After you create an Amazon EKS cluster, you must configure your Kubernetes tooling to communicate with the API server and launch nodes into your cluster\. For more information, see [Managing Cluster Authentication](https://docs.aws.amazon.com/eks/latest/userguide/managing-auth.html) and [Launching Amazon EKS nodes](https://docs.aws.amazon.com/eks/latest/userguide/launch-workers.html) in the *Amazon EKS User Guide*\.

## Syntax<a name="aws-resource-eks-cluster-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-eks-cluster-syntax.json"></a>

```
{
  "Type" : "AWS::EKS::Cluster",
  "Properties" : {
      "[EncryptionConfig](#cfn-eks-cluster-encryptionconfig)" : [ EncryptionConfig, ... ],
      "[KubernetesNetworkConfig](#cfn-eks-cluster-kubernetesnetworkconfig)" : KubernetesNetworkConfig,
      "[Logging](#cfn-eks-cluster-logging)" : Logging,
      "[Name](#cfn-eks-cluster-name)" : String,
      "[OutpostConfig](#cfn-eks-cluster-outpostconfig)" : OutpostConfig,
      "[ResourcesVpcConfig](#cfn-eks-cluster-resourcesvpcconfig)" : ResourcesVpcConfig,
      "[RoleArn](#cfn-eks-cluster-rolearn)" : String,
      "[Tags](#cfn-eks-cluster-tags)" : [ [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html), ... ],
      "[Version](#cfn-eks-cluster-version)" : String
    }
}
```

### YAML<a name="aws-resource-eks-cluster-syntax.yaml"></a>

```
Type: AWS::EKS::Cluster
Properties: 
  [EncryptionConfig](#cfn-eks-cluster-encryptionconfig): 
    - EncryptionConfig
  [KubernetesNetworkConfig](#cfn-eks-cluster-kubernetesnetworkconfig): 
    KubernetesNetworkConfig
  [Logging](#cfn-eks-cluster-logging): 
    Logging
  [Name](#cfn-eks-cluster-name): String
  [OutpostConfig](#cfn-eks-cluster-outpostconfig): 
    OutpostConfig
  [ResourcesVpcConfig](#cfn-eks-cluster-resourcesvpcconfig): 
    ResourcesVpcConfig
  [RoleArn](#cfn-eks-cluster-rolearn): String
  [Tags](#cfn-eks-cluster-tags): 
    - [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)
  [Version](#cfn-eks-cluster-version): String
```

## Properties<a name="aws-resource-eks-cluster-properties"></a>

`EncryptionConfig`  <a name="cfn-eks-cluster-encryptionconfig"></a>
The encryption configuration for the cluster\.  
*Required*: No  
*Type*: [List](aws-properties-eks-cluster-encryptionconfig.md) of [EncryptionConfig](aws-properties-eks-cluster-encryptionconfig.md)  
*Maximum*: `1`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`KubernetesNetworkConfig`  <a name="cfn-eks-cluster-kubernetesnetworkconfig"></a>
The Kubernetes network configuration for the cluster\.  
*Required*: No  
*Type*: [KubernetesNetworkConfig](aws-properties-eks-cluster-kubernetesnetworkconfig.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Logging`  <a name="cfn-eks-cluster-logging"></a>
The logging configuration for your cluster\.  
*Required*: No  
*Type*: [Logging](aws-properties-eks-cluster-logging.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Name`  <a name="cfn-eks-cluster-name"></a>
The unique name to give to your cluster\.  
*Required*: No  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `100`  
*Pattern*: `^[0-9A-Za-z][A-Za-z0-9\-_]*`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`OutpostConfig`  <a name="cfn-eks-cluster-outpostconfig"></a>
An object representing the configuration of your local Amazon EKS cluster on an AWS Outpost\. This object isn't available for clusters on the AWS cloud\.  
*Required*: No  
*Type*: [OutpostConfig](aws-properties-eks-cluster-outpostconfig.md)  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`ResourcesVpcConfig`  <a name="cfn-eks-cluster-resourcesvpcconfig"></a>
The VPC configuration that's used by the cluster control plane\. Amazon EKS VPC resources have specific requirements to work properly with Kubernetes\. For more information, see [Cluster VPC Considerations](https://docs.aws.amazon.com/eks/latest/userguide/network_reqs.html) and [Cluster Security Group Considerations](https://docs.aws.amazon.com/eks/latest/userguide/sec-group-reqs.html) in the *Amazon EKS User Guide*\. You must specify at least two subnets\. You can specify up to five security groups, but we recommend that you use a dedicated security group for your cluster control plane\.  
Updates require replacement of the `SecurityGroupIds` and `SubnetIds` sub\-properties\.
*Required*: Yes  
*Type*: [ResourcesVpcConfig](aws-properties-eks-cluster-resourcesvpcconfig.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RoleArn`  <a name="cfn-eks-cluster-rolearn"></a>
The Amazon Resource Name \(ARN\) of the IAM role that provides permissions for the Kubernetes control plane to make calls to AWS API operations on your behalf\. For more information, see [Amazon EKS Service IAM Role](https://docs.aws.amazon.com/eks/latest/userguide/service_IAM_role.html) in the * *Amazon EKS User Guide* *\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Tags`  <a name="cfn-eks-cluster-tags"></a>
The metadata that you apply to the cluster to assist with categorization and organization\. Each tag consists of a key and an optional value, both of which you define\. Cluster tags don't propagate to any other resources associated with the cluster\.  
You must have the `eks:TagResource` and `eks:UntagResource` permissions for your [IAM principal](https://docs.aws.amazon.com/IAM/latest/UserGuide/id_roles_terms-and-concepts.html) to manage the AWS CloudFormation stack\. If you don't have these permissions, there might be unexpected behavior with stack\-level tags propagating to the resource during resource creation and update\.
*Required*: No  
*Type*: List of [Tag](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-resource-tags.html)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Version`  <a name="cfn-eks-cluster-version"></a>
The desired Kubernetes version for your cluster\. If you don't specify a value here, the default version available in Amazon EKS is used\.  
The default version might not be the latest version available\.
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

## Return values<a name="aws-resource-eks-cluster-return-values"></a>

### Ref<a name="aws-resource-eks-cluster-return-values-ref"></a>

 When you pass the logical ID of this resource to the intrinsic `Ref`function, `Ref`returns the resource name\. For example:

 `{ "Ref": "myCluster" }` 

For the Amazon EKS cluster `myCluster`, `Ref` returns the name of the cluster\.

For more information about using the `Ref`function, see [Ref](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-ref.html)\.

### Fn::GetAtt<a name="aws-resource-eks-cluster-return-values-fn--getatt"></a>

The `Fn::GetAtt`intrinsic function returns a value for a specified attribute of this type\. The following are the available attributes and sample return values\.

For more information about using the `Fn::GetAtt`intrinsic function, see [Fn::GetAtt](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/intrinsic-function-reference-getatt.html)\.

#### <a name="aws-resource-eks-cluster-return-values-fn--getatt-fn--getatt"></a>

`Arn`  <a name="Arn-fn::getatt"></a>
The ARN of the cluster, such as `arn:aws:eks:us-west-2:666666666666:cluster/prod`\.

`CertificateAuthorityData`  <a name="CertificateAuthorityData-fn::getatt"></a>
The `certificate-authority-data` for your cluster\.

`ClusterSecurityGroupId`  <a name="ClusterSecurityGroupId-fn::getatt"></a>
The cluster security group that was created by Amazon EKS for the cluster\. Managed node groups use this security group for control plane to data plane communication\.  
This parameter is only returned by Amazon EKS clusters that support managed node groups\. For more information, see [Managed node groups](https://docs.aws.amazon.com/eks/latest/userguide/managed-node-groups.html) in the *Amazon EKS User Guide*\. 

`EncryptionConfigKeyArn`  <a name="EncryptionConfigKeyArn-fn::getatt"></a>
Amazon Resource Name \(ARN\) or alias of the customer master key \(CMK\)\.

`Endpoint`  <a name="Endpoint-fn::getatt"></a>
The endpoint for your Kubernetes API server, such as `https://5E1D0CEXAMPLEA591B746AFC5AB30262.yl4.us-west-2.eks.amazonaws.com`\.

`Id`  <a name="Id-fn::getatt"></a>
The ID of your local Amazon EKS cluster on an AWS Outpost\. This property isn't available for an Amazon EKS cluster on the AWS cloud\.

`KubernetesNetworkConfig.ServiceIpv6Cidr`  <a name="KubernetesNetworkConfig.ServiceIpv6Cidr-fn::getatt"></a>
The CIDR block that Kubernetes Service IP addresses are assigned from if you created a `1.21` or later cluster with version `>1.10.1` or later of the Amazon VPC CNI add\-on and specified `ipv6` for **ipFamily** when you created the cluster\. Kubernetes assigns Service addresses from the unique local address range \(`fc00::/7`\) because you can't specify a custom `IPv6` CIDR block when you create the cluster\.

`OpenIdConnectIssuerUrl`  <a name="OpenIdConnectIssuerUrl-fn::getatt"></a>
The issuer URL for the OIDC identity provider\.

## Examples<a name="aws-resource-eks-cluster--examples"></a>

### Create a cluster<a name="aws-resource-eks-cluster--examples--Create_a_cluster"></a>

The following example creates an Amazon EKS cluster named `Prod`\.

#### JSON<a name="aws-resource-eks-cluster--examples--Create_a_cluster--json"></a>

```
{
    "EKSCluster": {
       "Type": "AWS::EKS::Cluster",
       "Properties": {
          "Name": "Prod",
          "Version": "1.20",
          "RoleArn": "arn:aws:iam::012345678910:role/eks-service-role-AWSServiceRoleForAmazonEKS-EXAMPLEBQ4PI",
          "ResourcesVpcConfig": {
             "SecurityGroupIds": [
                "sg-6979fe18"
             ],
             "SubnetIds": [
                "subnet-6782e71e",
                "subnet-e7e761ac"
             ],
             "EndpointPublicAccess": false,
             "EndpointPrivateAccess": true,
             "PublicAccessCidrs": [
                "1.1.1.2/32"
             ]
          },
          "Logging": {
             "ClusterLogging": {
                "EnabledTypes": [
                   {
                      "Type": "api"
                   },
                   {
                      "Type": "audit"
                   }
                ]
             }
          },
          "Tags": [
             {
                "Key": "key",
                "Value": "val"
             }
          ]
       }
    }
 }
```

#### YAML<a name="aws-resource-eks-cluster--examples--Create_a_cluster--yaml"></a>

```
EKSCluster:
    Type: AWS::EKS::Cluster
    Properties:
      Name: Prod
      Version: "1.20"
      RoleArn: "arn:aws:iam::012345678910:role/eks-service-role-AWSServiceRoleForAmazonEKS-EXAMPLEBQ4PI"
      ResourcesVpcConfig:
        SecurityGroupIds:
          - sg-6979fe18
        SubnetIds:
          - subnet-6782e71e
          - subnet-e7e761ac
        EndpointPublicAccess: false
        EndpointPrivateAccess: true
        PublicAccessCidrs: [ "1.1.1.2/32" ]
      Logging:
        ClusterLogging:
          EnabledTypes:
            - Type: api
            - Type: audit
      Tags:
        - Key: "key"
          Value: "val"
```

## See also<a name="aws-resource-eks-cluster--seealso"></a>
+  [Clusters](https://docs.aws.amazon.com/eks/latest/userguide/clusters.html) in the *Amazon EKS User Guide*\.
+  [https://docs.aws.amazon.com/eks/latest/APIReference/API_CreateCluster.html](https://docs.aws.amazon.com/eks/latest/APIReference/API_CreateCluster.html) in the *Amazon EKS API Reference*\.