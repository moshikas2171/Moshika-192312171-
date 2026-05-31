module RotatorUnit(
    input clk,
    input rst,
    input dir,
    input [7:0] data_in,
    output reg [7:0] data_out
);

always @(posedge clk or posedge rst) begin
    if(rst)
        data_out <= data_in;
    else begin
        if(dir)
            data_out <= {data_out[6:0], data_out[7]};
        else
            data_out <= {data_out[0], data_out[7:1]};
    end
end

endmodule
