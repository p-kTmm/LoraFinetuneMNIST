# LoraFinetuneMNIST
Lora finetune on my own model


\documentclass{standalone}
\usepackage{tikz}
\usepackage{amsmath}

\begin{document}

\begin{tikzpicture}

    % Tô màu vùng polytope {Ay <= b}
    \fill[blue!10] (2,3) -- (4,4) -- (4,0) -- (2,0) -- cycle;

    % Vẽ trục tọa độ
    \draw[->, thick] (0,0) -- (0,4) node[left] {\(z\)};
    \draw[->, thick] (0,0) -- (5,0) node[below] {\(\eta^T y\)};
    
    % Vẽ V^-(z) và V^+(z)
    \draw[dotted] (2,0) -- (2,4);
    \node[below] at (2,0) {\(V^-(z)\)};
    
    \draw[dotted] (4,0) -- (4,4);
    \node[below] at (4,0) {\(V^+(z)\)};
    
    % Vẽ đường chiếu của y xuống eta^T y
    \draw[thick] (0,0) -- (4,3) node[above] {\(y\)};
    \draw[dashed, thick, red] (0,0) -- (4,0);
    
    % Vẽ nhãn cho \eta
    \node[below right] at (2.2,0.2) {\(\eta\)};
    
    % Nhãn cho {Ay <= b}
    \node at (3,3.6) {\(\{Ay \leq b\}\)};
    
\end{tikzpicture}

\end{document}
