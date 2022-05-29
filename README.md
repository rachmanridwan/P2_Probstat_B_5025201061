# P2_Probstat_B_5025201061

## Nama-NRP
| Nama                | NRP        |
|---------------------|------------|
|   Rachman Ridwan    | 5025201061 |

## Soal 1
>Carilah Standar Deviasi dari data selisih pasangan pengamatan tabel diatas
```R
data <- data.frame(responden,x,y)
standar_deviasi <- sd(data$x - data$y)

print("standar deviasi =  ")
standar_deviasi
```
>
![1a](https://user-images.githubusercontent.com/90601251/170879976-12b79207-1069-4f46-a7c4-15cdbce2e341.png)

>Carilah nilai t (p-value)
```R
h <- data$x - data$y
n <- 6
s <- sd(h[1:6])
mean1 <- mean(h)
zbar <- mean(h[1:6])
t <- ((zbar - mean1)/(s/sqrt(n)))
p <- (2*pt(-abs(t),df <- n-1))

print("t(p - value) = ")
t
p
```
>
![1b](https://user-images.githubusercontent.com/90601251/170880023-b719626b-bbb1-485b-82f2-8cad61de92be.png)

>Tentukanlah apakah terdapat pengaruh yang signifikan secara statistika
dalam hal kadar saturasi oksigen , sebelum dan sesudah melakukan
aktivitas 𝐴 jika diketahui tingkat signifikansi 𝛼 = 5% serta H0 : “tidak ada
pengaruh yang signifikan secara statistika dalam hal kadar saturasi
oksigen , sebelum dan sesudah melakukan aktivitas 𝐴”

## Soal 2
## Soal 3
>H0 dan H1
```R
library(mosaic)

# 3A
print("Nilai dari H0 dan H1 adalah ")
zH0 <- (3.64-0)/(1.67/sqrt(19))
zH1 <- (2.79-0)/(1.32/sqrt(27))

zH0
zH1
```
>
![3a](https://user-images.githubusercontent.com/90601251/170881216-660417f1-c3b2-4a0a-8463-65d1b25bb45d.png)

>Hitung Sampel Statistik
```R
print("Hitungan sampel statistik adalah ")
tsum.test(mean.x=3.64, s.x = 1.67, n.x = 19,
          mean.y =2.79 , s.y = 1.32, n.y = 27,
          alternative = "greater")
```
>
![3b](https://user-images.githubusercontent.com/90601251/170881496-ba9d95e3-d605-4dd3-b761-0e877618a93d.png)

>Lakukan Uji Statistik (df =2)
```R
print("hasil dari point C ")
uji_statistik <- plotDist(dist='t',df=2,  col="red")
uji_statistik
```
>
![3c](https://user-images.githubusercontent.com/90601251/170881355-9a98d2ea-4787-4c07-9025-501a24fd3ae8.png)

>Nilai Kritikal
```R
print("Nilai kritikal = ")
nilai_kritikal <- qchisq(p = 0.05, df = 2, lower.tail=FALSE)
nilai_kritikal
```
>
![3d](https://user-images.githubusercontent.com/90601251/170881639-0b3efc14-2cad-48f7-b061-26af16f26385.png)

## Soal 4
## Soal 5
