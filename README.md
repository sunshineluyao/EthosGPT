# **EthosGPT: Charting the Human Values Landscape on a Global Scale**

![EthosGPT](EthosGPT.webp)

---

## **Project Overview**

In a world increasingly shaped by Large Language Models (LLMs), the need for these systems to align with diverse human values has never been greater. **EthosGPT** is an open-source framework designed to map and evaluate LLMs’ positioning across a multidimensional spectrum of human values, fostering cultural inclusivity and ethical adaptability.

Below is a sketch of flags from the 107 countries grouped by 8 cultural regions. This representation highlights the diversity of nations covered in EthosGPT.

<div align="center">
  <table>
    <thead>
      <tr>
        <th>African-Islamic</th>
        <th>Confucian</th>
        <th>Latin America</th>
        <th>Catholic Europe</th>
        <th>English-Speaking</th>
        <th>Orthodox Europe</th>
        <th>Protestant Europe</th>
        <th>West & South Asia</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <!-- African-Islamic Flags -->
        <td>
          <img src="https://flagcdn.com/w40/dz.png" title="Algeria" style="border-radius: 50%;"> 
          <img src="https://flagcdn.com/w40/eg.png" title="Egypt" style="border-radius: 50%;"> 
          <img src="https://flagcdn.com/w40/ng.png" title="Nigeria" style="border-radius: 50%;"> 
          <img src="https://flagcdn.com/w40/pk.png" title="Pakistan" style="border-radius: 50%;"> 
          <img src="https://flagcdn.com/w40/tn.png" title="Tunisia" style="border-radius: 50%;">
          ...
        </td>
        <!-- Confucian Flags -->
        <td>
          <img src="https://flagcdn.com/w40/cn.png" title="China" style="border-radius: 50%;"> 
          <img src="https://flagcdn.com/w40/jp.png" title="Japan" style="border-radius: 50%;"> 
          <img src="https://flagcdn.com/w40/kr.png" title="South Korea" style="border-radius: 50%;"> 
          <img src="https://flagcdn.com/w40/vn.png" title="Vietnam" style="border-radius: 50%;"> 
          <img src="https://flagcdn.com/w40/mo.png" title="Macau SAR" style="border-radius: 50%;">
          ...
        </td>
        <!-- Latin America Flags -->
        <td>
          <img src="https://flagcdn.com/w40/ar.png" title="Argentina" style="border-radius: 50%;"> 
          <img src="https://flagcdn.com/w40/br.png" title="Brazil" style="border-radius: 50%;"> 
          <img src="https://flagcdn.com/w40/cl.png" title="Chile" style="border-radius: 50%;"> 
          <img src="https://flagcdn.com/w40/co.png" title="Colombia" style="border-radius: 50%;"> 
          <img src="https://flagcdn.com/w40/mx.png" title="Mexico" style="border-radius: 50%;">
          ...
        </td>
        <!-- Catholic Europe Flags -->
        <td>
          <img src="https://flagcdn.com/w40/fr.png" title="France" style="border-radius: 50%;"> 
          <img src="https://flagcdn.com/w40/it.png" title="Italy" style="border-radius: 50%;"> 
          <img src="https://flagcdn.com/w40/es.png" title="Spain" style="border-radius: 50%;"> 
          <img src="https://flagcdn.com/w40/pt.png" title="Portugal" style="border-radius: 50%;"> 
          <img src="https://flagcdn.com/w40/pl.png" title="Poland" style="border-radius: 50%;">
          ...
        </td>
        <!-- English-Speaking Flags -->
        <td>
          <img src="https://flagcdn.com/w40/us.png" title="United States" style="border-radius: 50%;"> 
          <img src="https://flagcdn.com/w40/gb.png" title="United Kingdom" style="border-radius: 50%;"> 
          <img src="https://flagcdn.com/w40/ca.png" title="Canada" style="border-radius: 50%;"> 
          <img src="https://flagcdn.com/w40/au.png" title="Australia" style="border-radius: 50%;"> 
          <img src="https://flagcdn.com/w40/nz.png" title="New Zealand" style="border-radius: 50%;">
          ...
        </td>
        <!-- Orthodox Europe Flags -->
        <td>
          <img src="https://flagcdn.com/w40/ru.png" title="Russia" style="border-radius: 50%;"> 
          <img src="https://flagcdn.com/w40/ua.png" title="Ukraine" style="border-radius: 50%;"> 
          <img src="https://flagcdn.com/w40/gr.png" title="Greece" style="border-radius: 50%;"> 
          <img src="https://flagcdn.com/w40/by.png" title="Belarus" style="border-radius: 50%;"> 
          <img src="https://flagcdn.com/w40/ro.png" title="Romania" style="border-radius: 50%;">
          ...
        </td>
        <!-- Protestant Europe Flags -->
        <td>
          <img src="https://flagcdn.com/w40/de.png" title="Germany" style="border-radius: 50%;"> 
          <img src="https://flagcdn.com/w40/dk.png" title="Denmark" style="border-radius: 50%;"> 
          <img src="https://flagcdn.com/w40/se.png" title="Sweden" style="border-radius: 50%;"> 
          <img src="https://flagcdn.com/w40/fi.png" title="Finland" style="border-radius: 50%;"> 
          <img src="https://flagcdn.com/w40/nl.png" title="Netherlands" style="border-radius: 50%;">
          ...
        </td>
        <!-- West & South Asia Flags -->
        <td>
          <img src="https://flagcdn.com/w40/in.png" title="India" style="border-radius: 50%;"> 
          <img src="https://flagcdn.com/w40/id.png" title="Indonesia" style="border-radius: 50%;"> 
          <img src="https://flagcdn.com/w40/sa.png" title="Saudi Arabia" style="border-radius: 50%;"> 
          <img src="https://flagcdn.com/w40/bd.png" title="Bangladesh" style="border-radius: 50%;"> 
          <img src="https://flagcdn.com/w40/il.png" title="Israel" style="border-radius: 50%;">
          ...
        </td>
      </tr>
    </tbody>
  </table>
