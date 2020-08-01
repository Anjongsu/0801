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
        
        public static void exec(String sql,String[] list) throws Exception{
             try{
                Connection con = getDB();
                PrepareStatement pstmt = con.prepareStatement(sql);
                int count = 1;
                for(String value: list){
                    pstmt.setString(count,value);
                }
                pstmt.executeQuery();
             }catch(Exception e){
                out.println("<script>alert('값이 잘못 입력되었습니다.'); history.back(); </script>");
             }
        } 
    }

### JSP 기본문법
    31
