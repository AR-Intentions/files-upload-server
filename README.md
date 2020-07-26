# files-upload-server

To start the server:
```
npm start
```

### The curl command to test
curl -X POST   http://localhost:3000/upload-yaml   -H 'content-type: multipart/form-data'   -F yaml=@<file_path>

### CSharp Rest code to test
```
var client = new RestClient("http://localhost:3000/upload-yaml");
var request = new RestRequest(Method.POST);
request.AddHeader("content-type", "multipart/form-data; boundary=----WebKitFormBoundary7MA4YWxkTrZu0gW");
request.AddParameter("multipart/form-data; boundary=----WebKitFormBoundary7MA4YWxkTrZu0gW", "------WebKitFormBoundary7MA4YWxkTrZu0gW\r\nContent-Disposition: form-data; name=\"yaml\"; filename=\"swagger.yml\"\r\nContent-Type: text/yaml\r\n\r\n\r\n------WebKitFormBoundary7MA4YWxkTrZu0gW--", ParameterType.RequestBody);
IRestResponse response = client.Execute(request);
```

