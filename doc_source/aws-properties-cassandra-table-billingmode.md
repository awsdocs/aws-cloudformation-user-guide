# AWS::Cassandra::Table BillingMode<a name="aws-properties-cassandra-table-billingmode"></a>

Determines the billing mode for the table \- on\-demand or provisioned\.

## Syntax<a name="aws-properties-cassandra-table-billingmode-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-cassandra-table-billingmode-syntax.json"></a>

```
{
  "[Mode](#cfn-cassandra-table-billingmode-mode)" : String,
  "[ProvisionedThroughput](#cfn-cassandra-table-billingmode-provisionedthroughput)" : ProvisionedThroughput
}
```

### YAML<a name="aws-properties-cassandra-table-billingmode-syntax.yaml"></a>

```
  [Mode](#cfn-cassandra-table-billingmode-mode): String
  [ProvisionedThroughput](#cfn-cassandra-table-billingmode-provisionedthroughput): 
    ProvisionedThroughput
```

## Properties<a name="aws-properties-cassandra-table-billingmode-properties"></a>

`Mode`  <a name="cfn-cassandra-table-billingmode-mode"></a>
The billing mode for the table:  
+ On\-demand mode \- `ON_DEMAND`
+ Provisioned mode \- `PROVISIONED`
**Note**  
If you choose `PROVISIONED` mode, then you'll also need to specify provisioned throughput \(read and write capacity\) for the table\.
Valid Values: `ON_DEMAND` \| `PROVISIONED`  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ProvisionedThroughput`  <a name="cfn-cassandra-table-billingmode-provisionedthroughput"></a>
The provisioned read capacity and write capacity for the table\. For more information, see [Provisioned Throughput Capacity Mode](https://docs.aws.amazon.com/keyspaces/latest/devguide/ReadWriteCapacityMode.html#ReadWriteCapacityMode.Provisioned) in the *Amazon Keyspaces Developer Guide*\.  
*Required*: No  
*Type*: [ProvisionedThroughput](aws-properties-cassandra-table-provisionedthroughput.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)