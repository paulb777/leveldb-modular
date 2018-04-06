# leveldb-modular

## Example

- git clone git@github.com:paulb777/leveldb-modular.git
- cd leveldb-modular/Example/
- pod update
- open leveldb-modular.xcworkspace/
- build and notice failure
- grep HEADER_SEARCH_PATH "Pods/Target Support Files/leveldb-modular/leveldb-modular.xcconfig"
```
HEADER_SEARCH_PATHS = $(inherited) "${PODS_ROOT}/Headers/Public"
```
- Remove `:modular_headers => true` from Podfile
- pod update
- grep HEADER_SEARCH_PATH "Pods/Target Support Files/leveldb-modular/leveldb-modular.xcconfig"
```
HEADER_SEARCH_PATHS = $(inherited) "${PODS_ROOT}/Headers/Public" "${PODS_ROOT}/Headers/Public/leveldb-library"
```
- Notice that the search path is now correct

## Requirements

## Installation

leveldb-modular is available through [CocoaPods](http://cocoapods.org). To install
it, simply add the following line to your Podfile:

```ruby
pod 'leveldb-modular'
```

## Author

Paul Beusterien, paulbeusterien@google.com

## License

leveldb-modular is available under the MIT license. See the LICENSE file for more info.
