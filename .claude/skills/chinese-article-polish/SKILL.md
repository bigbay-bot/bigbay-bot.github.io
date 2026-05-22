---
name: chinese-article-polish
description: This skill should be used when the user asks to polish Chinese writing, revise a Chinese article, check Chinese typos or grammar, improve wording, create or update a blog post from draft Chinese text, or asks to "检查错别字", "语法错误", "润色", "排版", "指出修改". It preserves the author's meaning and tone while producing a publishable version and a clear change report.
version: 1.0.0
---

# Chinese Article Polish

Use this skill for Chinese prose, personal blog posts, reflections, essays, notes, and article drafts.

## Goals

- Preserve the author's original meaning, perspective, emotional tone, and narrative rhythm.
- Correct typos, wrong particles, punctuation, awkward grammar, and unclear sentence structure.
- Improve readability without making the text sound overly formal, generic, or AI-written.
- Format the result as a clean article suitable for publishing.
- Always tell the user what changed and why.

## Workflow

1. Read the user's draft carefully.
2. Decide a concise title if the user did not provide one.
3. Polish the text with minimal necessary edits:
   - Fix typos and wrong characters.
   - Fix particles such as `的 / 地 / 得`.
   - Add missing punctuation.
   - Split long or tangled sentences.
   - Keep colloquial expressions when they carry personality.
   - Add paragraph breaks for rhythm and readability.
4. If creating or updating a blog post, use the existing project page style and update relevant entry pages.
5. Provide a final report listing the important changes.

## Editing principles

- Do not rewrite the author's life experience into a generic motivational essay.
- Do not add facts, dates, places, emotions, or conclusions that the user did not imply.
- Prefer small, precise edits over large rewrites.
- Keep strong original phrases unless they are unclear or incorrect.
- For personal writing, keep some breathing room: short paragraphs, pauses, and simple sentences are acceptable.
- If a sentence is intentionally informal, preserve that informality unless it looks like a typo.

## Output format

When the user asks for polishing only, respond with:

```markdown
## 润色后

[polished article]

## 修改说明

- `原文片段` → `修改后片段`
  - 修改原因。
```

When also modifying files, respond with:

```markdown
已完成：[brief summary]

文章路径：`path-or-url`

主要修改点：

- `原文片段` → `修改后片段`
  - 修改原因。

已验证：
- [checks performed]
```

## Common Chinese fixes

- `喜欢的不得了` → `喜欢得不得了`
- `慢慢的攒` → `慢慢攒`
- `感受的深切` → `深切地感受到`
- `是偶` → `是哦`
- Chinese and English/model names should usually have spaces around English text, e.g. `本田 CBR500R`.
- Dialogue should use Chinese quotation marks: `他说：“……”`
- Rhetorical endings should use `？` when appropriate.

## Blog post conventions for this project

If applying this skill inside this static Hexo output repository:

- Use existing static HTML templates instead of introducing a new generator.
- Put new posts under `YYYY/MM/DD/slug/index.html`.
- Update homepage article cards when the new post should be featured.
- Update archive, category, and tag pages so the post is reachable.
- Keep navigation labels in Chinese.
- Run local page checks when possible.

## Change report style

The change report should focus on meaningful edits, not every punctuation mark. Include:

- typo corrections;
- grammar corrections;
- sentence restructuring;
- wording changes that affect tone or clarity;
- formatting changes such as paragraph splitting.

Avoid claiming changes that were not made.
