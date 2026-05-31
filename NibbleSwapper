module NibbleSwapper(
    input [7:0] data_in,
    input swap_en,
    output reg [7:0] data_out
);

always @(*) begin
    if (swap_en)
        data_out = {data_in[3:0], data_in[7:4]};
    else
        data_out = data_in;
end

endmodule
