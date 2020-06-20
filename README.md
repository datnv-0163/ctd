ctd

bai 2: source Badung

token.h
Thêm SB_EXP vào enum TokenType

token.c

Thêm case SB_EXP vào tokenToString()

scanner.c

Thêm case SB_EXP vào printToken()
Sửa lại case CHAR_TIMES trong ham getToken

parser.c

Thêm case SB_EXP vào compileTerm2 => Đọc lại văn phạm.
De uu doc duoc ca truong hop nhu 2**(2*n) ta phai sua lai ham compileFactor(them truong hop sb_lpar)

bai 3:Ba Dung

token.h

Thêm KW_SWITCH, KW_CASE, KW_DEFAULT, KW_BREAK vào enum TokenType
Sửa lại KEYWORDS_COUNT = 24(trong code la 26 vi bai 4 them ca string voi double) => Thêm 4 keyword mới vào Token

token.c

Thêm các keyword mới vào struct keywords[]
Thêm case của keyword vào tokenToString()

scanner.c

Thêm case của keyword mới vào printToken();

parser.h

Thêm định nghĩa hàm compileSwitchSt(); cai nay la lam theo van pham dau bai cho

parser.c


Thêm case KW_SWITCH vào complileStatement => Đọc thêm văn phạm mới.
Thêm case KW_BREAK, KW_DEFAULT, KW_CASE vào compileStatement() => Follow của compileStatement(); (Sau khi compileStatement thì nó sẽ gặp những case này thì sẽ bỏ qua không xử lý Statement).
Thêm case KW_BREAK, KW_DEFAULT, KW_CASE, KW_BEGIN vào hàm compileExpression3() và hàm compileTerm2()=> Follow của hàm compileExpression(); Sau khi compileExpression() ở switch thì nó sẽ gặp những case này cần bỏ qua.
Viết thêm hàm compileSwitchSt();
