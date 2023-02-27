# AWS::WAFv2::WebACL Statement<a name="aws-properties-wafv2-webacl-statement"></a>

The processing guidance for a rule, used by AWS WAF to determine whether a web request matches the rule\. 

## Syntax<a name="aws-properties-wafv2-webacl-statement-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-wafv2-webacl-statement-syntax.json"></a>

```
{
  "[AndStatement](#cfn-wafv2-webacl-statement-andstatement)" : AndStatement,
  "[ByteMatchStatement](#cfn-wafv2-webacl-statement-bytematchstatement)" : ByteMatchStatement,
  "[GeoMatchStatement](#cfn-wafv2-webacl-statement-geomatchstatement)" : GeoMatchStatement,
  "[IPSetReferenceStatement](#cfn-wafv2-webacl-statement-ipsetreferencestatement)" : IPSetReferenceStatement,
  "[LabelMatchStatement](#cfn-wafv2-webacl-statement-labelmatchstatement)" : LabelMatchStatement,
  "[ManagedRuleGroupStatement](#cfn-wafv2-webacl-statement-managedrulegroupstatement)" : ManagedRuleGroupStatement,
  "[NotStatement](#cfn-wafv2-webacl-statement-notstatement)" : NotStatement,
  "[OrStatement](#cfn-wafv2-webacl-statement-orstatement)" : OrStatement,
  "[RateBasedStatement](#cfn-wafv2-webacl-statement-ratebasedstatement)" : RateBasedStatement,
  "[RegexMatchStatement](#cfn-wafv2-webacl-statement-regexmatchstatement)" : RegexMatchStatement,
  "[RegexPatternSetReferenceStatement](#cfn-wafv2-webacl-statement-regexpatternsetreferencestatement)" : RegexPatternSetReferenceStatement,
  "[RuleGroupReferenceStatement](#cfn-wafv2-webacl-statement-rulegroupreferencestatement)" : RuleGroupReferenceStatement,
  "[SizeConstraintStatement](#cfn-wafv2-webacl-statement-sizeconstraintstatement)" : SizeConstraintStatement,
  "[SqliMatchStatement](#cfn-wafv2-webacl-statement-sqlimatchstatement)" : SqliMatchStatement,
  "[XssMatchStatement](#cfn-wafv2-webacl-statement-xssmatchstatement)" : XssMatchStatement
}
```

### YAML<a name="aws-properties-wafv2-webacl-statement-syntax.yaml"></a>

```
  [AndStatement](#cfn-wafv2-webacl-statement-andstatement): 
    AndStatement
  [ByteMatchStatement](#cfn-wafv2-webacl-statement-bytematchstatement): 
    ByteMatchStatement
  [GeoMatchStatement](#cfn-wafv2-webacl-statement-geomatchstatement): 
    GeoMatchStatement
  [IPSetReferenceStatement](#cfn-wafv2-webacl-statement-ipsetreferencestatement): 
    IPSetReferenceStatement
  [LabelMatchStatement](#cfn-wafv2-webacl-statement-labelmatchstatement): 
    LabelMatchStatement
  [ManagedRuleGroupStatement](#cfn-wafv2-webacl-statement-managedrulegroupstatement): 
    ManagedRuleGroupStatement
  [NotStatement](#cfn-wafv2-webacl-statement-notstatement): 
    NotStatement
  [OrStatement](#cfn-wafv2-webacl-statement-orstatement): 
    OrStatement
  [RateBasedStatement](#cfn-wafv2-webacl-statement-ratebasedstatement): 
    RateBasedStatement
  [RegexMatchStatement](#cfn-wafv2-webacl-statement-regexmatchstatement): 
    RegexMatchStatement
  [RegexPatternSetReferenceStatement](#cfn-wafv2-webacl-statement-regexpatternsetreferencestatement): 
    RegexPatternSetReferenceStatement
  [RuleGroupReferenceStatement](#cfn-wafv2-webacl-statement-rulegroupreferencestatement): 
    RuleGroupReferenceStatement
  [SizeConstraintStatement](#cfn-wafv2-webacl-statement-sizeconstraintstatement): 
    SizeConstraintStatement
  [SqliMatchStatement](#cfn-wafv2-webacl-statement-sqlimatchstatement): 
    SqliMatchStatement
  [XssMatchStatement](#cfn-wafv2-webacl-statement-xssmatchstatement): 
    XssMatchStatement
```

## Properties<a name="aws-properties-wafv2-webacl-statement-properties"></a>

