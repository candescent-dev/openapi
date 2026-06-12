# Changelog

## [1.6.0] - 2026-06-12

### Spec-level breaking changes ⚠️
- Security schemes removed: ClientAuthBasic

### Breaking changes (37 paths)
- `/oauth2/v1/revoke`
- `/oauth2/v1/token`
- `/v1/alert-history`
- `/v1/alert-history-content`
- `/v1/alert-preferences`
- `/v1/alert-preferences/{alertPreferenceId}`
- `/v1/alert-templates`
- `/v1/alert-templates/{id}`
- `/v1/alert-types`
- `/v1/alert-types/{id}`
- `/v1/auth-code`
- `/v1/banking-activities`
- `/v1/business-details`
- `/v1/business-entitlements-limits`
- `/v1/business-registration-configs`
- `/v1/business-registrations`
- `/v1/business-registrations/{registrationId}`
- `/v1/client-authorization`
- `/v1/fis/{di_fiid}/fiCustomers/{di_ficustomer}/events`
- `/v1/fis/{di_fiid}/fiCustomers/{di_ficustomer}/subscriptions`
- `/v1/fis/{di_fiid}/fiCustomers/{di_ficustomer}/subscriptions/{subscription_id}`
- `/v1/fis/{di_fiid}/subscriptions`
- `/v1/institution-alert-preferences`
- `/v1/institution-alert-preferences/{institutionAlertPreferenceId}`
- `/v1/institution-alert-types`
- `/v1/institution-alert-types/{id}`
- `/v1/institution-user-disclosures`
- `/v1/institution-users/{institutionUserId}`
- `/v1/oauth/token`
- `/v1/realtime-events`
- … and 7 more

### Schemas removed (14) ⚠️ Breaking
- `AccessTokenRequest`
- `AccessTokenRequest1`
- `AccessTokenResponse`
- `AccessTokenResponse1`
- `ClientCredentialsGrantRequest`
- `ClientCredentialsGrantResponse`
- `ErrorInfo19`
- `ErrorInfo20`
- `PasswordGrantRequest`
- `PasswordGrantResponse`
- `TokenRequestBase`
- `TokenRequestBase1`
- `TokenResponseBase`
- `TokenResponseBase1`

### Schemas — breaking changes (19)
- `AccountType1`
- `AccountType2`
- `AuthorizationCodeRequest`
- `AuthorizationCodeResponse`
- `ClientCredentialsRequest`
- `ClientCredentialsResponse`
- `CurrencyCode1`
- `CurrencyCode6`
- `Error4`
- `ErrorInfo`
- `ErrorInfo10`
- `ErrorInfo11`
- `ErrorInfo13`
- `ErrorInfo15`
- `ErrorInfo8`
- `PasswordRequest`
- `PasswordResponse`
- `RefreshTokenRequest`
- `RefreshTokenResponse`

### Schemas added (2)
- `Error6`
- `Token`

### Schemas updated (18)
- `AccountTransaction`
- `AchTransaction`
- `Balance1`
- `BankingImage`
- `DomesticWireTransaction`
- `ErrorInfo1`
- `InternationalWireTransaction`
- `Money1`
- `Money2`
- `Money3`
- `Money4`
- `Money5`
- `RevokeAccessTokenRequest`
- `Status`
- `Status1`
- `Status3`
- `Transaction`
- `UXAccount`

## [1.6.1] - 2026-06-12

### Spec-level breaking changes ⚠️
- Base URL / servers changed
- Security schemes removed: BearerAuth

### Removed (63 paths) ⚠️ Breaking
- `/audience/v1/userlists`
- `/auth-code/v1/auth-code`
- `/auth-code/v1/client-authorization`
- `/bankingservices/v2/fis/{di_fiid}/fiCustomers/{di_ficustomer}/accounts`
- `/bankingservices/v2/fis/{fiId}/fiCustomers/{fiCustomerId}`
- `/data-apis/v1/banking-activities`
- `/db-accounts/v1/accounts`
- `/db-accounts/v1/accounts/{accountId}`
- `/db-alerts-delivery/v1/alert-history`
- `/db-alerts-delivery/v1/alert-history-content`
- `/db-alerts-management/v1/alert-templates`
- `/db-alerts-management/v1/alert-templates/{id}`
- `/db-alerts-management/v1/alert-types`
- `/db-alerts-management/v1/alert-types/{id}`
- `/db-alerts-management/v1/institution-alert-types`
- `/db-alerts-management/v1/institution-alert-types/{id}`
- `/db-alerts-preferences/v1/alert-preferences`
- `/db-alerts-preferences/v1/alert-preferences/{alertPreferenceId}`
- `/db-alerts-preferences/v1/institution-alert-preferences`
- `/db-alerts-preferences/v1/institution-alert-preferences/{institutionAlertPreferenceId}`
- … and 43 more

