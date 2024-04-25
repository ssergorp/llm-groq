# llm-groq

Updated with access to llama3-8b and 70b models via the Groq api.

[LLM](https://llm.datasette.io/) plugin providing access to [Groqcloud](http://console.groq.com) models.

## Installation

clone repo to your local machine, cd into dir, run cmd 'llm install -e .'

```bash
git clone https://github.com/ssergorp/llm-groq.git
cd llm-groq
llm install -e .
```

## Usage

First, obtain an API key for [Groqcloud](https://console.groq.com/).

Configure the key using the `llm keys set groq` command:
```bash
llm keys set groq
```

```
<paste key here>
```

You can now access these hosted models: `groq-llama2`, `groq-llama3-8b`, `groq-llama3-70b`, `groq-gemma` and `groq-mixtral`.

To run a prompt through `groq-mixtral`:

```bash
llm -m groq-mixtral 'A sassy name for a pet sasquatch'
```
To start an interactive chat session with `groq-mixtral`:
```bash
llm chat -m groq-mixtral
```
```
llm chat -m groq-mixtral
Chatting with groq-mixtral
Type 'exit' or 'quit' to exit
Type '!multi' to enter multiple lines, then '!end' to finish
> three proud names for a pet walrus
Here are three whimsical and proud-sounding names for a pet walrus:

1. Regalus Maximus
2. Glacierus Royalty
3. Arctican Aristocat

These names evoke a sense of majesty and grandeur, fitting for a noble and intelligent creature like a walrus. I hope you find these names fitting and amusing! If you have any other requests or need assistance with something else, please don't hesitate to ask.
```
To use a system prompt with `groq-mixtral` to explain some code:
```bash
cat example.py | llm -m groq-mixtral -s 'explain this code'
```

## Model options

TBD

## Development

To set up this plugin locally, first checkout the code. Then create a new virtual environment:
```bash
cd llm-groq
python3 -m venv venv
source venv/bin/activate
```
