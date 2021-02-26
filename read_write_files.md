## Reading from JSON Files
```
var data []string{}

jsonFile, err := os.Open("./foo.json")
if err != nil{
    log.Fatal(err)
}

// convert to bytes
jsonBytes, err := ioutil.ReadAll(jsonFile)
// convert to go
err = json.Unmarshal(jsonBytes, &data)
```