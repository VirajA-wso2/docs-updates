# Overview

## Introduction

To ensure the security and authenticity of your deployments, WSO2 provides signed container images. This section explains how to use the Cosign tool to verify that an image has not been tampered with and was officially released by WSO2.

## Prerequisites

Before verification, ensure:

* [Cosign](https://docs.sigstore.dev/cosign/system_config/installation/) is installed
* Access to the [WSO2 container registry](https://registry.wso2.com)
* Public key provided by WSO2

You need the WSO2 public key to validate the signatures. Save the following block into a file named **wso2-public-key.pub** on your local machine:

```
-----BEGIN PUBLIC KEY-----
MIIBIjANBgkqhkiG9w0BAQEFAAOCAQ8AMIIBCgKCAQEAw4rovhfVQqdUeXvtxxAl
3OKdNLNaUqiAlnb3zBxv7ITYCJXhXLByUk5wuKca6fr00d3NqwXoUeVARdrKMz5y
6a0QTLmM8CmD+l/ffGRqrNel23cdHkIi3wZFAJToHy+mFB6tYUoL6ieuEtLT+bFn
msBkucHBPp6ahicCVPfegiTWjSwBylnYSOPa9D/VmvQV13ROfuq1EgeejbCpepbc
9APj3pXjpFtOPWPBBYdofumqYj2sKR2y/V4yYl8mrEJon6SX3hBi5d0RXGNaFzdU
6D9rm4K6ZEEYX+l2uT+sHorTtI4e08KVOK7lU0VY4fiR+5Mh3FFKeLvF8KNMSYOZ
gQIDAQAB
-----END PUBLIC KEY-----
```


