
## Yêu cầu hệ thống

Trước khi bắt đầu, bạn cần cài đặt các công cụ sau:

- **Node.js** (phiên bản >= v20.18.3) - [Tải về tại đây](https://nodejs.org/en/download/)
- **Yarn** (v1 hoặc v2+) - [Hướng dẫn cài đặt Yarn v1](https://classic.yarnpkg.com/en/docs/install/) hoặc [Yarn v2+](https://yarnpkg.com/getting-started/install)
- **Git** - [Tải về tại đây](https://git-scm.com/downloads)

---

## Cài đặt

Chạy lệnh sau để cài đặt tất cả các dependencies cần thiết:

```bash
yarn install
```

---

## Hướng dẫn chạy từng bước

Dự án này yêu cầu chạy **3 terminal riêng biệt** để hoạt động đầy đủ:

### **Terminal 1: Khởi động Local Blockchain**

Mở terminal đầu tiên và chạy lệnh sau để khởi động mạng blockchain local:

```bash
yarn chain
```


**Giữ terminal này mở** - đây là mạng blockchain local.

---

### **Terminal 2: Deploy Smart Contracts**

Mở terminal thứ hai và chạy lệnh sau để deploy các smart contracts lên mạng local:

```bash
yarn deploy
```

---

### **Terminal 3: Khởi động Frontend**

Mở terminal thứ ba và chạy lệnh sau để khởi động ứng dụng frontend:

```bash
yarn start
```

---

### **Bước 4: Truy cập ứng dụng**

Mở trình duyệt và truy cập:

```
http://localhost:3000
```


---


## Cấu trúc dự án

```
challenge-dice-game/
├── packages/
│   ├── hardhat/              # Smart contracts và Hardhat config
│   │   ├── contracts/        # Solidity contracts
│   │   │   ├── DiceGame.sol  # Contract chính của Dice Game
│   │   │   └── RiggedRoll.sol # Contract để tấn công Dice Game
│   │   ├── deploy/           # Scripts deploy contracts
│   │   │   ├── 00_deploy_diceGame.ts
│   │   │   └── 01_deploy_riggedRoll.ts
│   │   └── test/             # Test files
│   │
│   └── nextjs/               # Frontend application
│       ├── app/              # Next.js App Router pages
│       ├── components/       # React components
│       └── hooks/            # Custom React hooks
│
├── package.json              # Root package.json với các scripts
└── README.md                 # File này
```

---

## Cách sử dụng ứng dụng

### 1. Kết nối ví

- Khi mở `http://localhost:3000`, bạn sẽ thấy nút "Connect Wallet"
- Click vào và chọn ví bạn muốn kết nối (MetaMask, WalletConnect, etc.)
- Hoặc sử dụng **Burner Wallet** (ví tạm thời) để test nhanh

### 2. Lấy ETH từ Faucet

- Ở góc dưới bên trái màn hình, bạn sẽ thấy nút **"Faucet"**
- Click vào để nhận ETH miễn phí cho mạng local
- Bạn cần ETH để thực hiện các giao dịch

### 3. Chơi Dice Game

- Truy cập trang Dice Game
- Gửi 0.002 ETH để roll dice
- Nếu roll được số 0, 1, 2, 3, 4, hoặc 5 → Bạn thắng!
- Giải thưởng sẽ được gửi về địa chỉ của bạn

### 4. Debug Contracts

- Truy cập `http://localhost:3000/debug` để xem và tương tác trực tiếp với contracts
- Bạn có thể gọi các hàm của contract từ đây

---

## Tài liệu tham khảo

- [Scaffold-ETH 2 Documentation](https://docs.scaffoldeth.io)
- [Scaffold-ETH 2 Website](https://scaffoldeth.io)
- [Hardhat Documentation](https://hardhat.org/docs)
- [Next.js Documentation](https://nextjs.org/docs)
- [Wagmi Documentation](https://wagmi.sh)

---
