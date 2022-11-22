Wallet Payment API End Points
Deposits
End Point https://customerservice.walletpayment.net/
api/v1/deposits
Method POST
Header Authorization
Token Creation
Issuer Walletpayment.net
Expires In 10 Minutes
Secret Merchant Key (From Mobile App)
Request
Payload
 {
 'txnid': transactionID,
 'amount': coins,
 'type': type,
 'address': address,
 'cid': customerId,
 'name': customerName,
 'email': customerEmail,
 'mobile': customerPhone,
 'successUrl': successUrl,
 'failureUrl': successUrl,
 'webhookUrl': webhookUrl
 }
Webhook
Response
data from Query Parameter or
Authorization Token in Response
Response
Payload
Decrypt JWT Response using Merchant Key
{
 "referenceNo": referenceNo (our id),
 "transactionId": transactionId (Your id in db),
 "transactionhash": transactionhash (blockchain),
 "status": status (Approved /Rejected)
}
Withdraw
End Point https://customerservice.walletpayment.net/
api/v1/requests
Method POST
Header Authorization
Token Creation
Issuer Walletpayment.net
Expires In 10 Minutes
Secret Merchant Key (From Mobile App)
Request
Payload
 {
 'txnid': transactionID,
 'amount': coins,
 'type': type,
 'address': address,
 'cid': customerId,
 'name': customerName,
 'email': customerEmail,
 'mobile': customerPhone,
 'webhookUrl': webhookUrl
 }
Webhook
Response
data from Query Parameter or
Authorization Token in Response
Response
Payload
Decrypt JWT Response using Merchant Key
{
 "referenceNo": referenceNo (our id),
 "transactionId": transactionId (Your id in db),
 "transactionhash": transactionhash (blockchain),
 "status": status (Approved /Rejected)
}
Or Validation Error
Whitelisting
End Point https://customerservice.walletpayment.net/
api/v1/whitelist
Method POST
Header Authorization
Token Creation
Issuer Walletpayment.net
Expires In 10 Minutes
Secret Merchant Key (From Mobile App)
Request
Payload
 {
 "address" : "Test",
 "type" : "BNB",
 "customerName" : "Developer",
 "customerEmail" : "test@test.com",
 "customerPhone" : "9876543210",
 "customerId" : "Test123",
 "minCoins" : 0.002,
 "maxCoins" : 1
}
Response
Payload
True or Error
