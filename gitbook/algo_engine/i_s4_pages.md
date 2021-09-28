### Algo invocation

Locate the API **invocationAlgorithm**

![algo_invoke](imgs/algo_invoke.png "")

Define Algo Name and Parameters

![algo_invoke_config](imgs/algo_invoke_config.png "")

Below 2 samples bodies

```json
{
"dataframe": "",
"input": "{\"partner.code\":\"demo_general\",\"start_date\":\"2018-01-01\",\"end_date\":\"2019-12-31\", \"group\":\"fluid\"}",
"technical_name": "LoamicsDemoAlgo"
}
```

or

```json
{
"dataframe": "",
"input": "{\"partner.code\":\"demo_general\",\"start_date\":\"2018-01-01\",\"end_date\":\"2019-12-31\", \"group\":\"delivery_point\"}",
"technical_name": "LoamicsDemoAlgo"
}
```

Get your Algo Result with an HTTP Code 200 JSON formated

![algo_invoke_out](imgs/algo_invoke_out.png "")

***/!\ Of course you can call and execute algo from where and what you want - Algo Engine, PostMan or your own apps - from the moment your Public IP is declared and authorized***