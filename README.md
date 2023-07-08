# clang-source-code-analysis
This project will collect the learning resources of the clang 1.0 compiler, and will output some document records about the design and implementation details of the source code

About my personal compiler practice, you can click [this][1]

## How to run the development environment

1.  You should install docker, see: https://docs.docker.com/engine/install

2. You can pull this docker image
    ```
    docker pull iiicp123/clangllvm
    ```

3. And Then
   ```
   docker run -itd -p 4567:22 --name clang_docker -v /home/ubuntu/download:/share -d iiicp123/clangllvm:2.6 /bin/zsh
   ```
4. You can get the container id by running the command 
   ```
   docker ps
   ``` 
5. Through the container id, enter the inside of the container 
   ```
   docker exec -it "container id" /bin/zsh
   ``` 
6. Go to the /home directory and you can see that clang1.0 has been built 
    ```
    cd /home/llvm2.6
    ```

7. Start the ssh service and access it through vscode 
    ```
    /etc/init.d/ssh restart
    ```

[1]: https://github.com/iiicp/lcc
