# AWS::WAFv2::RuleGroup StatementTwo<a name="aws-properties-wafv2-rulegroup-statementtwo"></a>

Rules statement\. 

## Syntax<a name="aws-properties-wafv2-rulegroup-statementtwo-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-wafv2-rulegroup-statementtwo-syntax.json"></a>

```
{
  "[AndStatement](#cfn-wafv2-rulegroup-statementtwo-andstatement)" : AndStatementTwo,
  "[ByteMatchStatement](#cfn-wafv2-rulegroup-statementtwo-bytematchstatement)" : ByteMatchStatement,
  "[GeoMatchStatement](#cfn-wafv2-rulegroup-statementtwo-geomatchstatement)" : GeoMatchStatement,
  "[IPSetReferenceStatement](#cfn-wafv2-rulegroup-statementtwo-ipsetreferencestatement)" : IPSetReferenceStatement,
  "[NotStatement](#cfn-wafv2-rulegroup-statementtwo-notstatement)" : NotStatementTwo,
  "[OrStatement](#cfn-wafv2-rulegroup-statementtwo-orstatement)" : OrStatementTwo,
  "[RateBasedStatement](#cfn-wafv2-rulegroup-statementtwo-ratebasedstatement)" : RateBasedStatementTwo,
  "[RegexPatternSetReferenceStatement](#cfn-wafv2-rulegroup-statementtwo-regexpatternsetreferencestatement)" : RegexPatternSetReferenceStatement,
  "[SizeConstraintStatement](#cfn-wafv2-rulegroup-statementtwo-sizeconstraintstatement)" : SizeConstraintStatement,
  "[SqliMatchStatement](#cfn-wafv2-rulegroup-statementtwo-sqlimatchstatement)" : SqliMatchStatement,
  "[XssMatchStatement](#cfn-wafv2-rulegroup-statementtwo-xssmatchstatement)" : XssMatchStatement
}
```

### YAML<a name="aws-properties-wafv2-rulegroup-statementtwo-syntax.yaml"></a>

```
  [AndStatement](#cfn-wafv2-rulegroup-statementtwo-andstatement): 
    AndStatementTwo
  [ByteMatchStatement](#cfn-wafv2-rulegroup-statementtwo-bytematchstatement): 
    ByteMatchStatement
  [GeoMatchStatement](#cfn-wafv2-rulegroup-statementtwo-geomatchstatement): 
    GeoMatchStatement
  [IPSetReferenceStatement](#cfn-wafv2-rulegroup-statementtwo-ipsetreferencestatement): 
    IPSetReferenceStatement
  [NotStatement](#cfn-wafv2-rulegroup-statementtwo-notstatement): 
    NotStatementTwo
  [OrStatement](#cfn-wafv2-rulegroup-statementtwo-orstatement): 
    OrStatementTwo
  [RateBasedStatement](#cfn-wafv2-rulegroup-statementtwo-ratebasedstatement): 
    RateBasedStatementTwo
  [RegexPatternSetReferenceStatement](#cfn-wafv2-rulegroup-statementtwo-regexpatternsetreferencestatement): 
    RegexPatternSetReferenceStatement
  [SizeConstraintStatement](#cfn-wafv2-rulegroup-statementtwo-sizeconstraintstatement): 
    SizeConstraintStatement
  [SqliMatchStatement](#cfn-wafv2-rulegroup-statementtwo-sqlimatchstatement): 
    SqliMatchStatement
  [XssMatchStatement](#cfn-wafv2-rulegroup-statementtwo-xssmatchstatement): 
    XssMatchStatement
```

## Properties<a name="aws-properties-wafv2-rulegroup-statementtwo-properties"></a>

