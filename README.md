# Gephi TwitterStreamingImporter Media Downloader

This small Python script takes a .csv export generated by the fantastic
[TwitterStreamingImporter Plugin](https://github.com/seinecle/gephi-tutorials/blob/master/src/main/asciidoc/en/plugins/twitter-streaming-importer-en.adoc) identifies
the tweets and then downloads the embedded media including...

* Photos
* Videos
* Animated Gifs

The script will also generate a report, allowing quick matching back to
your original CSV.

This script was created at the request of the AOIR Digital Methods Workgroup.

## Instructions
### I use Python / I know what I'm doing...
Great! This script requires [Tweepy](http://www.tweepy.org) and was
written in Python 3.6.
1. Download the script
2. Ensure your gephi export .csv is in the same folder as the script
3. Edit the `credentials.py` file so that...

        CONSUMER_KEY = 'YOUR_KEY'
        CONSUMER_SECRET = 'YOUR_SECRET'
4. Run `pip install -r requirements.txt`
5. Run `python download_twitter_media.py`
6. Follow the on-screen instructions

### I don't use Python / I don't know what I'm doing...
Not a problem, this script is for people like you!

##### 1. Install your Python Environment
**NOTE: If you already have Miniconda / Anaconda installed on your
machine, skip this step**.

Install either [Anaconda](https://www.anaconda.com/distribution/#download-section)
 or [Miniconda](https://docs.conda.io/en/latest/miniconda.html) to give yourself an up to date Python environment
that is seperate from any native environments on your machine.


If installing Anaconda you want...
* Python 3
* 64bit Graphical Installer

If installing Miniconda you want...
* Python 3
* most likely 64bit
* .pkg installer if you are on MacOS

**What's the difference?**
Anaconda is better overall for beginners as it comes preloaded with a lot of packages and
a GUI to launch different tools. If you want to get more into Python in the future
I'd recommend Anaconda. However it is also a large download so if bandwidth
or hard disk space is an issue, go for Miniconda.

##### 2. Download this package
* Download by clicking the green 'Clone or download' button above, and choose
'Download ZIP'.
* Unzip the package if necessary.
* You should have a folder called 'gephi_twitter_media_downloader-master'

##### 3. Edit the credentials file (optional - do once)
**This is an optional step. if you do not complete step 3 the script will ask you
for your API keys later. Completing step 3 saves you time on repeated uses.**
* You will need your Consumer Key and Consumer Secret from the Twitter API.
You would have generated these when you set up the Gephi plugin.
* Open the 'credentials.py' file using a regular text editor such as Notepad, Textedit
or something better like [Sublime Text](https://www.sublimetext.com).
* Once opened you will see the following...

        CONSUMER_KEY = ''
        CONSUMER_SECRET = ''
* Copy/paste your keys into the file so that it looks something like this (quote marks included)...

        CONSUMER_KEY = '5dsfgsd6dg8dshdg7g'
        CONSUMER_SECRET = 'is88wudndu84740010jf455634ghHNJKHSD66s86dgf'
* Save the file ensuring it still ends with `.py`

##### 4. Copy in your Gephi Export
* Create your .csv by opening your Gephi project, going to the Data Laboratory
and clicking Export Table. Save the file as a .csv into the same folder as this script.

##### 5. Open up the folder in a Command Line
**On Mac**
* [Open up the Terminal](https://www.wikihow.com/Open-a-Terminal-Window-in-Mac).
* Type `cd` and then drag and drop the folder onto the terminal window. This
will automatically add in the full path to your folder.
* Hit return.

**On Windows**
* Open the folder containing the script.
* Hold down shift on your keyboard and right-click inside the folder.
* On the menu, click `Open command windows here`.

##### 6. Install Package Requirements (NOT OPTIONAL - do once)
Before we can use the script we need to ensure your Python environment has
the packages the script uses. Whether you installed Anaconda or Miniconda
this step is required, but only once.

* In your command line type

        pip install -r requirements.txt

* You will see a lot of text run past and hopefully will be presented
with an empty command prompt at the end.

##### 7. Quick Checklist
* At this point you should be in a command prompt. On the left it should have the name of the
folder containing the script indicating your command prompt is 'in' your folder.
* You should have a .csv exported from Gephi in the same folder as the script.
* You could have completed step 3, though if you haven't you will be prompted for your credentials soon.
* You should have completed step 6.

##### 8. Run the script(!)
* Type the following command and hit enter...

        python download_twitter_media.py

* Follow the on-screen instructions


