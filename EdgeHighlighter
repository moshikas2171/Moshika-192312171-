module EdgeHighlighter(
    input clk,
    input rst,
    input sig_in,
    output reg rise_pulse,
    output reg fall_pulse
);

reg prev;

always @(posedge clk or posedge rst) begin
    if(rst) begin
        prev <= 0;
        rise_pulse <= 0;
        fall_pulse <= 0;
    end
    else begin
        rise_pulse <= sig_in & ~prev;
        fall_pulse <= ~sig_in & prev;
        prev <= sig_in;
    end
end

endmodule
