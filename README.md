# Credentials

* credentials.json: https://docs.gspread.org/en/latest/oauth2.html#for-bots-using-service-account

# ChatGPT Session

* https://chat.openai.com/c/70277a0e-e317-4b91-b38d-61ec9a69ac92

# big-eyes-to-sheet-ddg and Other DuckDuckGo API users

To avoid HTTP 403 rate limit, use the Tor browser

* Start "Tor Browser"
* Upstream also mentions iproyal.com residential proxiesa https://github.com/deedy5/duckduckgo_search#using-proxy

# https://github.com/topics/duckduckgo-api

* HTTP 403 Forbidden


```
  File "/Users/scottt/git/search-engine-automation/./bin/big-eyes-to-sheet-ddg", line 112, in search_bigeyes_articles_ddg
    result = list(ddgs.news('big eyes coin', region='wt-wt', safesearch='Off', timelimit=timelimit))
             ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "/Users/scottt/git/search-engine-automation/conda-env/lib/python3.11/site-packages/duckduckgo_search/duckduckgo_search.py", line 569, in news
    resp = self._get_url(
           ^^^^^^^^^^^^^^
  File "/Users/scottt/git/search-engine-automation/conda-env/lib/python3.11/site-packages/duckduckgo_search/duckduckgo_search.py", line 89, in _get_url
    raise ex
  File "/Users/scottt/git/search-engine-automation/conda-env/lib/python3.11/site-packages/duckduckgo_search/duckduckgo_search.py", line 83, in _get_url
    resp.raise_for_status()
  File "/Users/scottt/git/search-engine-automation/conda-env/lib/python3.11/site-packages/httpx/_models.py", line 749, in raise_for_status
    raise HTTPStatusError(message, request=request, response=self)
httpx.HTTPStatusError: Client error '403 Forbidden' for url 'https://duckduckgo.com/news.js?l=wt-wt&o=json&noamp=1&q=big%20eyes%20coin&vqd=4-221980983683420347283018166423795737405&p=-2&df=m&s=0'
For more information check: https://httpstatuses.com/403
```

# Google Sheet Count Sources

* https://stackoverflow.com/questions/74857270/list-all-unique-values-and-count-how-many-times-each-appears
