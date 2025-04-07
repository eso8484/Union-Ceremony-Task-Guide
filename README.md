# ✨ How to Participate in the Union Ceremony

Welcome to the Union Labs Ceremony! This guide will walk you through how to participate in the ceremony using the Union Dashboard.

---

## 🧾 Requirements

Before you begin, make sure you have:

- A Union-compatible wallet (e.g., MetaMask)
- A reliable internet connection
- Docker installed (for local client option)
- Some basic familiarity with blockchain tools (optional)

---

## 🚀 Quick Participation via Dashboard

### 1. **Visit the Ceremony Dashboard**
Go to: [https://ceremony.union.build](https://ceremony.union.build)

> 📌 You may need to connect your wallet when prompted.

---

### 2. **Connect Your Wallet**
- Click **Connect Wallet** at the top right.
- Approve the connection in your wallet (e.g., MetaMask).

---

### 3. **Check Eligibility**
- The dashboard will tell you if you're eligible to participate.
- If eligible, you'll see the **Join Ceremony** or **Participate** button.

---

### 4. **Follow the On-Screen Instructions**
- The ceremony involves cryptographic computation (don't worry — it's handled automatically).
- Allow a few minutes for the process to complete.
- Stay on the page until the confirmation shows up.

---

### 5. **You're Done! 🎉**
- You should now see a confirmation message.
- You might also get an NFT or airdrop eligibility in future rounds 👀

---

## 🐳 Optional: Participate Using Docker

For more advanced users, you can run the MPC client locally:

```bash
sudo mkdir -p ceremony && \
sudo docker pull ghcr.io/unionlabs/union/mpc-client:v1.2 && \
sudo docker run -v $(pwd)/ceremony:/ceremony -w /ceremony -p 4919:4919 --rm -it ghcr.io/unionlabs/union/mpc-client:v1.2

