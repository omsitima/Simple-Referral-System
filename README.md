# Simple-Referral-System
Simple Referral System
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.20;

contract Referral {
    mapping(address => address) public referrer;

    function register(address _ref) public {
        require(referrer[msg.sender] == address(0), "Already registered");
        referrer[msg.sender] = _ref;
    }
}
