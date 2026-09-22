Google Search Console ownership proof for alacrity-dev.vercel.app, which is
what Play Console checks the developer website against.

It is a directory rather than a file on purpose. `cleanUrls` in vercel.json
turns every `/x.html` request into a 308 to `/x`, and Google asks for the
exact `.html` URL. A directory of this name serves its index.html at
`/google1e82d958ace4c239.html` with a 200, which is what the check wants.

Google says to leave it in place after verification; removing it revokes the
verification, and with it the developer-website check.
