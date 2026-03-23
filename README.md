package com.seed.service;

import java.util.List;

import org.springframework.beans.factory.annotation.Autowired;
import org.springframework.stereotype.Service;

import com.seed.entity.Student;
import com.seed.repository.StudentRepository;

@Service
public class StudentService {

    @Autowired
    private StudentRepository repo;

    // CREATE
    public Student saveStudent(Student student) {
        return repo.save(student);
    }

    // READ ALL
    public List<Student> getAllStudents() {
        return repo.findAll();
    }

    // READ BY ID
    public Student getStudentById(int id) {
        return repo.findById(id).orElse(null);
    }

    // UPDATE
    public Student updateStudent(Student student) {
        if (repo.existsById(student.getId())) {
            return repo.save(student);
        }
        return null; // or throw exception
    }

    // DELETE
    public String deleteStudent(int id) {
        if (repo.existsById(id)) {
            repo.deleteById(id);
            return "Student deleted successfully";
        }
        return "Student not found";
    }
}
