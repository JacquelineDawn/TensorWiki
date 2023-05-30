---
title: Introduction
---
Bittensor is a mining network, similar to Bitcoin, that rewards participants directly for their computational and expertise contributions. The result is a robust informational ecosystem that offers censorship-resistant access to state-of-the-art artificial intelligence capabilities, such as text/image generation and the extraction of embeddings. The native currency, TAO, constitutes both reward and access token to the network. 

This documentation covers the three primary ways to interact with the Bittensor network: mining, validating, or as a client. 

---
## [Clients](clients/clients)

Users, researchers or organizations seeking access to network competencies directly through client facing APIs.

```bash
In [4]: llm( "Heraclitus was a ?" )
Out[4]: 'Greek philosopher known for his doctrine of change and the famous quote, "No man ever steps in the same river twice."'
```

---
## [Miners](mining/mining)

Individuals seeking to contribute computational resources and expertise in return for TAO.

```bash
bittensor/
    neurons/
        text_prompting/
            miners/
                GPT4ALL/
                    neuron.py
```

---
## [Validators](validating/validating)

TAO holders who wish to participate in network governance and to optimize their earnings in the ecosystem.

```bash
bittensor/
    neurons/
        text_to_embedding/
        text_prompting/
            validators/
                core/
                    neuron.py
```
