# STUDENT-REGISTRATION-FORM-FOR-PLACEMENT
Student Registration Form for placement is a dynamic website where it is used by students and TPO for applying to jobs.


1.0	Project Overview:
The Student Registration for Placement will help student as well as placement cell. The students can get information's and notification from this easily. Students can also generate resume from Student placement system ,also they can upload all their documents ,through this software sitting at remote part of the country. TPO can all the job details in that which will be useful for the students and the students will also be notified by the TPO. So, the  students can apply job before the last date to apply. 

2.0	Product Features:
2.1	USER LOGIN: A set of credentials used to authenticate User in Placement system. The login form consists of Login id, Password to authenticate 

2.2	GENERATE RESUME: Generate resume is a feature that generates a resume after a student fills all the required details.


2.3	JOB PROFILE: Job profile will be used by TPO to add job details and it will be used by student to apply job.

2.4	MY PROFILE: My Profile will be used by students to add and edit their profile details.


2.5	DOCUMENTS: Students can add their  Documents according to the type.


3.0	Use Case:
3.1 Activity Diagram (Login):
 


Use Case ID: G4.1
	Use Case Name: Login
Description

	1.	USER can login into the placement management system with valid user credentials and after giving valid login credential they will move to their respective home page.
Actor	                    Student, Admin, TPO
Preconditions	1.	Student, Admin, TPO should have a valid account in the Placement system.
Post conditions	1.	Student, Admin, TPO will be logged in.
Frequency of Use	     100  per day
Normal Course of Events	1.	The Student, Admin, TPO will open the website  and it will direct to the login page.
2.	The Student  , Admin , TPO will provide the valid user id and password. 
3.	After Successful Login, Student  ,Admin, TPO will be navigated to the respected Home Page.
Alternative Courses	Nil
Associated Use case diagrams 		                               Agen

STUDENT

  
  ADMIN    
Exceptions
	1.	Without valid user ID and Password they cannot login to the system.
Special Requirements	  Nil 
Assumptions	They must have a account
Test Plan Outline	   Nil
Notes and Issues	   Nil

3.2 Activity Diagram (Create Account):
 
Use Case ID: G4.2
	Use Case Name: Create Account
Description

	If Student don’t have account they can create account.
Actor	       Student
Preconditions	1.	Student must not have existing account
Post conditions	1.	After creating account student will be redirected to login page.
2.	After giving valid user credential they will be able to move home page.
Frequency of Use	               100 per day
Normal Course of Events	1.	Student click on create account.
2.	System displays the create account page.
3.	After giving required details account will be created.
Alternative Courses	Nil
Associated Use case diagrams 	

    Student
Exceptions
	1.	If any of the field is left blank or in case of invalid data then system shows the valid error message.
2.	If network failure happens the student will not be able to create account.
Special Requirements	
Assumptions	
Test Plan Outline	   Nil
Notes and Issues	   Nil






3.3 Activity Diagram (My Profile):
 
Use Case ID: G4.2
	Use Case Name: MyProfile
Description

	After giving valid login credential User will be directed to their MyProfile Page.
Actor	       Student
Preconditions	
Post conditions	
Frequency of Use	               100 per day
Normal Course of Events	1.Student click on MyProfile.
2. System displays the MyProfile page.
3.After that they can edit MyProfile page.
Alternative Courses	Nil
Associated Use case diagrams 	

    Student
Exceptions
	3.	If any of the field is left blank or in case of invalid data then system shows the valid error message.
4.	If network failure happens the student will be directed to Home page.
Special Requirements	
Assumptions	
Test Plan Outline	   Nil
Notes and Issues	   Nil

3.4 Activity Diagram (Job Profile):

 
Use Case ID: G4.2
	Use Case Name: Job Profile
Description

	After giving valid login credential User ,TPO will be directed to their Job Profile Page.
Actor	       Student, TPO
Preconditions	Once Student, TPO Login they can see Job Profile page.
Post conditions	1. After going to Job Profile Page TPO can add Jobs in that page.
2. After going to Job Profile Page Student can see the job description, what is the last date to apply and whether the User have applied or not.
TPO can 
Frequency of Use	               100 per day
Normal Course of Events	1. click on Job Profile.
2. System displays the Job Profile page.
3.After that they can see Job Profile page.
Alternative Courses	Nil
Associated Use case diagrams 		                               

STUDENT

                                                                  TPO
Exceptions
	1.	If any of the field is left blank or in case of invalid data then system shows the valid error message.
2.	If network failure happens the student will be directed to Home page.
Special Requirements	
Assumptions	
Test Plan Outline	   Nil
Notes and Issues	   Nil





3.5 Activity Diagram (Generate Resume):

 


Use Case ID: G4.2
	Use Case Name: Generate Resume
Description

	After giving valid login credential Student will be directed to the Generate Resume Page.
Actor	       Student
Preconditions	Once Student  Login they can access Generate Resume page.
Post conditions	1. After going Generate Resume Page Student can generate their resume in that page.
 
Frequency of Use	               100 per day
Normal Course of Events	1. Student click on Generate Resume.
2. System displays the Generate Resume page.
3.After that they can generate resume from that page.
Alternative Courses	Nil
Associated Use case diagrams 		                               

STUDENT                                                                  
Exceptions
	1.	If any of the field is left blank or in case of invalid data then system shows the valid error message.
2.	If network failure happens the student will not be able to upload documents and will be directed to Home page.
Special Requirements	
Assumptions	
Test Plan Outline	   Nil
Notes and Issues	   Nil

3.6 Activity Diagram (Documents):
 


Use Case ID: G4.2
	Use Case Name: Documents
Description

	After going to MyProfile their they can access the Documents.
Actor	       Student
Preconditions	Once Student  Login they can access their Documents page.
Post conditions	1. After going Documents Page Student can upload their documents by giving the type in that page.
 
Frequency of Use	               100 per day
Normal Course of Events	1. Student click on Documents.
2. System displays the Documents page.
3.After that they can upload their documents in  that page.
Alternative Courses	Nil
Associated Use case diagrams 		                               

STUDENT                                                                  
Exceptions
	
1.	If network failure happens the student will not be directed to Home page.
Special Requirements	
Assumptions	
Test Plan Outline	   Nil
Notes and Issues	   Nil



ER Diagram:

 package com.placement.springjwt;
import org.springframework.boot.SpringApplication;
import org.springframework.boot.autoconfigure.SpringBootApplication;
@SpringBootApplication
public class SpringBootSecurityJwtApplication {
public static void main(String[] args) {
SpringApplication.run(SpringBootSecurityJwtApplication.class, args);
}
}
package com.placement.springjwt.models;
import javax.persistence.*;
@Entity
@Table(name = "roles")
public class Role {
@Id
@GeneratedValue(strategy = GenerationType.IDENTITY)
private Integer id;
@Enumerated(EnumType.STRING)
@Column(length = 20)
private ERole name;
public Role() {
}
public Role(ERole name) {
this.name = name;
}
public Integer getId() {
return id;
}
public void setId(Integer id) {
this.id = id;
}

public ERole getName() {
return name;
}
public void setName(ERole name) {
this.name = name;
}
}
package com.placement.springjwt.models;
public enum ERole {
ROLE_USER,
ROLE_MODERATOR,
ROLE_ADMIN
}

