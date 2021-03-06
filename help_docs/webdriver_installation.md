## Installing Google Chromedriver, Firefox Geckodriver, and other drivers


To run automation on various web browsers, you'll need to download a driver file for each one and place it on your System **[PATH](http://java.com/en/download/help/path.xml)**. On a Mac, ``/usr/local/bin`` is a good spot. On Windows, make sure you set the System Path under Environment Variables to include the location where you placed the driver files. You may want to download newer versions of drivers as they become available.

* For Chrome, get [Chromedriver](https://sites.google.com/a/chromium.org/chromedriver/downloads) on your System Path.

* For Firefox, get [Geckodriver](https://github.com/mozilla/geckodriver/releases) on your System Path.

* For Microsoft Edge, get [Edge Driver (Microsoft WebDriver)](https://developer.microsoft.com/en-us/microsoft-edge/tools/webdriver/) on your System Path.

* For Safari, get [Safari Driver](https://github.com/seleniumbase/SeleniumBase/blob/master/help_docs/using_safari_driver.md) on your System Path.

* For PhantomJS headless browser automation, get [PhantomJS](http://phantomjs.org/download.html) on your System Path. (NOTE: PhantomJS is no longer officially supported by SeleniumHQ)

Mac:

* On a Mac, you can install drivers more easily by using ``brew`` (aka ``homebrew``), but you have to install that first. [Brew installation instructions are here](https://github.com/seleniumbase/SeleniumBase/blob/master/help_docs/install_python_pip_git.md).

```bash
brew install chromedriver

brew install geckodriver
```

(NOTE: If your existing version of chromedriver is less than 2.36, **upgrading is recommended!**)

```bash
brew upgrade chromedriver

brew upgrade geckodriver
```

Linux:

```bash
wget http://chromedriver.storage.googleapis.com/2.37/chromedriver_linux64.zip
unzip chromedriver_linux64.zip
mv chromedriver /usr/local/bin/
chmod +x /usr/local/bin/chromedriver
```

```bash
wget https://github.com/mozilla/geckodriver/releases/download/v0.20.0/geckodriver-v0.20.0-linux64.tar.gz
tar xvfz geckodriver-v0.20.0-linux64.tar.gz
mv geckodriver /usr/local/bin/
chmod +x /usr/local/bin/geckodriver
```

* To verify that the web drivers are working, **[follow these instructions](https://github.com/seleniumbase/SeleniumBase/blob/master/help_docs/verify_webdriver.md)**.
