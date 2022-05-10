# sg-bill-org-scraper
This is a web scraper to get Singapore Billing Organisations.

## Context

There are few places to find out Singapore Billing Organisations:
- https://www.posb.com.sg/personal/deposits/pay-with-ease/local-bill-payments/giro-payee-organisations.page
- https://e-station2.axs.com.sg/


In this project, I have chosen to scrape the POSB website because its DOM structure is easier :P

<details>
    <summary>Side note on AXS website<summary>

        I did attempt to scrape the AXS website initially, but you can check out the notebook to see how ugly the syntax has to be. The DOM structure is super strange (there's nested tables inside tables even though they look nothing like it)
    </details>

## Results

9 Categories, 104 Billing organisations found based on POSB website.

You can refer to `payees_with_category.xlsx` or `payees_with_category.csv`, whichever format you prefer. To use it in your project, you can either download the file locally, or you can fetch it at the raw file on GitHub.

