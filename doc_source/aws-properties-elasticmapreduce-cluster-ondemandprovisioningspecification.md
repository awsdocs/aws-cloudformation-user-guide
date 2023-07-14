# AWS::EMR::Cluster OnDemandProvisioningSpecification<a name="aws-properties-elasticmapreduce-cluster-ondemandprovisioningspecification"></a>

 The launch specification for On\-Demand Instances in the instance fleet, which determines the allocation strategy\. 

**Note**  
The instance fleet configuration is available only in Amazon EMR releases 4\.8\.0 and later, excluding 5\.0\.x versions\. On\-Demand Instances allocation strategy is available in Amazon EMR releases 5\.12\.1 and later\.

## Syntax<a name="aws-properties-elasticmapreduce-cluster-ondemandprovisioningspecification-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-elasticmapreduce-cluster-ondemandprovisioningspecification-syntax.json"></a>

```
{
  "[AllocationStrategy](#cfn-elasticmapreduce-cluster-ondemandprovisioningspecification-allocationstrategy)" : String
}
```

### YAML<a name="aws-properties-elasticmapreduce-cluster-ondemandprovisioningspecification-syntax.yaml"></a>

```
  [AllocationStrategy](#cfn-elasticmapreduce-cluster-ondemandprovisioningspecification-allocationstrategy): String
```

## Properties<a name="aws-properties-elasticmapreduce-cluster-ondemandprovisioningspecification-properties"></a>

`AllocationStrategy`  <a name="cfn-elasticmapreduce-cluster-ondemandprovisioningspecification-allocationstrategy"></a>
Specifies the strategy to use in launching On\-Demand instance fleets\. Currently, the only option is `lowest-price` \(the default\), which launches the lowest price first\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `lowest-price`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)