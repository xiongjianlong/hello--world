# hello--world
the fisrt test
<script type="text/javascript">
			var oSearch = document.getElementById("search");
			var searchReslut = document.getElementById("searchReslut");
			oSearch.onkeyup = function(){
				var val = this.value;
				if(val){
					var oScript = document.createElement("script");
					oScript.src = "https://sp0.baidu.com/5a1Fazu8AA54nxGko9WTAnF6hhy/su?wd="+val+"&cb=fly";
					document.body.appendChild(oScript);
					oScript.onload = function (){
						this.parentNode.removeChild(this);
					}
				}else{
					searchReslut.innerHTML = '';
				};
			};
			oSearch.onfocus = oSearch.onkeyup;
			oSearch.onblur = function(){
				var oLi = document.getElementsByTagName("li");
				for (var i = 0; i<oLi.length;i++) {
					oLi[i].className = '_display';
				}
			}
			function fly (myjonp){
				var s = myjonp.s;
				searchReslut.innerHTML = '';
				for (var i =0; i<s.length;i++) {
					searchReslut.innerHTML += '<li><a href="##">'+s[i]+'</a></li>'
				}
			}
		</script>
