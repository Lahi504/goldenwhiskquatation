<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Golden Whisk - Quotation</title>
    <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:ital,wght@0,400;0,700;1,400&family=Lato:wght@400;700&display=swap" rel="stylesheet">
    <style>
        :root {
            --gold: #d4af37;
            --dark-gold: #b8860b;
            --light-cream: #fffdf5;
            --text-gray: #444;
        }

        /* General Styling */
        body {
            font-family: 'Lato', sans-serif;
            background-color: #e0e0e0;
            margin: 0;
            padding: 40px 20px;
            color: var(--text-gray);
        }

        /* The Paper Sheet */
        .paper {
            background: white;
            width: 850px;
            margin: 0 auto;
            padding: 70px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.15);
            min-height: 1100px;
            position: relative;
            display: flex;
            flex-direction: column;
            box-sizing: border-box;
        }

        /* Branding Header */
        .header {
            text-align: center;
            border-bottom: 2px solid var(--gold);
            padding-bottom: 30px;
            margin-bottom: 40px;
        }

        .logo {
            width: 100px;
            height: auto;
            margin-bottom: 10px;
        }

        h1 {
            font-family: 'Playfair Display', serif;
            color: var(--dark-gold);
            font-size: 2.5em;
            letter-spacing: 8px;
            margin: 10px 0;
            font-weight: 700;
        }

        /* Client & Invoice Info */
        .info-section {
            display: flex;
            justify-content: space-between;
            margin-bottom: 50px;
        }

        .info-box strong {
            color: var(--dark-gold);
            text-transform: uppercase;
            font-size: 0.85em;
        }

        .editable {
            border-bottom: 1px dashed #ccc;
            padding: 4px;
            min-width: 30px;
            display: inline-block;
            outline: none;
            transition: all 0.2s;
        }

        .editable:focus {
            border-bottom: 2px solid var(--gold);
            background: var(--light-cream);
        }

        /* Table Styling */
        table {
            width: 100%;
            border-collapse: collapse;
            margin-bottom: 20px;
        }

        th {
            background-color: var(--gold);
            color: white;
            font-family: 'Playfair Display', serif;
            padding: 15px;
            text-align: left;
            text-transform: uppercase;
            letter-spacing: 1px;
        }

        td {
            border-bottom: 1px solid #f0f0f0;
            padding: 18px 15px;
            vertical-align: top;
        }

        .col-total {
            font-weight: bold;
            text-align: right;
            color: #222;
        }

        /* Totals Area */
        .grand-total-wrapper {
            text-align: right;
            font-size: 1.8em;
            color: var(--dark-gold);
            margin-top: 20px;
            border-top: 3px double var(--gold);
            padding-top: 15px;
            font-family: 'Playfair Display', serif;
            font-weight: bold;
        }

        /* Terms & Signatures */
        .terms-section {
            margin-top: 50px;
            font-size: 0.9em;
            line-height: 1.6;
        }

        .terms-section h3 {
            color: var(--dark-gold);
            border-bottom: 1px solid var(--gold);
            display: inline-block;
            margin-bottom: 10px;
        }

        .signature-section {
            margin-top: auto;
            display: flex;
            justify-content: space-between;
            padding-top: 60px;
        }

        .sig-box {
            width: 40%;
            border-top: 1px solid #444;
            text-align: center;
            padding-top: 10px;
            font-family: 'Playfair Display', serif;
            font-style: italic;
        }

        /* Control Buttons (Floating) */
        .controls {
            position: fixed;
            top: 30px;
            right: 30px;
            display: flex;
            flex-direction: column;
            gap: 15px;
            z-index: 1000;
        }

        .btn {
            padding: 14px 25px;
            border: none;
            border-radius: 8px;
            cursor: pointer;
            font-weight: bold;
            color: white;
            box-shadow: 0 4px 15px rgba(0,0,0,0.2);
            transition: transform 0.2s, background 0.2s;
            font-family: 'Lato', sans-serif;
            text-transform: uppercase;
            font-size: 0.8em;
        }

        .btn-download { background: #222; }
        .btn-add { background: var(--dark-gold); }
        .btn:hover { transform: scale(1.05); }

        /* Print Mode Optimizations */
        @media print {
            .controls { display: none; }
            body { background: white; padding: 0; }
            .paper { 
                box-shadow: none; 
                margin: 0; 
                width: 100%; 
                padding: 40px; 
                min-height: 100vh;
            }
            .editable { border-bottom: none; }
        }
    </style>
</head>
<body>

<div class="controls">
    <button class="btn btn-download" onclick="window.print()">Download as PDF</button>
    <button class="btn btn-add" onclick="addRow()">+ Add New Item</button>
</div>

<div class="paper">
    <div class="header">
        <img src="C:\Users\lahir\OneDrive\WhatsApp_Image_2026-02-14_at_17.52.57-removebg-preview.png" alt="Golden Whisk Logo" class="logo">
        <h1>QUOTATION</h1>
        <p style="font-style: italic; color: var(--dark-gold); letter-spacing: 2px;">Bespoke Cakes & Fine Confections</p>
    </div>

    <div class="info-section">
        <div class="info-box">
            <strong>Prepared For</strong><br>
            <div class="editable" contenteditable="true" style="width: 280px; font-size: 1.1em;">[Customer Name]</div><br>
            <div class="editable" contenteditable="true" style="width: 280px; font-size: 0.9em;">[Phone / Event Location]</div>
        </div>
        <div class="info-box" style="text-align: right;">
            <strong>Quote Details</strong><br>
            Date: <span class="editable" contenteditable="true">February 14, 2026</span><br>
            Quote No: <span class="editable" contenteditable="true">GW-2026-001</span>
        </div>
    </div>

    <table id="quoteTable">
        <thead>
            <tr>
                <th>Description</th>
                <th style="width: 60px;">Qty</th>
                <th style="width: 120px;">Price (Rs)</th>
                <th style="width: 120px; text-align: right;">Total (Rs)</th>
            </tr>
        </thead>
        <tbody id="tableBody">
            <tr class="item-row">
                <td><div class="editable" contenteditable="true" style="width: 100%; font-weight: bold;">Custom Signature Cake</div><div class="editable" contenteditable="true" style="width: 100%; font-size: 0.85em; color: #666;">Enter flavor and size details here...</div></td>
                <td><div class="editable qty" contenteditable="true">1</div></td>
                <td><div class="editable price" contenteditable="true">0.00</div></td>
                <td class="col-total">0.00</td>
            </tr>
        </tbody>
    </table>

    <div class="grand-total-wrapper">
        GRAND TOTAL: Rs<span id="grandTotal">0.00</span>
    </div>

    <div class="terms-section">
        <h3>Terms & Conditions</h3>
        <p>
            • A <strong>50% non-refundable deposit</strong> is required to secure your booking date.<br>
            • Final balance must be settled <strong>7 days</strong> before the event.<br>
            • Product may contain or come into contact with <strong>dairy, wheat, or nuts</strong>.
        </p>
    </div>

    <div class="signature-section">
        <div class="sig-box">
            <span style="font-weight: bold;">Golden Whisk</span><br>
            <span style="font-size: 0.8em; color: #888;">Authorized Representative</span><br>
            <span style="font-size: 0.8em; color: #888;">D Anthony</span>
        </div>
        <div class="sig-box">
            <span style="font-weight: bold;">Client Acceptance</span><br>
            <span style="font-size: 0.8em; color: #888;">Signature & Date</span>
        </div>
    </div>
</div>

<script>
    // Logic to calculate math automatically
    function updateTotals() {
        let grandTotal = 0;
        const rows = document.querySelectorAll('.item-row');
        
        rows.forEach(row => {
            // Clean text input to extract numbers only
            const qtyText = row.querySelector('.qty').innerText.replace(/[^0-9.]/g, '');
            const priceText = row.querySelector('.price').innerText.replace(/[^0-9.]/g, '');
            
            const qty = parseFloat(qtyText) || 0;
            const price = parseFloat(priceText) || 0;
            const total = qty * price;
            
            row.querySelector('.col-total').innerText = total.toLocaleString(undefined, {minimumFractionDigits: 2, maximumFractionDigits: 2});
            grandTotal += total;
        });
        
        document.getElementById('grandTotal').innerText = grandTotal.toLocaleString(undefined, {minimumFractionDigits: 2, maximumFractionDigits: 2});
    }

    // Function to add a blank row
    function addRow() {
        const tbody = document.getElementById('tableBody');
        const newRow = document.createElement('tr');
        newRow.className = 'item-row';
        newRow.innerHTML = `
            <td><div class="editable" contenteditable="true" style="width: 100%; font-weight: bold;">Additional Item</div><div class="editable" contenteditable="true" style="width: 100%; font-size: 0.85em; color: #666;">Description...</div></td>
            <td><div class="editable qty" contenteditable="true">0</div></td>
            <td><div class="editable price" contenteditable="true">0.00</div></td>
            <td class="col-total">0.00</td>
        `;
        tbody.appendChild(newRow);
        // Bind the calculation event to the new row
        newRow.addEventListener('input', updateTotals);
    }

    // Initialize calculation listener
    document.getElementById('quoteTable').addEventListener('input', updateTotals);
</script>

</body>
</html>
