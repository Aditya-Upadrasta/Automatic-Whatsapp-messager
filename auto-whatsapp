import time
from selenium import webdriver
from selenium.webdriver.chrome.options import Options
#*****************************************************************************************************************************************************************************#
#********************************** PROVIDE YOUR MESSAGE HERE!!!!!!!!!!!!!!!!!!!!!!!!!****************************************************************************************#


message = ["Type you message here!!!!!!!!!!!!"]

options = Options()
options.add_argument("--user-data-dir=chrome-data")
options.add_experimental_option("excludeSwitches", ["enable-automation"])
options.add_experimental_option('useAutomationExtension', False)

#*********************WEBDRIVER!!!!!!!**************************#
driver = webdriver.Chrome("#PASTE YOUR CHROME WEBDRIVER'S PATH HERE!!!!!!!!!!!!!!!!#", options=options)
driver.maximize_window()
driver.get('https://web.whatsapp.com')  # Already authenticated

time.sleep(20)

##################### Provide Recepient Name Here ###############################
driver.find_element_by_xpath("//*[@title='#TYPE THE RECIPIENT NAME, WHICH IS SAVED IN YOUR CONTACTS  ,,,, TYPE THE EXACT NAME#']").click()

for joke in message:
    driver.find_element_by_xpath('//*[@id="main"]/footer/div[1]/div[2]/div/div[2]').send_keys(joke)
    driver.find_element_by_xpath('//*[@id="main"]/footer/div[1]/div[3]/button/span').click()
    time.sleep(10)

time.sleep(30)
driver.close()
