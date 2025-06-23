<h1>しりとり</h1>
<input id="nextWordInput" type="text"/>
<button id="nextWordSendButton">送信</button>
<p id="previousWord"></p>

<script>
window.onload = async (event) => {
    const response = await fetch("/shiritori", { method: "GET" });
    const previousWord = await response.text();
    const paragraph = document.querySelector("#previousWord");
    paragraph.innerHTML = `前の単語: ${previousWord}`;
};

document.querySelector("#nextWordSendButton").onclick = async (event) => {
    const nextWordInput = document.querySelector("#nextWordInput");
    const nextWordInputText = nextWordInput.value;

    const response = await fetch("/shiritori", {
        method: "POST",
        headers: { "Content-Type": "application/json" },
        body: JSON.stringify({ nextWord: nextWordInputText })
    });

    if (response.status !== 200) {
        const errorJson = await response.text();
        const errorObj = JSON.parse(errorJson);
        alert(errorObj["errorMessage"]);
        return;  // エラー時はここで処理を終わる
    }

    const previousWord = await response.text();
    const paragraph = document.querySelector("#previousWord");
    paragraph.innerHTML = `前の単語: ${previousWord}`;
    nextWordInput.value = "";
};
</script>
</body>
</html>
~                                                                                          ~           
