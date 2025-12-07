# Contributing to Program Roadmaps

Thank you for your interest in contributing to Zindua School's program roadmaps! This document provides guidelines for contributing to this template repository and programs built with it.

## How to Contribute

There are several ways you can contribute:

1. **Improve the templates** - Enhance template structure and clarity
2. **Report issues** - Found a problem? Let us know
3. **Suggest improvements** - Have ideas for better organization?
4. **Share examples** - Contribute example programs or courses
5. **Fix errors** - Correct typos, broken links, or unclear instructions

## Getting Started

### For Template Improvements

1. **Fork the repository**
2. **Create a feature branch**
   ```bash
   git checkout -b feature/your-feature-name
   ```
3. **Make your changes**
4. **Test your changes** - Ensure templates are clear and well-formatted
5. **Submit a pull request**

### For Program-Specific Repositories

If you're contributing to a specific program roadmap (not the template):

1. **Review the program's structure** to understand the organization
2. **Follow the existing style** and formatting
3. **Keep content high-level** - Remember, we share structure not detailed content
4. **Focus on learning outcomes** and project specifications

## Contribution Guidelines

### What to Include

✅ **DO include:**
- Clear, concise descriptions
- Well-structured learning objectives
- Comprehensive topic lists
- Detailed project specifications
- Prerequisites and setup instructions
- Resource recommendations
- Assessment criteria (general)

❌ **DO NOT include:**
- Lecture notes or detailed lesson content
- Exercise solutions or answer keys
- Test questions and answers
- Proprietary or licensed materials
- Student work or submissions
- Internal grading details

### Style Guidelines

**Markdown Formatting:**
- Use proper heading hierarchy (H1 → H2 → H3)
- Use lists for enumeration
- Use tables for structured data
- Use code blocks for code examples or commands
- Use blockquotes for important notes

**Writing Style:**
- Be clear and concise
- Use active voice
- Write in present tense
- Be inclusive and welcoming
- Avoid jargon without explanation

**File Naming:**
- Use lowercase with hyphens: `my-file-name.md`
- Be descriptive but concise
- Follow the template naming conventions

### Template Structure

When modifying templates, maintain:
- Consistent section ordering
- Clear placeholders marked with `[brackets]`
- Helpful inline instructions
- Example content where appropriate

## Pull Request Process

1. **Describe your changes clearly**
   - What did you change?
   - Why did you make this change?
   - How does it improve the template/program?

2. **Link related issues** if applicable

3. **Ensure quality:**
   - Check for typos and grammatical errors
   - Verify all links work
   - Confirm markdown renders correctly
   - Test any instructions you've added

4. **Keep PRs focused** - One feature or fix per PR

5. **Be responsive** to review feedback

## Reporting Issues

When reporting an issue:

**For bugs or errors:**
- Describe what's wrong
- Specify which file(s) are affected
- Suggest a fix if you have one

**For enhancements:**
- Describe the improvement
- Explain the benefit
- Provide examples if helpful

Use the issue template if provided.

## Program Creation Guidelines

When creating a new program using this template:

### Initial Setup

1. **Copy or fork** the template repository
2. **Rename** to your program name
3. **Update README.md** with program details
4. **Create course directories** under `courses/`
5. **Add curriculum overview** in `CURRICULUM.md`

### Content Organization

**Directory Structure:**
```
program-name/
├── README.md              # Use PROGRAM_README.md template
├── CURRICULUM.md          # Use CURRICULUM.md template
├── courses/
│   ├── course-01-name/
│   │   ├── README.md     # Use COURSE_README.md template
│   │   ├── modules/
│   │   │   └── week-*.md # Use MODULE.md template
│   │   └── projects/
│   │       └── *.md      # Use PROJECT.md template
└── resources/
    └── *.md
```

### Quality Standards

**Completeness:**
- All template sections filled appropriately
- No placeholder text in final version (except examples)
- All internal links work correctly

**Clarity:**
- Learning objectives are specific and measurable
- Prerequisites are clearly stated
- Project requirements are detailed

**Consistency:**
- Similar formatting across all files
- Consistent terminology
- Uniform structure in similar sections

## Code of Conduct

### Our Standards

- Be respectful and professional
- Focus on constructive feedback
- Welcome newcomers and be patient
- Respect different viewpoints
- Accept responsibility for mistakes

### Unacceptable Behavior

- Harassment or discrimination
- Trolling or insulting comments
- Publishing others' private information
- Other unprofessional conduct

## Questions?

If you have questions about contributing:

- Open an issue for discussion
- Contact [maintainer-email]
- Join our community [community-link]

## License

By contributing, you agree that your contributions will be licensed under the same license as the project (MIT License).

---

**Thank you for contributing to Zindua School's open-source curriculum initiative!**
