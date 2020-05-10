<a name=".binaryiotools"></a>
## binaryiotools

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

<a name=".binaryiotools.IO"></a>
### IO

```python
class IO()
```

Class to handle i/o to a byte buffer or file-like object

<a name=".binaryiotools.IO.__init__"></a>
#### \_\_init\_\_

```python
 | __init__(data=None, idx=0, littleEndian=False, boolSize=8, stringEncoding='U')
```

**Arguments**:

- `data`: can be a data buffer or a file-like object
- `idx`: start reading/writing the data at the given index
- `littleEndian`: whether the default is big-endian or little-endian
- `boolSize`: how many default bits to use for a bool (8,16,32,or 64)
- `stringEncoding`: default string encoding A=Ascii, U=UTF-8, W-Unicode wide

<a name=".binaryiotools.IO.data"></a>
#### data

```python
 | @data.setter
 | data(data)
```

set data

<a name=".binaryiotools.IO.beginContext"></a>
#### beginContext

```python
 | beginContext(newIndex)
```

Start a new context where the index can be changed all you want,
and when endContext() is called, it will be restored to the current position

<a name=".binaryiotools.IO.endContext"></a>
#### endContext

```python
 | endContext()
```

Restore the index to the previous location where it was when
beginContext() was called

<a name=".binaryiotools.IO.bool"></a>
#### bool

```python
 | @bool.setter
 | bool(ioBool)
```

set bool

<a name=".binaryiotools.IO.bool8"></a>
#### bool8

```python
 | @bool8.setter
 | bool8(ioBool)
```

set a bool8

<a name=".binaryiotools.IO.bool16"></a>
#### bool16

```python
 | @bool16.setter
 | bool16(ioBool)
```

set bool16

<a name=".binaryiotools.IO.bool32"></a>
#### bool32

```python
 | @bool32.setter
 | bool32(ioBool)
```

set bool32

<a name=".binaryiotools.IO.bool64"></a>
#### bool64

```python
 | @bool64.setter
 | bool64(ioBool)
```

set bool64

<a name=".binaryiotools.IO.byte"></a>
#### byte

```python
 | @byte.setter
 | byte(byte)
```

set byte

<a name=".binaryiotools.IO.unsignedByte"></a>
#### unsignedByte

```python
 | @unsignedByte.setter
 | unsignedByte(byte)
```

set unsigned byte

<a name=".binaryiotools.IO.word"></a>
#### word

```python
 | @word.setter
 | word(word)
```

set a word

<a name=".binaryiotools.IO.unsignedWord"></a>
#### unsignedWord

```python
 | @unsignedWord.setter
 | unsignedWord(unsignedWord)
```

set an unsigned word

<a name=".binaryiotools.IO.dword"></a>
#### dword

```python
 | @dword.setter
 | dword(dword)
```

set a dword

<a name=".binaryiotools.IO.unsignedDword"></a>
#### unsignedDword

```python
 | @unsignedDword.setter
 | unsignedDword(unsignedDword)
```

set an unsigned dword

<a name=".binaryiotools.IO.qword"></a>
#### qword

```python
 | @qword.setter
 | qword(qword)
```

set a qword

<a name=".binaryiotools.IO.unsignedQword"></a>
#### unsignedQword

```python
 | @unsignedQword.setter
 | unsignedQword(unsignedQword)
```

set an unsigned qword

<a name=".binaryiotools.IO.i8"></a>
#### i8

```python
 | @i8.setter
 | i8(i8)
```

set an int8

<a name=".binaryiotools.IO.u8"></a>
#### u8

```python
 | @u8.setter
 | u8(u8)
```

set an unsigned int

<a name=".binaryiotools.IO.i16"></a>
#### i16

```python
 | @i16.setter
 | i16(i16)
```

set an int16

<a name=".binaryiotools.IO.u16"></a>
#### u16

```python
 | @u16.setter
 | u16(u16)
```

set an unint16

<a name=".binaryiotools.IO.i32"></a>
#### i32

```python
 | @i32.setter
 | i32(i32)
```

set an int32

<a name=".binaryiotools.IO.u32"></a>
#### u32

```python
 | @u32.setter
 | u32(u32)
```

set a unint32

<a name=".binaryiotools.IO.i64"></a>
#### i64

```python
 | @i64.setter
 | i64(i64)
```

set an int64

<a name=".binaryiotools.IO.u64"></a>
#### u64

```python
 | @u64.setter
 | u64(u64)
```

set a uint64

<a name=".binaryiotools.IO.float32"></a>
#### float32

```python
 | @float32.setter
 | float32(float32)
```

set a float32

<a name=".binaryiotools.IO.float64"></a>
#### float64

```python
 | @float64.setter
 | float64(float64)
```

set a float64

<a name=".binaryiotools.IO.u8be"></a>
#### u8be

```python
 | @u8be.setter
 | u8be(u8be)
```

set the uint8

<a name=".binaryiotools.IO.u8le"></a>
#### u8le

```python
 | @u8le.setter
 | u8le(u8le)
```

set the uint8

<a name=".binaryiotools.IO.i8le"></a>
#### i8le

```python
 | @i8le.setter
 | i8le(i8le)
```

set the int8

<a name=".binaryiotools.IO.i8be"></a>
#### i8be

```python
 | @i8be.setter
 | i8be(i8be)
```

set the int8

<a name=".binaryiotools.IO.u16be"></a>
#### u16be

```python
 | @u16be.setter
 | u16be(u16be)
```

set the uint16

