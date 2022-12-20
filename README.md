# Comp-7.8

public class Coin implements Lockable{
           
	   private final int HEADS =0;
	   private final int TAILS =1;
	   private final int LOCKED = 2;
	   private int key = 0;
	   private int face;
	   
           
           public Coin()
	   {
	   flip();
	   }
	  
           @Override

	   public void setKey(int key) {
	   this.key = key;
	   }

	   @Override

	   public void lock(int key) {
	   if(this.key == key)
	   face = LOCKED;
	   }

	   @Override

	   public void unlock(int key) {
	   if(this.key == key)
	   face = -1;
	   }

	   @Override

	   public boolean locked() {
	   if(face == LOCKED)
	   return true;
	   else return false;
	   }


	   public void flip(){
           if(face != LOCKED)
	   face = (int)(Math.random()*2);
	   }

	   public boolean isHeads(){
	   return(face == HEADS);
	   }

	   public String toString(){
	   String faceName;
	   if(face==HEADS)
                faceName = "Heads";
	   else if(face == TAILS)
                faceName = "Tails";
	   else
                faceName = "LOCKED";
	   return faceName;
	   }

}
