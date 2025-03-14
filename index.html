class CatVsDogGame extends Phaser.Scene {
    constructor() {
        super({ key: 'CatVsDogGame' });
    }

    preload() {
        this.load.image('background', 'path/to/background.png');
        this.load.image('cat', 'path/to/cat.png');
        this.load.image('dog', 'path/to/dog.png');
        this.load.image('rock', 'path/to/rock.png');
    }

    create() {
        this.add.image(400, 300, 'background');
        this.cat = this.physics.add.sprite(150, 450, 'cat').setScale(0.5);
        this.dog = this.physics.add.sprite(650, 450, 'dog').setScale(0.5);
        this.catHP = 100;
        this.dogHP = 100;
        this.isCatTurn = true;
        this.windPower = Phaser.Math.Between(-10, 10);
        this.windText = this.add.text(300, 50, `Wind: ${this.windPower}`, { fontSize: '20px', fill: '#fff' });
        this.hpText = this.add.text(300, 20, `Cat: ${this.catHP} HP | Dog: ${this.dogHP} HP`, { fontSize: '20px', fill: '#fff' });
        this.input.keyboard.on('keydown-SPACE', this.throwProjectile, this);
    }

    throwProjectile() {
        let attacker = this.isCatTurn ? this.cat : this.dog;
        let target = this.isCatTurn ? this.dog : this.cat;
        let xDirection = this.isCatTurn ? 1 : -1;
        let projectile = this.physics.add.sprite(attacker.x, attacker.y, 'rock');
        projectile.setVelocity(200 * xDirection + this.windPower * 10, -200);
        projectile.setGravityY(300);
        
        this.physics.add.collider(projectile, target, () => {
            projectile.destroy();
            let damage = Phaser.Math.Between(10, 30);
            if (this.isCatTurn) {
                this.dogHP -= damage;
            } else {
                this.catHP -= damage;
            }
            this.hpText.setText(`Cat: ${this.catHP} HP | Dog: ${this.dogHP} HP`);
            
            if (this.catHP <= 0 || this.dogHP <= 0) {
                this.add.text(300, 200, `${this.catHP <= 0 ? 'Dog Wins!' : 'Cat Wins!'}`, { fontSize: '30px', fill: '#ff0' });
                this.scene.pause();
            }
            
            this.isCatTurn = !this.isCatTurn;
            this.windPower = Phaser.Math.Between(-10, 10);
            this.windText.setText(`Wind: ${this.windPower}`);
        });
    }
}

const config = {
    type: Phaser.AUTO,
    width: 800,
    height: 600,
    physics: { default: 'arcade', arcade: { gravity: { y: 300 }, debug: false } },
    scene: CatVsDogGame
};

const game = new Phaser.Game(config);
