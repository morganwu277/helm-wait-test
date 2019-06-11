# QuickStart
1. prepare
```bash
kubectl create ns test
helm init --tiller-namespace test
helm install --namespace=test --name=test .
```
2. change `sleepSeconds` in values.yaml file
3. upgrade 
```bash
helm upgrade test .
```

# Introduction

This is a minimalistic test case to reproduce the following issues:

* https://github.com/kubernetes/helm/issues/3173
* https://github.com/kubernetes/helm/issues/3296

Where the `helm --wait` behaves differently than `kubectl rollout status deployment`

To run this test case:

* git clone https://github.com/paolomainardi/helm-wait-test
* kubectl create ns test
* helm init --tiller-namespace test
* helm upgrade --install test --wait --tiller-namespace test .



