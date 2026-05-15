<!DOCTYPE html>
<html lang="ja">
<head>
    <meta charset="UTF-8">
    <title>シャボン玉マウスエフェクト</title>
    <style>
        body {
            margin: 0;
            overflow: hidden;
            /* シャボン玉が見えやすいように、少し明るい背景にするか、
               青空のようなグラデーションにするのがおすすめです */
            background: linear-gradient(to bottom, #87CEEB, #E0F7FA);
        }
        canvas {
            display: block;
        }
    </style>
</head>
<body>

<canvas id="particleCanvas"></canvas>

<script>
    const canvas = document.getElementById('particleCanvas');
    const ctx = canvas.getContext('2d');

    // 画面サイズに合わせてキャンバスをリサイズ
    function resizeCanvas() {
        canvas.width = window.innerWidth;
        canvas.height = window.innerHeight;
    }
    window.addEventListener('resize', resizeCanvas);
    resizeCanvas();

    const particles = [];

    // シャボン玉クラス
    class Bubble {
        constructor(x, y) {
            this.x = x;
            this.y = y;
            // 初期サイズを少し大きく
            this.size = Math.random() * 15 + 5; 
            // 横移動はランダム、縦移動は上向きに
            this.speedX = Math.random() * 2 - 1;
            this.speedY = Math.random() * -2 - 1; // 上向き (-1 to -3)
            // 虹色の輪郭用の色相
            this.hue = Math.random() * 360;
            this.opacity = 1;
            this.wobble = Math.random() * Math.PI * 2; // ふらふらさせるための位相
        }

        update() {
            this.x += this.speedX + Math.sin(this.wobble) * 0.5; // ふらふらさせる
            this.y += this.speedY;
            this.wobble += 0.05; // ふらふらの位相を進める

            // 徐々に透明にする（小さくはしない）
            this.opacity -= 0.005;
            
            // 色相を変化させる
            this.hue += 1;
        }

        draw() {
            ctx.globalAlpha = this.opacity;
            // 塗りつぶしではなく、線で描画
            ctx.strokeStyle = `hsl(${this.hue}, 70%, 80%)`; // 虹色の線
            ctx.lineWidth = 1.5;
            ctx.beginPath();
            ctx.arc(this.x, this.y, this.size, 0, Math.PI * 2);
            ctx.stroke();

            // キラキラ感を少し残す（ハイライト）
            ctx.fillStyle = 'rgba(255, 255, 255, 0.3)';
            ctx.beginPath();
            ctx.arc(this.x - this.size * 0.3, this.y - this.size * 0.3, this.size * 0.2, 0, Math.PI * 2);
            ctx.fill();

            // ぼかしを少しだけ入れる
            ctx.shadowBlur = 5;
            ctx.shadowColor = `hsl(${this.hue}, 70%, 80%)`;
        }
    }

    function handleParticles() {
        for (let i = 0; i < particles.length; i++) {
            particles[i].update();
            particles[i].draw();

            // 透明になったシャボン玉を削除
            if (particles[i].opacity <= 0) {
                particles.splice(i, 1);
                i--;
            }
        }
    }

    // マウスが動いた時の処理
    window.addEventListener('mousemove', function(e) {
        // 一度の移動で生成する数を減らす（シャボン玉っぽく）
        if (Math.random() > 0.5) { // 常に生成するのではなく、間引く
            particles.push(new Bubble(e.x, e.y));
        }
    });

    // タッチ操作（スマホ）にも対応
    window.addEventListener('touchmove', function(e) {
        if (Math.random() > 0.5) {
            particles.push(new Bubble(e.touches[0].clientX, e.touches[0].clientY));
        }
    });

    function animate() {
        // 画面をクリア（残像効果なし）
        ctx.clearRect(0, 0, canvas.width, canvas.height);
        
        handleParticles();
        requestAnimationFrame(animate);
    }

    animate();
</script>

</body>
</html>
