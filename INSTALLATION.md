# Installation Guide

## Quick Install

### Option 1: Install from GitHub (Recommended)

1. Open Kiro
2. Open the Powers panel (Command Palette → "Kiro: Open Powers")
3. Click "Install from URL"
4. Enter your GitHub repository URL
5. Click "Install"

### Option 2: Manual Installation

1. Clone or download this repository
2. Copy the entire folder to your Kiro powers directory:
   - macOS/Linux: `~/.kiro/powers/aws-dev-best-practices/`
   - Windows: `%USERPROFILE%\.kiro\powers\aws-dev-best-practices\`
3. Restart Kiro or reload powers

## Verification

After installation, verify the power is active:

1. Open Kiro Powers panel
2. Look for "AWS Development Best Practices" in the installed powers list
3. Ensure it shows as "Active"

## Usage

Once installed, all steering files are automatically included in your Kiro context when working on AWS projects. The guidelines will be applied automatically when:

- Creating AWS infrastructure
- Writing Python or React code
- Deploying to AWS
- Building agentic applications
- Creating architecture diagrams
- Committing code

## Customization

To customize for your organization:

1. Fork this repository
2. Edit steering files in the `steering/` directory
3. Update `POWER.md` with your organization's information
4. Share the forked repository with your team

## Troubleshooting

**Power not showing up?**
- Ensure the folder structure is correct
- Restart Kiro
- Check the Kiro logs for errors

**Steering files not being applied?**
- Verify the power is marked as "Active"
- Check that steering files are in the `steering/` directory
- Ensure file names match those listed in `power.json`

## Support

For issues or questions:
- Check the README.md for documentation
- Review individual steering files for specific guidelines
- Consult AWS documentation for service-specific details
