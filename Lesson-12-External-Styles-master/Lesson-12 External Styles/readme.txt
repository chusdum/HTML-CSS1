inline -> <tag style="css"></tag>
global -> <head><style></style></head>
external ->
        page.html -----> <style class="css">
        
        
        style.css
        =============
            selector1{
            propr:val;
            }
            selector2{
                propr:val;
            }
        page.html
            ----------------
            head
            --> <link rel"stylesheet" href="style.css" />

================================================================================
CSS PRYORITY / CSS SPECIFICITY
1. element <---- style1,style2,style3....
            li{
                color:red;
            }
            .....
            li{
            color:red;
            }
    Daca unu si acela-si stil are aceea-si greutate (tag vs tag / class vs class / id vs id) , cel care-i ultimul - cistiga.

2. Simple Priority Rule
    inline > #id> .class > :pseude >tag > parent > default 
Cu cit stilul dat este mai apropiat de element, cu atit este mai prioritar.

3. Complex selectors - cu cit mai mare cifra , cu atit mai prioritar este .
    http://designshack.co.uk/wp-content/uploads/css-specificity-10.jpg
                ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
                ||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||||
    #container .content .col p{
        // 121
    }
    #container div .col p{
        // 112
    }