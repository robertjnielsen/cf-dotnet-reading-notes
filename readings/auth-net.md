# Auth<span></span>.Net

## What Is Auth<span></span>.Net?

Authorize<span></span>.Net is a payment processing and verification API service. It works by a merchant sending a secure JSON (or XML) object to the Authorize<span></span>.Net service, who will in turn pass that information on to the banking or credit agency. The information will be verified, and a response will be returned indicating whether the payment can be authorized or not.

## Live VS Sandbox

Authorize<span></span>.Net allows the use of two API services for developers, the live service, which accepts genuine payment and transaction data and will attempt to process that data to collect payment; and the sandbox API environment that is used for testing purposes.

Within the sandbox environment, developers can use predeclared credit card numbers and information to make "purchases" on the vendor site. This information will then generate a response based on given parameters, such as an address or zip code, or a card security number, etc.

In the sandbox environment, none of these financial accounts and cards are real, and the payment processing is simulated. This makes Authorize<span></span>.Net a great resource to develop an ecommerce application and run tests to ensure that payment processing will succeed in a production environment without anyone having to spend real money.