package com.placement.springjwt.models;
import java.util.HashSet;
import java.util.Set;
import javax.persistence.*;
import javax.validation.constraints.Email;
import javax.validation.constraints.NotBlank;
import javax.validation.constraints.Size;
@Entity
@Table( name = "users",
uniqueConstraints = {
@UniqueConstraint(columnNames = "username"),
@UniqueConstraint(columnNames = "email")
})
public class User {
@Id
@GeneratedValue(strategy = GenerationType.IDENTITY)
private Long id;

@NotBlank
@Size(max = 20)

private String username;
@NotBlank
@Size(max = 50)
@Email
private String email;
@NotBlank
@Size(max = 120)
private String password;
@ManyToMany(fetch = FetchType.LAZY)
@JoinTable( name = "user_roles",

joinColumns = @JoinColumn(name = "user_id"),
inverseJoinColumns = @JoinColumn(name = "role_id"))

private Set<Role> roles = new HashSet<>();
public User() {
}
public User(String username, String email, String password) {
this.username = username;
this.email = email;
this.password = password;
}
public Long getId() {
return id;
}
public void setId(Long id) {
this.id = id;
}
public String getUsername() {
return username;
}
public void setUsername(String username) {
this.username = username;

}
public String getEmail() {
return email;
}
public void setEmail(String email) {
this.email = email;
}
public String getPassword() {
return password;
}

public void setPassword(String password) {
this.password = password;
}

public Set<Role> getRoles() {
return roles;
}

public void setRoles(Set<Role> roles) {
this.roles = roles;
}
}
package com.placement.springjwt.models;

import java.math.BigInteger;

import javax.persistence.Column;
import javax.persistence.Entity;
import javax.persistence.GeneratedValue;
import javax.persistence.GenerationType;

import javax.persistence.Id;
import javax.persistence.Table;
@Entity
@Table(name = "student")

public class Student {
@Id
@GeneratedValue(strategy = GenerationType.IDENTITY)
private long id;
public Student() {
}
public Student(long id, String student_name, String student_regno, String
student_password, String student_emailID,

String student_phone, String student_DOB) {
super();
this.id = id;
this.student_name = student_name;
this.student_regno = student_regno;
this.student_password = student_password;
this.student_emailID = student_emailID;
this.student_phone = student_phone;
this.student_DOB = student_DOB;
}
public long getId() {
return id;
}
public void setId(long id) {
this.id = id;
}
public String getStudent_name() {
return student_name;

}
public void setStudent_name(String student_name) {
this.student_name = student_name;
}
public String getStudent_regno() {
return student_regno;
}
public void setStudent_regno(String student_regno) {
this.student_regno = student_regno;
}
public String getStudent_password() {
return student_password;
}
public void setStudent_password(String student_password) {
this.student_password = student_password;
}
public String getStudent_emailID() {
return student_emailID;
}
public void setStudent_emailID(String student_emailID) {
this.student_emailID = student_emailID;
}
public String getStudent_phone() {
return student_phone;
}
public void setStudent_phone(String student_phone) {
this.student_phone = student_phone;
}
public String getStudent_DOB() {
return student_DOB;
}

public void setStudent_DOB(String student_DOB) {
this.student_DOB = student_DOB;
}
@Column(name="student_name")
private String student_name;
@Column(name="student_regno")
private String student_regno;
@Column(name="student_password")
private String student_password;
@Column(name="student_emailid")
private String student_emailID;
@Column(name="student_phone")
private String student_phone;
@Column(name="student_DOB")
private String student_DOB;
}
package com.placement.springjwt.models;
import java.util.Set;
import javax.persistence.Column;
import javax.persistence.Entity;
import javax.persistence.GeneratedValue;
import javax.persistence.GenerationType;
import javax.persistence.Id;
import javax.persistence.Table;
import javax.validation.constraints.*;
@Entity
@Table(name = "TPO")
public class Tpo {
@Id
@GeneratedValue(strategy = GenerationType.IDENTITY)
private long id;

public Tpo() {
}
public Tpo(long id, String tpo_name, String tpo_password, @Email String tpo_emailID, String
tpo_phone) {
super();
this.id = id;
this.tpo_name = tpo_name;
this.tpo_password = tpo_password;
this.tpo_emailID = tpo_emailID;
this.tpo_phone = tpo_phone;
}
public long getId() {
return id;
}
public void setId(long id) {
this.id = id;
}
public String getTpo_name() {
return tpo_name;
}
public void setTpo_name(String tpo_name) {
this.tpo_name = tpo_name;
}
public String getTpo_password() {
return tpo_password;
}
public void setTpo_password(String tpo_password) {
this.tpo_password = tpo_password;
}
public String getTpo_emailID() {
return tpo_emailID;

}
public void setTpo_emailID(String tpo_emailID) {
this.tpo_emailID = tpo_emailID;
}
public String getTpo_phone() {
return tpo_phone;
}
public void setTpo_phone(String tpo_phone) {
this.tpo_phone = tpo_phone;
}
@Column(name="tpo_name")
private String tpo_name;
@Column(name="tpo_password")
private String tpo_password;
@Email
@Column(name="tpo_emailid")
private String tpo_emailID;
@Column(name="tpo_phone")
private String tpo_phone;
}
package com.placement.springjwt.models;
import javax.persistence.Column;
import javax.persistence.Entity;
import javax.persistence.GeneratedValue;
import javax.persistence.GenerationType;
import javax.persistence.Id;
import javax.persistence.Table;

@Entity
@Table(name = "jobdetail")

