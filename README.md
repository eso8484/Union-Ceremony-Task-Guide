# Union Testnet Ceremony Task Guide

This guide explains how to participate in the Union Testnet's **Trusted Setup Ceremony Task** on the Union Dashboard. Completing this task contributes to securing Union’s zero-knowledge interoperability layer and earns you XP on the dashboard.

## Prerequisites
- A supported wallet (e.g., MetaMask, Keplr) connected to the Union Dashboard.
- Accounts on X, Discord, and GitHub (for dashboard login and verification).
- A computer with Docker installed (Linux or macOS recommended).
- Internet access.

## Steps to Participate

1. **Access the Dashboard**
   - Go to [dashboard.union.build](https://dashboard.union.build).
   - Sign in with your X, Discord, or GitHub account.
   - Connect your wallet (e.g., MetaMask or Keplr) when prompted.

2. **Navigate to Missions**
   - On the dashboard, click the **"Missions"** tab.
   - Locate the **"Trusted Setup Ceremony"** task. If it’s not visible, ensure you’ve joined the Union Discord for updates on availability.

3. **Start the Ceremony Task**
   - Click the task to view details. It will direct you to [ceremony.union.build](https://ceremony.union.build).
   - If the public phase isn’t active, join the waitlist and wait for an email (sent 12-18 hours before the public phase starts).

4. **Set Up Docker**
   - Install Docker if you haven’t already:
     - Linux: `sudo apt install docker.io`
     - macOS: Download from [orbstack.dev](https://orbstack.dev) (for Apple Silicon or Intel).
   - Verify Docker is running: `docker --version`.


## 🐳 Optional: Participate Using Docker

For more advanced users, you can run the MPC client locally:

```bash
sudo mkdir -p ceremony && \
sudo docker pull ghcr.io/unionlabs/union/mpc-client:v1.2 && \
sudo docker run -v $(pwd)/ceremony:/ceremony -w /ceremony -p 4919:4919 --rm -it ghcr.io/unionlabs/union/mpc-client:v1.2

5. **Contribute Randomness**
   - Follow the instructions on [ceremony.union.build](https://ceremony.union.build):
     - Run the provided Dockerized application in your terminal:
       ```bash
       docker run --rm -it unionceremony/mpc-client
       ```
     - The app generates randomness and a GPG key, then submits your contribution to the MPC Coordinator.
   - Store your private GPG key safely (you’ll need it to prove your contribution later).

6. **Complete the Task**
   - After submitting, return to the dashboard.
   - The task should automatically mark as completed, awarding **65 XP** (or the current XP value).
   - Optionally, tweet your attestation on X to verify your contribution publicly.

## Troubleshooting
- **Docker Issues**: Ensure Docker is installed and running. Use `sudo` if permissions are denied.
- **Task Not Showing**: Join the [Union Discord](https://discord.gg/union) and check `#announcements` for updates.
- **Contribution Fails**: Retry the Docker command or contact support on Discord.

## Notes
- The Trusted Setup Ceremony is time-sensitive. The public phase follows a private phase for builders, so act quickly once it’s live.
- Only one honest contribution is needed for security, but every participant strengthens the system.

## Resources
- Dashboard: [dashboard.union.build](https://dashboard.union.build)
- Ceremony Site: [ceremony.union.build](https://ceremony.union.build)
- Docs: [docs.union.build](https://docs.union.build)
- Discord: [discord.gg/union](https://discord.gg/union)

Happy contributing!
