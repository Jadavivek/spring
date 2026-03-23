<dependency>
		    <groupId>org.apache.tomcat.embed</groupId>
		    <artifactId>tomcat-embed-jasper</artifactId>
		</dependency>		
 package com.seed.controller;
 
import org.springframework.stereotype.Controller;
import org.springframework.web.bind.annotation.GetMapping;
import org.springframework.web.bind.annotation.PostMapping;
import org.springframework.web.bind.annotation.RequestParam;
 
import jakarta.servlet.http.HttpSession;
 
@Controller
public class LoginController {
   
	@GetMapping("/login")
	public String loginPage() {
		return "login";
	}
	
	@PostMapping("/login")
	public String login(@RequestParam String username,@RequestParam String password,HttpSession session )
	{
		if(username.equals("admin") && password.equals("123")) {
			session.setAttribute("user", username);
			return "redirect:/";
		}
		
		return "login";  //invalid login
	}
	
 
}
 
