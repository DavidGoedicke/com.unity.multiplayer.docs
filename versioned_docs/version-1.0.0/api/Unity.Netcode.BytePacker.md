---  
id: Unity.Netcode.BytePacker  
title: Unity.Netcode.BytePacker  
---

<div class="markdown level0 summary">

Utility class for packing values in serialization.

</div>

<div class="markdown level0 conceptual">

</div>

<div class="inheritance">

##### Inheritance

<div class="level0">

System.Dynamic.ExpandoObject

</div>

<div class="level1">

System.Dynamic.ExpandoObject

</div>

</div>

<div class="inheritedMembers">

##### Inherited Members

<div>

Object.Equals(Object)

</div>

<div>

Object.Equals(Object, Object)

</div>

<div>

Object.GetHashCode()

</div>

<div>

Object.GetType()

</div>

<div>

Object.MemberwiseClone()

</div>

<div>

Object.ReferenceEquals(Object, Object)

</div>

<div>

Object.ToString()

</div>

</div>

##### **Namespace**: System.Dynamic.ExpandoObject

##### **Assembly**: MLAPI.dll

##### Syntax

``` lang-csharp
public static class BytePacker
```

## 

### WriteValueBitPacked(FastBufferWriter, Int16)

<div class="markdown level1 summary">

Writes a 14-bit signed short to the buffer in a bit-encoded packed
format. The first bit indicates whether the value is 1 byte or 2. The
sign bit takes up another bit. That leaves 14 bits for the value. A
value greater than 2^14-1 or less than -2^14 will throw an exception in
editor and development builds. In release builds builds the exception is
not thrown and the value is truncated by losing its two most significant
bits after zig-zag encoding.

</div>

<div class="markdown level1 conceptual">

</div>

#### Declaration

``` lang-csharp
public static void WriteValueBitPacked(FastBufferWriter writer, short value)
```

#### Parameters

| Type             | Name   | Description            |
|------------------|--------|------------------------|
| FastBufferWriter | writer | The writer to write to |
| System.Int16     | value  | The value to pack      |

### WriteValueBitPacked(FastBufferWriter, Int32)

<div class="markdown level1 summary">

Writes a 29-bit signed int to the buffer in a bit-encoded packed format.
The first two bits indicate whether the value is 1, 2, 3, or 4 bytes.
The sign bit takes up another bit. That leaves 29 bits for the value. A
value greater than 2^29-1 or less than -2^29 will throw an exception in
editor and development builds. In release builds builds the exception is
not thrown and the value is truncated by losing its three most
significant bits after zig-zag encoding.

</div>

<div class="markdown level1 conceptual">

</div>

#### Declaration

``` lang-csharp
public static void WriteValueBitPacked(FastBufferWriter writer, int value)
```

#### Parameters

| Type             | Name   | Description            |
|------------------|--------|------------------------|
| FastBufferWriter | writer | The writer to write to |
| System.Int32     | value  | The value to pack      |

### WriteValueBitPacked(FastBufferWriter, Int64)

<div class="markdown level1 summary">

Writes a 60-bit signed long to the buffer in a bit-encoded packed
format. The first three bits indicate whether the value is 1, 2, 3, 4,
5, 6, 7, or 8 bytes. The sign bit takes up another bit. That leaves 60
bits for the value. A value greater than 2^60-1 or less than -2^60 will
throw an exception in editor and development builds. In release builds
builds the exception is not thrown and the value is truncated by losing
its four most significant bits after zig-zag encoding.

</div>

<div class="markdown level1 conceptual">

</div>

#### Declaration

``` lang-csharp
public static void WriteValueBitPacked(FastBufferWriter writer, long value)
```

#### Parameters

| Type             | Name   | Description            |
|------------------|--------|------------------------|
| FastBufferWriter | writer | The writer to write to |
| System.Int64     | value  | The value to pack      |

### WriteValueBitPacked(FastBufferWriter, UInt16)

<div class="markdown level1 summary">

Writes a 15-bit unsigned short to the buffer in a bit-encoded packed
format. The first bit indicates whether the value is 1 byte or 2. That
leaves 15 bits for the value. A value greater than 2^15-1 will throw an
exception in editor and development builds. In release builds builds the
exception is not thrown and the value is truncated by losing its most
significant bit.

</div>

<div class="markdown level1 conceptual">

</div>

#### Declaration

``` lang-csharp
public static void WriteValueBitPacked(FastBufferWriter writer, ushort value)
```

#### Parameters

| Type             | Name   | Description            |
|------------------|--------|------------------------|
| FastBufferWriter | writer | The writer to write to |
| System.UInt16    | value  | The value to pack      |

