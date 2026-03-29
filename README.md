# Project Live On
# Our Mission
At the heart of every societal challenge lies awareness. Our mission is to empower individuals by providing clear, actionable insights about the issues affecting their communities, and to guide them toward resources that can make a real impact on their lives. By transforming data into understanding, we aim to foster informed communities capable of driving meaningful change.

## Key Features

**Interactive County Map:**  
Explore your zipcode through a live, dynamic map. Hover over any zipcode to reveal the three most significant local problems, allowing users to quickly understand the key challenges in their area.

**AI-Powered Insights:**  
Integrated AI generates concise, informative summaries of notable disparities in each county. Users can also compare local ZIP codes to the highest life expectancy ZIP code, offering a perspective on health and social outcomes relative to the rest of the nation.

**Personal Risk Assessment:**  
Positioned in the top-right corner, this tool provides a detailed, personalized evaluation and highlights local resources where users can seek help tailored to their specific needs.

**Prioritizing Awareness:**  
The first step is educating users about the realities in their communities. The map and aggregated data serve as the foundation for informed decision-making and awareness.

**Connecting Users to Support:**  
The next step focuses on linking users with local services, organizations, and programs that address their identified needs, providing tangible pathways to assistance.

**Driving Actionable Change:**  
Finally, the platform empowers users to take concrete action, whether through advocacy, community engagement, or accessing the resources they need, creating a cycle from awareness to intervention to long-term impact.

## How we Calculate Risk
We compare 14 metrics of health and quality of life to each other to result in a simple, single number that summarizes the overall health equity of that zipcode.\
Our 14 factors are as follows, in order of importance, followed by their weights in our calculation.<br>
<p><strong>&nbsp;&nbsp;&nbsp;&nbsp;1</strong>. Life Expectancy (10%)</p>
<p><strong>&nbsp;&nbsp;&nbsp;&nbsp;2</strong>. Blood Pressure (9%)</p>
<p><strong>&nbsp;&nbsp;&nbsp;&nbsp;3</strong>. Poverty Rate (9%)</p>
<p><strong>&nbsp;&nbsp;&nbsp;&nbsp;4</strong>. Uninsured Rate (8%)</p>
<p><strong>&nbsp;&nbsp;&nbsp;&nbsp;5</strong>. Disability (8%)</p>
<p><strong>&nbsp;&nbsp;&nbsp;&nbsp;6</strong>. Checkup Rate (8%)</p>
<p><strong>&nbsp;&nbsp;&nbsp;&nbsp;7</strong>. No Leisure Activity (7%)</p>
<p><strong>&nbsp;&nbsp;&nbsp;&nbsp;8</strong>. Poor Physical Help (7%)</p>
<p><strong>&nbsp;&nbsp;&nbsp;&nbsp;9</strong>. Social Vulnerability Index (6%)</p>
<p><strong>&nbsp;&nbsp;10</strong>. Depression (6%)</p>
<p><strong>&nbsp;&nbsp;11</strong>. Smoking (6%)</p>
<p><strong>&nbsp;&nbsp;12</strong>. Mental Health (6%)</p>
<p><strong>&nbsp;&nbsp;13</strong>. Food Insecurity (5%)</p>
<p><strong>&nbsp;&nbsp;14</strong>. High Cholesterol (5%)</p><br>
The above metrics are normalized for each zipcode to avoid major skew caused by greatly differing sample sizes.The aid scores are then calculated with: <br><br>

$score = \frac{\sum_{i=1}^{n} (normalized\ value_i\ \cdot\ weight_i)}{\sum_{i=1}^{n} weights\ of\ available\ factors_i} \times 100$
<br><br>
They are then assigned a severity tier,
* 75-100&nbsp;→ Critical
* 55-74 &nbsp;&nbsp;→ High
* 35-54 &nbsp;&nbsp;→ Moderate
* 0-34 &nbsp;&nbsp;&nbsp;&nbsp;→ Low
