# AWS::InspectorV2::Filter FilterCriteria<a name="aws-properties-inspectorv2-filter-filtercriteria"></a>

Details on the criteria used to define the filter\.

## Syntax<a name="aws-properties-inspectorv2-filter-filtercriteria-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-inspectorv2-filter-filtercriteria-syntax.json"></a>

```
{
  "[AwsAccountId](#cfn-inspectorv2-filter-filtercriteria-awsaccountid)" : [ StringFilter, ... ],
  "[ComponentId](#cfn-inspectorv2-filter-filtercriteria-componentid)" : [ StringFilter, ... ],
  "[ComponentType](#cfn-inspectorv2-filter-filtercriteria-componenttype)" : [ StringFilter, ... ],
  "[Ec2InstanceImageId](#cfn-inspectorv2-filter-filtercriteria-ec2instanceimageid)" : [ StringFilter, ... ],
  "[Ec2InstanceSubnetId](#cfn-inspectorv2-filter-filtercriteria-ec2instancesubnetid)" : [ StringFilter, ... ],
  "[Ec2InstanceVpcId](#cfn-inspectorv2-filter-filtercriteria-ec2instancevpcid)" : [ StringFilter, ... ],
  "[EcrImageArchitecture](#cfn-inspectorv2-filter-filtercriteria-ecrimagearchitecture)" : [ StringFilter, ... ],
  "[EcrImageHash](#cfn-inspectorv2-filter-filtercriteria-ecrimagehash)" : [ StringFilter, ... ],
  "[EcrImagePushedAt](#cfn-inspectorv2-filter-filtercriteria-ecrimagepushedat)" : [ DateFilter, ... ],
  "[EcrImageRegistry](#cfn-inspectorv2-filter-filtercriteria-ecrimageregistry)" : [ StringFilter, ... ],
  "[EcrImageRepositoryName](#cfn-inspectorv2-filter-filtercriteria-ecrimagerepositoryname)" : [ StringFilter, ... ],
  "[EcrImageTags](#cfn-inspectorv2-filter-filtercriteria-ecrimagetags)" : [ StringFilter, ... ],
  "[FindingArn](#cfn-inspectorv2-filter-filtercriteria-findingarn)" : [ StringFilter, ... ],
  "[FindingStatus](#cfn-inspectorv2-filter-filtercriteria-findingstatus)" : [ StringFilter, ... ],
  "[FindingType](#cfn-inspectorv2-filter-filtercriteria-findingtype)" : [ StringFilter, ... ],
  "[FirstObservedAt](#cfn-inspectorv2-filter-filtercriteria-firstobservedat)" : [ DateFilter, ... ],
  "[InspectorScore](#cfn-inspectorv2-filter-filtercriteria-inspectorscore)" : [ NumberFilter, ... ],
  "[LastObservedAt](#cfn-inspectorv2-filter-filtercriteria-lastobservedat)" : [ DateFilter, ... ],
  "[NetworkProtocol](#cfn-inspectorv2-filter-filtercriteria-networkprotocol)" : [ StringFilter, ... ],
  "[PortRange](#cfn-inspectorv2-filter-filtercriteria-portrange)" : [ PortRangeFilter, ... ],
  "[RelatedVulnerabilities](#cfn-inspectorv2-filter-filtercriteria-relatedvulnerabilities)" : [ StringFilter, ... ],
  "[ResourceId](#cfn-inspectorv2-filter-filtercriteria-resourceid)" : [ StringFilter, ... ],
  "[ResourceTags](#cfn-inspectorv2-filter-filtercriteria-resourcetags)" : [ MapFilter, ... ],
  "[ResourceType](#cfn-inspectorv2-filter-filtercriteria-resourcetype)" : [ StringFilter, ... ],
  "[Severity](#cfn-inspectorv2-filter-filtercriteria-severity)" : [ StringFilter, ... ],
  "[Title](#cfn-inspectorv2-filter-filtercriteria-title)" : [ StringFilter, ... ],
  "[UpdatedAt](#cfn-inspectorv2-filter-filtercriteria-updatedat)" : [ DateFilter, ... ],
  "[VendorSeverity](#cfn-inspectorv2-filter-filtercriteria-vendorseverity)" : [ StringFilter, ... ],
  "[VulnerabilityId](#cfn-inspectorv2-filter-filtercriteria-vulnerabilityid)" : [ StringFilter, ... ],
  "[VulnerabilitySource](#cfn-inspectorv2-filter-filtercriteria-vulnerabilitysource)" : [ StringFilter, ... ],
  "[VulnerablePackages](#cfn-inspectorv2-filter-filtercriteria-vulnerablepackages)" : [ PackageFilter, ... ]
}
```

