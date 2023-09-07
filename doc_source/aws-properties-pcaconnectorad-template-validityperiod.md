# AWS::PCAConnectorAD::Template ValidityPeriod<a name="aws-properties-pcaconnectorad-template-validityperiod"></a>

Information describing the end of the validity period of the certificate\. This parameter sets the “Not After” date for the certificate\. Certificate validity is the period of time during which a certificate is valid\. Validity can be expressed as an explicit date and time when the certificate expires, or as a span of time after issuance, stated in hours, days, months, or years\. For more information, see Validity in RFC 5280\. This value is unaffected when ValidityNotBefore is also specified\. For example, if Validity is set to 20 days in the future, the certificate will expire 20 days from issuance time regardless of the ValidityNotBefore value\. 

## Syntax<a name="aws-properties-pcaconnectorad-template-validityperiod-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-pcaconnectorad-template-validityperiod-syntax.json"></a>

```
{
  "[Period](#cfn-pcaconnectorad-template-validityperiod-period)" : Double,
  "[PeriodType](#cfn-pcaconnectorad-template-validityperiod-periodtype)" : String
}
```

### YAML<a name="aws-properties-pcaconnectorad-template-validityperiod-syntax.yaml"></a>

```
  [Period](#cfn-pcaconnectorad-template-validityperiod-period): Double
  [PeriodType](#cfn-pcaconnectorad-template-validityperiod-periodtype): String
```

## Properties<a name="aws-properties-pcaconnectorad-template-validityperiod-properties"></a>

`Period`  <a name="cfn-pcaconnectorad-template-validityperiod-period"></a>
The numeric value for the validity period\.  
*Required*: Yes  
*Type*: Double  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`PeriodType`  <a name="cfn-pcaconnectorad-template-validityperiod-periodtype"></a>
The unit of time\. You can select hours, days, weeks, months, and years\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `DAYS | HOURS | MONTHS | WEEKS | YEARS`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)