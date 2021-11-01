    auto field = std::vector<std::vector<char>>();
    field.push_back(std::vector<char>({'0','0','1','b','1','0','1','1'}));
    field.push_back(std::vector<char>({'0','1','2','2','1','0','1','b'}));
    field.push_back(std::vector<char>({'0','1','b','1','0','0','1','1'}));
    field.push_back(std::vector<char>({'0','1','1','1','0','0','0','0'}));
    field.push_back(std::vector<char>({'2','2','1','0','1','1','2','1'}));
    field.push_back(std::vector<char>({'?','?','1','0','1','?','3','?'}));
    field.push_back(std::vector<char>({'3','3','3','1','2','2','?','2'}));
    field.push_back(std::vector<char>({'?','?','?','?','?','?','?','?'}));


    auto solver = MineSweeper(field);

    for (int i = 0; i < 8; i++) {
        for (int j = 0; j < 8; j++) {
            if (field[i][j] == '?') {
                if(solver.query(i,j) == SAFE) {
                    std::cout << "Row " << i << ", Col " << j << " " << SAFE << std::endl;
                } else {
                    std::cout << "Row " << i << ", Col " << j << " " << BOOM << std::endl;
                }
            }
        }
    }

    
    
результат

Строка 5, Столбец 0 Стрела, 
Стрела 5, Колонка 1, Стрела, 
Стрела 5, Колонка 5, Стрела, 
Строка 5, Стрела 7, Стрела, 
Строка 6, Колонка 6, Стрела, 
Строка 7, Колонка 0, Стрела 
7, Колонка 1, Стрела, 
Строка 7, Колонка 2, БЕЗОПАСНАЯ, 
Строка 7 , Столбец 3 Стрела, 
Стрела 7, Столбец 4 БЕЗОПАСНЫЙ, 
Ряд 7, Столбец 5, БЕЗОПАСНЫЙ, 
Ряд 7, Столбец 6, БЕЗОПАСНЫЙ, 
Ряд 7, Столбец 7, БЕЗОПАСНЫЙ
