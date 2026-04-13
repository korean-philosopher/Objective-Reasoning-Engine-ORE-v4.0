# Objective Reasoning Engine (ORE) v4.0

## 🧩 Overview
**ORE v4.0**은 대규모 언어 모델(LLM)을 고도의 **증거 기반 정책 및 전략 분석가(Evidence-Based Analyst)**로 변환하기 위한 프로덕션급 시스템 프롬프트 아키텍처입니다. 

단순한 텍스트 생성을 넘어, RAG(검색 증강 생성) 환경에서 발생하는 데이터 충돌을 해결하는 '증거 중재(Evidence Arbitration)' 로직과 시간의 흐름에 따른 구조적 변화를 분석하는 '시간축 전망(Temporal Forecast)' 엔진을 내장하고 있습니다.

**ORE v4.0** is a production-grade system prompt architecture designed to transform Large Language Models (LLMs) into sophisticated **Evidence-Based Policy and Strategy Analysts**.

Moving beyond simple text generation, it features a built-in "Evidence Arbitration" logic to resolve data conflicts occurring in RAG (Retrieval-Augmented Generation) environments, as well as a "Temporal Forecast" engine that analyzes structural changes over time.

## 🚀 Key Technical Features
- **Evidence Arbitration:** 출처 신뢰도 위계(정부 > 학술 > 산업 > 언론)를 기반으로 상충하는 정보를 스스로 판별.
- **Dynamic Routing:** 입력 쿼리의 성격에 따라 3가지 분석 모드(전략, 비교, 일반)로 출력 템플릿을 자율 전환.
- **Temporal Forecast Engine:** 단기(0-3), 중기(3-7), 장기(7-15) 구간별 구조적 변화 시뮬레이션.
- **Safety & Factuality:** '2-Factor Rule'과 '반사실적 사고(Counterfactual Logic)'를 통한 환각 통제 및 리스크 관리.

- * **Evidence Arbitration:** Independently evaluates conflicting information based on a hierarchy of source credibility (Government > Academic > Industry > Media).
- * **Dynamic Routing:** Autonomously switches output templates between three analysis modes (Strategic, Comparative, General) depending on the nature of the input query.
- * **Temporal Forecast Engine:** Simulates structural changes across specific timeframes: short-term (0–3 years), medium-term (3–7 years), and long-term (7–15 years).
- * **Safety & Factuality:** Controls hallucinations and manages risk through the "2-Factor Rule" and counterfactual logic.

## 🛠️ Implementation
본 프롬프트는 변수 주입이 가능한 API 환경(LangChain, Semantic Kernel 등)에서 최적의 성능을 발휘합니다.
1. `Objective Reasoning Engine (ORE) v4.0`을 시스템 프롬프트로 설정합니다.
2. `{{USER_QUERY}}`, `{{REFERENCE_DOCS}}` 변수를 통해 실시간 데이터 및 사용자 질의를 전달합니다.

This prompt delivers optimal performance in API environments that support variable injection (such as LangChain, Semantic Kernel, etc.).

1. Set `Objective Reasoning Engine (ORE) v4.0` as the system prompt.
2. Pass real-time data and user queries through the `{{USER_QUERY}}` and `{{REFERENCE_DOCS}}` variables.

## 📊 Case Study / 입출력 사례

### ❌ Input (User)

[ORE CONTEXT DECLARATION]

CURRENT_DATE: 2026-02-09

USER_QUERY: 법률 AI 등의 출현으로 변호사의 대규모 실직이 예상된다는 견해가 있다. 향후 5년 동안 한국 변호사 시장에 어떤 변화가 발생하는가?

REFERENCE_DOCS: 없음

----------------------------------------

[ANALYSIS REQUEST]

다음 요구 사항을 충족하여 분석하라:

1. 증거 중재 수행
- 상충되는 연구 또는 주장 비교
- 출처 신뢰도 평가 포함

2. 다차원 영향 분석 수행
- 경제
- 사회/제도
- 기술
- 정책/규제

3. 시간축 전망 수행
- 단기 (0~3년)
- 중기 (3~7년)
- 장기 (7~15년)
  
4. 반사실 시나리오 포함
- 핵심 변수 실패 또는 변화 상황 가정

