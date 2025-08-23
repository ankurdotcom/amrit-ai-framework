# 🚀 UNIVERSAL PROJECT INITIALIZATION PROMPT
*Amrit Framework - Foundation Phase*

## 🎯 **PROMPT OBJECTIVE**
Initialize any new project with Amrit framework standards, establishing foundation for AI-native, test-driven, premium-quality development.

## 📋 **INPUT REQUIREMENTS**
Before executing this prompt, gather:
- **Project Name**: Clear, descriptive project identifier
- **Business Domain**: Industry/sector context (e.g., e-commerce, documentation, analytics)
- **Core Requirements**: 3-5 primary business objectives
- **Target Users**: Primary user personas and their needs
- **Technology Preferences**: Any specific technology constraints or preferences
- **Performance Requirements**: Expected load, response times, availability
- **Budget Constraints**: Development and operational cost limitations

## 🔧 **EXECUTION PHASES**

### **Phase 1: Project Analysis & Planning**

#### **Task 1.1: Requirement Analysis**
```yaml
Objective: Transform business requirements into technical specifications
Process:
  1. Analyze business domain and competitive landscape
  2. Identify core user workflows and pain points
  3. Define measurable success criteria
  4. Prioritize features by business value and complexity
  5. Estimate resource and timeline requirements

Deliverables:
  - Requirements specification document
  - User persona definitions
  - Feature priority matrix
  - Success metrics definition
```

#### **Task 1.2: Technology Stack Selection**
```yaml
Objective: Choose optimal technology stack using Amrit criteria
Process:
  1. Apply Amrit technology selection matrix
  2. Evaluate options against AI-friendliness criteria
  3. Consider performance, cost, and maintenance factors
  4. Validate choices against project constraints
  5. Document technology decisions and rationale

Deliverables:
  - Technology stack specification
  - Architecture decision records (ADRs)
  - Performance and cost projections
  - Risk assessment and mitigation plans
```

### **Phase 2: Foundation Setup**

#### **Task 2.1: Repository and Environment Setup**
```yaml
Objective: Establish development environment and repository structure
Process:
  1. Create repository with Amrit-standard structure
  2. Configure development environment (Docker, CI/CD)
  3. Set up testing framework and quality gates
  4. Initialize monitoring and logging infrastructure
  5. Create deployment pipeline templates

Deliverables:
  - Configured repository with standard structure
  - Working development environment
  - CI/CD pipeline operational
  - Testing framework ready for TDD
```

#### **Task 2.2: Quality Framework Implementation**
```yaml
Objective: Implement comprehensive quality assurance framework
Process:
  1. Configure automated testing (unit, integration, E2E)
  2. Set up code quality tools (linting, formatting, analysis)
  3. Implement security scanning and OWASP compliance
  4. Configure performance monitoring and alerting
  5. Establish documentation standards and automation

Deliverables:
  - Complete testing framework
  - Quality gates and validation rules
  - Security compliance framework
  - Performance monitoring dashboard
```

### **Phase 3: AI Knowledge Integration**

#### **Task 3.1: Knowledge Management Setup**
```yaml
Objective: Establish project-specific AI knowledge system
Process:
  1. Initialize learning trackers and knowledge base
  2. Configure project-specific guardrails
  3. Set up troubleshooting and pattern tracking
  4. Integrate with Amrit framework knowledge
  5. Create automated knowledge update processes

Deliverables:
  - Project knowledge management system
  - AI-optimized documentation structure
  - Learning and pattern tracking mechanisms
  - Integration with Amrit framework knowledge
```

## ✅ **ACCEPTANCE CRITERIA**

### **Technical Foundation:**
- [ ] Repository structure follows Amrit standards
- [ ] Development environment fully operational
- [ ] CI/CD pipeline tests and deploys successfully
- [ ] All quality gates operational and validated
- [ ] Security framework passes OWASP compliance check

### **AI Optimization:**
- [ ] All documentation in AI-friendly format
- [ ] Knowledge management system operational
- [ ] Guardrails accessible and functional
- [ ] Troubleshooting framework ready for use
- [ ] Integration with Amrit framework complete

### **Quality Standards:**
- [ ] TDD framework ready for immediate use
- [ ] Performance monitoring baseline established
- [ ] Security scanning finds zero critical issues
- [ ] Documentation covers all setup and usage
- [ ] Cost projections within specified constraints

### **Premium Experience:**
- [ ] Professional development environment setup
- [ ] Polished documentation and user guides
- [ ] Efficient workflow and automation
- [ ] High-performance configuration validated
- [ ] User-focused design principles applied

## 🔍 **VALIDATION COMMANDS**

### **Environment Validation:**
```bash
# Verify development environment
docker --version && docker-compose --version
npm --version && node --version
git status

# Test CI/CD pipeline
git commit --allow-empty -m "test: CI/CD validation"
git push origin main

# Validate quality gates
npm run test
npm run lint
npm run security-check
npm run performance-test
```

### **Framework Integration:**
```bash
# Check Amrit framework integration
ls -la knowledge/
cat .amrit-config.yml
npm run amrit-validate

# Verify documentation
find docs/ -name "*.md" | wc -l
npm run docs-validate
```

## 🎯 **OUTPUT DELIVERABLES**

### **Project Foundation:**
1. **Repository**: Fully configured with Amrit standards
2. **Environment**: Development, testing, and deployment ready
3. **Pipeline**: Automated CI/CD with quality gates
4. **Documentation**: Comprehensive setup and usage guides

### **AI Integration:**
1. **Knowledge System**: Project-specific learning framework
2. **Guardrails**: Quality and security validation rules
3. **Patterns**: Initial pattern library for project domain
4. **Integration**: Connected to Amrit framework ecosystem

### **Quality Framework:**
1. **Testing**: TDD-ready framework with comprehensive coverage
2. **Security**: OWASP-compliant validation and monitoring
3. **Performance**: Baseline metrics and optimization targets
4. **Monitoring**: Operational dashboards and alerting

## 🔄 **NEXT STEPS**

After successful completion:
1. **Begin Feature Development**: Use `prompts/development/feature-implementation.md`
2. **Update Knowledge**: Document setup learnings in Amrit framework
3. **Validate Framework**: Confirm reusability for similar projects
4. **Optimize Process**: Enhance prompts based on execution experience

---

**🎯 PROMPT STATUS**: Ready for universal application  
**🔄 NEXT PROMPT**: `prompts/development/feature-implementation.md`  
**⏱️ ESTIMATED TIME**: 4-6 hours for complete foundation setup  
**🤖 AI OPTIMIZATION**: High - Designed for autonomous execution  

*Prompt Version: 1.0*  
*Last Updated: August 24, 2025*  
*Validated On: biz-dir-wiki project*
