# Changelog

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
