<html lang="ja">
  <head>
    <meta charset="UTF-8">
  </head>
  <body>
    <div align="center">
      <h1>Search Chords Mode</h1>
      <hr size="2" width="90%" align="center" color="blue">
      <h2>コードから単音を検索する</h2>
      <p><img src="KeyBoard.gif" alt="キーボード"></p>
      <p>
        <select name="root">
          <option value="C">C</option>
          <option value="C#">C#</option>
          <option value="D">D</option>
          <option value="D#">D#</option>
          <option value="E">E</option>
          <option value="F">F</option>
          <option value="F#">F#</option>
          <option value="G">G</option>
          <option value="G#">G#</option>
          <option value="A">A</option>
          <option value="A#">A#</option>
          <option value="B">B</option>
        </select>
        <select name="3rd">
          <option value="(M)">(M)</option>
          <option value="m">m</option>
          <option value="sus2">sus2</option>
          <option value="sus4">sus4</option>
          <option value="(omit3)">(omit3)</option>
        </select>
        <select name="5th">
          <option value="(P5)">(P5)</option>
          <option value="+5">+5</option>
          <option value="-5">-5</option>
          <option value="(omit5)">(omit5)</option>
        </select>
        <select name="7th">
          <option value="(NonTension)">(NonTension)</option>
          <option value="6">6</option>
          <option value="6M7">6M7</option>
          <option value="7">7</option>
          <option value="M7">M7</option>
        </select>
        <form name="chbox">
          <input type="checkbox" value="add9">add9<br>
          <input type="checkbox" value="add11">add11<br>
          <input type="checkbox" value="add13">add13<br>
          <input type="button" value="確認" onclick="boxCheck()">
        </form>
        <script>
          function boxCheck(){
            var str="";                                     //チェックされた項目を記録する変数
            for( i=0; i<3; i++ ){                           //for文でチェックボックスを１つずつ確認
              if( document.chbox.elements[i].checked ){     //チェックされているか確認する
                if( str != "" ) str=str+",";                //変数strが空でない時、区切りのコンマを入れる
                str=str+document.chbox.elements[i].value;   //チェックボックスのvalue値を変数strに入れる
              }
            }
            if( str=="" ){  //strが空の時、警告を出す
              alert( "(NonTension)が選択されました。" );
            }else{
              alert( str + "が選択されました。" );
            }
          }
        </script>
      </p>
      <hr size="2" width="80%" align="center" color="orange">
      <h6 align="right">※この検索システムは、個人的にまとめたため、信頼度は低いです。あらかじめご了承ください。</h6>
    </div>
    <div align="right">
      <a href="https://takajo-soft08.github.io/SearchChord/">
         Back To Home
      </a>
    </div>
  </body>
</html>
