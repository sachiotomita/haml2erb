# haml2erb

haml2erb is a tool for converting [Haml](http://haml-lang.com/) to Erb markup.


convert your haml files to erb with command


## Installing and loading haml2erb



```ruby
gem 'haml2erb', :git => 'https://github.com/sachiotomita/haml2erb.git'
```







## Using haml2erb

Use the `haml2erb` command line or from Ruby call the `Haml2Erb.convert` method to have Haml markup translated into Erb.




```ruby
rails c
```


```ruby
hamls = Dir["app/views/**/*.haml"];
hamls.each do |haml| 
  puts haml
  erb = haml.sub(/\.haml$/, '.erb')
  File.open(erb, 'w') do |file| 
    file.write Haml2Erb.convert(File.read(haml)) 
  end
end
```




### Example: Simple conversion

```bash
  echo '.foo' | haml2erb
  # <div class='foo'></div>
```

```ruby
  Haml2Erb.convert('.foo')
  # => "<div class='foo'></div>\n"
```


## License

[MIT_LICENSE](/elia/haml2erb/blob/master/MIT_LICENSE)


## Credits

For the [original implementation](https://github.com/c1sgo/haml2erb): 

[Chris Goddard](https://github.com/cgoddard)
[Louis Sivillo](https://github.com/BeaconInteractive)
