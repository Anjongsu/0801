# JSP 

### 순서
    인코딩 
    Tocat연결
    Orace DB연결
    테이블 , 값 생성
    ( DB생성 ) 
    
### DB 
    class DB{
        public static Connection getDB() throws Exception{  // DB 연결 
              Class.forName(?);
              Connection con = ?????;
              return con;
        }
        
        public static ReseultSet fetchAll(String sql,String[] list) throws Exception{ // 데이터 불러오기
              Connection con = getDB();
              ResultSet rs = con.prepareStatement(sql).execute();
              return rs;
        }
        
        public static void exec(String sql,String[] list) throws Exception{ // insert,update,delete 메소드
             try{
                Connection con = getDB();
                PrepareStatement pstmt = con.prepareStatement(sql);
                int count = 1;
                for(String value: list){
                    pstmt.setString(count,value);
                }
                pstmt.executeQuery();
             }catch(Exception e){ // 에러가 뜰시 값이 잘못 입력되었습니다. 라고 뜨고 이전 페이지로 이동한다.
                out.println("<script>alert('값이 잘못 입력되었습니다.'); history.back(); </script>");
             }
        } 
    }

### JSP 기본문법
    <%@ page import="" %>  ( Java , Package 불러올때 ) 
    <%@ include file="" %> ( JSP 파일을 불러 올때 )
    <%!  public static class DB{  }  %>  ( Java 코드 적는곳 ) 
    request.getParameter(이름)  ( Form 값 가져오기 ) 
### 막는거 
    update문에서 primary key 키 값은 변경되면 안됨  <input readonly>
    form = document.test
    form.addEventListener("submit",function(e){
        e.preventDefault();
        if ( form.name.value.trim() == "" ){  //  trim 공백을 제거라 
            alert("name 값이 비어있습니다.");
            return form.name.focus()
        }else if( form.price.value.trim() == ""){
            alert("price 값이 비어있습니다.");
            return form.price.focus()
        }else{
            form.submit();
        }
    })
### Action.jsp  ( Form  을 무조건 POST )  
#### <form action="Action.jsp?Type=값" method="post" name="test"> 
    String type = request.getParameter("Type");
    switch(type){
        case "insert":
           String insert[] = { }
        break;
        case "update":
                
        break;
        
    }
