import requests
from bs4 import BeautifulSoup

req = requests.get("https://results.eci.gov.in/PcResultGenJune2024/index.htm")
soup = BeautifulSoup(req.content, "html.parser")

res = soup.title


print(soup.get_text())
