# Programming-Task
## 가위바위보 게임 만들기 upgrade
    package scissors2;
    
    import java.util.Random;
    import java.util.Scanner;
    import java.lang.System;

    public class paper2 {
      public static void main(String[] args) {
        try {
          Thread.sleep(900);
          System.out.println("컴퓨터: 가위바위보를 하자.");
        } catch (InterruptedException e) {
            e.printStackTrace();
        }
		
		    try {
          Thread.sleep(950);
          System.out.println("가위바위보를 하시겠습니까?");
        } catch (InterruptedException e) {
            e.printStackTrace();
        }
		
		    try {
          Thread.sleep(950);
          System.out.println("Yes/No");
        } catch (InterruptedException e) {
            e.printStackTrace();
        }
        
		    Scanner scanner = new Scanner(System.in);
		    String value = scanner.nextLine();
		
		    boolean stop = false;
		
		    while (!stop) {
			
			    switch (value) {
			    case "yes" :
				    System.out.println("원하는 항목의 숫자를 입력하세요. 1.가위 2.바위 3.보");
				    break;
			    case "no" :
				    System.out.println("프로그램을 종료합니다.");
				    System.exit(0);
			    default:
				    System.out.println("다시 입력해주세요.");
			    }
			
			    String answer = scanner.next();
			
			    int data = 0;
			    Random random = new Random();
			    data = random.nextInt(3)+1;

			    switch (data) {
			    case 1:
				    System.out.println("컴퓨터는 가위");
				    if (answer.equals("1")) {
					    System.out.println("비겼어요!");
				    } else if (answer.equals("2")) {
					    System.out.println("이겼어요!");
				    } else {
					    System.out.println("졌어요ㅜㅜ");
				    }
				    break;
			
			    case 2:
				    System.out.println("컴퓨터는 바위");
				    if (answer.equals("2")) {
					    System.out.println("비겼어요!");
				    } else if (answer.equals("3")) {
					    System.out.println("이겼어요!");
				    } else {
					    System.out.println("졌어요ㅜㅜ");
				    }
				    break;
				
			    case 3:
				    System.out.println("컴퓨터는 보");
				    if (answer.equals("3")) {
					    System.out.println("비겼어요!");
			    	} else if (answer.equals("1")) {
			    		System.out.println("이겼어요!");
			    	} else {
			    		System.out.println("졌어요ㅜㅜ");
			    	}
			    	break;
					
			    default:
			    	System.out.println("다시 선택해주세요.");
				
			    }
			
			    try {
	            Thread.sleep(950);
	            System.out.println("다시 하시겠습니까? : ");
	        } catch (InterruptedException e) {
	            e.printStackTrace();
	        }
			
		    	String ctu = scanner.next();
			
		    	if (ctu.equals("네")){
			    	System.out.println("---------------------");
			    	continue;
			    }
			    if (ctu.equals("아니요")) {
			    	System.out.println("시스템을 종료합니다.");
			    	System.exit(0);
			    	break;
		    	}
	    	scanner.close();
	    	}
	    }
    }
