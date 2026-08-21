# Dise-o_boleto<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Boleto Teatro Sing</title>
    <style>
        :root {
            --bg-dark: #0d0d0d;
            --ticket-bg: #1a0f0f;
            --gold: #dfba6b;
            --white: #ffffff;
            --gray: #a6a6a6;
        }

        body {
            background-color: var(--bg-dark);
            font-family: 'Arial', sans-serif;
            display: flex;
            justify-content: center;
            align-items: center;
            min-height: 100vh;
            margin: 0;
        }

        .ticket-container {
            display: flex;
            width: 900px;
            height: 450px;
            background-color: var(--ticket-bg);
            border: 2px solid var(--gold);
            color: var(--white);
            position: relative;
            box-shadow: 0 10px 30px rgba(0,0,0,0.7);
        }

        /* Cuerpo principal del boleto */
        .ticket-main {
            flex: 3;
            display: grid;
            grid-template-rows: 1fr 2fr 1fr;
            padding: 20px;
            border-right: 2px dashed var(--gold);
        }

        .header-section {
            display: flex;
            justify-content: space-between;
            align-items: center;
            border-bottom: 1px solid rgba(223, 186, 107, 0.3);
            padding-bottom: 10px;
        }

        .brand {
            text-align: center;
        }

        .brand h1 {
            color: var(--gold);
            margin: 0;
            font-size: 28px;
            letter-spacing: 2px;
        }

        .brand p {
            font-size: 9px;
            color: var(--gray);
            margin: 5px 0 0 0;
        }

        .show-info {
            text-align: center;
        }

        .show-info h2 {
            font-size: 14px;
            color: var(--gold);
            margin: 0;
            letter-spacing: 3px;
        }

        .show-info h3 {
            font-size: 26px;
            margin: 5px 0 0 0;
            letter-spacing: 1px;
        }

        /* Detalles de función y asientos */
        .details-section {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 15px;
            padding: 20px 0;
            text-align: center;
        }

        .info-box {
            border: 1px solid var(--gold);
            padding: 10px;
            border-radius: 4px;
        }

        .info-box .label {
            font-size: 11px;
            color: var(--gold);
            display: block;
            margin-bottom: 5px;
        }

        .info-box .value {
            font-size: 22px;
            font-weight: bold;
        }

        .price-tag {
            grid-column: span 2;
            display: flex;
            justify-content: center;
            align-items: center;
            border: 1px solid var(--gold);
            font-size: 24px;
            color: var(--gold);
            font-weight: bold;
        }

        .qr-placeholder {
            background-color: var(--white);
            width: 80px;
            height: 80px;
            margin: 0 auto;
            display: flex;
            align-items: center;
            justify-content: center;
            color: black;
            font-size: 10px;
            font-weight: bold;
        }

        /* Pie de página */
        .footer-section {
            display: flex;
            justify-content: space-between;
            align-items: center;
            font-size: 11px;
            color: var(--gray);
            border-top: 1px solid rgba(223, 186, 107, 0.3);
            padding-top: 10px;
        }

        /* Talón del boleto (Derecha) */
        .ticket-stub {
            flex: 1;
            padding: 20px;
            display: flex;
            flex-direction: column;
            justify-content: space-between;
            align-items: center;
            text-align: center;
            background-color: rgba(0, 0, 0, 0.2);
        }

        .stub-title {
            color: var(--gold);
            font-size: 18px;
            margin: 0;
        }

        .barcode-placeholder {
            background: linear-gradient(90deg, #000 5%, transparent 5%, transparent 10%, #000 10%, #000 15%, transparent 15%, #000 25%);
            background-size: 10px 100%;
            width: 100%;
            height: 40px;
            background-color: var(--white);
        }
    </style>
</head>
<body>

    <div class="ticket-container">
        <!-- CUERPO PRINCIPAL -->
        <div class="ticket-main">
            <div class="header-section">
                <div class="brand">
                    <h1>TEATRO SING</h1>
                    <p>DONDE CADA HISTORIA COBRA VIDA</p>
                </div>
                <div class="show-info">
                    <h2>OBRA</h2>
                    <h3>ROMEO Y JULIETA</h3>
                </div>
            </div>

            <div class="details-section">
                <div class="info-box">
                    <span class="label">FECHA</span>
                    <span class="value">20 SEPT 2026</span>
                </div>
                <div class="info-box">
                    <span class="label">HORA</span>
                    <span class="value">19:00</span>
                </div>
                <div class="info-box">
                    <span class="label">PUERTA</span>
                    <span class="value">2</span>
                </div>
                
                <div class="info-box">
                    <span class="label">SECTOR</span>
                    <span class="value" style="color: var(--gold);">VIP</span>
                </div>
                <div class="info-box">
                    <span class="label">FILA</span>
                    <span class="value">A</span>
                </div>
                <div class="info-box">
                    <span class="label">ASIENTO</span>
                    <span class="value">025</span>
                </div>

                <div class="price-tag">
                    PRECIO: $25,00
                </div>
                <div>
                    <div class="qr-placeholder">QR CODE</div>
                </div>
            </div>

            <div class="footer-section">
                <span>CAPACIDAD: 3.000 PERSONAS</span>
                <span style="color: var(--gold);">Gracias por ser parte de esta experiencia</span>
            </div>
        </div>

        <!-- TALÓN DE INGRESO -->
        <div class="ticket-stub">
            <div>
                <h4 class="stub-title">TEATRO SING</h4>
                <p style="font-size: 11px; margin: 5px 0;">ROMEO Y JULIETA</p>
            </div>
            
            <div style="font-size: 12px;">
                <p>20 SEPTIEMBRE 2026</p>
                <p><b>VIP</b> - FILA A - AS. 025</p>
                <p style="color: var(--gold); font-weight: bold;">$25,00</p>
            </div>

            <div style="width: 100%;">
                <div class="barcode-placeholder"></div>
                <p style="font-size: 9px; margin: 5px 0 0 0;">TS2026-0001256</p>
            </div>
        </div>
    </div>

</body>
</html>
