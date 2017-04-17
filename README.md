###3. Sử dụng Model: - ->where("row",$args)	: Tương đương câu lệnh where row = $args. 
 ->where("row",$args,"LIKE")	: Tương đương câu lệnh LIKE (Có thể thay LIKE) 
 ->orderBy("asc",$args)	: Tương đương câu lệnh sắp xếp 
 ->join("TABLE1","TABLE1.row = TABLE2.row","LEFT") : Tương đương câu lệnh JOIN (Có thể thay thế INNER JOIN ,RIGHT)
 ->num_rows()	: Lấy ra tổng số record - ->get()	: Lấy tất cả record
 ->get(null,null,$select)	: 3 Tham số $select = Tên row trong table 
 ->getOne()	: Lấy 1 record - ->delete()	: Xóa record 
 ->insert($data)	: Thêm record, $data = array( "row" => $row ) 
 ->update($data) : Cập nhật record, $data = array( "row" => $row ) 
 ->rawQuery($sql)	: Thực thi trực tiếp câp lệnh SQL 
 
 ###4. Các function hay sử dụng: - base_url() : base_url() tương đương với url gốc, giống codigniter - redirect($url)	: điều hướng tang web, nếu bên trong biến $url = "current" thì là bạn đang F5 trang web, còn ko bạn có thể truyền url vào bt để chuyển sang trang khác - lang($key) : dùng để xử lý đa ngôn ngữ, bên trong là $key, để xử lý vào trong thư mục App/lang/ngôn ngữ/main.php bạn có thể truyền $key vào - alias($string)	: chuyển chuỗi Unicode sang kiểu url chuẩn. - dd($array) : là hàm dùng để dump mảng. - createCaptcha() : Tạo mã Captcha. - checkCaptcha($input)	: Kiểm tra mã Captcha có chính xác ko. - getIp() : lấy địa chỉ IP client. - base64url_encode($var): mã hóa base 64. - base64url_decode($var): giải mã base 64. - recursiveMenu($data,$parent=0,$count=0) : Đệ quy menu : + trước khi dùng hàm này thì tạo ra một biến mới đặt tên là $data = array(); + loop vòng lặp mảng cũ, đặt parent id = key của $data mới(Tức là gom parent id chung lại) foreach ($_web['menu'] as $value) { $parent = $value['parent_id']; $data[$parent][] = $value; }

###5. Tích hợp thư viện mới: - Mở file composer.json thêm vào reuired: tên thư viện sau đó chạy lệnh php composer self-update

###6. Biến toàn cục: - $_web	: Có thể sử dụng được ở bất kỳ đâu trên trang web var_dump($_web) để xem
