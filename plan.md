### Phase 1: Project Setup & Core NFT
First, we need a solid foundation. This involves setting up a new Anchor project and defining the basic NFT.

1.  **Install Prerequisites**: Before we start, you'll need the [Solana tool suite](https://docs.solana.com/cli/install-solana-cli-tools), [Rust](https://www.rust-lang.org/tools/install), and the [Anchor framework](https://www.anchor-lang.com/docs/installation).
2.  **Initialize Project**: The best way to start is by creating a new Anchor project. This will generate the standard boilerplate for a Solana program, including the directory structure you've already started creating. You can run the following command in your terminal:
    ```bash
    anchor init mutable_nft
    ```
    This will set up the project in a new `mutable_nft` directory.
3.  **Define NFT Account**: In `mutable_nft/programs/mutable_nft/src/lib.rs`, we will define the main data structure (`Account`) for your NFT, holding its essential data like a metadata URI and the current authority.
4.  **Create Instruction**: We'll implement the first instruction, `create_nft`, to mint a new NFT.

### Phase 2: Mutability & Edit History
Once we can create NFTs, we'll make them dynamic.

5.  **Edit Instruction**: Implement an `edit_nft` instruction to allow for changes.
6.  **History Account**: Define a new account structure to log each edit, creating the on-chain provenance trail mentioned in your `README.md`.

### Phase 3: Royalties & Governance
Next, we'll add the economic and control layers.

7.  **Cumulative Royalties**: Extend the logic to allow editors to add their royalty share.
8.  **Governance Models**: Implement the Creator-Centric and Owner-Driven control flows.

### Phase 4: Testing & Advanced Features
Finally, we'll ensure everything works and tackle the more advanced concepts.

9.  **Write Tests**: We'll use TypeScript to write tests for all the instructions to ensure they work as expected.
10. **cNFT Integration**: Once the core on-chain logic is built and tested, we can explore how to link this state with Compressed NFTs (cNFTs). This is a more advanced topic, so it's best to tackle it after the core logic is solid.

This incremental plan will make the project much more manageable.

How does this approach sound to you? If you're ready, we can begin with Phase 1. Let me know if you have the prerequisites installed, and we can start structuring your `lib.rs` file.