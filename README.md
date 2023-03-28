A cross-platform streaming parser for the ESRI Shapefile spatial data
format.

This parser implementation is based on the
[ESRI Shapefile Technical Description](http://www.esri.com/library/whitepapers/pdfs/shapefile.pdf),
[dBASE Table for ESRI Shapefile (DBF)](http://www.digitalpreservation.gov/formats/fdd/fdd000326.shtml)
and
[Data File Header Structure for the dBASE Version 7 Table File](http://www.dbase.com/Knowledgebase/INT/db7_file_fmt.htm).

**shapefile.Reader**  
**\- open(String filepath)**: Mở tệp Shapefile và trả về một đối tượng Reader.  
**\- read():** Đọc các bản ghi từ tệp Shapefile và trả về một danh sách các đối tượng Shape.  
**shapefile.Shape**  
**\- getType()**: Trả về kiểu hình dạng của đối tượng Shape (point, polyline, polygon, multipoint, or null).  
**\- getShape():** Trả về tất cả các đối tượng hình dạng (Point, Polyline, Polygon hoặc MultiPoint) như là một List\<dynamic>.  
**\- toJson():** Chuyển đổi đối tượng Shape thành định dạng JSON.  
**shapefile.Point**  
**\- getX():** Trả về tọa độ x của điểm.  
**\- getY():** Trả về tọa độ y của điểm.  
**\- getZ():** Trả về giá trị Z của điểm.  
**\- getM():** Trả về giá trị M của điểm.  
**shapefile.Polyline và shapefile.Polygon**  
**\- getParts():** Trả về một List\<int> chứa các chỉ mục của điểm bắt đầu của các phần khác nhau của Polyline hoặc Polygon.  
**\- getPoints()**: Trả về một List\<Point> chứa tất cả các điểm trong Polyline hoặc Polygon.  
**shapefile.Writer**  
**\- create(String filepath, int type):** Tạo tệp Shapefile mới với kiểu hình dạng được chỉ định và trả về một đối tượng Writer.  
**\- addField(String name, String type, {int size = 0, int decimal = 0}):** Thêm một trường mới vào tệp Shapefile.  
**\- addRecord(List\<dynamic> shapes, List\<dynamic> data):** Thêm một bản ghi mới vào tệp Shapefile.
