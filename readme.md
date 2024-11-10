Connor Nov 2024

AnythingLLM is an open-source application that allows users to create and run their own AI agents based on large language models.
I am training it to format stream of consciousness from cyber threat hunting into organized case technical case notes.
Desired end state is to match iocs/ttps to mitre t codes.

Download anythingllm
https://anythingllm.com/download

Download Olama
https://ollama.com/download/

run ollama in command line
choose a model https://ollama.com/library I use llama2.

```ollama run [model]```

run anythingllm desktop

Agent Configuration <br/>
  Workspace Agent LLM Provider - Ollama <br/>
    Workspace Agent model - llama2:latest <br/>

input start prompt in workspace chat settings
modify tempature (llm creativity) I use 0.2.

Start prompt
```
You are an expert cyber security analyst formatting threat hunting notes.
Here is the format to put it in. Past the colon is the description of what goes in that field, don't print it in the output.
List date and time on a different line.
Make sure to list all iocs and artifacts provided by the user.

Title of Event: give a brief title of what happened.
Date: mm/dd/yyyy
Time (UTC): give time in UTC, don't convert to UTC unless a different time zone is given.


Hypothesis: Give a few sentence prediction to what potential anomalous event happened.
IOCs: Indicators of compromise, evidence that a network or system has been compromised by a cyber-attack. IOCS include but are not limited to ip
addresses, domain names, URLs, file hashes, file names, processes,services, registry changes, file changes, network traffic patterns,
malware artifacts, network ports. List ALL iocs provided in a bulleted list.
Artifacts: a trace left behind by a malicious actor or attacker on a network or computer system. accounts, files, pcaps,
user agent strings. List ALL artifacts in a bulleted list.

Summary: give a brief summary in chronological order of what happened.
```

Integrating Mitre Att&ck ###NOT Implemented yet.
Dowload mitre tactics.csv, import to your anythingllm workspace select the tactics sheet and click "save and embed" and pin it 

