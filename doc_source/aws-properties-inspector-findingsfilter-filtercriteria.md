# AWS::Inspector::FindingsFilter FilterCriteria<a name="aws-properties-inspector-findingsfilter-filtercriteria"></a>

<a name="aws-properties-inspector-findingsfilter-filtercriteria-description"></a>The `FilterCriteria` property type specifies Not currently supported by AWS CloudFormation\. for an [AWS::Inspector::FindingsFilter](aws-resource-inspector-findingsfilter.md)\.

## Syntax<a name="aws-properties-inspector-findingsfilter-filtercriteria-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-inspector-findingsfilter-filtercriteria-syntax.json"></a>

```
{
  "[AwsAccountId](#cfn-inspector-findingsfilter-filtercriteria-awsaccountid)" : [ StringFilter, ... ],
  "[ComponentId](#cfn-inspector-findingsfilter-filtercriteria-componentid)" : [ StringFilter, ... ],
  "[ComponentType](#cfn-inspector-findingsfilter-filtercriteria-componenttype)" : [ StringFilter, ... ],
  "[Ec2InstanceImageId](#cfn-inspector-findingsfilter-filtercriteria-ec2instanceimageid)" : [ StringFilter, ... ],
  "[Ec2InstanceSubnetId](#cfn-inspector-findingsfilter-filtercriteria-ec2instancesubnetid)" : [ StringFilter, ... ],
  "[Ec2InstanceVpcId](#cfn-inspector-findingsfilter-filtercriteria-ec2instancevpcid)" : [ StringFilter, ... ],
  "[EcrInstanceArchitecture](#cfn-inspector-findingsfilter-filtercriteria-ecrinstancearchitecture)" : [ StringFilter, ... ],
  "[EcrInstanceImageHash](#cfn-inspector-findingsfilter-filtercriteria-ecrinstanceimagehash)" : [ StringFilter, ... ],
  "[EcrInstanceImageTags](#cfn-inspector-findingsfilter-filtercriteria-ecrinstanceimagetags)" : [ StringFilter, ... ],
  "[EcrInstancePushedAt](#cfn-inspector-findingsfilter-filtercriteria-ecrinstancepushedat)" : [ DateFilter, ... ],
  "[EcrInstanceRegistry](#cfn-inspector-findingsfilter-filtercriteria-ecrinstanceregistry)" : [ StringFilter, ... ],
  "[EcrInstanceRepositoryName](#cfn-inspector-findingsfilter-filtercriteria-ecrinstancerepositoryname)" : [ StringFilter, ... ],
  "[EgressDestinationPortRange](#cfn-inspector-findingsfilter-filtercriteria-egressdestinationportrange)" : [ PortRangeFilter, ... ],
  "[EgressProtocol](#cfn-inspector-findingsfilter-filtercriteria-egressprotocol)" : [ StringFilter, ... ],
  "[EgressSourceAddress](#cfn-inspector-findingsfilter-filtercriteria-egresssourceaddress)" : [ IpFilter, ... ],
  "[FindingArn](#cfn-inspector-findingsfilter-filtercriteria-findingarn)" : [ StringFilter, ... ],
  "[FindingStatus](#cfn-inspector-findingsfilter-filtercriteria-findingstatus)" : [ StringFilter, ... ],
  "[FindingType](#cfn-inspector-findingsfilter-filtercriteria-findingtype)" : [ StringFilter, ... ],
  "[FirstObservedAt](#cfn-inspector-findingsfilter-filtercriteria-firstobservedat)" : [ DateFilter, ... ],
  "[IngressDestinationAddress](#cfn-inspector-findingsfilter-filtercriteria-ingressdestinationaddress)" : [ IpFilter, ... ],
  "[IngressProtocol](#cfn-inspector-findingsfilter-filtercriteria-ingressprotocol)" : [ StringFilter, ... ],
  "[IngressSourceAddress](#cfn-inspector-findingsfilter-filtercriteria-ingresssourceaddress)" : [ IpFilter, ... ],
  "[InspectorScore](#cfn-inspector-findingsfilter-filtercriteria-inspectorscore)" : [ NumberFilter, ... ],
  "[LastObservedAt](#cfn-inspector-findingsfilter-filtercriteria-lastobservedat)" : [ DateFilter, ... ],
  "[NetworkProtocol](#cfn-inspector-findingsfilter-filtercriteria-networkprotocol)" : [ StringFilter, ... ],
  "[PortRange](#cfn-inspector-findingsfilter-filtercriteria-portrange)" : [ PortRangeFilter, ... ],
  "[RelatedVulnerabilities](#cfn-inspector-findingsfilter-filtercriteria-relatedvulnerabilities)" : [ StringFilter, ... ],
  "[ResourceId](#cfn-inspector-findingsfilter-filtercriteria-resourceid)" : [ StringFilter, ... ],
  "[ResourceTags](#cfn-inspector-findingsfilter-filtercriteria-resourcetags)" : [ MapFilter, ... ],
  "[ResourceType](#cfn-inspector-findingsfilter-filtercriteria-resourcetype)" : [ StringFilter, ... ],
  "[Score](#cfn-inspector-findingsfilter-filtercriteria-score)" : [ NumberFilter, ... ],
  "[Severity](#cfn-inspector-findingsfilter-filtercriteria-severity)" : [ StringFilter, ... ],
  "[Title](#cfn-inspector-findingsfilter-filtercriteria-title)" : [ StringFilter, ... ],
  "[UpdatedAt](#cfn-inspector-findingsfilter-filtercriteria-updatedat)" : [ DateFilter, ... ],
  "[VendorSeverity](#cfn-inspector-findingsfilter-filtercriteria-vendorseverity)" : [ StringFilter, ... ],
  "[VulnerabilityId](#cfn-inspector-findingsfilter-filtercriteria-vulnerabilityid)" : [ StringFilter, ... ],
  "[VulnerabilitySource](#cfn-inspector-findingsfilter-filtercriteria-vulnerabilitysource)" : [ StringFilter, ... ],
  "[VulnerablePackages](#cfn-inspector-findingsfilter-filtercriteria-vulnerablepackages)" : [ PackageFilter, ... ]
}
```

