# PgnToGif
<a href="https://developer.android.com" target="_blank"><img src="https://img.shields.io/badge/Android-3DDC84?style=flat-square&logo=Android Studio&logoColor=white"/></a>
<a href="https://developer.android.com" target="_blank"><img src="https://img.shields.io/badge/intellijidea-000000?style=flat-square&logo=intellijidea&logoColor=white"/></a>
<a href="https://developer.android.com" target="_blank"><img src="https://img.shields.io/badge/apachemaven-C71A36?style=flat-square&logo=apachemaven&logoColor=white"/></a>
<a href="https://developer.android.com" target="_blank"><img src="https://img.shields.io/badge/Gradle-02303A?style=flat-square&logo=Gradle&logoColor=white"/></a>

![test](https://github.com/user-attachments/assets/cfaab0ea-98a3-492c-8943-e5f55b9863ec)


stable version :  '2.0.6'

## Introduction
hello everyone, CHESSX2_PGNPARSER is java library for programming service for controlling PGN data
(if you want to know about PGN format detailiy, please check https://www.chess.com/terms/chess-pgn)

maven server : https://central.sonatype.com/artifact/io.github.profrog/chessx2/overview  


## Setting  
Gradle  

    implementation group: 'io.github.profrog', name: 'chessx2', version: {stable version}

OR, you can mirror file following mirror branch
    
    git clone https://github.com/Profrog/chessx2_pgnparser.git -b mirror


User service simple example    
   
    package org.example;
    import io.github.profrog.PgnParse;

    public class main {
    
        public static String pgn_example = "\n" +
                "[Event \"Live Chess\"]\n" +
                "[Site \"Chess.com\"]\n" +
                "[Date \"2024.03.23\"]\n" +
                "[Round \"?\"]\n" +
                "[White \"MagicRoss\"]\n" +
                "[Black \"PFchessX2\"]\n" +
                "[Result \"0-1\"]\n" +
                "[ECO \"D02\"]\n" +
                "[WhiteElo \"1139\"]\n" +
                "[BlackElo \"1150\"]\n" +
                "[TimeControl \"120+1\"]\n" +
                "[EndTime \"19:04:44 PDT\"]\n" +
                "[Termination \"PFchessX2 won by checkmate\"]\n" +
                "\n" +
                "1. d4 d5 2. Nf3 Nc6 3. e3 Bf5 4. Bb5 a6 5. O-O e6 6. Bxc6+ bxc6 7. c3 Bd6 8. Re1 " +
                "Nf6 9. h3 h6 10. Nh4 Bh7 11. g4 Ne4 12. Nd2 Qxh4 13. Nxe4 Bxe4 14. f3 Qg3+ 15. " +
                "Kf1 Bxf3 16. Qd2 Qxh3+ 17. Kg1 Qh1+ 18. Kf2 Qg2# 0-1\n";
    
        public static String pgn_example2 = "\n" +
                "[Event \"Casual 긴 대국 game\"]\n" +
                "[Site \"https://lichess.org/3FLP6aWA\"]\n" +
                "[Date \"2024.04.02\"]\n" +
                "[White \"lichess AI level 1\"]\n" +
                "[Black \"profrog\"]\n" +
                "[Result \"0-1\"]\n" +
                "[UTCDate \"2024.04.02\"]\n" +
                "[UTCTime \"14:59:54\"]\n" +
                "[WhiteElo \"?\"]\n" +
                "[BlackElo \"1500\"]\n" +
                "[Variant \"Standard\"]\n" +
                "[TimeControl \"-\"]\n" +
                "[ECO \"C44\"]\n" +
                "[Opening \"Ponziani Opening\"]\n" +
                "[Termination \"Normal\"]\n" +
                "[Annotator \"lichess.org\"]\n" +
                "\n" +
                "1. e4 e5 2. Nf3 Nc6 3. c3 { C44 Ponziani Opening } Qf6 " +
                "4. d4 exd4 5. cxd4 Bb4+ 6. Ke2 Nh6 7. Nc3 Ng4 8. a3 Nxd4+ 9. Kd2 Bxc3+ 10. Kd3 Nxf2+ " +
                "11. Kc4 Nxd1 12. Rb1 b5+ 13. Kd5 Bb7+ 14. Kc5 d6# { Black wins by checkmate. } 0-1\n";
    
    
        public static void main(String[] args){
            String dir0 = "/home/mingyu/Pictures/chess";
            List<int[][]> alpa =  PgnParse.parserInit(pgn_example,0,0);
            String input_dir = PgnToImage.imageInit(alpa,dir0);

            ImageToGif.gifInit(dir0 + "/test.gif", input_dir, 1000);
        }
    
    }

## Detailed Feature

![Screenshot from 2024-05-12 02-34-24](https://github.com/Profrog/chessx2_pgnparser/assets/26535065/22a8d4cc-79bf-4fbb-bf0e-68187d495a5a)



for more detail information check that link
https://www.javadoc.io/doc/io.github.profrog/chessx2/latest/io/github/profrog/package-summary.html


## USER GUIDE(KOREAN)  
refer to 
https://blog.naver.com/ache159/223512620639
video : https://www.youtube.com/watch?v=tjTLnJ-7wKw  


  
