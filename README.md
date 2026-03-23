package com.seed.model;
 
import jakarta.persistence.*;

import jakarta.validation.constraints.*;
 
@Entity

public class Student {
 
    @Id

    @GeneratedValue(strategy = GenerationType.IDENTITY)

    private int id;
 
    @NotBlank(message="Name required")

    private String name;
 
    @Email

    private String email;
 
    private String course;
 
    @Lob  // 🔥 important for large data

    @Column(columnDefinition = "LONGBLOB")

    private byte[] image;
 
	public int getId() {

		return id;

	}
 
	public void setId(int id) {

		this.id = id;

	}
 
	public String getName() {

		return name;

	}
 
	public void setName(String name) {

		this.name = name;

	}
 
	public String getEmail() {

		return email;

	}
 
	public void setEmail(String email) {

		this.email = email;

	}
 
	public String getCourse() {

		return course;

	}
 
	public void setCourse(String course) {

		this.course = course;

	}
 
	public byte[] getImage() {

		return image;

	}
 
	public void setImage(byte[] image) {

		this.image = image;

	}
 
  

}
 
