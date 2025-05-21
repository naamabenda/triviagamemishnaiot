<!DOCTYPE html>
<html lang="he" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>משחק טריוויה - פרקי אבות</title>
    <style>
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background-color: #f0f8ff;
            text-align: center;
            margin: 0;
            padding: 20px;
            direction: rtl;
        }
        .container {
            max-width: 800px;
            margin: 0 auto;
            background-color: white;
            border-radius: 15px;
            padding: 20px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
        }
        h1 {
            color: #4b0082;
            margin-bottom: 30px;
        }
        .menu {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 15px;
            margin: 30px 0;
        }
        .mishna-btn {
            background-color: #6495ed;
            color: white;
            border: none;
            border-radius: 10px;
            padding: 20px 10px;
            font-size: 20px;
            cursor: pointer;
            transition: all 0.3s;
        }
        .mishna-btn:hover {
            background-color: #4169e1;
            transform: translateY(-5px);
            box-shadow: 0 6px 10px rgba(0, 0, 0, 0.2);
        }
        .question-container {
            display: none;
            margin-top: 20px;
        }
        .question {
            font-size: 22px;
            margin-bottom: 20px;
            color: #333;
        }
        .answers {
            display: grid;
            grid-template-columns: 1fr;
            gap: 10px;
        }
        .answer-btn {
            background-color: #e6e6fa;
            border: 2px solid #d8bfd8;
            border-radius: 8px;
            padding: 15px;
            font-size: 18px;
            cursor: pointer;
            transition: all 0.2s;
            text-align: right;
        }
        .answer-btn:hover {
            background-color: #d8bfd8;
        }
        .feedback {
            font-size: 24px;
            margin: 15px 0;
            min-height: 30px;
        }
        .score {
            font-size: 20px;
            color: #4b0082;
            font-weight: bold;
            margin: 15px 0;
        }
        .mishna-text {
            background-color: #f5f5f5;
            border-right: 5px solid #6495ed;
            padding: 15px;
            text-align: right;
            margin: 20px 0;
            border-radius: 5px;
            max-height: 150px;
            overflow-y: auto;
            font-size: 18px;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>משחק טריוויה - פרקי אבות</h1>
        <div id="score" class="score">ניקוד: 0</div>
        
        <div id="menu-screen">
            <h2>בחר משנה:</h2>
            <div class="menu">
                <button class="mishna-btn" onclick="selectMishna(1)">משנה א'</button>
                <button class="mishna-btn" onclick="selectMishna(2)">משנה ב'</button>
                <button class="mishna-btn" onclick="selectMishna(3)">משנה ג'</button>
                <button class="mishna-btn" onclick="selectMishna(4)">משנה ד'</button>
                <button class="mishna-btn" onclick="selectMishna(5)">משנה ה'</button>
            </div>
        </div>
        
        <div id="question-screen" class="question-container">
            <div id="mishna-text" class="mishna-text"></div>
            <div id="question" class="question"></div>
            <div id="answers" class="answers"></div>
            <div id="feedback" class="feedback"></div>
        </div>
    </div>

    <script>
        // משתנים גלובליים
        let currentMishna = 0;
        let currentQuestionIndex = 0;
        let score = 0;
        let questions = [];
        
        // טקסט המשניות
        const mishnayot = [
            "משה קבל תורה מסיני, ומסרה ליהושע, ויהושע לזקנים, וזקנים לנביאים, ונביאים מסרוה לאנשי כנסת הגדולה. הם אמרו שלשה דברים, הוו מתונים בדין, והעמידו תלמידים הרבה, ועשו סייג לתורה.",
            "שמעון הצדיק היה משירי כנסת הגדולה. הוא היה אומר, על שלשה דברים העולם עומד, על התורה ועל העבודה ועל גמילות חסדים.",
            "אנטיגנוס איש סוכו קבל משמעון הצדיק. הוא היה אומר, אל תהיו כעבדים המשמשין את הרב על מנת לקבל פרס, אלא הוו כעבדים המשמשין את הרב שלא על מנת לקבל פרס, ויהי מורא שמים עליכם.",
            "יוסי בן יועזר איש צרדה ויוסי בן יוחנן איש ירושלים קבלו מהם. יוסי בן יועזר איש צרדה אומר, יהי ביתך בית ועד לחכמים, והוי מתאבק בעפר רגליהם, והוי שותה בצמא את דבריהם.",
            "יוסי בן יוחנן איש ירושלים אומר, יהי ביתך פתוח לרוחה, ויהיו עניים בני ביתך, ואל תרבה שיחה עם האשה. באשתו אמרו, קל וחומר באשת חברו. מכאן אמרו חכמים, כל זמן שאדם מרבה שיחה עם האשה, גורם רעה לעצמו, ובוטל מדברי תורה, וסופו יורש גיהנום."
        ];

        // מאגר השאלות
        const allQuestions = [
            // משנה א'
            [
                {
                    question: "ממי קיבל משה את התורה לפי המשנה?",
                    answers: ["מאברהם אבינו", "מסיני (מהר סיני)", "מאהרן הכהן"],
                    correct: 1
                },
                {
                    question: "מי היתה החוליה האחרונה בשרשרת המסירה המוזכרת במשנה?",
                    answers: ["יהושע", "הנביאים", "אנשי כנסת הגדולה"],
                    correct: 2
                },
                {
                    question: "כמה דברים אמרו אנשי כנסת הגדולה?",
                    answers: ["שלושה דברים", "ארבעה דברים", "שני דברים"],
                    correct: 0
                },
                {
                    question: "מהו אחד מהדברים שאמרו אנשי כנסת הגדולה?",
                    answers: ["הוו שמחים בחלקכם", "הוו מתונים בדין", "אל תפרשו מן הציבור"],
                    correct: 1
                },
                {
                    question: "מה הכוונה ב\"עשו סייג לתורה\"?",
                    answers: ["לבנות גדר פיזית סביב בית המקדש", "להרחיק את האדם מן העבירה באמצעות הרחקות וגדרים", "להקפיד רק על מצוות מהתורה ולא על מצוות דרבנן"],
                    correct: 1
                }
            ],
            // משנה ב'
            [
                {
                    question: "מי היה שמעון הצדיק?",
                    answers: ["מתלמידי הלל ושמאי", "משירי כנסת הגדולה", "מהחשמונאים"],
                    correct: 1
                },
                {
                    question: "על כמה דברים העולם עומד לפי שמעון הצדיק?",
                    answers: ["שני דברים", "שלושה דברים", "ארבעה דברים"],
                    correct: 1
                },
                {
                    question: "מהם שלושת הדברים שעליהם העולם עומד לפי המשנה?",
                    answers: ["על התורה, על העבודה ועל גמילות חסדים", "על הדין, על האמת ועל השלום", "על התפילה, על המשפחה ועל הצדקה"],
                    correct: 0
                },
                {
                    question: "מה הכוונה ב\"עבודה\" בהקשר של המשנה?",
                    answers: ["עבודת כפיים", "עבודת המידות", "עבודת ה' (תפילה וקורבנות)"],
                    correct: 2
                },
                {
                    question: "מה פירוש המושג \"גמילות חסדים\"?",
                    answers: ["עזרה לזולת והטבה עמו", "לימוד תורה לשמה", "שמירת מצוות בין אדם למקום"],
                    correct: 0
                }
            ],
            // משנה ג'
            [
                {
                    question: "ממי קיבל אנטיגנוס איש סוכו את המסורת?",
                    answers: ["מיוסי בן יועזר", "משמעון הצדיק", "מאנשי כנסת הגדולה"],
                    correct: 1
                },
                {
                    question: "מה היה המסר המרכזי של אנטיגנוס איש סוכו?",
                    answers: ["לעבוד את ה' לשם קבלת שכר", "לעבוד את ה' שלא על מנת לקבל פרס", "לעבוד את ה' רק מתוך אהבה ולא מתוך יראה"],
                    correct: 1
                },
                {
                    question: "למה משווה אנטיגנוס את המאמינים במשנתו?",
                    answers: ["לעבדים המשמשים את הרב", "לבנים המשמשים את אביהם", "לתלמידים המשמשים את רבם"],
                    correct: 0
                },
                {
                    question: "מה מוסיף אנטיגנוס בסוף דבריו?",
                    answers: ["\"ויהי מורא שמים עליכם\"", "\"וקנה לך חבר\"", "\"והוי דן את כל האדם לכף זכות\""],
                    correct: 0
                },
                {
                    question: "איזו מידה חשובה מודגשת בדברי אנטיגנוס?",
                    answers: ["מידת הענווה", "מידת הזריזות", "מידת היראה וטוהר המניעים"],
                    correct: 2
                }
            ],
            // משנה ד'
            [
                {
                    question: "מי קיבלו את המסורת מאנטיגנוס איש סוכו?",
                    answers: ["הלל ושמאי", "יוסי בן יועזר ויוסי בן יוחנן", "שמעיה ואבטליון"],
                    correct: 1
                },
                {
                    question: "מהיכן היה יוסי בן יועזר?",
                    answers: ["מירושלים", "מצרדה", "מסוכו"],
                    correct: 1
                },
                {
                    question: "מה פירוש \"יהי ביתך בית ועד לחכמים\"?",
                    answers: ["שיש ללמד תורה רק בבית המדרש", "שיש להפוך את הבית למקום מפגש ללימוד תורה", "שיש להתרחק מהחכמים ולשמור על פרטיות"],
                    correct: 1
                },
                {
                    question: "מה פירוש \"והוי מתאבק בעפר רגליהם\"?",
                    answers: ["לנקות את בית המדרש", "להתקרב לחכמים ולשמש אותם", "לעשות תשובה ולהתנהג בענווה"],
                    correct: 1
                },
                {
                    question: "מה הכוונה ב\"והוי שותה בצמא את דבריהם\"?",
                    answers: ["לשתות מים בשעת הלימוד", "ללמוד מהחכמים בשקיקה ובצימאון", "לקבל כל דבר שהחכמים אומרים ללא ערעור"],
                    correct: 1
                }
            ],
            // משנה ה'
            [
                {
                    question: "מי אמר \"יהי ביתך פתוח לרוחה\"?",
                    answers: ["יוסי בן יועזר", "יוסי בן יוחנן", "אנטיגנוס איש סוכו"],
                    correct: 1
                },
                {
                    question: "מה פירוש \"יהי ביתך פתוח לרוחה\"?",
                    answers: ["לאוורר את הבית", "להכניס אורחים ברוחב לב", "לבנות בית גדול ומרווח"],
                    correct: 1
                },
                {
                    question: "מה הכוונה ב\"ויהיו עניים בני ביתך\"?",
                    answers: ["לתת צדקה לעניים", "להתייחס לעניים כאל בני משפחה", "להעסיק עניים בעבודות בית"],
                    correct: 1
                },
                {
                    question: "על מי נאמר \"ואל תרבה שיחה עם האשה\"?",
                    answers: ["רק על אשת חברו", "באשתו אמרו, קל וחומר באשת חברו", "רק על נשים זרות"],
                    correct: 1
                },
                {
                    question: "מה התוצאה של ריבוי שיחה עם האשה לפי חכמים?",
                    answers: ["גורם רעה לעצמו, בוטל מדברי תורה וסופו יורש גיהנום", "מביא אהבה ושלום בית למשפחה", "מפריע לריכוז בלימוד התורה בלבד"],
                    correct: 0
                }
            ]
        ];

        // פונקציה לבחירת משנה
        function selectMishna(mishnaNumber) {
            currentMishna = mishnaNumber;
            currentQuestionIndex = 0;
            questions = allQuestions[mishnaNumber - 1];
            
            // הצג את טקסט המשנה
            document.getElementById('mishna-text').textContent = mishnayot[mishnaNumber - 1];
            
            // הסתר את מסך התפריט והצג את מסך השאלות
            document.getElementById('menu-screen').style.display = 'none';
            document.getElementById('question-screen').style.display = 'block';
            
            // הצג את השאלה הראשונה
            showQuestion();
        }
        
        // פונקציה להצגת שאלה
        function showQuestion() {
            // נקה פידבק
            document.getElementById('feedback').textContent = '';
            
            if (currentQuestionIndex < questions.length) {
                const question = questions[currentQuestionIndex];
                
                // הצג את השאלה
                document.getElementById('question').textContent = question.question;
                
                // הצג את התשובות האפשריות
                const answersContainer = document.getElementById('answers');
                answersContainer.innerHTML = '';
                
                question.answers.forEach((answer, index) => {
                    const button = document.createElement('button');
                    button.className = 'answer-btn';
                    button.textContent = answer;
                    button.onclick = () => checkAnswer(index);
                    answersContainer.appendChild(button);
                });
            } else {
                // חזור למסך הבחירה אחרי כל השאלות
                setTimeout(() => {
                    document.getElementById('menu-screen').style.display = 'block';
                    document.getElementById('question-screen').style.display = 'none';
                }, 2000);
            }
        }
        
        // פונקציה לבדיקת התשובה
        function checkAnswer(answerIndex) {
            const currentQuestion = questions[currentQuestionIndex];
            const feedbackElement = document.getElementById('feedback');
            const answerButtons = document.querySelectorAll('.answer-btn');
            
            // השבת את כל הכפתורים
            answerButtons.forEach(button => {
                button.disabled = true;
            });
            
            // בדוק אם התשובה נכונה
            if (answerIndex === currentQuestion.correct) {
                feedbackElement.textContent = '😊 נכון מאוד!';
                score += 5;
                document.getElementById('score').textContent = 'ניקוד: ' + score;
            } else {
                feedbackElement.textContent = '😔 לא נכון. התשובה הנכונה היא: ' + currentQuestion.answers[currentQuestion.correct];
            }
            
            // עבור לשאלה הבאה אחרי 4 שניות
            currentQuestionIndex++;
            setTimeout(showQuestion, 4000);
        }
    </script>
</body>
</html>