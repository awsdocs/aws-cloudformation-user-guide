# AWS::EMR::InstanceFleetConfig OnDemandProvisioningSpecification<a name="aws-properties-elasticmapreduce-instancefleetconfig-ondemandprovisioningspecification"></a>

 The launch specification for On\-Demand Instances in the instance fleet, which determines the allocation strategy\. 

**Note**  
The instance fleet configuration is available only in Amazon EMR versions 4\.8\.0 and later, excluding 5\.0\.x versions\. On\-Demand Instances allocation strategy is available in Amazon EMR version 5\.12\.1 and later\.

## Syntax<a name="aws-properties-elasticmapreduce-instancefleetconfig-ondemandprovisioningspecification-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-elasticmapreduce-instancefleetconfig-ondemandprovisioningspecification-syntax.json"></a>

```
{
  "[AllocationStrategy](#cfn-elasticmapreduce-instancefleetconfig-ondemandprovisioningspecification-allocationstrategy)" : String
}
```

### YAML<a name="aws-properties-elasticmapreduce-instancefleetconfig-ondemandprovisioningspecification-syntax.yaml"></a>

```
  [AllocationStrategy](#cfn-elasticmapreduce-instancefleetconfig-ondemandprovisioningspecification-allocationstrategy): String
```

## Properties<a name="aws-properties-elasticmapreduce-instancefleetconfig-ondemandprovisioningspecification-properties"></a>

`AllocationStrategy`  <a name="cfn-elasticmapreduce-instancefleetconfig-ondemandprovisioningspecification-allocationstrategy"></a>
 Specifies the strategy to use in launching On\-Demand Instance fleets\. Currently, the only option is lowest\-price \(the default\), which launches the lowest price first\.   
*Required*: Yes  
*Type*: String  
*Allowed values*: `lowest-price`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)