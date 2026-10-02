# Implementation Plan for Issue #71

## Root Cause
The test fixture in `tests/unit/test_readme_parser.py::test_extract_heading_hierarchy` 
has 8-space indentation at the beginning of each line. This indentation causes Markdown 
to parse the text as a code block instead of regular content. The `_extract_heading_hierarchy` 
parser returns an empty list because it finds no headings in a code block.

**Evidence:** Reproduced in unit 2 — the test output shows `assert 0 > 0` (empty heading list) 
when running with `--runxfail`.

## Scope
This fix changes only:
- The test fixture indentation in `tests/unit/test_readme_parser.py` (remove leading spaces)
- The `@pytest.mark.xfail` marker that marks the test as expected-to-fail (remove it)

No changes to the parser code, no refactoring, no additional tests.

## Implementation Steps
1. Open `tests/unit/test_readme_parser.py`
2. Locate `test_extract_heading_hierarchy` method (around line 138)
3. Remove the 8-space indentation from the markdown fixture string (lines 141-153)
   - Change each indented line to start at column 0 (no leading spaces)
4. Remove the `@pytest.mark.xfail(strict=True, reason="issue #71...")` decorator
5. Save the file

## Testing & Verification
Run the test to verify the fix:
```bash
cd E:\CodePath\AI 301\pathreview-ai301-fa26-s3
source venv/Scripts/activate
python -m pytest tests/unit/test_readme_parser.py::TestReadmeParser::test_extract_heading_hierarchy -v
```

Expected result: Test passes (no XFAIL, no failures). Output should show:
` test_extract_heading_hierarchy PASSED [100%] `

## Unknowns & Notes
- None. The fixture removal is straightforward based on the reproduced evidence.