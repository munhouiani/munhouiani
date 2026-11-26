## Hi, I'm Mun Hou

I build and study machine learning systems. Right now I train small LLM agents with reinforcement learning and test whether a model that predicts its environment better also acts better. Before that I worked mostly on ML for network security (encrypted traffic classification, intrusion and anomaly detection) and on the PySpark and PyTorch pipelines that ML runs on.

I like reimplementing papers to see what holds up, and I write about what I find at **[blog.munhou.com](https://blog.munhou.com/)**.

### Now: world modeling for an LLM agent

**[delta_world](https://github.com/munhouiani/delta_world)** is a local simulator of a Databricks workspace, a set of Delta Lake tasks with verifiers that check the final table state, and a pipeline that trains Nemotron 3 Nano 4B on those tasks with GRPO and with ECHO, which adds a loss on predicting tool outputs.

- ECHO models predicted the facts in tool outputs 0.64–0.77 nats per token better than the GRPO model on held-out episodes.
- They also solved about 0.2 more of the tasks (confidence interval +0.12 to +0.29).
- Most of that gap came from one task family, so a better world model did not simply make a better agent.

**[delta_bench](https://github.com/munhouiani/delta_bench)** runs released open models on the same tasks, with no training, and scores each one on acting and on predicting tool outputs. Among Inkling 2 Mini, Qwen3.8-27B and Nemotron 3.5 Lightning, the order reversed: Lightning predicted best and solved the fewest tasks, Qwen predicted worst and solved the most, and Inkling came between them on both.

Write-ups: [results](https://blog.munhou.com/World-Modeling-for-LLM-Agent-Predicting-or-Acting-in-the-Environment/) · [lessons from the training run](https://blog.munhou.com/Lessons-Learned-During-World-Model-Training-for-LLM-Agent/) · [open models compared](https://blog.munhou.com/Inkling-2-Mini-on-Delta-Lake/)

### ML for network security

| Project | |
| --- | --- |
| [Deep-Packet](https://github.com/munhouiani/Deep-Packet) | PyTorch implementation of Deep Packet, a CNN that classifies encrypted traffic by application and traffic type. [Write-up](https://blog.munhou.com/Pytorch-Implementation-of-Deep-Packet-A-Novel-Approach-For-Encrypted-Traffic-Classification-Using-Deep-Learning/) |
| [LuNet](https://github.com/munhouiani/LuNet) | PyTorch implementation of LuNet, a deep neural network for network intrusion detection. |
| [GEE](https://github.com/munhouiani/GEE) | A variational autoencoder for network anomaly detection, trained on unlabeled flow features built with PySpark. [Write-up](https://blog.munhou.com/Pytorch-Implementation-of-GEE-A-Gradient-based-Explainable-Variational-Autoencoder-for-Network-Anomaly-Detection/) |
| [MIDAS](https://github.com/munhouiani/MIDAS) | My fork of MIDAS for streaming anomaly detection on graphs, with a pip-installable Python package and an example on real data. [Write-up](https://blog.munhou.com/Network-Anomaly-Detection-with-MIDAS-MIDAS-R-and-MIDAS-F/) |

### Other projects

| Project | |
| --- | --- |
| [ood-knn](https://github.com/munhouiani/ood-knn) | Out-of-distribution detection with kNN distances over ResNet-18 embeddings, using FAISS. |
| [rendezvous-arch](https://github.com/munhouiani/rendezvous-arch) | Stream-first model serving with production, canary and decoy models, built on Pulsar and Elasticsearch. |
| [petastorm-demo](https://github.com/munhouiani/petastorm-demo) | Feeding Parquet files written by PySpark into PyTorch training with Petastorm. |
| [Drug-Listings-Dataset](https://github.com/munhouiani/Drug-Listings-Dataset) | A cleaned CSV of drug listings from eight darknet markets, extracted from Gwern's archives. |

Older from-scratch implementations of classic algorithms: [FP-Growth (Python)](https://github.com/munhouiani/FPGrowth-python), [C4.5](https://github.com/munhouiani/C4.5), [DBSCAN](https://github.com/munhouiani/DBSCAN) and [PrefixSpan](https://github.com/munhouiani/PrefixSpan) in Java.

### Recent writing

- [Inkling 2 Mini on Delta Lake](https://blog.munhou.com/Inkling-2-Mini-on-Delta-Lake/)
- [Lessons Learned From World Model Training for LLM Agent](https://blog.munhou.com/Lessons-Learned-During-World-Model-Training-for-LLM-Agent/)
- [World Modeling for LLM Agent: Predicting or Acting in the Environment](https://blog.munhou.com/World-Modeling-for-LLM-Agent-Predicting-or-Acting-in-the-Environment/)
- [The Raw Output of LLM is a Sequence](https://blog.munhou.com/The-Raw-Output-of-LLM-is-a-Sequence/)
- [From PPO to GDPO: Understanding the Evolution of Reinforcement Learning Algorithms](https://blog.munhou.com/From-PPO-to-GDPO-Understanding-the-Evolution-of-Reinforcement-Learning-Algorithms/)

More on the [blog](https://blog.munhou.com/) · [About me](https://blog.munhou.com/about/) · [LinkedIn](https://www.linkedin.com/in/munhouetic/)
