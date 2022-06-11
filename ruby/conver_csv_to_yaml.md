```ruby
require 'csv'
require 'yaml'

data_csv = CSV.foreach('data.csv').map {|row| {"id" => row[0].to_i, "name" => row[1]}}
File.open('file.yml', 'w') {|f| f.write data_csv.to_yaml }
```
