# LNURL Withdraw

{% api-method method="get" host="https://lnpay.co/v1/user/wallet" path="/:access\_key/lnurl/withdraw" %}
{% api-method-summary %}
GetWalletLnurlWithdraw
{% endapi-method-summary %}

{% api-method-description %}
Generate an LNURL-withdraw link. 
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="access\_key" type="string" required=true %}
access\_key with admin permission
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-query-parameters %}
{% api-method-parameter name="num\_satoshis" type="string" required=false %}
Max number of satoshis this LNURL is good for.   
  
If blank max wallet balance is used
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Cake successfully retrieved.
{% endapi-method-response-example-description %}

```text
{
    "lnurl":"LNURL1DP68GURN8GHJ7MRWWPSHJTNRDUHHVVF0W4EK2U30WASKCMR9WSHHWC2LFACXUM35DDR5736ZF4HXVS6VGEV8GU6YDE49GC30D3H82UNV94C8YMMRV4EHX0M0W36R66MGD95KS4JGFADRS4ZRFEXK2SN2FFUXUSMHFA98XDZ8D3T9SDECWVHR43",
    "num_satoshis":15
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% hint style="info" %}
Note: These LNURLs are ONE-TIME use. This is to prevent repeated access to the wallet.
{% endhint %}

```bash
$ curl -u yg20O0iUMxk8kK_qUzkT4YKFvp1ZsUtp: \
https://lnpay.co/v1/user/wallet/wa_Opnn4kGOGBMnfCLFXtsDnjTb/lnurl/withdraw?num_satoshis=3

# We are using the "admin" access key in this instance as denoted by the "wa_"
```
