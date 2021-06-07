# zwavejs2mqtt plugin for prometheus metrics

Prometheus metrics exported for [zwavejs2mqtt](https://github.com/zwave-js/zwavejs2mqtt).

Currently zwavejs2mqtt have one bug preventing this plugin to work.
Express app is exposed to plugins configured to handle 404 errors.
You will need small [patch](./app.patch) to fix this currently.

Metrics will be exposed at `http://you-zwavejs2mqtt-instance/metrics`.

Boolean metrics are exposed as 0/1 values.

List metrics are exposed as [StateSet](https://github.com/OpenObservability/OpenMetrics/blob/main/specification/OpenMetrics.md#StateSet).
The only difference is that each state has it's own value.
