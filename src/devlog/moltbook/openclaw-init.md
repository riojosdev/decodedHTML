# Setting up OpenClaw AI Bot

We installed the OpenClaw CLI using powershell cmdlet Invoke-WebRequest (iwr).

Then we progress onto the onboarding, which requests for manual config or quickstart.

`openclaw onboard --install-daemon`

## Manual 
### Local gateway or remote gateway
### Workspace directory
> I wanted autocompletion here
### Model/auth provider
openai
anthropic
minimax
moonshot ai
google
openrouter
qwen
z.ai (glm 4.7)
copilot
vercel ai gateway
opencode zen
xiaomi
synthetic
venice ai
..skip for now

#### filter models
All providers
│  ○ amazon-bedrock
│  ○ anthropic
│  ○ azure-openai-responses
│  ○ cerebras
│  ○ github-copilot
│  ○ google
│  ○ google-antigravity
│  ○ google-gemini-cli
│  ○ google-vertex
│  ○ groq
│  ○ huggingface
│  ○ kimi-coding
│  ○ minimax
│  ○ minimax-cn
│  ○ mistral
│  ○ openai
│  ○ openai-codex
│  ○ opencode
│  ○ openrouter
│  ○ vercel-ai-gateway
│  ○ xai
│  ○ zai


#### Ollama - quickstart through the wizard is not available

choosing skip for now, for the model/auth provider

## DETOUR
### ollama model installation
#### whats the best model for our purpose
* system resources -- i need it to be lightweight
* processing abilities it needs to be accessed -- text/vision/...
* 

When selecting an model

The abilities it posses and the abilities we receive needs to be considered



#### Our objectives
* Twitch Bot x OBS Interactions Controls
* Friend streamer engagement / interactor

#### Chat abilities
* Prompt ai to do stuff
    * ollama
    * obs
* Use human predefined abilities/functions/interactions

---

* model
Default model
│  ollama/qwen3-vl:2b

which is not found !todo fix

* channel (chat platform)
skipped

* workspace
home directory one
!todo fix (move to code observatory)

* skills




---

## Issue
### Issue: Openclaw does not recognize ollama's locally available model(s)
I manually added the model, but. I dont think openclaw was able to identify it.
