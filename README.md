# Simulation Template

This is a simulation template for ApiGear and its internal simulation framework.

The template generates a JS script from an API description with additional type information.

The script can be executed with the `apigear simulate run` command.

## Usage
To use this template, ensure you have the necessary API description files and create a solution file that references this template.

```yaml
# my.solution.yaml
schema: apigear.solution/1.0
targets:
  - name: BaseInstrumentCluster
    output: sim
    inputs:
      - bic.module.idl
    template: apigear-io/template-simulation
```

And then run the following command to generate the simulation script:

```bash
apigear generate solution my.solution.yaml
```


## Generated Output
The generated output will include a JavaScript file that contains the simulation logic for the specified API.

- In the api module you will find the data types and typescript data types. 
- A client (*client.js) will be generated to interact with an module connected via Object Link Protocol. 
- In the service (*.service.js) you will find the service implementation that can be used to simulate the API service. You would normally connect from a API client to this service.

