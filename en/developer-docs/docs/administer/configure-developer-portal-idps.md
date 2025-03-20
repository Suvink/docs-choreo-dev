# Configure Identity Providers for Developer Portal

You can manage which Identity Providers (IdPs) are available for consumers to authenticate and generate API keys in the Developer Portal.

!!! Note -
    For organizations created after <date>, the Choreo Built-in Identity Provider is configured by default. Organizations created before this date allow all configured identity providers to be used in the Developer Portal. 

Follow these steps to configure Identity Providers:

1. Sign in to [Choreo](https://console.choreo.dev/).

2. In the Choreo Console, go to the top navigation menu and click **Organization**. Then select your organization. 

3. In the left navigation menu, click **Settings**. Under the **API Management** tab, go to **Developer Portal**.

4. In the **Identity Providers** section, specify which identity providers should be used for both the **Sandbox** and **Production** environments of the Developer Portal.

!!! Note -
    Any identity provider configured for the Developer Portal's **Production** environment must also be enabled in the Choreo **Production** environment.
