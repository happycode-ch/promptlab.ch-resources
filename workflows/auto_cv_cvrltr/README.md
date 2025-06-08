# Prompts Directory

This directory contains all AI prompts organized by workflow phase and purpose.

## Directory Structure

### Phase 1: Data Collection (`phase1-data-collection/`)
Prompts for building your personal data foundation:
- **`role_exploration_prompt.md`** - Extract structured data from past roles and experiences
- **`skills_inventory_prompt.md`** - Catalog and contextualize your skills and competencies

### Phase 2: Market Analysis (`phase2-market-analysis/`)
Prompts for analyzing job market signals:
- **`employer_signal_extractor.md`** - Extract key signals from job descriptions
- **`role_signal_profiler_prompt.md`** - Profile role patterns and requirements
- **`role_signal_outputs/`** - Directory containing example outputs and analysis results

### Phase 3: Content Generation (`phase3-content-generation/`)
Prompts for generating tailored CV and cover letter content:
- **`full_agent_system_prompt_test_17_04_2025.md`** - Comprehensive system prompt for content generation
- **`gpt_system_prompt.md`** - Core GPT system prompt for CV creation
- **`outreach_prompt_mini_cv_cvrltr.md`** - Generate concise CV and cover letter for outreach

### Evaluation (`evaluation/`)
Prompts for evaluating and optimizing generated content:
- **`ATSEvalAgent.md`** - Comprehensive ATS compatibility evaluation

## Usage Guidelines

### Sequential Workflow
1. Start with Phase 1 prompts to build your data foundation
2. Use Phase 2 prompts to analyze target roles and market signals
3. Apply Phase 3 prompts to generate tailored content
4. Utilize evaluation prompts to optimize and refine

### Customization
- Adapt prompts to your specific industry or role type
- Modify language and tone to match your personal style
- Add examples and context relevant to your experience level

### Best Practices
- Use consistent data formats across all prompts
- Keep personal data updated in `data/` directory
- Test prompts with different AI models to find optimal performance
- Document any customizations for future reference

## Integration with Data

These prompts are designed to work with the structured data in:
- `data/personal/` - Your personal skills, style, and experience data
- `data/roles/` - Role descriptions and professional portfolio
- `config/targeting/` - Industry and role targeting preferences

## Output Management

Generated content should be saved to:
- `outputs/generated/` - For current working documents
- `outputs/examples/` - For reference examples and templates 