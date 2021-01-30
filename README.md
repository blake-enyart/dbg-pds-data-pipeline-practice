
# Welcome to your CDK Python project!

You should explore the contents of this project. It demonstrates a CDK app with an instance of a stack (`restful_api_gateway_stack`)
which contains a RESTful API consisting of AWS API Gateway linked to AWS Lambda. This system is completely self-documenting via FastAPI and all of this is Dockerized for deployment.

This API was developed based on the following 2 part series:
* [FastAPI + AWS = robust API (Part 1)](https://towardsdatascience.com/fastapi-aws-robust-api-part-1-f67ae47390f9)
* [FastAPI + AWS = secure API (Part 2)](https://towardsdatascience.com/fastapi-aws-secure-api-part-2-1123bff28b55)

The `cdk.json` file tells the CDK Toolkit how to execute your app.

This project is set up like a standard Python project.  The initialization process also creates
a virtualenv within this project, stored under the .venv directory.  To create the virtualenv
it assumes that there is a `python3` executable in your path with access to the `venv` package.
If for any reason the automatic creation of the virtualenv fails, you can create the virtualenv
manually once the init process completes.

To manually create a virtualenv on MacOS and Linux:

```
$ python3 -m venv .venv
```

After the init process completes and the virtualenv is created, you can use the following
step to activate your virtualenv.

```
$ source .venv/bin/activate
```

If you are a Windows platform, you would activate the virtualenv like this:

```
% .venv\Scripts\activate.bat
```

Once the virtualenv is activated, you can install the required dependencies.

```
$ poetry install
```

At this point you can now synthesize the CloudFormation template for this code.

```
$ cdk synth
```

For local testing, you must be in the api directory and you can run:

```
$ uvicorn main:app --reload 
```
This allows for rapid prototyping while in development on the local machine.

You can now begin exploring the source code, contained in the api directory.
There is also a very trivial test included that can be run like this:

```
$ pytest
```

To add additional dependencies, for example other CDK libraries, just run `poetry add <library>`
command.

When you are ready to deploy the application, ensure your `tasks.py` is configured appropriately and run:

```
$ inv deploy
```

That's it! You are done and now have a fully functioning RESTful API that is completely self-documenting. Amazing!!!

## Useful commands

 * `inv ls`          list all stacks in the app
 * `inv synth`       emits the synthesized CloudFormation template
 * `inv deploy`      deploy this stack to your default AWS account/region
 * `inv diff`        compare deployed stack with current state
 * `cdk docs`        open CDK documentation

Enjoy!
