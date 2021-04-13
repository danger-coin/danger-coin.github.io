## Danger Funds Token

Danger Funds Token or DND are community-driven projects on #BSC with its deflationary function, 6% locked to liquidity - 4% redistributed to holders.
Reflection, LP rewards, burn each tx is DND smart contract function, you can cross check our smart contract on [Bscscan](https://bscscan.com)

## Smart Contract

Shorten version, you can directly match our smart contracts on [Github](https://github.com/dangertoken/dangertoken.github.io/blob/main/contracts) or [Bscscan](https://bscscan.com)

```markdown

/**
  
   #DangerFundsToken
   
   #DND features:
   6% fee auto add to the liquidity pool to locked forever when selling
   4% fee auto distribute to all holders
   DND Token will deflate itself with each tx
   
/**

   contract DangerFundsToken is Context, IERC20, Ownable {
    using SafeMath for uint256;
    using Address for address;

    mapping (address => uint256) private _rOwned;
    mapping (address => uint256) private _tOwned;
    mapping (address => mapping (address => uint256)) private _allowances;

    mapping (address => bool) private _isExcludedFromFee;

    mapping (address => bool) private _isExcluded;
    address[] private _excluded;
   
    uint256 private constant MAX = ~uint256(0);
    uint256 private _tTotal = 1000000000000000000000000000000;
    uint256 private _rTotal = (MAX - (MAX % _tTotal));
    uint256 private _tFeeTotal;

    string private _name = "Danger Funds Token";
    string private _symbol = "DND";
    uint8 private _decimals = 18;
    
    uint256 public _taxFee = 4;
    uint256 private _previousTaxFee = _taxFee;
    
    uint256 public _liquidityFee = 6;
    uint256 private _previousLiquidityFee = _liquidityFee;

    IUniswapV2Router02 public immutable uniswapV2Router;
    address public immutable uniswapV2Pair;
    
    bool inSwapAndLiquify;
    bool public swapAndLiquifyEnabled = true;
    
    uint256 public _maxTxAmount = 5000000 * 10**6 * 10**9;
    uint256 private numTokensSellToAddToLiquidity = 500000 * 10**6 * 10**9;
    
    event MinTokensBeforeSwapUpdated(uint256 minTokensBeforeSwap);
    event SwapAndLiquifyEnabledUpdated(bool enabled);
    event SwapAndLiquify(
        uint256 tokensSwapped,
        uint256 ethReceived,
        uint256 tokensIntoLiqudity
    );
```

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/dangerfunds/dangerfunds.github.io/settings/pages). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://docs.github.com/categories/github-pages-basics/) or [contact support](https://support.github.com/contact) and we’ll help you sort it out.
