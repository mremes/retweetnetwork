# Social network analysis crawler
This is a Python 2.7 CLI utility for fetching tweeter-retweeter relationships based on a hashtag. The app takes care of making the calls into necessary endpoints to construct the resulting relationships and throttling the API requests.

The app was developed for a one-off purpose for this one specific use case. If you have any suggestions for further development or you want to report a bug, please do [open an issue](https://github.com/mremes/retweetnetwork/issues). You can contribute by [opening a pull request](https://github.com/mremes/retweetnetwork/pulls).
## Prerequisites
### Twitter API credentials
Twitter APIs that are used by the program need to be provided user-specific keys and secrets. These are provided to `envvars.txt` file in this format:
```
consumer_key=...
consumer_secret=...
access_token_key=...
access_token_secret=...
```
You can acquire the credentials from [Twitter Application Management](https://apps.twitter.com/).
### Python environment
I recommend using a [Python virtual environment](https://virtualenv.pypa.io/en/stable/). Then you simply do `pip install -r requirements` inside an active virtual environment.

After providing the credentials and installing the packages, you should be set up for running the tool.

## Usage
```
python app.py <hashtag> <# of tweets> <separator> <language code> <filter out not retweeted (True or False)>
```
You can also put arguments into `args.txt` file (for Windows GUI user convenience).

Running the program will result in a `results.csv` file containing the data in the following format:
```
tweeter,retweeter
user1,user2
...
```
