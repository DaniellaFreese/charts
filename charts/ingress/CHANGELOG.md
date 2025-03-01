# Changelog

## 0.8.0

### Improvements

- Controller Pods now include annotations to exempt the gateway admin API port
  from Kuma and Istio mesh interception. Controller to admin API configuration
  uses its own mTLS configuration, which is not compatible with mesh mTLS.
  [#913](https://github.com/Kong/charts/pull/913)
- Allow using templates (via `tpl`) when specifying `controller.proxy.nameOverride`.
  [#915](https://github.com/Kong/charts/pull/915)
- Bumped dependency `kong/kong` to `2.30.0`.
  [#915](https://github.com/Kong/charts/pull/915)

## 0.7.0

- Bumped dependency `kong/kong` minimum to `2.28.1`. Review the [kong chart
  changelog](https://github.com/Kong/charts/blob/main/charts/kong/CHANGELOG.md#2281)
  for details.

## 0.6.0

### Improvements

- Bumped dependency `kong/kong` to `2.26.2`.
  [#862](https://github.com/Kong/charts/pull/862)

## 0.5.0

### Breaking changes

The new `kong/kong` chart requires manual changes to values.yaml if using this
chart with controller versions <=2.10 and Kong versions >=3.3. See the 
[the kong/kong 2.26 upgrade instructions](https://github.com/Kong/charts/blob/main/charts/kong/UPGRADE.md#2260)
for details.

### Improvements

- Bumped dependencies on `kong/kong` chart to `>=2.26.0`.
  [#855](https://github.com/Kong/charts/pull/855)

## 0.4.0

### Improvements

- Generate the `adminApiService.name` value from `.Release.Name` rather than
  hardcoding to `kong`
  [#840](https://github.com/Kong/charts/pull/840)

## 0.3.0

### Fixes

- Changed default `gateway.admin` service from `NodePort` to headless `ClusterIP`
  which is expected for Gateway Discovery to work.
  [#835](https://github.com/Kong/charts/pull/835)

## 0.2.0

### Improvements

- Bumped dependencies on `kong/kong` chart to `>=2.23.0`.
  [#817](https://github.com/Kong/charts/pull/817)

## 0.1.0

### Improvements

- Created opinionated KIC + Gateway Discovery chart with predefined `values.yaml`
  [#806](https://github.com/Kong/charts/pull/806)
