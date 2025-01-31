# Develop an integration with Integration Studio

Choreo simplifies the process of building, deploying, and managing integration components, making it easy to expose integrations as APIs. This guide walks you through the steps to expose an integration created in WSO2 Integration Studio as an API in Choreo.

In this guide, you will:
- Create a component to expose a sample integration from the [Choreo samples repository](https://github.com/wso2/choreo-samples) as an API.
- Deploy, test, and observe the integration component.
- Publish the integration component as an API to the Choreo Developer Portal.

!!! note
    - To develop integrations for **Manual Task** and **Schedule Task** components in Choreo, use the **automation mode** in the WSO2 Micro Integrator. See [Running MI in Automation Mode](https://apim.docs.wso2.com/en/4.2.0/install-and-setup/install/running-the-mi-in-automation-mode/).
    - For other component types (Service, webhook, event-handler, etc.), use the **server mode**.

## Prerequisites

Before starting, complete the following:

1. **Create an Organization** (if you're new to Choreo):
    - Go to [https://console.choreo.dev/](https://console.choreo.dev/) and sign in.
    - Enter a unique organization name (e.g., `Stark Industries`).
    - Read and accept the privacy policy and terms of use.
    - Click **Create**. This creates the organization and opens the **Project Home** page.

2. **Fork the Choreo Samples Repository**:
    - Fork the [Choreo samples repository](https://github.com/wso2/choreo-samples), which contains the sample integration for this guide.

## Step 1: Create the integration component

1. **Sign in to Choreo Console**:
   Go to [https://console.choreo.dev/](https://console.choreo.dev/) and sign in. This opens the **Project Home** page.

2. **Create a New Component**:
   - If you already have components in your project, click **+ Create**.
   - Click the **Service** card.

3. **Enter Component Details**:
   Provide a unique name and description for the component:

    | **Field**          | **Value**              |
    |--------------------|------------------------|
    | **Component Name** | `Hello World`          |
    | **Description**    | `Hello World REST API` |

4. **Connect to GitHub**:
   - Go to the **GitHub** tab.
   - Click **Authorize with GitHub** to connect your GitHub account. If you haven't connected your GitHub repository to Choreo, enter your GitHub credentials and select the repository you forked in the prerequisites section to install the [Choreo GitHub App](https://github.com/marketplace/choreo-apps).

    !!! note
        The **Choreo GitHub App** requires the following permissions:
        - Read and write access to code and pull requests.
        - Read access to issues and metadata.
        
        You can [revoke access](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/reviewing-your-authorized-integrations#reviewing-your-authorized-github-apps) if needed. Write access is only used for sending pull requests; Choreo will not push changes directly to your repository.

5. **Provide Repository Details**:
   Enter the following information:

    | **Field**             | **Description**              |
    |-----------------------|----------------------------- |
    | **Organization**      | Your GitHub account          |
    | **Repository**        | `choreo-samples`            |
    | **Branch**            | **`main`**                   |
    | **Buildpack**         | **WSO2 MI** (since you're creating the REST API from a [WSO2 Integration Studio](https://wso2.com/micro-integrator/) project) |
    | **Project Directory** | `hello-world-mi`             |

6. **Create the Component**:
   Click **Create**. Choreo initializes the component with the sample integration.

## Step 2: Deploy the integration component

1. **Navigate to Deploy**:
   In the Choreo Console left navigation menu, click **Deploy**.

2. **Configure and Deploy**:
   - In the **Build Area** card, click **Configure & Deploy**.
   - In the **Configurations** pane, click **Next**. This displays the endpoint details ready for deployment.
   - Click **Deploy**. This deploys the integration component to the development environment.

    !!! tip
        - Choreo uses [endpoints](../../choreo-concepts/endpoint.md) to expose **Service** components to the network. Learn more about configuring endpoints in [Configure Endpoints](../configure-endpoints.md).
        - Automatic deployment is enabled by default, so only the first deployment needs to be done manually.

3. **Verify Deployment**:
   The **Development** card shows the **Deployment Status** as **Active** when the integration is successfully deployed.

## Step 3: Test the integration

1. **Open the OpenAPI Console**:
   - In the Choreo Console left navigation menu, click **Test** and then click **Console**.
   - In the OpenAPI Console, select **Development** from the environment drop-down list.

2. **Test the Endpoint**:
   - Expand the **GET /integration** operation.
   - Click **Try it out**, then click **Execute**. This sends a request to your deployed integration.

3. **Check the Response**:
   - In the **Response body** section, observe the response. If the integration works as expected, you should see:
     ```json
     {"Hello" : "Integration"}
     ```

## Step 4: Observe the integration

1. **Navigate to Observability**:
   Click **Observability** in the left navigation menu to monitor the performance of the integration component.

2. **View Metrics**:
   - Observe throughput and latencies of requests over time.
   - View logs generated during a specific period.
   - Analyze the flame graph (Diagnostics View) for performance insights.

   For more details, see [Observability Overview](../../monitoring-and-insights/observability-overview.md).

## Step 5: Publish the integration component

1. **Navigate to Lifecycle Management**:
   - In the Choreo Console left navigation menu, click **Manage** and then click **Lifecycle**.
   - The **Lifecycle Management** pane shows the current lifecycle stage as **Created**.

2. **Publish the API**:
   - Click **Publish**. This changes the lifecycle stage to **Published** and exposes the integration as an API in the Choreo Developer Portal.
   - To view the published API, click **Go to Devportal**. In the Developer Portal, you can manage subscriptions and generate access tokens for testing.

Now you have successfully exposed an integration designed in WSO2 Integration Studio as a REST API in Choreo!