# spider
爬虫爬呀爬
import urllib.request
import re
import requests
from bs4 import BeautifulSoup
def open_url(url):
    req = urllib.request.Request(url)
    req.add_header('User-Agent','Mozilla/5.0 (Macintosh; Intel Mac OS X 10_10_1) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/39.0.2171.95 Safari/537.36')
    page = urllib.request.urlopen(req)
    html = page.read().decode('utf-8')
    return html
def get_title(html):
    soup = BeautifulSoup(html,'lxml')
   # m = soup.find(class_="lemma-summary")
    for child in m.children:
        print(child.string)
    return
if __name__ == '__main__':

   # url = ["https://baike.baidu.com/item/python"]

    for url in url:
        print(get_title(open_url(url)))



