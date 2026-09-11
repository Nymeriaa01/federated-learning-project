# Contribution note — Florian Magnan

> This repository is a **fork** of [`redaouzz/federated-learning-project`](https://github.com/redaouzz/federated-learning-project),
> published by Réda Ouzzane. I forked it so that work I took part in is visible from my profile.
> **I do not claim authorship of this repository.**

## Authors

Academic project carried out at **Politecnico di Torino**, course *Machine Learning and Deep
Learning* (Project 5 — *Federated Learning Under the Lens of Model Editing*).

The final report is co-signed by four authors:

| Author | |
|---|---|
| **Giovanna Brod Zamojska** (s337350) | main author of the codebase — code architecture, experiment manager, masking strategies |
| **Réda Ouzzane** (s347803) | co-author |
| **Florian Magnan** (s347801) | co-author — that's me |
| **Niloofar Vazirpanah** (s340784) | co-author of the report (wrote the introduction) |

The code and experimental work was carried out by three of us: Giovanna, Réda and myself.

## What I actually did

With **Réda Ouzzane**, I designed and implemented the **IID and non-IID federated
architecture** — not just training a network, but the client partitioning, the FedAvg loop, the
entire fine-tuning campaign and the testing protocol.

The implementation strategy was agreed on by the three of us together with Giovanna. Réda and I
then developed as a pair, taking turns part by part on the same files — which is why we cannot
split our respective contributions commit by commit.

The project was graded **28/30**.

### Why the git history doesn't show this

Two reasons, and I would rather state them than let anyone draw their own conclusions:

- The day-to-day development happened in a **separate repository that is private**, owned by
  Giovanna Brod Zamojska, plus a good deal of pair work on Google Colab. Giovanna wrote the
  majority of that codebase.
- **This** repository is a re-upload: Réda published the project here in a single batch on
  20 August 2025, months after the work was finished. Every commit therefore carries his name,
  and the history documents nobody's contribution — not his, not mine.

So the commit log here should not be read as a record of who did what.

## The project in two lines

Federated Learning on CIFAR-100 with a DINO-pretrained ViT-S/16 backbone. Centralized training
compared against FedAvg under IID and non-IID partitions, then model editing via sparse
fine-tuning guided by Fisher sensitivity masks. Original contribution: a comparison of five
mask selection rules (sensitivity / magnitude / random).

Headline results (test accuracy): Centralized 74.62% → Centralized + editing **84.31%**;
FedAvg IID 72.41%; FedAvg non-IID 66.51%.

## Dates — to avoid any confusion

- **Work carried out:** February – July 2025
- **Published on GitHub by Réda:** 20 August 2025
- **Fork created on my account:** September 2026, while rebuilding my GitHub profile

## License

The upstream repository carries an MIT license. This fork modifies no source file — it only
adds this note and the final report.
