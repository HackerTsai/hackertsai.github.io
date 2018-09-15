---
layout: post
comments: true
title: 【程式概念簡單講】- 函式
---
函式，英文 function，可以將程式碼整合，並動態變更程式碼所需要的值。這樣就不用因為一樣的程式碼稍微不同、或需要重複使用而寫出冗長的程式碼，使程式不易維護。
#### 函式的宣告
這裡是一個 C# 函式的宣告，可以算出三個整數的總和：
```csharp
int sum(int a, int b, int c) {
    return a + b + c;
}
```
看不懂嗎？沒關係，讓我一個一個解釋：
- 開頭的 `int` 代表這個函示會傳回一個整數（**int**eger）。
- sum 是這個函式的名稱。
- 三個整數 `a`、`b`、`c` 是這個函式的「引數（arguments）」。
- 大括號 {} 內是函式所包含的程式碼。
- `return a + b + c;` 指的是「傳回 a 加 b 加 c 的結果」。

還看不懂？我用虛擬碼寫一次：
```
傳回類型整數 加總(整數 a, 整數 b, 整數 c) {
    傳回 a + b + c
}
```
容易理解多了吧！
#### 函式的使用
那我們要如何使用函式呢？很簡單，函式宣告完成後，使用 `sum(30, 26, 19);` 就可以了。
請注意，不一定要是「30, 26, 19」，可以是你想要加總的任何整數。

使用函式的動作我們稱為「呼叫函式（call function）」。
#### 發生了什麼？
當你使用 `sum(30, 26, 19);` 時，函式做了什麼？事實上，引數 `a`、`b`、`c` 依照順序被分別替換成 `30`、`26`、`19`，並以這個值執行它們應該執行的程式碼，也就是：
```csharp
return 30 + 26 + 19;
```
那括號裡的 `30`、`26`、`19` 有一個名字，叫「參數（parameters）」。

但大家一定還是搞不懂「傳回」是什麼意思，讓我來舉個例子：
```csharp
Console.WriteLine(sum(30, 26, 19)); // 輸出 30 + 26 + 19 的結果
```
這段程式實際上會執行：
```csharp
Console.WriteLine(30 + 26 + 19); // 輸出 30 + 26 + 19 的結果
```
也就是說，呼叫函式的動作會被替換成函式傳回的結果。

以下是完整的 C# 程式碼，供大家參考：
```csharp
using System;

class Program {

    static void Main(string[] args) {
        Console.WriteLine(sum(30, 26, 19));
    }

    int sum(int a, int b, int c) {
        return a + b + c;
    }
}
```
以下再補充 Python 和 JavaScript 的程式碼：

Python:
```python
def sum(a, b, c):
    return a + b + c

print(sum(30, 26, 19))
```
JavaScript:
```javascript
function sum(var a, var b, var c) {
    return a + b + c;
}
console.log(sum(30, 26, 19));
```
注意 Python 和 JavaScript 在宣告函式時不需要指定傳回型別，取而代之的是 `def`（Python）和 `function`（JavaScript）表明這是宣告的動作。

以上就是我對於函式的說明，相信大家是不是對它更加了解了呢？如果我的說明有誤，也煩請各位大大在下面留言指正，並繼續關注我喔！