public class JobDetail {
@Id
@GeneratedValue(strategy = GenerationType.IDENTITY)
private long id;

public JobDetail() {

}

public long getId() {
return id;
}

public void setId(long id) {
this.id = id;
}

public String getCompanyname() {
return companyname;
}

public void setCompanyname(String companyname) {
this.companyname = companyname;
}

public String getAgreement() {
return agreement;
}

public void setAgreement(String agreement) {
this.agreement = agreement;

}
public String getDesignation() {
return designation;
}
public void setDesignation(String designation) {
this.designation = designation;
}
public String getCTC() {
return CTC;
}
public void setCTC(String cTC) {
CTC = cTC;
}
public int getBatch() {
return batch;
}
public void setBatch(int batch) {
this.batch = batch;
}
public String getInternship_period() {
return Internship_period;
}
public void setInternship_period(String internship_period) {
Internship_period = internship_period;
}
public String getRequirements() {
return requirements;
}
public void setRequirements(String requirements) {
this.requirements = requirements;
}

public String getSelectioncriteria() {
return selectioncriteria;
}
public void setSelectioncriteria(String selectioncriteria) {
this.selectioncriteria = selectioncriteria;
}
public String getDescription() {
return description;
}
public void setDescription(String description) {
this.description = description;
}
@Column(name="companyname")
private String companyname;
@Column(name="agreement")
private String agreement;
@Column(name="designation")
private String designation;
public JobDetail(long id, String companyname, String agreement, String designation, String
cTC, int batch,

String internship_period, String requirements, String selectioncriteria, String

description) {
super();
this.id = id;
this.companyname = companyname;
this.agreement = agreement;
this.designation = designation;
CTC = cTC;
this.batch = batch;
Internship_period = internship_period;
this.requirements = requirements;
this.selectioncriteria = selectioncriteria;

this.description = description;
}
@Column(name="CTC")
private String CTC;
@Column(name="batch")
private int batch;
@Column(name="Internship_period")
private String Internship_period;
@Column(name="requirements")
private String requirements;
@Column(name="selectioncriteria")
private String selectioncriteria;
@Column(name="description")
private String description;
}
package com.placement.springjwt.models;
import javax.persistence.Entity;
import javax.persistence.GeneratedValue;
import javax.persistence.Id;
import javax.persistence.Lob;
import javax.persistence.Table;
import org.hibernate.annotations.GenericGenerator;
@Entity
@Table(name = "files")
public class FileDB {
@Id
@GeneratedValue(generator = "uuid")
@GenericGenerator(name = "uuid", strategy = "uuid2")
private String id;
private String name;
private String type;

@Lob
private byte[] data;
public FileDB() {
}
public FileDB(String name, String type, byte[] data) {
this.name = name;
this.type = type;
this.data = data;
}
public String getId() {
return id;
}
public String getName() {
return name;
}
public void setName(String name) {
this.name = name;
}
public String getType() {
return type;
}
public void setType(String type) {
this.type = type;
}
public byte[] getData() {
return data;
}
public void setData(byte[] data) {
this.data = data;
}
}

CONTROLLLER
package com.placement.springjwt.controllers;
import java.util.HashSet;
import java.util.List;
import java.util.Set;
import java.util.stream.Collectors;
import javax.validation.Valid;
import org.springframework.beans.factory.annotation.Autowired;
import org.springframework.http.ResponseEntity;
import org.springframework.security.authentication.AuthenticationManager;
import org.springframework.security.authentication.UsernamePasswordAuthenticationToken;
import org.springframework.security.core.Authentication;
import org.springframework.security.core.context.SecurityContextHolder;
import org.springframework.security.crypto.password.PasswordEncoder;
import org.springframework.web.bind.annotation.CrossOrigin;
import org.springframework.web.bind.annotation.PostMapping;
import org.springframework.web.bind.annotation.RequestBody;
import org.springframework.web.bind.annotation.RequestMapping;
import org.springframework.web.bind.annotation.RestController;
import com.placement.springjwt.models.ERole;
import com.placement.springjwt.models.Role;
import com.placement.springjwt.models.User;
import com.placement.springjwt.payload.request.LoginRequest;
import com.placement.springjwt.payload.request.SignupRequest;
import com.placement.springjwt.payload.response.JwtResponse;
import com.placement.springjwt.payload.response.MessageResponse;
import com.placement.springjwt.repository.RoleRepository;
import com.placement.springjwt.repository.UserRepository;
import com.placement.springjwt.security.jwt.JwtUtils;
import com.placement.springjwt.security.services.UserDetailsImpl;
@CrossOrigin(origins = "*", maxAge = 3600)

