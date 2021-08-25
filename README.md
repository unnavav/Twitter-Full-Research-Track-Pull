# Twitter Full Research Track Pull
This code will enable academic researchers with access to the full archive search on twitter to pull data without the Tweepy package, which doesn't presently support full-archive search with academic access. The code is quite simple, but relies on two text files.

## Authentication

One simply needs to put their Twitter API access keys into a .txt file located in whereever they prefer in the directory. The file path location to modify is in ```line 37``` of the code.

In the text file, simply write the following, with your API access codes inputtted:

```
API_Key [your_api_key]
API_Secret_Key [your_api_secret_key]
Bearer_Token [your_bearer_token]
```

For clarity's sake, I note that there should be no brackets in the actual `.txt` file.

## Keywords

With this code, it's possible to do searches of multiple queries. This again, is stored in a .txt file and is called in `line 51` of the code. There's no obligation to do this, but is helpful for when you are searching multiple terms over the same time period.

In your text file, simply list all the keywords, without commas, on separate lines:

```
hello
world
```

If there are no keywords inputted, the query defauls to "the -the", a generalized search attempting to pull a random sample of tweets, as per [this community solution here](https://twittercommunity.com/t/generating-a-random-set-of-tweet-ids/150255). 

To add additional query speicifications, a full list of available search specifications is available through [Twitter's API here](https://developer.twitter.com/en/docs/twitter-api/tweets/search/api-reference/get-tweets-search-all).

## Outputs

The tweets results are output as a `.csv` file, saved whereever one prefers. This can be modified on `line 179` of the code.

## Running the code

This part is simple. Modify anything else that you would wish to; feel free to contact me on twitter or through email if there's anything in particular unclear about the functions. Then run the code from the command line. This code is written in Python 3 and should be called using the `python3` command.
