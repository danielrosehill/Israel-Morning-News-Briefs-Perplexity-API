[Perplexity home page![light logo](https://mintlify.s3.us-west-1.amazonaws.com/perplexity/logo/SonarByPerplexity.svg)![dark logo](https://mintlify.s3.us-west-1.amazonaws.com/perplexity/logo/Sonar_Wordmark_Light.svg)](https://docs.perplexity.ai/home.mdx)

Search docs

Ctrl K

Search...

Navigation

Sonar Deep Research

[Home](https://docs.perplexity.ai/home) [Guides](https://docs.perplexity.ai/guides/getting-started) [API Reference](https://docs.perplexity.ai/api-reference/chat-completions) [Changelog](https://docs.perplexity.ai/changelog/changelog) [System Status](https://docs.perplexity.ai/system-status/system-status) [FAQ](https://docs.perplexity.ai/faq/faq) [Roadmap](https://docs.perplexity.ai/feature-roadmap) [Discussions](https://docs.perplexity.ai/discussions/discussions)

_A powerful research model capable of conducting exhaustive searches, synthesizing expert-level insights, and generating detailed reports._

- **Model Type**: Deep Research / Reasoning
- **Use Case**: Perfect for conducting exhaustive research into topics and generating reports with highly detailed analyses/insights.
- **Context Length**: 128k

**Key Features:**

- Exhaustive research across hundreds of sources
- Expert-level subject analysis
- Detailed report generation

**Real-World Examples:**

- Writing white papers for industry thought leadership
- Crafting highly detailed go-to-market (GTM) plans
- Creating educational content for universities or training programs

* * *

## [​](https://docs.perplexity.ai/guides/models/sonar-deep-research\#pricing)  **Pricing**

| Pricing Component | Cost |
| --- | --- |
| **Input Tokens (Per Million)** | **$2** |
| **Reasoning Tokens (Per Million)** | **$3** |
| **Output Tokens (Per Million)** | **$8** |
| **Price per 1,000 Requests** | **$5** |

* * *

## [​](https://docs.perplexity.ai/guides/models/sonar-deep-research\#test-the-model)  **Test the Model**

cURL

python

Copy

```bash
curl --request POST \
  --url https://api.perplexity.ai/chat/completions \
  --header 'Authorization: Bearer <token>' \
  --header 'Content-Type: application/json' \
  --data '{
  "model": "sonar-deep-research",
  "messages": [\
    {"role": "user", "content": "Provide an in-depth analysis of the impact of AI on global job markets over the next decade."}\
  ],
  "max_tokens": 500
}'

```

**Sample Response Metadata**

Copy

```json
{
  'id': 'a2f2ce2d-7b7e-48f8-8b56-4509d39e1937',
  'model': 'sonar-deep-research',
  'created': 1743529939,
  'usage': {'prompt_tokens': 19, 'completion_tokens': 1313, 'total_tokens': 1332, 'citation_tokens': 9478, 'num_search_queries': 10},
  'citations': ['https://www.nexford.edu/insights/how-will-ai-affect-jobs', 'https://technologymagazine.com/articles/wef-report-the-impact-of-ai-driving-170m-new-jobs-by-2030', 'https://ijgis.pubpub.org/pub/gdfpmgv9', 'https://builtin.com/artificial-intelligence/artificial-intelligence-future', 'https://www.innopharmaeducation.com/blog/the-impact-of-ai-on-job-roles-workforce-and-employment-what-you-need-to-know', 'https://explodingtopics.com/blog/ai-replacing-jobs', 'https://www.weforum.org/stories/2023/09/ai-automation-augmentation-workplace-jobs-of-tomorrow/', 'https://news.stthomas.edu/generative-ais-real-world-impact-on-job-markets/', 'https://litslink.com/blog/how-many-jobs-will-ai-take-over-the-statistics', 'https://institute.global/insights/economic-prosperity/the-impact-of-ai-on-the-labour-market', 'https://www.sandtech.com/insight/ai-and-the-future-of-work/', 'https://www.epi.org/press/the-pressing-threat-to-workers-isnt-ai-its-unbalanced-employer-power-in-the-labor-market/', 'https://sustainabilitymag.com/articles/wef-report-the-impact-of-ai-driving-170m-new-jobs-by-2030', 'https://www.nexford.edu/insights/how-will-ai-affect-jobs', 'https://jfsdigital.org/wp-content/uploads/2017/01/JFS212Final%EF%BC%88%E5%B7%B2%E6%8B%96%E7%A7%BB%EF%BC%89-6.pdf', 'https://www.chicagobooth.edu/review/ai-is-going-disrupt-labor-market-it-doesnt-have-destroy-it'],
  'object': 'chat.completion',
  'choices': [{'index': 0,\
  'finish_reason':\
  'stop',\
  'message': {'role': 'assistant',\
  'content': "<think>\nOkay, I need to tackle this query about the impact of AI on global job markets over the next decade. Let's start by going through the search results to gather the main points. \n\nFirst, the Goldman Sachs report mentions that AI could replace 300 million jobs, but also lead to a productivity boom and a 7% increase in global GDP. That's a big number, so job displacement is a major point. Then there's the WEF report from 2025 predicting 170 million new jobs against 92 million displaced, resulting in a net gain. This seems optimistic but highlights the transformative nature of AI.\n\nAnother source from IJGIS in May 2024 talks about a 40% displacement vs. 60% creation ratio. That's another figure supporting job creation over loss. However, some sectors like manufacturing and administrative roles are more at risk, according to Nexford and the University of Pennsylvania/OpenAI study, which points out white-collar workers earning up to $80k might be affected. \n\nMcKinsey's data in the search results mentions that by 2030, 14% of workers might need to switch careers. Also, the EPI report warns about the imbalance of power between employers and workers, suggesting policies are crucial. Skills gaps and the need for upskilling come up repeatedly, especially in the WEF and Siemens AG mentions. Judith Wiese's comment about skills becoming outdated quickly is key here.\n\nLooking at industries, the WEF notes that tech is leading in AI adoption, while construction lags. Countries like the US, China, Japan, and Germany are leading in robotics. Regional disparities are a concern, with lower adoption in low-income economies. \n\nThe impact isn't uniform across demographics. The EPI report says women are more exposed to AI displacement due to skill gaps. Also, younger workers worry more about job obsolescence than older ones. \n\nOn the positive side, roles in AI training, data analysis, cybersecurity, and ethics are emerging. The Tony Blair Institute breaks down AI's impact into labor demand, supply, and workplace experience, which is a useful framework. \n\nI also need to mention the potential for AI to augment jobs, like in insurance underwriting or healthcare, where it can handle routine tasks, allowing humans to focus on complex issues. The EPI's emphasis on policy solutions like strengthening unions and social safety nets should be included to balance the discussion.\n\nPutting it all together, the answer should cover displacement vs. creation, sector-specific impacts, skills and upskilling, economic effects, regional variations, and policy recommendations. Make sure to cite the relevant sources, like Goldman Sachs for the 300 million jobs, WEF for the 170 million new jobs, McKinsey for the 14% career change, etc. Highlight the conflicting views—some reports are optimistic about job creation, others warn about displacement and inequality. Conclude with the need for proactive policies and education to navigate the transition.\n</think>\n\nAI's impact on global job markets through 2035 will be profound and multifaceted, characterized by both significant displacement and unprecedented opportunity. Key analyses from leading institutions reveal several critical trends:\n\n### Job Displacement vs. Creation\n1. **Automation Scale**:  \n   - 300 million jobs globally (equivalent to 9% of current roles) face automation risk, primarily affecting routine white-collar tasks like credit analysis (81% automatable) and administrative support[1][8][14].  \n   - **Net gains** are expected, with the World Economic Forum (WEF) forecasting **170 million new jobs** (e.g., AI trainers, cybersecurity specialists) outweighing **92 million displaced roles**[2][13].  \n   - Sector ratios show **40% displacement vs. 60% creation**, driven by AI-enabled productivity boosts (potentially adding $7 trillion to global GDP)[3][16].\n\n2. **Industry-Specific Risks**:  \n   - **High-risk sectors**: Manufacturing (12 million jobs at risk by 2030), office/administrative roles (46% automatable)[9][6].  \n   - **Growth sectors**: Healthcare, STEM, and creative industries will see demand for AI ethicists (+72% augmentation potential) and human-machine teaming managers[5][7].\n\n### Workforce Transformation\n3. **Skill Evolution**:  \n   - **39% of current skills** will become obsolete by 2030, with AI literacy, data analytics, and adaptability becoming critical[2][11].  \n   - White-collar professionals earning up to $80,000 annually face the highest automation exposure, while roles requiring empathy (nursing) or creativity (art direction) gain augmentation potential[1][7].\n\n4. **Economic and Demographic Disparities**:  \n   - Advanced economies will see **60% job disruption** vs. 26% in low-income nations, exacerbating global inequality[6][10].  \n   - Women face disproportionate risks due to AI skill gaps and higher representation in clerical roles[4][12].\n\n### Systemic Shifts\n5. **Corporate Adaptation**:  \n   - **86% of businesses** expect AI-driven restructuring by 2030, with 85% prioritizing workforce upskilling[11][13].  \n   - Hybrid human-AI collaboration models will dominate, shifting task allocation from 47% human-operated today to near-even splits with machines by 2030[11].\n\n| Key AI Job Market Dynamics (2025-2035) |  \n|----------------------------------------|  \n| **Global GDP Growth** | +7% ($7T) |  \n| **Prime Displacement Targets** | White-collar roles, manufacturing |  \n| **Emerging Roles** | AI ethics specialists, data engineers |  \n| **Critical Skills Gap** | Analytics, cybersecurity, AI-augmented creativity |  \n\n### Policy Imperatives\nTo mitigate disruptions, the WEF and Economic Policy Institute emphasize:  \n- **Education reform**: Lifelong learning systems to address 85 million midcareer transitions[7][12].  \n- **Labor protections**: Updated regulations for AI ethics and strengthened collective bargaining[12][15].  \n- **Economic safeguards**: Universal basic income pilots and expanded social safety nets[12][15].\n\nWhile AI will eliminate certain roles, historical parallels (e.g., 60% of 2025 jobs didn’t exist in 1940) suggest adaptability remains achievable[16]. Success hinges on balancing automation gains with equitable access to emerging opportunities."},\
  'delta': {'role': 'assistant', 'content': ''}}]
}

```