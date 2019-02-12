#
# B2B, B2C Integration
	
Product is capable of exposing services for integration. API layer is clearly identified and exposed business entities are modeled according to the best practices.

#
# Implementation - 01

### Scope
Following implementation is applicable to the projects that uses AWS and AWS Cognito for handling user authentication and authorization

### Cloud Service
- [AWS Cognito](https://aws.amazon.com/cognito/)

### Description
Cognito is HIPAA eligible and PCI DSS, SOC, and ISO/IEC 27001, ISO/EIC 27017, ISO/EIC 27018, and ISO 9001 compliant. Cognito allows users to integrate with different application via standard protocols. It supports OpenID Connect, SAML and Auth2.0 

### How?
- Create a client application in Cognito that is attached to a userpool
- Get the SAML/Auth2/OpenID Connect configuration from the connecting application
- Set the configuration under identity provider settings
- Get the configuration from the Cognito app client 
- Update the configuration on the integrating application (Eg: Redirect URL etc..)

### Tips
- You can use Cognito for SSO easily with Cognito Userpool
- For B2B integrations, use a suitable OAuth flow (eg: Client Credentials etc...)