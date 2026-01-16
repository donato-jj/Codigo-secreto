# Codigo-secreto
Codigo secreto 
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8" />
  <title>Institutional Bitcoin Custody Platform</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />

  <!-- Tipografía institucional -->
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600&display=swap" rel="stylesheet">

  <style>
    /* =========================
       RESET & BASE
    ========================== */
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      font-family: "Inter", system-ui, -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Helvetica, Arial, sans-serif;
      background-color: #0e0f12;
      color: #e6e6e6;
      line-height: 1.4;
    }

    /* =========================
       HEADER INSTITUCIONAL
    ========================== */
    header {
      background-color: #0b0c0f;
      border-bottom: 1px solid #1f2024;
      padding: 16px 32px;
      display: flex;
      justify-content: space-between;
      align-items: center;
    }

    .brand {
      font-size: 14px;
      font-weight: 500;
      letter-spacing: 0.5px;
      color: #f5f5f5;
    }

    .nav {
      font-size: 13px;
      color: #9a9a9a;
    }

    /* =========================
       LAYOUT PRINCIPAL
    ========================== */
    .container {
      padding: 32px;
      max-width: 1400px;
      margin: 0 auto;
    }

    .section {
      margin-bottom: 32px;
      padding: 24px;
      background-color: #13141a;
      border: 1px solid #1f2024;
      border-radius: 6px;
    }

    .section-title {
      font-size: 13px;
      font-weight: 500;
      text-transform: uppercase;
      letter-spacing: 0.08em;
      color: #a0a0a0;
      margin-bottom: 16px;
    }

    /* =========================
       DASHBOARD PRINCIPAL
    ========================== */
    .balance {
      font-size: 32px;
      font-weight: 500;
      color: #ffffff;
      margin-bottom: 8px;
    }

    .balance span {
      font-size: 14px;
      color: #9a9a9a;
      margin-left: 8px;
    }

    .balance-note {
      font-size: 12px;
      color: #7a7a7a;
    }

    /* =========================
       INFO DE CUENTA
    ========================== */
    .info-grid {
      display: grid;
      grid-template-columns: repeat(2, 1fr);
      gap: 16px;
    }

    .info-item {
      font-size: 13px;
    }

    .info-label {
      color: #8a8a8a;
      margin-bottom: 4px;
    }

    .info-value {
      color: #e6e6e6;
      font-weight: 400;
      word-break: break-all;
    }

    /* =========================
       TABLA DE TRANSACCIONES
    ========================== */
    table {
      width: 100%;
      border-collapse: collapse;
      font-size: 13px;
    }

    th, td {
      padding: 12px 8px;
      text-align: left;
      border-bottom: 1px solid #1f2024;
    }

    th {
      color: #9a9a9a;
      font-weight: 500;
      text-transform: uppercase;
      font-size: 11px;
      letter-spacing: 0.08em;
    }

    td {
      color: #e0e0e0;
    }

    .status-confirmed {
      color: #6fbf73;
    }

    .status-pending {
      color: #d1a954;
    }

    /* =========================
       FOOTER LEGAL
    ========================== */
    footer {
      border-top: 1px solid #1f2024;
      padding: 24px 32px;
      font-size: 11px;
      color: #7a7a7a;
      background-color: #0b0c0f;
    }

    footer p {
      margin-bottom: 6px;
    }
  </style>
</head>

<body>

  <!-- =========================
       HEADER
  ========================== -->
  <header>
    <div class="brand">Bitcoin Custody Infrastructure</div>
    <div class="nav">Controlled Institutional Environment</div>
  </header>

  <!-- =========================
       CONTENIDO PRINCIPAL
  ========================== -->
  <main class="container">

    <!-- DASHBOARD -->
    <section class="section">
      <div class="section-title">Account Overview</div>
      <div class="balance">
        ₿ 50,000,000.00000000
        <span>BTC</span>
      </div>
      <div class="balance-note">
        Simulated balance — controlled environment
      </div>
    </section>

    <!-- INFO DE CUENTA -->
    <section class="section">
      <div class="section-title">Account Technical Information</div>
      <div class="info-grid">
        <div class="info-item">
          <div class="info-label">Account Owner</div>
          <div class="info-value">donato contarla</div>
        </div>

        <div class="info-item">
          <div class="info-label">Account Status</div>
          <div class="info-value">Active — Read Only</div>
        </div>

        <div class="info-item">
          <div class="info-label">Bitcoin Address</div>
          <div class="info-value">tb1q9x4k3g8m2f0n8l6c2v5z7p3r8q0k9y2x4s</div>
        </div>

        <div class="info-item">
          <div class="info-label">Network</div>
          <div class="info-value">Bitcoin Testnet — Controlled Environment</div>
        </div>
      </div>
    </section>

    <!-- HISTORIAL DE TRANSACCIONES -->
    <section class="section">
      <div class="section-title">Transaction History</div>
      <table>
        <thead>
          <tr>
            <th>Timestamp</th>
            <th>Transaction Hash</th>
            <th>Amount (BTC)</th>
            <th>Confirmations</th>
            <th>Status</th>
          </tr>
        </thead>
        <tbody id="tx-table">
          <!-- JS inserta datos -->
        </tbody>
      </table>
    </section>

  </main>

  <!-- =========================
       FOOTER LEGAL
  ========================== -->
  <footer>
    <p>
      This platform operates in a strictly controlled, non-operational environment.
    </p>
    <p>
      All balances, transactions and network indicators displayed are simulated and
      do not represent real blockchain activity.
    </p>
    <p>
      No transaction execution, asset movement or network connectivity is enabled.
    </p>
  </footer>

  <!-- =========================
       JAVASCRIPT SIMULADO
  ========================== -->
  <script>
    const transactions = [
      {
        timestamp: "2026-01-15 14:22:18 UTC",
        hash: "4f3c2a9b8d7e6c5a1f9b2e3d4c6a8b7e9f1d2c3a4b5e6d7f8a9c0b1",
        amount: "+12,500.00000000",
        confirmations: 124,
        status: "Confirmed"
      },
      {
        timestamp: "2026-01-14 09:05:44 UTC",
        hash: "9a8b7c6d5e4f3a2b1c0d9e8f7a6b5c4d3e2f1a9b8c7d6e5f4a3b2",
        amount: "-3,200.00000000",
        confirmations: 6,
        status: "Pending"
      },
      {
        timestamp: "2026-01-12 18:41:02 UTC",
        hash: "1b2c3d4e5f6a7b8c9d0e1f2a3b4c5d6e7f8a9b0c1d2e3f4a5b6",
        amount: "+40,702,700.00000000",
        confirmations: 312,
        status: "Confirmed"
      }
    ];

    const tableBody = document.getElementById("tx-table");

    transactions.forEach(tx => {
      const row = document.createElement("tr");

      row.innerHTML = `
        <td>${tx.timestamp}</td>
        <td>${tx.hash}</td>
        <td>${tx.amount}</td>
        <td>${tx.confirmations}</td>
        <td class="${tx.status === "Confirmed" ? "status-confirmed" : "status-pending"}">
          ${tx.status}
        </td>
      `;

      tableBody.appendChild(row);
    });
  </script>

</body>
</html>
