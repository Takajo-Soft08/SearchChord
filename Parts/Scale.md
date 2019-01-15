<html lang="ja">
  <head>
    <meta charset="UTF-8">
  </head>
  <body>
    <div align="center">
      <h1>Search Chords Mode</h1>
      <hr size="2" width="90%" align="center" color="blue">
      <h2>調性</h2>
      <p><img src="KeyBoard.gif" alt="キーボード"></p>
      <p>
      <form name="selector">
        <select name="Key">
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
        <select name="Maj">
          <option value="Major">Major</option>
          <option value="minor">minor</option>
        </select>
      </form>
      </p>
      <input type="button" value="Enter" onclick="entry()"/>
      <h2>実行結果</h2>
      <table id="move">
        <tr>
          <td>基調、主調(Key Note)</td>
          <td>C Major</td>
        </tr>
        <tr>
          <td>同主調(Parallel Key)</td>
          <td>C minor</td>
        </tr>
        <tr>
          <td>平行調(Relative Key)</td>
          <td>A minor</td>
        </tr>
        <tr>
          <td>属調(Dominant Key)</td>
          <td>G Major</td>
        </tr>
        <tr>
          <td>下属調(Subdominant Key)</td>
          <td>F Major</td>
        </tr>
          <td>属調平行調</td>
          <td>E minor</td>
        </tr>
        <tr>
          <td>下属調平行調</td>
          <td>D minor</td>
        </tr>
      </table>
      <script>
          function entry(){
            var table=document.getElementById('move');
            var tr=table.rows[0];
            var td=tr.cells[1];
            const Key=document.selector.Key;
            const numKey=document.selector.Key.selectedIndex;
            const strKey=document.selector.Key.options[numKey].value;
            const Maj=document.selector.Maj;
            const numMaj=document.selector.Maj.selectedIndex;
            const strMaj=document.selector.Maj.options[numMaj].value;    
            document.getElementById(table.rows[0].cells[1]).textContent= strKey+" "+strMaj;
<!--
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
                           var table=document.createElement( 'table' );
-->
          }
        </script>
      
      
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

