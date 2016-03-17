FIND_PATH=-I/home/insist_crazy/Bit/Linux/httpd/tinyhttpd/sql_connect -I/home/insist_crazy/Bit/Linux/httpd/tinyhttpd/sql_connect/mysql_lib/include -L/home/insist_crazy/Bit/Linux/httpd/tinyhttpd/sql_connect/mysql_lib/lib -lmysqlclient

.PHONY:all
all:math_cgi show_student_cgi register_cgi
math_cgi:math_cgi.c
	gcc -o $@ $^
show_student_cgi:show_student_cgi.cpp /home/insist_crazy/Bit/Linux/httpd/tinyhttpd/sql_connect/sql_connect.cpp 
	g++ -o $@ $^ $(FIND_PATH) -g

register_cgi:register_cgi.cpp /home/insist_crazy/Bit/Linux/httpd/tinyhttpd/sql_connect/sql_connect.cpp 
	g++ -o $@ $^ $(FIND_PATH)


.PHONY:output
output:
	cp math_cgi ../../output/htdocs/cgi_bin 
	cp show_student_cgi ../../output/htdocs/cgi_bin
	cp register_cgi ../../output/htdocs/cgi_bin

.PHONY:clean
clean:
	rm -rf math_cgi show_student_cgi register_cgi
