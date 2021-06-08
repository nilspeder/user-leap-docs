# Skip Logic

## Skip Logic

Skip logic, like audience targeting, is a great way to better segment and ensure the right audience is displayed the right question. 

For example, imagine the following survey question: 

![](../../.gitbook/assets/screen-shot-2021-03-23-at-8.13.09-pm.png)

If the user answers with a **2**, it wouldn't make sense to follow up with: "What do you like most about the cut & paste feature in Google Docs?". 

Instead, you might consider some sort routing logic to only show a different question based on the response/response group. 

## **Skip Logic in UserLeap**

UserLeap supports skip logic for the following question types: 

* 1-5 Rating Scale
* Multiple Choice Single Select
* Multiple Choice Multi Select\*
* NPS 
* Open-end Response

\*_Multiple Choice Multi Select supports advanced skip logic_ 

see below for supported logic by question type

### 1-5 Rating Scale

![](https://lh5.googleusercontent.com/V37h6MSaWMNtROaXJ1WV0E7vcGzJnd26x0FcOdbQI_kFbrklYyZzNoHXeqxhRk-QFaCahhP-AUWrY55X-twRhtI2APo3cUIJj3l-Ul-JZhfEnPm4WQkw3ltlOsNtqzk76w0ULSKS)

**Logic Supported:**

1. is equal to 
2. is not equal to 
3. is less than
4. is less than or equal to
5. is greater than
6. is greater than or equal to
7. is submitted\*

_\*Is submitted is accepted when any value is selected by survey respondent_

### Multiple Choice Single Select

![](https://lh4.googleusercontent.com/wdkcAre5AHHwL_CsUg1lqLHGzFSYJOELf5_Wlpo85P98Hmylh61qRKlAS0SSTaLQGAnTaqrY07yGAHGYaDNheru-e24tw2tlpHbWim2k4ZXW2QQqZE1wRdqnb9bNlDQCazNGsjRw)

#### **Logic Supported:**

1. is equal to 
2. is not equal to 
3. is submitted\*

_\*Is submitted is accepted when any value is selected by survey respondent_

### **Multiple Choice Multi Select**

![](https://p35.tr2.n0.cdn.getcloudapp.com/items/Z4uodgQA/0325b441-47b8-424e-b347-1633d180c53a.gif?v=c732b5e617a6863fff773b8e5bdbd082)

#### **Logic Supported:**

* **is exactly:** evaluates to **TRUE** when respondent selects the **EXACT** options specified

| **Rule** | **Options** | **Result** |
| :--- | :--- | :--- |
| **Exactly \[a, b\]** | **\[a, b\]** | **true** |
| **Exactly \[a, b\]** | **\[a\]** | **false** |
| **Exactly \[a, b\]** | **\[a, b, c\]** | **false** |

* **includes all:** includes at least one: evaluates to **TRUE** when respondents select **one or more** options specified 

| **Rule** | **Options** | **Result** |
| :--- | :--- | :--- |
| **Includes all \[a, b\]** | **\[a, b\]** | **true** |
| **Includes all \[a, b\]** | **\[a\]** | **false** |
| **Includes all \[a, b\]** | **\[a, b, c\]** | **true** |

* **includes at least one:** includes all: evaluates to **TRUE** when respondents select **ALL** that are included within specified options 

| **Rule** | **Options** | **Result** |
| :--- | :--- | :--- |
| **Includes at least one \[a, b\]** | **\[a\]** | **true** |
| **Includes at least one \[a, b\]** | **\[a, b\]** | **true** |
| **Includes at least one \[a, b\]** | **\[a, b, c\]** | **true** |
| **Includes at least one \[a, b\]** | **\[c\]** | **false** |

{% hint style="danger" %}
If you have multiple matching rows of logic, for example: 

* **includes at least one** a or b = skip to 2
* **includes all** a and b = skip to 3

If the user selects **a and b**, they would be routed to question 2 The first set of logic that returns **TRUE** is accepted. In the example above, selecting **a** and **b** would activate the first set, before checking the second set
{% endhint %}

### **NPS**

![](https://lh5.googleusercontent.com/4AmILEGx3yWRVqUOatnqX-VxINq_MhL3PYq3c6Lbj8h43vu3GZP_jtJD_NsBCh1EeSTHh4V_SRVXqIs1Of5fUxAnJXiZbIla65NIombDHCJpzGo8l3_1N3cVUIC8on2Jr4jkOyfk)

**Logic Supported:**

1. is equal to 
2. is not equal to 
3. is less than
4. is less than or equal to
5. is greater than
6. is greater than or equal to
7. is submitted\*

_\*Is submitted is accepted when any value is selected by survey respondent_

### **Open-end Response**

![](https://lh5.googleusercontent.com/m5LYnmDHVcxZg9fKvc5ce2tcmOQNLrV_Uup9UIeIx8RQreeJY_Zb1P7rTN0V7iVE7D8TOGekirTL4X_1c0Q0yq_PU3yhENJ3BRpyurEqElCUenxPQAFDTveaIy5GSs2Ntp6xtvsZ)

**Logic Supported:**

1. is submitted\*

_\*Is submitted is accepted when any value is selected by survey respondent_



