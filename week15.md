計時器，時間到響鈴
```JAVA

import processing.sound.*;
SoundFile player; //外掛下載

void setup(){
size (400,200);
textSize(40);
player=new SoundFile(this,"bell.mp3"); //插入外掛+MP3檔
} //step03的程式
void draw(){ //每秒60次
  background(41,109,207);
  int s=second();
  text(9-s%10,100,100);
  
  if(9-s%10==0 && player.isPlaying()){ 
    player.play();
  }//if第0秒且沒播放就play
}
```
