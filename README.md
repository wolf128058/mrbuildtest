# Lüllümons Cobblemon-Modrinth-Pack

## Wasch isch dasch?

Einfach nur 'ne Ansicht von den Änderungen.

Erzeugt mit:

    jq '
    .files |= sort_by(.path)
    | .files[].hashes |= {sha512: .sha512, sha1: .sha1}
    | .files[].env |= {client: .client, server: .server}
    ' modrinth.index.json > tmp.json && mv tmp.json modrinth.index.json

