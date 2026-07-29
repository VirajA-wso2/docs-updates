# User Guide

Before running verification, make sure you have completed the steps in the [Overview](registry-image-verification-overview.md), including installing Cosign and saving the WSO2 public key.

## Verify Your Image

### Run the Verification Command

The command you run depends on whether you are logged in to the WSO2 container registry. Use the following command structure to verify your image. Replace `<image_path>` with the full registry path of the WSO2 image (e.g., `registry.wso2.com/wso2-am/am:v1.0.0`).

### A. If Already Logged In (Docker/OCI Client)

Verify the image directly:

```shell
cosign verify --key /path/to/wso2-public-key.pub <image_path>
```

### B. If Not Logged In

Pass credentials securely using environment variables:

1. Set credentials:

    ```shell
    export REGISTRY_USERNAME=<username>
    export REGISTRY_PASSWORD=<password>
    ```

2. Verify the image:

    ```shell
    cosign verify \
      --registry-username="$REGISTRY_USERNAME" \
      --registry-password="$REGISTRY_PASSWORD" \
      --key /path/to/wso2-public-key.pub \
      <image_path>
    ```

## Understanding the Results

When you run the command, a successful verification will display a message confirming that the **Cosign claims were validated** and the **signatures were verified** against the public key. If the verification fails, do not deploy the image and contact WSO2 support.

A successful verification confirms:

* Signature is valid
* Image digest matches signed content

![Registry Image Verification Preview](../assets/img/updates/registry-image-verification-preview.jpg)
