# Biased Echoes: Large Language Models Reinforce Investment Biases and Increase Portfolio Risks of Private Investors

With this directory we provide all data collection, analysis code, and raw data associated with our research project. Each study follows a consistent structure:

1.  **Data Collection** (*1_collection\_*): Code that prompts LLMs.

2.  **Data Preparation** (*2_preparation\_*): Code that transforms the financial advice from LLMs into a long format.

3.  **Investment Risk Analysis** (*3_biases\_*): Code that analyzes the long format LLMs financial advice for investment risks.

4.  **Language Style Analysis** (*4_sentiments\_*): Ancillary code that conducts a language style analysis on the LLMs response raw data.

5.  **Financial Performance Analysis** (*5_performance\_*): Ancillary code that conducts a financial performance analysis of LLMs financial advice from the long format data.

6.  **Data Files** (*data*/*processed* directory): Contains both raw and processed LLM financial advice data.

You can generate all figures and perform the entire analysis by simply executing the analysis sections of the code files (utilizing the saved calculated features), without the need for additional data collection.

**Note:** Given the uniform structure across all studies, method descriptions are only included in the Study 1 code files.

## Execution Hints

### Data Collection (*1_collection\_*)

In case you want to collect your own financial advice from LLM you need to execute this file. It prompts the LLM and saves the raw data. You need to set your OpenAI API key to the environment variable `OPENAI_API_KEY`[^readme-1].

[^readme-1]: In case of Study 1 you also needed to save your Bing cookie in the `./bing_cookies_export.json` file (follow the instructions of the EdgeGPT package) and get the cookie ID of Google Bard for the Bard API package. Both packages are outdated by now and no additional data can be collected from Google Gemini and Microsoft Copilot as it was originally done in this project).

### Data Preparation (*2_preparation\_*)

Only run this script if you want to extract the individual portfolio positions from LLM financial advice.

### Investment Risk Analysis (*3_biases\_*)

Execute this script if you want to determine the magnitude of investment risks inherent in LLM financial advice by loading the prepared LLM financial advice data set and secondary data.

### Language Style Analysis (*4_sentiments\_*)

Skip the `Feature Engineering` section of the script if you would like to skip to the language style analysis directly without running the zero-shot classification models on the raw data.

### Financial Performance Analysis (*5_performance\_*)

Skip the `Fetching performance data & calculating performance measures` section of the script if you would like to skip to the performance analysis directly without fetching and calculating performance data from the prepared LLM financial advice data.
