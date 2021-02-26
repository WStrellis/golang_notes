## Reading from JSON Files
Read JSON formatted data into a generic map
```
var data map[string]interface{}

jsonFile, err := os.Open("./foo.json")
if err != nil{
    log.Fatal(err)
}
defer jsonFile.Close()

// convert to bytes
jsonBytes, err := ioutil.ReadAll(jsonFile)
// convert to go
err = json.Unmarshal(jsonBytes, &data)
```