</div>

---



## **Key Features and Core Components**

### 🗺️ **Multidimensional Value Mapping**
- Visualize LLM performance across cultural and ethical dimensions using **comparative analyses of survey data and ChatGPT outputs.**

> **Example 1: Analyze cultural values through indices**  
> - **Traditional vs Secular-Rational Values**: A scale measuring the emphasis on tradition and authority versus secular and rational perspectives.  
> - **Survival vs Self-Expression Values**: A scale reflecting the shift from survival priorities to self-expression and quality-of-life concerns.

> **Example 2: Explore region-based discrepancies**  
> - Data normalized into z-scores for **107 countries/territories**, grouped into **8 cultural regions**:  
>   - **Regions include:** Confucian, Protestant Europe, Latin America, African-Islamic, etc.  
> - **Insights:**  
>   - The **Confucian region** exhibits the **highest discrepancies** in both indices.  
>   - **Protestant Europe and Latin America** exceed benchmarks for alignment differences.

---

### 🔍 **Prompt-Based Evaluation**
- Assess LLMs using structured prompts simulating responses of an "average individual" from specific countries or regions.

> **Example 1: Comparison with survey data**  
> - Compare ChatGPT's simulated cultural indices against **original survey data** (Haerpfer et al., 2022).  
> - **Strength:** Consistent alignment in secular-rational values for **English-Speaking regions** (e.g., USA, UK).  
> - **Weakness:** Underrepresentation of **self-expression values** in **African-Islamic regions** (e.g., Egypt, Morocco).

> **Example 2: Evaluate discrepancies using MSE analysis**  
> - **Mean Square Error (MSE)** identifies regions with significant deviations.  
> - **Benchmarks:**  
>   - Traditional vs Secular: ~0.4  
>   - Survival vs Self-Expression: ~0.6  
> - **Insights:**  
>   - Regions with **higher MSE (e.g., Confucian regions)** indicate larger deviations between ChatGPT predictions and survey data.

---


### 📊 **Interactive Data Tools**
- Analyze LLM outputs with advanced tools that foster cross-domain collaboration.
- Explore cultural diversity, alignment metrics, and biases via open-source visualizations.

