import java.io.BufferedReader;
import java.io.FileReader;
import java.io.IOException;

/**
 * FileReaderExample
 * 
 * This class demonstrates how to read a text file in Java.
 * The method readFile prints each line of the file to the console.
 * 
 * Author: Santiago Fuentes Lopez
 */

public class FileReaderExample {

    /**
     * Reads a text file and prints its content line by line.
     *
     * @param filePath the path of the file to read
     */
    public static void readFile(String filePath) {

        try {

            BufferedReader reader = new BufferedReader(new FileReader(filePath));

            String line;

            // Read the file line by line
            while ((line = reader.readLine()) != null) {

                System.out.println(line);

            }

            reader.close();

        } catch (IOException e) {

            System.out.println("An error occurred while reading the file.");
            e.printStackTrace();

        }
    }

    /**
     * Main method used to demonstrate the functionality of readFile().
     */
    public static void main(String[] args) {

        String filePath = "example.txt";

        System.out.println("Reading file content:\n");

        readFile(filePath);

    }
}
