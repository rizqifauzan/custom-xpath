## Custom Xpath

bahasa kueri untuk memilih bagian - bagian (nodes) dari sebuah dokumen XML

Untuk Automation Test Engineer, xpath digunakan untuk memilih elemen yang akan di interaksikan ( seperti di click, getText, set Text ataupun lainya )

## Cara menulis custom xpath

- Jalur / langkah
- Properties
- Predikat
- Hubungan / Relasi

## Jalur / Langkah

- `/` pilih elemen dari jalur akar
- `//` pilih elemen yang cocok terlepas dari lokasi mereka

contoh

```jsx
# Akar
/html/body/div[2]/form/div/div[2]/div[1]/input

# Non Akar
//div/input
```

## Properties

Menggunakan atribut / properties dari elemen untuk memilih element tersebut

- equals
- contains
- `starts-with`

contoh

```jsx
//input[@name='username']
//input[contains(@class,"form-control")]
//input[starts-with(@name, 'pass')]
```

## Perdikat

- Index
- Last

Contoh 

```jsx
//div[@id='home_module_list']/div[1]
//div[@id='home_module_list']/div[last()]
//div[@id='home_module_list']/div[last()-2]
```

## Hubungan / Relasi

- Parent
- following-sibling

Contoh

```jsx
//ul[li]
//li/parent::ul
//h1/following-sibling::ul
```

## Tips & Trik

- Gunakan xpath yang mudah dimengerti
- Gunakan xpath sependek mungkin

```arduino
# Before
//div[@class='css-j4yt6r']
/html/body/div[2]/form/div/div[2]/div[1]/input

# After
//div[@data-testid='divVarContainerBody']/div[1]
//input[@name='username']
```
