# Cross-compile-toolchain


1.  install rustup              $curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
2.  add rustup to path env      $echo 'export PATH="$HOME/.cargo/bin:$PATH"' >> ~/.profile
3.  set cargo config            $cp config ~/.cargo/config
4.  add all target platform     $rustup target add all
5.  set toolchain               $mv /.musl_cc ~/.musl_cc
7.  add musl to path env        $echo 'source /home/$user/.musl_cc/env' >> ~/.profile
6.  download toolchain          $sh fetch.sh
