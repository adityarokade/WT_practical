# WT_practical

#assignment_6

LoginPage.jsp
<%@ page language="Java" contentType="text/html; charset=ISO-8859-1"
pageEncoding="ISO-8859-1'%>
<!DOCTYPE html>
<html>
<head>
<meta charset="ISO-8859-1'>
<title>login page</title>
</head>
<body>
<form method="post" action=" ‘Logincheck">
<table>
=r
<td>User Name</td>
<td><input type="text"
name="uname"></td>
</tr>
<tr>
<td>password</td>
<td><input type="password"
name="password"></td>
</tr>
<tr>
<td></td>
<td><input type="submit"
name="Login"></td>
</tr>
</table>
</form>
</body>
</html>
Scanne d with CamScannerSuccess.jsp
<%@ page language="Java" contentType=' text/html; charset=ISO-8859-1"
pageEncoding="ISO-8859-1"%>
<!DOCTYPE html>
<html>
<head>
<meta charset="ISO-8859-1'>
<title>Insert title here</title>
</head>
<body>
<hi>
Welcome you are Logged in </h1>
</body>
</html>
error.jsp
<%@ page language="java" contentType= text/html; charset=ISO-8859-1"
pageEncoding= "ISO-8859-1'%>
<!DOCTYPE html>
<html>
<head>
<meta charset="ISO-8859-1'>
<title>Insert title here</title>
</head>
<body>
please Check your
UserName OR password
</body>
</html>
Scanne d with CamScannerServlet Files
LoginCheck. java
import jakarta.servlet.ServletException;
import jakarta.servlet.annotation. WebServlet;
import jJakarta.servlet.http. HttpServlet;
import jakarta.servlet.http. HttpServletRequest;
import jakarta.servlet.http.HttpServletResponse;
import java.io.1[OException;
/**
* Servlet implementation class Logincheck
*/
public class Logincheck extends HttpServlet {
private static final long serialVersionUID = 1L;
/**g
* @see HttpServlet#HttpServlet()
*/
public Logincheck() {
super();
// TODO Auto-generated constructor stub
i
;**
* @see HttpServlet#doGet(HttpServletRequest request, HttpServletResponse
response)
*/
protected void doGet(HttpServletRequest request, HttpServletResponse response)
throws ServletException, IOException {
// TODO Auto-generated method stub
response.getWriter().append("Served at:
").append(request.getContextPath());
f
Scanne d with CamScannerfre
* @see HttpServlet#doPost(HttpServletRequest request, HttpServletResponse
response)
*/
protected void doPost(HttpServletRequest request, HttpServletResponse response)
throws ServletException, IOException ~{
String uname=request.getParameter("uname');
String password=request.getParameter("
password );
if(uname.equals("Arif") && password.equals("9503643167'
))
t
response.sendRedirect("success.jsp");
f
else
t
response.sendRedirect("error.jsp");
f
