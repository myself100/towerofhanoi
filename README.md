# towerofhanoi

import java.util.Scanner;
public class towerofhanoi {

	public static void main(String[] args) {
		// TODO Auto-generated method stub
		Scanner s=new Scanner(System.in);
		int n=s.nextInt();                                                             ////no. of disk
		tower(n,'A','C','B');
	}
	public static void tower(int n,char from_rod,char to_rod,char aux_rod) {
		if(n==1) {
			System.out.println("Move disk 1 from_rod " + from_rod +" to_rod " + to_rod );               
			return;
		}
		tower(n-1,from_rod,aux_rod,to_rod);
		System.out.println("Move disk "+ n + " from_rod " +from_rod+ " to_rod " + to_rod);
		tower(n-1,aux_rod,to_rod,from_rod);
	}
}

output:: 
3
Move disk 1 from_rod A to_rod C
Move disk 2 from_rod A to_rod B
Move disk 1 from_rod C to_rod B
Move disk 3 from_rod A to_rod C
Move disk 1 from_rod B to_rod A
Move disk 2 from_rod B to_rod C
Move disk 1 from_rod A to_rod C
