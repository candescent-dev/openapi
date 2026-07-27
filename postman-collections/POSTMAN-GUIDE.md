# Candescent API Postman Collections

The [Candescent OpenAPI repository](https://github.com/candescent-dev/openapi) publishes Postman collections for **external integrators** alongside the [Candescent DI API](https://docs.candescent.com/api/generated/candescent-di-api/) OpenAPI specification. Use these collections to explore, test, and validate Digital Banking API operations from [Postman](https://www.postman.com/) without writing custom HTTP clients first.

## What the Collections Provide

| Capability | Description |
|------------|-------------|
| **Ready-made requests** | Pre-built requests for each API area, aligned with the public OpenAPI spec |
| **Environment templates** | Per-collection environment files for Sandbox, Stage, and Production tiers |
| **Authentication flows** | OAuth V1/V2 folders that obtain and store `access_token` values automatically |
| **Test scripts** | Collection scripts that capture tokens and IDs from responses into environment variables |

Use the collections when you want to:

- Validate your Developer Console application credentials against live Stage endpoints for a target FI
- Walk through OAuth client-credentials or password-grant flows before wiring them into your partner application
- Exercise a specific API domain (Accounts, Transactions, Authentication, and others) in isolation
- Share reproducible API examples with your integration team across FI environments

## Repository Location

Collections and environments in this repository:

| Resource | Location |
|----------|----------|
| **OpenAPI spec** | [`documentation/candescent-di-api.yaml`](../../documentation/candescent-di-api.yaml) |
| **Postman Collections** | [`Postman Collections`](https://github.com/candescent-dev/openapi/tree/main/postman-collections) |
| **Public OpenAPI repo** | [github.com/candescent-dev/openapi](https://github.com/candescent-dev/openapi) |

## Collection Layout

All published collections live under `postman-collections/`. This is the partner-facing set of requests and environments for Marketplace Partners and other external integrators building solutions that connect to Candescent Digital Banking on behalf of financial institutions.

Within `postman-collections/`, folders follow **API category** names that match the Candescent DI API tag groups — for example `Authentication`, `Core Banking`, `Customer Management`, `Documents And Preferences`, and `MX`.

Postman collections are available for selected API areas today. Additional collections will be published in upcoming releases as they become ready for external integrators.

Each API category folder contains:

- A `*.postman_collection.json` file with requests and test scripts
- An `environment/` subfolder with tier-specific `*.postman_environment.json` files (`-sbx`, `-stg`, and `-prd` suffixes)

## Who Should Use the Collections

These instructions are for **external users only** — Marketplace Partners, fintechs, and other third-party developers integrating with Candescent on behalf of one or more financial institutions (FIs).

You should use the collections if you:

- Build a product or integration that multiple FIs can adopt
- Need to test API behavior per FI before go-live
- Want hands-on examples of partner-facing API paths and entitlements

Obtain environment variable values from each target FI and from your Developer Console application before running authenticated requests. Configure a separate Postman environment per FI when you test across institutions.

## Environments

Postman environment files name the Apigee tier in the filename. External integrators use **Sandbox**, **Stage**, and **Production**:

| Suffix | Tier | When to use |
|--------|------|-------------|
| `-sbx` | Sandbox | Early integration testing and exploration before Stage |
| `-stg` | Stage | Development, integration testing, and FI validation |
| `-prd` | Production | Production certification (restricted access) |

Start with **Sandbox** or **Stage** unless your integration PM directs you to Production.

## Related Resources

| Resource | Description |
|----------|-------------|
| [Candescent DI API](https://docs.candescent.com/api/generated/candescent-di-api/) | Full REST API reference |
| [Quick Start](https://docs.candescent.com/guides/getting-started/quickstart) | Obtain API credentials and your first access token |
| [Developer Console overview](https://docs.candescent.com/guides/Developer%20Console/overview) | Create applications and generate Shared Key / Secret Key |
| [Create OAuth Token (V2)](https://docs.candescent.com/api/generated/create-access-token-v-2/) | Token endpoint reference used by Authentication collections |

---

## Installation

Import Candescent **external** Postman collections and environments into your Postman workspace. No additional packages are required beyond the [Postman desktop or web app](https://www.postman.com/downloads/).

### Prerequisites

Before importing collections:

- A [Postman](https://www.postman.com/) account
- Access to the [Candescent Developer Console](https://console.candescent.com) with an application created for your partner integration
- **Shared Key** (`client_id`) and **Secret Key** (`client_secret`) for your application
- FI-provided values for institution, user, and customer identifiers required by your API area (see [Environment variables](#environment-variables) below)

### Get the Collection Files

Browse `postman-collections/` in this repository and download the `*.postman_collection.json` and `*.postman_environment.json` files you need, or import them directly from the repository in Postman.

Collections are grouped by API category under `postman-collections/`. Import the folders for the API areas your integration uses.

Common starting points:

| API area | Collection folder |
|----------|---------------------|
| Authentication | `postman-collections/Authentication/OAuth V2/` |
| Accounts | `postman-collections/Core Banking/Accounts/` |
| Transactions | `postman-collections/Core Banking/Transactions/` |

### Create or Select a Workspace

1. Open the [Postman desktop or web app](https://www.postman.com/downloads/) and sign in.
2. In the header, open the **Workspaces** switcher.
3. **Select** an existing workspace where you want to import the collections, **or create** a new one:
   1. Click **Create** (or **Create Workspace**).
   2. Enter a name (for example `Candescent API`).
   3. Select **Internal** as the workspace type (recommended for partner integration work).
   4. Choose **Blank workspace**.
   5. Set access to only you and invited people, or your team — as appropriate for your organization.
   6. Click **Create Workspace**.
4. Confirm the workspace is selected in the switcher, then continue to import your collection.

### Import a Collection

With your workspace selected:

1. Open the Import dialog by clicking **Import**, pressing **Ctrl+O** (Windows/Linux) or **⌘+O** (macOS), choosing **File → Import** in the desktop app, or dragging a collection file into Postman.
2. Select the `*.postman_collection.json` file for your API category (for example `OAuth V2.postman_collection.json` or `Accounts.postman_collection.json`).
3. Confirm the collection appears in your workspace sidebar.

Repeat for each API category you need to test.

### Import an Environment

Each collection folder includes an `environment/` subfolder with tier-specific files:

```
environment/
  apigee-accounts-sbx.postman_environment.json
  apigee-accounts-stg.postman_environment.json
  apigee-accounts-prd.postman_environment.json
```

1. Open the Import dialog by clicking **Import**, pressing **Ctrl+O** (Windows/Linux) or **⌘+O** (macOS), choosing **File → Import** in the desktop app, or dragging an environment file into Postman.
2. Select the environment file for your target tier (start with **`-sbx`** for Sandbox or **`-stg`** for Stage).
3. Open **Environments** in the Postman sidebar and select the imported environment.
4. Set it as the **active environment** (checkmark in the environment dropdown).

Import a matching environment for every collection you use. Environment variable names are aligned with the requests in that collection.

### Environment Variables

Each `*.postman_environment.json` file defines variables in a fixed order. Variables at the top of the list must be populated **before** you can obtain an `access_token`.

> **Important — FI-provided values**
>
> **All environment variables listed before `access_token` must be acquired from the financial institution (FI) associated with the application you are developing.**
>
> This includes gateway URLs, API credentials, institution identifiers, and test user or customer identifiers. Your FI integration contact or Candescent Integration PM provides these values for each environment (Sandbox, Stage, or Production). Do not guess or reuse values from another FI.

Typical variables that appear **before** `access_token`:

| Variable | Source |
|----------|--------|
| `apigee_base_url` | FI / Candescent — API gateway base URL for the target tier |
| `client_id` | Developer Console — Shared Key for your application |
| `client_secret` | Developer Console — Secret Key for your application |
| `authorized_client_id` | FI / Developer Console — when a separate authorized client is required |
| `authorized_client_secret` | FI / Developer Console — secret for the authorized client |
| `institution_id` | FI — institution identifier for your integration |
| `retail_user_host_user_id` | FI — test retail user identifier |
| `retail_user_login_id` | FI — test retail login |
| `retail_user_password` | FI — test retail password |
| `business_user_login_id` | FI — test business user login |
| `business_user_password` | FI — test business user password |
| `business_tin` | FI — test business TIN |
| `institution_customer_id` | FI — customer identifier for account-scoped requests |

Variables at or **after** `access_token` (such as `access_token`, `refresh_token`, and `authorization_code`) are typically populated automatically when you run the Authentication collection requests. You do not need to set them manually before your first token request.

### Set Initial Values in Postman

1. Select your imported environment.
2. Click **⋯** → **Edit**.
3. Enter FI-provided and Developer Console values for every variable that appears **before** `access_token` in the environment file.
4. Leave `access_token` blank until you run an Authentication request.
5. Save the environment.

> **Warning:** Never commit populated environment files with live secrets to version control. Use Postman's secret variable type for `client_secret` and passwords where supported.

### Verify the Import

After import:

1. Confirm the collection and environment names match (for example `Authentication - OAuth V2` with `apigee-oauthv2-sbx` or `apigee-oauthv2-stg`).
2. Open any request and verify `{{variable}}` placeholders resolve in the URL and headers panel.
3. Proceed to [Quick Start](#quick-start) to obtain an access token and send your first API call.

---

## Quick Start

Obtain an access token and call a Digital Banking API from Postman in a few minutes. This section is for **external integrators** and assumes you completed [Installation](#installation) and imported an **external** Authentication collection plus at least one API collection (for example **Accounts**).

### Before You Begin

Confirm your active Postman environment has values for every variable that appears **before** `access_token`:

> **Important — FI-provided values**
>
> **All environment variables listed before `access_token` must be acquired from the financial institution (FI) associated with the application you are developing.** Values include `apigee_base_url`, `client_id`, `client_secret`, `institution_id`, and any user or customer identifiers required by your collection.

See [Environment variables](#environment-variables) for the full list and sources.

### Step 1: Select Your Environment

1. In Postman, choose your imported **Sandbox** or **Stage** environment (filename suffix `-sbx` or `-stg`) from the environment dropdown.
2. Verify `client_id`, `client_secret`, `institution_id`, and `apigee_base_url` are set.

### Step 2: Obtain an Access Token

Open the **Authentication** collection you imported (for example **Authentication - OAuth V2**).

#### Client credentials (server-to-server)

For backend integrations that use the client-credentials grant:

1. Expand **Retail User** → **Access Token** → **Client Credential** (or the equivalent folder for your user type).
2. Select **1. Generate Access Token**.
3. Click **Send**.

On success, the collection test script stores the response `access_token` in your environment. Postman sets `{{access_token}}` for subsequent requests automatically.

#### Password grant (user-context testing)

If your FI provided test user credentials and your integration uses the password grant:

1. Ensure `retail_user_login_id`, `retail_user_password`, and related user variables are set from FI-provided values.
2. Run the **Password** token request in the Authentication collection.
3. Confirm `access_token` is populated in your environment after the response.

See [Create OAuth Token (V2)](https://docs.candescent.com/api/generated/create-access-token-v-2/) for grant types, headers, and request body fields.

### Step 3: Run an API Request

With `access_token` set, switch to an API collection — for example **Accounts**:

1. Open a read-only request such as **List Accounts**.
2. Confirm the request uses `Authorization: Bearer {{access_token}}` (or equivalent collection auth).
3. Verify required headers reference environment variables (`institutionId`, `transactionId`, and so on).
4. Click **Send**.

A `200` response with account data confirms your credentials, FI-provided variables, and token flow are configured correctly.

### Step 4: Run Requests in Order

Many collections are designed to run folders in sequence:

1. **Authentication** — obtain `access_token`
2. **Discovery or setup requests** — capture IDs (account, customer, and so on) into environment variables
3. **API operations under test** — use captured IDs in path or query parameters

Check the collection folder names and request descriptions for the recommended order. Scripts in earlier requests often set variables used by later ones.

### Example: OAuth V2 Client Credentials Flow

When you send **Generate Access Token**:

1. Postman sends `POST {{apigee_base_url}}/oauth2/v1/token` with `grant_type=client_credentials`.
2. Basic authentication uses `{{client_id}}` and `{{client_secret}}`.
3. Headers include `institutionId: {{institution_id}}` and a generated `transactionId`.
4. The test script runs: `pm.environment.set("access_token", jsonData.access_token)`.
5. Downstream requests in any imported collection can reference `{{access_token}}`.

### Environment URLs

Your FI provides the `apigee_base_url` for each target tier. External collections use the partner-facing gateway path for that institution — do not assume the same base URL across FIs.

| Tier | Typical use |
|------|-------------|
| Sandbox (`-sbx`) | Early partner integration and exploration |
| Stage (`-stg`) | Partner integration and validation testing |
| Production (`-prd`) | Production certification (restricted access) |

Set `apigee_base_url` in your Postman environment to the value your FI supplies for the tier you are testing.

---

## Troubleshooting

Common issues when importing and running **external** Candescent Postman collections.

### Environment Variables

#### `access_token` is empty

**Symptom:** API requests fail with `401 Unauthorized` and `{{access_token}}` is blank in the environment.

**What to check:**

1. Run an **Authentication** collection token request first (for example **Generate Access Token**).
2. Confirm the token request returned `200` and a JSON body with `access_token`.
3. Open the Postman **Console** (View → Show Postman Console) and verify the test script ran without errors.
4. Ensure every variable **before** `access_token` is set — missing `client_id`, `client_secret`, or `institution_id` causes token requests to fail silently or return errors.

> **Important:** All environment variables listed before `access_token` must come from the FI associated with your application. Incorrect or placeholder values prevent token generation.

#### Unresolved `{{variable}}` in requests

**Symptom:** Postman shows red unresolved variables in the URL or headers.

**What to check:**

1. The correct environment is **active** (selected in the environment dropdown).
2. The variable name in the request matches the environment file exactly (case-sensitive).
3. For IDs captured from earlier requests, run prerequisite requests in the collection folder order.

#### Wrong institution or user context

**Symptom:** `403 Forbidden` or empty data sets despite a valid token.

**What to check:**

1. `institution_id` matches the FI environment you are testing against.
2. User identifiers (`retail_user_host_user_id`, `institution_customer_id`, and similar) belong to the same FI and test entitlements as your Developer Console application.
3. Your application has the API endpoints enabled in the Developer Console for the operations you are calling.

### Authentication

#### `401` on token request

| Cause | Resolution |
|-------|------------|
| Invalid `client_id` / `client_secret` | Regenerate keys in the [Developer Console](https://docs.candescent.com/guides/Developer%20Console/managing-applications-and-api-credentials) and update the environment |
| Wrong `apigee_base_url` | Confirm the base URL with your FI for the target tier |
| Missing `institutionId` header value | Set `institution_id` in the environment |
| Expired token on API calls | Re-run the Authentication token request; tokens expire (typically within ~24 hours) |

#### Password grant folders fail

Password-grant requests require FI-provided test user credentials. If you do not have `retail_user_password` or `business_user_password` values, use **client credentials** flows instead or request test users from your FI integration contact.

### Collection and Import Issues

#### Collection does not match environment

**Symptom:** Variables are missing or requests reference wrong paths.

**Resolution:** Import the environment file from the **same** API category folder under `postman-collections/` as the collection (for example both from `postman-collections/Core Banking/Accounts/`). Do not mix an Accounts collection with an OAuth V2 environment file.

#### Wrong base URL or tier

**Symptom:** Requests hit unexpected hosts or return routing errors.

**Resolution:** External collections use FI-specific `apigee_base_url` values. Confirm the base URL and tier (`-sbx`, `-stg`, or `-prd`) with your FI integration contact or Candescent Integration PM for each institution you test against.

### Request Failures

#### Missing `transactionId`

Most Candescent APIs require a `transactionId` header (UUID). Collections usually set this with `{{$guid}}` in the request headers. If you author custom requests, add a unique UUID per call.

#### `400 Bad Request`

Review required query parameters and headers in the [API reference](https://docs.candescent.com/api/generated/candescent-di-api/) for the operation. Collection requests mirror the OpenAPI contract — compare your active environment IDs with the parameters the operation expects.

### Getting Help

| Resource | When to use |
|----------|-------------|
| [Candescent DI API](https://docs.candescent.com/api/generated/candescent-di-api/) | Request parameters, headers, and response schemas |
| [Developer Console troubleshooting](https://docs.candescent.com/guides/Developer%20Console/troubleshooting-and-support) | Console access and credential issues |
| FI integration contact / Candescent Integration PM | FI-specific URLs, test users, and institution identifiers |
| [Quick Start](#quick-start) | Step-by-step token and first-request walkthrough |
