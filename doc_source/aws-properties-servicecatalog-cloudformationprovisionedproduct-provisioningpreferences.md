# AWS::ServiceCatalog::CloudFormationProvisionedProduct ProvisioningPreferences<a name="aws-properties-servicecatalog-cloudformationprovisionedproduct-provisioningpreferences"></a>

The user\-defined preferences that will be applied when updating a provisioned product\. Not all preferences are applicable to all provisioned product type

One or more AWS accounts that will have access to the provisioned product\.

Applicable only to a `CFN_STACKSET` provisioned product type\.

The AWS accounts specified should be within the list of accounts in the `STACKSET` constraint\. To get the list of accounts in the `STACKSET` constraint, use the `DescribeProvisioningParameters` operation\.

If no values are specified, the default value is all accounts from the `STACKSET` constraint\.

## Syntax<a name="aws-properties-servicecatalog-cloudformationprovisionedproduct-provisioningpreferences-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-servicecatalog-cloudformationprovisionedproduct-provisioningpreferences-syntax.json"></a>

```
{
  "[StackSetAccounts](#cfn-servicecatalog-cloudformationprovisionedproduct-provisioningpreferences-stacksetaccounts)" : [ String, ... ],
  "[StackSetFailureToleranceCount](#cfn-servicecatalog-cloudformationprovisionedproduct-provisioningpreferences-stacksetfailuretolerancecount)" : Integer,
  "[StackSetFailureTolerancePercentage](#cfn-servicecatalog-cloudformationprovisionedproduct-provisioningpreferences-stacksetfailuretolerancepercentage)" : Integer,
  "[StackSetMaxConcurrencyCount](#cfn-servicecatalog-cloudformationprovisionedproduct-provisioningpreferences-stacksetmaxconcurrencycount)" : Integer,
  "[StackSetMaxConcurrencyPercentage](#cfn-servicecatalog-cloudformationprovisionedproduct-provisioningpreferences-stacksetmaxconcurrencypercentage)" : Integer,
  "[StackSetOperationType](#cfn-servicecatalog-cloudformationprovisionedproduct-provisioningpreferences-stacksetoperationtype)" : String,
  "[StackSetRegions](#cfn-servicecatalog-cloudformationprovisionedproduct-provisioningpreferences-stacksetregions)" : [ String, ... ]
}
```

### YAML<a name="aws-properties-servicecatalog-cloudformationprovisionedproduct-provisioningpreferences-syntax.yaml"></a>

```
  [StackSetAccounts](#cfn-servicecatalog-cloudformationprovisionedproduct-provisioningpreferences-stacksetaccounts): 
    - String
  [StackSetFailureToleranceCount](#cfn-servicecatalog-cloudformationprovisionedproduct-provisioningpreferences-stacksetfailuretolerancecount): Integer
  [StackSetFailureTolerancePercentage](#cfn-servicecatalog-cloudformationprovisionedproduct-provisioningpreferences-stacksetfailuretolerancepercentage): Integer
  [StackSetMaxConcurrencyCount](#cfn-servicecatalog-cloudformationprovisionedproduct-provisioningpreferences-stacksetmaxconcurrencycount): Integer
  [StackSetMaxConcurrencyPercentage](#cfn-servicecatalog-cloudformationprovisionedproduct-provisioningpreferences-stacksetmaxconcurrencypercentage): Integer
  [StackSetOperationType](#cfn-servicecatalog-cloudformationprovisionedproduct-provisioningpreferences-stacksetoperationtype): String
  [StackSetRegions](#cfn-servicecatalog-cloudformationprovisionedproduct-provisioningpreferences-stacksetregions): 
    - String
```

## Properties<a name="aws-properties-servicecatalog-cloudformationprovisionedproduct-provisioningpreferences-properties"></a>

