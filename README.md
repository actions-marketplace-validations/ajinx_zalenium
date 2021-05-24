![CI](https://github.com/ajinx/zalenium/workflows/CI/badge.svg)

# zalenium V1
Start Zalenium inside github actions workflow.

## Zalenium :
      A flexible and scalable container based Selenium Grid with video recording, live preview, basic auth & dashboard.
      
More documentation available at
      https://opensource.zalando.com/zalenium/
      

Action workflow example
```
on: [push]

jobs:
  tests:
    runs-on: ubuntu-latest
    name: <Any name> 
    steps:
    - uses: actions/checkout@v2
    - name: <e.g. Zalenium >
      uses: ajinx/zalenium@1.1
    - name: Run test
      env:
        SELENIUM_HUB_HOST: 'localhost'
      run: <Test execution command e.g. mvn test, npm test, ./gradlew test etc> 
 ```
In your test configuration, specify remote url as http://localhost:4444/wd/hub

This is still in BETA and might not work on Windows and MAC runners, Log any issues you noticed.

