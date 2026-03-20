package com.seed.controller;
 
import org.springframework.stereotype.Controller;

import org.springframework.ui.Model;

import org.springframework.web.bind.annotation.RequestMapping;

import org.springframework.web.bind.annotation.RequestParam;
 
@Controller

public class StudentController {

    @RequestMapping("/form")

     public String loadForm()

     {

    	 return "form";

     }

    @RequestMapping("/result")

    public String handleForm(@RequestParam("name") String name,

    		                      @RequestParam("email") String email,

    		                      @RequestParam("course") String course,Model model)

    {

    	model.addAttribute("name",name);

    	model.addAttribute("email",email);

    	model.addAttribute("course",course);

   	    return "result";

    }


}
 