`AndStatement`  <a name="cfn-wafv2-webacl-statement-andstatement"></a>
A logical rule statement used to combine other rule statements with AND logic\. You provide more than one [Statement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-wafv2-webacl-notstatement.html#cfn-wafv2-webacl-notstatement-statement) within the `AndStatement`\.   
*Required*: No  
*Type*: [AndStatement](aws-properties-wafv2-webacl-andstatement.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ByteMatchStatement`  <a name="cfn-wafv2-webacl-statement-bytematchstatement"></a>
A rule statement that defines a string match search for AWS WAF to apply to web requests\. The byte match statement provides the bytes to search for, the location in requests that you want AWS WAF to search, and other settings\. The bytes to search for are typically a string that corresponds with ASCII characters\. In the AWS WAF console and the developer guide, this is called a string match statement\.  
*Required*: No  
*Type*: [ByteMatchStatement](aws-properties-wafv2-webacl-bytematchstatement.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`GeoMatchStatement`  <a name="cfn-wafv2-webacl-statement-geomatchstatement"></a>
A rule statement that labels web requests by country and region and that matches against web requests based on country code\. A geo match rule labels every request that it inspects regardless of whether it finds a match\.  
+ To manage requests only by country, you can use this statement by itself and specify the countries that you want to match against in the `CountryCodes` array\. 
+ Otherwise, configure your geo match rule with Count action so that it only labels requests\. Then, add one or more label match rules to run after the geo match rule and configure them to match against the geographic labels and handle the requests as needed\. 
 AWS WAF labels requests using the alpha\-2 country and region codes from the International Organization for Standardization \(ISO\) 3166 standard\. AWS WAF determines the codes using either the IP address in the web request origin or, if you specify it, the address in the geo match `ForwardedIPConfig`\.   
If you use the web request origin, the label formats are `awswaf:clientip:geo:region:<ISO country code>-<ISO region code>` and `awswaf:clientip:geo:country:<ISO country code>`\.  
If you use a forwarded IP address, the label formats are `awswaf:forwardedip:geo:region:<ISO country code>-<ISO region code>` and `awswaf:forwardedip:geo:country:<ISO country code>`\.  
For additional details, see [Geographic match rule statement](https://docs.aws.amazon.com/waf/latest/developerguide/waf-rule-statement-type-geo-match.html) in the [AWS WAF Developer Guide](https://docs.aws.amazon.com/waf/latest/developerguide/waf-chapter.html)\.   
*Required*: No  
*Type*: [GeoMatchStatement](aws-properties-wafv2-webacl-geomatchstatement.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IPSetReferenceStatement`  <a name="cfn-wafv2-webacl-statement-ipsetreferencestatement"></a>
A rule statement used to detect web requests coming from particular IP addresses or address ranges\. To use this, create an [AWS::WAFv2::IPSet](aws-resource-wafv2-ipset.md) that specifies the addresses you want to detect, then use the ARN of that set in this statement\.   
Each IP set rule statement references an IP set\. You create and maintain the set independent of your rules\. This allows you to use the single set in multiple rules\. When you update the referenced set, AWS WAF automatically updates all rules that reference it\.  
*Required*: No  
*Type*: [IPSetReferenceStatement](aws-properties-wafv2-webacl-ipsetreferencestatement.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LabelMatchStatement`  <a name="cfn-wafv2-webacl-statement-labelmatchstatement"></a>
A rule statement to match against labels that have been added to the web request by rules that have already run in the web ACL\.   
The label match statement provides the label or namespace string to search for\. The label string can represent a part or all of the fully qualified label name that had been added to the web request\. Fully qualified labels have a prefix, optional namespaces, and label name\. The prefix identifies the rule group or web ACL context of the rule that added the label\. If you do not provide the fully qualified name in your label match string, AWS WAF performs the search for labels that were added in the same context as the label match statement\.   
*Required*: No  
*Type*: [LabelMatchStatement](aws-properties-wafv2-webacl-labelmatchstatement.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ManagedRuleGroupStatement`  <a name="cfn-wafv2-webacl-statement-managedrulegroupstatement"></a>
A rule statement used to run the rules that are defined in a managed rule group\. To use this, provide the vendor name and the name of the rule group in this statement\.   
You cannot nest a `ManagedRuleGroupStatement`, for example for use inside a `NotStatement` or `OrStatement`\. It can only be referenced as a top\-level statement within a rule\.  
*Required*: No  
*Type*: [ManagedRuleGroupStatement](aws-properties-wafv2-webacl-managedrulegroupstatement.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NotStatement`  <a name="cfn-wafv2-webacl-statement-notstatement"></a>
A logical rule statement used to negate the results of another rule statement\. You provide one [Statement](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-properties-wafv2-webacl-notstatement.html#cfn-wafv2-webacl-notstatement-statement) within the `NotStatement`\.  
*Required*: No  
*Type*: [NotStatement](aws-properties-wafv2-webacl-notstatement.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`OrStatement`  <a name="cfn-wafv2-webacl-statement-orstatement"></a>
A logical rule statement used to combine other rule statements with OR logic\. You provide more than one `Statement` within the `OrStatement`\.   
*Required*: No  
*Type*: [OrStatement](aws-properties-wafv2-webacl-orstatement.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RateBasedStatement`  <a name="cfn-wafv2-webacl-statement-ratebasedstatement"></a>
A rate\-based rule tracks the rate of requests for each originating IP address, and triggers the rule action when the rate exceeds a limit that you specify on the number of requests in any 5\-minute time span\. You can use this to put a temporary block on requests from an IP address that is sending excessive requests\.   
 AWS WAF tracks and manages web requests separately for each instance of a rate\-based rule that you use\. For example, if you provide the same rate\-based rule settings in two web ACLs, each of the two rule statements represents a separate instance of the rate\-based rule and gets its own tracking and management by AWS WAF\. If you define a rate\-based rule inside a rule group, and then use that rule group in multiple places, each use creates a separate instance of the rate\-based rule that gets its own tracking and management by AWS WAF\.   
When the rule action triggers, AWS WAF blocks additional requests from the IP address until the request rate falls below the limit\.  
You can optionally nest another statement inside the rate\-based statement, to narrow the scope of the rule so that it only counts requests that match the nested statement\. For example, based on recent requests that you have seen from an attacker, you might create a rate\-based rule with a nested AND rule statement that contains the following nested statements:  
+ An IP match statement with an IP set that specifies the address 192\.0\.2\.44\.
+ A string match statement that searches in the User\-Agent header for the string BadBot\.
In this rate\-based rule, you also define a rate limit\. For this example, the rate limit is 1,000\. Requests that meet the criteria of both of the nested statements are counted\. If the count exceeds 1,000 requests per five minutes, the rule action triggers\. Requests that do not meet the criteria of both of the nested statements are not counted towards the rate limit and are not affected by this rule\.  
You cannot nest a `RateBasedStatement` inside another statement, for example inside a `NotStatement` or `OrStatement`\. You can define a `RateBasedStatement` inside a web ACL and inside a rule group\.   
*Required*: No  
*Type*: [RateBasedStatement](aws-properties-wafv2-webacl-ratebasedstatement.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RegexMatchStatement`  <a name="cfn-wafv2-webacl-statement-regexmatchstatement"></a>
A rule statement used to search web request components for a match against a single regular expression\.   
*Required*: No  
*Type*: [RegexMatchStatement](aws-properties-wafv2-webacl-regexmatchstatement.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RegexPatternSetReferenceStatement`  <a name="cfn-wafv2-webacl-statement-regexpatternsetreferencestatement"></a>
A rule statement used to search web request components for matches with regular expressions\. To use this, create a [AWS::WAFv2::RegexPatternSet](aws-resource-wafv2-regexpatternset.md) that specifies the expressions that you want to detect, then use the ARN of that set in this statement\. A web request matches the pattern set rule statement if the request component matches any of the patterns in the set\.   
Each regex pattern set rule statement references a regex pattern set\. You create and maintain the set independent of your rules\. This allows you to use the single set in multiple rules\. When you update the referenced set, AWS WAF automatically updates all rules that reference it\.  
*Required*: No  
*Type*: [RegexPatternSetReferenceStatement](aws-properties-wafv2-webacl-regexpatternsetreferencestatement.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RuleGroupReferenceStatement`  <a name="cfn-wafv2-webacl-statement-rulegroupreferencestatement"></a>
A rule statement used to run the rules that are defined in a [AWS::WAFv2::RuleGroup](aws-resource-wafv2-rulegroup.md)\. To use this, create a rule group with your rules, then provide the ARN of the rule group in this statement\.  
You cannot nest a `RuleGroupReferenceStatement`, for example for use inside a `NotStatement` or `OrStatement`\. You can only use a rule group reference statement at the top level inside a web ACL\.   
*Required*: No  
*Type*: [RuleGroupReferenceStatement](aws-properties-wafv2-webacl-rulegroupreferencestatement.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SizeConstraintStatement`  <a name="cfn-wafv2-webacl-statement-sizeconstraintstatement"></a>
A rule statement that compares a number of bytes against the size of a request component, using a comparison operator, such as greater than \(>\) or less than \(<\)\. For example, you can use a size constraint statement to look for query strings that are longer than 100 bytes\.   
If you configure AWS WAF to inspect the request body, AWS WAF inspects only the first 8192 bytes \(8 KB\)\. If the request body for your web requests never exceeds 8192 bytes, you could use a size constraint statement to block requests that have a request body greater than 8192 bytes\.  
If you choose URI for the value of Part of the request to filter on, the slash \(/\) in the URI counts as one character\. For example, the URI `/logo.jpg` is nine characters long\.  
*Required*: No  
*Type*: [SizeConstraintStatement](aws-properties-wafv2-webacl-sizeconstraintstatement.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SqliMatchStatement`  <a name="cfn-wafv2-webacl-statement-sqlimatchstatement"></a>
A rule statement that inspects for malicious SQL code\. Attackers insert malicious SQL code into web requests to do things like modify your database or extract data from it\.   
*Required*: No  
*Type*: [SqliMatchStatement](aws-properties-wafv2-webacl-sqlimatchstatement.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`XssMatchStatement`  <a name="cfn-wafv2-webacl-statement-xssmatchstatement"></a>
A rule statement that inspects for cross\-site scripting \(XSS\) attacks\. In XSS attacks, the attacker uses vulnerabilities in a benign website as a vehicle to inject malicious client\-site scripts into other legitimate web browsers\.   
*Required*: No  
*Type*: [XssMatchStatement](aws-properties-wafv2-webacl-xssmatchstatement.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)