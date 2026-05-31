module EvenOddFSM(
    input clk,
    input rst,
    input [7:0] number,
    output reg even
);

always @(posedge clk or posedge rst) begin
    if (rst)
        even <= 1'b1;
    else
        even <= ~number[0];
end

endmodule
