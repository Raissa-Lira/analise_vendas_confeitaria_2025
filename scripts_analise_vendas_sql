 -- 1. Total vendido por produto e mês
SELECT Produto, strftime('%Y-%m', Data) AS Mes, SUM(Quantidade) AS TotalVendida
FROM vendas
GROUP BY Produto, Mes
ORDER BY TotalVendida DESC;

-- 2. Total vendido por cidade e produto
SELECT Cidade, Produto, SUM(Quantidade) AS Total
FROM vendas
GROUP BY Cidade, Produto
ORDER BY Cidade, Total DESC;

-- 3. Média mensal de vendas por produto
SELECT Produto, AVG(Mensal) AS MediaMensal FROM (
    SELECT Produto, strftime('%Y-%m', Data) AS Mes, SUM(Quantidade) AS Mensal
    FROM vendas
    GROUP BY Produto, Mes
) GROUP BY Produto
ORDER BY MediaMensal DESC;