<a name=".binaryiotools.IO.u16le"></a>
#### u16le

```python
 | @u16le.setter
 | u16le(u16le)
```

set the uint16

<a name=".binaryiotools.IO.i16le"></a>
#### i16le

```python
 | @i16le.setter
 | i16le(i16le)
```

set the int16

<a name=".binaryiotools.IO.i16be"></a>
#### i16be

```python
 | @i16be.setter
 | i16be(i16be)
```

set the int16

<a name=".binaryiotools.IO.u32be"></a>
#### u32be

```python
 | @u32be.setter
 | u32be(u32be)
```

set the uint32

<a name=".binaryiotools.IO.u32le"></a>
#### u32le

```python
 | @u32le.setter
 | u32le(u32le)
```

set the uint32

<a name=".binaryiotools.IO.i32le"></a>
#### i32le

```python
 | @i32le.setter
 | i32le(i32le)
```

set the int32

<a name=".binaryiotools.IO.i32be"></a>
#### i32be

```python
 | @i32be.setter
 | i32be(i32be)
```

set the int32

<a name=".binaryiotools.IO.u64be"></a>
#### u64be

```python
 | @u64be.setter
 | u64be(u64be)
```

set the uint64

<a name=".binaryiotools.IO.u64le"></a>
#### u64le

```python
 | @u64le.setter
 | u64le(u64le)
```

set the uint64

<a name=".binaryiotools.IO.i64le"></a>
#### i64le

```python
 | @i64le.setter
 | i64le(i64le)
```

set the int64

<a name=".binaryiotools.IO.i64be"></a>
#### i64be

```python
 | @i64be.setter
 | i64be(i64be)
```

set the int64

<a name=".binaryiotools.IO.float"></a>
#### float

```python
 | @float.setter
 | float(f)
```

set a float

<a name=".binaryiotools.IO.double"></a>
#### double

```python
 | @double.setter
 | double(f)
```

set a double

<a name=".binaryiotools.IO.float32be"></a>
#### float32be

```python
 | @float32be.setter
 | float32be(float32be)
```

set a 32 bit float

<a name=".binaryiotools.IO.float32le"></a>
#### float32le

```python
 | @float32le.setter
 | float32le(float32le)
```

set a 32 bit float

<a name=".binaryiotools.IO.float64be"></a>
#### float64be

```python
 | @float64be.setter
 | float64be(float64be)
```

set a 64 bit float

<a name=".binaryiotools.IO.float64le"></a>
#### float64le

```python
 | @float64le.setter
 | float64le(float64le)
```

set a 64 bit float

<a name=".binaryiotools.IO.getBytes"></a>
#### getBytes

```python
 | getBytes(nbytes)
```

grab some raw bytes and advance the index

<a name=".binaryiotools.IO.addBytes"></a>
#### addBytes

```python
 | addBytes(ioBytes)
```

add some raw bytes and advance the index

alias for setBytes()

**Arguments**:

- `bytes`: can be a string, bytearray, or another IO object

<a name=".binaryiotools.IO.setBytes"></a>
#### setBytes

```python
 | setBytes(ioBytes)
```

add some raw bytes and advance the index

alias for addBytes()

**Arguments**:

- `ioBytes`: can be a string, bytearray, or another IO object

<a name=".binaryiotools.IO.sz754"></a>
#### sz754

```python
 | @sz754.setter
 | sz754(sz754)
```

set sz754

<a name=".binaryiotools.IO.sz754A"></a>
#### sz754A

```python
 | @sz754A.setter
 | sz754A(sz754)
```

set sz754A

<a name=".binaryiotools.IO.sz754W"></a>
#### sz754W

```python
 | @sz754W.setter
 | sz754W(sz754)
```

set sz754W

<a name=".binaryiotools.IO.sz754U"></a>
#### sz754U

```python
 | @sz754U.setter
 | sz754U(sz754)
```

set sz754U

<a name=".binaryiotools.IO.textLine"></a>
#### textLine

```python
 | @textLine.setter
 | textLine(text)
```

Set a sequence of chars until the next new line char

<a name=".binaryiotools.IO.textLineA"></a>
#### textLineA

```python
 | @textLineA.setter
 | textLineA(text)
```

Set a sequence of chars until the next new line char in ascii

<a name=".binaryiotools.IO.textLineW"></a>
#### textLineW

```python
 | @textLineW.setter
 | textLineW(text)
```

Set a sequence of chars until the next new line char in ucs-2

<a name=".binaryiotools.IO.textLineU"></a>
#### textLineU

```python
 | @textLineU.setter
 | textLineU(text)
```

Set a sequence of chars until the next new line char in utf-8

<a name=".binaryiotools.IO.cString"></a>
#### cString

```python
 | @cString.setter
 | cString(text)
```

Set a sequence of chars and add a null byte

<a name=".binaryiotools.IO.cStringA"></a>
#### cStringA

```python
 | @cStringA.setter
 | cStringA(text)
```

Set a sequence of chars and add a null byte in ascii

<a name=".binaryiotools.IO.cStringW"></a>
#### cStringW

```python
 | @cStringW.setter
 | cStringW(text)
```

Set a sequence of chars and add a null byte in ucs-2

<a name=".binaryiotools.IO.cStringU"></a>
#### cStringU

```python
 | @cStringU.setter
 | cStringU(text)
```

Set a sequence of chars and add a null byte in utf-8

<a name=".make"></a>
## make

Makefile for python. Run one of the following subcommands:

install: Poetry install
build: Building docs, requirements.txt, setup.py, poetry build

