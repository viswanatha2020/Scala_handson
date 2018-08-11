# Scala_handson

class Test1 {
	public static void main(String args[]) {
		String st = "124455534";
		int hh = 0;
		int mm = 0;
		int maxmm = 0;
		int maxhh = 0;
		int a[] = new int[st.length()];

		for (int i = 0; i < st.length(); i++) {
			System.out.println(st.charAt(i));
			a[i] = Character.getNumericValue((st.charAt(i)));
		}

		for (int i = 0; i < st.length(); i++) {
			for (int j = 0; j < 4; j++) {
				if (a[i] * 10 + a[j] <= 24) {
					hh = a[i] * 10 + a[j];
					if (maxhh < a[i] * 10 + a[j]) {
						maxhh = a[i] * 10 + a[j];
					}
				}

				if (a[i] * 10 + a[j] <= 59) {
					mm = a[i] * 10 + a[j];
					if (maxmm < mm) {
						maxmm = (mm);
					}
				}
				System.out.println(hh + ":" + mm);

			}
		}
		System.out.println("MAX Time "+maxhh + ":" + maxmm);
	}

}
