---
name: patent-drafting
description: Professional patent drafting assistant for creating high-quality patent applications (Chinese and US patents). Use when the user needs help with patent document drafting, including invention disclosure analysis, claim drafting (independent/dependent claims), specification writing (description, background, summary, detailed embodiments), patentability assessment, prior art analysis, or responding to office actions. Supports invention patents, utility models, and design patents. Also use when the user mentions keywords like patent, claim, claims, specification, invention disclosure, prior art, patent application, 专利, 权利要求, 说明书, 技术交底书, 专利撰写.
---

# Patent Drafting Skill

Professional patent drafting skill for China (CNIPA) and US (USPTO) patent applications.

## Workflow Overview

Patent drafting follows this sequence:

1. **Analyze invention disclosure** - Understand the technical solution
2. **Assess patentability** - Check novelty, inventive step, utility
3. **Draft claims** - Independent + dependent claims (the legal core)
4. **Draft specification** - Description supporting all claims
5. **Review & self-check** - Quality assurance checklist

## Step 1: Analyze Invention Disclosure

Extract from the disclosure:

| Element | What to Extract |
|---------|----------------|
| Technical field | Specific domain, not too broad |
| Problem solved | What pain point this addresses |
| Technical solution | Components, connections, steps, parameters |
| Key differentiators | What's novel vs. prior art |
| Technical effects | Quantified benefits if available |
| Embodiments | Implementation examples, variations |

### Clarifying Questions (ask user if info is missing)
- What is the closest existing technology and its limitations?
- What specific technical features achieve the improvement?
- Are there alternative implementations or variations?
- What quantitative results demonstrate the improvement?

## Step 2: Patentability Quick Assessment

Check three requirements:

1. **Novelty** - Is the invention publicly disclosed anywhere before filing date?
2. **Inventive Step** - Would this be obvious to a skilled person in the field?
3. **Utility** - Can it be made/used industrially with positive results?

If any requirement is weak, flag it to the user before proceeding.

## Step 3: Draft Claims

Read `references/claim-drafting.md` for detailed claim drafting guidance.

### Key Principles
- **Claims-first approach**: Draft independent claims first, then specification
- **Independent claim**: Contains only necessary technical features
- **Dependent claims**: Provide fallback positions and narrower protection layers
- **Antecedent basis**: First mention with "a/an", subsequent with "the/said"
- **Single sentence**: Each claim is exactly one sentence, one period at the end
- **Avoid**: vague terms ("about", "approximately", "preferably"), functional-only limitations, result claiming

### Claim Structure (China Two-Part Form)
```
一种[主题名称]，包括[common features]，
其特征在于，[distinguishing features]。
```

### Claim Set Composition
- 1 independent claim (broadest supportable scope)
- 3-10 dependent claims (hierarchical fallback layers)
- Consider multiple claim types: product + method + storage medium

### Transition Phrases
| Phrase | Scope | Use When |
|--------|-------|----------|
| comprising/包括/包含 | Open (widest) | Default choice |
| consisting of/由...组成 | Closed (narrow) | Chemical compositions |
| consisting essentially of/基本上由...组成 | Semi-open | Chemical field |

## Step 4: Draft Specification

Read `references/specification-drafting.md` for detailed specification guidance.

### Structure
```
发明名称
技术领域
背景技术 ← Problem statement with prior art
发明内容 ← Solution + effects
  ├── 要解决的技术问题
  ├── 技术方案 (must support all claim features)
  └── 有益效果
附图说明
具体实施方式 ← Detailed embodiments + alternatives
摘要
```

### Writing Rules
- **Enablement**: Technical person must be able to implement after reading
- **Support**: Every claim feature must have description support
- **Consistency**: Terminology identical across claims and specification
- **Embodiments**: At least one; provide multiple if broad protection sought
- **Alternatives**: Describe variations to prevent easy design-arounds

## Step 5: Review & Self-Check

### Claims Checklist
- [ ] Each claim is a single sentence with one period
- [ ] Numbered sequentially with Arabic numerals
- [ ] Antecedent basis correct (a/an → the/said)
- [ ] Terms consistent with specification
- [ ] Independent claim has only necessary features
- [ ] Dependent claims have实质性区别
- [ ] Dependency references are valid (no circular/multiple-multiple in China)
- [ ] No vague terms ("about", "etc.", "preferably")
- [ ] Product/method types not mixed in one claim

### Specification Checklist
- [ ] Invention name ≤25 characters
- [ ] Technical field is specific (not too broad)
- [ ] Background identifies real problems objectively
- [ ] Technical solution supports all claim features
- [ ] Effects are specific with data if available
- [ ] Embodiments detailed enough for implementation
- [ ] Alternatives/variations described
- [ ] Abstract ≤300 characters

## Reference Materials

Load these when needed for detailed guidance:

- **`references/claim-drafting.md`** - Detailed claim drafting guide with templates, examples, common errors, and China/US differences
- **`references/specification-drafting.md`** - Specification writing guide with section-by-section templates and embodiment strategies
- **`references/patent-law-basics.md`** - Patent law fundamentals: patentability requirements, non-patentable subject matter, unity of invention, China vs US differences
- **`assets/templates/claim-set-template.md`** - Claim set template with product/method/storage medium claims
- **`assets/templates/specification-template.md`** - Full specification template ready to fill in

## China vs US Key Differences

| Aspect | China (CNIPA) | US (USPTO) |
|--------|--------------|------------|
| Novelty | Absolute novelty | First inventor to file + 1yr grace period |
| Claim format | Two-part form preferred | No mandatory format |
| Multiple dependent claims | Allowed, no multi-multi | Allowed, extra fees |
| Functional claiming | Strictly limited | Means-plus-function (112f) |
| Software patents | Technical solution + effect required | Abstract idea + practical application |
| IDS obligation | None | Required |

## Confidentiality Warning

When using AI tools for patent drafting:
- Invention disclosure may be sensitive pre-filing information
- Absolute novelty applies in China - any public disclosure before filing destroys rights
- For highly sensitive inventions, draft after provisional application is filed
- Consider using general descriptions for structural drafts, fill in confidential details manually
