<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Inventaire de Matériel Nomade</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background-color: #f4f4f9;
            color: #333;
        }
        header {
            background-color: #007BFF;
            color: white;
            padding: 1em 0;
            text-align: center;
        }
        form {
            max-width: 600px;
            margin: 2em auto;
            padding: 1em;
            background: white;
            border: 1px solid #ddd;
            border-radius: 5px;
            box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
        }
        form label {
            display: block;
            margin-bottom: 0.5em;
        }
        form input, form select {
            width: 100%;
            padding: 0.5em;
            margin-bottom: 1em;
            border: 1px solid #ddd;
            border-radius: 4px;
        }
        form button {
            background-color: #007BFF;
            color: white;
            padding: 0.5em 1em;
            border: none;
            border-radius: 4px;
            cursor: pointer;
        }
        form button:hover {
            background-color: #0056b3;
        }
        table {
            width: 90%;
            margin: 2em auto;
            border-collapse: collapse;
            box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
        }
        table th, table td {
            padding: 1em;
            border: 1px solid #ddd;
            text-align: left;
        }
        table th {
            background-color: #007BFF;
            color: white;
        }
        .actions {
            max-width: 600px;
            margin: 2em auto;
            display: flex;
            justify-content: space-between;
        }
        .actions button {
            padding: 0.5em 1em;
            border: none;
            border-radius: 4px;
            cursor: pointer;
        }
        .actions .export-excel {
            background-color: #28a745;
            color: white;
        }
        .actions .export-pdf {
            background-color: #dc3545;
            color: white;
        }
        .actions .clear-data {
            background-color: #6c757d;
            color: white;
        }
    </style>
</head>
<body>
    <header>
        <h1>Inventaire de Matériel Nomade</h1>
    </header>
    <main>
        <form id="inventoryForm">
            <label for="itemName">Nom du matériel</label>
            <input type="text" id="itemName" placeholder="Exemple : Ordinateur portable" required>
            
            <label for="itemCategory">Catégorie</label>
            <input type="text" id="itemCategory" placeholder="Exemple : Informatique" required>
            
            <label for="itemQuantity">Quantité</label>
            <input type="number" id="itemQuantity" min="1" value="1" required>
            
            <label for="itemLocation">Emplacement</label>
            <input type="text" id="itemLocation" placeholder="Exemple : Bureau 3" required>
            
            <button type="submit">Ajouter au stock</button>
        </form>
        
        <table id="inventoryTable">
            <thead>
                <tr>
                    <th>Nom du matériel</th>
                    <th>Catégorie</th>
                    <th>Quantité</th>
                    <th>Emplacement</th>
                </tr>
            </thead>
            <tbody></tbody>
        </table>
        
        <div class="actions">
            <button class="export-excel">Exporter en Excel</button>
            <button class="export-pdf">Exporter en PDF</button>
            <button class="clear-data">Effacer les données</button>
        </div>
    </main>
    <script>
        const form = document.getElementById('inventoryForm');
        const tableBody = document.querySelector('#inventoryTable tbody');

        // Chargement des données depuis le localStorage
        const loadInventory = () => {
            const inventory = JSON.parse(localStorage.getItem('inventory')) || [];
            tableBody.innerHTML = '';
            inventory.forEach((item, index) => {
                const row = document.createElement('tr');
                row.innerHTML = `
                    <td>${item.name}</td>
                    <td>${item.category}</td>
                    <td>${item.quantity}</td>
                    <td>${item.location}</td>
                `;
                tableBody.appendChild(row);
            });
        };

        // Sauvegarde de l'inventaire dans le localStorage
        const saveInventory = (item) => {
            const inventory = JSON.parse(localStorage.getItem('inventory')) || [];
            inventory.push(item);
            localStorage.setItem('inventory', JSON.stringify(inventory));
        };

        // Gestion de la soumission du formulaire
        form.addEventListener('submit', (event) => {
            event.preventDefault();
            const newItem = {
                name: document.getElementById('itemName').value,
                category: document.getElementById('itemCategory').value,
                quantity: document.getElementById('itemQuantity').value,
                location: document.getElementById('itemLocation').value
            };
            saveInventory(newItem);
            loadInventory();
            form.reset();
        });

        // Exportation des données en Excel
        document.querySelector('.export-excel').addEventListener('click', () => {
            const inventory = JSON.parse(localStorage.getItem('inventory')) || [];
            let csvContent = 'Nom du matériel,Catégorie,Quantité,Emplacement\n';
            inventory.forEach(item => {
                csvContent += `${item.name},${item.category},${item.quantity},${item.location}\n`;
            });
            const blob = new Blob([csvContent], { type: 'text/csv;charset=utf-8;' });
            const url = URL.createObjectURL(blob);
            const a = document.createElement('a');
            a.href = url;
            a.download = 'inventaire.csv';
            a.click();
            URL.revokeObjectURL(url);
        });

        // Exportation des données en PDF
        document.querySelector('.export-pdf').addEventListener('click', () => {
            const inventory = JSON.parse(localStorage.getItem('inventory')) || [];
            const doc = new jsPDF();
            doc.text('Inventaire de Matériel Nomade', 10, 10);
            let y = 20;
            inventory.forEach(item => {
                doc.text(`Nom : ${item.name}, Catégorie : ${item.category}, Quantité : ${item.quantity}, Emplacement : ${item.location}`, 10, y);
                y += 10;
            });
            doc.save('inventaire.pdf');
        });

        // Effacement des données
        document.querySelector('.clear-data').addEventListener('click', () => {
            localStorage.removeItem('inventory');
            loadInventory();
        });

        // Chargement initial
        loadInventory();
    </script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/jspdf/2.4.0/jspdf.umd.min.js"></script>
</body>
</html>
