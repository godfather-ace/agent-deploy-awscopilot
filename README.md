### Environment Creation
```
python3 -m venv env
source env/bin/activate
```

### Library Installation
```
pip install -r requirements.txt
```

### App Creation
```
langchain app new .
```

### Poetry Setup
```
poetry add langchain-core langgraph langchain langchain-aws langchain-community langchain-pinecone boto3 langchain-cli pydantic@">=2,<3"
```
go to pyproject.toml and update --> python = ">=3.13,<3.14"

### Update the poetry configuration
```
poetry update
```

### Add the packages through poetry in pyproject.toml
```
poetry add langchain-core langgraph langchain langchain-aws langchain-community langchain-pinecone boto3 langchain-cli pydantic@">=2,<3"
```

### Check again
```
poetry add langchain-core langgraph langchain langchain-aws langchain-community langchain-pinecone boto3 langchain-cli pydantic@">=2,<3"
```

### Launch the deployed app
```
langchain serve
```

### AWS Copilot - Install AWS Copilot (using Homebrew in MAC) 
- Make sure to put aws credentials and put Access Key and Secret Key using aws credentials
- Use an IAM user (with full access or assume role) as AWS Copilot doesn't works for root user.
```
copilot init \
--app ai-agent \
--name ai-agent \
--type 'Load Balanced Web Service' \
--dockerfile './Dockerfile'
```

### Deploy the app
```
copilot deploy
```

## Delete the app and used AWS infra resources
```
copilot app delete
```

### References
- https://aws.amazon.com/containers/copilot/
- https://aws.github.io/copilot-cli/
- https://ai.gopubby.com/how-i-built-deployed-an-ai-agent-with-langgraph-langserve-aws-54c4eb04c640

