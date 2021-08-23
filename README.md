# url shortening with python

# required libraries
# requests : pip install requests

# http://tinyurl.com/api-create.php?url=

import requests  

def shorten_url(url):
	base_url = 'http://tinyurl.com/api-create.php?url='
	url = base_url + url
	print('Original URL', url)
	r = requests.get(url)
	print(r.text)

url = 'https://www.sololearn.com/profile/22857063'
shorten_url(url)
