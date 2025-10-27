<!doctype html>
<html lang="ru">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>Тест: Первый уровень Python</title>
  <style>
    :root{--bg:#ffffff;--primary:#1e62d0;--muted:#6b7280;--card:#f8fafc;--maxw:900px}
    *{box-sizing:border-box}
    body{margin:0;font-family:Inter, Roboto, "Helvetica Neue", Arial, sans-serif;background:var(--bg);color:#0f172a}
    .wrap{max-width:var(--maxw);margin:28px auto;padding:20px}
    header{display:flex;align-items:center;gap:16px}
    .logo{width:52px;height:52px;border-radius:10px;background:linear-gradient(135deg,var(--primary),#3aa0ff);display:flex;align-items:center;justify-content:center;color:white;font-weight:700}
    h1{margin:0;font-size:20px}
    p.lead{color:var(--muted);margin:8px 0 18px}
    .card{background:var(--card);padding:18px;border-radius:12px;box-shadow:0 6px 18px rgba(16,24,40,0.03)}
    label.field{display:block;margin-bottom:10px}
    input[name="fio"]{width:100%;padding:10px;border-radius:8px;border:1px solid #e6edf3}
    .controls{display:flex;gap:8px;align-items:center;margin-top:12px}
    button{background:var(--primary);color:white;padding:10px 14px;border-radius:8px;border:0;font-weight:600;cursor:pointer}
    button.ghost{background:transparent;color:var(--primary);border:1px solid rgba(30,98,208,0.12)}
    .questions{margin-top:18px}
    .q{padding:14px;border-radius:10px;border:1px solid #eef2f6;margin-bottom:12px}
    .q h3{margin:0 0 8px;font-size:15px}
    pre{background:#f3f4f6;padding:8px;border-radius:6px;overflow-x:auto;font-family:Consolas,monospace;font-size:14px;margin:6px 0}
    .answers{display:flex;flex-direction:column;gap:8px}
    .small{font-size:13px;color:var(--muted)}
    .timer{font-weight:600;color:var(--primary);margin-bottom:10px}
    .result{margin-top:18px;padding:14px;border-radius:10px;background:#eef6ff;border:1px solid rgba(30,98,208,0.12)}
    .copy-area{margin-top:8px;display:flex;gap:8px}
    textarea#resultText{width:100%;height:80px;padding:10px;border-radius:8px;border:1px solid #e6edf3}
    @media (max-width:640px){.wrap{padding:12px}h1{font-size:18px}}
  </style>
</head>
<body>
  <div class="wrap">
    <header>
      <div class="logo">Py</div>
      <div>
        <h1>Тест — Первый уровень Python (20 вопросов)</h1>
        <p class="lead">Введите ФИО, пройдите тест. Вопросы перемешиваются при каждом запуске. Порог прохождения: 15/20. Время: 30 минут.</p>
      </div>
    </header>

    <div class="card" id="startCard">
      <label class="field">
        <div class="small">ФИО</div>
        <input type="text" id="fio" placeholder="Иванов Иван Иванович" />
      </label>
      <div class="controls">
        <button id="startBtn">Начать тест</button>
      </div>
    </div>

    <div id="timerBlock" class="timer" style="display:none;text-align:right;"></div>

    <form id="testForm" style="display:none;" class="card">
      <div id="questionBlock" class="questions"></div>
      <div style="display:flex;gap:8px;justify-content:space-between;margin-top:12px">
        <button type="button" id="prevBtn" class="ghost">Назад</button>
        <button type="button" id="nextBtn">Далее</button>
      </div>
    </form>

    <div id="resultBlock" style="display:none;" class="card result">
      <div id="summary"></div>
      <div class="copy-area">
        <textarea id="resultText" readonly></textarea>
        <div style="display:flex;flex-direction:column;gap:8px">
          <button id="copyBtn">Скопировать</button>
          <button id="restartBtn" class="ghost">Пройти заново</button>
        </div>
      </div>
      <p class="small" style="margin-top:8px">Скопируй текст и отправь в Telegram: <a href="https://t.me/makcuma28" target="_blank">@makcuma28</a></p>
    </div>

  </div>

  <script>
    const QUESTIONS = [
      {q:'Какая команда в Python используется для вывода информации на экран?',opts:['echo()','print()','output()','display()'],a:[1]},
      {q:'Какой тип данных используется для хранения целых чисел?',opts:['float','str','int','bool'],a:[2]},
      {q:'Какие операторы используются для сравнения в Python? (выберите все подходящие)',opts:['=','==','!=','+='],a:[1,2],multi:true},
      {q:'Что делает команда input()?',opts:['Выводит текст','Сохраняет файл','Получает данные от пользователя','Завершает программу'],a:[2]},
      {q:'Какой результат выполнения кода:<pre><code>print(3 + 2 * 2)</code></pre>',opts:['10','7','8','9'],a:[1]},
      {q:'Что делает цикл:<pre><code>for i in range(5):\n    print(i)</code></pre>',opts:['Повторяет код 4 раза','Повторяет код 5 раз','Повторяет код бесконечно','Не запускается'],a:[1]},
      {q:'Что выведет код:<pre><code>for i in range(3):\n    print(i * 2)</code></pre>',opts:['0 1 2','0 2 4','2 4 6','1 3 5'],a:[1]},
      {q:'Что делает функция:<pre><code>len([10, 20, 30])</code></pre>',opts:['Складывает числа','Возвращает длину списка','Умножает элементы','Очищает список'],a:[1]},
      {q:'Что делает выражение:<pre><code>numbers.append(5)</code></pre>',opts:['Добавляет элемент в список','Удаляет элемент','Создаёт новый список','Возвращает длину'],a:[0]},
      {q:'Какое значение будет у переменной result после выполнения кода:<pre><code>numbers = [1, 2, 3, 4, 5]\nresult = sum(numbers)</code></pre>',opts:['10','15','20','25'],a:[1]},
      {q:'Что делает ключевое слово def в Python?',opts:['Создаёт цикл','Определяет функцию','Завершает программу','Определяет переменную'],a:[1]},
      {q:'Как правильно вызвать функцию hello()? ',opts:['call hello','run hello()','hello()','def hello()'],a:[2]},
      {q:'Что делает оператор return в функции?',opts:['Возвращает значение из функции','Завершает программу','Печатает результат','Повторяет цикл'],a:[0]},
      {q:'Что выведет код:<pre><code>for i in range(1, 6):\n    if i % 2 == 0:\n        print(i)</code></pre>',opts:['1 3 5','2 4','1 2 3 4 5','0 2 4 6'],a:[1]},
      {q:'Что делает выражение my_list[0]?',opts:['Возвращает последний элемент списка','Возвращает первый элемент списка','Удаляет элемент','Добавляет элемент'],a:[1]},
      {q:'Что выведет код:<pre><code>x = 0\nwhile x < 3:\n    print(x)\n    x += 1</code></pre>',opts:['0 1 2','1 2 3','0 1 2 3','3 2 1'],a:[0]},
      {q:'Как досрочно завершить цикл while?',opts:['continue','end','stop','break'],a:[3]},
      {q:'Что делает метод list.remove(x)?',opts:['Удаляет первый элемент списка','Удаляет элемент x','Удаляет все элементы','Возвращает длину списка'],a:[1]},
      {q:'Что выведет код:<pre><code>def add(a, b):\n    return a + b\nprint(add(2, 3))</code></pre>',opts:['2','3','5','Ошибка'],a:[2]},
      {q:'Что делает функция range(3)?',opts:['Создаёт список из 3 элементов','Создаёт последовательность 0, 1, 2','Создаёт случайные числа','Ничего не делает'],a:[1]}
    ];

    function shuffle(array){for(let i=array.length-1;i>0;i--){const j=Math.floor(Math.random()*(i+1));[array[i],array[j]]=[array[j],array[i]];}}

    let current=0,answers={},timer,remaining=30*60;

    const startBtn=document.getElementById('startBtn');
    const startCard=document.getElementById('startCard');
    const testForm=document.getElementById('testForm');
    const questionBlock=document.getElementById('questionBlock');
    const nextBtn=document.getElementById('nextBtn');
    const prevBtn=document.getElementById('prevBtn');
    const resultBlock=document.getElementById('resultBlock');
    const summary=document.getElementById('summary');
    const resultText=document.getElementById('resultText');
    const copyBtn=document.getElementById('copyBtn');
    const restartBtn=document.getElementById('restartBtn');
    const timerBlock=document.getElementById('timerBlock');

    let qs=[];

    startBtn.onclick=()=>{
      const fio=document.getElementById('fio').value.trim();
      if(!fio)return alert('Введите ФИО');
      startCard.style.display='none';
      testForm.style.display='block';
      timerBlock.style.display='block';
      qs=JSON.parse(JSON.stringify(QUESTIONS));
      shuffle(qs);
      showQuestion();
      startTimer();
    };

    function startTimer(){
      updateTimer();
      timer=setInterval(()=>{
        remaining--;
        if(remaining<=0){clearInterval(timer);finish();}
        updateTimer();
      },1000);
    }

    function updateTimer(){
      const m=Math.floor(remaining/60);const s=remaining%60;
      timerBlock.textContent=`Осталось времени: ${m}:${s.toString().padStart(2,'0')}`;
    }

    function showQuestion(){
      questionBlock.innerHTML='';
      const q=qs[current];
      const qDiv=document.createElement('div');qDiv.className='q';
      qDiv.innerHTML=`<h3>${current+1}. ${q.q}</h3>`;
      q.opts.forEach((opt,i)=>{
        const id='q'+current+'_'+i;
        const label=document.createElement('label');label.style.display='flex';label.style.alignItems='center';label.style.gap='8px';
        const inp=document.createElement('input');inp.type=q.multi?'checkbox':'radio';inp.name='q_'+current;inp.value=i;
        if(answers[current]&&answers[current].includes(i))inp.checked=true;
        const span=document.createElement('span');span.textContent=opt;
        label.appendChild(inp);label.appendChild(span);qDiv.appendChild(label);
      });
      questionBlock.appendChild(qDiv);
      prevBtn.style.display=current===0?'none':'inline-block';
      nextBtn.textContent=current===qs.length-1?'Завершить':'Далее';
    }

    nextBtn.onclick=()=>{
      saveAnswers();
      if(current<qs.length-1){current++;showQuestion();}
      else finish();
    };
    prevBtn.onclick=()=>{saveAnswers();if(current>0){current--;showQuestion();}};

    function saveAnswers(){
      const nodes=document.querySelectorAll('input[name="q_'+current+'"]');
      answers[current]=Array.from(nodes).filter(n=>n.checked).map(n=>Number(n.value));
    }

    function finish(){
      clearInterval(timer);
      testForm.style.display='none';timerBlock.style.display='none';
      let score=0;
      qs.forEach((q,i)=>{
        const correct=q.a.slice().sort();
        const sel=(answers[i]||[]).slice().sort();
        const equal=correct.length===sel.length&&correct.every((v,j)=>v===sel[j]);
        if(equal)score++;
      });
      const fio=document.getElementById('fio').value.trim();
      const pass=score>=15;
      summary.innerHTML=`<strong>ФИО:</strong> ${fio}<br><strong>Баллы:</strong> ${score}/20<br><strong>Статус:</strong> ${pass?'Прошёл первый уровень':'Не прошёл'}`;
      resultText.value=`${fio} , ${score}/20 , ${pass?'Прошёл первый уровень':'Не прошёл'}`;
      resultBlock.style.display='block';
    }

    copyBtn.onclick=async()=>{await navigator.clipboard.writeText(resultText.value);copyBtn.textContent='Скопировано';setTimeout(()=>copyBtn.textContent='Скопировать',1500);};
    restartBtn.onclick=()=>location.reload();
  </script>
</body>
</html>
