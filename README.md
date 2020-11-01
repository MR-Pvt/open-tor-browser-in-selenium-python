# open-tor-browser-in-selenium-python

and its in the .py and ipynb file
### #here's the python code to do it...and its also in the .py and ipynb file

from selenium import webdriver

from selenium.webdriver.chrome.options import Options

import subprocess

#### #Here put the path of your tor browser file named as firefox.exe in Tor Browser\Browser
torexe = subprocess.Popen(r'C:\Users\rafay\Dropbox\My PC (DESKTOP-JFP260O)\Desktop\Tor Browser\Browser\firefox.exe')

PROXY = "socks5://127.0.0.1:9150" # IP:PORT or HOST:PORT

options = webdriver.ChromeOptions()

options.add_argument('--proxy-server=%s' % PROXY)

#### #Here put the path of your chromedriver in executable path
driver = webdriver.Chrome(executable_path=r'D:/chromedriver', options=options)

#### #Here put the url/link of your desired website
driver.get("http://ivononic.com/4AOe")
