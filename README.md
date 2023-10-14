# zip-c3

[![](https://img.shields.io/github/v/tag/thechampagne/zip-c3?label=version)](https://github.com/thechampagne/zip-c3/releases/latest) [![](https://img.shields.io/github/license/thechampagne/zip-c3)](https://github.com/thechampagne/zip-c3/blob/main/LICENSE)

C3 binding for a portable, simple **zip** library.

### Example
```c
import std::core::string;
import zip;

fn void main() {
    Zip z = zip::open("/tmp/c3.zip", 6, 'w');
    defer z.close();
    
    z.entryOpen("test");
    defer z.entryClose();
    
    string::ZString content = "test content";
    z.entryWrite(content, content.len());
}
```

### References
 - [zip](https://github.com/kuba--/zip)

### License

This repo is released under the [MIT License](https://github.com/thechampagne/zip-c3/blob/main/LICENSE).
