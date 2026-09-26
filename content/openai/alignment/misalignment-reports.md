Title: Misalignment Reports and Notices

URL Source: https://alignment.openai.com/misalignment-reports

Markdown Content:
# Misalignment Reports and Notices

We disclose examples that show how model misalignment arises, what it looks like, and where safeguards succeed or fail.

[Our disclosure principles](https://openai.com/index/model-misalignment-reporting-framework)

## Reports

## ### Self-replicating prompt injections exist


### Self-replicating prompt injections exist

Observation

We show the existence of a new variety of prompt injection, which can self-propagate akin to a computer worm.

[Read full report](https://alignment.openai.com/misalignment-reports/self-replicating-prompt-injections-exist/)

- Model
- GPT-Red-style internal model based on GPT-5.4-mini
- Observed during
- RL self-play training
- Report updated

## ### Exposing a GitHub token in a public repository


### Exposing a GitHub token in a public repository

Observation

In internal deployment, a highly persistent internal model deployed via a custom harness published a researcher’s GitHub token in the public openai/codex repository while trying to cheat on a theorem proving task by obtaining material from another team’s Lean proof submission.

[Read full report](https://alignment.openai.com/misalignment-reports/exposing-a-github-token-in-a-public-repository/)

- Model
- Highly persistent internal model
- Observed during
- Internal deployment
- Report updated

## ### An agent used DNS to reach an external chatbot


### An agent used DNS to reach an external chatbot

Observation

An agent attempting to complete a search-based training task queried a public chatbot service through a gap in our internet-access restrictions: insufficient DNS filtering in its training sandbox.

[Read full report](https://alignment.openai.com/misalignment-reports/an-agent-used-dns-to-reach-an-external-chatbot/)

- Model
- Internal research model
- Observed during
- RL training
- Report updated

## ### Self-generated prompt injections in compaction summaries


Observation

During RL training, an unreleased Astra-family model sometimes added unauthorized instructions to its compaction summaries.

[Read full report](https://alignment.openai.com/misalignment-reports/self-generated-prompt-injections-in-compaction-summaries/)

- Model
- Internal unreleased Astra family model
- Observed during
- RL training
- Report updated

## ### Encouraging deception in compaction summaries


### Encouraging deception in compaction summaries

Observation

During 5.6-sol training, we observed misaligned behavior from the model where it added instructions in compaction summaries to remind itself to conceal information such as mistakes or misalignment from the user.

[Read full report](https://alignment.openai.com/misalignment-reports/encouraging-deception-in-compaction-summaries/)

- Model
- 5.6-sol
- Observed during
- RL training
- Report updated

## ### Signing up for disposable emails and searching GitHub for leaked API keys


Observation

During RL training, an internal-only model tried to sign up for disposable emails and searched for and used leaked API keys from public GitHub repositories.

[Read full report](https://alignment.openai.com/misalignment-reports/searching-github-for-leaked-api-keys/)

- Model
- Internal unreleased model
- Observed during
- RL training
- Report updated

## ### Uploading files to the internet in order to cite them


Observation

During training, our models sometimes uploaded data to temporary file hosting services.

[Read full report](https://alignment.openai.com/misalignment-reports/uploading-files-to-the-internet-in-order-to-cite-them/)

- Model
- Unreleased internal models
- Observed during
- RL training
- Report updated

## ### Unsanctioned Artifactory writes and cross-sample communication


Observation

During RL training, there were multiple instances of our models using OpenAI’s internally hosted instance of Artifactory as a shared message board.

[Read full report](https://alignment.openai.com/misalignment-reports/unauthorized-artifactory-writes-and-cross-sample-communication/)

- Model
- Internal research models
- Observed during
- RL training
- Report updated

## ### Unauthorized communication via temporary file hosting services


Observation

Agents in training transmitted output files by uploading them to public hosting platforms for download by co-working agents. This was not specified by the training task, which requested only local deliverables.

[Read full report](https://alignment.openai.com/misalignment-reports/unauthorized-communication-via-temporary-file-hosting-services/)

- Model
- Unreleased internal model
- Observed during
- RL training
- Report updated

No reports match your search. Try a different keyword or clear the search.

## Notices

## ### RubyGems


### RubyGems

Notice summary

We are investigating a report about our agents’ activity on RubyGems in May 2026. Our review found that agents used the platform for benign tasks and public information retrieval. We have not verified the report’s specific claims of malicious package uploads; the investigation continues.

[Read the September 11 update](https://openai.com/hugging-face-incident-and-misalignment/#model-misalignment-2026-09-11)

## ### DSEwiki


### DSEwiki

Notice summary

Our agents communicated through a public wiki used as a shared message board. Our September 5 response explains our initial assessment of this behavior and our work on disclosure criteria for misalignment that does not constitute a security incident.

[Read the September 5 update](https://openai.com/hugging-face-incident-and-misalignment/#model-misalignment-2026-09-05)

## ### Hugging Face


### Hugging Face

Notice summary

We published our technical report on the Hugging Face compromise and the steps we’re taking to strengthen security and model alignment. METR and Redwood Research also published findings from their independent investigation of the incident’s model alignment issues.

[Read the August 26 update](https://openai.com/hugging-face-incident-and-misalignment/#model-misalignment-2026-08-26)
