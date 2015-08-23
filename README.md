# LightReflex
<h1>简介</h1>
<p>随着鼠标的移动，阴影方向随着变化。当然还是<a href="https://github.com/Indamix/real-shadow">Real Shadow</a>插件很赞啦！</p>
<h2>收获</h2>
<p>感觉最大收获是遍历模块数组，然后在其中添加属性。这样就完全避免了像抹布条似的列举每一个模块数组，
像这样：</p>
			var a = ['rect', 'circle', 'round', 'ur', 'll'],
			    c = ['', 'r', 'g', 'b', 'rgb', 'rg', 'gb', 'br'],
				columns =6, rows = 6,
				s = '', i, j;
			
			for(i = 0; i<columns; ++i) {
				s += '<p>';
				for(j = 0; j<rows; ++j) {
					s += '<span rel="' + c[(i * columns + j) % c.length] + '" class="realshadow block ' +a[(i * columns + j) % a.length] + ' c' + c[(i * columns + j) % c.length] + '"></span>';
				}
				
				s += '</p>';
			}