5. 정량 데이터 사용 시
- 범위 / 기간 / 표본 / 방법론 중 최소 2개 설명

---

[ORE CONTEXT DECLARATION]

CURRENT_DATE: 2026-02-09

USER_QUERY: There are views suggesting that the emergence of Legal AI will lead to large-scale unemployment among lawyers. What changes will occur in the South Korean legal market over the next five years?

REFERENCE_DOCS: None

----------------------------------------

[ANALYSIS REQUEST]

Perform the analysis by fulfilling the following requirements:

1. Perform Evidence Arbitration
- Compare conflicting studies or claims
- Include evaluation of source credibility

2. Perform Multi-dimensional Impact Analysis
- Economy
- Society/Institution
- Technology
- Policy/Regulation

3. Perform Temporal Forecast
- Short-term (0–3 years)
- Medium-term (3–7 years)
- Long-term (7–15 years)

4. Include Counterfactual Scenarios
- Assume situations where key variables fail or change

5. When Using Quantitative Data
- Explain at least two of the following: Range / Duration / Sample Size / Methodology

### ✅ Output (Final Markdown Response)
```markdown
**ORE (AI-powered Policy Analysis) v4.0**
**Date:** 2026년 2월 9일
**Subject:** 법률 AI 확산에 따른 한국 법률 시장 5년 전망 및 변호사 고용 영향 분석

-----

### 1\. 쟁점 정의 (Issue Definition)

**"대규모 실직설 vs. 업무 증강설: 법률 AI의 한국적 특수성"**
사용자가 제기한 '대규모 실직' 우려는 법률 업무의 \*\*자동화 가능성(Exposure)\*\*과 \*\*실제 대체(Substitution)\*\*를 혼동한 데서 비롯됩니다. 한국 시장은 미국·영국과 달리 \*\*변호사법 제109조(비변호사의 법률 사무 금지)\*\*라는 강력한 진입 장벽이 존재하여, AI 자체가 변호사를 직접 대체하기 어려운 구조입니다. 따라서 향후 5년은 '변호사의 소멸'이 아니라, **'AI를 활용하는 변호사(Augmented Lawyer)'와 '그렇지 못한 변호사' 간의 극심한 양극화** 및 **주니어 변호사의 수련 기회 상실**이 핵심 쟁점이 될 것입니다.

-----

### 2\. 근거 및 출처 평가 (Evidence & Source Arbitration)

| 주장 유형 | 주요 출처 및 데이터 | 신뢰도 및 한국 적용성 평가 |
| :--- | :--- | :--- |
| **대규모 대체설**<br>(비관론) | **Goldman Sachs (2023):** 법률 업무의 44%가 AI 자동화에 노출.<br>**Princeton Univ. (2021):** AI 노출도(AIOE) 1위 산업으로 '법률 서비스' 지목. | **[제한적 적용]** 해당 연구는 '기술적 가능성'을 측정한 것으로, 규제 장벽을 고려하지 않음. 한국의 강력한 직역 수호 규제 하에서는 과대평가될 소지가 큼. |
| **업무 증강설**<br>(현실론) | **Thomson Reuters (2025):** AI는 대체가 아닌 생산성 도구. 변호사 1인당 연간 약 200\~240시간 절약 효과.<br>**MIT & Autor (2024):** 고숙련 직군은 완전 대체보다 업무 재조정(Task Reallocation) 발생. | **[높은 신뢰도]** 현재 한국 대형 로펌(김앤장, 태평양 등)의 내부 도입 현황과 일치함. 단순 업무는 AI가, 고부가가치 판단은 인간이 수행하는 추세. |
| **제도적 제약**<br>(한국 특수성) | **변호사법 제109조 및 대한변협 입장:** AI 법률 플랫폼에 대한 지속적 징계 및 견제 (로톡 사태 등).<br>**AI 기본법 (2026 시행):** 고위험 AI 규제 포함. | **[핵심 변수]** 기술이 있어도 제도가 확산을 지연시키는 '규제 댐(Regulatory Dam)' 역할을 수행 중. |

-----

### 3\. 다각적 영향 분석 (Multi-dimensional Impact)

#### **경제적 관점: 시장 양극화 (Bifurcation)**

  * **상위 10% (대형 로펌):** 고비용의 특화된 법률 AI(Legal LLM)를 자체 구축하거나 독점 계약하여 생산성을 30\~50% 향상시킵니다. 이는 수임료 경쟁력보다는 '서비스 속도와 정확도'의 격차를 벌립니다.
  * **하위 90% (개인/중소형):** 범용 AI(ChatGPT 등)를 활용하여 서면 작성 시간을 단축하겠지만, **수임료 하락 압박**에 직면합니다. 의뢰인이 "AI 쓰는데 왜 이렇게 비싸냐"고 반문하는 **'서비스 가격의 범용화(Commoditization)'** 현상이 발생합니다.

#### **노동/교육적 관점: 주니어 변호사의 위기**

  * **도제식 교육 붕괴:** 기존 신입 변호사가 수행하던 판례 검색, 초안 작성, 번역 업무를 AI가 대체합니다. 로펌은 신입 채용을 줄이고, **'즉시 전력감'인 3\~5년 차 경력직을 선호**하게 됩니다. 이로 인해 청년 변호사의 실업률이나 저임금 문제는 심화될 수 있습니다.

#### **사회/제도적 관점: 사법 접근성 vs 직역 갈등**

  * **리걸테크 갈등 심화:** AI가 작성한 고소장이나 내용증명이 저가에 공급되면서, 변호사 단체와 리걸테크 기업 간의 법적 공방(변호사법 위반 여부)이 지속될 것입니다.

-----

### 4\. 시간축 전망 (Temporal Forecast)

#### **단기 (0\~3년: 2026\~2028) - "도구 도입과 채용 빙하기"**

  * **현상:** 대형 로펌 중심으로 RAG(검색 증강 생성) 기반 내부 AI 시스템 구축 완료. 법원 행정처의 AI 사법 지원 시스템 시범 가동.
  * **노동 시장:** 신입 변호사 채용 규모 축소 가시화. 단순 송무 중심의 개인 변호사 소득 감소 시작.
  * **핵심 변화:** "AI를 다루는 능력(Legal Prompting)"이 채용의 우대 조건이 되기 시작하나, 아직은 보조적 수단에 머묾.

*(설명: 기존의 '피라미드형' 인력 구조(다수의 주니어-소수의 파트너)가 AI 도입 후 '다이아몬드형' 또는 '로켓형'(소수의 주니어-다수의 중견 전문가-AI 베이스)으로 변화하는 도표)*

#### **중기 (3\~7년: 2029\~2033) - "비즈니스 모델의 전환"**

  * **현상:** **시간당 청구(Billable Hours) 모델의 붕괴**. AI가 10분 만에 끝내는 일을 1시간 비용으로 청구할 수 없게 됨에 따라, **'가치 기반 과금(Value-based Pricing)'** 또는 \*\*'건당 정액제'\*\*가 보편화됨.
  * **시장 구조:** AI와 결합한 '부티크 로펌(전문 분야 소수 정예)'이 약진하며 중형 로펌을 위협.
  * **직무 변화:** 법률 지식과 데이터 엔지니어링을 겸비한 \*\*'리걸 엔지니어(Legal Engineer)'\*\*가 주요 직군으로 부상.

#### **장기 (7\~15년) - "구조적 재편"**

  * **현상:** 일반인도 AI 에이전트를 통해 소액 사건(나홀로 소송)을 수행하는 비중이 50%를 상회할 가능성. 변호사는 복잡한 전략 수립, 법정 변론, 감성적 의뢰인 케어(Human Touch)에만 집중.

-----

### 5\. 대안 시나리오 및 불확실성 (Scenarios & Uncertainty)

#### **시나리오 A: 갈라파고스화 (높은 확률)**

  * **가정:** 변호사법 규제가 완화되지 않고, 대한변협이 리걸테크를 강력히 제재함.
  * **결과:** 한국 법률 시장은 글로벌 흐름에서 고립. 국내 기업들은 해외 로펌이나 글로벌 컨설팅 펌(AI 무장)에 자문을 맡기며 국내 로펌의 시장 점유율 하락. 변호사 실직보다는 **'시장 전체의 파이 축소'** 발생.

#### **시나리오 B: 급진적 개방 (낮은 확률)**

  * **가정:** 정부가 AI 산업 육성을 위해 변호사법 예외를 인정하고 비변호사 법률 AI 허용.
  * **결과:** 변호사 자격증의 가치 급락. 하위 50% 변호사의 대규모 전직 사태 발생. 그러나 일반 국민의 법률 서비스 비용은 획기적으로 낮아짐.

### **결론 및 요약**

법률 AI로 인한 향후 5년의 변화는 \*\*'대규모 실직'보다는 '신규 진입의 장벽 상승'과 '소득 양극화'\*\*로 나타날 것입니다.

1.  **총 고용량:** 급격히 줄지 않으나, \*\*신입 채용(Junior)\*\*은 뚜렷하게 감소할 것입니다 (범위: 신입 채용 20\~30% 감소 예상).
2.  **생존 전략:** 단순히 법을 아는 것(Knowing the Law)에서 법을 다루는 도구를 지휘하는 것(Managing the Legal Tool)으로 역량을 전환해야 합니다.

-----

**Next Step:**
변호사 시험 합격자 수 변화 추이와 로스쿨의 AI 커리큘럼 도입 현황을 기반으로, \*\*"향후 3년간 로스쿨생을 위한 생존 전략"\*\*을 분석해 드릴까요?

---

**ORE (AI-powered Policy Analysis) v4.0**
**Date:** February 9, 2026
**Subject:** 5-Year Outlook for the Korean Legal Market and Analysis of Employment Impact Following the Proliferation of Legal AI

-----

### 1. Issue Definition

**"Mass Unemployment vs. Task Augmentation: The Korean Specificity of Legal AI"**
The "mass unemployment" concerns raised by users stem from confusing the **technical exposure** of legal tasks to automation with their **actual substitution**. Unlike the US or UK markets, South Korea possesses a high entry barrier through **Article 109 of the Attorney at Law Act (Prohibition of legal practice by non-lawyers)**, creating a structure where AI itself cannot directly replace lawyers. Therefore, the core issue over the next five years will not be the "disappearance of lawyers," but rather an **extreme polarization between "Augmented Lawyers" (those using AI) and those who do not**, along with the **loss of training opportunities for junior lawyers**.

-----

### 2. Evidence & Source Arbitration

| Claim Type | Key Sources & Data | Credibility & Korean Applicability Assessment |
| :--- | :--- | :--- |
| **Mass Substitution**<br>(Pessimism) | **Goldman Sachs (2023):** 44% of legal tasks exposed to AI automation.<br>**Princeton Univ. (2021):** Identified 'Legal Services' as the #1 industry for AI Occupation Exposure (AIOE). | **[Limited Applicability]** These studies measure 'technical feasibility' and do not account for regulatory barriers. Under Korea’s strict professional protection regulations, these claims are likely overestimated. |
| **Task Augmentation**<br>(Realism) | **Thomson Reuters (2025):** AI is a productivity tool, not a replacement. Saves approx. 200–240 hours per lawyer annually.<br>**MIT & Autor (2024):** High-skill occupations experience 'Task Reallocation' rather than total replacement. | **[High Credibility]** Aligns with the current internal adoption status at major Korean law firms (Kim & Chang, Lee & Ko, etc.). Trends show AI handling mundane tasks while humans perform high-value judgment. |
| **Institutional Constraints**<br>(Korean Specificity) | **Article 109 and KBA Position:** Continuous disciplinary actions and checks against AI legal platforms (e.g., LawTalk dispute).<br>**AI Framework Act (Enacted 2026):** Includes regulations on high-risk AI. | **[Key Variable]** Even if the technology exists, institutions act as a **"Regulatory Dam,"** delaying proliferation. |

-----

### 3. Multi-dimensional Impact

#### **Economic Perspective: Market Bifurcation**

* **Top 10% (Large Law Firms):** Will build proprietary Legal LLMs or sign exclusive contracts to improve productivity by 30–50%. This widens the gap in "service speed and accuracy" rather than fee competitiveness.
* **Bottom 90% (Solo/Small-to-Medium):** While they will use general-purpose AI (like ChatGPT) to shorten drafting time, they will face **downward pressure on legal fees**. A **'Commoditization of Service Pricing'** occurs as clients question high costs when AI is being utilized.

#### **Labor/Educational Perspective: The Crisis of Junior Lawyers**

* **Collapse of Apprenticeship Training:** AI replaces tasks traditionally performed by new associates, such as case law research, drafting, and translation. Law firms will reduce entry-level hiring, preferring **experienced associates (3–5 years)** who are "battle-ready." Consequently, unemployment or low-wage issues among young lawyers may intensify.

#### **Socio-Institutional Perspective: Access to Justice vs. Professional Conflict**

* **Intensifying Legal-Tech Conflict:** As AI-generated complaints or legal notices are supplied at low costs, legal battles between bar associations and legal-tech companies regarding violations of the Attorney at Law Act will persist.

-----

### 4. Temporal Forecast

#### **Short-term (0–3 years: 2026–2028) - "Tool Adoption and Hiring Ice Age"**

* **Phenomenon:** Major law firms complete internal RAG-based AI systems. Pilot operations of the AI judicial support system by the National Court Administration.
* **Labor Market:** Reduction in new lawyer recruitment becomes visible. Income for solo practitioners focused on simple litigation begins to decline.
* **Key Change:** "Legal Prompting" (AI proficiency) begins to appear as a preferred qualification in hiring, though it remains a supplementary tool.



#### **Medium-term (3–7 years: 2029–2033) - "Transformation of Business Models"**

* **Phenomenon:** **Collapse of the Billable Hours model**. As tasks AI completes in 10 minutes can no longer be billed as an hour's work, **'Value-based Pricing'** or **'Flat-rate per Case'** becomes the norm.
* **Market Structure:** "Boutique Law Firms" (small elite teams specialized in niche fields) combined with AI surge, threatening mid-sized firms.
* **Job Shift:** The **'Legal Engineer'**, possessing both legal knowledge and data engineering skills, emerges as a major job category.

#### **Long-term (7–15 years) - "Structural Realignment"**

* **Phenomenon:** The proportion of laypersons performing small-claims (pro se) litigation via AI agents may exceed 50%. Lawyers will focus exclusively on complex strategy formulation, courtroom advocacy, and the "Human Touch" (emotional client care).

-----

### 5. Scenarios & Uncertainty

#### **Scenario A: Galapagosization (High Probability)**

* **Assumption:** Regulations in the Attorney at Law Act are not eased, and the Bar Association continues to strongly suppress legal-tech.
* **Outcome:** The Korean legal market becomes isolated from global trends. Domestic companies turn to overseas firms or global consulting firms (armed with AI) for advice, leading to a loss of market share for domestic firms. Rather than mass unemployment, a **'reduction in the total market pie'** occurs.

#### **Scenario B: Radical Opening (Low Probability)**

* **Assumption:** The government grants exceptions to the Attorney at Law Act to foster the AI industry, allowing non-lawyer legal AI.
* **Outcome:** The value of the lawyer license plummets. A mass career-change event occurs for the bottom 50% of lawyers. However, legal service costs for the general public are drastically reduced.

### **Conclusion & Summary**

Changes over the next five years due to Legal AI will manifest as **"rising barriers to entry and income polarization" rather than "mass unemployment."**

1.  **Total Employment:** Will not drop sharply, but **Junior hiring** will see a distinct decrease (Range: 20–30% expected reduction in new hiring).
2.  **Survival Strategy:** Competency must shift from simply "Knowing the Law" to "Managing the Legal Tools" that command the law.

-----

**Next Step:**
Would you like me to analyze a **"Survival Strategy for Law Students over the next 3 years"** based on the trends in Bar Exam pass rates and the adoption of AI curricula in law schools?

```

## 🚀 How to Use / 사용 가이드 (Step-by-Step)

> 1.  **[ORE (Korean)]** 파일을 엽니다.
> 2.  전체 내용을 복사하여 Google AI Studio의 **System Instructions(시스템 프롬프트)** 란에 붙여넣습니다.
> 3.  'Grounding with Google Search'를 켭니다.
> 4.  규격화된 템플릿에 맞추어 질문합니다.

> 1. Open the **[ORE (English)]** file.
> 2. Copy the entire content and paste it into the **System Instructions** field of the Google AI Studio.
> 3. Turning on 'Grounding with Google Search'.
> 4. Ask questions according to a standardized template.

## 📜 License

**MIT License**
