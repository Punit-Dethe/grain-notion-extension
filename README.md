# Notion for Grain

Candidate **0.1.2** corrects store copy that implied every Agent action opens an
approval dialog and updates the author instructions. URL, OAuth, tool behavior
and the 512×512 icon/three wide gallery images are unchanged. This candidate still
needs its own exact source approval, signing and public activation through the
maintained registry workflow. See [artwork sources](assets/README.md).

A Grain-authored definition and store listing for [Notion's official hosted MCP
server](https://developers.notion.com/guides/mcp/get-started-with-mcp) at
`https://mcp.notion.com/mcp`. Notion operates the tools. No worker, local MCP
process, JavaScript dependencies or custom Notion API implementation.

## Status

Version 0.1.1 is published to the tester catalogue at index 7, registry commit
`15b87cf75c36f5d330470196094738001a6b9426`. The user has also confirmed live
sign-in and representative search/read/create/edit actions in Grain. This does
not certify every Notion tool. See [verification](VERIFICATION.md) for historical
publication evidence and the new candidate's status. Existing release tags stay
immutable; documentation changes do not move them.

## Authentication

Notion documents OAuth with PKCE, refresh and dynamic client registration in its
[integration guide](https://github.com/makenotion/notion-cookbook/blob/main/docs/mcp-client-integration.md).
Grain's shared SDK/vault flow owns these operations. No GitHub-style OAuth app,
permanent website identity, packaged secret or user-created developer registration
is intended. The descriptor needs no `oauthClient` override or GitHub toolset header.

Install the published extension, sign in with Notion and enable its tools.
Access follows the user's Notion permissions and workspace/admin policies;
start acceptance with a disposable workspace. Do not promise page-specific scope
that the provider does not offer.

## Package and publish

From this directory, using Grain's maintained CLI:

```powershell
grain-ext doctor
grain-ext pack
```

The output is `com.grain.notion-0.1.2.mcp.json`. `DESCRIPTION.md` is store copy,
README is author documentation, `media/icon.png` is the square listing icon and
`media/cover.webp` is the first wide preview.
See `assets/README.md` for original artwork provenance and separate brand terms.

Commit and tag source, then `grain-ext submit --update-from 0.1.1` using the actual
full source commit, tag and registry checkout. Push the submission branch and use
`grain-ext pr` or a manual draft PR. Maintainers follow the registry's
[publication runbook](https://github.com/Punit-Dethe/Grain-Extention/blob/main/PUBLISHING.md)
for exact review, isolated preparation/attestation, local signing and activation.
This candidate does not inherit approval from previous Notion or GitHub versions.

## Bounded live checkpoint

After publication and browser approval: verify install/sign-in, discovery, one
test-page read/create/edit, recovery after restart and GitHub/Notion selection
without crossing accounts. Use existing normal tests for ownership/contract faults.
No second test engine or exhaustive Notion API matrix. Never replay uncertain writes.

## License

Metadata/documentation are MIT licensed. Notion artwork is excluded. This is a
Grain integration, not a Notion-authored or Notion-endorsed extension.
