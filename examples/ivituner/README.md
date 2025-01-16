# Ivituner Simulation

Fir generate the simulation code fome the API description in ivi.tuner.idl, run the following command:

```bash
apigear generate solution ivi.tuner.idl
```

The simulation code is generated in the `./simulation` folder

Now we need to run the apigear server with the simulation service:

```bash
apigear serve
```

Now we can start the generated simulation script:

```bash
apigear simulate run simulation/ivi.tuner.script.js
```

If the script has a main function, it will run automatically.

Other functions can be called from the command line:

```bash
apigear simulate call demo1
```

The code in the "gen" folder is auto-generated and will be updated if the API description changes. The module `script.js` file will not be updated, as it may container user code.