# Public VulnScan reusable workflow

This directory is the source for the public repository
`Tanay-Ko/vulnscan-workflows`. Copy its contents into that public GitHub repository, then create
and maintain the `v1` release tag referenced by VulnScan-generated caller workflows.

The reusable workflow scans the calling repository, removes secret-bearing fields from Gitleaks
JSON, and uploads the machine-readable reports as a seven-day Actions artifact. VulnScan's
authenticated backend imports that artifact and generates the private PDF stored in Supabase.

The GitHub App that opens caller-workflow pull requests needs Contents: read and write and Pull
requests: read and write permissions. It must not write or modify any other repository files.
