# Long short-term memory

An LSTM is a RNN without the vanishing gradient problem. It introduces a cell state for. It is defined by

\[\begin{eqnarray}
f_t & = & \sigma(W_f \cdot x_t + U_f \cdot h_{t-1} + b_f) \\
i_t & = & \sigma(W_i \cdot x_t + U_i \cdot h_{t-1} + b_i) \\
o_t & = & \sigma(W_o \cdot x_t + U_o \cdot h_{t-1} + b_o) \\
\tilde{c}_t & = & \tanh(W_c \cdot x_t + U_c \cdot h_{t-1} + b_c) \\
c_t & = & f_i \circ c_t + i_i \circ \tilde{c}_t \\
h_t & = & o_t \circ \tanh(c_t)
\end{eqnarray}\]

There exists different flavors of the LSTM, e.g. peephole LSTM or LSTM without a forget gate.