

- InputStream超类

- FileInputStream(String filepath).read(byte[])

- BufferedInputStream(new FileInputStream(Fpath)).read(bytes[])

字符流
- InputSteamReader(FileInputStream).read(char[])

---

- OutputSteam超类

- FileOutputStream(String filepath,append).write(byte[],off,len)

- BufferedOutputStream(new FileOutputStream(Fpath)).write(S.getBytes())

字符流
- FileOutputWriter(FileOutputSteam).write(String,off,len)


---
字符集(编码)

- String.getBytes(String charsetName)

---
便捷流
- FileReader(fpath)
- FileWriter(fpath)

- BufferedReader(FileReader()).readLine()
- BufferedWriter(FileWriter()).newline()   //.flush