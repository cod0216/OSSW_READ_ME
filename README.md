# ๐ ์กฐ์ฌ๋ด์ฉ READMEํ์ผ๋ก ์ ๋ฆฌํ๊ธฐ
๐๊ด๊ธฐ์  ๊ณตํ๊ณผ 20161682 ์ต์์ฐฝ

## ๋ชฉ์ฐจ

+ [top ๋ช๋ น์ด](#%EF%B8%8F-top-๋ช๋ น์ด)

+ [ps ๋ช๋ น์ด](#%EF%B8%8F-ps-๋ช๋ น์ด)

+ [jobs ๋ช๋ น์ด](#%EF%B8%8F-jobs-๋ช๋ น์ด)

+ [kill ๋ช๋ น์ด](#%EF%B8%8F-kill-๋ช๋ น์ด)

+ [vim ๋งคํฌ๋ก](#vim-์๋ํฐ์์-๋งคํฌ๋ก-ํ์ฉ๋ฐฉ๋ฒ)

## top, ps, jobs, kill ๋ช๋ น์ด

### โ๏ธ top ๋ช๋ น์ด

top ๋ช๋ น์ด๋ ๋ฆฌ๋์ค ๊ณ์ด ์๋ฒ์ OS ์ํ๋ฅผ ํ์ธํ  ์ ์๋ CLI ์ดํ๋ฆฌ ์ผ์ด์์ด๋ค.

top ๋ช๋ น์ด๋ฅผ ํตํด ์๋ฒ์ CPU ์ฌ์ฉ๋, ๋ฉ๋ชจ๋ฆฌ ์ฌ์ฉ๋ ๋ฑ์ ํ์ธํ  ์ ์๋ค

 * #### ์ฌ์ฉ๋ฒ

๋ฆฌ๋์ค์์ top ๋ช๋ น์ด๋ฅผ ์น๊ณ  ๋ค์ด๊ฐ๋ฉด ๋๋ค. 

` $ top `


<img width="1440" alt="แแณแแณแแตแซแแฃแบ 2022-05-29 แแฉแแฎ 6 40 23" src="https://user-images.githubusercontent.com/83526046/170861804-f13387a4-34fd-4409-bffe-7eea0c4c0067.png">
 


์ ๊ทธ๋ฆผ์ฒ๋ผ top๋ช๋ น์ด๋ ***์๋ถ๋ถ***๊ณผ ***์๋ซ๋ถ๋ถ***์ผ๋ก ๋๋์ด ๋ณผ ์ ์๋ค. 

์ ๋ถ๋ถ์ ์ฃผ๋ก ํ์ฌ ์์คํ์ ์ํ๋ฅผ ๋ณด์ฌ์ฃผ๋๋ฐ, ์์คํ ์๊ฐ์ด๋ uptime ๋ฑ์ ํ์ธ ํด ๋ณผ ์ ์๊ณ 

์๋ซ๋ถ๋ถ์ ํ์ฌ ์คํํ๊ณ  ์๋ ํ๋ก์ธ์ค ํํฉ์ ๋ณผ ์ ์๋ค.

* #### Top ์ ๋ณด ์์คํ ๋ด์ฉ

|๋ด์ฉ|์ค๋ช|
|:----:|:----|
|18:40:23|ํ์ฌ ์๋ฒ์ ์๊ฐ|
|9 day, 5:24|uptime(์ผ์ ธ์๋์๊ฐ)|
|3 users|์ ์ |
|load average|ํ์ฌ ์์คํ์ด ์ผ๋ง๋ ์ผ์ ํ๊ณ  ์๋์ง 1๋ถ, 5๋ถ, 15๋ถ ๋จ์๋ก ์คํ/๋๊ธฐ ์ค์ธ ํ๋ก์ธ์ค ์๋ฅผ ๋ํ๋ด๊ณ  ์์|
|tasks|ํ๋ก์ธ์ค ๊ฐ์|

* #### CPU
|๋ด์ฉ|์ค๋ช|
|:----:|:----|
|%us|์ ์ ๋ ๋ฒจ์์ ์ฌ์ฉํ๊ณ  ์๋ CPU ๋น์ค|
|%sy|์์คํ ๋ ๋ฒจ์์ ์ฌ์ฉํ๊ณ  ์๋ CPU ๋น์ค|
|%id|์ ํด ์ํ์ CPU ๋น์ค|
|%wa|์์คํ์ด I/O ์์ฒญ์ ์ฒ๋ฆฌํ์ง ๋ชปํ ์ํ์์์ CPU idle ์ํ์ธ ๋น์ค|
|tasks|ํ๋ก์ธ์ค ๊ฐ์|

>์ผ๋ฐ์ ์ผ๋ก %us์ %sy๋ฅผ ๋ํ ๊ฐ์ด CPU ์ฌ์ฉ๋ฅ ์ด๋ผ๊ณ  ๋ณด๋ฉด ๋๋ฉฐ, id ๊ฐ์ด ์ฌ์  cpu๋ผ๊ณ  ๋ณด๋ฉด ๋๋ค.
>๊ทธ ์ธ์ wa ๋ ni ๋ฑ์ ๊ฐ๋ค์ด ํฌ๋ค๋ฉด ์์ธ ๋ถ์์ด ํ์ํ  ์ ์๋ค.









* #### ํ๋ก์ธ์ค 

|๋ด์ฉ|์ค๋ช|
|:----:|:----|
|PID|ํ๋ก์ธ์ค ID (PID)|
|USER|ํ๋ก์ธ์ค๋ฅผ ์คํ์ํจ ์ฌ์ฉ์ ID|
|PRI|ํ๋ก์ธ์ค์ ์ฐ์ ์์(priority)|
|NI|NICE ๊ฐ, ์ผ์ nice valuce๊ฐ์ด๋ค. ๋ง์ด๋์ค๋ฅผ ๊ฐ์ง๋ ncie value๋ ์ฐ์ ์์๊ฐ ๋์.|
|VIRT|๊ฐ์ ๋ฉ๋ชจ๋ฆฌ์ ์ฌ์ฉ๋(SWAP+RES)|
|RES|ํ์ฌ ํ์ด์ง๊ฐ ์์ฃผํ๊ณ  ์๋ ํฌ๊ธฐ(Resident Size)|
|SHR|๋ถํ ๋ ํ์ด์ง, ํ๋ก์ธ์ค์ ์ํด ์ฌ์ฉ๋ ๋ฉ๋ชจ๋ฆฌ๋ฅผ ๋๋ ๋ฉ๋ชจ๋ฆฌ์ ์ดํฉ.|
|S|ํ๋ก์ธ์ค์ ์ํ [S(sleeping), R(running), W(swapped out process), Z(zombies)]|
|%CPU|ํ๋ก์ธ์ค๊ฐ ์ฌ์ฉํ๋ CPU์ ์ฌ์ฉ์จ|
|%MEM|ํ๋ก์ธ์ค๊ฐ ์ฌ์ฉํ๋ ๋ฉ๋ชจ๋ฆฌ์ ์ฌ์ฉ์จ|
|COMMAND|์คํ๋ ๋ช๋ น์ด|

* #### Top ๋ช๋ น์ด ์ต์

๋จผ์  top ๋ช๋ น์ ์ดํ๋ฆฌ์ผ์ด์์ด๊ธฐ ๋๋ฌธ์ ์คํ ์ ์ต์๊ณผ ์คํ ํ ์ต์์ด ์๋ค.

|์ต์|์ค๋ช|
|:----:|:----|
|1|CPU ์ฝ์ด๋ณ ์ฌ์ฉ ํํฉ|
|m|๋ฉ๋ชจ๋ฆฌ ์ฌ์ฉ๋ฅ  ์๊ฐํ ํ์|
|shift+p|CPU ์ฌ์ฉ๋ฅ ์ด ๋์ ํ๋ก์ธ์ค๋ฅผ ๊ธฐ์ค์ผ๋ก ๋์ด|
|shift+m|๋ฉ๋ชจ๋ฆฌ ์ฌ์ฉ๋ฅ ์ด ๋์ ํ๋ก์ธ์ค๋ฅผ ๊ธฐ์ค์ผ๋ก ๋์ด|
|shift+t|์ํ ์๊ฐ์ด ๊ธด ํ๋ก์ธ์ค๋ฅผ ๊ธฐ์ค์ผ๋ก ๋์ด|
|k|kill ํ  ํ๋ก์ธ์ค PID๋ฅผ ์๋ ฅํ  ์ ์์|
|H|์๋จ์ Tasks ๊ธฐ์ค์ ์ฐ๋ ๋๋ก ๋ณ๊ฒฝ|
|u|๋ชจ๋ํฐ๋งํ  user๋ฅผ ์ ํํ์ฌ, ํด๋น ๊ถํ ํ๋ก์ธ์ค ๊ฐ์|

---
### โ๏ธ ps ๋ช๋ น์ด

<img width="399" alt="์คํฌ๋ฆฐ์ท 2022-05-25 ์ค์  9 16 01" src="https://user-images.githubusercontent.com/83526046/170152352-0ad1ec1f-d3f1-4983-ae49-bb34951e5c07.png">

ps๋ช๋ น์ด๋ ํ์ฌ ๋ฆฌ๋์ค ์์คํ์์ ์คํ ์ค์ธ ํ๋ก์ธ์ค์ ๋ํ ์ ๋ณด๋ค์ ์ถ๋ ฅํ๋ ๋ช๋ ์ด์ด๋ค.

> ์ด ๋ช๋ น์ด๋ฅผ ์์ฃผ ์ฌ์ฉํ๋ ์ด์ ๋ ํ๋ก์ธ์ค ์ฌ์ฉ์ ์ค์ง์ํฌ kill๋ช๋ น์ด๋ก ์ค์ง ์ํฌ๊ฒฝ์ฐ PID์ ๋ณด๊ฐ ํ์ํ๊ธฐ ๋๋ฌธ์ด๋ค.

|๋ด์ฉ|์ค๋ช|
|:----:|:----|
|PID|ํ๋ก์ธ์ค ID|
|TTY|ํ๋ก์ธ์ค ์์ถ๋ ฅ ๋ด๋น ํฐ๋ฏธ๋|
|TIME|๊ตฌ๋์๊ฐ|
|CMD|ํ๋ก์ธ์ค ์คํ ๋ช๋ น์ด|
 
 **-f ์ต์ ์ฌ์ฉ์**
 
|๋ด์ฉ|์ค๋ช|
|:----:|:----|
|UID|์คํ ์ ์ |
|PPID|๋ถ๋ชจ ํ๋ก์ธ์ค PID|
|C|CPU ์ฌ์ฉ๋|
|STIME|ํ๋ก์ธ์ค ์์ ์๊ฐ|

* #### ps ๋ช๋ น์ด ์ต์

` $ ps -[์ต์] `

|์ต์|์ค๋ช|
|:----:|:----|
|-e|๋ชจ๋  ํ๋ก์ธ์ค๋ฅผ ์ถ๋ ฅํด์ค๋ค.|
|-f|ํ ํฌ๋ฉง์ผ๋ก ๋ณด์ฌ๋๋ค.(UID, PID ๋ฑ)|
|-l|๊ธด ํฌ๋ฉง์ผ๋ก ๋ณด์ฌ์ค๋ค.|
|p,-p|ํน์  PID์ ํ๋ก์ธ์ค๋ฅผ ๋ณด์ฌ์ค๋ค.|
|-u|ํน์  ์ฌ์ฉ์์ ํ๋ก์ธ์ค๋ฅผ ๋ณด์ฌ์ค๋ค.|

---

### โ๏ธ jobs ๋ช๋ น์ด

jobs ๋ช๋ น์ด๋ ์ง์์ ์ํ๋ฅผ ํ์ํ๋ ๋ช๋ น์ด๋ค. ํ์ฌ ์ ์ธ์์์ ์คํ ์ํจ ๋ฐฑ ๊ทธ๋ผ์ด๋ ์์์ ๋ชฉ๋ก์ด ์ถ๋ ฅ๋๋ฉฐ, ๊ฐ ์์์๋ ๋ฒํธ๊ฐ ๋ถ์ด ์์ด kill ๋ช๋ น์ด ๋ค์ '%๋ฒํธ' ๋ฑ์ผ๋ก ์ฌ์ฉํ  ์ ์๋ค.

> job ๋ช๋ น์ด๋ ํ์ฌ ์ ํ๋ก์ธ์ค ์์ ๋ฐฑ ๊ทธ๋ผ์ด๋ ํ๋ก์ธ์ค๋ค์ ๋ณด์ฌ์ค๋ค๊ณ  ์๊ฐํ๋ฉด ๋๋ค.

<img width="916" alt="แแณแแณแแตแซแแฃแบ 2022-05-29 แแฉแแฎ 6 45 03" src="https://user-images.githubusercontent.com/83526046/170862862-7deeb15b-43ee-4a26-bdde-e0eb70c0ef83.png">


* #### ์ํ

|์ํ|์ค๋ช|
|:----:|:----|
|Running|์์์ด ๊ณ์ ์งํ์ค์|
|Done|์์์ด ์๋ฃ๋์ด 0์ ๋ฐํ|
|Done(code)|์์์ด ์ข๋ฃ๋์์ผ๋ฉฐ 0์ด ์๋ ์ฝ๋๋ฅผ ๋ฐํ|
|Stopped|์์์ด ์ผ์ ์ค๋จ|
|Stopped(SIGTSTP)|SIGTSTP ์๊ทธ๋์ด ์์์ ์ผ์ ์ค๋จ|
|Stopped(SIGSTOP)|SIGSTOP ์๊ทธ๋์ด ์์์ ์ผ์ ์ค๋จ|
|Stopped(SIGTTIN)|SIGTTIN ์๊ทธ๋์ด ์์์ ์ผ์ ์ค๋จ|
|Stopped(SIGTTOU)|SIGTTOU ์๊ทธ๋์ด ์์์ ์ผ์ ์ค๋จ|

* #### jobs ๋ช๋ น์ด ์ต์

`$ job [์ต์][์์๋ฒํธ] `

|์ต์|์ค๋ช|
|:----:|:----|
|-i|ํ๋ก์ธ์ค ๊ทธ๋ฃน ID๋ฅผ state ํ๋ ์์ ์ถ๋ ฅ|
|-n|ํ๋ก์ธ์ค ๊ทธ๋ฃน ์ค์ ๋ํ ํ๋ก์ธ์ค ID๋ฅผ ์ถ๋ ฅ|
|-p|๊ฐ ํ๋ก์ธ์ค ID์ ๋ํ ํ ๋ช์ฉ ์ถ๋ ฅ|
|command|์ง์ ํ ๋ช๋ น์ด๋ฅผ ์คํ|

---

### โ๏ธ kill ๋ช๋ น์ด

kill ๋ช๋ น์ด๋ ํ๋ก์ธ์ค๋ฅผ ๊ฐ์  ์ข๋ฃํ๋ ๋ช๋ น์ด์ด๋ค.

> ๋ฆฌ๋์ค์์ ์์์ ํ  ๋ ์์ฉํ๋ก๊ทธ๋จ์ด๋ ํ๋ก์ธ์ค๊ฐ ๋ฉ์ถ๋ ๊ฒฝ์ฐ๊ฐ ์๋๋ฐ ์ด๋ ์ ์ฉํ๊ฒ ์ฌ์ฉ ํ  ์ ์๋ ๋ช๋ น์ด ์ด๋ค.

<img width="1437" alt="แแณแแณแแตแซแแฃแบ 2022-05-29 แแฉแแฎ 7 14 59" src="https://user-images.githubusercontent.com/83526046/170862986-dabda231-b1b4-462e-a9dd-9582bcffacd2.png">

* #### kill ๋ช๋ น์ด ์ต์

`$ kill [์ต์] <PID>..`

|์ต์|์ค๋ช|
|:----:|:----|
|1|ํ๋ก์ธ์ค๋ฅผ ๋ค์ ๋ก๋|
|9|ํ๋ก์ธ์ค๋ฅผ ๊ฐ์  ์ข๋ฃ|
|15|ํ๋ก์ธ์ค๋ฅผ ์ ์์ ์ผ๋ก ์ค์ง|
|l|์ฌ์ฉ ๊ฐ๋ฅํ ๋ชจ๋  ์ ํธ ๋ชฉ๋ก|



## vim ์๋ํฐ์์ ๋งคํฌ๋ก ํ์ฉ๋ฐฉ๋ฒ

์ฐ์  vim ๋งคํฌ๋ก๋ฅผ ์์ํ๊ธฐ ์ ์ vim์ ๋ํด ์์๋ณด์ 

### vim์ด๋ ๋ฌด์์ธ๊ฐ? 

์ํค๋ฐฑ๊ณผ ๋ด์ฉ์ ์ธ์ฉํ๋ค

> Vim์ Bram Moolenaar๊ฐ ๋ง๋  vi ํธํ ํ์คํธ ํธ์ง๊ธฐ์ด๋ค. CUI์ฉ Vim๊ณผ GUI์ฉ gVim์ด ์๋ค. ๋ณธ๋ ์๋ฏธ๊ฐ ์ปดํจํฐ ์ฉ ํ๋ก๊ทธ๋จ์ด์์ผ๋ ํ์ฌ๋ ๋ง์ดํฌ๋ก์ํํธ ์๋์ฐ, ๋ฆฌ๋์ค, ๋งฅ ์ค์์ค ํ์ ๋น๋กฏํ ์ฌ๋ฌ ํ๊ฒฝ์ ์ง์ํ๋ค. 

์ฝ๊ฒ ๋ง CLI ํ๊ฒฝ์ ์ฌ์ฉ ๊ฐ๋ฅํ ํ์คํธ ํธ์ง๊ธฐ ์ด๋ค.

๊ทธ๋ผ ๋ณธ๊ฒฉ์ ์ผ๋ก vim ๋งคํฌ๋ก ๊ธฐ๋ฅ์ ๋ํด ์์๋ณด๊ฒ ๋ค.

**์ฌ์ฉ๋ฒ**

```
1) `q[name]` ๋ก ๋งคํฌ๋ก ๊ธฐ๋ก ์์
2) `q`๋ก ๋งคํฌ๋ก ๊ธฐ๋ก ์ข๋ฃ
3) `@[name]` ๋ก ์ ์ฅ๋ ๋งคํฌ๋ก ์คํ
4) `[number]@[name]`๋ก ๋งคํฌ๋ก ์ฌ๋ฌ๋ฒ ์คํ
```

### 2) q[name] ๋ก ๋งคํฌ๋ก ๊ธฐ๋ก ์์ `q`๋ก ๋งคํฌ๋ก ๊ธฐ๋ก ์ข๋ฃ

<img width="1440" alt="แแณแแณแแตแซแแฃแบ 2022-05-30 แแฉแแฎ 2 23 15" src="https://user-images.githubusercontent.com/83526046/170925300-33e779d1-d8b1-4680-9ce8-9c94ff410ddc.png">

Normal Mode ์์ qt, qg, qq ๋ฑ `q[name]` ์ ์๋ ฅํ  ๊ฒฝ์ฐ ์ ์ฌ์ง๊ณผ ๊ฐ์ด โ๊ธฐ๋ก์คโ ์ด๋ผ๋ ๊ธ์ ํ์ธ ํ  ์ ์๋ค.

์ผ๋ จ์ ๋์๋ค์ ์๋ ฅํ ๋ค ๋ค์ `q`๋ฅผ ์๋ ฅํ๋ฉด ๋งคํฌ๋ก ๊ธฐ๋ก์ด ์ข๋ฃ๋๋ค.

>ํ์๋ `qt dd q` ๋ฅผ ์๋ ฅํ์๋ค.

### 2) @[name] - Vim Macro ์คํํ๊ธฐ

`@[name]`์ผ๋ก ํน์  ๋ ์ง์คํฐ์ ์ ์ฅ๋ ๋งคํฌ๋ก๋ฅผ ์คํ์ํฌ ์๋ ์๊ณ , `@@`๋ก ์ง์ ์ ์คํํ ๋งคํฌ๋ก๋ฅผ ์ฌ ์คํํ  ์๋ ์๋ค. 

<img width="1440" alt="แแณแแณแแตแซแแฃแบ 2022-05-30 แแฉแแฎ 2 37 07" src="https://user-images.githubusercontent.com/83526046/170925361-5233edad-1b16-42a1-ae5e-bd2d85dc6a28.png">

์ ๊ทธ๋ฆผ์ฒ๋ผ qt์ dd๋ฅผ ๋๋ฌ 9๋ฒ ๋ผ์ธ์ ์ ๊ฑฐํ @t๋ฅผ ๋๋ฌ ์ ์ฅํ ๋งคํฌ๋ก๋ฅผ ์คํ์์ผ 8๋ฒ ๋ผ์ธ์ ์์ด์์ ํ์ธ ํ  ์ ์๋ค.

### 3) [number]@[name]๋ก ๋งคํฌ๋ก ์ฌ๋ฌ๋ฒ ์คํ

<img alt="แแณแแณแแตแซแแฃแบ 2022-05-30 แแฉแแฎ 2 38 20" src="https://user-images.githubusercontent.com/83526046/170925429-dbe94059-20e6-456e-be93-a5e15cea6cdc.png" width="500" heigh="500"> <img alt="แแณแแณแแตแซแแฃแบ 2022-05-30 แแฉแแฎ 2 38 37" src="https://user-images.githubusercontent.com/83526046/170925446-b7baeef4-b0a4-41dd-821f-fa1b1c686331.png" width="500" heigh="500">


์ ๋ ์ฌ์ง์ `qt`๋ฅผ ํตํด ๋ผ์ธ ์ง์ฐ๊ธฐ๋ฅผ ๋งคํฌ๋ก์ ์ ์ฅํ ๋งคํฌ๋ก๋ฅผ `2@t`๋ฅผ ํ์ฉํ์ฌ ์ฐ์์ผ๋ก ๋งคํฌ๋ก๊ฐ 2๋ฒ ์คํํ๊ฒ ํ์๋ค.

๋ณด๋ฉด ***6๋ผ์ธ๊ณผ 7๋ผ์ธ์ด ์ง์์ง๊ฑธ ํ์ธ*** ํ  ์ ์๋ค.

## ๐๋ง์น๋ฉฐ
top, jobs, ps, kill๋ฑ ํ๋ก์ธ์ ๊ด๋ฆฌ์ ํ์ํ ๋ช๋ น์ด๋ค์ ์์๋ณด๋ ์๊ฐ์ ๊ฐ์ก๋ค. 

๋ฆฌ๋์ค์์ ์ฌ์ฉ ๊ฐ๋ฅํ ๋ช๋ น์ด๋ค์ด์ง๋ง ๋ฉ๋ถ์ ์ฌ์ฉํ๊ณ  ์๋ ๋ํํ๋ ๋งค์ฐ ์ ์ฉํ ๋ช๋ น์ด๋ค์ด๊ธฐ์ ์ด๋ฒ ๊ณผ์ ๋ฅผ ํตํด ๊ณต๋ถํด๋ณด๊ณ  ๋์ค์ ๋ ์ถ๊ฐ์ ์ผ๋ก ๊ณต๋ถํ  ์ ์๋ ์๊ฐ์ ๊ฐ์ ธ์ผ๊ฒ ๋ค.

๋ํ vim ์๋ํฐ์ ๋งคํฌ๋ก ๊ฒฝ์ฐ ์ด ๊ธฐ๋ฅ์ ํ์ฉํ์ฌ ๋ณต์กํ๊ฑฐ๋ ํน์ ์ ์ฉํ ๊ธฐ๋ฅ์ ํ๋ ํค์ ์กฐํฉ๋ค์ ์ ์ฅํ์ฌ ํ์์ ๋ฐ๋ผ ๋ฐ๋ก ๊บผ๋ด ์ฌ์ฉ ํ  ์ ์๋ค. 

์ฃผ๋ก vim์ ์ฌ์ฉํ๊ธฐ ๋๋ฌธ์ ์ด ๊ธฐ๋ฅ์ ์ด๋ฒ ๊ธฐํ์ ํ์คํ ๋ฐฐ์๋๊ณ  ์์ฃผ ์ฌ์ฉํด์ผ๊ฒ ๋ค.

## ๐ก์ฐธ๊ณ 

 [Top](https://ironmask84.tistory.com/355 "top ๋ช๋ น์ด ์ฐธ๊ณ  ์ฌ์ดํธ")

 [Ps](https://jhnyang.tistory.com/268 "ps ๋ช๋ น์ด ์ฐธ๊ณ  ์ฌ์ดํธ")

 [Jobs](https://hbase.tistory.com/265 "ps ๋ช๋ น์ด ์ฐธ๊ณ  ์ฌ์ดํธ")

 [Kill](https://m.blog.naver.com/koromoon/220804715310 "kill ๋ช๋ น์ด ์ฐธ๊ณ  ์ฌ์ดํธ")

 [vim](https://ko.wikipedia.org/wiki/Vim "์๋ํฐ ์ฐธ๊ณ  ์ฌ์ดํธ")
