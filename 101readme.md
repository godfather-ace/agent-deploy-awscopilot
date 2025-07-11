## Environment Creation
python3 -m venv env
source env/bin/activate

## Library Installation
pip install -r requirements.txt

## App Creation
langchain app new .

## Poetry Setup
poetry add langchain-core langgraph langchain langchain-aws langchain-community langchain-pinecone boto3 langchain-cli pydantic@">=2,<3"

go to pyproject.toml and update --> python = ">=3.13,<3.14"

## Update the poetry configuration
poetry update

## Add the packages through poetry in pyproject.toml
poetry add langchain-core langgraph langchain langchain-aws langchain-community langchain-pinecone boto3 langchain-cli pydantic@">=2,<3"

## Check again
poetry add langchain-core langgraph langchain langchain-aws langchain-community langchain-pinecone boto3 langchain-cli pydantic@">=2,<3"

## launch the deployed app
langchain serve

## AWS Copilot - Install AWS Copilot (using Homebrew in MAC) 
### Make sure to put aws credentials and put Access Key and Secret Key using aws credentials
copilot init \
--app ai-agent \
--name ai-agent \
--type 'Load Balanced Web Service' \
--dockerfile './Dockerfile' 

copilot deploy

copilot app delete