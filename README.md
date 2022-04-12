# Jogo da Cobrinha
O jogo consiste em fazer a cobrinha pegar a maçã e fazer ela ficar o maior possivel.

## tecnologias utilzadas
- **HTML**: estrutura do site
- *_JS_*: funções do site


### Disponibilizado em 
[GitHubPage]( https://lgci12.github.io/jogo_x_lucas_erik/)


### Prints da tela

| ID | Primeira tela | Segunda tela | 
|----|---------------|--------------|
| 1  |inicio do jogo | jogo em andamento|
| 2  | ![inicio do jogo](https://user-images.githubusercontent.com/100213140/162988560-3649e5d1-a1cf-4b52-9065-e56ce321a403.png) | ![jogo em andamento](https://user-images.githubusercontent.com/100213140/162988857-5600b008-c431-4e6c-aedd-16e1baa734f6.png) |


#### função principal
```js: 
function game(){
    px += vx;
    py += vy;
    if (px <0) {
        px = qp-1;
    }
    if (px > qp-1) {
        px = 0;
    }
    if (py < 0) {
        py = qp-1;
    }
    if (py > qp-1) {
        py = 0;
    }

    ctx.fillStyle = "black";
    ctx.fillRect(0,0, area.width, area.height);

    ctx.fillStyle = "red";
    ctx.fillRect(ax*tp, ay*tp, tp,tp);

    ctx.fillStyle = "green";
    for (var i = 0; i < trail.length; i++) {
        ctx.fillRect(trail[i].x*tp, trail[i].y*tp, tp-1,tp-1);
        if (trail[i].x == px && trail[i].y == py)
        {
            vx = vy=0;
            tail =5;
        }
    }
```

#### comando git
para iniciar o projeto
```bash:
git init
```
