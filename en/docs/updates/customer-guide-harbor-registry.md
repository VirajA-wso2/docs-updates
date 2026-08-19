# Overview

This guide provides instructions on how to access WSO2 products container images using the [WSO2 Container Registry](https://registry.wso2.com).

There are two primary ways to interact with the WSO2 container registry:

1. **Web Portal**: For browsing images, viewing tags using your WSO2 login.
2. **Command Line Interface (CLI)**: For pulling images in Docker, Kubernetes, or CI/CD pipelines using User or Service Tokens generated in WSO2 support portal.

## Image Retention Policy

To manage registry storage efficiently, older container images are periodically removed from the WSO2 Container Registry. The following retention rules apply to all projects:

* Images pushed within the last **6 months** are retained.
* The **latest image tag** in each repository is always retained, regardless of its age.

These rules ensure that repositories which have not been updated for more than 6 months still retain their latest image, preventing removal of images that may still be required.

!!! Important "Mirror Images to your own container registry"
     Older image tags are removed periodically, WSO2 recommends copying the images you use to your own container registry after pulling them, rather than relying on a tag remaining available in the WSO2 Container Registry. Maintaining your own copy guarantees that the exact image your deployments depend on remains available for redeployments, rollbacks, and scaling, regardless of the retention schedule.