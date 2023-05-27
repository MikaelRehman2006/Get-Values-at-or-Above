# Finds every value in a specific array that is equal or above another certain value

	public class getValuesEqualOrAbove
	{
		public static void main(String[] args)
		    {

				int[] myArray = {3, 2 ,1 ,4, 5, 6};

				System.out.println(countNumberBelow(myArray, 3 ));
		    }


			 public static int countNumberBelow(int[] array, int num) {
				int count = 0;
				for (int i = 0; i < array.length; i++) {
				    if (array[i] < num) {
					count++;
				    }
				}
				return count;
			    }


			 public static int[] getValuesAtOrAbove(int[] array, int threshold) 
			 {
				int count = countNumberBelow(array, threshold);                    // I made a method called countNumberBelow and used it in this method
				int[] result = new int[array.length - count];
				int index = 0;
				for (int i = 0; i < array.length; i++) 
				{
				    if (array[i] >= threshold) 
				    {
					result[index] = array[i];
					index++;
				    }
				}
				return result;
			    }
		}


    
