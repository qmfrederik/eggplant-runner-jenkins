<img src="https://www.eggplantsoftware.com/hubfs/Branding/Keysight-Eggplant-Logo_RGB_full-color.svg" width="300px"/>

# Eggplant DAI Plugin for Jenkins

## Introduction

The [Eggplant DAI](https://www.eggplantsoftware.com/digital-automation-intelligence) Plugin for Jenkins launches DAI tests from within a Jenkins pipeline.  You can use it to continuously test your application using Eggplant's [model-based approach to testing](https://docs.eggplantsoftware.com/docs/dai-using-eggplant-dai/).  For more information about Eggplant, visit https://www.eggplantsoftware.com.

_This introduction should include a screenshot of a Jenkins pipline triggering a DAI run_.

## Installing and using the Eggplant DAI Plugin for Jenkins

_This section should contain a visual overview of how to enable the Eggplant plugin in Jenkins, with screenshots_

## Advanced Usage

The plugin can be used by executing it as follows in your `Jenkinsfile`:

```yaml
pipeline {
    agent any

    environment {
        DAI_CLIENT_SECRET = credentials('eggplant-runner-client-secret')
    }

    stages {
        stage('Eggplant Runner') {
            steps {
                eggplantRunner serverURL: 'https://edge.dai.webperfdev.com/', testConfigId: '307fee3e-9d6b-43e6-b31e-f1d379f27cdf'
            }
        }
    }
}
```

## License

This plug-in is licensed under the terms of the [MIT license](LICENSE.md)

## Contributing

You need to install the following dependencies if you want to contribute to the Eggplant DAI Runner for Jenkins:

1. You can download and install Java 11 from the [Eclipse Temurin website](https://adoptium.net/).
2. Download Maven from the [Apache Maven website](https://maven.apache.org/). Make sure to download one of the binary archives (with bin in their name).
3. To verify that Maven is installed, run the following command: `mvn -version`
4. You can use `launch.json` to run 'Debug (Attach)' to launch an local Jenkins instance for development.
