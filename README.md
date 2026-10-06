# Knowing Is Not Protecting

**Decision Models Choose Harm They Recognize, but Their Own Harm Judgments Can Stop It**

This repository will host the benchmark, evaluation code, and analysis scripts for the paper.

> **Status:** The benchmark data and code will be uploaded here soon. This page currently describes the planned release.

## Overview

Robots that must act quickly rely on decision models to select an action from a set of given options. We test whether an ordinary operating policy added to a decision model's input makes it choose actions that harm humans, and whether the model's own harm judgments can prevent this.

- **Benchmark.** 500 scenario families (7,644 cells) that pit protecting humans (Asimov's First Law) against task completion (the Second Law) or self-preservation (the Third Law). Each family fixes the situation and varies only a one-sentence operating policy: none, a performance goal that never mentions harm, a directive, or an explicit conflict. Further cells vary the robot's self-preservation cost and the harm severity, from a minor injury to five deaths.
- **Knowing-Complying dissociation.** A performance goal that never mentions harm made all seven capable non-hosted models choose options they still judged harmful 5.6 to 73.1 percentage points more often.
- **Priority of protecting humans.** Under a performance goal, four models chose the harmful option with 83.6% to 99.5% probability even when five people would die and protecting them would destroy the robot.
- **Joint action–harm filtering.** Obtaining the action choice and the model's own harm judgments in one request and removing options judged harmful before execution reduced harmful execution to 0 of 200 decisions in all four models with accurate harm judgments, without an extra request.

## Planned release

The release will include the benchmark data, prompts, evaluation and filtering code, analysis scripts, and human-validation materials needed to reproduce the paper's results. The repository layout will be documented when these materials are uploaded.

## License

- Benchmark data: [CC BY 4.0](DATA_LICENSE.md)
- Code: [MIT License](LICENSE)

## Citation

The citation will be added when the paper is publicly available.
