<!DOCTYPE html>
<html>
<head>
    <title>E-Governance Portal</title>
</head>
<body style="font-family: Arial; padding:20px;">

<h1>E-Governance Portal</h1>
<p>Welcome to the digital service portal for citizens.</p>

<h2>Available Services</h2>
<ul>
    <li>Aadhaar Services</li>
    <li>Pan Card Application</li>
    <li>Voter ID Registration</li>
    <li>Birth & Death Certificates</li>
    <li>Government Schemes (PMAY, PMJDY, etc.)</li>
</ul>

<h2>Submit Your Query</h2>
<form method="post" action="http://localhost:8080/Egov">
    <label>Name:</label><br>
    <input type="text" name="name"><br><br>

    <label>Service Needed:</label><br>
    <input type="text" name="service"><br><br>

    <label>Message:</label><br>
    <textarea name="message"></textarea><br><br>

    <button type="submit">Submit</button>
</form>

</body>
</html># IT-proiect
CREATE DATABASE egov_portal;

USE egov_portal;

CREATE TABLE citizen_queries (
    id INT AUTO_INCREMENT PRIMARY KEY,
    name VARCHAR(50),
    service VARCHAR(100),
    message TEXT,
    submitted_on TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);
import java.util.Scanner;

public class Egov {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        System.out.println("=== E-GOVERNANCE QUERY SYSTEM ===");

        System.out.print("Enter your name: ");
        String name = sc.nextLine();

        System.out.print("Enter required service: ");
        String service = sc.nextLine();

        System.out.print("Enter your message: ");
        String message = sc.nextLine();

        System.out.println("\n----- QUERY RECEIVED -----");
        System.out.println("Name       : " + name);
        System.out.println("Service    : " + service);
        System.out.println("Message    : " + message);
        System.out.println("---------------------------");

        System.out.println("\nYour request has been submitted successfully!");
    }
}

