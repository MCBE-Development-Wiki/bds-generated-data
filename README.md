# bds-generated-data

## Auto-Generation

Create a file named `test_config.json` under the BDS directory root and fill it with:

```json
{ "generate_documentation": true }
```

Execute `bedrock_server.exe` and you will find docs generated in the `docs` folder.

## Generate More Contents

Auto-generated docs are determined by world settings. Please check the following `level.dat` options to guarantee a complete generation.

- Check all experimental options on
- Check `baseGameVersion` is `*` to generate the newest contents
- Check `editorWorldType` is `1` for successfully generating `project` command
- Check `eduOffer` and `educationFeaturesEnabled `are `1`s to generate Education Edition featured contents
- To generate integrated edu contents, you need hook `DedicatedServer::isEduMode` to always return `true` (you can use [PreLoader](https://github.com/LiteLDev/PreLoader) to complete this)
