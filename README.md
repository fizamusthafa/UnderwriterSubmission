# UnderwriterSubmission

A Power Platform solution containing a Copilot Studio AI agent for automating underwriter submission workflows.

## Solution Contents

### `solution.zip`
The deployable Power Platform solution package. Import this file directly into your Power Platform environment.

### `solution/` Directory
The unpackaged solution files for version control:

- **`solution.xml`** — Solution manifest with metadata and component references
- **`customizations.xml`** — Bot/agent component definitions
- **`[Content_Types].xml`** — Package content type declarations
- **`BotComponents/cr_UnderwriterAgent/`** — Copilot Studio agent definition files
  - `UnderwriterAgent.dialog.yaml` — Main agent dialog configuration
  - `topics/SubmitNewRequest.yaml` — Topic for submitting new underwriting requests
  - `topics/CheckSubmissionStatus.yaml` — Topic for checking submission status
  - `topics/GetPolicyInfo.yaml` — Topic for retrieving policy information
  - `topics/Fallback.yaml` — Fallback topic for unrecognized intents

## Agent Capabilities

The **Underwriter Agent** (`cr_UnderwriterAgent`) supports the following capabilities:

| Topic | Description |
|---|---|
| Submit New Request | Guides users through submitting a new underwriting request, collecting policyholder details, policy type, coverage amount, and risk description |
| Check Submission Status | Allows users to track the status of an existing submission using a reference number |
| Get Policy Information | Provides information about underwriting guidelines, required documents, and available policy types |

## Importing the Solution

1. Navigate to [make.powerapps.com](https://make.powerapps.com)
2. Select your target environment
3. Go to **Solutions** in the left navigation
4. Click **Import solution**
5. Upload `solution.zip`
6. Follow the import wizard to complete the deployment

## Publishing the Agent

After importing:

1. Open the solution and find the **Underwriter Agent**
2. Click to open it in **Copilot Studio**
3. Review and customize topics as needed
4. Click **Publish** to make the agent available

## Solution Details

| Property | Value |
|---|---|
| Solution Name | UnderwriterSubmission |
| Unique Name | `UnderwriterSubmission` |
| Version | 1.0.0.0 |
| Publisher | Default Publisher |
| Customization Prefix | `cr` |
| Agent Schema Name | `cr_UnderwriterAgent` |