`StackSetAccounts`  <a name="cfn-servicecatalog-cloudformationprovisionedproduct-provisioningpreferences-stacksetaccounts"></a>
One or more AWS accounts where the provisioned product will be available\.  
Applicable only to a `CFN_STACKSET` provisioned product type\.  
The specified accounts should be within the list of accounts from the `STACKSET` constraint\. To get the list of accounts in the `STACKSET` constraint, use the `DescribeProvisioningParameters` operation\.  
If no values are specified, the default value is all acounts from the `STACKSET` constraint\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StackSetFailureToleranceCount`  <a name="cfn-servicecatalog-cloudformationprovisionedproduct-provisioningpreferences-stacksetfailuretolerancecount"></a>
The number of accounts, per region, for which this operation can fail before AWS Service Catalog stops the operation in that region\. If the operation is stopped in a region, AWS Service Catalog doesn't attempt the operation in any subsequent regions\.  
Applicable only to a `CFN_STACKSET` provisioned product type\.  
Conditional: You must specify either `StackSetFailureToleranceCount` or `StackSetFailureTolerancePercentage`, but not both\.  
The default value is `0` if no value is specified\.  
*Required*: No  
*Type*: Integer  
*Minimum*: `0`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StackSetFailureTolerancePercentage`  <a name="cfn-servicecatalog-cloudformationprovisionedproduct-provisioningpreferences-stacksetfailuretolerancepercentage"></a>
The percentage of accounts, per region, for which this stack operation can fail before AWS Service Catalog stops the operation in that region\. If the operation is stopped in a region, AWS Service Catalog doesn't attempt the operation in any subsequent regions\.  
When calculating the number of accounts based on the specified percentage, AWS Service Catalog rounds down to the next whole number\.  
Applicable only to a `CFN_STACKSET` provisioned product type\.  
Conditional: You must specify either `StackSetFailureToleranceCount` or `StackSetFailureTolerancePercentage`, but not both\.  
*Required*: No  
*Type*: Integer  
*Minimum*: `0`  
*Maximum*: `100`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StackSetMaxConcurrencyCount`  <a name="cfn-servicecatalog-cloudformationprovisionedproduct-provisioningpreferences-stacksetmaxconcurrencycount"></a>
The maximum number of accounts in which to perform this operation at one time\. This is dependent on the value of `StackSetFailureToleranceCount`\. `StackSetMaxConcurrentCount` is at most one more than the `StackSetFailureToleranceCount`\.  
Note that this setting lets you specify the maximum for operations\. For large deployments, under certain circumstances the actual number of accounts acted upon concurrently may be lower due to service throttling\.  
Applicable only to a `CFN_STACKSET` provisioned product type\.  
Conditional: You must specify either `StackSetMaxConcurrentCount` or `StackSetMaxConcurrentPercentage`, but not both\.  
*Required*: No  
*Type*: Integer  
*Minimum*: `1`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StackSetMaxConcurrencyPercentage`  <a name="cfn-servicecatalog-cloudformationprovisionedproduct-provisioningpreferences-stacksetmaxconcurrencypercentage"></a>
The maximum percentage of accounts in which to perform this operation at one time\.  
When calculating the number of accounts based on the specified percentage, AWS Service Catalog rounds down to the next whole number\. This is true except in cases where rounding down would result is zero\. In this case, AWS Service Catalog sets the number as `1` instead\.  
Note that this setting lets you specify the maximum for operations\. For large deployments, under certain circumstances the actual number of accounts acted upon concurrently may be lower due to service throttling\.  
Applicable only to a `CFN_STACKSET` provisioned product type\.  
Conditional: You must specify either `StackSetMaxConcurrentCount` or `StackSetMaxConcurrentPercentage`, but not both\.  
*Required*: No  
*Type*: Integer  
*Minimum*: `1`  
*Maximum*: `100`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StackSetOperationType`  <a name="cfn-servicecatalog-cloudformationprovisionedproduct-provisioningpreferences-stacksetoperationtype"></a>
Determines what action AWS Service Catalog performs to a stack set or a stack instance represented by the provisioned product\. The default value is `UPDATE` if nothing is specified\.  
Applicable only to a `CFN_STACKSET` provisioned product type\.    
CREATE  
Creates a new stack instance in the stack set represented by the provisioned product\. In this case, only new stack instances are created based on accounts and regions; if new ProductId or ProvisioningArtifactID are passed, they will be ignored\.  
UPDATE  
Updates the stack set represented by the provisioned product and also its stack instances\.  
DELETE  
Deletes a stack instance in the stack set represented by the provisioned product\.
*Required*: No  
*Type*: String  
*Allowed values*: `CREATE | DELETE | UPDATE`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`StackSetRegions`  <a name="cfn-servicecatalog-cloudformationprovisionedproduct-provisioningpreferences-stacksetregions"></a>
One or more AWS Regions where the provisioned product will be available\.  
Applicable only to a `CFN_STACKSET` provisioned product type\.  
The specified regions should be within the list of regions from the `STACKSET` constraint\. To get the list of regions in the `STACKSET` constraint, use the `DescribeProvisioningParameters` operation\.  
If no values are specified, the default value is all regions from the `STACKSET` constraint\.  
*Required*: No  
*Type*: List of String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)