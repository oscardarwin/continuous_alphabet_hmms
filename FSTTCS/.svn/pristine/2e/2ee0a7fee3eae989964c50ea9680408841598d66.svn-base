const N := 10;   
const Bits := 4 ;
m :int%N, inc:com |-
var%2 exponent[Bits] = [0,1,0,1];
com power(x:int%N) {
	var%N s := 1;
	var%N R;
	for(var%(Bits + 1) k; k < Bits; ++k) do {
		R:=s;
		if(exponent[k]) then {
			R := R*x;
			if(5<=R) then { inc; inc } else { inc }
		}
		s := R*R;
	}
}
var%N message := m*rand[N];
power(message) : com
