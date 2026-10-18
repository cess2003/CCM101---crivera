# Mission Reflection

**1. Why object storage suits millions of photos better than block storage.**
Block storage works like a hard drive attached to a single server, so its capacity is limited and has to be managed manually. Object storage keeps each photo as an object with metadata and a unique ID in a flat structure, so it can scale to millions of files without managing folders or disk sizes. It is also accessed through a web API, which suits a photo-sharing application.

**2. How Docker made deploying MinIO easier.**
Docker let me deploy MinIO with one command instead of installing it, setting up dependencies and configuring it by hand. The image already contained everything needed, and the port mappings and environment variables set up access and credentials immediately. I also learned that images depend on registries: the original MinIO image was no longer available, so I had to use the `pgsty/silo` fork instead.

**3. What a bucket is.**
A bucket is a top-level container in object storage that holds objects (files). It works like a folder at the highest level, with its own name and access rules. In this lab, `client-photos` is the bucket that holds the client's uploaded images.

**4. How enterprises prevent data loss if a server crashes.**
Large companies replicate their data across multiple drives, servers and even different data centers or regions, so a copy still exists if one machine fails. Many systems also use erasure coding, which splits data into pieces with extra parity so the original can be rebuilt. Regular backups and versioning add another layer of protection.

**5. My growing confidence with the Linux command line.**
I am becoming more comfortable with the command line because I can now run Docker commands, check running containers and read error messages to find the cause of a problem. When the MinIO image failed to pull, I could understand the error and try another image instead of giving up. Each lab builds on the previous one, so commands that once looked confusing now feel familiar.
