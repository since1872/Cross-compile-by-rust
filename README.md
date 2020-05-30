# Cross-compile-toolchain



1.  install rustup              $curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
2.  add rustup to path env      $echo 'export PATH="$HOME/.cargo/bin:$PATH"' >> ~/.profile
3.  set cargo config            $cp config ~/.cargo/config
4.  add all target platform     $rustup target add all
5.  set toolchain               $mv /.musl_cc ~/.musl_cc
7.  add musl to path env        $echo 'source /home/$user/.musl_cc/env' >> ~/.profile
6.  download toolchain          $cd /.musl_cc/toolchainsh && sh fetch.sh
7.  cargo new helloworld

    cd helloworld
    
    cargo build --target arm-unknown-linux-musleabi (--release)
    
    
    #cargo build --target aarch64-unknown-linux-musl
    
    #cargo build --target arm-unknown-linux-musleabi
    
    #cargo build --target arm-unknown-linux-musleabihf
    
    #cargo build --target i686-unknown-linux-musl
    
    #cargo build --target mips-unknown-linux-musl
    
    #cargo build --target mips64-unknown-linux-muslabi64
    
    #cargo build  --target mips64el-unknown-linux-muslabi64
    
    #cargo build  --target mipsel-unknown-linux-musl
    
    #cargo build  --target x86_64-unknown-linux-musl
