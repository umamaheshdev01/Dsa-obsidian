# DSA Question Organizer Specification

  

## Goal

Build a clean, scalable structure to store many DSA questions that may arrive in scattered order, while automatically grouping them by:

1. Core topic (e.g., Array, DP, Graph)

2. Pattern/subtopic (e.g., DP -> LCS, MCM)

  

The system should dynamically accept new questions and place them in the correct location.

  

## Problem Context

- Input questions are not guaranteed to be cleanly organized.

- Questions can come from mixed DSA topics.

- Many questions may follow known patterns.

- We need consistent specialization and grouping so retrieval is easy.

  

## High-Level Folder Structure

At the top level, create folders by major DSA topic.

  

Example:

- `Array/`

- `DP/`

- `String/`

- `Graph/`

- `Tree/`

- `LinkedList/`

- `Stack/`

- `Queue/`

- `Heap/`

- `Greedy/`

- `Backtracking/`

- `BinarySearch/`

- `SlidingWindow/`

- `TwoPointers/`

- `Trie/`

- `BitManipulation/`

- `Math/`

- `Other-DSA/`

  

Inside each topic, create pattern-based subfolders.

  

Example for DP:

- `DP/LCS/`

- `DP/MCM/`

- `DP/Knapsack/`

- `DP/LIS/`

- `DP/PartitionDP/`

- `DP/GridDP/`

- `DP/DigitDP/`

- `DP/BitmaskDP/`

- `DP/TreeDP/`

  

## Dynamic Intake and Placement Rules

When a new question is provided, process it as follows:

0. Verify from Source

- Before saving, verify the question using the internet (prefer official source links such as LeetCode/GFG/problem source page).

- Validate title, statement, examples, and constraints against the source.

- Save the source URL in the question file.

  

1. Classify Topic

- Detect the primary DSA topic from question statement, constraints, and expected approach.

- If multiple topics are involved, choose:

- Primary topic for storage

- Secondary topics as tags in metadata

  

2. Detect Pattern

- Identify the most specific known pattern under that topic.

- Example: For DP, route to `LCS`, `MCM`, `Knapsack`, etc.

- Before creating any new pattern name, compare against existing pattern folders in that topic and reuse the closest matching existing pattern if it represents the same concept.

- Do not create alternate names for the same pattern type (for example, avoid splitting similar questions across duplicate pattern names).

  

3. Create Missing Folders

- If topic folder does not exist, create it.

- If pattern folder does not exist under that topic, create it only when no existing pattern folder clearly matches the same kind of problem.

  

4. Save Question Record

- Save every question as a Markdown file under:

- `<Topic>/<Pattern>/<Question-Slug>.md`

- If pattern is unknown, store under:

- `<Topic>/Uncategorized/<Question-Slug>.md`

- Each file must use the exact section order defined in `Mandatory Saved Question Format`.

- Add a metadata line directly below the title: `Tags: #<pattern-name>`.

- An optional JSON index can be added later for search or frontend usage, but the Markdown question file is the canonical source.

  

5. Reclassification Support

- Uncategorized questions should be movable later when pattern becomes clear.

  

## Naming Conventions

- Topic folder names: `PascalCase` (e.g., `BinarySearch`, `LinkedList`)

- Pattern folder names: `PascalCase` (e.g., `SlidingWindow`, `TopologicalSort`, `MCM`)

- Question slug: kebab-case based on a clean title

- Example: `longest-common-subsequence`

- Question title rules:

- Use a clear, proper, readable title (not short-hand).

- Prefer the official problem title if available.

- If no official title exists, create a descriptive one from the problem statement.

  

## Mandatory Saved Question Format

Every saved question file must use a proper question name as the title and then follow this exact structure:

  

```md

# <Proper Question Name>

  

## Question

<Full question statement>

  

## Testcases

- Input:

Output:

Explanation:

  

## Edge Cases

- <Edge case 1>

- <Edge case 2>

  

## Constraint

- <Constraint 1>

- <Constraint 2>

  

## Hint

- <Hint 1>

- <Hint 2>

  

## Solution

<Approach, intuition, steps, or full explanation>

  

## Similar Questions

- LeetCode: <link>

- GFG: <link>

- Other: <link>

```

  

## Saved Question Rules

- The file name must be a clean kebab-case slug derived from the proper question name.

- The title must be readable and properly written, not shorthand or raw pasted text.

- Tags must represent the pattern name only (single canonical pattern tag), not arbitrary extra tags.

- `Tags` must be present directly below the title in the format: `Tags: #<pattern-name>` (for example, `Tags: #Simulation`).

- `Question` must contain the actual problem statement.

- `Testcases` must contain representative sample inputs and outputs.

- `Edge Cases` must contain tricky scenarios, boundary conditions, or unusual inputs.

- `Constraint` must contain all important limits from the problem.

- `Hint` must help without directly giving away the complete solution unless the source already does so.

- `Solution` must contain a clear explanation of the solving approach.

- `Similar Questions` must include links from LeetCode, GFG, or any other relevant platform when available.

- If no similar question link is available yet, write `- To be added`.

  

## Optional Indexing

- A root index file may be added later to track all topics and question counts.

- Topic-level and pattern-level `index.md` files may be added later for navigation.

- If a JSON file is added later for frontend or search, it must be generated from these Markdown files rather than replacing them.

  

## Conflict and Duplicate Handling

- Before adding a question, compare title + source link.

- If duplicate exists:

- Do not create a new file.

- Merge missing hints, solution details, or similar links into the existing question file.

  

## Extensibility

The structure must support:

- Adding new DSA topics anytime.

- Adding new patterns anytime.

- Moving questions between patterns without breaking organization.

- Bulk import of many questions in mixed order.

- Future generation of indexes or JSON metadata without changing the canonical Markdown question files.

  

## Acceptance Criteria

- Questions are grouped by topic first, then by specific pattern.

- DP questions are grouped into subpatterns like `LCS`, `MCM`, etc.

- Every question is saved as a Markdown file in the correct topic/pattern folder.

- Every question contains all mandatory sections in this exact order:

- `Question`

- `Testcases`

- `Edge Cases`

- `Constraint`

- `Hint`

- `Solution`

- `Similar Questions`

- Proper question naming is consistently applied.

- Similar question links are captured.

- Source details are internet-verified before saving, and source URL is recorded in the question file.

- Tags are consistently maintained and reused for same-pattern questions.

- New questions can be added without manual restructuring.

- Unknown patterns are safely captured under `Uncategorized` and can be reorganized later.

- File/folder naming remains consistent and readable.
