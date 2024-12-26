// SPDX-License-Identifier: MIT
pragma solidity ^0.8.0;

import "@openzeppelin/contracts/token/ERC20/ERC20.sol";

contract MyToken is ERC20 {
    constructor(uint256 initialSupply) ERC20("MyToken", "MTK") {
        _mint(msg.sender, initialSupply);
    }
}
use solana_program::{
    account_info::AccountInfo,
    entrypoint,
    entrypoint::ProgramResult,
    program_error::ProgramError,
    pubkey::Pubkey,
};

entrypoint!(process_instruction);

fn process_instruction(
    program_id: &Pubkey,
    accounts: &[AccountInfo],
    instruction_data: &[u8],
) -> ProgramResult {
    // اینجا کد ایجاد توکن خود را قرار دهید
    Ok(())
}
import requests

url = "https://api.omniwallet.org/v1/transaction/build"

payload = {
    "fromaddress": "YOUR_BITCOIN_ADDRESS",
    "toaddress": "RECIPIENT_BITCOIN_ADDRESS",
    "amount": "AMOUNT_OF_TOKENS",
    "propertyid": "PROPERTY_ID_OF_YOUR_TOKEN",
    "fee": "TRANSACTION_FEE"
}

response = requests.post(url, json=payload)

print(response.json())
