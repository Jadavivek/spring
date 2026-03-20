//	@RequestMapping("/home2")
//	  public String home2(String name,HttpSession session)
//	{
//		System.out.println("welcome"+ name);
//		
//		session.setAttribute("name", name);
//	  	return "home2";   
//	  }
	
	
	//@RequestParam -used to get values from the URL(Query Paramter)
//	@RequestMapping("/home2")
//	public String home2(@RequestParam("name") String myName,HttpSession session)
//	{
//		System.out.println("welcome"+ myName);
//		
//		session.setAttribute("name", myName);
//	  	return "home2";   
//	 }
	
	
	//passing data to view(jsp) using Model only
	@RequestMapping("/home2")
	public String home2(@RequestParam("name") String name,Model model)
	{
		System.out.println("welcome"+ name);
		
		model.addAttribute("username",name);   //setting data to Model insted of session
	  	return "home2";   
	 }
 
