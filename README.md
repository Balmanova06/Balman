# Balman
Psyhelper
(HTML ішіне <script> ретінде қосылады)

<script>
  async function askAI(question) {
    const response = await fetch("https://api.openai.com/v1/chat/completions", {
      method: "POST",
      headers: {
        "Content-Type": "application/json",
        "Authorization": "Bearer СІЗДІҢ_API_КІЛТ"
      },
      body: JSON.stringify({
        model: "gpt-4",
        messages: [{ role: "user", content: question }]
      })
    });

    const data = await response.json();
    alert("Жауап: " + data.choices[0].message.content);
  }
</script>
<button onclick="askAI('Мен стресс деңгейімді қалай түсіре аламын?')">Кеңес сұрау</button>