### YAML<a name="aws-properties-inspectorv2-filter-filtercriteria-syntax.yaml"></a>

```
  [AwsAccountId](#cfn-inspectorv2-filter-filtercriteria-awsaccountid): 
    - StringFilter
  [ComponentId](#cfn-inspectorv2-filter-filtercriteria-componentid): 
    - StringFilter
  [ComponentType](#cfn-inspectorv2-filter-filtercriteria-componenttype): 
    - StringFilter
  [Ec2InstanceImageId](#cfn-inspectorv2-filter-filtercriteria-ec2instanceimageid): 
    - StringFilter
  [Ec2InstanceSubnetId](#cfn-inspectorv2-filter-filtercriteria-ec2instancesubnetid): 
    - StringFilter
  [Ec2InstanceVpcId](#cfn-inspectorv2-filter-filtercriteria-ec2instancevpcid): 
    - StringFilter
  [EcrImageArchitecture](#cfn-inspectorv2-filter-filtercriteria-ecrimagearchitecture): 
    - StringFilter
  [EcrImageHash](#cfn-inspectorv2-filter-filtercriteria-ecrimagehash): 
    - StringFilter
  [EcrImagePushedAt](#cfn-inspectorv2-filter-filtercriteria-ecrimagepushedat): 
    - DateFilter
  [EcrImageRegistry](#cfn-inspectorv2-filter-filtercriteria-ecrimageregistry): 
    - StringFilter
  [EcrImageRepositoryName](#cfn-inspectorv2-filter-filtercriteria-ecrimagerepositoryname): 
    - StringFilter
  [EcrImageTags](#cfn-inspectorv2-filter-filtercriteria-ecrimagetags): 
    - StringFilter
  [FindingArn](#cfn-inspectorv2-filter-filtercriteria-findingarn): 
    - StringFilter
  [FindingStatus](#cfn-inspectorv2-filter-filtercriteria-findingstatus): 
    - StringFilter
  [FindingType](#cfn-inspectorv2-filter-filtercriteria-findingtype): 
    - StringFilter
  [FirstObservedAt](#cfn-inspectorv2-filter-filtercriteria-firstobservedat): 
    - DateFilter
  [InspectorScore](#cfn-inspectorv2-filter-filtercriteria-inspectorscore): 
    - NumberFilter
  [LastObservedAt](#cfn-inspectorv2-filter-filtercriteria-lastobservedat): 
    - DateFilter
  [NetworkProtocol](#cfn-inspectorv2-filter-filtercriteria-networkprotocol): 
    - StringFilter
  [PortRange](#cfn-inspectorv2-filter-filtercriteria-portrange): 
    - PortRangeFilter
  [RelatedVulnerabilities](#cfn-inspectorv2-filter-filtercriteria-relatedvulnerabilities): 
    - StringFilter
  [ResourceId](#cfn-inspectorv2-filter-filtercriteria-resourceid): 
    - StringFilter
  [ResourceTags](#cfn-inspectorv2-filter-filtercriteria-resourcetags): 
    - MapFilter
  [ResourceType](#cfn-inspectorv2-filter-filtercriteria-resourcetype): 
    - StringFilter
  [Severity](#cfn-inspectorv2-filter-filtercriteria-severity): 
    - StringFilter
  [Title](#cfn-inspectorv2-filter-filtercriteria-title): 
    - StringFilter
  [UpdatedAt](#cfn-inspectorv2-filter-filtercriteria-updatedat): 
    - DateFilter
  [VendorSeverity](#cfn-inspectorv2-filter-filtercriteria-vendorseverity): 
    - StringFilter
  [VulnerabilityId](#cfn-inspectorv2-filter-filtercriteria-vulnerabilityid): 
    - StringFilter
  [VulnerabilitySource](#cfn-inspectorv2-filter-filtercriteria-vulnerabilitysource): 
    - StringFilter
  [VulnerablePackages](#cfn-inspectorv2-filter-filtercriteria-vulnerablepackages): 
    - PackageFilter
```

