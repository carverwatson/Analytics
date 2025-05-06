<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Carver Watson - Hockey Analytics</title>
    <script src="https://cdn.tailwindcss.com"></script>
</head>
<body class="bg-gray-100 font-sans">
    <header class="bg-blue-600 text-white py-6 text-center">
        <h1 class="text-3xl font-bold">Hockey Analytics by Carver W. Watson</h1>
        <p class="text-lg mt-2">Player Game Score Tracker</p>
    </header>
    <main class="max-w-4xl mx-auto py-8 px-4">
        <section class="bg-white shadow-lg rounded-lg p-6">
            <h2 class="text-2xl font-semibold mb-4">Select a Player</h2>
            <p class="text-gray-700 mb-4">Click a player to view or input game stats and track season performance.</p>
            <ul class="space-y-2">
                <li><a href="player1.html" class="text-blue-600 hover:underline text-lg">Player 1 (John Doe)</a></li>
                <li><a href="player2.html" class="text-blue-600 hover:underline text-lg">Player 2 (Jane Smith)</a></li>
            </ul>
        </section>
    </main>
    <footer class="bg-gray-800 text-white text-center py-4">
        <p>Contact: <a href="mailto:carver.watson@gmail.com" class="hover:underline">carver.watson@gmail.com</a> | (920) 287-4014</p>
        <p><a href="https://linkedin.com/in/carverwatson" target="_blank" class="hover:underline">LinkedIn Profile</a></p>
    </footer>
</body>
</html>
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Player Analytics - John Doe</title>
    <script src="https://cdn.tailwindcss.com"></script>
