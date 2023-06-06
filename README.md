# TTS | Voice Text-to-Speech API

**Description:** The Voice Text-to-Speech (TTS) API allows conversion of textual content to speech easier than ever. Just connect to our Text-to-Speech (TTS) API with a few lines of code and get verbal representation of a textual content.

**URL:** https://rapidapi.com/zilinskivan/api/text-to-speech-tts-engine

**Demo (EN):** https://20fix.com/xtts/1288585753.mp3

**Languages Supported:** ru, en, de, fr, es, it, nl, zh

**Code Samples:**

**- HTTP:**

<pre>GET /?t=Here%20is%20a%20text%20to%20be%20converted.&l=en HTTP/1.1
X-Rapidapi-Key: Your Key
X-Rapidapi-Host: text-to-speech-tts-engine.p.rapidapi.com
Host: text-to-speech-tts-engine.p.rapidapi.com</pre>

**- Node.js**

<pre>
const axios = require('axios');

const options = {
  method: 'GET',
  url: 'https://text-to-speech-tts-engine.p.rapidapi.com/',
  params: {
    t: 'Here is a text to be converted.',
    l: 'en'
  },
  headers: {
    'X-RapidAPI-Key': 'Your Key',
    'X-RapidAPI-Host': 'text-to-speech-tts-engine.p.rapidapi.com'
  }
};

try {
	const response = await axios.request(options);
	console.log(response.data);
} catch (error) {
	console.error(error);
}
</pre>

**- Javascript**

<pre>
const data = null;

const xhr = new XMLHttpRequest();
xhr.withCredentials = true;

xhr.addEventListener('readystatechange', function () {
	if (this.readyState === this.DONE) {
		console.log(this.responseText);
	}
});

xhr.open('GET', 'https://text-to-speech-tts-engine.p.rapidapi.com/?t=Here%20is%20a%20text%20to%20be%20converted.&l=en');
xhr.setRequestHeader('X-RapidAPI-Key', 'Your Key');
xhr.setRequestHeader('X-RapidAPI-Host', 'text-to-speech-tts-engine.p.rapidapi.com');

xhr.send(data);
</pre>

**- GO**

<pre>
package main

import (
	"fmt"
	"net/http"
	"io"
)

func main() {

	url := "https://text-to-speech-tts-engine.p.rapidapi.com/?t=Here%20is%20a%20text%20to%20be%20converted.&l=en"

	req, _ := http.NewRequest("GET", url, nil)

	req.Header.Add("X-RapidAPI-Key", "Your Key")
	req.Header.Add("X-RapidAPI-Host", "text-to-speech-tts-engine.p.rapidapi.com")

	res, _ := http.DefaultClient.Do(req)

	defer res.Body.Close()
	body, _ := io.ReadAll(res.Body)

	fmt.Println(res)
	fmt.Println(string(body))

}
</pre>

**- PHP**

<pre>
<?php

$curl = curl_init();

curl_setopt_array($curl, [
	CURLOPT_URL => "https://text-to-speech-tts-engine.p.rapidapi.com/?t=Here%20is%20a%20text%20to%20be%20converted.&l=en",
	CURLOPT_RETURNTRANSFER => true,
	CURLOPT_ENCODING => "",
	CURLOPT_MAXREDIRS => 10,
	CURLOPT_TIMEOUT => 30,
	CURLOPT_HTTP_VERSION => CURL_HTTP_VERSION_1_1,
	CURLOPT_CUSTOMREQUEST => "GET",
	CURLOPT_HTTPHEADER => [
		"X-RapidAPI-Host: text-to-speech-tts-engine.p.rapidapi.com",
		"X-RapidAPI-Key: Your Key"
	],
]);

$response = curl_exec($curl);
$err = curl_error($curl);

curl_close($curl);

if ($err) {
	echo "cURL Error #:" . $err;
} else {
	echo $response;
}
</pre>
