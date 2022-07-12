# 18-blockchain-based-ledger-system

In this challenge, I assumed the role of the lead developer on the decentralized finance team at one of the largest banks in the world. My task was to build a blockchain-based ledger system, complete with a user-friendly web interface. This ledger allows partner banks to conduct financial transactions (that is, to transfer money between senders and receivers) and to verify the integrity of the data in the ledger.

To accomplish this goal, I updated a basic PyChain ledger structure as follows:

(1) Created a new data class named Record. This class served as the blueprint for the financial transaction records that the blocks of the ledger stored.
(2) Changed the existing Block data class by replacing the generic data attribute with a record attribute that’s of type Record.
(3) Created additional user input areas in the Streamlit application. These input areas should collect the relevant information for each financial record that you’ll store in the PyChain ledger.
(4) Tested the complete PyChain ledger.

## Installation Guide

The following package needs to be installed into the development environment.

```python
!pip install streamlit
!pip install dataclasses
```
---

## Technologies

This project leverages python 3.7 with the following libraries and dependencies:

* [pandas](https://github.com/pandas-dev/pandas) - For manipulating data

* [streamlit](https://github.com/streamlit/streamlit) - The fastest way to build and share data apps.

---

### **Step 1: Created a Record Data Class**

Defined a new Python data class named Record. Gave this new class a formalized data structure that consists of the sender, receiver, and amount attributes. To do so, I completed the following steps:

(1) Defined a new class named `Record`.
(2) Added the `@dataclass` decorator immediately before the `Record` class definition.
(3) Added an attribute named `sender` of type `str`.
(4) Added an attribute named `receiver` of type `str`.
(5) Added an attribute named `amount` of type `float`.

Note that you’ll use this new `Record` class as the data type of your `record` attribute in the next section.

### **Step 2: Modified the Existing Block Data Class to Store Record Data**

Renamed the `data` attribute in the Block class to record, and then set it to use an instance of the new `Record` class created in the previous section. To do so, I completed the following steps:

(1) In the Block class, renamed the data attribute to record.
(2) Set the data type of the record attribute to Record.
    
### **Step 3: Added Relevant User Inputs to the Streamlit Interface**

Coded additional input areas for the user interface of your Streamlit application. Created these input areas to capture the sender, receiver, and amount for each transaction stored in the `Block` record. To do so, I completed the following steps:

(1) Deleted the `input_data` variable from the Streamlit interface.
(2) Added an input area where you can get a value for `sender` from the user.
(3) Added an input area where you can get a value for `receiver` from the user.
(4) Added an input area where you can get a value for `amount` from the user.
(5) As part of the Add Block button functionality, updated `new_block` so that Block consists of an attribute named `record`, which is set equal to a `Record` that contains the `sender`, `receiver`, and `amount` values. The updated `Blocks` also include the attributes for `creator_id` and `prev_hash`.

### **Step 4: Test the PyChain Ledger by Storing Records**

Tested complete PyChain ledger and user interface by running Streamlit application and storing some mined blocks in the PyChain ledger. Then tested the blockchain validation process by using the PyChain ledger. To do so, I completed the following steps:

(1) In the terminal, navigated to the project folder where I coded the Challenge.
(2) In the terminal, ran the Streamlit application by using `streamlit run pychain.py`.
(3) Entered values for the sender, receiver, and amount, and then clicked the Add Block button. Did this several times to store several blocks in the ledger.
(4) Verified the block contents and hashes in the Streamlit drop-down menu. Took a screenshot of the Streamlit application page, detailing a blockchain that consists of multiple blocks. See the following:

* ![cumulative_return_plot_1](cumulative_return_plot_3.png) 

(5) Tested the blockchain validation process by using the web interface. Took a screenshot of the Streamlit application page, which should indicate the validity of the blockchain. See the following:

* ![cumulative_return_plot_1](cumulative_return_plot_3.png) 

---
## Contributors

Brought to you by Wilson Rosa. https://www.linkedin.com/in/wilson-rosa-angeles/.

---
## License

MIT