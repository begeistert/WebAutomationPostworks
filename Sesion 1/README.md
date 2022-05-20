import org.openqa.selenium.WebDriver;
import org.openqa.selenium.chrome.ChromeDriver;
import org.testng.annotations.AfterTest;
import org.testng.annotations.BeforeTest;
import org.testng.annotations.Test;

import java.time.Duration;

public class PruebaTestNG {

    @BeforeTest
    public void beforeTest() {
        System.setProperty("webdriver.chrome.driver", "src/test/resources/WebDriver/chromedriver.exe");
        WebDriver driver = new ChromeDriver();

        driver.manage().window().maximize();
        driver.get("https://bedu.org/");
        driver.manage().timeouts().implicitlyWait(Duration.ofSeconds(10));
        driver.close();
    }

    @Test
    public void test() {
    }

    @AfterTest
    public void afterTest() {
    }
}