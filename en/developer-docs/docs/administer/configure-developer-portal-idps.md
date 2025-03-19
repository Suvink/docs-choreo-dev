# Configure Identity Providers for Developer Portal

You can manage which Identity Providers (IdPs) are available for consumers to authenticate and generate API keys in the Developer Portal.

!!! Note -
    For organizations created after <date>, the Choreo Built-in Identity Provider is configured by default. Organizations created before this date allow all configured Identity Providers to be used in the Developer Portal. 

Follow these steps to configure Identity Providers:

1. Navigate to the Choreo Console at [https://console.choreo.dev/](https://console.choreo.dev/) and sign in using your Google, GitHub, or Microsoft account.

2. Select your organization from the **Organization** dropdown in the Choreo Console header.

3. From the left navigation menu, select **API Management** > **Developer Portal**.

4. In the **Identity Providers** section, specify which Identity Providers are allowed for both the **Sandbox** and **Production** environments of the Developer Portal.

!!! Note -
    Any Identity Provider configured for the Developer Portal's **Production** environment must also be enabled in the Choreo **Production** environment.
