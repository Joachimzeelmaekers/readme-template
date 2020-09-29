
# Project title and information - template

Here we give an overview in a couple of sentences on what this service or application does. Simple for the information of the developers. Below this, we add a link to the Confluence page that is linked to this project. 

**Confluence:** [project information](link-to-confluence)

## Getting Started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes. See deployment for notes on how to deploy the project on a live system.

### Prerequisites

What things you need to install the software and how to install them by listing the technologies.

- Virtual environment of choice (anaconda, venv, ...)
- Python 3.6
- pip

optional:

- gcloud
- kubectl

### Installing

A step by step series of examples that tell you how to get a development environment running.

#### 1. Install requirements

```
pip install -r requirements.txt
```

#### 2. Set the environment variables

****required**

| Environment Variable | Default | Explanation |
| -------------------- | ------- | ----------- |
| REDIS_IP             | localhost | Connection to the redis. For the default to work use kubectl port-forwarding or run redis locally
| CLIENT_ID**          | | Office 365 client id.
| CLIENT_SECRET**      | | Office 365 client secret
| LOG_LEVEL            | debug   | Can be one of the following: CRITICAL, FATAL, ERROR, WARN, WARNING, INFO, DEBUG, NOTSET
| SCOPES               | message_all | The scope of the mail listener. For normal mailboxes is it the default value. for shared mailboxes is this `SCOPES=message_all_shared`
| SHARED_MAILBOX       | me      | Which mailbox is used. me for normal mailboxes. The email address for shared mailboxes.

All the values for the environment variables can be found at X (link).
If you don't have access please ask the Technical Lead according to the Confluence page. 

#### 3. Run the application

In this section we list all steps of local development.
```
python -m outlook_service
```

## Run the tests

You can run the test by running pytest:

```bash
pytest
```

## Deployment

This project has CI with bitbucket pipelines. When pushing to master branch (customize if needed) it will be build 
and deployed automatically.
