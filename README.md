# Thomas algorithm
Реализация алгоритма Томаса (метода прогонки) для трехдиагональной матрицы

## Постановка задачи
Дана система линейных алгебраических уравнений
$$ Au = B, $$
где $A$ — трехдиагональная матрица такая, что
$$
    A = \begin{pmatrix}
        \beta_0 & \alpha_0 & 0 & 0 & 0 & \dots & 0 \\
        \gamma_1 & \beta_1 & \alpha_1 & 0 & 0 & \dots & 0 \\
        0 & \gamma_2 & \beta_2 & \alpha_2 & 0 & \dots & 0 \\
        0 & 0 & \gamma_3 & \beta_3 & \alpha_3 & \dots & 0 \\
        \dots & \dots & \dots & \dots & \dots & \dots & \dots \\
        0 & 0 & 0 & 0 & \gamma_{N-2} & \beta_{N-2} & \alpha_{N-2} \\
        0 & 0 & 0 & 0 & \gamma_{N-1} & \beta_{N-1} & \alpha_{N-1}
    \end{pmatrix},
$$
столбцы неизвестных и свободных членов соответственно:
$$ u = \begin{pmatrix}
        u_0 \\ u_1 \\ \dots \\ u_{N-1}
    \end{pmatrix}, \quad
    B = \begin{pmatrix}
        B_0 \\ B_1 \\ \dots \\ B_{N-1}
    \end{pmatrix}.
$$

Считаем, что $\gamma_0$ и $\alpha_{N-1}$ равны нулю.

Найти решение данной системы.