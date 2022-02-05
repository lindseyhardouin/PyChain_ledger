# PyChain_ledger

This blockchain based application allows users to conduct financial transactions via Streamlit, a user-friendly interface. Additionally, it allows users to verify the integrity of the data in the ledger.
---

## Technologies

This project leverages python 3.7. It utilizes the following packages:

**[Pandas Library Python](https://pandas.pydata.org/)** - a fast, powerful, flexible and easy to use open source data analysis and manipulation tool.<br>

**[Streamlit Library Python](https://streamlit.io/)** -  turns data scripts into shareable web apps in minutes.<br>

**Dataclasses Library Python** - provides a decorator and functions for automatically adding generated special methods such as __init__() and __repr__() to user-defined classes. <br>

**Typing Library Python** - provides runtime support for type hints. <br>

**Datetime Library Python** - supplies classes for manipulating dates and times.<br>

**Hashlib Library Python** - implements a common interface to many different secure hash and message digest algorithms.<br>


---

## Installation Guide

Before running the application, install the following dependencies:

1) To install the Streamlit library, confirm your dev virtual environment is active, and then run the following command:

```python
pip install streamlit
```

---

## Usage

To use the application, clone the repository and run the **pychain.py** file in streamlit with the following code:

```python
streamlit run pychain.py
```

![Streamlit Interface](images/st.PNG)


---

## Evaluation Summary

The app creates a baseline trading algorithm. The baseline algorithim utilizes an SVM model with test dataset of three months, and short and long SMA windows of 4 and 100 respectively. Then, the baseline is tuned and adjusted as described below:

   1. The model compared test results using two different test timeframe slices of three months and six months, begining April 20, 2015. While the strategy using the longer timeframe initially does not produce returns greater than that of the actuals, in the longrun they greatly outperform the returns of the actuals and of the shorter timeframe strategy. Therefore, the bot was adjusted to utilize the longer test dataset.

   2. The model compared test results using different SMA periods. By increasing the SMA short and long windows from 4 & 100 to 20 & 150, the returns decreased. Ultimately, the increase in SMA windows resulted in returns below that of the actual returns. Therefore, the original windows of 4 & 100 are utilized in this bot. 

   The visualizations below compare the baseline algorthim to the tuned algorithm, as described in the section above:

   Baseline:

  
   
Next, using the baseline model, a Logistic Regression classifer was used and compared to the SVM model. Comparison shows the SVM model outperforms the Logistic Regression model. As shown below, the Logistic Regression model produces substandard returns. Therefore, it is recommended to implement the SVM classifier in this case.

   LR:

  
---

 
## Contributors

**Contributor:** Lindsey Hardouin<br>
**Email Address:** lindseyhardouin@gmail.com<br>