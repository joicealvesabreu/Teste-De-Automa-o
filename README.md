package TestPrimeiro;

import java.util.concurrent.TimeUnit;

import org.junit.Test;
import org.openqa.selenium.By;
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.WebElement;
import org.openqa.selenium.chrome.ChromeDriver;

public class TesteCadrastaFacebook {
	@Test
	
	public void Cadastranofacebook() {
		
		WebDriver driver =  new  ChromeDriver();
		driver.manage().timeouts().implicitlyWait(5, TimeUnit.SECONDS);
		
		driver.get("https://pt-br.facebook.com");
		driver.findElement(By.id("u_0_m")).sendKeys("JOICE");
		driver.findElement(By.id("u_0_o")).sendKeys("Natalice");
		
		driver.findElement(By.id("u_0_r")).sendKeys("joice@gmail.com");
		
		driver.findElement(By.id("u_0_u")).sendKeys("joice@gmail.com");
		driver.findElement(By.id("u_0_w")).sendKeys("1234");
		
		
		WebElement botaonascimento = driver.findElement(By.id("day"));
		botaonascimento.sendKeys("24");
		WebElement botaonascimento1 = driver.findElement(By.id("month"));
		botaonascimento1.sendKeys("11");
		WebElement botaonascimento2 = driver.findElement(By.id("year"));
		botaonascimento2.sendKeys("1990");
	
		WebElement sexofer= driver.findElement(By.id("u_0_7"));
		sexofer.isSelected();
		
		driver.findElement(By.id("u_0_13")).click();
		driver.close();
