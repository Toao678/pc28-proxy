import requests
from http.server import BaseHTTPRequestHandler
import json

class handler(BaseHTTPRequestHandler):
    def do_GET(self):
        try:
            url = "https://yu28.top/api/kj?nbr=80"
            headers = {"X-Api-Key": "yu28_c3d2e45ca3d68e6d"}
            resp = requests.get(url, headers=headers, timeout=10)
            data = resp.json()
            
            self.send_response(200)
            self.send_header('Content-Type', 'application/json')
            self.send_header('Access-Control-Allow-Origin', '*')
            self.end_headers()
            self.wfile.write(json.dumps(data).encode())
        except Exception as e:
            self.send_response(500)
            self.end_headers()
            self.wfile.write(json.dumps({"error": str(e)}).encode())