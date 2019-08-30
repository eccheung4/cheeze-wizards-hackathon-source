## Sūrya's Description Report

### Files Description Table


|  File Name  |  SHA-1 Hash  |
|-------------|--------------|
| contracts/BasicTournament.sol | 8e7c7dc6ab38341c38eb65da2a6a5c6a949484d6 |
| contracts/InauguralGateKeeper.sol | 3f0eb94420fa8e21fded37a9e3701bfc0dbd7494 |
| contracts/ThreeAffinityDuelResolver.sol | 7fe11f95f7ea25633ef5afa3477f32733d4d4869 |
| contracts/WizardGuild.sol | 43eced2e58a27cf76d4041f40179fb6f37579e33 |
| contracts/WizardPresale.sol | 1f20f65c634cb714db9574952a70695b75afdb12 |


### Contracts Description Table


|  Contract  |         Type        |       Bases      |                  |                 |
|:----------:|:-------------------:|:----------------:|:----------------:|:---------------:|
|     └      |  **Function Name**  |  **Visibility**  |  **Mutability**  |  **Modifiers**  |
||||||
| **ERC165Interface** | Interface |  |||
| └ | supportsInterface | External ❗️ |   |NO❗️ |
||||||
| **WizardConstants** | Implementation |  |||
||||||
| **ERC1654** | Implementation |  |||
| └ | isValidSignature | External ❗️ |   |NO❗️ |
||||||
| **IERC165** | Interface |  |||
| └ | supportsInterface | External ❗️ |   |NO❗️ |
||||||
| **IERC721** | Implementation | IERC165 |||
| └ | balanceOf | Public ❗️ |   |NO❗️ |
| └ | ownerOf | Public ❗️ |   |NO❗️ |
| └ | approve | Public ❗️ | 🛑  |NO❗️ |
| └ | getApproved | Public ❗️ |   |NO❗️ |
| └ | setApprovalForAll | Public ❗️ | 🛑  |NO❗️ |
| └ | isApprovedForAll | Public ❗️ |   |NO❗️ |
| └ | transferFrom | Public ❗️ | 🛑  |NO❗️ |
| └ | safeTransferFrom | Public ❗️ | 🛑  |NO❗️ |
| └ | safeTransferFrom | Public ❗️ | 🛑  |NO❗️ |
||||||
| **WizardGuildInterfaceId** | Implementation |  |||
||||||
| **WizardGuildInterface** | Implementation | IERC721, WizardGuildInterfaceId |||
| └ | getWizard | External ❗️ |   |NO❗️ |
| └ | setAffinity | External ❗️ | 🛑  |NO❗️ |
| └ | mintWizards | External ❗️ | 🛑  |NO❗️ |
| └ | mintReservedWizards | External ❗️ | 🛑  |NO❗️ |
| └ | setMetadata | External ❗️ | 🛑  |NO❗️ |
| └ | isApprovedOrOwner | External ❗️ |   |NO❗️ |
| └ | verifySignature | External ❗️ |   |NO❗️ |
| └ | verifySignatures | External ❗️ |   |NO❗️ |
||||||
| **DuelResolverInterfaceId** | Implementation |  |||
||||||
| **DuelResolverInterface** | Implementation | DuelResolverInterfaceId, ERC165Interface |||
| └ | isValidMoveSet | Public ❗️ |   |NO❗️ |
| └ | isValidAffinity | External ❗️ |   |NO❗️ |
| └ | resolveDuel | Public ❗️ |   |NO❗️ |
||||||
| **AccessControl** | Implementation |  |||
| └ | \<Constructor\> | Public ❗️ | 🛑  | |
| └ | checkControlAddress | Internal 🔒 |   | |
| └ | setCeo | External ❗️ | 🛑  | onlyCEO |
| └ | _setCeo | Private 🔐 | 🛑  | |
| └ | setCoo | Public ❗️ | 🛑  | onlyCEO |
| └ | setCfo | Public ❗️ | 🛑  | onlyCEO |
||||||
| **TournamentTimeAbstract** | Implementation | AccessControl |||
| └ | getTimeParameters | External ❗️ |   |NO❗️ |
| └ | getBlueMoldParameters | External ❗️ |   |NO❗️ |
| └ | \<Constructor\> | Internal 🔒 | 🛑  | AccessControl |
| └ | _isRevivalPhase | Internal 🔒 |   | |
| └ | _isEliminationPhase | Internal 🔒 |   | |
| └ | _isEnterPhase | Internal 🔒 |   | |
| └ | _isInWindow | Internal 🔒 |   | |
| └ | checkAscensionWindow | Internal 🔒 |   | |
| └ | checkFightWindow | Internal 🔒 |   | |
| └ | checkResolutionWindow | Internal 🔒 |   | |
| └ | checkCullingWindow | Internal 🔒 |   | |
| └ | _ascensionDuelTimeout | Internal 🔒 |   | |
| └ | canChallengeAscendingWizard | Internal 🔒 |   | |
| └ | _blueMoldPower | Internal 🔒 |   | |
| └ | pause | External ❗️ | 🛑  | onlyCOO |
| └ | isPaused | External ❗️ |   |NO❗️ |
||||||
| **TournamentInterfaceId** | Implementation |  |||
||||||
| **TournamentInterface** | Implementation | TournamentInterfaceId, ERC165Interface |||
| └ | revive | External ❗️ |  💵 |NO❗️ |
| └ | enterWizards | External ❗️ |  💵 |NO❗️ |
| └ | isActive | External ❗️ |   |NO❗️ |
| └ | powerScale | External ❗️ |   |NO❗️ |
| └ | destroy | External ❗️ | 🛑  |NO❗️ |
||||||
| **BasicTournament** | Implementation | TournamentInterface, TournamentTimeAbstract, WizardConstants, DuelResolverInterfaceId |||
| └ | getRemainingWizards | External ❗️ |   |NO❗️ |
| └ | getAscendingWizardId | External ❗️ |   |NO❗️ |
| └ | \<Constructor\> | Public ❗️ | 🛑  | TournamentTimeAbstract |
| └ | \<Fallback\> | External ❗️ |  💵 |NO❗️ |
| └ | supportsInterface | External ❗️ |   |NO❗️ |
| └ | isActive | Public ❗️ |   |NO❗️ |
| └ | checkGateKeeper | Internal 🔒 |   | |
| └ | checkExists | Internal 🔒 |   | |
| └ | checkController | Internal 🔒 |   | |
| └ | getWizard | Public ❗️ |   | exists |
| └ | wizardFingerprint | External ❗️ |   |NO❗️ |
| └ | isReady | Public ❗️ |   | exists |
| └ | _isReady | Internal 🔒 |   | |
| └ | enterWizards | External ❗️ |  💵 | duringEnterPhase onlyGateKeeper |
| └ | revive | External ❗️ |  💵 | exists duringRevivalPhase onlyGateKeeper |
| └ | updateAffinity | External ❗️ | 🛑  | exists |
| └ | startAscension | External ❗️ | 🛑  | duringAscensionWindow onlyWizardController |
| └ | _checkChallenge | Internal 🔒 |   | |
| └ | challengeAscending | External ❗️ | 🛑  | duringFightWindow onlyWizardController |
| └ | acceptAscensionChallenge | External ❗️ | 🛑  | duringFightWindow onlyWizardController |
| └ | completeAscension | External ❗️ | 🛑  | duringResolutionWindow |
| └ | oneSidedCommit | External ❗️ | 🛑  | duringFightWindow onlyWizardController exists |
| └ | cancelCommitment | External ❗️ | 🛑  | onlyWizardController |
| └ | doubleCommit | External ❗️ | 🛑  | duringFightWindow |
| └ | _signedHash | Internal 🔒 |   | |
| └ | _beginDuel | Internal 🔒 | 🛑  | |
| └ | oneSidedReveal | External ❗️ | 🛑  |NO❗️ |
| └ | doubleReveal | External ❗️ | 🛑  |NO❗️ |
| └ | _resolveDuel | Internal 🔒 | 🛑  | |
| └ | _updatePower | Internal 🔒 | 🛑  | |
| └ | resolveTimedOutDuel | External ❗️ | 🛑  |NO❗️ |
| └ | giftPower | External ❗️ | 🛑  | onlyWizardController exists duringFightWindow |
| └ | cullMoldedWithSurvivor | External ❗️ | 🛑  | exists duringCullingWindow |
| └ | cullMoldedWithMolded | External ❗️ | 🛑  | duringCullingWindow |
| └ | cullTiredWizards | External ❗️ | 🛑  | duringCullingWindow |
| └ | claimTheBigCheeze | External ❗️ | 🛑  | duringCullingWindow onlyWizardController |
| └ | claimSharedWinnings | External ❗️ | 🛑  | duringCullingWindow onlyWizardController |
| └ | destroy | External ❗️ | 🛑  | onlyGateKeeper |
||||||
| **WizardConstants** | Implementation |  |||
||||||
| **IERC165** | Interface |  |||
| └ | supportsInterface | External ❗️ |   |NO❗️ |
||||||
| **IERC721** | Implementation | IERC165 |||
| └ | balanceOf | Public ❗️ |   |NO❗️ |
| └ | ownerOf | Public ❗️ |   |NO❗️ |
| └ | approve | Public ❗️ | 🛑  |NO❗️ |
| └ | getApproved | Public ❗️ |   |NO❗️ |
| └ | setApprovalForAll | Public ❗️ | 🛑  |NO❗️ |
| └ | isApprovedForAll | Public ❗️ |   |NO❗️ |
| └ | transferFrom | Public ❗️ | 🛑  |NO❗️ |
| └ | safeTransferFrom | Public ❗️ | 🛑  |NO❗️ |
| └ | safeTransferFrom | Public ❗️ | 🛑  |NO❗️ |
||||||
| **WizardGuildInterfaceId** | Implementation |  |||
||||||
| **WizardGuildInterface** | Implementation | IERC721, WizardGuildInterfaceId |||
| └ | getWizard | External ❗️ |   |NO❗️ |
| └ | setAffinity | External ❗️ | 🛑  |NO❗️ |
| └ | mintWizards | External ❗️ | 🛑  |NO❗️ |
| └ | mintReservedWizards | External ❗️ | 🛑  |NO❗️ |
| └ | setMetadata | External ❗️ | 🛑  |NO❗️ |
| └ | isApprovedOrOwner | External ❗️ |   |NO❗️ |
| └ | verifySignature | External ❗️ |   |NO❗️ |
| └ | verifySignatures | External ❗️ |   |NO❗️ |
||||||
| **ERC165Interface** | Interface |  |||
| └ | supportsInterface | External ❗️ |   |NO❗️ |
||||||
| **TournamentInterfaceId** | Implementation |  |||
||||||
| **TournamentInterface** | Implementation | TournamentInterfaceId, ERC165Interface |||
| └ | revive | External ❗️ |  💵 |NO❗️ |
| └ | enterWizards | External ❗️ |  💵 |NO❗️ |
| └ | isActive | External ❗️ |   |NO❗️ |
| └ | powerScale | External ❗️ |   |NO❗️ |
| └ | destroy | External ❗️ | 🛑  |NO❗️ |
||||||
| **AccessControl** | Implementation |  |||
| └ | \<Constructor\> | Public ❗️ | 🛑  | |
| └ | checkControlAddress | Internal 🔒 |   | |
| └ | setCeo | External ❗️ | 🛑  | onlyCEO |
| └ | _setCeo | Private 🔐 | 🛑  | |
| └ | setCoo | Public ❗️ | 🛑  | onlyCEO |
| └ | setCfo | Public ❗️ | 🛑  | onlyCEO |
||||||
| **WizardPresaleInterface** | Implementation |  |||
| └ | absorbWizard | External ❗️ | 🛑  |NO❗️ |
| └ | absorbWizardMulti | External ❗️ | 🛑  |NO❗️ |
| └ | powerToCost | Public ❗️ |   |NO❗️ |
| └ | costToPower | Public ❗️ |   |NO❗️ |
||||||
| **IERC721Receiver** | Implementation |  |||
| └ | onERC721Received | Public ❗️ | 🛑  |NO❗️ |
||||||
| **Address** | Implementation |  |||
| └ | isContract | Internal 🔒 |   | |
||||||
| **InauguralGateKeeper** | Implementation | AccessControl, WizardConstants, Address, WizardGuildInterfaceId, TournamentInterfaceId |||
| └ | getTournamentPowerScale | External ❗️ |   |NO❗️ |
| └ | \<Constructor\> | Public ❗️ | 🛑  | AccessControl |
| └ | \<Fallback\> | External ❗️ |  💵 |NO❗️ |
| └ | registerTournament | External ❗️ | 🛑  | onlyCOO |
| └ | conjureWizard | External ❗️ |  💵 |NO❗️ |
| └ | conjureWizardMulti | Public ❗️ |  💵 |NO❗️ |
| └ | conjureExclusiveMulti | External ❗️ |  💵 | onlyCOO |
| └ | _computeWizardPowers | Internal 🔒 | 🛑  | |
| └ | absorbPresaleWizards | External ❗️ | 🛑  |NO❗️ |
| └ | revive | External ❗️ |  💵 | onlyWizardController |
| └ | setAffinity | External ❗️ | 🛑  | onlyWizardController |
| └ | costToPower | Public ❗️ |   |NO❗️ |
| └ | powerToCost | Public ❗️ |   |NO❗️ |
| └ | _potContribution | Internal 🔒 |   | |
| └ | withdraw | External ❗️ | 🛑  | onlyCFO |
| └ | destroy | External ❗️ | 🛑  | onlyCOO |
| └ | destroyTournament | External ❗️ | 🛑  | onlyCOO |
| └ | _transferRefund | Private 🔐 | 🛑  | |
||||||
| **ERC165Interface** | Interface |  |||
| └ | supportsInterface | External ❗️ |   |NO❗️ |
||||||
| **DuelResolverInterfaceId** | Implementation |  |||
||||||
| **DuelResolverInterface** | Implementation | DuelResolverInterfaceId, ERC165Interface |||
| └ | isValidMoveSet | Public ❗️ |   |NO❗️ |
| └ | isValidAffinity | External ❗️ |   |NO❗️ |
| └ | resolveDuel | Public ❗️ |   |NO❗️ |
||||||
| **ThreeAffinityDuelResolver** | Implementation | DuelResolverInterface |||
| └ | supportsInterface | External ❗️ |   |NO❗️ |
| └ | isValidMoveSet | Public ❗️ |   |NO❗️ |
| └ | isValidAffinity | Public ❗️ |   |NO❗️ |
| └ | resolveDuel | Public ❗️ |   |NO❗️ |
| └ | _duelScore | Internal 🔒 |   | |
| └ | _powerTransfer | Private 🔐 |   | |
| └ | _fakePowQ10 | Private 🔐 |   | |
| └ | _fakePowInternal | Private 🔐 |   | |
||||||
| **WizardConstants** | Implementation |  |||
||||||
| **ERC165Query** | Implementation |  |||
| └ | doesContractImplementInterface | Internal 🔒 |   | |
| └ | noThrowCall | Internal 🔒 |   | |
||||||
| **IERC165** | Interface |  |||
| └ | supportsInterface | External ❗️ |   |NO❗️ |
||||||
| **IERC721** | Implementation | IERC165 |||
| └ | balanceOf | Public ❗️ |   |NO❗️ |
| └ | ownerOf | Public ❗️ |   |NO❗️ |
| └ | approve | Public ❗️ | 🛑  |NO❗️ |
| └ | getApproved | Public ❗️ |   |NO❗️ |
| └ | setApprovalForAll | Public ❗️ | 🛑  |NO❗️ |
| └ | isApprovedForAll | Public ❗️ |   |NO❗️ |
| └ | transferFrom | Public ❗️ | 🛑  |NO❗️ |
| └ | safeTransferFrom | Public ❗️ | 🛑  |NO❗️ |
| └ | safeTransferFrom | Public ❗️ | 🛑  |NO❗️ |
||||||
| **IERC721Receiver** | Implementation |  |||
| └ | onERC721Received | Public ❗️ | 🛑  |NO❗️ |
||||||
| **ERC165Interface** | Interface |  |||
| └ | supportsInterface | External ❗️ |   |NO❗️ |
||||||
| **Address** | Implementation |  |||
| └ | isContract | Internal 🔒 |   | |
||||||
| **WizardNFT** | Implementation | ERC165Interface, IERC721, WizardConstants, Address |||
| └ | supportsInterface | Public ❗️ |   |NO❗️ |
| └ | balanceOf | Public ❗️ |   |NO❗️ |
| └ | ownerOf | Public ❗️ |   |NO❗️ |
| └ | approve | Public ❗️ | 🛑  |NO❗️ |
| └ | getApproved | Public ❗️ |   |NO❗️ |
| └ | setApprovalForAll | Public ❗️ | 🛑  |NO❗️ |
| └ | isApprovedForAll | Public ❗️ |   |NO❗️ |
| └ | transferFrom | Public ❗️ | 🛑  |NO❗️ |
| └ | safeTransferFrom | Public ❗️ | 🛑  |NO❗️ |
| └ | safeTransferFrom | Public ❗️ | 🛑  |NO❗️ |
| └ | _exists | Internal 🔒 |   | |
| └ | _isApprovedOrOwner | Internal 🔒 |   | |
| └ | _createWizard | Internal 🔒 | 🛑  | |
| └ | _burn | Internal 🔒 | 🛑  | |
| └ | _burn | Internal 🔒 | 🛑  | |
| └ | _transferFrom | Internal 🔒 | 🛑  | |
| └ | _checkOnERC721Received | Internal 🔒 | 🛑  | |
| └ | _clearApproval | Private 🔐 | 🛑  | |
||||||
| **WizardGuildInterfaceId** | Implementation |  |||
||||||
| **WizardGuildInterface** | Implementation | IERC721, WizardGuildInterfaceId |||
| └ | getWizard | External ❗️ |   |NO❗️ |
| └ | setAffinity | External ❗️ | 🛑  |NO❗️ |
| └ | mintWizards | External ❗️ | 🛑  |NO❗️ |
| └ | mintReservedWizards | External ❗️ | 🛑  |NO❗️ |
| └ | setMetadata | External ❗️ | 🛑  |NO❗️ |
| └ | isApprovedOrOwner | External ❗️ |   |NO❗️ |
| └ | verifySignature | External ❗️ |   |NO❗️ |
| └ | verifySignatures | External ❗️ |   |NO❗️ |
||||||
| **AccessControl** | Implementation |  |||
| └ | \<Constructor\> | Public ❗️ | 🛑  | |
| └ | checkControlAddress | Internal 🔒 |   | |
| └ | setCeo | External ❗️ | 🛑  | onlyCEO |
| └ | _setCeo | Private 🔐 | 🛑  | |
| └ | setCoo | Public ❗️ | 🛑  | onlyCEO |
| └ | setCfo | Public ❗️ | 🛑  | onlyCEO |
||||||
| **SigTools** | Library |  |||
| └ | _splitSignature | Internal 🔒 |   | |
||||||
| **ERC1654** | Implementation |  |||
| └ | isValidSignature | External ❗️ |   |NO❗️ |
||||||
| **WizardGuild** | Implementation | AccessControl, WizardNFT, WizardGuildInterface, ERC165Query |||
| └ | getNextWizardIndex | External ❗️ |   |NO❗️ |
| └ | \<Constructor\> | Public ❗️ | 🛑  | AccessControl |
| └ | openSeries | External ❗️ | 🛑  | onlyCOO |
| └ | closeSeries | External ❗️ | 🛑  | duringSeries |
| └ | supportsInterface | Public ❗️ |   |NO❗️ |
| └ | getWizard | Public ❗️ |   |NO❗️ |
| └ | mintWizards | External ❗️ | 🛑  | onlyMinter |
| └ | mintReservedWizards | External ❗️ | 🛑  | onlyMinter |
| └ | setMetadata | External ❗️ | 🛑  | duringSeries |
| └ | setAffinity | External ❗️ | 🛑  | onlyMinter |
| └ | isApprovedOrOwner | External ❗️ |   |NO❗️ |
| └ | verifySignature | Public ❗️ |   |NO❗️ |
| └ | verifySignatures | External ❗️ |   |NO❗️ |
| └ | _validSignatureForAddress | Internal 🔒 |   | |
||||||
| **IERC165** | Interface |  |||
| └ | supportsInterface | External ❗️ |   |NO❗️ |
||||||
| **WizardConstants** | Implementation |  |||
||||||
| **IERC721** | Implementation | IERC165 |||
| └ | balanceOf | Public ❗️ |   |NO❗️ |
| └ | ownerOf | Public ❗️ |   |NO❗️ |
| └ | approve | Public ❗️ | 🛑  |NO❗️ |
| └ | getApproved | Public ❗️ |   |NO❗️ |
| └ | setApprovalForAll | Public ❗️ | 🛑  |NO❗️ |
| └ | isApprovedForAll | Public ❗️ |   |NO❗️ |
| └ | transferFrom | Public ❗️ | 🛑  |NO❗️ |
| └ | safeTransferFrom | Public ❗️ | 🛑  |NO❗️ |
| └ | safeTransferFrom | Public ❗️ | 🛑  |NO❗️ |
||||||
| **IERC721Receiver** | Implementation |  |||
| └ | onERC721Received | Public ❗️ | 🛑  |NO❗️ |
||||||
| **ERC165** | Implementation | IERC165 |||
| └ | \<Constructor\> | Internal 🔒 | 🛑  | |
| └ | supportsInterface | External ❗️ |   |NO❗️ |
| └ | _registerInterface | Internal 🔒 | 🛑  | |
||||||
| **Address** | Implementation |  |||
| └ | isContract | Internal 🔒 |   | |
||||||
| **WizardPresaleNFT** | Implementation | ERC165, IERC721, Address |||
| └ | \<Constructor\> | Public ❗️ | 🛑  | |
| └ | balanceOf | Public ❗️ |   |NO❗️ |
| └ | ownerOf | Public ❗️ |   |NO❗️ |
| └ | approve | Public ❗️ | 🛑  |NO❗️ |
| └ | getApproved | Public ❗️ |   |NO❗️ |
| └ | setApprovalForAll | Public ❗️ | 🛑  |NO❗️ |
| └ | isApprovedForAll | Public ❗️ |   |NO❗️ |
| └ | transferFrom | Public ❗️ | 🛑  |NO❗️ |
| └ | safeTransferFrom | Public ❗️ | 🛑  |NO❗️ |
| └ | safeTransferFrom | Public ❗️ | 🛑  |NO❗️ |
| └ | _exists | Internal 🔒 |   | |
| └ | _isApprovedOrOwner | Internal 🔒 |   | |
| └ | _burn | Internal 🔒 | 🛑  | |
| └ | _burn | Internal 🔒 | 🛑  | |
| └ | _transferFrom | Internal 🔒 | 🛑  | |
| └ | _checkOnERC721Received | Internal 🔒 | 🛑  | |
| └ | _clearApproval | Private 🔐 | 🛑  | |
||||||
| **WizardPresaleInterface** | Implementation |  |||
| └ | absorbWizard | External ❗️ | 🛑  |NO❗️ |
| └ | absorbWizardMulti | External ❗️ | 🛑  |NO❗️ |
| └ | powerToCost | Public ❗️ |   |NO❗️ |
| └ | costToPower | Public ❗️ |   |NO❗️ |
||||||
| **WizardPresale** | Implementation | WizardPresaleNFT, WizardPresaleInterface, WizardConstants |||
| └ | \<Constructor\> | Public ❗️ | 🛑  | |
| └ | setGatekeeper | External ❗️ | 🛑  | onlyGuildmaster |
| └ | postponeSale | External ❗️ | 🛑  | onlyGuildmaster |
| └ | isDuringSale | External ❗️ |   |NO❗️ |
| └ | getWizard | Public ❗️ |   |NO❗️ |
| └ | costToPower | Public ❗️ |   |NO❗️ |
| └ | powerToCost | Public ❗️ |   |NO❗️ |
| └ | absorbWizard | External ❗️ | 🛑  | onlyGatekeeper |
| └ | absorbWizardMulti | External ❗️ | 🛑  | onlyGatekeeper |
| └ | _createWizard | Internal 🔒 | 🛑  | |
| └ | _transferRefund | Private 🔐 | 🛑  | |
| └ | conjureExclusiveWizard | Public ❗️ |  💵 | onlyGuildmaster |
| └ | safeConjureExclusiveWizard | External ❗️ |  💵 | onlyGuildmaster |
| └ | conjureExclusiveWizardMulti | External ❗️ |  💵 | onlyGuildmaster |
| └ | setAffinity | External ❗️ | 🛑  |NO❗️ |
| └ | _conjureWizard | Private 🔐 | 🛑  | |
| └ | conjureWizard | External ❗️ |  💵 | onlyDuringSale |
| └ | conjureWizardMulti | External ❗️ |  💵 | onlyDuringSale |
| └ | destroy | External ❗️ | 🛑  | onlyGuildmaster |


### Legend

|  Symbol  |  Meaning  |
|:--------:|-----------|
|    🛑    | Function can modify state |
|    💵    | Function is payable |
