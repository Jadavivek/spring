package com.seed;
 
import org.springframework.stereotype.Controller;
import org.springframework.web.bind.annotation.RequestMapping;
 
@Controller
public class HomeController {
	
//	@RequestMapping("home")
//    public void home() {
//    	System.out.println("hi hello.....");
//    }
	
	@RequestMapping("home")
    public String home() {
    	return "home.jsp";
    }
	
	//remove extention when we are reading file from any specific folder
	@RequestMapping("/home2")
    public String home2() {
    	return "home2";   
    }
}
 
 
