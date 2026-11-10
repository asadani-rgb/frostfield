# FrostField

Self-hosted web app for generating AI video and images, forked from [Open Higgsfield](https://github.com/wide-trace/open-higgsfield). Connects to the Higgsfield API with your own keys, stores media in Vercel Blob, and supports optional fal.ai models for broader coverage.

## Features

- **Higgsfield API integration** - generate video and images from text and image prompts using the models exposed by the Higgsfield API.
- **fal.ai support (optional)** - add your fal.ai API key to access additional models that the Higgsfield API does not provide.
- **Vercel Blob storage** - reference images and generated media are stored in your own Vercel Blob container, so your assets stay under your control.
- **Bring your own keys** - API credentials are supplied by you and configured locally. Nothing is shared with a hosted backend.
- **Self-hosted** - runs locally as a web app, with no vendor lock-in.

## Getting Started

1. Clone the repository and install dependencies.
2. Create a Vercel Blob store and copy its read/write token.
3. Add your credentials to a `.env` file:

   ```
   HIGGSFIELD_API_KEY=your_key_here
   BLOB_READ_WRITE_TOKEN=your_vercel_blob_token
   FAL_KEY=your_fal_key_here   # optional
   ```

4. Start the app and open it in your browser.

## Windows Installer

A packaged Windows installer is available on the [Releases](../../releases) page. Each user must set up their own Vercel Blob storage and API keys on first run.

## Configuration

| Variable | Required | Purpose |
|---|---|---|
| `HIGGSFIELD_API_KEY` | Yes | Authenticates generation requests to Higgsfield |
| `BLOB_READ_WRITE_TOKEN` | Yes | Connects to your Vercel Blob container for uploads |
| `FAL_KEY` | No | Enables fal.ai models |

## Notes

Each user should provision their own Vercel Blob store and API keys. Generation usage is billed by the respective providers (Higgsfield, fal.ai, Vercel) to your own accounts.

## Credits

Forked from [open-higgsfield](https://github.com/wide-trace/open-higgsfield). All credit for the original project goes to its authors. This fork is not affiliated with Higgsfield or fal.ai.
