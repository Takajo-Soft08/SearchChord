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
     <script>
      function entry(){
       <!--
        var table=document.getElementById('move');
        var tr=table.rows[0];
        var td=tr.cells[1];
-->
        const Key=document.selector.Key;
        const numKey=document.selector.Key.selectedIndex;
        const Maj=document.selector.Maj;
        const numMaj=document.selector.Maj.selectedIndex;
        const strMaj=document.selector.Maj.options[numMaj].value;
        const strMajInv=document.selector.Maj.options[1-numMaj].value;       

        const strKeyI  =document.selector.Key.options[numKey].value;
        const strKeyPl;
        if(numMaj==0) strKeyPl = document.selector.Key.options[(numKey+9)%12].value;
        if(numMaj==1) strKeyPl = document.selector.Key.options[(numKey+3)%12].value;
        const strKeyD  =document.selector.Key.options[(numKey+7)%12].value;
        const strKeySD =document.selector.Key.options[(numKey+5)%12].value;
        const strKeyDm =document.selector.Key.options[(numKey+4)%12].value;
        const strKeySDm=document.selector.Key.options[(numKey+2)%12].value;

        document.getElementById("span1").textContent= strKeyI  +" "+ strMaj;
        document.getElementById("span2").textContent= strKeyI  +" "+ strMajInv;
        document.getElementById("span3").textContent= strKeyPl +" "+ strMajInv;
        document.getElementById("span4").textContent= strKeyD  +" "+ strMaj;
        document.getElementById("span5").textContent= strKeySD +" "+ strMaj;
        document.getElementById("span6").textContent= strKeyDm +" "+ strMajInv;
        document.getElementById("span7").textContent= strKeySDm+" "+ strMajInv;
      }
     </script>
     <input type="button" value="Enter" onclick="entry()">
      <h2>実行結果</h2>
      <table id="move">
        <tr>
          <td>基調、主調(Key Note)</td>
          <td><span id="span1"></span></td>
        </tr>
        <tr>
          <td>同主調(Parallel Key)</td>
          <td><span id="span2"></span></td>
        </tr>
        <tr>
          <td>平行調(Relative Key)</td>
          <td><span id="span3"></span></td>
        </tr>
        <tr>
          <td>属調(Dominant Key)</td>
          <td><span id="span4"></span></td>
        </tr>
        <tr>
          <td>下属調(Subdominant Key)</td>
          <td><span id="span5"></span></td>
        </tr>
        <tr>
          <td>属調平行調</td>
          <td><span id="span6"></span></td>
        </tr>
        <tr>
          <td>下属調平行調</td>
          <td><span id="span7"></span></td>
        </tr>
      </table>      
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

