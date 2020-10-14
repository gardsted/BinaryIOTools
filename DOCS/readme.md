Module binaryiotools
====================
Base binary I/O helper.

Does boilerplate things like reading the next uint32 from a file or binary stream

Create a new IO object and initialize/ set data

Example
```python
f = open(fileName, 'rb')
data = f.read()
f.close()
io = IO(data)
width = io.u32
height = io.u32
```

The example above reads a file in binary and sets the variables width and height
as the first two unsigned integer 32s

For a file starting with the bytes:

```none
00 00 00 C8 00 01 90
```

The values for width and height would be 200, 400

Classes
-------

`IO(data: Optional[bytearray] = None, idx: int = 0, littleEndian: bool = False, boolSize: int = 8, stringEncoding: str = 'U')`
:   Class to handle i/o to a byte buffer or file-like object
    
    :param data: can be a data buffer or a file-like object
    :param idx: start reading/writing the data at the given index
    :param littleEndian: whether the default is big-endian or little-endian
    :param boolSize: how many default bits to use for a bool (8,16,32,or 64)
    :param stringEncoding: default string encoding A=Ascii, U=UTF-8, W-Unicode wide

    ### Instance variables

    `bool16: Union[str, bytearray, binaryiotools.IO, int, float]`
    :   get bool16

    `bool32: Union[str, bytearray, binaryiotools.IO, int, float]`
    :   get bool32

    `bool64: Union[str, bytearray, binaryiotools.IO, int, float]`
    :   get bool64

    `bool8: Union[str, bytearray, binaryiotools.IO, int, float]`
    :   get bool8

    `boolean`
    :   return bool

    `byte: Union[str, bytearray, binaryiotools.IO, int, float]`
    :   get byte

    `cString: Union[str, bytearray, binaryiotools.IO, int, float]`
    :   Read a sequence of chars until the next null byte

    `cStringA: Union[str, bytearray, binaryiotools.IO, int, float]`
    :   Read a sequence of chars until the next null byte in ascii

    `cStringU: Union[str, bytearray, binaryiotools.IO, int, float]`
    :   Read a sequence of chars until the next null byte in utf-8

    `cStringW: Union[str, bytearray, binaryiotools.IO, int, float]`
    :   Read a sequence of chars until the next null byte in ucs-2

    `data: bytearray`
    :   return data

    `double: Union[str, bytearray, binaryiotools.IO, int, float]`
    :   get a double

    `dword: Union[str, bytearray, binaryiotools.IO, int, float]`
    :   get a dword

    `float32: Union[str, bytearray, binaryiotools.IO, int, float]`
    :   get a float32

    `float32be: Union[str, bytearray, binaryiotools.IO, int, float]`
    :   read the next 32 bit float and advance the index

    `float32le: Union[str, bytearray, binaryiotools.IO, int, float]`
    :   read the next 32 bit float and advance the index

    `float64: Union[str, bytearray, binaryiotools.IO, int, float]`
    :   get a float64

    `float64be: Union[str, bytearray, binaryiotools.IO, int, float]`
    :   read the next 64 bit float and advance the index

    `float64le: Union[str, bytearray, binaryiotools.IO, int, float]`
    :   read the next 64 bit float and advance the index

    `floating: Union[str, bytearray, binaryiotools.IO, int, float]`
    :   get a float

    `i16: Union[str, bytearray, binaryiotools.IO, int, float]`
    :   get an int16

    `i16be: Union[str, bytearray, binaryiotools.IO, int, float]`
    :   read the next signed int16 and advance the index

    `i16le: Union[str, bytearray, binaryiotools.IO, int, float]`
    :   read the next signed int16 and advance the index

    `i32: Union[str, bytearray, binaryiotools.IO, int, float]`
    :   get an int32

    `i32be: Union[str, bytearray, binaryiotools.IO, int, float]`
    :   read the next signed int32 and advance the index

    `i32le: Union[str, bytearray, binaryiotools.IO, int, float]`
    :   read the next signed int32 and advance the index

    `i64: Union[str, bytearray, binaryiotools.IO, int, float]`
    :   get an int64

    `i64be: Union[str, bytearray, binaryiotools.IO, int, float]`
    :   read the next signed int64 and advance the index

    `i64le: Union[str, bytearray, binaryiotools.IO, int, float]`
    :   read the next signed int64 and advance the index

    `i8: Union[str, bytearray, binaryiotools.IO, int, float]`
    :   get an int8

    `i8be: Union[str, bytearray, binaryiotools.IO, int, float]`
    :   read the next signed int8 and advance the index

    `i8le: Union[str, bytearray, binaryiotools.IO, int, float]`
    :   read the next signed int8 and advance the index

    `index: int`
    :   return data

    `qword: Union[str, bytearray, binaryiotools.IO, int, float]`
    :   get a qword

    `sz754: Union[str, bytearray, binaryiotools.IO, int, float]`
    :   sz754

    `sz754A: Union[str, bytearray, binaryiotools.IO, int, float]`
    :   sz754A

    `sz754U: Union[str, bytearray, binaryiotools.IO, int, float]`
    :   sz754U

    `sz754W: Union[str, bytearray, binaryiotools.IO, int, float]`
    :   sz754W

    `textLine: Union[str, bytearray, binaryiotools.IO, int, float]`
    :   Read a sequence of chars until the next new line char

    `textLineA: Union[str, bytearray, binaryiotools.IO, int, float]`
    :   Read a sequence of chars until the next new line char in ascii

    `textLineU: Union[str, bytearray, binaryiotools.IO, int, float]`
    :   Read a sequence of chars until the next new line char in utf-8

    `textLineW: Union[str, bytearray, binaryiotools.IO, int, float]`
    :   Read a sequence of chars until the next new line char in ucs-2

    `u16: Union[str, bytearray, binaryiotools.IO, int, float]`
    :   get an uint16

    `u16be: Union[str, bytearray, binaryiotools.IO, int, float]`
    :   read the next uint16 and advance the index

    `u16le: Union[str, bytearray, binaryiotools.IO, int, float]`
    :   read the next uint16 and advance the index

    `u32: Union[str, bytearray, binaryiotools.IO, int, float]`
    :   get a uint32

    `u32be: Union[str, bytearray, binaryiotools.IO, int, float]`
    :   read the next uint32 and advance the index

    `u32le: Union[str, bytearray, binaryiotools.IO, int, float]`
    :   read the next uint32 and advance the index

    `u64: Union[str, bytearray, binaryiotools.IO, int, float]`
    :   get a uint64

    `u64be: Union[str, bytearray, binaryiotools.IO, int, float]`
    :   read the next uint64 and advance the index

    `u64le: Union[str, bytearray, binaryiotools.IO, int, float]`
    :   read the next uint64 and advance the index

    `u8: Union[str, bytearray, binaryiotools.IO, int, float]`
    :   get an unsigned int

    `u8be: Union[str, bytearray, binaryiotools.IO, int, float]`
    :   read the next uint8 and advance the index

    `u8le: Union[str, bytearray, binaryiotools.IO, int, float]`
    :   read the next uint8 and advance the index

    `unsignedByte: Union[str, bytearray, binaryiotools.IO, int, float]`
    :   get unsigned byte

    `unsignedDword: Union[str, bytearray, binaryiotools.IO, int, float]`
    :   get a unsigned dword

    `unsignedQword: Union[str, bytearray, binaryiotools.IO, int, float]`
    :   get an unsigned qword

    `unsignedWord: Union[str, bytearray, binaryiotools.IO, int, float]`
    :   get an unsigned word

    `word: Union[str, bytearray, binaryiotools.IO, int, float]`
    :   get a word

    ### Methods

    `addBytes(self, ioBytes: Union[str, bytearray, IO, int, float])`
    :   add some raw bytes and advance the index
        
        alias for setBytes()
        
        :param bytes: can be a string, bytearray, or another IO object

    `beginContext(self, newIndex: int)`
    :   Start a new context where the index can be changed all you want,
        and when endContext() is called, it will be restored to the current position

    `endContext(self)`
    :   Restore the index to the previous location where it was when
        beginContext() was called

    `getBytes(self, nbytes: int)`
    :   grab some raw bytes and advance the index

    `setBytes(self, ioBytes: Union[str, bytearray, IO, int, float])`
    :   add some raw bytes and advance the index
        
        alias for addBytes()
        
        :param ioBytes: can be a string, bytearray, or another IO object