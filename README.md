# MCP Server Demo with Arista CloudVision

> [!WARNING]
> Please note that this is not officially supported by Arista.
>
> You might not want to do this in your production environment as it is not using a local LLM.
>


Kudos to [@noredistribution](https://github.com/noredistribution). This demo is almost entirely built on their work with few small modifications to make it work for me.

Any API call can be added very easy with the `@mcp.tool()` decorator.

To learn more about MCP please visit [https://modelcontextprotocol.io/introduction](https://modelcontextprotocol.io/introduction).

## Example usage

1\. Create a .env file like the following and place it in this directory.

```bash
CVPTOKEN="Insert CloudVision Service account token here"
CVP="www.arista.io"
```

2\. Crate the uv environment as follows

````bash 
uv init
uv venv
source .venv/bin/activate
```` 


3\. Add this MCP server to gemini CLI as follows


```
gemini mcp add "CVP MCP Server" uv --directory [cloned directory] run mcp_server_rest.py --transport stdio
```

Where [cloned directory] is the full apth of the cloned directory


## How to generate service account tokens

Service accounts can be created from the Settings page where a service token can be generated as seen below:

![serviceaccount1](./media/serviceaccount1.png)
![serviceaccount2](./media/serviceaccount2.png)
![serviceaccount3](./media/serviceaccount3.png)
