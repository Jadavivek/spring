package com.seed.controller;
 
import com.seed.model.Student;

import org.springframework.stereotype.Controller;

import org.springframework.ui.Model;

import org.springframework.web.bind.annotation.ModelAttribute;

import org.springframework.web.bind.annotation.RequestMapping;
 
@Controller

public class StudentController {
 
    // Load form

    @RequestMapping("/form")

    public String loadForm(Model model) {

        model.addAttribute("student", new Student()); // important

        return "form";

    }
 
  

    //Handle form

    @RequestMapping("/result")

    public String handleForm(@ModelAttribute("student") Student student) {

    	System.out.println(student.getName());

    	System.out.println(student.getEmail());

    	System.out.println(student.getCourse());

        return "result";

    }

}
 