### WriteValueBitPacked(FastBufferWriter, UInt32)

<div class="markdown level1 summary">

Writes a 30-bit unsigned int to the buffer in a bit-encoded packed
format. The first two bits indicate whether the value is 1, 2, 3, or 4
bytes. That leaves 30 bits for the value. A value greater than 2^30-1
will throw an exception in editor and development builds. In release
builds builds the exception is not thrown and the value is truncated by
losing its two most significant bits.

</div>

<div class="markdown level1 conceptual">

</div>

#### Declaration

``` lang-csharp
public static void WriteValueBitPacked(FastBufferWriter writer, uint value)
```

#### Parameters

| Type             | Name   | Description            |
|------------------|--------|------------------------|
| FastBufferWriter | writer | The writer to write to |
| System.UInt32    | value  | The value to pack      |

### WriteValueBitPacked(FastBufferWriter, UInt64)

<div class="markdown level1 summary">

Writes a 61-bit unsigned long to the buffer in a bit-encoded packed
format. The first three bits indicate whether the value is 1, 2, 3, 4,
5, 6, 7, or 8 bytes. That leaves 31 bits for the value. A value greater
than 2^61-1 will throw an exception in editor and development builds. In
release builds builds the exception is not thrown and the value is
truncated by losing its three most significant bits.

</div>

<div class="markdown level1 conceptual">

</div>

#### Declaration

``` lang-csharp
public static void WriteValueBitPacked(FastBufferWriter writer, ulong value)
```

#### Parameters

| Type             | Name   | Description            |
|------------------|--------|------------------------|
| FastBufferWriter | writer | The writer to write to |
| System.UInt64    | value  | The value to pack      |

### WriteValuePacked(FastBufferWriter, Color)

<div class="markdown level1 summary">

Convenience method that writes four varint floats from the color to the
buffer

</div>

<div class="markdown level1 conceptual">

</div>

#### Declaration

``` lang-csharp
public static void WriteValuePacked(FastBufferWriter writer, Color color)
```

#### Parameters

| Type             | Name   | Description            |
|------------------|--------|------------------------|
| FastBufferWriter | writer | The writer to write to |
| Color            | color  | Color to write         |

### WriteValuePacked(FastBufferWriter, Color32)

<div class="markdown level1 summary">

Convenience method that writes four varint floats from the color to the
buffer

</div>

<div class="markdown level1 conceptual">

</div>

#### Declaration

``` lang-csharp
public static void WriteValuePacked(FastBufferWriter writer, Color32 color)
```

#### Parameters

| Type             | Name   | Description            |
|------------------|--------|------------------------|
| FastBufferWriter | writer | The writer to write to |
| Color32          | color  | Color to write         |

### WriteValuePacked(FastBufferWriter, Quaternion)

<div class="markdown level1 summary">

Writes the rotation to the buffer.

</div>

<div class="markdown level1 conceptual">

</div>

#### Declaration

``` lang-csharp
public static void WriteValuePacked(FastBufferWriter writer, Quaternion rotation)
```

#### Parameters

| Type             | Name     | Description            |
|------------------|----------|------------------------|
| FastBufferWriter | writer   | The writer to write to |
| Quaternion       | rotation | Rotation to write      |

### WriteValuePacked(FastBufferWriter, Ray)

<div class="markdown level1 summary">

Convenience method that writes two packed Vector3 from the ray to the
buffer

</div>

<div class="markdown level1 conceptual">

</div>

#### Declaration

``` lang-csharp
public static void WriteValuePacked(FastBufferWriter writer, Ray ray)
```

#### Parameters

| Type             | Name   | Description            |
|------------------|--------|------------------------|
| FastBufferWriter | writer | The writer to write to |
| Ray              | ray    | Ray to write           |

### WriteValuePacked(FastBufferWriter, Ray2D)

<div class="markdown level1 summary">

Convenience method that writes two packed Vector2 from the ray to the
buffer

</div>

<div class="markdown level1 conceptual">

</div>

#### Declaration

``` lang-csharp
public static void WriteValuePacked(FastBufferWriter writer, Ray2D ray2d)
```

#### Parameters

| Type             | Name   | Description            |
|------------------|--------|------------------------|
| FastBufferWriter | writer | The writer to write to |
| Ray2D            | ray2d  | Ray2D to write         |

### WriteValuePacked(FastBufferWriter, Boolean)

<div class="markdown level1 summary">

Write a bool to the buffer.

</div>

<div class="markdown level1 conceptual">

</div>

#### Declaration

``` lang-csharp
public static void WriteValuePacked(FastBufferWriter writer, bool value)
```

