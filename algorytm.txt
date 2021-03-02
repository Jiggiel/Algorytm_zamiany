<script>
var n = prompt("Podaj liczbę");
var liczby = [["","I","II","III","IV","V","VI","VII","VIII","IX"],
             ["","X","XX","XXX", "XL", "L", "LX", "LXX", "LXXX", "XC"],
             ["","C","CC","CCC","CD","D","DC","DCC","DCCC","CM"]];

function convert(num) {
  var numer = "";
  var znaki = num.toString().split('').reverse();
  for (var i=0; i < znaki.length; i++){
    numer = liczby[i][parseInt(znaki[i])] + numer;
  }
  return numer;
}
if (n>=1&&n<1000)
	document.write(convert(n));
else
	document.write("Błąd, można tylko przekonwertować liczbę z przedziału od 1 do 999")
</script>