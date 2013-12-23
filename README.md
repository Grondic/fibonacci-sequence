fibonacci-sequence

public class test {
	static int[] a = new int[100];
	
    public static int F(int N) {
        a[0] = 0; /* sets up first 2 digits in the sequence */
        a[1] = 1;
        if (N < 2) {
            return N;
        }
        a[N] = a[N - 1] + a[N - 2]; /* appends F num for next number in the list */
        return a[N]; /* should return the last number */
    }//this code i found it is used to find the Fibonacci sequence

    public static void main(String[] args) {
        for (int N = 0; N < 34; N++){
        if ( F(N) % 2 == 0) { /*this finds the even numbers of the sequence should i
        return it into an array and then total that array?*/
        int total = 0;	
        total += a[F(N)];
        System.out.println(total);
        	}
        }
    }
}
