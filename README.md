# Cloud Agent Repository

## Overview

This repository contains an Agent capable of performing operations to assist with various cloud provider CLI task. The agent is configured to interact with users, providing expert guidance and executing tasks as instructed.

## Pre-reqs

You will need an OpenAI API key, and the AWS, Azure, and Google Cloud CLIs installed on your system.

- [OpenAI API Key](https://platform.openai.com/signup)
- [AWS CLI](https://docs.aws.amazon.com/cli/latest/userguide/install-cliv2.html)
- [Azure CLI](https://docs.microsoft.com/en-us/cli/azure/install-azure-cli)
- [Google Cloud CLI](https://cloud.google.com/sdk/docs/install)

## Authentication

The agent can perform some login operations for you, but in order to do so, you will need to already have accounts on each of the providers.

Current supported auth methods:

- AWS: `aws sso login` with profiles setup in the aws config.
- Azure: `az login` with profiles setup in the azure config.
- Google Cloud: `gcloud auth login` with profiles setup in the gcloud config.

The agent can run the login commands if you are running on your local machine. The web browser will open and you will need to authenticate with the provider.

You can also run the login commands manually if you prefer, or if you set env variables/configurations the CLIs will pick up on their own it should just work.

## Usage

To run the agent, you need gptscript installed. You can run:

```bash
gptscript github.com/cloudnautique/cloud-agent
```
