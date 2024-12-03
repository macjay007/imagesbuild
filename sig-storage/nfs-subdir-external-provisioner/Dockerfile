# 克隆仓库到本地
git clone git@github.com:macjay007/imagesbuild.git

# 进入克隆的仓库目录
cd imagesbuild

# 创建所需的目录结构
mkdir -vp sig-storage/nfs-subdir-external-provisioner

# 使用 tee 命令创建并写入 Dockerfile
tee sig-storage/nfs-subdir-external-provisioner/Dockerfile <<'EOF'
FROM k8s.gcr.io/sig-storage/nfs-subdir-external-provisioner:v4.0.2
LABEL maintainer="master@macjay007.top"
LABEL buildtype="Aliyun"
EOF

# 无需回到仓库的根目录，因为我们已经在正确的位置
# cd ..  # 这行可以注释掉或删除

# 添加所有更改到 git 暂存区
git add .

# 提交更改到仓库，使用更具描述性的提交信息
git commit -m "Add Dockerfile for nfs-subdir-external-provisioner in sig-storage directory"

# 推送更改到远程仓库
git push