</head>
<body class="bg-gray-100 font-sans">
    <header class="bg-blue-600 text-white py-6 text-center">
        <h1 class="text-3xl font-bold">Player Analytics: John Doe</h1>
        <p class="text-lg mt-2">Game Score and Season Tracking</p>
    </header>
    <main class="max-w-4xl mx-auto py-8 px-4">
        <section class="bg-white shadow-lg rounded-lg p-6 mb-6">
            <h2 class="text-2xl font-semibold mb-4">Input Game Statistics</h2>
            <form id="statsForm" class="space-y-4">
                <div>
                    <label class="block text-gray-700">Game Date (YYYY-MM-DD):</label>
                    <input type="date" id="gameDate" class="w-full p-2 border rounded" required>
                </div>
                <div>
                    <label class="block text-gray-700">Goals:</label>
                    <input type="number" id="goals" class="w-full p-2 border rounded" min="0" value="0" required>
                </div>
                <div>
                    <label class="block text-gray-700">Assists:</label>
                    <input type="number" id="assists" class="w-full p-2 border rounded" min="0" value="0" required>
                </div>
                <div>
                    <label class="block text-gray-700">Time on Ice (minutes):</label>
                    <input type="number" id="toi" class="w-full p-2 border rounded" min="0" step="0.1" value="0" required>
                </div>
                <div>
                    <label class="block text-gray-700">Blocked Shots:</label>
                    <input type="number" id="blocks" class="w-full p-2 border rounded" min="0" value="0" required>
                </div>
                <div>
                    <label class="block text-gray-700">Scoring Chances For:</label>
                    <input type="number" id="chancesFor" class="w-full p-2 border rounded" min="0" value="0" required>
                </div>
                <div>
                    <label class="block text-gray-700">Scoring Chances Against:</label>
                    <input type="number" id="chancesAgainst" class="w-full p-2 border rounded" min="0" value="0" required>
                </div>
                <div>
                    <label class="block text-gray-700">Corsi For (shot attempts):</label>
                    <input type="number" id="corsiFor" class="w-full p-2 border rounded" min="0" value="0" required>
                </div>
                <div>
                    <label class="block text-gray-700">Corsi Against (shot attempts):</label>
                    <input type="number" id="corsiAgainst" class="w-full p-2 border rounded" min="0" value="0" required>
                </div>
                <div>
                    <label class="block text-gray-700">Fenwick For (unblocked attempts):</label>
                    <input type="number" id="fenwickFor" class="w-full p-2 border rounded" min="0" value="0" required>
                </div>
                <div>
                    <label class="block text-gray-700">Fenwick Against (unblocked attempts):</label>
                    <input type="number" id="fenwickAgainst" class="w-full p-2 border rounded" min="0" value="0" required>
                </div>
                <button type="submit" class="bg-blue-600 text-white py-2 px-4 rounded hover:bg-blue-700">Add Game</button>
            </form>
        </section>
        <section class="bg-white shadow-lg rounded-lg p-6">
            <h2 class="text-2xl font-semibold mb-4">Game History</h2>
            <table id="gameTable" class="w-full border-collapse">
                <thead>
                    <tr class="bg-gray-200">
                        <th class="border p-2">Date</th>
                        <th class="border p-2">Game Score</th>
                        <th class="border p-2">Game Score/60</th>
                        <th class="border p-2">Corsi%</th>
                        <th class="border p-2">Fenwick%</th>
                    </tr>
                </thead>
                <tbody id="gameTableBody"></tbody>
            </table>
            <h3 class="text-xl font-semibold mt-6">Season Averages</h3>
            <p id="seasonGameScore" class="text-gray-700"></p>
            <p id="seasonGameScorePer60" class="text-gray-700"></p>
            <p id="seasonCorsiPercent" class="text-gray-700"></p>
            <p id="seasonFenwickPercent" class="text-gray-700"></p>
        </section>
    </main>
    <footer class="bg-gray-800 text-white text-center py-4">
        <p>Contact: <a href="mailto:carver.watson@gmail.com" class="hover:underline">carver.watson@gmail.com</a> | (920) 287-4014</p>
        <p><a href="https://linkedin.com/in/carverwatson" target="_blank" class="hover:underline">LinkedIn Profile</a></p>
    </footer>
    <script>
        const playerId = 'player1'; // Change to 'player2' for player2.html, etc.

        function calculateGameScore(stats) {
            console.log('Calculating Game Score for:', stats);
            const baseScore = (2 * stats.goals) + (1 * stats.assists) +
                              (0.5 * stats.blocks) - (0.2 * stats.chancesAgainst) +
                              (0.1 * stats.corsiFor) - (0.1 * stats.corsiAgainst) +
                              (0.15 * stats.fenwickFor) - (0.15 * stats.fenwickAgainst) +
                              (0.3 * stats.chancesFor) - (0.3 * stats.chancesAgainst);
            const gameScore = stats.toi > 0 ? (5 * (60 / stats.toi) * baseScore).toFixed(2) : 0;
            console.log('Game Score:', gameScore);
            return gameScore;
        }

        function calculateMetrics(stats) {
            const gameScorePer60 = calculateGameScore(stats); // Already normalized per 60
            const corsiPercent = (stats.corsiFor + stats.corsiAgainst) > 0 ? ((stats.corsiFor / (stats.corsiFor + stats.corsiAgainst)) * 100).toFixed(1) : 0;
            const fenwickPercent = (stats.fenwickFor + stats.fenwickAgainst) > 0 ? ((stats.fenwickFor / (stats.fenwickFor + stats.fenwickAgainst)) * 100).toFixed(1) : 0;
            console.log('Metrics:', { gameScorePer60, corsiPercent, fenwickPercent });
            return { gameScorePer60, corsiPercent, fenwickPercent };
        }

        function saveGameData() {
            const stats = {
                date: document.getElementById('gameDate').value,
                goals: parseInt(document.getElementById('goals').value),
                assists: parseInt(document.getElementById('assists').value),
                toi: parseFloat(document.getElementById('toi').value),
                blocks: parseInt(document.getElementById('blocks').value),
                chancesFor: parseInt(document.getElementById('chancesFor').value),
                chancesAgainst: parseInt(document.getElementById('chancesAgainst').value),
                corsiFor: parseInt(document.getElementById('corsiFor').value),
                corsiAgainst: parseInt(document.getElementById('corsiAgainst').value),
                fenwickFor: parseInt(document.getElementById('fenwickFor').value),
                fenwickAgainst: parseInt(document.getElementById('fenwickAgainst').value)
            };
            console.log('Saving game data:', stats);
            try {
                const games = JSON.parse(localStorage.getItem(playerId) || '[]');
                games.push(stats);
                localStorage.setItem(playerId, JSON.stringify(games));
                console.log('Data saved for player:', playerId);
            } catch (e) {
                console.error('Error saving to localStorage:', e);
                alert('Failed to save game data. Please try again.');
            }
        }

        function loadPlayerData() {
            console.log('Loading data for player:', playerId);
            let games;
            try {
                games = JSON.parse(localStorage.getItem(playerId) || '[]');
            } catch (e) {
                console.error('Error loading from localStorage:', e);
                games = [];
            }
            console.log('Loaded games:', games);
            const tableBody = document.getElementById('gameTableBody');
            tableBody.innerHTML = '';
            let totalGameScore = 0, totalGameScorePer60 = 0, totalCorsiPercent = 0, totalFenwickPercent = 0;
            games.forEach(game => {
                const gameScore = calculateGameScore(game);
                const metrics = calculateMetrics(game);
                const row = `<tr>
                    <td class="border p-2">${game.date}</td>
                    <td class="border p-2">${gameScore}</td>
                    <td class="border p-2">${metrics.gameScorePer60}</td>
                    <td class="border p-2">${metrics.corsiPercent}%</td>
                    <td class="border p-2">${metrics.fenwickPercent}%</td>
                </tr>`;
                tableBody.insertAdjacentHTML('beforeend', row);
                totalGameScore += parseFloat(gameScore);
                totalGameScorePer60 += parseFloat(metrics.gameScorePer60);
                totalCorsiPercent += parseFloat(metrics.corsiPercent);
                totalFenwickPercent += parseFloat(metrics.fenwickPercent);
            });
            const gameCount = games.length;
            document.getElementById('seasonGameScore').textContent = `Average Game Score: ${gameCount > 0 ? (totalGameScore / gameCount).toFixed(2) : 0}`;
            document.getElementById('seasonGameScorePer60').textContent = `Average Game Score per 60: ${gameCount > 0 ? (totalGameScorePer60 / gameCount).toFixed(2) : 0}`;
            document.getElementById('seasonCorsiPercent').textContent = `Average Corsi%: ${gameCount > 0 ? (totalCorsiPercent / gameCount).toFixed(1) : 0}%`;
            document.getElementById('seasonFenwickPercent').textContent = `Average Fenwick%: ${gameCount > 0 ? (totalFenwickPercent / gameCount).toFixed(1) : 0}%`;
        }

        document.getElementById('statsForm').addEventListener('submit', function(e) {
            e.preventDefault();
            console.log('Form submitted');
            saveGameData();
            loadPlayerData();
            document.getElementById('statsForm').reset();
        });

        // Load data on page load
        loadPlayerData();
    </script>
</body>
</html>