### YAML<a name="aws-properties-inspector-findingsfilter-filtercriteria-syntax.yaml"></a>

```
  [AwsAccountId](#cfn-inspector-findingsfilter-filtercriteria-awsaccountid): 
    - StringFilter
  [ComponentId](#cfn-inspector-findingsfilter-filtercriteria-componentid): 
    - StringFilter
  [ComponentType](#cfn-inspector-findingsfilter-filtercriteria-componenttype): 
    - StringFilter
  [Ec2InstanceImageId](#cfn-inspector-findingsfilter-filtercriteria-ec2instanceimageid): 
    - StringFilter
  [Ec2InstanceSubnetId](#cfn-inspector-findingsfilter-filtercriteria-ec2instancesubnetid): 
    - StringFilter
  [Ec2InstanceVpcId](#cfn-inspector-findingsfilter-filtercriteria-ec2instancevpcid): 
    - StringFilter
  [EcrInstanceArchitecture](#cfn-inspector-findingsfilter-filtercriteria-ecrinstancearchitecture): 
    - StringFilter
  [EcrInstanceImageHash](#cfn-inspector-findingsfilter-filtercriteria-ecrinstanceimagehash): 
    - StringFilter
  [EcrInstanceImageTags](#cfn-inspector-findingsfilter-filtercriteria-ecrinstanceimagetags): 
    - StringFilter
  [EcrInstancePushedAt](#cfn-inspector-findingsfilter-filtercriteria-ecrinstancepushedat): 
    - DateFilter
  [EcrInstanceRegistry](#cfn-inspector-findingsfilter-filtercriteria-ecrinstanceregistry): 
    - StringFilter
  [EcrInstanceRepositoryName](#cfn-inspector-findingsfilter-filtercriteria-ecrinstancerepositoryname): 
    - StringFilter
  [EgressDestinationPortRange](#cfn-inspector-findingsfilter-filtercriteria-egressdestinationportrange): 
    - PortRangeFilter
  [EgressProtocol](#cfn-inspector-findingsfilter-filtercriteria-egressprotocol): 
    - StringFilter
  [EgressSourceAddress](#cfn-inspector-findingsfilter-filtercriteria-egresssourceaddress): 
    - IpFilter
  [FindingArn](#cfn-inspector-findingsfilter-filtercriteria-findingarn): 
    - StringFilter
  [FindingStatus](#cfn-inspector-findingsfilter-filtercriteria-findingstatus): 
    - StringFilter
  [FindingType](#cfn-inspector-findingsfilter-filtercriteria-findingtype): 
    - StringFilter
  [FirstObservedAt](#cfn-inspector-findingsfilter-filtercriteria-firstobservedat): 
    - DateFilter
  [IngressDestinationAddress](#cfn-inspector-findingsfilter-filtercriteria-ingressdestinationaddress): 
    - IpFilter
  [IngressProtocol](#cfn-inspector-findingsfilter-filtercriteria-ingressprotocol): 
    - StringFilter
  [IngressSourceAddress](#cfn-inspector-findingsfilter-filtercriteria-ingresssourceaddress): 
    - IpFilter
  [InspectorScore](#cfn-inspector-findingsfilter-filtercriteria-inspectorscore): 
    - NumberFilter
  [LastObservedAt](#cfn-inspector-findingsfilter-filtercriteria-lastobservedat): 
    - DateFilter
  [NetworkProtocol](#cfn-inspector-findingsfilter-filtercriteria-networkprotocol): 
    - StringFilter
  [PortRange](#cfn-inspector-findingsfilter-filtercriteria-portrange): 
    - PortRangeFilter
  [RelatedVulnerabilities](#cfn-inspector-findingsfilter-filtercriteria-relatedvulnerabilities): 
    - StringFilter
  [ResourceId](#cfn-inspector-findingsfilter-filtercriteria-resourceid): 
    - StringFilter
  [ResourceTags](#cfn-inspector-findingsfilter-filtercriteria-resourcetags): 
    - MapFilter
  [ResourceType](#cfn-inspector-findingsfilter-filtercriteria-resourcetype): 
    - StringFilter
  [Score](#cfn-inspector-findingsfilter-filtercriteria-score): 
    - NumberFilter
  [Severity](#cfn-inspector-findingsfilter-filtercriteria-severity): 
    - StringFilter
  [Title](#cfn-inspector-findingsfilter-filtercriteria-title): 
    - StringFilter
  [UpdatedAt](#cfn-inspector-findingsfilter-filtercriteria-updatedat): 
    - DateFilter
  [VendorSeverity](#cfn-inspector-findingsfilter-filtercriteria-vendorseverity): 
    - StringFilter
  [VulnerabilityId](#cfn-inspector-findingsfilter-filtercriteria-vulnerabilityid): 
    - StringFilter
  [VulnerabilitySource](#cfn-inspector-findingsfilter-filtercriteria-vulnerabilitysource): 
    - StringFilter
  [VulnerablePackages](#cfn-inspector-findingsfilter-filtercriteria-vulnerablepackages): 
    - PackageFilter
```

