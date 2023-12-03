># Lecture 11
![](./%D0%91%D0%B5%D0%B7%20%D0%BD%D0%B0%D0%B7%D0%B2%D0%B0%D0%BD%D0%B8%D1%8F%20(2).png)
># Table of content;
## 1.Base 64;
## 2.new FileReader;
># What is base 64 used for;
## Asosan base 64 baroi ramzguzori malumonhoi dui iane binari lodho istifoda meshavad;
![](./download.jpg)
># About addEventListener;
## addEventListener method iak namud hodisai ast ki az tarafi igon kas angom meiobad dar parametrash 3 chiz kabul mekad(type ,  callback , useCapture)
># what is FileReader;
## FileReader in iak objecte hast ki silkai shumoro tavre megardonad ki asinkhroni onro khonda tavonad; filereader bo khud iak methode dorad ki nomi on readAsDataUrl meboshad; va result on boshad dar kluchivoi slova result malum ast;
```
for example;
fileInp.addEventListener("change", (e) => {
  let file = e.target.files[0];
  console.log(file);
  let reader = new FileReader();
  reader.readAsDataURL(file);

  console.log(reader.result);

  btn.onclick = async (e) => {
    try {
      let { data } = await axios.post("http://localhost:3000/data", {
        img: reader.result,
        name: textInp.value,
      });
    } catch (error) {
      console.log(error);
    }
  };
});

```