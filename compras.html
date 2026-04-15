<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no, viewport-fit=cover">
    <title>Mi Lista ✨</title>

    <meta name="apple-mobile-web-app-capable" content="yes">
    <meta name="apple-mobile-web-app-status-bar-style" content="black-translucent">
    <meta name="apple-mobile-web-app-title" content="Compras ✨">
    <link rel="apple-touch-icon" href="https://cdn-icons-png.flaticon.com/512/3737/3737372.png">
    
    <link href="https://fonts.googleapis.com/css2?family=Outfit:wght@400;600;800&display=swap" rel="stylesheet">

    <style>
        :root {
            --accent: #ff6b6b;
            --bg: #f8f9fa;
            --card: #ffffff;
            --text: #2d3436;
            --gray: #b2bec3;
            --shadow: 0 10px 20px rgba(0,0,0,0.05);
        }

        * { margin: 0; padding: 0; box-sizing: border-box; -webkit-tap-highlight-color: transparent; }

        body {
            font-family: 'Outfit', sans-serif;
            background-color: var(--bg);
            color: var(--text);
            padding-bottom: 100px;
        }

        /* HEADER CHULO */
        .header {
            background: linear-gradient(135deg, #ff6b6b, #ff8e8e);
            padding: 60px 25px 30px;
            color: white;
            border-radius: 0 0 30px 30px;
            box-shadow: var(--shadow);
        }

        h1 { font-size: 28px; font-weight: 800; }
        .stats { font-size: 14px; opacity: 0.9; margin-top: 5px; }

        /* INPUT SECCIÓN */
        .input-box {
            margin: -25px 20px 20px;
            background: var(--card);
            padding: 8px;
            border-radius: 20px;
            display: flex;
            box-shadow: var(--shadow);
        }

        input {
            flex: 1;
            border: none;
            padding: 15px;
            font-size: 16px;
            font-family: inherit;
            outline: none;
            border-radius: 15px;
        }

        .add-btn {
            background: var(--accent);
            color: white;
            border: none;
            width: 50px;
            height: 50px;
            border-radius: 15px;
            font-size: 24px;
            font-weight: bold;
            cursor: pointer;
        }

        /* LISTA */
        .list-container { padding: 0 20px; }
        
        .item {
            background: var(--card);
            margin-bottom: 12px;
            padding: 15px 20px;
            border-radius: 18px;
            display: flex;
            align-items: center;
            justify-content: space-between;
            box-shadow: 0 4px 6px rgba(0,0,0,0.02);
            transition: all 0.3s ease;
            animation: slideIn 0.3s ease-out;
        }

        @keyframes slideIn {
            from { opacity: 0; transform: translateY(10px); }
            to { opacity: 1; transform: translateY(0); }
        }

        .item.checked {
            opacity: 0.6;
            background: #f1f2f6;
            transform: scale(0.98);
        }

        .item-text {
            font-size: 16px;
            font-weight: 600;
            flex: 1;
            cursor: pointer;
        }

        .item.checked .item-text {
            text-decoration: line-through;
            color: var(--gray);
        }

        .delete-btn {
            color: #fab1a0;
            font-size: 18px;
            margin-left: 15px;
            cursor: pointer;
        }

        /* BARRA INFERIOR */
        .footer-tools {
            position: fixed;
            bottom: 20px;
            left: 20px;
            right: 20px;
            display: flex;
            gap: 10px;
        }

        .tool-btn {
            flex: 1;
            padding: 15px;
            border-radius: 15px;
            border: none;
            background: var(--text);
            color: white;
            font-weight: 600;
            font-family: inherit;
            box-shadow: 0 10px 20px rgba(0,0,0,0.15);
        }

        .clear-btn { background: #dfe6e9; color: #636e72; }
    </style>
</head>
<body>

    <div class="header">
        <h1>Mi Lista ✨</h1>
        <div class="stats" id="counter">Tienes 0 productos pendientes</div>
    </div>

    <div class="input-box">
        <input type="text" id="itemInput" placeholder="Añadir leche, pan, fruta..." onkeypress="if(event.key==='Enter') addItem()">
        <button class="add-btn" onclick="addItem()">+</button>
    </div>

    <div class="list-container" id="list">
        </div>

    <div class="footer-tools">
        <button class="tool-btn clear-btn" onclick="clearChecked()">Limpiar comprados</button>
        <button class="tool-btn" onclick="resetAll()">Borrar todo</button>
    </div>

    <script>
        let items = JSON.parse(localStorage.getItem('myShoppingList')) || [];

        function addItem() {
            const input = document.getElementById('itemInput');
            if (input.value.trim() === '') return;

            const newItem = {
                id: Date.now(),
                text: input.value,
                checked: false
            };

            items.unshift(newItem); // Añade al principio
            input.value = '';
            render();
            save();
        }

        function toggleItem(id) {
            items = items.map(item => {
                if (item.id === id) item.checked = !item.checked;
                return item;
            });
            render();
            save();
        }

        function deleteItem(id) {
            items = items.filter(item => item.id !== id);
            render();
            save();
        }

        function clearChecked() {
            items = items.filter(item => !item.checked);
            render();
            save();
        }

        function resetAll() {
            if(confirm('¿Borrar toda la lista?')) {
                items = [];
                render();
                save();
            }
        }

        function save() {
            localStorage.setItem('myShoppingList', JSON.stringify(items));
        }

        function render() {
            const list = document.getElementById('list');
            const counter = document.getElementById('counter');
            list.innerHTML = '';

            // Ordenar: primero pendientes, luego comprados
            const sortedItems = [...items].sort((a, b) => a.checked - b.checked);

            sortedItems.forEach(item => {
                const div = document.createElement('div');
                div.className = `item ${item.checked ? 'checked' : ''}`;
                div.innerHTML = `
                    <div class="item-text" onclick="toggleItem(${item.id})">${item.text}</div>
                    <div class="delete-btn" onclick="deleteItem(${item.id})">✕</div>
                `;
                list.appendChild(div);
            });

            const pending = items.filter(i => !i.checked).length;
            counter.innerText = pending === 0 ? "¡Todo listo! ✨" : `Tienes ${pending} productos pendientes`;
        }

        window.onload = render;
    </script>
</body>
</html>
