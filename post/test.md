
# -*- coding utf-8 -*-

importrequests,bs4

frombs4importBeautifulSoup


sogou =open('SOGOU.html',"w",newline="",encoding="UTF-8-sig")


headers = {"User-Agent":"Mozilla/5.0 (Windows NT6.1; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/79.0.3945.88 Safari/537.36"}


a =input("输入要搜索的内容：")


url ="https://www.sogou.com/web?query=";+str(a)


res = requests.get(url,headers=headers)


html = res.text


soup = BeautifulSoup(html,"html.parser")


sogou.write(str(soup))


sogou.close()
