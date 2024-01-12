/*
 * To change this license header, choose License Headers in Project Properties.
 * To change this template file, choose Tools | Templates
 * and open the template in the editor.
 */
package javaapplication38;

import java.util.Scanner;

/**
 *
 * @author MICHAE LOU LIM
 */
public class JavaApplication38 {

    /**5
     * @param args the command line arguments
     */
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        // Input the elevation for point A
        System.out.print("Enter the elevation for point A (m): ");
        double elevationPointA = scanner.nextDouble();

        // Input the elevation for point B
        System.out.print("Enter the elevation for point B (m): ");
        double elevationPointB = scanner.nextDouble();

        // Calculate the height of instrument to point A (assuming point A is +100)
        double hiPointA = elevationPointA + 100.0;

        // Calculate the height of instrument to point B (assuming point B is minuses the result of hiPointA)
        double hiPointB = (-elevationPointB) + hiPointA;

        // Calculate the difference in levels (Point A - Point B)
        double differenceInLevels = elevationPointA - elevationPointB;

        // Display the results
        System.out.println("(H.I.) to point A: " + hiPointA + " m");
        System.out.println("Elevation of  B: " + hiPointB + " m");
        System.out.println("Difference level between point A and B: " + differenceInLevels + " m");

        // Close the scanner
        scanner.close();
    }
}
