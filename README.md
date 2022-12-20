# Comp-7.8

public class Comp78 {


	public static void main(String[] args) {   
		Coin myCoin = new Coin();
		int key = 0;
		
                myCoin.flip();
		System.out.println(myCoin);
		
                myCoin.setKey(key);
		myCoin.lock(key);
		myCoin.flip();
		
                System.out.println(myCoin);
		System.out.println(myCoin.locked());
		
                myCoin.unlock(key);
		myCoin.flip();
		System.out.println(myCoin);
	}
	
}
