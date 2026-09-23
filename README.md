# sleepcast-script-review

[中文说明](README.zh.md)

Review adult English SleepCast scripts and produce a Chinese review report with quoted English, proposed replacements, and Chinese translations for human comparison.

## Install

Clone this private repository with an account that has access:

```sh
git clone https://github.com/ZimaBlue1226/sleepcast-script-review.git
```

Place the complete `sleepcast-script-review` folder in your agent's skills directory. Keep `SKILL.md` and `references/` together. An existing installation can be updated with these files; preserve any local changes before replacing them.

## Use

Invoke the skill and attach a script Markdown file or provide its local path:

```text
Use $sleepcast-script-review to review ./scripts/episode.md.
```

To choose the report location:

```text
Use $sleepcast-script-review to review ./scripts/episode.md.
Save the report in ./reviews/.
```

Provide the script file and select a review category: vintage/realistic (古典类) or secondary-world fantasy (第二世界幻想类). If you have not explicitly selected one for this script, the skill asks and waits before reviewing; it does not infer or default the category. Vintage/realistic uses the general standards; secondary-world fantasy adds the fantasy standards. No theme outline is required. The subsequent review workflow is unchanged. It accepts English-only and bilingual files. English narration is the sole review basis; any supplied Chinese is not reviewed. Empty, Chinese-only or markup-only inputs cannot be reviewed. Excerpts are reviewed within their stated scope.

## Review scope

- Natural North American English and listening comprehension.
- Adult sleep suitability, safety and low-pressure narration.
- Narrative, spatial and perceptual logic.
- Genre consistency, with fantasy-world consistency where applicable.
- Pacing, repetition and redundancy.

Severity describes impact, not editing order:

| Level | Meaning |
|---|---|
| P0 | Clearly destroys the safe sleep experience or makes the central experience untenable. |
| P1 | A demonstrable defect causes misunderstanding, disrupted comprehension, loss of immersion or local arousal, while the core experience remains viable. |
| P2 | A demonstrable expression or pacing defect reduces fluency without undermining comprehension or the core experience. |

Personal preferences are not findings. BGM, audio markup, TTS implementation and synthesized duration are outside scope.

## Output

One UTF-8 Markdown report, `<input-stem>-审查报告.md`, beside the input by default. A specified output directory takes precedence. Existing reports receive an unused version suffix rather than being overwritten.

The report contains scope, issue statistics, detailed findings and a conclusion. Each finding includes its ID, severity, type, original file line numbers, explanation, quoted English and proposed replacement, with Chinese translations derived from those English passages. PART labels are included when present. Repairs requiring a core creative decision are marked pending confirmation. A zero-finding review still produces a report.

The input script remains unchanged. The skill does not automatically rewrite, run review/rewrite loops, publish reports or send notifications.

## Maintain

Maintain [SKILL.md](SKILL.md) and the bundled [general standards](references/general-standards.md), [fantasy standards](references/fantasy-standards.md), [severity definitions](references/severity.md) and [report template](references/report-template.md) directly. Execution does not require Feishu, external SOP downloads or another skill.
