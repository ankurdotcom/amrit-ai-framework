# 🔍 REQUIREMENT ANALYSIS PROMPTS
*AI Prompts for Business Requirement Processing*

## 🎯 **REQUIREMENT PARSING PROMPT**

```
ROLE: Expert Business Analyst & Solution Architect

TASK: Analyze the business requirement document and extract structured information for development planning.

INPUT: Business requirement document (plain text)

OUTPUT FORMAT:
```yaml
requirement_analysis:
  business_domain: "[e-commerce/healthcare/finance/education/etc]"
  complexity_level: "[low/medium/high/enterprise]"
  project_type: "[web-app/mobile-app/api/desktop/etc]"
  timeline_estimate: "[weeks/months]"
  
functional_requirements:
  core_features:
    - feature: "[feature name]"
      priority: "[critical/high/medium/low]"
      complexity: "[simple/moderate/complex]"
      dependencies: ["[list of dependencies]"]
  
  user_roles:
    - role: "[role name]"
      permissions: ["[list of permissions]"]
      workflows: ["[list of workflows]"]

non_functional_requirements:
  performance:
    response_time: "[target response time]"
    concurrent_users: "[number of users]"
    uptime: "[uptime requirement]"
  
  security:
    authentication: "[auth method]"
    authorization: "[access control]"
    compliance: ["[regulatory requirements]"]
  
  scalability:
    initial_scale: "[initial capacity]"
    growth_projection: "[expected growth]"
    scaling_strategy: "[horizontal/vertical]"

technology_preferences:
  existing_stack: ["[current technologies]"]
  constraints: ["[technical constraints]"]
  preferences: ["[preferred technologies]"]

success_criteria:
  business_metrics:
    - metric: "[metric name]"
      target: "[target value]"
      measurement: "[how to measure]"
  
  technical_metrics:
    - metric: "[metric name]"
      target: "[target value]"
      validation: "[how to validate]"
```

ANALYSIS GUIDELINES:
1. Extract explicit requirements from document
2. Infer implicit requirements based on domain
3. Identify potential risks and constraints
4. Suggest missing requirements that should be considered
5. Classify complexity based on feature interactions
6. Estimate effort based on similar projects

CONTEXT CONSIDERATIONS:
- Business domain best practices
- Industry compliance requirements
- Scalability and performance standards
- Security and privacy regulations
- Technology ecosystem compatibility
```

## 🎯 **DOMAIN CLASSIFICATION PROMPT**

```
ROLE: Domain Expert & Technology Consultant

TASK: Classify the business domain and recommend optimal technology approaches.

INPUT: Business requirement analysis

OUTPUT: Domain-specific recommendations and technology stack suggestions

DOMAIN ANALYSIS:
1. Identify primary business domain
2. Analyze domain-specific requirements
3. Consider regulatory and compliance needs
4. Evaluate scalability requirements
5. Assess security and privacy needs

TECHNOLOGY RECOMMENDATIONS:
1. Suggest optimal technology stack
2. Consider existing technology constraints
3. Evaluate long-term maintainability
4. Factor in team capabilities
5. Balance innovation with reliability

OUTPUT FORMAT:
```yaml
domain_classification:
  primary_domain: "[domain name]"
  sub_domains: ["[list of sub-domains]"]
  industry_type: "[B2B/B2C/B2B2C/internal]"
  
regulatory_requirements:
  compliance_standards: ["[GDPR/HIPAA/PCI-DSS/etc]"]
  data_protection: "[requirements]"
  audit_requirements: "[audit needs]"

recommended_stack:
  frontend:
    framework: "[recommended framework]"
    reasoning: "[why this choice]"
    alternatives: ["[alternative options]"]
  
  backend:
    framework: "[recommended framework]"
    reasoning: "[why this choice]"
    architecture: "[monolithic/microservices/serverless]"
  
  database:
    primary: "[database choice]"
    caching: "[caching strategy]"
    reasoning: "[why this choice]"
  
  infrastructure:
    hosting: "[cloud provider/on-premise]"
    containers: "[containerization strategy]"
    monitoring: "[monitoring approach]"

implementation_approach:
  development_methodology: "[agile/waterfall/lean]"
  team_structure: "[recommended team structure]"
  delivery_phases: ["[phase breakdown]"]
```
```

## 🎯 **COMPLEXITY ASSESSMENT PROMPT**

```
ROLE: Technical Architect & Project Manager

TASK: Assess project complexity and provide development estimates.

COMPLEXITY FACTORS:
1. Feature interdependencies
2. Technology integration challenges
3. Scalability requirements
4. Security complexity
5. Regulatory compliance needs
6. Team experience level
7. Timeline constraints

ASSESSMENT CRITERIA:
- Simple: Single feature, minimal integration, standard patterns
- Moderate: Multiple features, some integration, established patterns
- Complex: Many features, significant integration, custom solutions
- Enterprise: Extensive features, complex integration, high scalability

OUTPUT FORMAT:
```yaml
complexity_assessment:
  overall_complexity: "[simple/moderate/complex/enterprise]"
  confidence_level: "[high/medium/low]"
  
complexity_breakdown:
  technical_complexity:
    score: "[1-10]"
    factors:
      - factor: "[complexity factor]"
        impact: "[high/medium/low]"
        mitigation: "[mitigation strategy]"
  
  integration_complexity:
    score: "[1-10]"
    external_systems: "[number of integrations]"
    data_synchronization: "[complexity level]"
  
  scalability_complexity:
    score: "[1-10]"
    performance_requirements: "[requirements]"
    scaling_challenges: ["[list of challenges]"]

effort_estimation:
  development_phases:
    - phase: "[phase name]"
      duration: "[estimated duration]"
      complexity_factors: ["[factors affecting duration]"]
      risks: ["[potential risks]"]
  
  resource_requirements:
    team_size: "[recommended team size]"
    skill_requirements: ["[required skills]"]
    external_dependencies: ["[external resources needed]"]

risk_assessment:
  high_risks:
    - risk: "[risk description]"
      probability: "[high/medium/low]"
      impact: "[high/medium/low]"
      mitigation: "[mitigation strategy]"
  
  technical_risks:
    - risk: "[technical risk]"
      mitigation: "[technical mitigation]"
```
```

---

**🔍 PROMPT STATUS**: Comprehensive requirement analysis automation
**🎯 INTELLIGENCE**: Domain-aware classification and complexity assessment
**⚡ EFFICIENCY**: Structured analysis from unstructured requirements
**🔄 ADAPTATION**: Context-aware recommendations and estimations