#### Parameters

| Type             | Name   | Description            |
|------------------|--------|------------------------|
| FastBufferWriter | writer | The writer to write to |
| System.Boolean   | value  | Value to write         |

### WriteValuePacked(FastBufferWriter, Byte)

<div class="markdown level1 summary">

Write a byte to the buffer.

</div>

<div class="markdown level1 conceptual">

</div>

#### Declaration

``` lang-csharp
public static void WriteValuePacked(FastBufferWriter writer, byte value)
```

#### Parameters

| Type             | Name   | Description            |
|------------------|--------|------------------------|
| FastBufferWriter | writer | The writer to write to |
| System.Byte      | value  | Value to write         |

### WriteValuePacked(FastBufferWriter, Char)

<div class="markdown level1 summary">

Write a two-byte character as a varint to the buffer. WARNING: If the
value you're writing is \> 2287, this will use MORE space (3 bytes
instead of 2), and if your value is \> 240 you'll get no savings at all.
Only use this if you're certain your value will be small.

</div>

<div class="markdown level1 conceptual">

</div>

#### Declaration

``` lang-csharp
public static void WriteValuePacked(FastBufferWriter writer, char c)
```

#### Parameters

| Type             | Name   | Description            |
|------------------|--------|------------------------|
| FastBufferWriter | writer | The writer to write to |
| System.Char      | c      | Value to write         |

### WriteValuePacked(FastBufferWriter, Double)

<div class="markdown level1 summary">

Write double-precision floating point value to the buffer as a varint

</div>

<div class="markdown level1 conceptual">

</div>

#### Declaration

``` lang-csharp
public static void WriteValuePacked(FastBufferWriter writer, double value)
```

#### Parameters

| Type             | Name   | Description            |
|------------------|--------|------------------------|
| FastBufferWriter | writer | The writer to write to |
| System.Double    | value  | Value to write         |

### WriteValuePacked(FastBufferWriter, Int16)

<div class="markdown level1 summary">

Write a signed short (Int16) as a ZigZag encoded varint to the buffer.
WARNING: If the value you're writing is \> 2287, this will use MORE
space (3 bytes instead of 2), and if your value is \> 240 you'll get no
savings at all. Only use this if you're certain your value will be
small.

</div>

<div class="markdown level1 conceptual">

</div>

#### Declaration

``` lang-csharp
public static void WriteValuePacked(FastBufferWriter writer, short value)
```

#### Parameters

| Type             | Name   | Description            |
|------------------|--------|------------------------|
| FastBufferWriter | writer | The writer to write to |
| System.Int16     | value  | Value to write         |

### WriteValuePacked(FastBufferWriter, Int32)

<div class="markdown level1 summary">

Write a signed int (Int32) as a ZigZag encoded varint to the buffer.

</div>

<div class="markdown level1 conceptual">

</div>

#### Declaration

``` lang-csharp
public static void WriteValuePacked(FastBufferWriter writer, int value)
```

#### Parameters

| Type             | Name   | Description            |
|------------------|--------|------------------------|
| FastBufferWriter | writer | The writer to write to |
| System.Int32     | value  | Value to write         |

### WriteValuePacked(FastBufferWriter, Int64)

<div class="markdown level1 summary">

Write a signed long (Int64) as a ZigZag encoded varint to the buffer.

</div>

<div class="markdown level1 conceptual">

</div>

#### Declaration

``` lang-csharp
public static void WriteValuePacked(FastBufferWriter writer, long value)
```

#### Parameters

| Type             | Name   | Description            |
|------------------|--------|------------------------|
| FastBufferWriter | writer | The writer to write to |
| System.Int64     | value  | Value to write         |

### WriteValuePacked(FastBufferWriter, SByte)

<div class="markdown level1 summary">

Write a signed byte to the buffer.

</div>

<div class="markdown level1 conceptual">

</div>

#### Declaration

``` lang-csharp
public static void WriteValuePacked(FastBufferWriter writer, sbyte value)
```

#### Parameters

| Type             | Name   | Description            |
|------------------|--------|------------------------|
| FastBufferWriter | writer | The writer to write to |
| System.SByte     | value  | Value to write         |

### WriteValuePacked(FastBufferWriter, Single)

<div class="markdown level1 summary">

Write single-precision floating point value to the buffer as a varint

</div>

<div class="markdown level1 conceptual">

</div>

#### Declaration

``` lang-csharp
public static void WriteValuePacked(FastBufferWriter writer, float value)
```

#### Parameters