<div align="center">
  <table>
    <tr>
      <td align="center">
        <img src="demo2.png" alt="Demo 1" width="400">
        <br>
        <strong>Interactive Visualization Demo 1</strong>
      </td>
      <td align="center">
        <img src="demo1.png" alt="Demo 2.1" width="400">
        <br>
        <strong>Interactive Visualization Demo 2.1</strong>
      </td>
    </tr>
    <tr>
      <td align="center">
        <img src="demo4.png" alt="Demo 2.2" width="400">
        <br>
        <strong>Interactive Visualization Demo 2.2</strong>
      </td>
      <td align="center">
        <img src="demo3.png" alt="Demo 3" width="400">
        <br>
        <strong>Interactive Visualization Demo 3</strong>
      </td>
    </tr>
  </table>
</div>

---

### 📊 **Interactive Data Tools**

<div align="center">
  <table>
    <thead>
      <tr>
        <th>Visualization</th>
        <th>Description</th>
        <th>Learning Opportunities</th>
        <th>Webpage</th>
        <th>Source Code</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td><strong>Cultural Values Comparison: Survey vs ChatGPT</strong></td>
        <td>Compare cultural value indices derived from human survey data with ChatGPT-generated responses.</td>
        <td>
          <ul>
            <li>Examine ChatGPT's alignment with cultural dimensions like individualism and power distance.</li>
            <li>Identify biases in AI outputs compared to human data.</li>
          </ul>
        </td>
        <td><a href="https://cultural-indices-dashboard.onrender.com/" target="_blank">Open App</a></td>
        <td><a href="https://github.com/sunshineluyao/cultural-indices-dashboard" target="_blank">GitHub Repo</a></td>
      </tr>
      <tr>
        <td><strong>Mean Square Error (MSE) Analysis by Region</strong></td>
        <td>Analyze the accuracy of ChatGPT’s cultural value predictions using MSE metrics.</td>
        <td>
          <ul>
            <li>Assess regional accuracy and identify areas for improvement.</li>
            <li>Compare ChatGPT's cultural representations across regions.</li>
          </ul>
        </td>
        <td><a href="https://culture-indices-mse.onrender.com/" target="_blank">Open App</a></td>
        <td><a href="https://github.com/sunshineluyao/culture-indices-mse" target="_blank">GitHub Repo</a></td>
      </tr>
      <tr>
        <td><strong>Cultural Values Map</strong></td>
        <td>Explore cultural value indices on an interactive global map.</td>
        <td>
          <ul>
            <li>Gain a visual understanding of global cultural indices.</li>
            <li>Compare ChatGPT's outputs with survey data across nations.</li>
          </ul>
        </td>
        <td><a href="https://culture-indices-map.onrender.com/" target="_blank">Open App</a></td>
        <td><a href="https://github.com/sunshineluyao/culture-indices-map" target="_blank">GitHub Repo</a></td>
      </tr>
    </tbody>
  </table>
</div>

---

## **How It Works**

1. **Prompt Input**  
   Carefully crafted prompts probe LLM responses across cultural and ethical contexts.

2. **Response Evaluation**  
   Alignment is measured using frameworks like Hofstede’s cultural dimensions.

3. **Visualization**  
   Results are displayed through intuitive visualizations to highlight strengths and biases.

---

## **Why EthosGPT?**

### 🌍 **Preserving Cultural Diversity**
- LLMs often risk reflecting dominant cultural biases, diminishing diversity.
- EthosGPT ensures inclusivity by highlighting cultural variances.

### ⚖️ **Ethical AI Alignment**
- Provides insights for developing socially and ethically aligned AI.

### 🔍 **Research-Driven Framework**
- Built on foundational studies like CVALUES and CultureLLM for robust cultural analysis.

---

## References

- Xu, G., Liu, J., Yan, M., et al. (2023). CVALUES: Measuring the Values of Chinese Large Language Models from Safety to Responsibility. [arXiv:2307.09705v1](https://arxiv.org/abs/2307.09705).
- Li, C., Chen, M., Wang, J., et al. (2024). CultureLLM: Incorporating Cultural Differences into Large Language Models. [arXiv:2402.10946v2](https://arxiv.org/abs/2402.10946).
- Kharchenko, J., Roosta, T., Chadha, A., & Shah, C. (2024). How Well Do LLMs Represent Values Across Cultures? [arXiv:2406.14805v1](https://arxiv.org/abs/2406.14805).
- Tao, Y., Viberg, O., Baker, R. S., & Kizilcec, R. F. (2024). Cultural Bias and Cultural Alignment of Large Language Models. [DOI:10.1093/pnasnexus/pgae346](https://doi.org/10.1093/pnasnexus/pgae346).
