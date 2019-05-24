## Geckodriver
wget https://github.com/mozilla/geckodriver/releases/download/v0.23.0/geckodriver-v0.23.0-linux64.tar.gz<br>
sudo sh -c 'tar -x geckodriver -zf geckodriver-v0.23.0-linux64.tar.gz -O > /usr/bin/geckodriver'<br>
sudo chmod +x /usr/bin/geckodriver<br>
rm geckodriver-v0.23.0-linux64.tar.gz<br>

## Chromedriver
wget https://chromedriver.storage.googleapis.com/2.29/chromedriver_linux64.zip<br>
unzip chromedriver_linux64.zip<br>
sudo chmod +x chromedriver<br>
sudo mv chromedriver /usr/bin/<br>
rm chromedriver_linux64.zip<br>
