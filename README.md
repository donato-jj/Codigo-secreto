
<!DOCTYPE html>
<html lang="en">
<head>
    <!--
    LEGAL & TECHNICAL NOTICE (MANDATORY)
    This is a non-operational visual system.
    No real Bitcoin, no blockchain interaction, no custody of funds.
    No financial services are provided.
    For visualization and development purposes only.
    -->

    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <meta name="description" content="Digital Bitcoin Account Interface - Visual Financial Representation" />
    <meta name="author" content="Donato Conturla" />

    <title>Donato Conturla | Digital Bitcoin Account</title>

    <style>
        :root {
            --bg-dark: #0b0f14;
            --bg-panel: #121822;
            --accent-btc: #2ecc71;
            --text-main: #e6eaf0;
            --text-muted: #8a94a6;
            --danger: #e74c3c;
            --radius: 14px;
        }

        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
            font-family: "Segoe UI", Roboto, Arial, sans-serif;
        }

        body {
            background: linear-gradient(180deg, #05070a, var(--bg-dark));
            color: var(--text-main);
            min-height: 100vh;
        }

        /* LOGIN */
        #loginScreen {
            display: flex;
            align-items: center;
            justify-content: center;
            height: 100vh;
        }

        .login-box {
            background: var(--bg-panel);
            padding: 40px;
            width: 100%;
            max-width: 420px;
            border-radius: var(--radius);
            box-shadow: 0 0 60px rgba(0,0,0,0.6);
        }

        .login-box h1 {
            text-align: center;
            margin-bottom: 10px;
            font-weight: 600;
        }

        .login-box p {
            text-align: center;
            font-size: 0.85rem;
            color: var(--text-muted);
            margin-bottom: 30px;
        }

        .login-box input {
            width: 100%;
            padding: 14px;
            margin-bottom: 14px;
            border-radius: 10px;
            border: none;
            background: #0e131c;
            color: var(--text-main);
        }

        .login-box button {
            width: 100%;
            padding: 14px;
            border-radius: 10px;
            border: none;
            background: linear-gradient(135deg, var(--accent-btc), #27ae60);
            font-weight: 600;
            cursor: pointer;
        }

        .error {
            margin-top: 12px;
            color: var(--danger);
            font-size: 0.8rem;
            text-align: center;
            display: none;
        }

        .notice {
            margin-top: 18px;
            font-size: 0.75rem;
            color: var(--text-muted);
            text-align: center;
        }

        /* DASHBOARD */
        #dashboard {
            display: none;
            min-height: 100vh;
        }

        .sidebar {
            width: 240px;
            background: var(--bg-panel);
            position: fixed;
            top: 0;
            bottom: 0;
            padding: 30px 20px;
        }

        .main {
            margin-left: 240px;
            padding: 30px;
        }

        .balance-card {
            background: #0e141d;
            padding: 30px;
            border-radius: var(--radius);
            margin-bottom: 30px;
        }

        footer {
            margin-top: 40px;
            font-size: 0.75rem;
            color: var(--text-muted);
            text-align: center;
        }

        @media(max-width: 900px) {
            .sidebar {
                position: relative;
                width: 100%;
            }
            .main {
                margin-left: 0;
            }
        }
    </style>
</head>
<body>

<!-- LOGIN -->
<div id="loginScreen">
    <div class="login-box">
        <h1>Digital Bitcoin Account</h1>
        <p>Secure access portal</p>

        <input type="text" id="username" placeholder="Username" />
        <input type="password" id="password" placeholder="Password" />

        <button onclick="login()">Access Account</button>

        <div class="error" id="errorMsg">
            Invalid credentials. Access denied.
        </div>

        <div class="notice">
            This system does not provide access to real financial assets or blockchain networks.
        </div>
    </div>
</div>

<!-- DASHBOARD -->
<div id="dashboard">
    <div class="sidebar">
        <h2>Donato Conturla</h2>
    </div>

    <div class="main">
        <div class="balance-card">
            <h3>Total Balance</h3>
            <div style="font-size:2rem;color:#2ecc71;">
                ₿ 50,000,000.00 BTC-DONATO
            </div>
        </div>

        <footer>
            This is a non-operational visual system. No real Bitcoin, no blockchain interaction, no custody of funds.
            No financial services are provided. For visualization and development purposes only.
        </footer>
    </div>
</div>

<script>
    /* ACCESS CREDENTIALS (FRONTEND ONLY) */
    const VALID_USERNAME = "conturladonato10";
    const VALID_PASSWORD = "donato100";

    function login() {
        const user = document.getElementById("username").value;
        const pass = document.getElementById("password").value;
        const error = document.getElementById("errorMsg");

        if (user === VALID_USERNAME && pass === VALID_PASSWORD) {
            document.getElementById("loginScreen").style.display = "none";
            document.getElementById("dashboard").style.display = "block";
        } else {
            error.style.display = "block";
        }
    }
</script>

</body>
</html>
