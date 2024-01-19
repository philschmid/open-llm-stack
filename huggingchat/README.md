# Use Case: Hugging Chat - [Environment: AWS/On-Premise]

This README provides guidance on setting up and running the Hugging Chat application within the Open LLM Stack, specifically tailored for AWS & On-Premise environments.   Hugging Chat is an open ChatGPT alternative using open source technologies. With Hugging Chat, you can create your own chatbot and deploy it on your own server.  

## Stack components

* [HuggingChat UI](https://github.com/huggingface/chat-ui): UI for the chatbot
* [Text Generation Inferece](https://github.com/huggingface/text-generation-inference): Used to serve the chatbot
* [MongoDB](https://github.com/mongodb/mongo) _optional: MongoDB Atlas_: Database for storing chat history

## Configuration

Default Stacks are configured via [helm charts](https://helm.sh/). Adjust the values in the [values.yaml](helm/values.yaml) file to suit the [On-Premise/AWS/etc.] environment.

Available Values:

* `MONGODB_URL`: URL to MongoDB instance or MongoDB Atlas. Default: `mongodb://localhost:27017`
* `MODELS`: List of model configurations to use. See [.env.example](.env.example) for an example

**Addvance Configuration:**

* Hugging Chat supports more advance features including OpenID Connect, Web Search or Theming. Please refer to the [Hugging Chat Documentation](https://github.com/huggingface/chat-ui?tab=readme-ov-file#extra-parameters) for more information.
* Use MongoDB Atlas for a managed MongoDB instance. See [MongoDB Atlas](https://www.mongodb.com/cloud/atlas) for more information.

## Deployment & Development

This stack currently can be deployed on AWS or On-Premise.  

### AWS

Deployment to AWS is done via [AWS CDK](https://aws.amazon.com/cdk/). The stack will be deployed as EKS cluster with a self-managed MongoDB instance. After the infrastructure is deployed, the application will be deployed via helm charts.

### On-Premise

Deployment to On-Premise is done via Helm Charts.  

## Additional Notes

* [Any specific notes or warnings pertinent to this environment or use case.]
