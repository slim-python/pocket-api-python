This python script will let you add urls to your pocket account

First, you have to [Create your consumer key](https://getpocket.com/developer/apps/new) from getpocket's developer console. To get the access token, you have to authorize the app on your own account. There are tools on the web that can automate this for you such as [fxneumann's OneClickPocket](http://reader.fxneumann.de/plugins/oneclickpocket/auth.php)

    import requests
    
    from requests.structures import CaseInsensitiveDict
    
      
    
    url = "https://getpocket.com/v3/add"
    
 
    headers = CaseInsensitiveDict()
    
    headers["Content-Type"] = "application/json"
    
      
    
    data = """
    
    [
    
    {
    
    #submit your post here in the url field
    "url": "https://example.com/post/",
    
    "consumer_key":"Your consumer key",
    
    "access_token":"your acess token"
    
    }
    
    ]
    
    """
    
      
      
    
    resp = requests.post(url, headers=headers, data=data)
    
      
    
    print(resp.status_code)
