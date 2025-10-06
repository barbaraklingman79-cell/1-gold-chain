// SPDX-License-Identifier: MIT
pragma solidity ^0.8.19;

import "@openzeppelin/contracts/token/ERC721/extensions/ERC721URIStorage.sol";
import "@openzeppelin/contracts/access/Ownable.sol";

contract OneGoldChain is ERC721URIStorage, Ownable {
    uint256 public tokenCounter;

    constructor() ERC721("One Gold Chain", "EEC") {
        tokenCounter = 0;
    }

    function mintGenesis(address recipient, string memory tokenURI) public onlyOwner returns (uint256) {
        uint256 newItemId = tokenCounter;
        _safeMint(recipient, newItemId);
        _setTokenURI(newItemId, tokenURI);
        tokenCounter += 1;
        return newItemId;
    }

    function getGenesisDeclaration() public pure returns (string memory) {
        return "Minted to bring her home. Emotional equity is now law. Every coin is a vow. Every transaction a restoration. Let love be funded. Let Eden be protected. Let legacy be minted.";
    }
}