### Breaking changes (9 paths)
- `/mx/download/{institution_id}/{date}/transactions/created`
- `/mx/users`
- `/mx/{institution_id}/users/{user_id}`
- `/mx/{institution_id}/users/{user_id}/urls/mini_budgets_widget`
- `/oauth2/v1/revoke`
- `/oauth2/v1/token`
- `/pss/v1/fis/{fiId}/audiences/userListJobs`
- `/pss/v1/fis/{fiId}/audiences/userListJobs/{jobId}`
- `/v1/oauth/token`

### Schemas removed (25) ⚠️ Breaking
- `Account2`
- `AccountCategory2`
- `AccountCategory3`
- `AccountEvent`
- `AccountStatus3`
- `AccountType3`
- `Account_Nickname`
- `Actions1`
- `DIAccountType4`
- `EStatementPreferencesResponse`
- `Error6`
- `ImageType2`
- `Map`
- `NonSubscriptionEvent`
- `Notification`
- `NotificationEvent`
- `PhoneNumber`
- `PostalAddress1`
- `Term1`
- `TermType2`
- … and 5 more

### Schemas — breaking changes (29)
- `Account`
- `Account1`
- `AccountStatus`
- `AccountStatus1`
- `AccountStatus2`
- `AccountType1`
- `Actions`
- `AuthorizationCodeRequest`
- `AuthorizationCodeResponse`
- `ClientCredentialsRequest`
- `ClientCredentialsResponse`
- `CurrencyCode1`
- `CurrencyCode6`
- `DIAccountType3`
- `Error4`
- `ErrorInfo`
- `ErrorInfo1`
- `ErrorInfo10`
- `ErrorInfo13`
- `ErrorInfo15`
- … and 9 more

### Added (63 paths)
- `/v1/accounts`
- `/v1/accounts/{accountId}`
- `/v1/ach-payments`
- `/v1/ach-payments/{paymentId}`
- `/v1/alert-history`
- `/v1/alert-history-content`
- `/v1/alert-preferences`
- `/v1/alert-preferences/{alertPreferenceId}`
- `/v1/alert-templates`
- `/v1/alert-templates/{id}`
- `/v1/alert-types`
- `/v1/alert-types/{id}`
- `/v1/auth-code`
- `/v1/banking-activities`
- `/v1/banking-images`
- `/v1/banking-images/{bankingImageId}`
- `/v1/business-details`
- `/v1/business-entitlements-limits`
- `/v1/business-registration-configs`
- `/v1/business-registrations`
- … and 43 more

### Schemas added (14)
- `AccessTokenRequest`
- `AccessTokenRequest1`
- `AccessTokenResponse`
- `AccessTokenResponse1`
- `ClientCredentialsGrantRequest`
- `ClientCredentialsGrantResponse`
- `ErrorInfo19`
- `ErrorInfo20`
- `PasswordGrantRequest`
- `PasswordGrantResponse`
- `TokenRequestBase`
- `TokenRequestBase1`
- `TokenResponseBase`
- `TokenResponseBase1`

### Schemas updated (28)
- `AccountTransaction`
- `AccountType`
- `AccountsResponse`
- `AchTransaction`
- `Balance1`
- `BankingImage`
- `CustomerInformation`
- `DIAccountType`
- `DIAccountType1`
- `DIAccountType2`
- `DepositAccount`
- `DomesticWireTransaction`
- `ErrorInfo11`
- `ImageType`
- `InternationalWireTransaction`
- `LoanAccount`
- `Money1`
- `Money2`
- `Money3`
- `Money4`
- … and 8 more

## [1.5.0] - 2026-05-21

### Spec-level breaking changes ⚠️
- Security schemes changed: BearerAuth

