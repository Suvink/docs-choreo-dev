# Unit Testing in Choreo Build Pipeline

Choreo supports unit testing as part of the build pipeline, enabling users to validate their applications before deployment. This feature ensures that code changes are tested early, reducing the risk of defects in production.

!!! note
        Currently, Choreo only supports unit testing for the `WSO2 MI` buildpack.

## How It Works

### Develop tests

In your source code, develop unit tests using standard testing libraries. For example, unit tests can be developed for a WSO2 MI project by following this [documentation](https://mi.docs.wso2.com/en/latest/develop/creating-unit-test-suite/).

### Enable Unit Testing
1. Navigate to the **Build** page of your component in Choreo.
2. Enable **Unit Test** to activate it in the build pipeline.
3. **Save** the changes.
4. Trigger a new build.

### View Test Results

If unit testing fails, Choreo allows you to view logs. Click **View Details** of the failed build, then click the failed **Unit Test** step to view logs.

## Get Started

To get started, try out the [WSO2 MI helloworld](https://github.com/wso2/choreo-samples/tree/main/hello-world-java-task) sample. 


