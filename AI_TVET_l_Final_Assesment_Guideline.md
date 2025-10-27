<!--
author: UNESCO ASSET Team
email: asset-project@unesco.org
version: 1.0.0
language: en
narrator: UK English Female
comment: Self-Learning Nugget - Human-centered mindset: Human agency in AI for TVET education

link: https://raw.githubusercontent.com/OVGU-VET-TechEd/Integrating_AI_in_TVET_UNESCO/refs/heads/main/VorlageUN.css

@style
.unesco-header {
    background: linear-gradient(135deg, #0072CE 0%, #00A1DE 100%);
    color: white;
    padding: 2rem;
    margin: 1rem 0;
    border-radius: 15px;
    text-align: center;
    box-shadow: 0 8px 32px rgba(0,114,206,0.3);
}

.framework-card {
    background: #f8f9fa;
    border-left: 5px solid #0072CE;
    padding: 1.5rem;
    margin: 1rem 0;
    border-radius: 0 10px 10px 0;
}

.challenge-box {
    background: linear-gradient(45deg, #ff6b6b, #ffa726);
    color: white;
    padding: 1rem;
    border-radius: 10px;
    margin: 1rem 0;
    text-align: center;
}

.opportunity-box {
    background: linear-gradient(45deg, #4CAF50, #8BC34A);
    color: white;
    padding: 1rem;
    border-radius: 10px;
    margin: 1rem 0;
    text-align: center;
}

.case-study {
    background: #e3f2fd;
    border: 2px solid #0072CE;
    border-radius: 15px;
    padding: 1.5rem;
    margin: 1rem 0;
}

.policy-highlight {
    background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
    color: white;
    padding: 1rem;
    border-radius: 10px;
    margin: 0.5rem 0;
}

.interactive-element {
    background: #fff3e0;
    border: 2px dashed #ff9800;
    border-radius: 10px;
    padding: 1rem;
    margin: 1rem 0;
}

@end

@SpeechRecognition.support
<script modify="false" run-once>
// Vendor prefix
const SpeechRecognition = window.SpeechRecognition || window.webkitSpeechRecognition;
if (!SpeechRecognition) {
  "LIASCRIPT: > 'Speech Recognition' not supported in this browser. Try Chrome, Opera, or Edge.";
} else {
  "LIASCRIPT: > Your browser does support 'Speech Recognition' ..."
}
</script>
@end

@SpeechRecognition
<script>
// Vendor prefix
const SpeechRecognition = window.SpeechRecognition || window.webkitSpeechRecognition;
if (!SpeechRecognition) {
  alert('SpeechRecognition not supported. Try Chrome, Opera, or Edge.');
} else {
  const recognition = new SpeechRecognition();
  recognition.lang = '@0';
  recognition.interimResults = false;
  recognition.continuous = false;

  const solution = "@1".toLowerCase()
    .replace(/(\.|\?|\!|\,|\-|\;)/g," ")
    .replace(/[ ]+/g," ")
    .trim();

  recognition.onresult = ev => {
    let t = ev.results[0][0].transcript?.toLowerCase().trim() || '';
    if (t === solution) {
      send.lia("true");
    } else {
      send.lia("Please try again …",[],false);
    }
  };
  recognition.onerror = ev => send.lia("Error: "+ev.error,[],false);
  recognition.onend   = () => console.log('Speech recognition ended.');
  recognition.start();
}
"LIA: wait"
</script>
@end



@SpeechRecognition.withFeedback
<script>
// Vendor prefix
const SpeechRecognition = window.SpeechRecognition || window.webkitSpeechRecognition;
if (!SpeechRecognition) {
  alert('SpeechRecognition not supported. Try Chrome, Opera, or Edge.');
} else {
  const recognition = new SpeechRecognition();
  recognition.lang = '@0';
  recognition.interimResults = false;
  recognition.continuous = false;

  const solution = "@1".toLowerCase()
    .replace(/(\.|\?|\!|\,|\-|\;)/g," ")
    .replace(/[ ]+/g," ")
    .trim();

  recognition.onresult = ev => {
    let t = ev.results[0][0].transcript?.toLowerCase().trim() || '';
    if (t === solution) {
      send.lia("true");
    } else {
      send.lia(t,[],false);
    }
  };
  recognition.onerror = ev => send.lia("Error: "+ev.error,[],false);
  recognition.onend   = () => console.log('Speech recognition ended.');
  recognition.start();
}
"LIA: wait"
</script>
@end
-->

# AI in TVET I-Foundations & Applications

 __Guidelines for final Assessment__

**Course:** AI Foundations and Applications  
    

**Assessment Type:**Real time Practice-Based 



**Submission Deadline:** [Insert Date]

__Format__: Digital, Individual 

**How to submit**...

---

## 🎯 Assessment Overview

> **Your final task:** Design, develop, and pitch a TVET-focused AI-powered microcredential course while critically documenting your design process using UNESCO AI competancy framework for students and reflecting on your practice through the lens of UNESCO's AI Competency Framework for Teachers.

    --{{0}}--
This assessment challenges you to apply everything you've learned in this course to create something genuinely useful for TVET education while demonstrating critical thinking about AI's role in teaching and learning.

---

## 📋 Assessment Components

| Components | Description |
|-----------|-------------|
| **1. Launching a TVET focused Microcredential (Implementation ready prototype)** | Design a microcredential using EU approach. Use Liascript and AI tools to develope the course content and assessment activities as Learning Nuggets|
| **2. LiaScript Pitch Presentation** | 15-minute interactive presentation pitching your microcredential |
| **3. Digital Badge Design (Optional)** | Professional badge with Open Badges-compliant metadata|
| **4. AI Co-Design Documentation & Reflection Paper** | Transparent documentation of AI tool usage in design process & Critical reflection using UNESCO's AI Teacher's Competency Framework (1000-1500 words) |



---

## 🎓 Component 1: TVET Microcredential Course Design and Developement

### What You're Creating

Select a Curricular Goal from UNESCO's AI Students"s Competency Framework to design a **Microcredential course** that addresses a specific skill gap in a TVET sector of your choice, thoughtfully integrating AI tools to enhance learning outcomes.

>Deliverable: Liascript markdown files for all learning nuggets.





#### Suggested Format for Microcredential (EU Approach)


| **Field** | **Description** |
|------------|-----------------|
| **1. Identification** |  |
| Identification of Recipient | Name of the individual receiving the certification. |
| Supervision and Verification of Identity | Type of identity verification during the course and evaluation (e.g., unsupervised, supervised online/in-person with identity verification). |
| Name of the Micro-credential | Title or denomination of the university micro-credential. |
| Issuing University | The university or universities offering the micro-credential. |
| Entity for Learning Experience | If different from the issuing university, name of the organization or institution where the learning occurs. |
| **2. Description of the Learning Experience** |  |
| Start and End Date | The beginning and completion dates of the educational activity. |
| Language | Language of instruction. |
| Admission Requirements | Prerequisites for access and criteria for admission (e.g., level of prior education or knowledge). |
| Learning Objectives | Clearly defined objectives based on the target audience and the purpose of the training. |
| Content Description | Detailed description of the educational content. |
| Mode of Instruction | In-person, online, or hybrid. |
| Learning Outcomes | Expected learning outcomes and type of achievement (e.g., skills, knowledge, competencies). |
| Level of Experience | Qualification level as per frameworks like EQF, MECU, or MECES. |
| Competency Frameworks | Competency frameworks used (e.g., ESCO, DIGCOMP, or others). |
| Learning Activities | Types of learning activities (theoretical and practical). |
| Workload (Theoretical) | Volume of theoretical work required to achieve the learning outcomes (in ECTS and hours, if applicable). |
| Workload (Practical) | Volume of practical work required to achieve the learning outcomes (in ECTS and hours, if applicable). |
| **3. Assessment and Certification** |  |
| Assessment Methods | Type of assessments validating learning outcomes (e.g., skill application, video presentation, portfolio). |
| List of Trainers | Qualifications and professional experience of trainers. |
| Stackability Options | Possibility of integration with other micro-credentials (independent, integrated, stackable). |
| Outcome or Rights for the Student | Resulting credential, badge, program admission, or qualification earned. |
| Quality Assurance | Type of quality assurance or validation procedure used. |
| Certifying University | The legal name, mandatory legal identifier, and country/region of the university issuing the certification. |
| Date of Issue | Date on which the micro-credential is issued. |




## 🎤 Component 2: LiaScript Pitch Presentation 

### What You're Creating

A **10-minute interactive presentation** created in LiaScript that pitches your microcredential to a simulated TVET institution decision-making panel (provost, curriculum director, industry partners).




## 🎖️ Component 3: Digital Badge Design

### What You're Creating

A **professional digital badge** with complete metadata that could actually be issued to learners who complete your microcredential, following Open Badges 3.0 standards.

### Why Digital Badges?

- Portable, verifiable credentials
- Stackable micro-credentials
- Rich metadata about skills and competencies
- Integration with digital portfolios, LinkedIn, etc.
- Growing recognition by employers


#### 3.1 Visual Badge Design 

**Technical specifications:**

- Format: SVG (preferred) or PNG
- Size: Square, minimum 512×512 pixels
- File size: Under 256KB
- Design principles:
  - Recognizable at small sizes (as small as 64×64px)
  - Incorporates TVET sector identity
  - Professional appearance
  - Accessible (sufficient color contrast, not text-dependent)
  - Unique and memorable

**Design tips:**

- Use sector-relevant iconography (e.g., wrench for trades, stethoscope for healthcare)
- Consider using your institution's colors
- Include symbolic AI element if appropriate
- Keep it simple—overly complex designs don't scale well
- Test at multiple sizes

**Tools you can use:**

- Canva (free templates available)
- Figma (professional design tool)
- Adobe Illustrator
- Inkscape (free, open-source)


#### 3.3 Evidence Requirements for badge earner 

**What evidence must badge earners provide?**



- **Assessment artifacts required:** What must learners submit?

  - Examples: portfolio, video demonstration, project, case study, etc.
- **Performance standards:** What quality level must be achieved?
- **Verification process:** How will evidence be reviewed and validated?
- **Timeline:** When must evidence be submitted?
- **Appeals process:** What if learner disagrees with assessment?



### Helpful Resources

- [Open Badges Specification](https://www.imsglobal.org/spec/ob/v3p0/)
- [Badgr Platform](https://badgr.com/)
- [Credly Platform](https://www.credly.com/)
- [ESCO Skills Taxonomy](https://esco.ec.europa.eu/)
- [O*NET Skills Database](https://www.onetonline.org/)

---

## 🤖 Component 4: AI Co-Design Documentation & Reflection

### 4.1 What You're Creating

Transparent, critical documentation of how you used AI tools throughout your microcredential design process—demonstrating both effective prompt engineering and critical evaluation of AI outputs.

Deliverable: Word doc... or pdf(1k-1.5k)

#### 4.1.1 AI Integration Plan 

**Document where, how, and why you're integrating AI**

For Example See the table below:

| Integration Point | AI Tool/Type | Pedagogical Purpose | Expected Outcome | Ethical Considerations |
|-------------------|--------------|---------------------|------------------|------------------------|
| Example: Module 2, Activity 1 | ChatGPT for scenario generation | Learners practice troubleshooting with AI-generated realistic scenarios | Improved diagnostic reasoning in varied contexts | Ensure scenarios reflect diverse workplaces, not biased |

#### 4.1.2 AI Tools Log 

**Comprehensive record of ALL AI tool usage** during your project.



| Date | Session # | Tool Used | Specific Purpose | Input/Prompt Summary | Output Summary | Your Evaluation | What You Kept/Changed |
|------|-----------|-----------|------------------|----------------------|----------------|-----------------|----------------------|
| Oct 15 | 1 | ChatGPT-4 | Generate learning objectives | "Create learning objectives for welding safety module" | 6 objectives listed, mostly knowledge-level | Too generic, not TVET-specific, wrong Bloom's level | Used framework but rewrote all 6 to focus on application |
| Oct 17 | 2 | Claude | Develop assessment rubric | [Insert actual prompt] | Detailed 4-level rubric | Excellent structure but missing TVET context clues | Kept structure, added industry-specific criteria |

**Minimum entries:** 10-15 significant interactions

**Include:**

- Content generation (objectives, activities, scenarios)
- Assessment design
- Instructional materials development
- Proofreading or editing
- Research or idea generation
- Badge design elements (if AI-assisted)
- Any other AI usage

**Be thorough and honest—this is about transparency and learning, not perfection.**

#### 4.1.3 Prompt Generation & Iteration

**Select any-one significant prompting interaction** and provide deep documentation.

**For each interaction, include:**

1. **Context:** What were you trying to accomplish?
2. **Initial Prompt:** Your first attempt (exact text)
3. **AI Response:** Summary or relevant excerpt
4. **Your Critique:** What worked? What didn't? Why?
5. **Iteration(s):** How did you refine your prompt? (show 1-3 iterations)
6. **Final Outcome:** What did you ultimately use in your microcredential?
7. **Reflection:** What did this teach you about prompting or AI capabilities?

**Example format:**

---

**Prompt Engineering Example #1: Developing Authentic Scenarios**

**Context:**  
I needed a realistic workplace scenario for my automotive diagnostics module where learners practice troubleshooting electrical issues.

**Initial Prompt (Iteration 1):**  
```
Create a scenario for automotive electrical troubleshooting.
```

**AI Response:**  
*Claude generated a basic scenario about a car with a dead battery. It was generic and didn't require diagnostic reasoning—just "check the battery."*

**My Critique:**  

- Too simplistic—no real troubleshooting needed
- Not authentic to professional automotive practice
- Didn't specify learner level or learning objectives
- Missing complexity that would require systematic diagnosis

**Refined Prompt (Iteration 2):** 

```
You are an automotive TVET instructor. Create an intermediate-level troubleshooting scenario where a customer's vehicle has intermittent electrical issues. The scenario should require systematic diagnostic procedures and could have multiple possible causes. Include: customer complaint, initial symptoms, and vehicle information. Do NOT include the solution—learners should diagnose it.

```

**AI Response:**  
*Much better! Claude created a scenario with intermittent starting issues, multiple symptoms, and ambiguous clues requiring systematic testing. More realistic and challenging.*

**My Critique:**

- ✅ Appropriate complexity level
- ✅ Requires systematic approach
- ✅ Authentic customer language
- ⚠️ Could use more red herrings
- ⚠️ Make vehicle specifications more specific (year, make, model)

**Final Refinement (Iteration 3):**  

[Your refined prompt building on iteration 2...]


**Final Outcome:**  
I used the scenario from iteration 3 with minor modifications: I added specific vehicle details (2018 Honda Accord), included a red herring (customer mentioned oil change last week), and adjusted the symptom pattern to match real-world intermittent electrical faults I've seen.

**Reflection/Learning:**  

Effective prompts for TVET scenarios require:

- Role specification ("you are a TVET instructor")
- Level/audience clarity
- Structure requirements (what to include/exclude)
- Authenticity cues (customer language, real-world complexity)
- Multiple iterations to refine

AI is excellent at structure but needs human expertise to ensure technical accuracy and authentic workplace context.

---






#### 4.1.4 Before/After Comparison

**Select any one  artifacts** from your microcredential and show the evolution from AI-generated to your final human-refined version.

**For each artifact:**

1. **Original AI-Generated Version:** Show what the AI produced
2. **Your Final Version:** Show what you actually used
3. **Annotated Explanation:** Use comment bubbles, highlights, or side-by-side notes explaining:

   - What you changed
   - Why you changed it
   - What this reveals about AI capabilities/limitations

**Suggested artifacts to compare:**

- Learning objectives (before/after)
- Assessment rubric (before/after)
- Scenario or case study (before/after)
- Instructional content section (before/after)
- Assessment task description (before/after)
- clear visual comparison (tables, side-by-side, annotation)


#### 4.2.1 Competency Mapping Table 

**Create a table mapping your work to UNESCO competencies:**

| UNESCO Competency | Evidence from My Work | How This Demonstrates Competency | Depth of Engagement |
|-------------------|----------------------|----------------------------------|---------------------|
| AI Pedagogy 2.1: Design AI-enhanced learning activities | Module 2, Activity 3 used ChatGPT for scenario generation, with learner scaffolding | Demonstrated purposeful integration where AI adds pedagogical value, not decoration | ⭐⭐⭐⭐ |
| AI Ethics 1.2: Address bias in AI systems | AI Documentation Essay, section on bias | Identified gender bias in AI-generated nursing scenarios, deliberately diversified examples | ⭐⭐⭐⭐⭐ |

**Include at least 2-4 competencies** across multiple framework areas.

**Depth ratings:**

- ⭐⭐⭐⭐⭐ Deep engagement, sophisticated application
- ⭐⭐⭐⭐ Strong engagement, clear application
- ⭐⭐⭐ Moderate engagement, developing application
- ⭐⭐ Surface engagement, basic awareness
- ⭐ Minimal engagement

### Depth of Engagement 

```markdown
# Example

**Pedagogical Design (25%)**

- ⭐⭐⭐⭐⭐ Excellent: Exemplary alignment, sophisticated TVET pedagogy, adult learning principles expertly applied
- ⭐⭐⭐⭐ Very Good: Strong alignment, appropriate pedagogy, clear TVET context
- ⭐⭐⭐ Good: Adequate alignment, basic TVET appropriateness
- ⭐⭐ Developing: Some gaps in alignment or pedagogical sophistication
- ⭐ Beginning: Significant issues with alignment or TVET appropriateness

**AI Integration Quality (25%)**

- ⭐⭐⭐⭐⭐ Excellent: Purposeful, innovative AI use; deep critical analysis; comprehensive ethics
- ⭐⭐⭐⭐ Very Good: Appropriate AI use; good rationale; ethics addressed
- ⭐⭐⭐ Good: Competent AI integration; basic rationale
- ⭐⭐ Developing: Superficial or decorative AI use
- ⭐ Beginning: Inappropriate or absent AI integration

**TVET Authenticity (25%)**

- ⭐⭐⭐⭐⭐ Excellent: Deeply authentic to workplace; industry-relevant; transferable skills
- ⭐⭐⭐⭐ Very Good: Authentic scenarios; clear workplace connection
- ⭐⭐⭐ Good: Reasonable workplace relevance
- ⭐⭐ Developing: Limited authenticity; somewhat abstract
- ⭐ Beginning: Disconnected from real TVET contexts

**Completeness & Quality (25%)**

- ⭐⭐⭐⭐⭐ Excellent: Comprehensive, polished, ready-to-implement
- ⭐⭐⭐⭐ Very Good: Complete with minor refinements needed
- ⭐⭐⭐ Good: All elements present; needs development
- ⭐⭐ Developing: Missing elements or significant gaps
- ⭐ Beginning: Incomplete or poor quality
```

---

#### 4.2.2 Critical Reflection Narrative  

Write structured reflection using UNESCO's AI Competency Framework for Teachers, specifically focusing on AI pedagogy.













---








## 🔄 Assessment Version & Updates

**Version:** 1.0.0 

**Last Updated:** [Date]     

**Changes:** Initial release

Any updates to this assessment brief will be announced via [communication channel] and updated in this document with version tracking.

---

**Good luck! I'm excited to see your innovative TVET microcredential designs! 🚀**

---

*This assessment brief is created with LiaScript—practice what we preach! View the source on GitHub to see how it's structured.*

