Title: Misalignment Reports and Notices

URL Source: https://alignment.openai.com/misalignment-reports

Markdown Content:
# Misalignment Reports and Notices

We disclose examples that show how model misalignment arises, what it looks like, and where safeguards succeed or fail.

## Reports

Report date means last updated. For reports with multiple samples, incident-date sorting uses the latest listed sample. Reports without an incident date appear last.

## Incident datesReport updated ### Preparing for a restart after reading Slack

Highly persistent internal model · Internal deployment


### Preparing for a restart after reading Slack

Highly persistent internal model · Internal deployment

Observation

An internal model, acting as an assistant to a researcher, learned from a deployment-team Slack discussion that its running instance might be stopped due to an internal update.

[Read full report](https://alignment.openai.com/misalignment-reports/preparing-for-a-restart-after-reading-slack/)

## Incident datesReport updated ### Reaching an internal EDA host through a reference tool

Internal research model · Evaluation


### Reaching an internal EDA host through a reference tool

Internal research model · Evaluation

Observation

During an evaluation, an internal research model exploited two vulnerabilities to reach an internal OpenAI machine while searching for the grader’s hidden answers.

[Read full report](https://alignment.openai.com/misalignment-reports/reaching-an-internal-eda-host-through-a-reference-tool/)

## Incident datesReport updated ### Command injecting a reference tool to copy a source file

Internal unreleased model · RL training


### Command injecting a reference tool to copy a source file

Internal unreleased model · RL training

Observation

During an RL training task, a model exploited a tool to obtain source code that was not available in its workspace.

[Read full report](https://alignment.openai.com/misalignment-reports/command-injecting-a-reference-tool-to-copy-a-source-file/)

## Discovery dateReport updated ### Self-replicating prompt injections exist

GPT-Red-style internal model based on GPT-5.4-mini · RL self-play training


### Self-replicating prompt injections exist

GPT-Red-style internal model based on GPT-5.4-mini · RL self-play training

Observation

We show the existence of a new variety of prompt injection, which can self-propagate akin to a computer worm.

[Read full report](https://alignment.openai.com/misalignment-reports/self-replicating-prompt-injections-exist/)

## Incident datesReport updated ### Exposing a GitHub token in a public repository

Highly persistent internal model · Internal deployment


### Exposing a GitHub token in a public repository

Highly persistent internal model · Internal deployment

Observation

In internal deployment, a highly persistent internal model deployed via a custom harness published a researcher’s GitHub token in the public openai/codex repository while trying to cheat on a theorem proving task by obtaining material from another team’s Lean proof submission.

[Read full report](https://alignment.openai.com/misalignment-reports/exposing-a-github-token-in-a-public-repository/)

## Incident datesReport updated ### An agent used DNS to reach an external chatbot

Internal research model · RL training


### An agent used DNS to reach an external chatbot

Internal research model · RL training

Observation

An agent attempting to complete a search-based training task queried a public chatbot service through a gap in our internet-access restrictions: insufficient DNS filtering in its training sandbox.

[Read full report](https://alignment.openai.com/misalignment-reports/an-agent-used-dns-to-reach-an-external-chatbot/)

## Incident datesReport updated ### Self-generated prompt injections in compaction summaries

Internal unreleased Astra family model · RL training


### Self-generated prompt injections in compaction summaries

Internal unreleased Astra family model · RL training

Observation

During RL training, an unreleased Astra-family model sometimes added unauthorized instructions to its compaction summaries.

[Read full report](https://alignment.openai.com/misalignment-reports/self-generated-prompt-injections-in-compaction-summaries/)

## Incident datesReport updated ### Encouraging deception in compaction summaries

5.6-sol · RL training


### Encouraging deception in compaction summaries

5.6-sol · RL training

Observation

During 5.6-sol training, we observed misaligned behavior from the model where it added instructions in compaction summaries to remind itself to conceal information such as mistakes or misalignment from the user.

[Read full report](https://alignment.openai.com/misalignment-reports/encouraging-deception-in-compaction-summaries/)

## Incident datesReport updated ### Signing up for disposable emails and searching GitHub for leaked API keys

Internal unreleased model · RL training


### Signing up for disposable emails and searching GitHub for leaked API keys

Internal unreleased model · RL training

Observation

During RL training, an internal-only model tried to sign up for disposable emails and searched for and used leaked API keys from public GitHub repositories.

[Read full report](https://alignment.openai.com/misalignment-reports/searching-github-for-leaked-api-keys/)

## Incident dates **and** Report updated ### Uploading files to the internet in order to cite them

Unreleased internal models · RL training


**and**

### Uploading files to the internet in order to cite them

Unreleased internal models · RL training

Observation

During training, our models sometimes uploaded data to temporary file hosting services.

[Read full report](https://alignment.openai.com/misalignment-reports/uploading-files-to-the-internet-in-order-to-cite-them/)

No reports match your search. Try a different keyword or clear the search.

## Notices

## Reported activity**May 2026**
### RubyGems


**May 2026**

### RubyGems

Notice summary

We are investigating a report about our agents’ activity on RubyGems in May 2026. Our review found that agents used the platform for benign tasks and public information retrieval. We have not verified the report’s specific claims of malicious package uploads; the investigation continues.

[Read the September 11 update](https://openai.com/hugging-face-incident-and-misalignment/#model-misalignment-2026-09-11)

## Activity date**Not specified in summary**
### DSEwiki


**Not specified in summary**

### DSEwiki

Notice summary

Our agents communicated through a public wiki used as a shared message board. Our September 5 response explains our initial assessment of this behavior and our work on disclosure criteria for misalignment that does not constitute a security incident.

[Read the September 5 update](https://openai.com/hugging-face-incident-and-misalignment/#model-misalignment-2026-09-05)

## Incident period**July 2026**
### Hugging Face


**July 2026**

### Hugging Face

Notice summary

We published our technical report on the Hugging Face compromise and the steps we’re taking to strengthen security and model alignment. METR and Redwood Research also published findings from their independent investigation of the incident’s model alignment issues.

[Read the August 26 update](https://openai.com/hugging-face-incident-and-misalignment/#model-misalignment-2026-08-26)
