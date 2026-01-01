# Modelo-ER
SELECT      M.Nome_Musica,     A.Nome_Autor FROM MUSICA M JOIN MUSICA_AUTOR MA ON M.Codigo_Musica = MA.Codigo_Musica JOIN AUTOR A ON MA.Codigo_Autor = A.Codigo_Autor ORDER BY M.Nome_Musica;
