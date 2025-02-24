# Integrate Unit Tests into the Build Pipeline

Choreo supports integrating unit tests into the build pipeline, allowing you to validate code before deployment. This ensures early testing of code changes, reducing the risk of defects in production.

!!! note
        Currently, Choreo supports unit tests only for the `WSO2 MI` buildpack.

## How it works

### Write tests

You can create unit tests in your source code using standard testing libraries. For step-by-step instructions on creating unit tests for WSO2 Micro Integrator projects, see [Creating a Unit Test Suite](https://mi.docs.wso2.com/en/latest/develop/creating-unit-test-suite/).

### Enable unit testing
1. Navigate to the **Build** page of your component in Choreo.
2. Enable **Unit Test** to activate it in the build pipeline.
3. **Save** the changes.
4. Trigger a new build.

### View test results

If unit testing fails, Choreo allows you to view logs. Click **View Details** of the failed build, then click the failed **Unit Test** step to view logs.

## Explore a sample

To get started, try out the [WSO2 MI helloworld](https://github.com/wso2/choreo-samples/tree/main/hello-world-java-task) sample. 


