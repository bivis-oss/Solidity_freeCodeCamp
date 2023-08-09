//SPDX-License-Identifier: MIT
pragma solidity ^0.8.8;

import"./SimpleStorage.sol";

contract StorageFactory {

    /* address can be checked due to "piblic" status of variable */
    SimpleStorage[] public simpleStorageArray;

    /* creates "simpleStorage" contract */
    function createSimpleStorageContract() public {
        SimpleStorage simpleStorage = new SimpleStorage();
        simpleStorageArray.push(simpleStorage);
    }

    /* stores favorite number at simpleStorage["index"] */
    function sfStore(uint256 _simpleStorageIndex, uint256 _simpleStorageNumber) public {
        // need Address and ABI( Application Binary Interface )
        simpleStorageArray[_simpleStorageIndex].store(_simpleStorageNumber);
    }

    /* returns favorite number from simpleStorage["index"] */
    function sfGet(uint256 _simpleStorageIndex) public view returns(uint256){
        return simpleStorageArray[_simpleStorageIndex].retrieve();
    }

}
