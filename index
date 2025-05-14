<<<<<<< OLD
import { useState, useEffect } from 'react';
import { ConnectionProvider, WalletProvider } from "@solana/wallet-adapter-react";
import { WalletModalProvider } from "@solana/wallet-adapter-react-ui";
import "@solana/wallet-adapter-react-ui/styles.css";
import { motion } from 'framer-motion';
const AppWithProvider = () => {
  const endpoint = 'https://rpc.dev.fun/2a3391377ede3b72d2bd';
  return <ConnectionProvider endpoint={endpoint}>
      <WalletProvider wallets={[]} autoConnect>
        <WalletModalProvider>
          <App />
        </WalletModalProvider>
      </WalletProvider>
    </ConnectionProvider>;
};
const DISCOUNT_PERCENTAGE = 15;
function App() {
  const connected = true;
  const [hasToken,,] = useState(true);
=======
import { useState, useEffect } from 'react';
import { ConnectionProvider, WalletProvider } from "@solana/wallet-adapter-react";
import { WalletModalProvider } from "@solana/wallet-adapter-react-ui";
import "@solana/wallet-adapter-react-ui/styles.css";
import { motion } from 'framer-motion';
const AppWithProvider = () => {
  const endpoint = 'https://rpc.dev.fun/2a3391377ede3b72d2bd';
  return <ConnectionProvider endpoint={endpoint}>
      <WalletProvider wallets={[]} autoConnect>
        <WalletModalProvider>
          <App />
        </WalletModalProvider>
      </WalletProvider>
    </ConnectionProvider>;
};
const DISCOUNT_PERCENTAGE = 15;
function App() {
  const [connected, setConnected] = useState(false);
  const [hasToken, setHasToken] = useState(false);
  const [showWalletOptions, setShowWalletOptions] = useState(false);
>>>>>>> NEW



<<<<<<< OLD
  useEffect(() => {
    if (connected) {
      setIsChecking(true);
      setTimeout(() => {
        setIsChecking(false);
      }, 800);
    }
  }, []);
=======
  useEffect(() => {
    if (connected) {
      setIsChecking(true);
      setTimeout(() => {
        setIsChecking(false);
        setHasToken(true);
      }, 800);
    }
  }, [connected]);

  const connectWallet = () => {
    setConnected(true);
    setShowWalletOptions(false);
  };
>>>>>>> NEW



<<<<<<< OLD
        <div className="flex justify-between items-center mb-8">
          <h1 className="text-2xl font-bold">tokencheck</h1>
          <div className="wallet-adapter-dropdown">
            {}
            <button className="wallet-adapter-button wallet-adapter-button-trigger !bg-white !text-black hover:!bg-gray-200 !transition-all">
              <span>Connected: Bvz5...Jemk</span>
            </button>
          </div>
        </div>
=======
        <div className="flex justify-between items-center mb-8">
          <h1 className="text-2xl font-bold">tokencheck</h1>
          <div className="wallet-adapter-dropdown relative">
            <button 
              onClick={() => !connected && setShowWalletOptions(!showWalletOptions)} 
              className="wallet-adapter-button wallet-adapter-button-trigger !bg-white !text-black hover:!bg-gray-200 !transition-all"
            >
              {connected ? <span>Connected: Bvz5...Jemk</span> : <span>Select Wallet</span>}
            </button>
            
            {showWalletOptions && !connected && (
              <motion.div 
                initial={{ opacity: 0, y: -10 }}
                animate={{ opacity: 1, y: 0 }}
                className="absolute right-0 mt-2 w-56 bg-gray-800 rounded-md shadow-lg z-10"
              >
                <div className="py-1">
                  <button
                    onClick={connectWallet}
                    className="flex items-center px-4 py-3 w-full text-left hover:bg-gray-700 transition-colors"
                  >
                    <img
