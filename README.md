# Modelo-ER
SELECT 
    G.Nome_Gravadora,
    C.Nome_CD,
    F.Numero_Faixa,
    M.Nome_Musica,
    M.Duracao
FROM GRAVADORA G
JOIN CD C ON G.Codigo_Gravadora = C.Codigo_Gravadora
JOIN FAIXA F ON C.Codigo_CD = F.Codigo_CD
JOIN MUSICA M ON F.Codigo_Musica = M.Codigo_Musica
ORDER BY C.Nome_CD, F.Numero_Faixa;

SELECT 
    M.Nome_Musica,
    A.Nome_Autor
FROM MUSICA M
JOIN MUSICA_AUTOR MA ON M.Codigo_Musica = MA.Codigo_Musica
JOIN AUTOR A ON MA.Codigo_Autor = A.Codigo_Autor
ORDER BY M.Nome_Musica;

SELECT 
    C.Nome_CD,
    C.Preco_Venda,
    CAT.Codigo_Categoria AS Categoria_Preco
FROM CD C, CD_CATEGORIA CAT
WHERE C.Preco_Venda BETWEEN CAT.Menor_Preco AND CAT.Maior_Preco;
SELECT 
    C1.Nome_CD AS CD_Principal,
    C2.Nome_CD AS CD_Recomendado
FROM CD C1
LEFT JOIN CD C2 ON C1.CD_Indicado = C2.Codigo_CD;
