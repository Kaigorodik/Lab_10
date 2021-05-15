package task1.example2;

import java.io.ByteArrayInputStream;
import java.io.FileInputStream;
import java.io.IOException;
import java.io.InputStream;
import java.net.URL;

public class Primer1 {
    public static void readAllByByte(InputStream in) throws IOException {
        while (true) {
            int oneByte = in.read();
            if (oneByte != -1) {
                System.out.print((char) oneByte);
            } else {
                System.out.print("\n" + "end");
                break;
            }
        }
    }

    public static void main(String[] args) {
        try {
            InputStream inputFile = new FileInputStream("lab10\\src\\task1\\example2\\Новый текстовый документ.txt");
            readAllByByte(inputFile);
            System.out.print("\n\n\n");
            inputFile.close();

            InputStream inputUrl = new URL("https://www.google.ru/").openStream();
            readAllByByte(inputUrl);
            System.out.print("\n\n\n");
            inputUrl.close();

            InputStream inputArr = new ByteArrayInputStream(new byte[]{1,2,4,1,4,7,1});
            readAllByByte(inputArr);
            System.out.print("\n\n\n");
            inputArr.close();

        } catch (IOException e) {
            System.out.println("Ошибка: " + e);
        }
    }
}
