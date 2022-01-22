# trikam

from selenium import webdriver
from selenium.webdriver.common.by import By

driver = webdriver.Chrome(executable_path="C:/Program Files (x86)/Google/Chrome/Application/chromedriver.exe")
driver.get("http://linkedin.com")

links = driver.find_elements_by_tag_name("a")

("Number of links present:", len(links))

for links in links:
    print(links.text)

driver.find_element_by_link_text("Jobs").click() # Method 1
#driver.find_element(By.LINK_TEXT,"Jobs").click()