## Properties<a name="aws-properties-inspector-findingsfilter-filtercriteria-properties"></a>

`AwsAccountId`  <a name="cfn-inspector-findingsfilter-filtercriteria-awsaccountid"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: No  
*Type*: List of [StringFilter](aws-properties-inspector-findingsfilter-stringfilter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ComponentId`  <a name="cfn-inspector-findingsfilter-filtercriteria-componentid"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: No  
*Type*: List of [StringFilter](aws-properties-inspector-findingsfilter-stringfilter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ComponentType`  <a name="cfn-inspector-findingsfilter-filtercriteria-componenttype"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: No  
*Type*: List of [StringFilter](aws-properties-inspector-findingsfilter-stringfilter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Ec2InstanceImageId`  <a name="cfn-inspector-findingsfilter-filtercriteria-ec2instanceimageid"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: No  
*Type*: List of [StringFilter](aws-properties-inspector-findingsfilter-stringfilter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Ec2InstanceSubnetId`  <a name="cfn-inspector-findingsfilter-filtercriteria-ec2instancesubnetid"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: No  
*Type*: List of [StringFilter](aws-properties-inspector-findingsfilter-stringfilter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Ec2InstanceVpcId`  <a name="cfn-inspector-findingsfilter-filtercriteria-ec2instancevpcid"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: No  
*Type*: List of [StringFilter](aws-properties-inspector-findingsfilter-stringfilter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EcrInstanceArchitecture`  <a name="cfn-inspector-findingsfilter-filtercriteria-ecrinstancearchitecture"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: No  
*Type*: List of [StringFilter](aws-properties-inspector-findingsfilter-stringfilter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EcrInstanceImageHash`  <a name="cfn-inspector-findingsfilter-filtercriteria-ecrinstanceimagehash"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: No  
*Type*: List of [StringFilter](aws-properties-inspector-findingsfilter-stringfilter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EcrInstanceImageTags`  <a name="cfn-inspector-findingsfilter-filtercriteria-ecrinstanceimagetags"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: No  
*Type*: List of [StringFilter](aws-properties-inspector-findingsfilter-stringfilter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EcrInstancePushedAt`  <a name="cfn-inspector-findingsfilter-filtercriteria-ecrinstancepushedat"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: No  
*Type*: List of [DateFilter](aws-properties-inspector-findingsfilter-datefilter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EcrInstanceRegistry`  <a name="cfn-inspector-findingsfilter-filtercriteria-ecrinstanceregistry"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: No  
*Type*: List of [StringFilter](aws-properties-inspector-findingsfilter-stringfilter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EcrInstanceRepositoryName`  <a name="cfn-inspector-findingsfilter-filtercriteria-ecrinstancerepositoryname"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: No  
*Type*: List of [StringFilter](aws-properties-inspector-findingsfilter-stringfilter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EgressDestinationPortRange`  <a name="cfn-inspector-findingsfilter-filtercriteria-egressdestinationportrange"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: No  
*Type*: List of [PortRangeFilter](aws-properties-inspector-findingsfilter-portrangefilter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EgressProtocol`  <a name="cfn-inspector-findingsfilter-filtercriteria-egressprotocol"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: No  
*Type*: List of [StringFilter](aws-properties-inspector-findingsfilter-stringfilter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EgressSourceAddress`  <a name="cfn-inspector-findingsfilter-filtercriteria-egresssourceaddress"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: No  
*Type*: List of [IpFilter](aws-properties-inspector-findingsfilter-ipfilter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FindingArn`  <a name="cfn-inspector-findingsfilter-filtercriteria-findingarn"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: No  
*Type*: List of [StringFilter](aws-properties-inspector-findingsfilter-stringfilter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FindingStatus`  <a name="cfn-inspector-findingsfilter-filtercriteria-findingstatus"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: No  
*Type*: List of [StringFilter](aws-properties-inspector-findingsfilter-stringfilter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FindingType`  <a name="cfn-inspector-findingsfilter-filtercriteria-findingtype"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: No  
*Type*: List of [StringFilter](aws-properties-inspector-findingsfilter-stringfilter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FirstObservedAt`  <a name="cfn-inspector-findingsfilter-filtercriteria-firstobservedat"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: No  
*Type*: List of [DateFilter](aws-properties-inspector-findingsfilter-datefilter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IngressDestinationAddress`  <a name="cfn-inspector-findingsfilter-filtercriteria-ingressdestinationaddress"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: No  
*Type*: List of [IpFilter](aws-properties-inspector-findingsfilter-ipfilter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IngressProtocol`  <a name="cfn-inspector-findingsfilter-filtercriteria-ingressprotocol"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: No  
*Type*: List of [StringFilter](aws-properties-inspector-findingsfilter-stringfilter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IngressSourceAddress`  <a name="cfn-inspector-findingsfilter-filtercriteria-ingresssourceaddress"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: No  
*Type*: List of [IpFilter](aws-properties-inspector-findingsfilter-ipfilter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`InspectorScore`  <a name="cfn-inspector-findingsfilter-filtercriteria-inspectorscore"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: No  
*Type*: List of [NumberFilter](aws-properties-inspector-findingsfilter-numberfilter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LastObservedAt`  <a name="cfn-inspector-findingsfilter-filtercriteria-lastobservedat"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: No  
*Type*: List of [DateFilter](aws-properties-inspector-findingsfilter-datefilter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NetworkProtocol`  <a name="cfn-inspector-findingsfilter-filtercriteria-networkprotocol"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: No  
*Type*: List of [StringFilter](aws-properties-inspector-findingsfilter-stringfilter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PortRange`  <a name="cfn-inspector-findingsfilter-filtercriteria-portrange"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: No  
*Type*: List of [PortRangeFilter](aws-properties-inspector-findingsfilter-portrangefilter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RelatedVulnerabilities`  <a name="cfn-inspector-findingsfilter-filtercriteria-relatedvulnerabilities"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: No  
*Type*: List of [StringFilter](aws-properties-inspector-findingsfilter-stringfilter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ResourceId`  <a name="cfn-inspector-findingsfilter-filtercriteria-resourceid"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: No  
*Type*: List of [StringFilter](aws-properties-inspector-findingsfilter-stringfilter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ResourceTags`  <a name="cfn-inspector-findingsfilter-filtercriteria-resourcetags"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: No  
*Type*: List of [MapFilter](aws-properties-inspector-findingsfilter-mapfilter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ResourceType`  <a name="cfn-inspector-findingsfilter-filtercriteria-resourcetype"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: No  
*Type*: List of [StringFilter](aws-properties-inspector-findingsfilter-stringfilter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Score`  <a name="cfn-inspector-findingsfilter-filtercriteria-score"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: No  
*Type*: List of [NumberFilter](aws-properties-inspector-findingsfilter-numberfilter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Severity`  <a name="cfn-inspector-findingsfilter-filtercriteria-severity"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: No  
*Type*: List of [StringFilter](aws-properties-inspector-findingsfilter-stringfilter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Title`  <a name="cfn-inspector-findingsfilter-filtercriteria-title"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: No  
*Type*: List of [StringFilter](aws-properties-inspector-findingsfilter-stringfilter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`UpdatedAt`  <a name="cfn-inspector-findingsfilter-filtercriteria-updatedat"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: No  
*Type*: List of [DateFilter](aws-properties-inspector-findingsfilter-datefilter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VendorSeverity`  <a name="cfn-inspector-findingsfilter-filtercriteria-vendorseverity"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: No  
*Type*: List of [StringFilter](aws-properties-inspector-findingsfilter-stringfilter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VulnerabilityId`  <a name="cfn-inspector-findingsfilter-filtercriteria-vulnerabilityid"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: No  
*Type*: List of [StringFilter](aws-properties-inspector-findingsfilter-stringfilter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VulnerabilitySource`  <a name="cfn-inspector-findingsfilter-filtercriteria-vulnerabilitysource"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: No  
*Type*: List of [StringFilter](aws-properties-inspector-findingsfilter-stringfilter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VulnerablePackages`  <a name="cfn-inspector-findingsfilter-filtercriteria-vulnerablepackages"></a>
Not currently supported by AWS CloudFormation\.  
*Required*: No  
*Type*: List of [PackageFilter](aws-properties-inspector-findingsfilter-packagefilter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)