`AndStatement`  <a name="cfn-wafv2-rulegroup-statementtwo-andstatement"></a>
Logical AND statement used in statement nesting\.  
*Required*: No  
*Type*: [AndStatementTwo](aws-properties-wafv2-rulegroup-andstatementtwo.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ByteMatchStatement`  <a name="cfn-wafv2-rulegroup-statementtwo-bytematchstatement"></a>
A rule statement that defines a string match search for AWS WAF to apply to web requests\. The byte match statement provides the bytes to search for, the location in requests that you want AWS WAF to search, and other settings\. The bytes to search for are typically a string that corresponds with ASCII characters\. In the AWS WAF console and the developer guide, this is refered to as a string match statement\.  
*Required*: No  
*Type*: [ByteMatchStatement](aws-properties-wafv2-rulegroup-bytematchstatement.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`GeoMatchStatement`  <a name="cfn-wafv2-rulegroup-statementtwo-geomatchstatement"></a>
Statement used to identify web requests based on country of origin\.  
*Required*: No  
*Type*: [GeoMatchStatement](aws-properties-wafv2-rulegroup-geomatchstatement.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IPSetReferenceStatement`  <a name="cfn-wafv2-rulegroup-statementtwo-ipsetreferencestatement"></a>
Statement that references a set of IP addresses to compare to incoming requests\.   
*Required*: No  
*Type*: [IPSetReferenceStatement](aws-properties-wafv2-rulegroup-ipsetreferencestatement.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NotStatement`  <a name="cfn-wafv2-rulegroup-statementtwo-notstatement"></a>
Logical NOT statement used to negate the match results of a nested statement\.  
*Required*: No  
*Type*: [NotStatementTwo](aws-properties-wafv2-rulegroup-notstatementtwo.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`OrStatement`  <a name="cfn-wafv2-rulegroup-statementtwo-orstatement"></a>
Logical OR statement\.  
*Required*: No  
*Type*: [OrStatementTwo](aws-properties-wafv2-rulegroup-orstatementtwo.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RateBasedStatement`  <a name="cfn-wafv2-rulegroup-statementtwo-ratebasedstatement"></a>
A rate\-based rule tracks the rate of requests for each originating IP address, and triggers the rule action when the rate exceeds a limit that you specify on the number of requests in any 5\-minute time span\. You can use this to put a temporary block on requests from an IP address that's sending excessive requests\.   
 When the rule action triggers, AWS WAF blocks additional requests from the IP address until the request rate falls below the limit\.   
 You can optionally nest another statement inside the rate\-based statement, to narrow the scope of the rule so that it only counts requests that match the nested statement\. You can't nest a RateBasedStatement, for example for use inside a NotStatement or OrStatement\. It can only be referenced as a top\-level statement within a rule\.  
*Required*: No  
*Type*: [RateBasedStatementTwo](aws-properties-wafv2-rulegroup-ratebasedstatementtwo.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RegexPatternSetReferenceStatement`  <a name="cfn-wafv2-rulegroup-statementtwo-regexpatternsetreferencestatement"></a>
A rule statement used to search web request components for matches with regular expressions\. To use this, create a RegexPatternSet with the expressions that you want to detect, then use that set in this statement\. A web request matches the pattern set rule statement if the request component matches any of the patterns in the set\.  
*Required*: No  
*Type*: [RegexPatternSetReferenceStatement](aws-properties-wafv2-rulegroup-regexpatternsetreferencestatement.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SizeConstraintStatement`  <a name="cfn-wafv2-rulegroup-statementtwo-sizeconstraintstatement"></a>
A rule statement that compares a number of bytes against the size of a request component, using a comparison operator, such as greater than or less than\. For example, you can use a size constraint statement to look for query strings that are longer than 100 bytes\.  
If you configure AWS WAF to inspect the request body, AWS WAF inspects only the first 8192 bytes \(8 KB\)\. If the request body for your web requests never exceeds 8192 bytes, you can create a size constraint condition and block requests that have a request body greater than 8192 bytes\.  
If you choose URI for the value of Part of the request to filter on, the slash \(/\) in the URI counts as one character\. For example, the URI /logo\.jpg is nine characters long\.  
*Required*: No  
*Type*: [SizeConstraintStatement](aws-properties-wafv2-rulegroup-sizeconstraintstatement.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SqliMatchStatement`  <a name="cfn-wafv2-rulegroup-statementtwo-sqlimatchstatement"></a>
Attackers sometimes insert malicious SQL code into web requests in an effort to extract data from your database\. To allow or block web requests that appear to contain malicious SQL code, create one or more SQL injection match conditions\. An SQL injection match condition identifies the part of web requests, such as the URI or the query string, that you want AWS WAF to inspect\. Later in the process, when you create a web ACL, you specify whether to allow or block requests that appear to contain malicious SQL code\.  
*Required*: No  
*Type*: [SqliMatchStatement](aws-properties-wafv2-rulegroup-sqlimatchstatement.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`XssMatchStatement`  <a name="cfn-wafv2-rulegroup-statementtwo-xssmatchstatement"></a>
A rule statement that defines a cross\-site scripting \(XSS\) match search for AWS WAF to apply to web requests\. XSS attacks are those where the attacker uses vulnerabilities in a benign website as a vehicle to inject malicious client\-site scripts into other legitimate web browsers\. The XSS match statement provides the location in requests that you want AWS WAF to search and text transformations to use on the search area before AWS WAF searches for character sequences that are likely to be malicious strings\.  
*Required*: No  
*Type*: [XssMatchStatement](aws-properties-wafv2-rulegroup-xssmatchstatement.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)