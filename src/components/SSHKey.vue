<template>
  <span
    text
    class="ssh-key"
    @click="copySSHKey"
  >
    Copy SSH Key
  </span>
</template>

<script>
export default {
  name: 'SSHKey',
  methods: {
    async copySSHKey() {
      await navigator.clipboard.writeText('ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABgQCr7F7+EBogt2ELrLAbzc1IL7xORpP1XcuTz3bz+y5kW3l72sGrfFqUusc0LlpJFR3rfTLHJUpg8//iVoTHpxDDOtpAVT7j2X7G4qITllQGZz/Y3lafyipO+aw04MD06z0eSVOejlPlYrp57yMyTCTYTFuYmW4LM2ysgu8ZYdnn46zI/UdPw03jFV3NwsKtpBtr9l2HxRWrX4i7fPlaFALAdaMzILw/LTAIPd/YXP/A1/e/JJuiFDUylbY7B0ryPc54ftosF36IQncCN6kDQrmWtQyadlaJ9Yj/pEeFMGPCp1NniSUe2UPxSvTfa9bcTtn9eLA1k+2egFYvpiuE570IdW/yi/+LvAsSdlAcC7bspdL2IBzNxDfgBHYx0jogUqkv5KUQ6pA1OlrDcWM0W/ZGjkQWEeeuCRNVxz3YSQUtunUU45O6gZuxpOaCMCNN7aNhnm3Cr0sgT2snkj4YoejIK+GPdxCFlVPwEHA2Pvt28UcTHdvgQOK5KXBrrikJZWc= Pixel4XL');
    },
  },
}
</script>

<style>
.ssh-key {
  text-decoration: none;
  font-size: 14px;
  color: green;

  transition: color 0.5s ease;
}

.ssh-key:hover {
  color: lightgreen;
}
</style>
