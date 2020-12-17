# AWS::GuardDuty::Filter FindingCriteria<a name="aws-properties-guardduty-filter-findingcriteria"></a>

Represents a map of finding properties that match specified conditions and values when querying findings\.

## Syntax<a name="aws-properties-guardduty-filter-findingcriteria-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-guardduty-filter-findingcriteria-syntax.json"></a>

```
{
  "[Criterion](#cfn-guardduty-filter-findingcriteria-criterion)" : Json,
  "[ItemType](#cfn-guardduty-filter-findingcriteria-itemtype)" : Condition
}
```

### YAML<a name="aws-properties-guardduty-filter-findingcriteria-syntax.yaml"></a>

```
  [Criterion](#cfn-guardduty-filter-findingcriteria-criterion): Json
  [ItemType](#cfn-guardduty-filter-findingcriteria-itemtype): 
    Condition
```

## Properties<a name="aws-properties-guardduty-filter-findingcriteria-properties"></a>

`Criterion`  <a name="cfn-guardduty-filter-findingcriteria-criterion"></a>
Represents a map of finding properties that match specified conditions and values when querying findings\.  
For a mapping of JSON criterion to their console equivalent see [Finding criteria](https://docs.aws.amazon.com/guardduty/latest/ug/guardduty_filter-findings.html#filter_criteria)\. The following are the available criterion:  
+ accountId
+ region
+ confidence
+ id
+ resource\.accessKeyDetails\.accessKeyId
+ resource\.accessKeyDetails\.principalId
+ resource\.accessKeyDetails\.userName
+ resource\.accessKeyDetails\.userType
+ resource\.instanceDetails\.iamInstanceProfile\.id
+ resource\.instanceDetails\.imageId
+ resource\.instanceDetails\.instanceId
+ resource\.instanceDetails\.outpostArn
+ resource\.instanceDetails\.networkInterfaces\.ipv6Addresses
+ resource\.instanceDetails\.networkInterfaces\.privateIpAddresses\.privateIpAddress
+ resource\.instanceDetails\.networkInterfaces\.publicDnsName
+ resource\.instanceDetails\.networkInterfaces\.publicIp
+ resource\.instanceDetails\.networkInterfaces\.securityGroups\.groupId
+ resource\.instanceDetails\.networkInterfaces\.securityGroups\.groupName
+ resource\.instanceDetails\.networkInterfaces\.subnetId
+ resource\.instanceDetails\.networkInterfaces\.vpcId
+ resource\.instanceDetails\.tags\.key
+ resource\.instanceDetails\.tags\.value
+ resource\.resourceType
+ service\.action\.actionType
+ service\.action\.awsApiCallAction\.api
+ service\.action\.awsApiCallAction\.callerType
+ service\.action\.awsApiCallAction\.errorCode
+ service\.action\.awsApiCallAction\.remoteIpDetails\.city\.cityName
+ service\.action\.awsApiCallAction\.remoteIpDetails\.country\.countryName
+ service\.action\.awsApiCallAction\.remoteIpDetails\.ipAddressV4
+ service\.action\.awsApiCallAction\.remoteIpDetails\.organization\.asn
+ service\.action\.awsApiCallAction\.remoteIpDetails\.organization\.asnOrg
+ service\.action\.awsApiCallAction\.serviceName
+ service\.action\.dnsRequestAction\.domain
+ service\.action\.networkConnectionAction\.blocked
+ service\.action\.networkConnectionAction\.connectionDirection
+ service\.action\.networkConnectionAction\.localPortDetails\.port
+ service\.action\.networkConnectionAction\.protocol
+ service\.action\.networkConnectionAction\.localIpDetails\.ipAddressV4
+ service\.action\.networkConnectionAction\.remoteIpDetails\.city\.cityName
+ service\.action\.networkConnectionAction\.remoteIpDetails\.country\.countryName
+ service\.action\.networkConnectionAction\.remoteIpDetails\.ipAddressV4
+ service\.action\.networkConnectionAction\.remoteIpDetails\.organization\.asn
+ service\.action\.networkConnectionAction\.remoteIpDetails\.organization\.asnOrg
+ service\.action\.networkConnectionAction\.remotePortDetails\.port
+ service\.additionalInfo\.threatListName
+ service\.archived

  When this attribute is set to TRUE, only archived findings are listed\. When it's set to FALSE, only unarchived findings are listed\. When this attribute is not set, all existing findings are listed\.
+ service\.resourceRole
+ severity
+ type
+ updatedAt

  Type: ISO 8601 string format: YYYY\-MM\-DDTHH:MM:SS\.SSSZ or YYYY\-MM\-DDTHH:MM:SSZ depending on whether the value contains milliseconds\.
*Required*: No  
*Type*: Json  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ItemType`  <a name="cfn-guardduty-filter-findingcriteria-itemtype"></a>
Specifies the condition to be applied to a single field when filtering through findings\.  
*Required*: No  
*Type*: [Condition](aws-properties-guardduty-filter-condition.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)