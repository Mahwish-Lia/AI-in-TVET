<!--
author: Mahwish Kanwal
email: mahwish.kanwal@ovgu.de
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

# Guidelines for Final Assessment

 

**Seminar:** AI in TVET I - Foundations and Applications  
    

**Assessment Type:**Real time Practice-Based 



**Submission Deadline:** 30.March.2026

__Format__: Digital, Individual 

**How to submit** Upload workable md files in your folders 

---

    --{{0}}--
This assessment challenges you to apply everything you've learned in this course to create something genuinely useful for TVET education while demonstrating critical thinking about AI's role in teaching and learning.

---

## 📋 Assessment Components


1) Design and develop a TVET focused Microcredential (Implementation ready prototype) using UNESCO's Teacher competency framework. Use Liascript and AI tools to develope the course content and assessment activities .

2) Documentation of Critical Reflection using EU guidance of Microcredential and UNESCO's Teacher competency frameowrk.
Acceptable formats : md files 

3) Use Talk as a discussion thread - Ask TWO content specific questions and Comment on any TWO questions raised by your peers.

---

## 🎓 Component 1: TVET Microcredential Course Design and Developement

### What You're Creating

Select a learning objective from UNESCO's AI Teacher's Competency Framework to design a **Microcredential course** thoughtfully integrating AI tools to achieve the learning objective.


#### Potential Indicators for Microcredential (EU Approach)


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





---

## 🤖 Component 2: Critical Reflection

### 4.1 What You're Creating

Transparent, critically reflected documentation of how you used AI tools throughout your microcredential design process—demonstrating both effective prompt engineering and critical evaluation of AI outputs.
Provide clear evidences of the alignment points with selected competency its respective curricular goal and learning outcome.


#### Example 1: Prompt Generation & Iteration (Example)

**Select any three significant prompting interactions** and provide deep documentation.

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

#### Example 2: Before/After Comparison

**Select any three  artifacts** from your microcredential and show the evolution from AI-generated to your final human-refined version.

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
---

**Good luck! I'm excited to see your innovative TVET microcredential designs! 🚀**

---

*This assessment brief is created with LiaScript—practice what we preach! View the source on GitHub to see how it's structured.*
