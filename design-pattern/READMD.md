# Design Pattern

我們在說程式架構時，不只是在說每一行、每一個 function 該怎麼寫得好 (因為這是基本的)，而是這些一個個軟體模組如何能用漂亮、優雅、美妙的方式建出的一個良好的「軟體大樓」，所以良好的程式碼不等於良好的構架。

「我們可以用大量精心製作的磚塊來製造垃圾」- Robert C. Martin

那當我們有了精心製作的磚塊，我們又該何去何從？這就是我們這系列文章的主題，SOLID 原則。

SOLID 原則告訴我們，該如何將我們的 data 與 Function 安排到類別中，以及這些類別該如何相互關聯。

這裡的類別是泛指任何 data 與 Function 的集合，而不只是單指 OO 類別的軟體架構。在網路上有很多講 SOLID 原則的文章，但很少有指出「類別」的到底是指什麼，很多人也會誤會「類別」是真的指 OO 的 Class ，但實則並非如此！

在 Clean Architecture 書中有提到，SOLID 原則目標是建立中層級的軟體結構，而「中層級」是指這些原則是程式設計師在模組層級工作時應用的原則。它們應用在程式碼層級之上，並且有助於定義模組和元件內使用的軟體結構類型。

這「中層級」就是我們上文說到的「類別」，是 data 與 function 的集合。所以是在程式碼層級之上，如 OO 中的類別就是一個中層級模組。而SOLID 原則就是為他們而服務，讓我們可以透過這些原則寫出能容忍變化、易於理解，且能被模組使用的良好「地基」。

所以，說了這麼多，我們要來了解一下 SOLID 是什麼。

SOLID 是5大原則的簡稱，分別為：
S = Single-responsibility principle (SRP) = 單一職責原則
O = Open–closed principle (OCP) = 開放封閉原則
L =Liskov substitution principle (LSP) = 里氏替換原則
I = Interface segregation principle (ISP) = 介面隔離原則
D = Dependency inversion principle (DIP) = 依賴反向原則

Ref: [使人瘋狂的 SOLID 原則](https://medium.com/%E7%A8%8B%E5%BC%8F%E6%84%9B%E5%A5%BD%E8%80%85/%E4%BD%BF%E4%BA%BA%E7%98%8B%E7%8B%82%E7%9A%84-solid-%E5%8E%9F%E5%89%87-%E7%9B%AE%E9%8C%84-b33fdfc983ca)