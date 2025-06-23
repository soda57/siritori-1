import { serveDir } from "jsr:@std/http/file-server";

let previousWord = "しりとり";

Deno.serve(async (_req) => {

    const pathname = new URL(_req.url).pathname;
    console.log(`pathname: ${pathname}`);

    // GET /shiritori → 単語を返す
    if (_req.method === "GET" && pathname === "/shiritori") {
        return new Response(previousWord);
    }

    // POST /shiritori → 単語を更新
    if (_req.method === "POST" && pathname === "/shiritori") {
        const requestJson = await _req.json();
        const nextWord = requestJson["nextWord"];
        if (previousWord.slice(-1) === nextWord.slice(0, 1)) {
            previousWord = nextWord;
        }
        return new Response(previousWord);
    }else{
            return new Response(
                    JSON.stringify({
                            "errorMessage":"前の単語に続いていません",
                            "errorCode":"10001"
                    }),
                    {
                            status:400,
                            headers:{"Content-Type":"application/json;charset=utf-8"},
                    }
            );
    }



    // その他 静的ファイルを返す
    return serveDir(_req);
