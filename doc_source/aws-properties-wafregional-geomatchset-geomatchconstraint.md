# AWS::WAFRegional::GeoMatchSet GeoMatchConstraint<a name="aws-properties-wafregional-geomatchset-geomatchconstraint"></a>

**Note**  
This is **AWS WAF Classic** documentation\. For more information, see [AWS WAF Classic](https://docs.aws.amazon.com/waf/latest/developerguide/classic-waf-chapter.html) in the developer guide\.  
 **For the latest version of AWS WAF**, use the AWS WAFV2 API and see the [AWS WAF Developer Guide](https://docs.aws.amazon.com/waf/latest/developerguide/waf-chapter.html)\. With the latest version, AWS WAF has a single set of endpoints for regional and global use\. 

The country from which web requests originate that you want AWS WAF to search for\.

## Syntax<a name="aws-properties-wafregional-geomatchset-geomatchconstraint-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-wafregional-geomatchset-geomatchconstraint-syntax.json"></a>

```
{
  "[Type](#cfn-wafregional-geomatchset-geomatchconstraint-type)" : String,
  "[Value](#cfn-wafregional-geomatchset-geomatchconstraint-value)" : String
}
```

### YAML<a name="aws-properties-wafregional-geomatchset-geomatchconstraint-syntax.yaml"></a>

```
  [Type](#cfn-wafregional-geomatchset-geomatchconstraint-type): String
  [Value](#cfn-wafregional-geomatchset-geomatchconstraint-value): String
```

## Properties<a name="aws-properties-wafregional-geomatchset-geomatchconstraint-properties"></a>

`Type`  <a name="cfn-wafregional-geomatchset-geomatchconstraint-type"></a>
The type of geographical area you want AWS WAF to search for\. Currently `Country` is the only valid value\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `Country`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`Value`  <a name="cfn-wafregional-geomatchset-geomatchconstraint-value"></a>
The country that you want AWS WAF to search for\.  
*Required*: Yes  
*Type*: String  
*Allowed values*: `AD | AE | AF | AG | AI | AL | AM | AO | AQ | AR | AS | AT | AU | AW | AX | AZ | BA | BB | BD | BE | BF | BG | BH | BI | BJ | BL | BM | BN | BO | BQ | BR | BS | BT | BV | BW | BY | BZ | CA | CC | CD | CF | CG | CH | CI | CK | CL | CM | CN | CO | CR | CU | CV | CW | CX | CY | CZ | DE | DJ | DK | DM | DO | DZ | EC | EE | EG | EH | ER | ES | ET | FI | FJ | FK | FM | FO | FR | GA | GB | GD | GE | GF | GG | GH | GI | GL | GM | GN | GP | GQ | GR | GS | GT | GU | GW | GY | HK | HM | HN | HR | HT | HU | ID | IE | IL | IM | IN | IO | IQ | IR | IS | IT | JE | JM | JO | JP | KE | KG | KH | KI | KM | KN | KP | KR | KW | KY | KZ | LA | LB | LC | LI | LK | LR | LS | LT | LU | LV | LY | MA | MC | MD | ME | MF | MG | MH | MK | ML | MM | MN | MO | MP | MQ | MR | MS | MT | MU | MV | MW | MX | MY | MZ | NA | NC | NE | NF | NG | NI | NL | NO | NP | NR | NU | NZ | OM | PA | PE | PF | PG | PH | PK | PL | PM | PN | PR | PS | PT | PW | PY | QA | RE | RO | RS | RU | RW | SA | SB | SC | SD | SE | SG | SH | SI | SJ | SK | SL | SM | SN | SO | SR | SS | ST | SV | SX | SY | SZ | TC | TD | TF | TG | TH | TJ | TK | TL | TM | TN | TO | TR | TT | TV | TW | TZ | UA | UG | UM | US | UY | UZ | VA | VC | VE | VG | VI | VN | VU | WF | WS | YE | YT | ZA | ZM | ZW`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)