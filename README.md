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
>![1b](https://user-images.githubusercontent.com/90601251/170880023-b719626b-bbb1-485b-82f2-8cad61de92be.png)

>Tentukanlah apakah terdapat pengaruh yang signifikan secara statistika
dalam hal kadar saturasi oksigen , sebelum dan sesudah melakukan
aktivitas 𝐴 jika diketahui tingkat signifikansi 𝛼 = 5% serta H0 : “tidak ada
pengaruh yang signifikan secara statistika dalam hal kadar saturasi
oksigen , sebelum dan sesudah melakukan aktivitas 𝐴”
