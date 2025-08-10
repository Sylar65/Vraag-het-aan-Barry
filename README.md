# Vraag-het-aan-Barry
Vraag het aan Barry gaat over de conventies van bridge
<!DOCTYPE html>
<html lang="nl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Vraag Barry over Bridge Conventies</title>
    <style>
        body {
            font-family: Georgia, serif;
            background: linear-gradient(135deg, #1a237e 0%, #000051 50%, #1a237e 100%);
            min-height: 100vh;
            color: #333;
            margin: 0;
            padding: 20px;
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            background: white;
            border-radius: 20px;
            padding: 40px;
            box-shadow: 0 15px 40px rgba(0,0,0,0.4);
            border: 3px solid #d4af37;
        }
        
        .header {
            text-align: center;
            margin-bottom: 30px;
        }
        
        .header h1 {
            color: #1a237e;
            font-size: 2.5em;
            margin-bottom: 10px;
        }
        
        .header p {
            color: #666;
            font-size: 1.2em;
            font-style: italic;
        }
        
        .barry-intro {
            display: flex;
            align-items: center;
            gap: 25px;
            margin-bottom: 30px;
            padding: 25px;
            background: linear-gradient(135deg, #f8f9fa 0%, #e9ecef 100%);
            border-radius: 15px;
            border-left: 5px solid #d4af37;
        }
        
        .barry-avatar {
            width: 100px;
            height: 100px;
            background: #1a237e;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 2.5em;
            color: #d4af37;
            border: 3px solid #d4af37;
            flex-shrink: 0;
        }
        
        .intro-text h2 {
            color: #1a237e;
            margin-bottom: 10px;
        }
        
        .intro-text p {
            color: #555;
            line-height: 1.6;
            margin-bottom: 10px;
        }
        
        .search-section {
            background: #f8f9fa;
            padding: 25px;
            border-radius: 15px;
            border: 2px solid #d4af37;
            margin-bottom: 30px;
        }
        
        .form-group {
            margin-bottom: 20px;
        }
        
        .form-group label {
            display: block;
            margin-bottom: 8px;
            font-weight: bold;
            color: #1a237e;
        }
        
        .form-group input {
            width: 100%;
            padding: 12px;
            border: 2px solid #ddd;
            border-radius: 8px;
            font-size: 1.1em;
        }
        
        .form-group input:focus {
            outline: none;
            border-color: #1a237e;
            box-shadow: 0 0 10px rgba(26, 35, 126, 0.2);
        }
        
        .ask-button {
            background: #1a237e;
            color: white;
            padding: 15px 30px;
            border: none;
            border-radius: 25px;
            font-size: 1.1em;
            cursor: pointer;
            display: block;
            margin: 20px auto 0;
            transition: all 0.3s ease;
        }
        
        .ask-button:hover {
            background: #000051;
            transform: translateY(-2px);
            box-shadow: 0 5px 15px rgba(0,0,0,0.3);
        }
        
        .answer-section {
            display: none;
            margin-top: 30px;
        }
        
        .barry-response {
            background: linear-gradient(135deg, #f8f9fa 0%, #e9ecef 100%);
            border-radius: 15px;
            padding: 30px;
            border-left: 5px solid #d4af37;
        }
        
        .response-header {
            display: flex;
            align-items: center;
            gap: 20px;
            margin-bottom: 25px;
        }
        
        .barry-avatar-small {
            width: 80px;
            height: 80px;
            background: #1a237e;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 2em;
            color: #d4af37;
            border: 3px solid #d4af37;
            flex-shrink: 0;
        }
        
        .response-title {
            color: #1a237e;
            font-size: 1.6em;
            margin: 0;
        }
        
        .convention-explanation {
            background: white;
            padding: 25px;
            border-radius: 10px;
            border: 1px solid #ddd;
            margin-bottom: 20px;
        }
        
        .convention-explanation h3 {
            color: #1a237e;
            margin-top: 0;
            margin-bottom: 15px;
            font-size: 1.3em;
        }
        
        .convention-explanation h4 {
            color: #0066cc;
            margin-top: 20px;
            margin-bottom: 10px;
        }
        
        .bid-example {
            background: #e3f2fd;
            padding: 15px;
            border-radius: 8px;
            margin: 15px 0;
            border-left: 4px solid #2196f3;
        }
        
        .bid-sequence {
            font-family: 'Courier New', monospace;
            font-weight: bold;
            color: #1565c0;
            margin-bottom: 5px;
        }
        
        .requirements {
            background: #f1f8e9;
            padding: 15px;
            border-radius: 8px;
            margin: 15px 0;
            border-left: 4px solid #4caf50;
        }
        
        .requirements h4 {
            color: #2e7d32;
            margin-top: 0;
        }
        
        .warning {
            background: #fff3e0;
            padding: 15px;
            border-radius: 8px;
            margin: 15px 0;
            border-left: 4px solid #ff9800;
        }
        
        .warning h4 {
            color: #ef6c00;
            margin-top: 0;
        }
        
        .card-symbols {
            font-size: 1.1em;
            font-weight: bold;
        }
        
        .spades { color: black; }
        .hearts { color: red; }
        .diamonds { color: red; }
        .clubs { color: black; }
        
        .convention-categories {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 20px;
            margin-top: 30px;
        }
        
        .category-card {
            background: white;
            padding: 25px;
            border-radius: 12px;
            border: 2px solid #d4af37;
            cursor: pointer;
            text-align: center;
            transition: all 0.3s ease;
        }
        
        .category-card:hover {
            background: #e3f2fd;
            transform: translateY(-3px);
            box-shadow: 0 8px 25px rgba(0,0,0,0.15);
        }
        
        .category-card h3 {
            color: #1a237e;
            margin-bottom: 15px;
            font-size: 1.2em;
        }
        
        .category-card p {
            color: #666;
            font-size: 0.95em;
            margin-bottom: 15px;
        }
        
        .category-examples {
            font-size: 0.85em;
            color: #888;
            font-style: italic;
        }
        
        @media (max-width: 768px) {
            .barry-intro,
            .response-header {
                flex-direction: column;
                text-align: center;
            }
            
            .container {
                padding: 20px;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="header">
            <h1>🎩 Vraag Barry over Bridge Conventies</h1>
            <p>De complete conventie encyclopedie van de Bridge Illusionist</p>
        </div>
        
        <div class="barry-intro">
            <div class="barry-avatar">🎩</div>
            <div class="intro-text">
                <h2>Welkom bij Barry's Conventie Gids!</h2>
                <p>Hallo bridgevrienden! Ik ben Barry, en ik heb alle bridge conventies bestudeerd - van de klassieke Stayman tot de meest geavanceerde systemen. Stel me een vraag over elke conventie, en ik onthul de geheimen erachter!</p>
                <p><strong>Tip:</strong> Typ de naam van een conventie (zoals "Stayman", "Blackwood", "Jacoby") of stel een vraag zoals "Hoe verdedig ik tegen 1SA?"</p>
            </div>
        </div>
        
        <div class="search-section">
            <div class="form-group">
                <label for="userName">Jouw naam:</label>
                <input type="text" id="userName" placeholder="Hoe mag Barry je noemen?">
            </div>
            
            <div class="form-group">
                <label for="conventionQuestion">Vraag over een bridge conventie:</label>
                <input type="text" id="conventionQuestion" placeholder="Bijv: Wat is Stayman? of Hoe werkt Blackwood? of Multi 2 opening">
            </div>
            
            <button class="ask-button" onclick="askBarry()">Vraag het aan Barry!</button>
        </div>

        <div id="answer-section" class="answer-section">
            <div class="barry-response">
                <div class="response-header">
                    <div class="barry-avatar-small">🎩</div>
                    <h2 class="response-title" id="barry-greeting"></h2>
                </div>
                <div id="barry-answer"></div>
            </div>
        </div>
        
        <div class="convention-categories">
            <div class="category-card" onclick="quickConvention('Stayman')">
                <h3>🎯 Basisconventies</h3>
                <p>De fundamentele conventies die elke bridgespeler moet kennen</p>
                <div class="category-examples">Stayman • Blackwood • Jacoby Transfers</div>
            </div>
            
            <div class="category-card" onclick="quickConvention('Multi 2♦')">
                <h3>🚀 Moderne Openingen</h3>
                <p>Geavanceerde openingssystemen en zwakke twee-biedingen</p>
                <div class="category-examples">Multi 2♦ • Muiderberg • Weak Two</div>
            </div>
            
            <div class="category-card" onclick="quickConvention('DONT')">
                <h3>🛡 Verdediging tegen 1SA</h3>
                <p>Systemen om te interfereren na tegenstanders 1SA opening</p>
                <div class="category-examples">DONT • Landy • Cappelletti • Multi-Landy</div>
            </div>
            
            <div class="category-card" onclick="quickConvention('Roman Key Card')">
                <h3>🏰 Slam Conventies</h3>
                <p>Geavanceerde technieken voor slam onderzoek</p>
                <div class="category-examples">RKC Blackwood • Gerber • Splinters • Cue-bids</div>
            </div>
            
            <div class="category-card" onclick="quickConvention('Negatief doublet')">
                <h3>⚔ Competitieve Biedingen</h3>
                <p>Conventies na tussenbiedingen van tegenstanders</p>
                <div class="category-examples">Negatief Doublet • Lebensohl • Support Doublet</div>
            </div>
            
            <div class="category-card" onclick="quickConvention('Lavinthal signaal')">
                <h3>🔍 Signaal Systemen</h3>
                <p>Verdedigingstechnieken en partner communicatie</p>
                <div class="category-examples">Lavinthal • Count Signalen • Attitude Signalen</div>
            </div>
        </div>
    </div>

    <script>
        // Barry's complete Bridge Conventie Encyclopedie
        const conventionDatabase = {
            // === STAYMAN VARIANTEN ===
            'stayman': {
                keywords: ['stayman', '2♣', '2 klaveren'],
                title: 'De Stayman Conventie',
                content: `
                    <div class="convention-explanation">
                        <h3>🎯 Barry onthult: De Stayman Conventie</h3>
                        <p>Ah, de beroemde Stayman! Een van de meest elegante conventies in bridge. Laat me je de geheimen ervan onthullen...</p>
                        
                        <h4>Wat is Stayman?</h4>
                        <p>Stayman is een conventioneel bod van <strong>2♣</strong> na partner's 1SA opening. Het vraagt: "Partner, heb je een 4-kaart hoge kleur?" Dit helpt je een 4-4 fit in harten of schoppen te vinden.</p>
                        
                        <div class="bid-example">
                            <div class="bid-sequence">1SA - 2♣ - ?</div>
                            <p><strong>Partner's antwoorden:</strong><br>
                            • 2♦ = Geen 4-kaart hoge kleur<br>
                            • 2♥ = 4-kaart harten (kan ook 4 schoppen hebben)<br>
                            • 2♠ = 4-kaart schoppen, geen 4 harten</p>
                        </div>
                        
                        <div class="requirements">
                            <h4>Wanneer gebruik je Stayman?</h4>
                            <ul>
                                <li>Je hebt minimaal een 4-kaart hoge kleur</li>
                                <li>Minimaal 8+ punten (voor game interest)</li>
                                <li>Je zoekt een 4-4 fit in harten of schoppen</li>
                            </ul>
                        </div>
                        
                        <h4>Barry's Geheime Tips:</h4>
                        <p>• <strong>Garbage Stayman:</strong> Met een zwakke hand en beide hoge kleuren kun je Stayman gebruiken om ergens op 2-niveau te eindigen<br>
                        • <strong>Na 2♦:</strong> Je kunt nog steeds je 4-kaart hoge kleur bieden om partner een laatste kans te geven<br>
                        • <strong>Smolen Transfer:</strong> Met 5-4 in de hoge kleuren: gebruik Stayman eerst, dan spring in je 4-kaart</p>
                        
                        <div class="warning">
                            <h4>Let op!</h4>
                            <p>Gebruik Stayman niet met alleen een 4-kaart hoge kleur en 4-3-3-3 verdeling met 8-9 punten - dan is 1SA vaak het beste contract!</p>
                        </div>
                    </div>
                `
            },
            
            // === BLACKWOOD ===
            'blackwood': {
                keywords: ['blackwood', '4sa', '4 sa', 'azen vragen'],
                title: 'Blackwood Conventie',
                content: `
                    <div class="convention-explanation">
                        <h3>🏰 Barry's Slam Geheimen: Blackwood</h3>
                        <p>Hier onthul ik een van de machtigste wapens voor slam onderzoek - de Blackwood conventie!</p>
                        
                        <h4>Wat is Blackwood?</h4>
                        <p>4SA vraagt naar het aantal azen bij je partner. Simple as that! Maar er zit meer finesse in dan je denkt...</p>
                        
                        <div class="bid-example">
                            <div class="bid-sequence">4SA - ?</div>
                            <p><strong>Partner's antwoorden:</strong><br>
                            • 5♣ = 0 of 4 azen<br>
                            • 5♦ = 1 aas<br>
                            • 5♥ = 2 azen<br>
                            • 5♠ = 3 azen</p>
                        </div>
                        
                        <h4>Na de azen: Heren vragen</h4>
                        <p>Als je alle azen hebt, vraag je met <strong>5SA</strong> naar heren:</p>
                        <div class="bid-example">
                            <div class="bid-sequence">4SA - 5♥ - 5SA - ?</div>
                            <p>Zelfde schaal: 6♣ = 0/4, 6♦ = 1, 6♥ = 2, 6♠ = 3 heren</p>
                        </div>
                        
                        <div class="requirements">
                            <h4>Wanneer gebruik je Blackwood?</h4>
                            <ul>
                                <li>Je hebt een troefkleur vastgesteld</li>
                                <li>Je denkt aan slam (33+ punten samen)</li>
                                <li>Je hebt geen renonce in ongecontroleerde zijkleuren</li>
                            </ul>
                        </div>
                        
                        <div class="warning">
                            <h4>Barry's Waarschuwing!</h4>
                            <p>Gebruik Blackwood NIET met een renonce in een zijkleur - je kunt wel alle azen hebben maar toch down gaan door die renonce!</p>
                        </div>
                        
                        <h4>Moderne Varianten:</h4>
                        <p>• <strong>Roman Key Card Blackwood:</strong> Troef-heer telt als 5de aas<br>
                        • <strong>1430 RKC:</strong> 5♣ = 1/4, 5♦ = 0/3 sleutelkaarten<br>
                        • <strong>Exclusion Blackwood:</strong> Spring naar 4-niveau in zijkleur = azen behalve in die kleur</p>
                    </div>
                `
            }
        };
        
        // Default antwoord
        const defaultAnswer = "Interessante vraag! Ik ben Barry, specialist in bridge conventies. Ik kan je helpen met allerlei conventies zoals Stayman, Blackwood, Jacoby Transfers, Multi 2♦, DONT, Negatief Doublets, Roman Key Card, Lebensohl, en nog veel meer! Probeer eens een specifieke conventie naam te typen, of vraag: 'Hoe verdedig ik tegen 1SA?' of 'Wat zijn slam conventies?'";

        function askBarry() {
            const userName = document.getElementById('userName').value.trim();
            const question = document.getElementById('conventionQuestion').value.trim();
            
            if (!userName) {
                alert('Vertel Barry je naam zodat hij je persoonlijk kan aanspreken!');
                return;
            }
            
            if (!question) {
                alert('Stel Barry een vraag over een bridge conventie!');
                return;
            }
            
            const response = findConventionAnswer(question);
            showBarryAnswer(userName, question, response);
        }
        
        function quickConvention(conventionName) {
            const userName = document.getElementById('userName').value.trim() || 'bridgevriend';
            document.getElementById('conventionQuestion').value = conventionName;
            const response = findConventionAnswer(conventionName);
            showBarryAnswer(userName, Wat is ${conventionName}?, response);
        }
        
        function findConventionAnswer(question) {
            const lowerQuestion = question.toLowerCase();
            
            // Zoek naar matchende conventie
            for (const convention in conventionDatabase) {
                const convData = conventionDatabase[convention];
                
                // Check of conventie naam direct voorkomt
                if (lowerQuestion.includes(convention)) {
                    return {
                        title: convData.title,
                        content: convData.content
                    };
                }
                
                // Check keywords
                for (const keyword of convData.keywords) {
                    if (lowerQuestion.includes(keyword)) {
                        return {
                            title: convData.title,
                            content: convData.content
                        };
                    }
                }
            }
            
            // Default response
            return {
                title: 'Barry\'s Conventie Hulp',
                content: `
                    <div class="convention-explanation">
                        <h3>🎩 Barry helpt je verder!</h3>
                        <p>${defaultAnswer}</p>
                        <p><strong>Populaire conventies die ik ken:</strong></p>
                        <p>• <strong>Basis:</strong> Stayman, Blackwood, Jacoby Transfers<br>
                        • <strong>Openingen:</strong> Multi 2♦, Weak Two, Muiderberg<br>
                        • <strong>Verdediging:</strong> DONT, Landy, Cappelletti<br>
                        • <strong>Competitief:</strong> Negatief Doublet, Lebensohl<br>
                        • <strong>Slam:</strong> Roman Key Card, Gerber, Splinters<br>
                        • <strong>Signalen:</strong> Lavinthal, Count, Attitude</p>
                    </div>
                `
            };
        }
        
        function showBarryAnswer(userName, question, response) {
            document.getElementById('barry-greeting').textContent = Hallo ${userName}!;
            document.getElementById('barry-answer').innerHTML = `
                <div style="background: white; padding: 20px; border-radius: 10px; margin-bottom: 15px; border-left: 4px solid #1a237e;">
                    <strong>Je vroeg:</strong> "${question}"
                </div>
                ${response.content}
                <div style="margin-top: 25px; padding: 15px; background: #e3f2fd; border-radius: 8px; text-align: center; font-style: italic; color: #1565c0;">
                    "Heb je nog vragen over andere conventies? Stel ze gerust! Ik ken er nog veel meer..." - Barry 🎩
                </div>
            `;
            
            document.getElementById('answer-section').style.display = 'block';
            document.getElementById('answer-section').scrollIntoView({behavior: 'smooth'});
        }
    </script>
</body>
</html>
