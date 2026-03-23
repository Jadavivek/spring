package com.seed.controller;
 
import org.springframework.beans.factory.annotation.Autowired;
import org.springframework.stereotype.Controller;
import org.springframework.ui.Model;
import org.springframework.web.bind.annotation.GetMapping;
 
import com.seed.repository.StudentRepository;
 
import jakarta.servlet.http.HttpSession;
 
@Controller
public class StudentController {
 
	@Autowired
	private StudentRepository repo;
	
   @GetMapping("/")
   public String list(HttpSession session, Model model)
   {
	   if(session.getAttribute("user")==null) {
		   return "redirect:/login";
	   }
	   
	   model.addAttribute("students",repo.findAll());
	   return "list";
	   
   }
}
 
