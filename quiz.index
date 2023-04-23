const quiz = [
  {
    question: "世界で一番多い血液型は何型でしょうか？",
    answers: [  
    "A型",
    "B型",
    "O型",
    "AB型"
  ],
  correct: "O型"
  },
  {   
    question: "うわばみとはどんな人のことでしょうか？",
    answers: [  
    "大食いの人",
    "酒をたくさん飲む人",
    "よく寝る人",
    "よく喋る人"
],
correct: "酒をたくさん飲む人" },
  {
    question: "東京ディズニーリゾートには全部でいくつの隠れミッキーがあるでしょうか？",
    answers: [  
    "34個",
    "77個",
    "365個",
    "総数は分からない"
],
correct: "総数は分からない"}
];
const quizLength = quiz.length;
let quizIndex = 0;
let score = 0;

const $button = document.getElementsByTagName("button");
let buttonLength =$button.length

// クイズの問題分、選択肢を定義
const setupQuiz = () =>{
  document.getElementById("js-question").textContent  = quiz[quizIndex].question;
  let buttonIndex =0;
  while(buttonIndex < buttonLength){
    $button[buttonIndex].textContent = quiz[quizIndex].answers[buttonIndex]
    buttonIndex++;
  }
}
setupQuiz();


const clickHandler =(e) => {
  if(quiz[quizIndex].correct === e.target.textContent){
    window.alert("正解!");
    score++;
  }else{
    window.alert("不正解!");
  }

  quizIndex++;


if(quizIndex < quizLength){
  // 問題がまだあればこちらを実行
  setupQuiz();
} else {
  // 問題がもうなければこちらを実行
  window.alert("終了！あなたの正解数は" + quizLength + "問中" + score + "問です！");
  if(quizLength === score) {
    window.alert("すごい！！全問正解！！");
  } else if (score === quizLength - 1) {
    window.alert("あと少し！！")
  }else{
    window.alert("残念！！")
  }
  

}
};




// ボタンをクリックしたら正誤判定
let handlerIndex = 0;
while (handlerIndex < buttonLength) {
  $button [handlerIndex].addEventListener("click",(e) => {
    clickHandler(e);
  });
  handlerIndex++;
}
