# AWS::ACMPCA::Certificate Validity<a name="aws-properties-acmpca-certificate-validity"></a>

Validity specifies the period of time during which a certificate is valid\. Validity can be expressed as an explicit date and time when the certificate expires, or as a span of time after issuance, stated in days, months, or years\. For more information, see [Validity](https://tools.ietf.org/html/rfc5280#section-4.1.2.5) in RFC 5280\.

You can issue a certificate by calling the [IssueCertificate](https://docs.aws.amazon.com/acm-pca/latest/APIReference/API_IssueCertificate.html) action\.

## Syntax<a name="aws-properties-acmpca-certificate-validity-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-acmpca-certificate-validity-syntax.json"></a>

```
{
  "[Type](#cfn-acmpca-certificate-validity-type)" : String,
  "[Value](#cfn-acmpca-certificate-validity-value)" : Integer
}
```

### YAML<a name="aws-properties-acmpca-certificate-validity-syntax.yaml"></a>

```
  [Type](#cfn-acmpca-certificate-validity-type): String
  [Value](#cfn-acmpca-certificate-validity-value): Integer
```

## Properties<a name="aws-properties-acmpca-certificate-validity-properties"></a>

`Type`  <a name="cfn-acmpca-certificate-validity-type"></a>
Determines how *ACM Private CA* interprets the `Value` parameter, an integer\. Supported validity types include those listed below\. Type definitions with values include a sample input value and the resulting output\.   
 `END_DATE`: The specific date and time when the certificate will expire, expressed using UTCTime \(YYMMDDHHMMSS\) or GeneralizedTime \(YYYYMMDDHHMMSS\) format\. When UTCTime is used, if the year field \(YY\) is greater than or equal to 50, the year is interpreted as 19YY\. If the year field is less than 50, the year is interpreted as 20YY\.  
+ Sample input value: 491231235959 \(UTCTime format\)
+ Output expiration date/time: 12/31/2049 23:59:59
 `ABSOLUTE`: The specific date and time when the certificate will expire, expressed in seconds since the Unix Epoch\.   
+ Sample input value: 2524608000
+ Output expiration date/time: 01/01/2050 00:00:00
 `DAYS`, `MONTHS`, `YEARS`: The relative time from the moment of issuance until the certificate will expire, expressed in days, months, or years\.   
Example if `DAYS`, issued on 10/12/2020 at 12:34:54 UTC:  
+ Sample input value: 90
+ Output expiration date: 01/10/2020 12:34:54 UTC
The minimum validity duration for a certificate using relative time \(`DAYS`\) is one day\. The minimum validity for a certificate using absolute time \(`ABSOLUTE` or `END_DATE`\) is one second\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `ABSOLUTE | DAYS | END_DATE | MONTHS | YEARS`  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)

`Value`  <a name="cfn-acmpca-certificate-validity-value"></a>
A long integer interpreted according to the value of `Type`, below\.  
*Required*: Yes  
*Type*: Integer  
*Update requires*: [Replacement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-replacement)