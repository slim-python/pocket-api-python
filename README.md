    import requests
    
    from requests.structures import CaseInsensitiveDict
    
      
    
    url = "https://getpocket.com/v3/add"
    
 
    headers = CaseInsensitiveDict()
    
    headers["Content-Type"] = "application/json"
    
      
    
    data = """
    
    [
    
    {
    
    "url": "https://example.com/post/",
    
    "consumer_key":"Your consumer key",
    
    "access_token":"your acess token"
    
    }
    
    ]
    
    """
    
      
      
    
    resp = requests.post(url, headers=headers, data=data)
    
      
    
    print(resp.status_code)