@RestController
@RequestMapping("/api/auth")
public class AuthController {
@Autowired
AuthenticationManager authenticationManager;
@Autowired
UserRepository userRepository;
@Autowired
RoleRepository roleRepository;
@Autowired
PasswordEncoder encoder;
@Autowired
JwtUtils jwtUtils;
@PostMapping("/signin")
public ResponseEntity<?> authenticateUser(@Valid @RequestBody LoginRequest
loginRequest) {

Authentication authentication = authenticationManager.authenticate(

new

UsernamePasswordAuthenticationToken(loginRequest.getUsername(),
loginRequest.getPassword()));

SecurityContextHolder.getContext().setAuthentication(authentication);
String jwt = jwtUtils.generateJwtToken(authentication);
UserDetailsImpl userDetails = (UserDetailsImpl) authentication.getPrincipal();

List<String> roles = userDetails.getAuthorities().stream()
.map(item -> item.getAuthority())
.collect(Collectors.toList());
return ResponseEntity.ok(new JwtResponse(jwt,

userDetails.getId(),
userDetails.getUsername(),

userDetails.getEmail(),
roles));
}

@PostMapping("/signup")
public ResponseEntity<?> registerUser(@Valid @RequestBody SignupRequest
signUpRequest) {

if (userRepository.existsByUsername(signUpRequest.getUsername())) {
return ResponseEntity
.badRequest()
.body(new MessageResponse("Error: Username is already

taken!"));
}

if (userRepository.existsByEmail(signUpRequest.getEmail())) {
return ResponseEntity
.badRequest()
.body(new MessageResponse("Error: Email is already in

use!"));
}

// Create new user's account
User user = new User(signUpRequest.getUsername(),

signUpRequest.getEmail(),

encoder.encode(signUpRequest.getPassword()));

Set<String> strRoles = signUpRequest.getRole();
Set<Role> roles = new HashSet<>();

if (strRoles == null) {

Role userRole = roleRepository.findByName(ERole.ROLE_USER)

.orElseThrow(() -> new RuntimeException("Error: Role is not

found."));

roles.add(userRole);
} else {
strRoles.forEach(role -> {
switch (role) {
case "admin":
Role adminRole =
roleRepository.findByName(ERole.ROLE_ADMIN)
.orElseThrow(() -> new RuntimeException("Error: Role is not found."));

roles.add(adminRole);

break;
case "mod":

Role modRole = roleRepository.findByName(ERole.ROLE_MODERATOR)
.orElseThrow(() -> new RuntimeException("Error: Role is not found."));

roles.add(modRole);

break;
default:
Role userRole =
roleRepository.findByName(ERole.ROLE_USER)

.orElseThrow(() -> new RuntimeException("Error: Role is not

found."));

roles.add(userRole);
}
});
}

user.setRoles(roles);
userRepository.save(user);

return ResponseEntity.ok(new MessageResponse("User registered successfully!"));
}
}
package com.placement.springjwt.controllers;

import java.util.HashMap;
import java.util.List;
import java.util.Map;
import org.springframework.beans.factory.annotation.Autowired;
import org.springframework.http.ResponseEntity;
import org.springframework.security.access.prepost.PreAuthorize;
import org.springframework.web.bind.annotation.CrossOrigin;
import org.springframework.web.bind.annotation.DeleteMapping;
import org.springframework.web.bind.annotation.GetMapping;
import org.springframework.web.bind.annotation.PathVariable;
import org.springframework.web.bind.annotation.PostMapping;
import org.springframework.web.bind.annotation.PutMapping;
import org.springframework.web.bind.annotation.RequestBody;
import org.springframework.web.bind.annotation.RestController;
import com.placement.springjwt.exce.ResourceNotFoundException;
import com.placement.springjwt.models.Student;
import com.placement.springjwt.repository.AddStudentRepo;
@CrossOrigin(origins = "http://localhost:3000")
@RestController
//@RequestMapping("/SRP/ADMIN")
public class AddStudent {
@Autowired
private AddStudentRepo addStudentRepo;
@GetMapping("/stud")
@PreAuthorize(" hasRole('ADMIN') ")

public List<Student> getAllStudent(){
return addStudentRepo.findAll();
}
@PostMapping("/stud")
@PreAuthorize(" hasRole('ADMIN')")
public Student createStudent(@RequestBody Student student) {
return addStudentRepo.save(student);
}
@PutMapping("/stud/{id}")
@PreAuthorize(" hasRole('ADMIN') or hasRole('USER') ")
public ResponseEntity<Student> updateStudent(@PathVariable Long id, @RequestBody
Student student){

Student Students = addStudentRepo.findById(id)

.orElseThrow(() -> new ResourceNotFoundException("Student not

exist with id :" + id));

Students.setStudent_name(student.getStudent_name());
Students.setStudent_regno(student.getStudent_regno());
Students.setStudent_emailID(student.getStudent_emailID());
Students.setStudent_DOB(student.getStudent_DOB());
Students.setStudent_phone(student.getStudent_phone());
Students.setStudent_password(student.getStudent_password());
Student updatedStudentDetail = addStudentRepo.save(Students);
return ResponseEntity.ok(updatedStudentDetail);
}
@GetMapping("/stud/{id}")
@PreAuthorize(" hasRole('ADMIN') or hasRole('USER') ")
public ResponseEntity<Student> getStudentById(@PathVariable Long id) {
Student student = addStudentRepo.findById(id)

.orElseThrow(() -> new ResourceNotFoundException("Student not

exist with id :" + id));

return ResponseEntity.ok(student);

}
@DeleteMapping("/stud/{id}")
@PreAuthorize(" hasRole('ADMIN') ")
public ResponseEntity<Map<String, Boolean>> deleteStudent(@PathVariable Long id){
Student student = addStudentRepo.findById(id)

.orElseThrow(() -> new ResourceNotFoundException("Student not

exist with id :" + id));

addStudentRepo.delete(student);
Map<String, Boolean> response = new HashMap<>();
response.put("deleted", Boolean.TRUE);
return ResponseEntity.ok(response);
}
}
package com.placement.springjwt.controllers;
import java.util.HashMap;
import java.util.List;
import java.util.Map;
import org.springframework.beans.factory.annotation.Autowired;
import org.springframework.http.ResponseEntity;
import org.springframework.security.access.prepost.PreAuthorize;
import org.springframework.web.bind.annotation.CrossOrigin;
import org.springframework.web.bind.annotation.DeleteMapping;
import org.springframework.web.bind.annotation.GetMapping;
import org.springframework.web.bind.annotation.PathVariable;
import org.springframework.web.bind.annotation.PostMapping;
import org.springframework.web.bind.annotation.PutMapping;
import org.springframework.web.bind.annotation.RequestBody;
import org.springframework.web.bind.annotation.RequestMapping;
import org.springframework.web.bind.annotation.RestController;

import com.placement.springjwt.exce.ResourceNotFoundException;
import com.placement.springjwt.models.Tpo;
import com.placement.springjwt.repository.AddTpoRepo;
@CrossOrigin(origins = "http://localhost:3000")
@RestController
public class AddTpo {
@Autowired
private AddTpoRepo addTpoRepo;
@GetMapping("/tpo")
@PreAuthorize(" hasRole('ADMIN') ")
public List<Tpo> getAllTpo(){
return addTpoRepo.findAll();
}
@PostMapping("/tpo")
@PreAuthorize(" hasRole('ADMIN') ")
public Tpo createTpo(@RequestBody Tpo tpo) {
return addTpoRepo.save(tpo);
}
@PutMapping("/tpo/{id}")
@PreAuthorize(" hasRole('ADMIN') or hasRole('MODERATOR') ")
public ResponseEntity<Tpo> updateTpo(@PathVariable Long id, @RequestBody Tpo tpo){
Tpo tpO = addTpoRepo.findById(id)

.orElseThrow(() -> new ResourceNotFoundException("Tpo not exist

with id :" + id));

tpO.setTpo_name(tpo.getTpo_name());
tpO.setTpo_emailID(tpo.getTpo_emailID());
tpO.setTpo_password(tpo.getTpo_password());
tpO.setTpo_phone(tpo.getTpo_phone());
Tpo updatedtpoDetail = addTpoRepo.save(tpO);
return ResponseEntity.ok(updatedtpoDetail);

}
@GetMapping("/tpo/{id}")
public ResponseEntity<Tpo> getTpoById(@PathVariable Long id) {
Tpo tpo = addTpoRepo.findById(id)

.orElseThrow(() -> new ResourceNotFoundException("Tpo not exist

with id :" + id));

return ResponseEntity.ok(tpo);
}
@DeleteMapping("/tpo/{id}")
@PreAuthorize(" hasRole('ADMIN') ")
public ResponseEntity<Map<String, Boolean>> deleteTpo(@PathVariable Long id){
Tpo tpo = addTpoRepo.findById(id)

.orElseThrow(() -> new ResourceNotFoundException("Tpo not exist

with id :" + id));

addTpoRepo.delete(tpo);
Map<String, Boolean> response = new HashMap<>();
response.put("deleted", Boolean.TRUE);
return ResponseEntity.ok(response);
}
}
package com.placement.springjwt.controllers;

import java.util.HashMap;
import java.util.List;
import java.util.Map;

import org.springframework.beans.factory.annotation.Autowired;
import org.springframework.http.ResponseEntity;
import org.springframework.security.access.prepost.PreAuthorize;
import org.springframework.web.bind.annotation.CrossOrigin;

import org.springframework.web.bind.annotation.DeleteMapping;
import org.springframework.web.bind.annotation.GetMapping;
import org.springframework.web.bind.annotation.PathVariable;
import org.springframework.web.bind.annotation.PostMapping;
import org.springframework.web.bind.annotation.PutMapping;
import org.springframework.web.bind.annotation.RequestBody;
import org.springframework.web.bind.annotation.RequestMapping;
import org.springframework.web.bind.annotation.RestController;
import com.placement.springjwt.exce.ResourceNotFoundException;
import com.placement.springjwt.models.JobDetail;
import com.placement.springjwt.repository.JobDetailRepo;
@CrossOrigin(origins = "http://localhost:3000")
@RestController
public class TPOAddJob {
@Autowired
private JobDetailRepo jobDetailRepo;
@GetMapping("/job")
@PreAuthorize("hasRole('USER') or hasRole('MODERATOR') or hasRole('ADMIN')")
public List<JobDetail> getAllJob(){
return jobDetailRepo.findAll();
}
@PostMapping("/job")
@PreAuthorize(" hasRole('MODERATOR') or hasRole('ADMIN')")
public JobDetail createJob(@RequestBody JobDetail jobDetails) {
return jobDetailRepo.save(jobDetails);
}
@PutMapping("/job/{id}")
@PreAuthorize(" hasRole('MODERATOR') or hasRole('ADMIN')")
public ResponseEntity<JobDetail> updateJob(@PathVariable Long id, @RequestBody
JobDetail jobDetails){

JobDetail jobDetail = jobDetailRepo.findById(id)

.orElseThrow(() -> new ResourceNotFoundException("Job not exist

with id :" + id));

jobDetail.setCompanyname(jobDetails.getCompanyname());
jobDetail.setDesignation(jobDetails.getDesignation());

jobDetail.setCTC(jobDetails.getCTC());
jobDetail.setBatch(jobDetails.getBatch());
jobDetail.setInternship_period(jobDetails.getInternship_period());
jobDetail.setRequirements(jobDetails.getRequirements());
jobDetail.setSelectioncriteria(jobDetails.getSelectioncriteria());
jobDetail.setAgreement(jobDetails.getAgreement());
jobDetail.setDescription(jobDetails.getDescription());

JobDetail updatedjobDetail = jobDetailRepo.save(jobDetail);
return ResponseEntity.ok(updatedjobDetail);
}
@GetMapping("/job/{id}")
@PreAuthorize(" hasRole('MODERATOR') or hasRole('ADMIN')")
public ResponseEntity<JobDetail> getJobById(@PathVariable Long id) {
JobDetail jobDetail = jobDetailRepo.findById(id)

.orElseThrow(() -> new ResourceNotFoundException("Job not exist

with id :" + id));

return ResponseEntity.ok(jobDetail);
}
@DeleteMapping("/job/{id}")
@PreAuthorize(" hasRole('MODERATOR') or hasRole('ADMIN')")
public ResponseEntity<Map<String, Boolean>> deleteJob(@PathVariable Long id){
JobDetail jobDetail = jobDetailRepo.findById(id)

.orElseThrow(() -> new ResourceNotFoundException("Job not exist

with id :" + id));

jobDetailRepo.delete(jobDetail);

Map<String, Boolean> response = new HashMap<>();
response.put("deleted", Boolean.TRUE);
return ResponseEntity.ok(response);
}

}
package com.placement.springjwt.controllers;
import java.util.HashMap;
import java.util.List;
import java.util.Map;
import org.springframework.beans.factory.annotation.Autowired;
import org.springframework.http.ResponseEntity;
import org.springframework.security.access.prepost.PreAuthorize;
import org.springframework.web.bind.annotation.CrossOrigin;
import org.springframework.web.bind.annotation.DeleteMapping;
import org.springframework.web.bind.annotation.GetMapping;
import org.springframework.web.bind.annotation.PathVariable;
import org.springframework.web.bind.annotation.PostMapping;
import org.springframework.web.bind.annotation.PutMapping;
import org.springframework.web.bind.annotation.RequestBody;
import org.springframework.web.bind.annotation.RestController;
import com.placement.springjwt.exce.ResourceNotFoundException;
import com.placement.springjwt.models.AppliedJob;
import com.placement.springjwt.models.Student;
import com.placement.springjwt.repository.AddStudentRepo;
import com.placement.springjwt.repository.AppliedJobRepo;
@CrossOrigin(origins = "http://localhost:3000")
@RestController
//@RequestMapping("/SRP/ADMIN")
public class ApplyJob {
@Autowired

private AppliedJobRepo appliedJobRepo;
@GetMapping("/apply")
@PreAuthorize(" hasRole('USER') ")
public List<AppliedJob> getAllStudent(){
return appliedJobRepo.findAll();
}
@PostMapping("/apply")
@PreAuthorize(" hasRole('USER')")
public AppliedJob createStudent(@RequestBody AppliedJob appliedJob) {
return appliedJobRepo.save(appliedJob);
}
@PutMapping("/apply/{id}")
@PreAuthorize(" hasRole('ADMIN') or hasRole('USER') ")
public ResponseEntity<AppliedJob> updateStudent(@PathVariable Long id, @RequestBody
AppliedJob appliedJob){

AppliedJob Appliedjob = appliedJobRepo.findById(id)

.orElseThrow(() -> new ResourceNotFoundException("Student not

exist with id :" + id));

Appliedjob.setName(appliedJob.getName());
Appliedjob.setEmail(appliedJob.getEmail());
Appliedjob.setAddress(appliedJob.getAddress());
Appliedjob.setRegno(appliedJob.getRegno());
Appliedjob.setPhone(appliedJob.getPhone());
Appliedjob.setCampus(appliedJob.getCampus());
Appliedjob.setTenth(appliedJob.getTenth());
Appliedjob.setTwelth(appliedJob.getTwelth());

AppliedJob updatedStudentDetail = appliedJobRepo.save(Appliedjob);
return ResponseEntity.ok(updatedStudentDetail);
}

}
package com.placement.springjwt.controllers;
import java.util.List;
import java.util.stream.Collectors;
import org.springframework.beans.factory.annotation.Autowired;
import org.springframework.http.HttpHeaders;
import org.springframework.http.HttpStatus;
import org.springframework.http.ResponseEntity;
import org.springframework.stereotype.Controller;
import org.springframework.web.bind.annotation.CrossOrigin;
import org.springframework.web.bind.annotation.GetMapping;
import org.springframework.web.bind.annotation.PathVariable;
import org.springframework.web.bind.annotation.PostMapping;
import org.springframework.web.bind.annotation.RequestParam;
import org.springframework.web.multipart.MultipartFile;
import org.springframework.web.servlet.support.ServletUriComponentsBuilder;
import com.placement.springjwt.message.ResponseFile;
import com.placement.springjwt.message.ResponseMessage;
import com.placement.springjwt.models.FileDB;
import com.placement.springjwt.security.services.FileStorageService;
@Controller
//@CrossOrigin("http://localhost:8081")
public class FileController {
@Autowired
private FileStorageService storageService;
@PostMapping("/upload")
public ResponseEntity<ResponseMessage> uploadFile(@RequestParam("file") MultipartFile file) {
String message = "";
try {
storageService.store(file);
message = "Uploaded the file successfully: " + file.getOriginalFilename();

return ResponseEntity.status(HttpStatus.OK).body(new ResponseMessage(message));
} catch (Exception e) {
message = "Could not upload the file: " + file.getOriginalFilename() + "!";
return ResponseEntity.status(HttpStatus.EXPECTATION_FAILED).body(new
ResponseMessage(message));
}
}
@GetMapping("/files")
public ResponseEntity<List<ResponseFile>> getListFiles() {
List<ResponseFile> files = storageService.getAllFiles().map(dbFile -> {
String fileDownloadUri = ServletUriComponentsBuilder
.fromCurrentContextPath()
.path("/files/")
.path(dbFile.getId())
.toUriString();
return new ResponseFile(
dbFile.getName(),
fileDownloadUri,
dbFile.getType(),
dbFile.getData().length);
}).collect(Collectors.toList());
return ResponseEntity.status(HttpStatus.OK).body(files);
}
@GetMapping("/files/{id}")
public ResponseEntity<byte[]> getFile(@PathVariable String id) {
FileDB fileDB = storageService.getFile(id);
return ResponseEntity.ok()
.header(HttpHeaders.CONTENT_DISPOSITION, "attachment; filename=\"" + fileDB.getName() +
"\"")
.body(fileDB.getData());
}
}

package com.placement.springjwt.security.services;
import java.util.Collection;
import java.util.List;
import java.util.Objects;
import java.util.stream.Collectors;
import org.springframework.security.core.GrantedAuthority;
import org.springframework.security.core.authority.SimpleGrantedAuthority;
import org.springframework.security.core.userdetails.UserDetails;

import com.fasterxml.jackson.annotation.JsonIgnore;
import com.placement.springjwt.models.User;

public class UserDetailsImpl implements UserDetails {
private static final long serialVersionUID = 1L;
private Long id;
private String username;
private String email;

@JsonIgnore
private String password;

private Collection<? extends GrantedAuthority> authorities;

public UserDetailsImpl(Long id, String username, String email, String password,
Collection<? extends GrantedAuthority> authorities) {
this.id = id;
this.username = username;
this.email = email;
this.password = password;
this.authorities = authorities;
}

public static UserDetailsImpl build(User user) {
List<GrantedAuthority> authorities = user.getRoles().stream()

.map(role -> new SimpleGrantedAuthority(role.getName().name()))
.collect(Collectors.toList());

return new UserDetailsImpl(
user.getId(),
user.getUsername(),
user.getEmail(),
user.getPassword(),
authorities);

}
@Override
public Collection<? extends GrantedAuthority> getAuthorities() {
return authorities;
}
public Long getId() {
return id;
}
public String getEmail() {
return email;
}
@Override
public String getPassword() {
return password;
}

@Override
public String getUsername() {
return username;
}

@Override
public boolean isAccountNonExpired() {
return true;
}
@Override
public boolean isAccountNonLocked() {
return true;
}
@Override
public boolean isCredentialsNonExpired() {
return true;
}

@Override
public boolean isEnabled() {
return true;
}
@Override
public boolean equals(Object o) {
if (this == o)
return true;
if (o == null || getClass() != o.getClass())
return false;
UserDetailsImpl user = (UserDetailsImpl) o;
return Objects.equals(id, user.id);
}
}
package com.placement.springjwt.security.services;
import org.springframework.beans.factory.annotation.Autowired;
import org.springframework.security.core.userdetails.UserDetails;
import org.springframework.security.core.userdetails.UserDetailsService;

import org.springframework.security.core.userdetails.UsernameNotFoundException;
import org.springframework.stereotype.Service;
import org.springframework.transaction.annotation.Transactional;
import com.placement.springjwt.models.User;
import com.placement.springjwt.repository.UserRepository;
@Service
public class UserDetailsServiceImpl implements UserDetailsService {
@Autowired
UserRepository userRepository;
@Override
@Transactional
public UserDetails loadUserByUsername(String username) throws
UsernameNotFoundException {

User user = userRepository.findByUsername(username)

.orElseThrow(() -> new UsernameNotFoundException("User Not

Found with username: " + username));

return UserDetailsImpl.build(user);
}
}
FRONTEND:
import React, { Component } from 'react'
import JobService from '../service/JobService';
export class AddJob extends Component {
constructor(props) {
super(props)
this.state = {
id:this.props.match.params.id,
companyname: '',
agreement: '',
designation: '',
ctc:'',

internship_period:'',
batch:'',
requirements:'',
selectioncriteria:'',
description:''
}
this.changecompanyname = this.changecompanyname.bind(this);
this.changeagreement=this.changeagreement.bind(this);
this.changedesignation=this.changedesignation.bind(this);
this.changectc=this.changectc.bind(this);
this.changeinternship_period=this.changeinternship_period.bind(this);
this.changebatch=this.changebatch.bind(this);
this.changerequirements=this.changerequirements.bind(this);
this.changeselectioncriteria=this.changeselectioncriteria.bind(this);
this.changedescription=this.changedescription.bind(this);
this.saveOrUpdateJob = this.saveOrUpdateJob.bind(this);
this.cancel = this.cancel.bind(this);
}
saveOrUpdateJob = (e) => {
e.preventDefault();
let job = {companyname: this.state.companyname, agreement: this.state.agreement,
designation: this.state.designation,ctc: this.state.ctc,internship_period:
this.state.internship_period,batch:
this.state.batch,requirements:this.state.requirements,selectioncriteria:this.state.selectioncriteria,de
scription:this.state.description};
console.log('Job => ' +JSON.stringify(job));
if(this.state.id === '_add'){
JobService.createJob(job).then(res =>{
this.props.history.push('/job');
});
}else{
JobService.updateJob(job, this.state.id).then( res => {

this.props.history.push('/job');
});
}
}
componentDidMount(){
if(this.state.id === '_add'){
return
}else{
JobService.getJobById(this.state.id).then ( (res)=>{
let job= res.data;
this.setState({companyname:job.companyname,
agreement: job.agreement,
batch:job.batch,
designation:job.designation,
internship_period:job.internship_period,
ctc:job.ctc,
requirements:job.requirements,
selectioncriteria:job.selectioncriteria,
description:job.description
});
});
}
}
cancel(){
this.props.history.push('/job/');
}
getTitle(){
if(this.state.id === '_add'){
return <h3 className="text-center">Add Job</h3>
}else{
return <h3 className="text-center">Update Job</h3>

}
}
changecompanyname= (event) => {
this.setState({companyname: event.target.value});
}
changeagreement= (event) => {
this.setState({agreement: event.target.value});
}
changedesignation= (event) => {
this.setState({designation: event.target.value});
}
changectc= (event) => {
this.setState({ctc: event.target.value});
}
changeinternship_period= (event) => {
this.setState({internship_period: event.target.value});
}
changebatch= (event) => {
this.setState({batch: event.target.value});
}
changedescription= (event) => {
this.setState({description: event.target.value});
}
changerequirements= (event) => {
this.setState({requirements: event.target.value});
}
changeselectioncriteria= (event) => {
this.setState({selectioncriteria: event.target.value});
}
render() {
return (

<div>
<br></br>
<div className = "container" >
<div className = "row" >
<div className = "card col-md-6 offset-md-3 offset-md-3" id="add">
{
this.getTitle()
}
<div className = "card-body" >
<form>
<div className = "form-group" >
<label> Company Name: </label>
<input placeholder="Company Name" name="companyname"
className="form-control"
value={this.state.companyname} onChange={this.changecompanyname} />
</div>
<div className = "form-group">
<label> Batch: </label>
<input placeholder="Batch" name="batch" className="form-control"
value={this.state.batch} onChange={this.changebatch}/>
</div>
<div className = "form-group">
<label> Designation: </label>

<input placeholder="Designation" name="designation" className="form-
control"

value={this.state.designation} onChange={this.changedesignation}/>
</div>
<div className = "form-group">
<label>CTC: </label>
<input placeholder="CTC" name="ctc" className="form-control"
value={this.state.ctc} onChange={this.changectc}/>
</div>

<div className = "form-group">
<label> Agreement: </label>

<input placeholder="Agreement" name="agreement" className="form-
control"

value={this.state.agreement} onChange={this.changeagreement}/>
</div>
<div className = "form-group">
<label> Job Requirements: </label>
<input placeholder=" Job Requirements" name=" requirements"
className="form-control"
value={this.state.requirements} onChange={this.changerequirements}/>
</div>
<div className = "form-group">
<label> Selectioncriteria: </label>
<input placeholder="Selectioncriteria" name="selectioncriteria"
className="form-control"
value={this.state.selectioncriteria}
onChange={this.changeselectioncriteria}/>
</div>
<div className = "form-group">
<label> Internship_period: </label>
<input placeholder="Internship_period" name="internship_period"
className="form-control"
value={this.state.internship_period}
onChange={this.changeinternship_period}/>
</div>
<div className = "form-group">
<label> Description: </label>

<input placeholder="description" name="description" className="form-
control"

value={this.state.description} onChange={this.changedescription}/>
</div>
<button className="btn btn-success"
onClick={this.saveOrUpdateJob}>Save</button>

<button className="btn btn-danger" onClick={this.cancel.bind(this)}
style={{marginLeft: "10px"}}>Cancel</button>
</form>
</div>
</div>
</div>
</div>
</div>
)
}
}
export default AddJob
import React, { Component } from 'react'
import ApplyJobService from '../service/ApplyJobService';
export class ApplyJob extends Component {
constructor(props) {
super(props)
this.state = {
name: '',
email: '',
address: '',
phone:'',
regno:'',
campus:'',
tenth:'',
twelth:'',
}
this.changename = this.changename.bind(this);
this.changeemail=this.changeemail.bind(this);
this.changeaddress=this.changeaddress.bind(this);
this.changephone=this.changephone.bind(this);

this.changeregno=this.changeregno.bind(this);
this.changecampus=this.changecampus.bind(this);
this.changetenth=this.changetenth.bind(this);
this.changetwelth=this.changetwelth.bind(this);
this.saveJob = this.saveJob.bind(this);
this.cancel = this.cancel.bind(this);
}
saveJob = (e) => {
e.preventDefault();
let job = {name: this.state.name, email: this.state.email, address: this.state.address,phone:
this.state.phone, regno: this.state.regno, campus: this.state.campus, tenth: this.state.tenth, twelth:
this.state.twelth};
console.log('job => ' + JSON.stringify(job));
ApplyJobService.createJob(job).then(res =>{
this.props.history.push('/JobProfStud');
});
}
cancel(){
this.props.history.push('/JobProfStud/');
}
changename= (event) => {
this.setState({name: event.target.value});
}
changeemail= (event) => {
this.setState({email: event.target.value});
}
changeaddress= (event) => {
this.setState({address: event.target.value});
}
changeregno= (event) => {
this.setState({regno: event.target.value});
}

changecampus= (event) => {
this.setState({campus: event.target.value});
}
changetenth= (event) => {
this.setState({tenth: event.target.value});
}
changetwelth= (event) => {
this.setState({twelth: event.target.value});
}
changephone= (event) => {
this.setState({phone: event.target.value});
}
render() {
return (
<div>
<br></br>
<div className = "container" >
<div className = "row" >
<div className = "card col-md-6 offset-md-3 offset-md-3" id="add">
<h3 style={{textAlign:"center"}}>Apply Job</h3>
<div className = "card-body" >
<form>
<div className = "form-group" >
<label> Name: </label>
<input placeholder=" Name" name="name" className="form-control"
type="text"
value={this.state.name} onChange={this.changename} />
</div>
<div className = "form-group">
<label> Email: </label>
<input placeholder="Email" name="email" className="form-control"
type="email"

value={this.state.email} onChange={this.changeemail} />
</div>
<div className = "form-group">
<label> Address: </label>
<input placeholder="Address" name="address" className="form-control"
value={this.state.address} onChange={this.changeaddress} />
</div>
<div className = "form-group">
<label>Phone: </label>
<input placeholder="Phone" name="phone" className="form-control"
value={this.state.phone} onChange={this.changephone} />
</div>
<div className = "form-group">
<label> Registration No.: </label>

<input placeholder="Registration No." name="regno" className="form-
control"

value={this.state.regno} onChange={this.changeregno} />
</div>
<div className = "form-group">
<label> Campus: </label>
<input placeholder="Campus" name="campus" className="form-control"
value={this.state.campus} onChange={this.changecampus} />
</div>
<div className = "form-group">
<label> Tenth Marks: </label>
<input placeholder="TenthMarks: " name="tenth: " className="form-control"
value={this.state.tenth} onChange={this.changetenth} />
</div>
<div className = "form-group">
<label> Twelth Marks: </label>
<input placeholder="TwelthMarks" name="twelth" className="form-control"

value={this.state.twelth} onChange={this.changetwelth} />
</div>
<button className="btn btn-success" onClick={this.saveJob} >Apply</button>
<button className="btn btn-danger"
onClick={this.cancel}style={{marginLeft: "10px"}}>Cancel</button>
</form>
</div>
</div>
</div>

</div>
</div>
)
}
}

import axios from 'axios';
import authHeader from './auth-header';
const JOB_API_BASE_URL = "http://localhost:8080/job";
class JobService {
getJob(){
return axios.get(JOB_API_BASE_URL, { headers: authHeader() });
}
createJob(job){
return axios.post(JOB_API_BASE_URL,job,{ headers: authHeader() });
}
getJobById(jobId){
return axios.get(JOB_API_BASE_URL + '/ ' + jobId,{ headers: authHeader() });
}
updateJob(job, jobId){
return axios.put(JOB_API_BASE_URL + '/' + jobId, job,{ headers: authHeader() });

}
deleteJob(jobId){
return axios.delete(JOB_API_BASE_URL + '/' + jobId,{ headers: authHeader() });
}
}
import axios from 'axios';
import authHeader from './auth-header';
const JOB_API_BASE_URL = "http://localhost:8080/apply";
class ApplyJobService {
createJob(job){
return axios.post(JOB_API_BASE_URL,job,{ headers: authHeader() });}
getJobById(jobId){
return axios.get(JOB_API_BASE_URL + '/ ' + jobId,{ headers: authHeader() });
}}
import axios from "axios";

const API_URL = "http://localhost:8080/api/auth/";

class AuthService {
login(username, password) {
return axios
.post(API_URL + "signin", {
username,
password
})
.then(response => {
if (response.data.accessToken) {
localStorage.setItem("user", JSON.stringify(response.data));
}

return response.data;

});
}

logout() {
localStorage.removeItem("user");
}

register(username, email, password) {
return axios.post(API_URL + "signup", {
username,
email,
password
});
}

getCurrentUser() {
return JSON.parse(localStorage.getItem('user'));;
}
}

export default new AuthService();
export default new ApplyJobService()
export default new JobService()
export default ApplyJob
import React,{Component} from "react";
import "./App.css";
import "bootstrap/dist/css/bootstrap.min.css";
import AuthService from "./service/auth.service";
import Login from "./Component/login.component";
import Register from "./Component/register.component";
import Home from "./Component/home.component";

import Profile from "./Component/profile.component";
import BoardUser from "./Component/board-user.component";
import BoardModerator from "./Component/board-moderator.component";
import BoardAdmin from "./Component/board-admin.component";
import {BrowserRouter as Router,Switch,Route,Link} from "react-router-dom";
import JobProfile from "./Component/JobProfile";
import AddJob from "./Component/AddJob";
import ViewJob from "./Component/ViewJob";
import STUDENTComponent from "./Component/STUDENTComponent";
import AddSTUDENT from "./Component/AddSTUDENT";
import ViewStudComponent from "./Component/ViewStudComponent";
import JobStud from "./Component/JobStud";
import TPOComponent from "./Component/TPOComponent";
import AddTpoComponent from "./Component/AddTpoComponent";
import ViewTPO from "./Component/ViewTPO";
import { Navbar } from "react-bootstrap";
import ApplyJob from "./Component/ApplyJob";
import upload from "./Component/upload-file.component";
import ContactUs from "./Component/ContactForm";
import UploadFiles from "./Component/upload-files";
class App extends Component {
constructor(props) {
super(props);
this.logOut = this.logOut.bind(this);
this.state = {
showModeratorBoard: false,
showAdminBoard: false,
currentUser: undefined,
};
}
componentDidMount() {

const user = AuthService.getCurrentUser();

if (user) {
this.setState({
currentUser: user,
showModeratorBoard: user.roles.includes("ROLE_MODERATOR"),
showAdminBoard: user.roles.includes("ROLE_ADMIN"),
showUserBoard: user.roles.includes("ROLE_USER"),
});
}
}
logOut() {
AuthService.logout();
}
render() {
const { currentUser, showModeratorBoard, showAdminBoard,showUserBoard } = this.state;
return (
<div>
<Router>
<nav className="navbar navbar-expand navbar-dark bg-dark">
<Link to={"/"} className="navbar-brand">

<img style={{marginLeft:"50px"}}src="https://www.allschoolscolleges.com/education-
crm/images/partner/CU.jpg"height="70px" width="70px"/>

CUTM
</Link>
<Navbar.Toggle aria-controls="responsive-navbar-nav" />

<div className="navbar-nav mr-auto" >
<li className="nav-item">
<Link to={"/home"} className="nav-link">
Home

</Link>
</li>
{showModeratorBoard && (
<li className="nav-item">
<Link to={"/mod"} className="nav-link">
TPO Board
</Link>
</li>
)}
{showModeratorBoard && (
<li className="nav-item">
<Link to={"/job"} className="nav-link">
JobProfile
</Link>
</li>
)}
{showAdminBoard && (
<li className="nav-item">
<Link to={"/admin"} className="nav-link">
Admin Board
</Link>
</li>
)}
{showAdminBoard && (
<li className="nav-item">
<Link to={"/job"} className="nav-link">
JobProfile
</Link>
</li>
)}
{showAdminBoard && (

<li className="nav-item">
<Link to={"/STUDENT"} className="nav-link">
Student
</Link>
</li>
)}
{showAdminBoard && (
<li className="nav-item">
<Link to={"/TPO"} className="nav-link">
TPO
</Link>
</li>
)}

{showUserBoard && (
<li className="nav-item">
<Link to={"/JobProfStud"} className="nav-link">
JobProfile
</Link>
</li>
)}
{showUserBoard && (
<li className="nav-item">
<Link to={"/documents"} className="nav-link">
MyDocuments
</Link>
</li>
)}
<div className="navbar-nav mr-auto" >
<li className="nav-item">
<Link to={"/contactus"} className="nav-link">

ContactUs
</Link>
</li>
</div>
{/* {currentUser && (
<li className="nav-item">
<Link to={"/user"} className="nav-link">
User
</Link>
</li>
)} */}
</div>
{currentUser ? (
<div className="navbar-nav ml-auto">
<li className="nav-item">
<Link to={"/profile"} className="nav-link">
{currentUser.username}
</Link>
</li>
<li className="nav-item">
<a href="/login" className="nav-link" onClick={this.logOut}>
LogOut
</a>
</li>
</div>
) : (
<div className="navbar-nav ml-auto">
<li className="nav-item">
<Link to={"/login"} className="nav-link">
Login
</Link>

</li>
<li className="nav-item">
<Link to={"/register"} className="nav-link">
Sign Up
</Link>
</li>
</div>
)}
</nav>
<div className="container mt-3">
<Switch>
<Route exact path={["/", "/home"]} component={Home} />
<Route exact path="/login" component={Login} />
<Route exact path="/register" component={Register} />
<Route exact path="/profile" component={Profile} />
{/* <Route path="/user" component={BoardUser} /> */}
<Route path="/user" component={JobStud} />
<Route path="/job" component={JobProfile} />
<Route path="/documents" component={upload} />
<Route path="/upload" component={UploadFiles} />
<Route path="/contactus" component={ContactUs} />
<Route path="/JobProfStud" component={JobStud} />
<Route path='/add-job/:id' component={AddJob} />
<Route path = "/view-job/:id" component={ViewJob} />
<Route path='/STUDENT' component={STUDENTComponent} />
<Route path='/add-STUDENT/:id' component={AddSTUDENT} />
<Route path='/view-STUDENT/:id' component={ViewStudComponent} />
<Route path="/TPO" component={TPOComponent} />
<Route path='/add-TPO/:id' component={AddTpoComponent} />
<Route path="/admin" component={BoardAdmin} />
<Route path='/view-TPO/:id' component={ViewTPO} />

<Route path="/mod" component={BoardModerator} />
<Route path="/apply" component={ApplyJob} />
</Switch>
</div>
</Router>
</div>

);
}
}
export default App;
Project Screenshot

STUDENT LOGIN

TRAINING PLACEMENT LOGIN

ADMIN LOGIN

CONCLUSION