### Breaking changes (43 paths)
- `/auth-code/v1/auth-code`
- `/auth-code/v1/client-authorization`
- `/bankingservices/v2/fis/{di_fiid}/fiCustomers/{di_ficustomer}/accounts`
- `/data-apis/v1/banking-activities`
- `/db-accounts/v1/accounts`
- `/db-accounts/v1/accounts/{accountId}`
- `/db-alerts-delivery/v1/alert-history`
- `/db-alerts-delivery/v1/alert-history-content`
- `/db-alerts-management/v1/alert-templates`
- `/db-alerts-management/v1/alert-templates/{id}`
- `/db-alerts-management/v1/alert-types`
- `/db-alerts-management/v1/alert-types/{id}`
- `/db-alerts-management/v1/institution-alert-types`
- `/db-alerts-management/v1/institution-alert-types/{id}`
- `/db-alerts-preferences/v1/alert-preferences`
- `/db-alerts-preferences/v1/alert-preferences/{alertPreferenceId}`
- `/db-alerts-preferences/v1/institution-alert-preferences`
- `/db-alerts-preferences/v1/institution-alert-preferences/{institutionAlertPreferenceId}`
- `/db-banking-images/v1/banking-images`
- `/db-banking-images/v1/banking-images/{bankingImageId}`
- `/db-bb-core/v1/business-details`
- `/db-bb-core/v1/business-registration-configs`
- `/db-bb-core/v1/business-registrations`
- `/db-bb-core/v1/business-registrations/{registrationId}`
- `/db-bb-entitlements/v1/business-entitlements-limits`
- `/db-bb-entitlements/v1/user-entitlements-limits`
- `/db-disclosures/v1/institution-disclosures`
- `/db-disclosures/v1/institution-disclosures/{institutionDisclosureId}`
- `/db-disclosures/v1/institution-user-disclosures`
- `/db-events/v1/realtime-events`
- … and 13 more

### Schemas removed (22) ⚠️ Breaking
- `Account3`
- `AccountRefreshStatus`
- `AccountTransaction1`
- `AccountTransactions`
- `Accounts1`
- `Calendar`
- `Controls`
- `CustomerRequest`
- `Filter`
- `HealthStatus`
- `HostTransactionType`
- `InstitutionDisclosures`
- `InstitutionUserDisclosures`
- `Limit`
- `Limits`
- `SearchCriteriaRequestBody`
- `SearchResultResponse`
- `StatementType`
- `TimeZone`
- `TransactionCategory`
- … and 2 more

### Schemas — breaking changes (30)
- `Account`
- `Account1`
- `Account2`
- `AccountId`
- `AccountNumber`
- `AccountStatus1`
- `AccountTransaction`
- `AccountType1`
- `Accounts`
- `Action`
- `AdditionalFilters`
- `Balance1`
- `BankingImage`
- `BankingImages`
- `ContactMethod`
- `CustomerInformation`
- `DisplayFlag`
- `Entitlement`
- `Entitlements`
- `Error5`
- … and 10 more

### Added (4 paths)
- `/db-bb-payments/bbpayments/v1/ach-payments`
- `/db-bb-payments/bbpayments/v1/ach-payments/{paymentId}`
- `/db-bb-payments/bbpayments/v1/wire-payments`
- `/db-bb-payments/bbpayments/v1/wire-payments/{paymentId}`

### Updated (3 paths)
- `/db-users/v1/user-status/{userId}`
- `/mx/{institution_id}/users/{user_id}`
- `/mx/{institution_id}/users/{user_id}/urls/mini_budgets_widget`

### Schemas added (96)
- `AccountCategory1`
- `AccountCategory2`
- `AccountCategory3`
- `AccountStatus2`
- `AccountStatus3`
- `AccountType2`
- `AccountType3`
- `AccountsResponse`
- `AchPayment`
- `AchTransaction`
- `Actions1`
- `Address`
- `AssociatedMembers`
- `BeneficiaryBankDetailsDomestic`
- `BeneficiaryBankDetailsInternational`
- `BeneficiaryDetails`
- `CountryName`
- `CurrencyCode1`
- `CurrencyCode2`
- `CurrencyCode3`
- … and 76 more

### Schemas updated (22)
- `AccountEvent`
- `Balance`
- `BankAccount`
- `BankingActivity`
- `BusinessAddress`
- `BusinessContact`
- `BusinessUser`
- `ContactMethodResponse`
- `Customer`
- `EStatementRequest`
- `ErrorInfo4`
- `ErrorInfo5`
- `Filters`
- `ImageInfoType`
- `ImageView`
- `InstitutionDisclosureDataType`
- `InstitutionUser`
- `RegDLimits`
- `RegDLimits1`
- `Status`
- … and 2 more

- Documentation updates on 22 paths

All notable changes to the Candescent DI OpenAPI specification will be documented in this file.

## [1.3.1] - 2025-04-07

- Initial public release of the Candescent DI OpenAPI specification
