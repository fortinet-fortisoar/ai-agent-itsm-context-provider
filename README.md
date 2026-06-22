# Release Information

- **Version**: 1.0.0

- **Certified**: Yes

- **Publisher**: Fortinet

- **Scope**: Context and Enrichment, Triage

- **Verified with Models**: Fortinet FortiAI (AI model Medium)

# ITSM Context Provider

Finds related tickets and incidents by correlating investigations and alerts with investigation ID, alert ID, and key entities such as hosts, users, and IPs.

## Installation

This agent installs along with the FortiAI solution pack.

## Configuration

**Required MCP Servers**: SOC Framework

> [!Note]
>
> Refer to [Configuring MCP Servers](https://docs.fortinet.com/document/fortisoar/8.0.0/administration-guide/823139/mcp-servers#Configure_MCP_Servers) on FortiSOAR platform documentation for information on configuring a custom MCP server.
> 

### Prerequisites

- The FortiAI solution pack must be installed and configured with the Fortinet FortiAI connector.

  - To configure the FortiAI solution pack, refer to the [FortiAI](https://github.com/fortinet-fortisoar/solution-pack-fortinet-advisor/) solution pack documentation.
  - To configure the Fortinet FortiAI connector, refer to the [Fortinet FortiAI](https://docs.fortinet.com/fortisoar/connectors/fortinet-fortiai) connector documentation.

> [!Note]
>
> FortiAI solution pack and Fortinet FortiAI connector are preconfigured out-of-the-box with FortiSOAR `v8.0.0`.
> 


## Input Parameters

The input must be provided as a JSON object.

| Parameter          | Description                                                                      |
|--------------------|----------------------------------------------------------------------------------|
| `question`         | The question that needs to be answered                                           |
| `entities`       | Array of investigation hypotheses requiring validation and evidence correlation. |
| `time_window_days` | Number of past days to constrain the ticket search scope                         |


## Response

The output is returned as a JSON object.

| Parameter    | Description                                                     |
|--------------|-----------------------------------------------------------------|
| `answer`     | Answer to the query derived from available data.                |
| `confidence` | Confidence percentage indicating reliability of the answer.     |
| `evidence`   | Supporting information and details from retrieved data sources. |

