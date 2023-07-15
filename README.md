contract MyToken {

    // public variables here
string public tokenName="SOLIDITY";
string public tokenAbbrv="SLIDTY";
uint public totalSupply=0;

    // mapping variable here
    mapping(address => uint) public balances;

    // Mint function
    function mint(address recipient, uint value) public {
        totalSupply += value;
        balances[recipient] += value;
    }
    
    // burn function
function burn(address add, uint val) public {
        if (balances[add] >= val){
        totalSupply -= val;
        balances[add] -= val; 
        }
    }
}
