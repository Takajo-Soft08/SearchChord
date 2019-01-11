<html lang="ja">
  <head>
    <meta charset="UTF-8">
  </head>
  <body>
    <div align="center">
      <h1>Search Chords Mode</h1>
      <hr size="2" width="90%" align="center" color="blue">
      <h2>単音からコードを検索する</h2>
      <form name="chbox">
        <p>コードの構成音を選んでください。</p>
        <input type="checkbox" value="C">C <br>
        <input type="checkbox" value="C#">C#<br>
        <input type="checkbox" value="D">D <br>
        <input type="checkbox" value="D#">D#<br>
        <input type="checkbox" value="E">E <br>
        <input type="checkbox" value="F">F <br>
        <input type="checkbox" value="F#">F#<br>
        <input type="checkbox" value="G">G <br>
        <input type="checkbox" value="G#">G#<br>
        <input type="checkbox" value="A">A <br>
        <input type="checkbox" value="A#">A#<br>
        <input type="checkbox" value="B">B <br>
        <input type="button" value="確認" onclick="boxCheck()">
      </form>
      <script>
        function boxCheck(){
          var str="";                                     //チェックされた項目を記録する変数
          for( i=0; i<12; i++ ){                           //for文でチェックボックスを１つずつ確認
            if( document.chbox.elements[i].checked ){     //チェックされているか確認する
              if( str != "" ) str=str+",";                //変数strが空でない時、区切りのコンマを入れる
              str=str+document.chbox.elements[i].value;   //チェックボックスのvalue値を変数strに入れる
            }
          }
          if( str=="" ){  //strが空の時、警告を出す
            alert( "デフォルトとして(C,E,G,)が選択されました。" );
          }else{
            alert( str + "が選択されました。" );
          }
        }
      </script>      
      <hr size="2" width="80%" align="center" color="orange">
      <h6 align="right">※この検索システムは、個人的にまとめたため、信頼度は低いです。あらかじめご了承ください。</h6>
    </div>
    <div align="right">
      <a href="https://takajo-soft08.github.io/SearchChord/" align="left">
        Back To Home
      </a>
    </div>
  </body>
</html>
