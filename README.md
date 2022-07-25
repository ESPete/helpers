# Helpers

This repository contains helper scripts and files to assist with the development and integration process of other ESPete libraries.

## Files

* `buildFlagsToString.yaml`
  This is a [ytt](https://carvel.dev/ytt/) overlay that converts an array format of `build_args` into a string.
  The array format is much more convenient for changing and updating dependencies, but `platformio.ini` requires it to be a string.

* `jsonToIni.jq`
  This is a jq module that converts a JSON file to an INI configuration file.
  Specifically, it's used in the process of turning the YAML based platformio.yaml file into an INI file.
  Surprisingly, there's no really good way to convert YAML to INI without building your own tool or script, but JSON to INI workse with this module.
