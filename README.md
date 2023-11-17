# table2latex

## Instalation
Download form https://www.mathworks.com/matlabcentral/fileexchange/155182-table2latex and add it to your Matlab path.

## Description
This function is able to generate latex function from same syntax as Matlab table has.

Defaul formating for latex table is left align.

Defaul formating for numbers is two digits.


## Example

T = table(Model,R2,RMSE,MSE)

latexTable = table2latex(Model,R2,RMSE,MSE)

Output:

    Model      R2        RMSE      MSE  
    _____    _______    ______    ______
    "SP"      0.8872    40.622    1650.1
    "ESP"    0.93557    30.702    942.61
    "LP"     0.91596    35.016    1223.3
    "ELP"    0.98761    13.194    174.08

    latexTable =
        '\begin{table}
            \centering
                \begin{tabular}{llll}
                    \textbf{Model} & \textbf{R2} & \textbf{RMSE} & \textbf{MSE}\\
                    $SP$ & $0.887$ & $40.622$ & $1650.109$ \\
                    $ESP$ & $0.936$ & $30.702$ & $942.608$ \\
                    $LP$ & $0.916$ & $35.016$ & $1223.294$ \\
                    $ELP$ & $0.988$ & $13.194$ & $174.083$ 
                \end{tabular}
        \end{table}'

## Add custom formating

format = '%0.2f';\
align = 'c';\
latexTable = table2latex(Model, R2, RMSE, MSE, format, align)