# Test WebSocket Endpoints Using the WebSocket Console

Choreo provides an integrated WebSocket Console to test publicly exposed WebSocket endpoints of Service components you create and deploy. The WebSocket Console allows you to connect to your service and interactively exchange messages. By default, Choreo secures WebSocket APIs with OAuth 2.0, and the console automatically generates test keys for authenticated API testing.

Follow these steps to test a WebSocket endpoint using the WebSocket Console:

1. **Sign in to the Choreo Console**  
   Go to the [Choreo Console](https://console.choreo.dev/) and log in.

2. **Select the Component**  
   In the **Component Listing** pane, click on the component you want to test.

3. **Open the WebSocket Console**  
   Click **Test** in the left navigation menu, then select **Console**. This opens the **WebSocket Console** pane.

4. **Choose the Environment**  
   In the **WebSocket Console** pane, select the desired environment from the drop-down list.

5. **Select the Endpoint**  
   Choose the endpoint you want to test from the **Endpoint** list.

    !!! note
        - The **Network Visibility** of an endpoint is configured in the **endpoints.yaml** file. You can set it to **Public**, **Organization**, or **Project**.
        - If the **Network Visibility** is set to **Public**, proceed to step 7.
        - If the **Network Visibility** is set to **Organization**, the endpoint won't be accessible outside the organization. For testing, Choreo allows you to generate a temporary URL that remains active for 15 minutes. Follow step 6 to generate the URL.

6. **Generate a Temporary URL (if applicable)**  
   If the **Network Visibility** is set to **Organization**, click **Generate URL** to create a temporary test URL valid for 15 minutes. Otherwise, skip this step.

    !!! note
        The temporary test URL is valid for **15 minutes** and will expire afterward. To manually deactivate it, click **Deactivate URL**.

    ![WebSocket Console](../assets/img/testing/websocket-console.png){.cInlineImage-full}

7. **Expand the Channel**  
   Expand the channel you want to test.

8. **Connect to the Endpoint**  
   Click **Connect** to establish a connection. The connection status will be displayed in the output logs.

9. **Send and Receive Messages**  
   Interact with the deployed service by sending and receiving messages.

    !!! note
        The maximum connection duration is **15 minutes**. After that, the connection terminates. To reconnect, click **Connect** again.