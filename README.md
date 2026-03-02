import java.util.Scanner;

public class OnlineQuizApp {

public static void main(String[] args) {

    Scanner sc = new Scanner(System.in);

    String questions[] = {
            "1. Which language is used for Java programming?",
            "2. Which keyword is used to inherit a class in Java?",
            "3. Which method is the entry point of Java program?",
            "4. Which concept allows same method name with different parameters?",
            "5. Which package contains Scanner class?"
    };

    String options[][] = {
            {"A. Python", "B. Java", "C. C++", "D. HTML"},
            {"A. implement", "B. extends", "C. inherit", "D. super"},
            {"A. start()", "B. run()", "C. main()", "D. init()"},
            {"A. Encapsulation", "B. Inheritance", "C. Polymorphism", "D. Abstraction"},
            {"A. java.io", "B. java.lang", "C. java.util", "D. java.sql"}
    };

    char answers[] = {'B', 'B', 'C', 'C', 'C'};

    int score = 0;

    for (int i = 0; i < questions.length; i++) {

        System.out.println(questions[i]);

        for (int j = 0; j < options[i].length; j++) {
            System.out.println(options[i][j]);
        }

        System.out.print("Enter your answer: ");
        char userAnswer = sc.next().toUpperCase().charAt(0);

        if (userAnswer == answers[i]) {
            score++;
        }

        System.out.println();
    }

    System.out.println("===== QUIZ RESULT =====");
    System.out.println("Total Score: " + score + "/" + questions.length);

    sc.close();
}
}
