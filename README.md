# volume_of_lack
google volume of lack
public class Main {
    public static void main(String[] args)
    {
       //
        // System.out.println("Hello world!");
         int[] height = new int[0];
        int trappedWater =0;
        int leftIndex=0;
        int RightIndex= height.length-1;
        int leftMax= 0;
        int RightMax = 0;
        while(leftIndex<RightIndex){
            if(height[leftIndex]<=height[RightIndex]){
                leftMax=Math.max(leftMax,height[leftIndex]);
                trappedWater+= Math.max(0,leftMax-height[leftIndex]);
                leftMax+=1;
            }else{
                RightMax=Math.max(RightMax,height[RightIndex]);
                trappedWater+= Math.max(0,RightMax-height[RightIndex]);
                RightIndex-=1;
            }
        }
    }
}
