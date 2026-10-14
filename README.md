# Notion for Grain

A Grain-authored definition and store listing for [Notion's official hosted MCP
server](https://developers.notion.com/guides/mcp/get-started-with-mcp) at
`https://mcp.notion.com/mcp`. Notion operates the tools. No worker, local MCP
process, JavaScript dependencies or custom Notion API implementation.

## Status

Version 0.1.0 is an unpublished candidate. Validation/packing, signed publication,
browser sign-in and live Agent acceptance are separate; the latter steps are
not claimed complete.

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

The output is `com.grain.notion-0.1.0.mcp.json`. `DESCRIPTION.md` is store copy,
README is author documentation and `media/cover.webp` identifies the integration.
See `assets/README.md` for original artwork provenance and separate brand terms.

Commit and tag reviewed source, then `grain-ext submit` using the actual full
source commit, tag and registry checkout. Follow the existing source-review,
attestation, signing and complete-catalogue publication route. This candidate
has no approval to reuse the GitHub-only tester exception.

## Bounded live checkpoint

After publication and browser approval: verify install/sign-in, discovery, one
test-page read/create/edit, recovery after restart and GitHub/Notion selection
without crossing accounts. Use existing normal tests for ownership/contract faults.
No second test engine or exhaustive Notion API matrix. Never replay uncertain writes.

## License

Metadata/documentation are MIT licensed. Notion artwork is excluded. This is a
Grain integration, not a Notion-authored or Notion-endorsed extension.
