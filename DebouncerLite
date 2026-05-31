module DebouncerLite(
    input clk,
    input rst,
    input noisy_in,
    output reg clean_out
);

reg [2:0] count;

always @(posedge clk or posedge rst) begin
    if (rst) begin
        count <= 0;
        clean_out <= 0;
    end
    else begin
        if(noisy_in) begin
            if(count < 3)
                count <= count + 1;
            else
                clean_out <= 1;
        end
        else begin
            count <= 0;
            clean_out <= 0;
        end
    end
end

endmodule
