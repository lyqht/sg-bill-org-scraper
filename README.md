# sg-bill-org-scraper
This is a web scraper to get Singapore Billing Organisations. Scraping is performed with [RPA Python](https://github.com/tebelorg/RPA-Python) and [pandas](https://github.com/pandas-dev/pandas).

## Context

There are few places to find out Singapore Billing Organisations:
- https://www.posb.com.sg/personal/deposits/pay-with-ease/local-bill-payments/giro-payee-organisations.page
- https://e-station2.axs.com.sg/


In this project, I have chosen to scrape the POSB website because its DOM structure is easier :stuck_out_tongue:

<details>
<summary>Side note on AXS website for curious peeps</summary>

> I did attempt to scrape the AXS website initially, but you can check out the notebook to see how ugly the syntax has to be. The DOM structure is super strange (there's nested tables inside tables even though they look nothing like it 😆)
</details>

## Results

**9 Categories**, **104 Billing organisations** found.

An example:

| Billing Organisation |	Bill Reference Number |	Field Length |	Example |
| -- | -- | -- | -- |
|StarHub Ltd | Account No. with StarHub Ltd as displayed on your right hand corner of your bill | Numeric with decimals, ending with a letter. | Eg: 1.12345678A,Telecommunications and Utilities

You can refer to [payees_with_category.xlsx](./payees_with_category.xlsx) or [payees_with_category.csv](./payees_with_category.csv), whichever file format you prefer. 

### Using the data in your project

To use it in your project, you can either download the file locally, or you can fetch it at the [raw file on GitHub](https://raw.githubusercontent.com/lyqht/sg-bill-org-scraper/main/payees_with_category.csv).

An upcoming example will be added soon to the README!

## Setup instructions

If you want to try out the notebook, create your own venv and activate it. The activate command may differ depending if you're using Mac or other platforms.

```bash
python3 -m venv .venv
source .venv/bin/activate
```

Install the necessary packages

```
pip3 install -r requirements.txt
```

To start JupyterLab and see the notebook, run

```bash
jupyterlab
```