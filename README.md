# TowerSiege-1
ellipse(ball.position.x,ball.position.y,20);
  display(){
    if(this.body.speed < 3){
      super.display();
    }
    else {
      World.remove(world, this.body);
      push();
      this.visibility = this.visibility - 5;
      //We don't want to change the colour
      tint(255, this.visibility);
      image(this.image, this.body.position.x, this.body.position.y, 50, 50);
      pop();
    }
  }

};