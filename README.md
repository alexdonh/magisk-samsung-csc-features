# Csc Features

## Description

This module attends to change csc features by replacing the relevant xml files in /product/omc/<CSC CODE>/conf. Magisk v20.0+ is required to replace /product.
  
## How to

1. Get the file `adb pull /product/omc/<CSC CODE>/conf /to/your/local/`
2. Decode the file `java -jar omc-decoder.jar -i cscfeature.xml -o cscfeature_decoded.xml`
3. Modify the _decoded.xml as needed
4. Encode the file `java -jar omc-decoder.jar -e -i cscfeature_decoded.xml -o cscfeature.xml`
5. Put the modified cscfeature.xml in `<MODULE PATH>/system/product/omc/<CSC CODE>/conf/`
6. Package zip, install and profit!
  
## Credits

- @topjohnwu for the magical [Magisk](https://github.com/topjohnwu/Magisk)
- @fei-ke for his [OmcTextDecoder](https://github.com/fei-ke/OmcTextDecoder)
- me

## Source code

[Github](https://github.com/alexdonh/magisk-module-cscfeatures)

## Changelog

### v1.0

- Initial commit