| Type             | Name   | Description            |
|------------------|--------|------------------------|
| FastBufferWriter | writer | The writer to write to |
| System.Single    | value  | Value to write         |

### WriteValuePacked(FastBufferWriter, String)

<div class="markdown level1 summary">

Writes a string in a packed format

</div>

<div class="markdown level1 conceptual">

</div>

#### Declaration

``` lang-csharp
public static void WriteValuePacked(FastBufferWriter writer, string s)
```

#### Parameters

| Type             | Name   | Description            |
|------------------|--------|------------------------|
| FastBufferWriter | writer | The writer to write to |
| System.String    | s      | The value to pack      |

### WriteValuePacked(FastBufferWriter, UInt16)

<div class="markdown level1 summary">

Write an unsigned short (UInt16) as a varint to the buffer. WARNING: If
the value you're writing is \> 2287, this will use MORE space (3 bytes
instead of 2), and if your value is \> 240 you'll get no savings at all.
Only use this if you're certain your value will be small.

</div>

<div class="markdown level1 conceptual">

</div>

#### Declaration

``` lang-csharp
public static void WriteValuePacked(FastBufferWriter writer, ushort value)
```

#### Parameters

| Type             | Name   | Description            |
|------------------|--------|------------------------|
| FastBufferWriter | writer | The writer to write to |
| System.UInt16    | value  | Value to write         |

### WriteValuePacked(FastBufferWriter, UInt32)

<div class="markdown level1 summary">

Write an unsigned int (UInt32) to the buffer.

</div>

<div class="markdown level1 conceptual">

</div>

#### Declaration

``` lang-csharp
public static void WriteValuePacked(FastBufferWriter writer, uint value)
```

#### Parameters

| Type             | Name   | Description            |
|------------------|--------|------------------------|
| FastBufferWriter | writer | The writer to write to |
| System.UInt32    | value  | Value to write         |

### WriteValuePacked(FastBufferWriter, UInt64)

<div class="markdown level1 summary">

Write an unsigned long (UInt64) to the buffer.

</div>

<div class="markdown level1 conceptual">

</div>

#### Declaration

``` lang-csharp
public static void WriteValuePacked(FastBufferWriter writer, ulong value)
```

#### Parameters

| Type             | Name   | Description            |
|------------------|--------|------------------------|
| FastBufferWriter | writer | The writer to write to |
| System.UInt64    | value  | Value to write         |

### WriteValuePacked(FastBufferWriter, Vector2)

<div class="markdown level1 summary">

Convenience method that writes two varint floats from the vector to the
buffer

</div>

<div class="markdown level1 conceptual">

</div>

#### Declaration

``` lang-csharp
public static void WriteValuePacked(FastBufferWriter writer, Vector2 vector2)
```

#### Parameters

| Type             | Name    | Description            |
|------------------|---------|------------------------|
| FastBufferWriter | writer  | The writer to write to |
| Vector2          | vector2 | Vector to write        |

### WriteValuePacked(FastBufferWriter, Vector3)

<div class="markdown level1 summary">

Convenience method that writes three varint floats from the vector to
the buffer

</div>

<div class="markdown level1 conceptual">

</div>

#### Declaration

``` lang-csharp
public static void WriteValuePacked(FastBufferWriter writer, Vector3 vector3)
```

#### Parameters

| Type             | Name    | Description            |
|------------------|---------|------------------------|
| FastBufferWriter | writer  | The writer to write to |
| Vector3          | vector3 | Vector to write        |

### WriteValuePacked(FastBufferWriter, Vector4)

<div class="markdown level1 summary">

Convenience method that writes four varint floats from the vector to the
buffer

</div>

<div class="markdown level1 conceptual">

</div>

#### Declaration

``` lang-csharp
public static void WriteValuePacked(FastBufferWriter writer, Vector4 vector4)
```

#### Parameters

| Type             | Name    | Description            |
|------------------|---------|------------------------|
| FastBufferWriter | writer  | The writer to write to |
| Vector4          | vector4 | Vector to write        |

### WriteValuePacked\&lt;TEnum&gt;(FastBufferWriter, TEnum)

<div class="markdown level1 summary">

Write a packed enum value.

</div>

<div class="markdown level1 conceptual">

</div>

#### Declaration

``` lang-csharp
public static void WriteValuePacked<TEnum>(FastBufferWriter writer, TEnum value)
    where TEnum : struct, Enum
```

#### Parameters

| Type             | Name   | Description            |
|------------------|--------|------------------------|
| FastBufferWriter | writer | The writer to write to |
| TEnum            | value  | The value to write     |

#### Type Parameters

| Name  | Description  |
|-------|--------------|
| TEnum | An enum type |