## Properties<a name="aws-properties-inspectorv2-filter-filtercriteria-properties"></a>

`AwsAccountId`  <a name="cfn-inspectorv2-filter-filtercriteria-awsaccountid"></a>
Details of the AWS account IDs used to filter findings\.  
*Required*: No  
*Type*: List of [StringFilter](aws-properties-inspectorv2-filter-stringfilter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ComponentId`  <a name="cfn-inspectorv2-filter-filtercriteria-componentid"></a>
Details of the component IDs used to filter findings\.  
*Required*: No  
*Type*: List of [StringFilter](aws-properties-inspectorv2-filter-stringfilter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ComponentType`  <a name="cfn-inspectorv2-filter-filtercriteria-componenttype"></a>
Details of the component types used to filter findings\.  
*Required*: No  
*Type*: List of [StringFilter](aws-properties-inspectorv2-filter-stringfilter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Ec2InstanceImageId`  <a name="cfn-inspectorv2-filter-filtercriteria-ec2instanceimageid"></a>
Details of the Amazon EC2 instance image IDs used to filter findings\.  
*Required*: No  
*Type*: List of [StringFilter](aws-properties-inspectorv2-filter-stringfilter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Ec2InstanceSubnetId`  <a name="cfn-inspectorv2-filter-filtercriteria-ec2instancesubnetid"></a>
Details of the Amazon EC2 instance subnet IDs used to filter findings\.  
*Required*: No  
*Type*: List of [StringFilter](aws-properties-inspectorv2-filter-stringfilter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Ec2InstanceVpcId`  <a name="cfn-inspectorv2-filter-filtercriteria-ec2instancevpcid"></a>
Details of the Amazon EC2 instance VPC IDs used to filter findings\.  
*Required*: No  
*Type*: List of [StringFilter](aws-properties-inspectorv2-filter-stringfilter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EcrImageArchitecture`  <a name="cfn-inspectorv2-filter-filtercriteria-ecrimagearchitecture"></a>
Details of the Amazon ECR image architecture types used to filter findings\.  
*Required*: No  
*Type*: List of [StringFilter](aws-properties-inspectorv2-filter-stringfilter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EcrImageHash`  <a name="cfn-inspectorv2-filter-filtercriteria-ecrimagehash"></a>
Details of the Amazon ECR image hashes used to filter findings\.  
*Required*: No  
*Type*: List of [StringFilter](aws-properties-inspectorv2-filter-stringfilter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EcrImagePushedAt`  <a name="cfn-inspectorv2-filter-filtercriteria-ecrimagepushedat"></a>
Details on the Amazon ECR image push date and time used to filter findings\.  
*Required*: No  
*Type*: List of [DateFilter](aws-properties-inspectorv2-filter-datefilter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EcrImageRegistry`  <a name="cfn-inspectorv2-filter-filtercriteria-ecrimageregistry"></a>
Details on the Amazon ECR registry used to filter findings\.  
*Required*: No  
*Type*: List of [StringFilter](aws-properties-inspectorv2-filter-stringfilter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EcrImageRepositoryName`  <a name="cfn-inspectorv2-filter-filtercriteria-ecrimagerepositoryname"></a>
Details on the name of the Amazon ECR repository used to filter findings\.  
*Required*: No  
*Type*: List of [StringFilter](aws-properties-inspectorv2-filter-stringfilter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`EcrImageTags`  <a name="cfn-inspectorv2-filter-filtercriteria-ecrimagetags"></a>
The tags attached to the Amazon ECR container image\.  
*Required*: No  
*Type*: List of [StringFilter](aws-properties-inspectorv2-filter-stringfilter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FindingArn`  <a name="cfn-inspectorv2-filter-filtercriteria-findingarn"></a>
Details on the finding ARNs used to filter findings\.  
*Required*: No  
*Type*: List of [StringFilter](aws-properties-inspectorv2-filter-stringfilter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FindingStatus`  <a name="cfn-inspectorv2-filter-filtercriteria-findingstatus"></a>
Details on the finding status types used to filter findings\.  
*Required*: No  
*Type*: List of [StringFilter](aws-properties-inspectorv2-filter-stringfilter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FindingType`  <a name="cfn-inspectorv2-filter-filtercriteria-findingtype"></a>
Details on the finding types used to filter findings\.  
*Required*: No  
*Type*: List of [StringFilter](aws-properties-inspectorv2-filter-stringfilter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`FirstObservedAt`  <a name="cfn-inspectorv2-filter-filtercriteria-firstobservedat"></a>
Details on the date and time a finding was first seen used to filter findings\.  
*Required*: No  
*Type*: List of [DateFilter](aws-properties-inspectorv2-filter-datefilter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`InspectorScore`  <a name="cfn-inspectorv2-filter-filtercriteria-inspectorscore"></a>
The Amazon Inspector score to filter on\.  
*Required*: No  
*Type*: List of [NumberFilter](aws-properties-inspectorv2-filter-numberfilter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LastObservedAt`  <a name="cfn-inspectorv2-filter-filtercriteria-lastobservedat"></a>
Details on the date and time a finding was last seen used to filter findings\.  
*Required*: No  
*Type*: List of [DateFilter](aws-properties-inspectorv2-filter-datefilter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NetworkProtocol`  <a name="cfn-inspectorv2-filter-filtercriteria-networkprotocol"></a>
Details on the ingress source addresses used to filter findings\.  
*Required*: No  
*Type*: List of [StringFilter](aws-properties-inspectorv2-filter-stringfilter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PortRange`  <a name="cfn-inspectorv2-filter-filtercriteria-portrange"></a>
Details on the port ranges used to filter findings\.  
*Required*: No  
*Type*: List of [PortRangeFilter](aws-properties-inspectorv2-filter-portrangefilter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RelatedVulnerabilities`  <a name="cfn-inspectorv2-filter-filtercriteria-relatedvulnerabilities"></a>
Details on the related vulnerabilities used to filter findings\.  
*Required*: No  
*Type*: List of [StringFilter](aws-properties-inspectorv2-filter-stringfilter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ResourceId`  <a name="cfn-inspectorv2-filter-filtercriteria-resourceid"></a>
Details on the resource IDs used to filter findings\.  
*Required*: No  
*Type*: List of [StringFilter](aws-properties-inspectorv2-filter-stringfilter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ResourceTags`  <a name="cfn-inspectorv2-filter-filtercriteria-resourcetags"></a>
Details on the resource tags used to filter findings\.  
*Required*: No  
*Type*: List of [MapFilter](aws-properties-inspectorv2-filter-mapfilter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ResourceType`  <a name="cfn-inspectorv2-filter-filtercriteria-resourcetype"></a>
Details on the resource types used to filter findings\.  
*Required*: No  
*Type*: List of [StringFilter](aws-properties-inspectorv2-filter-stringfilter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Severity`  <a name="cfn-inspectorv2-filter-filtercriteria-severity"></a>
Details on the severity used to filter findings\.  
*Required*: No  
*Type*: List of [StringFilter](aws-properties-inspectorv2-filter-stringfilter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Title`  <a name="cfn-inspectorv2-filter-filtercriteria-title"></a>
Details on the finding title used to filter findings\.  
*Required*: No  
*Type*: List of [StringFilter](aws-properties-inspectorv2-filter-stringfilter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`UpdatedAt`  <a name="cfn-inspectorv2-filter-filtercriteria-updatedat"></a>
Details on the date and time a finding was last updated at used to filter findings\.  
*Required*: No  
*Type*: List of [DateFilter](aws-properties-inspectorv2-filter-datefilter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VendorSeverity`  <a name="cfn-inspectorv2-filter-filtercriteria-vendorseverity"></a>
Details on the vendor severity used to filter findings\.  
*Required*: No  
*Type*: List of [StringFilter](aws-properties-inspectorv2-filter-stringfilter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VulnerabilityId`  <a name="cfn-inspectorv2-filter-filtercriteria-vulnerabilityid"></a>
Details on the vulnerability ID used to filter findings\.  
*Required*: No  
*Type*: List of [StringFilter](aws-properties-inspectorv2-filter-stringfilter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VulnerabilitySource`  <a name="cfn-inspectorv2-filter-filtercriteria-vulnerabilitysource"></a>
Details on the vulnerability score to filter findings by\.  
*Required*: No  
*Type*: List of [StringFilter](aws-properties-inspectorv2-filter-stringfilter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`VulnerablePackages`  <a name="cfn-inspectorv2-filter-filtercriteria-vulnerablepackages"></a>
Details on the vulnerable packages used to filter findings\.  
*Required*: No  
*Type*: List of [PackageFilter](aws-properties-inspectorv2-filter-packagefilter.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)