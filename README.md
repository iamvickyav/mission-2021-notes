# Mission 2021

HTTP Basics, HTML, CSS - Bootstarp + Grid (12), JQuery, Templates, Spring Boot -> RestController, JDBCTemplate, Service

IntelliJ, VS Code (Live Server Plugin), MySQL Workbench 

Postman

## HTTP 

	Protocol - Rules
	
	REQUEST

		- URL 
			- PATH VARIABLE
			- QUERY PARAM
		- HEADER
		- Method - GET, POST, PUT, DELETE
		- BODY - JSON

	RESPONSE

		- HEADER
		- STATUS - 200, 201, 404
		- BODY - JSON


## BACKEND APPLICATION (Middleware)

	- Java + Spring Boot

	SPRINT BOOT

		- @RestController

			Annotations

				- @Autowired (HAS A)
				- @RequestMapping
				- @PathVariable
				- @RequestParam

			ResponseEntity

		- @Service

		- @Repository

			JDBCTemplate

		application.properties

			spring.datasource.url=jdbc:mysql://localhost:3306/itech_db
			spring.datasource.username=root
			spring.datasource.password=rootroot

	POSTMAN

		- TOOL to test Backend application

## FRONT END APPLICATION 

	HTML with VSCode - Live Server Plugin

		table, th, tr, td
		h1 to h6
		img
		ol, ul, li
		button
		input type text
		input type checkbox

	CSS

		. (class)
		# (id)

		How to load as separate file - CSS - <link>

		BOOTSTRAP

			- Version 4

			CDN URL

			Navigation bar
			Image from awesomefont <i>

		Border
		Grid - 12
		Span vs Div
		Margin vs Padding

	Javascript (vanilla Javascript)

		HTML render - DOM - Access, Change -> Javascript

		Function, var, document.getElementById(), innerHTML, value

	JQuery (javascript library)

		$("")

		queryselector with template

		hide/show, toggle

	AJAX (To make call to backend URLs asynchronously)

		$.ajax({})
