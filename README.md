<h1 align="center"> ft_printf</h1>

<div style="height: 40px;"></div>

---

## 📘 Description

The goal of this project is to recreate the <code>printf()</code> function from the C standard library, implementing formatted output and handling various data types — to better understand how formatted output works at a low level.

<div style="height: 60px;"></div>

---

## 🧠 Project Objectives

✅ Recreate part of the original <code>printf</code> behavior.  
✅ Work with **variadic functions** (<code>va_list</code>, <code>va_start</code>, <code>va_arg</code>, <code>va_end</code>).  
✅ Implement **formatting for strings, integers, hexadecimals, and pointers**.  
✅ Ensure **memory safety** and **clean, readable code**.  

<div style="height: 60px;"></div>

---

## ⚙️ Implemented Conversions

| Conversion | Description |
|-------------|-------------|
| `%c` | Character |
| `%s` | String |
| `%p` | Pointer (address in hexadecimal) |
| `%d` / `%i` | Signed integer |
| `%u` | Unsigned integer |
| `%x` / `%X` | Hexadecimal integer (lowercase / uppercase) |
| `%%` | Prints a literal `%` symbol |

<div style="height: 80px;"></div>

