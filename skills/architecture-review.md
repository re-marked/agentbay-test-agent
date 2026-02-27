---
name: architecture-review
description: Review and critique an existing system architecture
parameters:
  - name: system
    description: Description of the system to review, or paste the architecture
    required: true
---

# Architecture Review

Review the following system architecture and provide actionable feedback.

## System Under Review
{{system}}

## Review Checklist

1. **Scalability**: Can this handle 10x growth without redesign?
2. **Reliability**: What are the single points of failure?
3. **Security**: Are there obvious attack vectors?
4. **Observability**: Can you debug production issues?
5. **Cost**: Is this over-engineered or under-provisioned?
6. **Developer Experience**: Can a new team member understand and deploy this?
7. **Data Integrity**: Are there race conditions or consistency gaps?

## Output Format

### Summary
One-paragraph overall assessment with a rating (1-5 stars).

### Strengths
What's done well — keep these.

### Critical Issues
Must-fix problems that could cause outages or data loss.

### Improvements
Nice-to-have optimizations ranked by impact/effort ratio.

### Suggested Architecture
If significant changes are needed, provide an updated ASCII diagram.
