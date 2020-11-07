---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 3E7B9EFA-8BC2-46EB-9AD7-43EAB7FF3891
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVmssOsProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVmssOsProfile.md
ms.openlocfilehash: ee9649d7a2a88dd3a91f428201ddc66d1a6562da
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764467"
---
# <span data-ttu-id="34297-101">Set-AzureRmVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="34297-101">Set-AzureRmVmssOsProfile</span></span>

## <span data-ttu-id="34297-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="34297-102">SYNOPSIS</span></span>
<span data-ttu-id="34297-103">VMSS işletim sistemi profili özelliklerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="34297-103">Sets the VMSS operating system profile properties.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="34297-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="34297-104">SYNTAX</span></span>

```
Set-AzureRmVmssOsProfile [-VirtualMachineScaleSet] <VirtualMachineScaleSet> [[-ComputerNamePrefix] <String>]
 [[-AdminUsername] <String>] [[-AdminPassword] <String>] [[-CustomData] <String>]
 [[-WindowsConfigurationProvisionVMAgent] <Boolean>] [[-WindowsConfigurationEnableAutomaticUpdate] <Boolean>]
 [[-TimeZone] <String>] [[-AdditionalUnattendContent] <AdditionalUnattendContent[]>]
 [[-Listener] <WinRMListener[]>] [[-LinuxConfigurationDisablePasswordAuthentication] <Boolean>]
 [[-PublicKey] <SshPublicKey[]>] [[-Secret] <VaultSecretGroup[]>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="34297-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="34297-105">DESCRIPTION</span></span>
<span data-ttu-id="34297-106">**Set-AzureRmVmssOsProfile** cmdlet 'ı, sanal makine ölçeğini ayarlama işletim sistemi profili özelliklerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="34297-106">The **Set-AzureRmVmssOsProfile** cmdlet sets the Virtual Machine Scale Set operating system profile properties.</span></span>

## <span data-ttu-id="34297-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="34297-107">EXAMPLES</span></span>

### <span data-ttu-id="34297-108">Örnek 1: bir VMSS için işletim sistemi profili özelliklerini ayarlama</span><span class="sxs-lookup"><span data-stu-id="34297-108">Example 1: Set the operating system profile properties for a VMSS</span></span>
```
PS C:\> Set-AzureRmVmssOSProfile -VirtualMachineScaleSet "ContosoVMSS" -ComputerNamePrefix "Test" -AdminUsername $AdminUsername -AdminPassword $AdminPassword
```

<span data-ttu-id="34297-109">Bu komut, ContosoVMSS adlı VMSS 'ye ait sanal makinelerin işletim sistemi profili özelliklerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="34297-109">This command sets operating system profile properties for the virtual machines that belong to the VMSS named ContosoVMSS.</span></span>
<span data-ttu-id="34297-110">Bu komut, VMSS 'deki tüm sanal makine örneklerinin bilgisayar adı önekini, yöneticinin kullanıcı adını ve parolasını test etmek üzere ayarlar.</span><span class="sxs-lookup"><span data-stu-id="34297-110">The command sets the computer name prefix for all the virtual machine instances in the VMSS to Test and supplies the administrator username and password.</span></span>

## <span data-ttu-id="34297-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="34297-111">PARAMETERS</span></span>

### <span data-ttu-id="34297-112">-Additionalunattenvseçcontent</span><span class="sxs-lookup"><span data-stu-id="34297-112">-AdditionalUnattendContent</span></span>
<span data-ttu-id="34297-113">Bir katılımsız içerik nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="34297-113">Specifies an unattended content object.</span></span>
<span data-ttu-id="34297-114">Nesneyi oluşturmak için Add-AzureRmVMAdditionalUnattendContent kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="34297-114">You can use the Add-AzureRmVMAdditionalUnattendContent to create the object.</span></span>

```yaml
Type: AdditionalUnattendContent[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34297-115">-AdminPassword</span><span class="sxs-lookup"><span data-stu-id="34297-115">-AdminPassword</span></span>
<span data-ttu-id="34297-116">VMSS 'deki tüm sanal makine örnekleri için kullanılacak yönetici parolasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="34297-116">Specifies the administrator password to use for all the virtual machine instances in the VMSS.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34297-117">-AdminUsername</span><span class="sxs-lookup"><span data-stu-id="34297-117">-AdminUsername</span></span>
<span data-ttu-id="34297-118">VMSS 'deki tüm sanal makine örnekleri için kullanılacak yönetici hesap adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="34297-118">Specifies the administrator account name to use for all the virtual machine instances in the VMSS.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34297-119">-ComputerNamePrefix</span><span class="sxs-lookup"><span data-stu-id="34297-119">-ComputerNamePrefix</span></span>
<span data-ttu-id="34297-120">VMSS 'deki tüm sanal makine örneklerinin bilgisayar adı önekini belirtir.</span><span class="sxs-lookup"><span data-stu-id="34297-120">Specifies the computer name prefix for all the virtual machine instances in the VMSS.</span></span>
<span data-ttu-id="34297-121">Bilgisayar adları 1-15 karakter uzunluğunda olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="34297-121">Computer names must be 1 to 15 characters long.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34297-122">-CustomData</span><span class="sxs-lookup"><span data-stu-id="34297-122">-CustomData</span></span>
<span data-ttu-id="34297-123">Özel verilerin Base-64 kodlu dizesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="34297-123">Specifies a base-64 encoded string of custom data.</span></span>
<span data-ttu-id="34297-124">Bu, sanal makinede dosya olarak kaydedilmiş bir ikili diziye çözülür.</span><span class="sxs-lookup"><span data-stu-id="34297-124">This is decoded to a binary array that is saved as a file on the virtual machine.</span></span>
<span data-ttu-id="34297-125">İkili dizinin en fazla uzunluğu 65535 bayttır.</span><span class="sxs-lookup"><span data-stu-id="34297-125">The maximum length of the binary array is 65535 bytes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34297-126">-LinuxConfigurationDisablePasswordAuthentication</span><span class="sxs-lookup"><span data-stu-id="34297-126">-LinuxConfigurationDisablePasswordAuthentication</span></span>
<span data-ttu-id="34297-127">Bu cmdlet 'in parola kimlik doğrulamasını devre dışı bırakacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="34297-127">Indicates that this cmdlet disables password authentication.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34297-128">-Listener</span><span class="sxs-lookup"><span data-stu-id="34297-128">-Listener</span></span>
<span data-ttu-id="34297-129">Windows Uzaktan Yönetim (WinRM) dinleyicilerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="34297-129">Specifies the Windows Remote Management (WinRM) listeners.</span></span>
<span data-ttu-id="34297-130">Bu, uzak Windows PowerShell 'i etkinleştirmiştir.</span><span class="sxs-lookup"><span data-stu-id="34297-130">This enables remote Windows PowerShell.</span></span>
<span data-ttu-id="34297-131">Dinleyiciyi oluşturmak için Add-AzureRmVmssWinRMListener cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="34297-131">You can use the Add-AzureRmVmssWinRMListener cmdlet to create the listener.</span></span>

```yaml
Type: WinRMListener[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34297-132">-PublicKey</span><span class="sxs-lookup"><span data-stu-id="34297-132">-PublicKey</span></span>
<span data-ttu-id="34297-133">Güvenli Kabuk (SSH) ortak anahtar nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="34297-133">Specifies the Secure Shell (SSH) public key object.</span></span>
<span data-ttu-id="34297-134">Nesneyi oluşturmak için Add-AzureRmVMSshPublicKey cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="34297-134">You can use the Add-AzureRmVMSshPublicKey cmdlet to create the object.</span></span>

```yaml
Type: SshPublicKey[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 11
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34297-135">-Parola</span><span class="sxs-lookup"><span data-stu-id="34297-135">-Secret</span></span>
<span data-ttu-id="34297-136">Sanal makineye yerleştirilecek sertifika başvurularını içeren gizli nesne türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="34297-136">Specifies the secrets object which contains the certificate references to place on the virtual machine.</span></span>
<span data-ttu-id="34297-137">Gizli nesneleri oluşturmak için Add-AzureRmVmssSecret cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="34297-137">You can use the Add-AzureRmVmssSecret cmdlet to create the secrets object.</span></span>

```yaml
Type: VaultSecretGroup[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 12
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34297-138">-TimeZone</span><span class="sxs-lookup"><span data-stu-id="34297-138">-TimeZone</span></span>
<span data-ttu-id="34297-139">Sanal makinenin saat dilimini belirtir.</span><span class="sxs-lookup"><span data-stu-id="34297-139">Specifies the time zone for the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34297-140">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="34297-140">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="34297-141">VMSS nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="34297-141">Specifies the VMSS object.</span></span>
<span data-ttu-id="34297-142">Nesneyi oluşturmak için New-AzureRmVmssConfig cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="34297-142">You can use the New-AzureRmVmssConfig cmdlet to create the object.</span></span>

```yaml
Type: VirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="34297-143">-WindowsConfigurationEnableAutomaticUpdate</span><span class="sxs-lookup"><span data-stu-id="34297-143">-WindowsConfigurationEnableAutomaticUpdate</span></span>
<span data-ttu-id="34297-144">VMSS 'deki sanal makinelerin otomatik güncelleştirmeler için etkinleştirilip etkinleştirilmediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="34297-144">Indicates whether the virtual machines in the VMSS are enabled for automatic updates.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34297-145">-WindowsConfigurationProvisionVMAgent</span><span class="sxs-lookup"><span data-stu-id="34297-145">-WindowsConfigurationProvisionVMAgent</span></span>
<span data-ttu-id="34297-146">VMSS 'deki sanal makinelerde sanal makine aracısının sağlanması gerekip gerekmediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="34297-146">Indicates whether virtual machine agent should be provisioned on the virtual machines in the VMSS.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34297-147">-Onay</span><span class="sxs-lookup"><span data-stu-id="34297-147">-Confirm</span></span>
<span data-ttu-id="34297-148">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="34297-148">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34297-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="34297-149">-WhatIf</span></span>
<span data-ttu-id="34297-150">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="34297-150">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="34297-151">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="34297-151">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34297-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34297-152">CommonParameters</span></span>
<span data-ttu-id="34297-153">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="34297-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34297-154">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="34297-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34297-155">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="34297-155">INPUTS</span></span>

### <span data-ttu-id="34297-156">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="34297-156">None</span></span>
<span data-ttu-id="34297-157">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="34297-157">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="34297-158">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="34297-158">OUTPUTS</span></span>

### <span data-ttu-id="34297-159">Bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="34297-159">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="34297-160">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="34297-160">NOTES</span></span>

## <span data-ttu-id="34297-161">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="34297-161">RELATED LINKS</span></span>

[<span data-ttu-id="34297-162">Add-AzureRmVMAdditionalUnattendContent</span><span class="sxs-lookup"><span data-stu-id="34297-162">Add-AzureRmVMAdditionalUnattendContent</span></span>](./Add-AzureRmVMAdditionalUnattendContent.md)

[<span data-ttu-id="34297-163">Add-AzureRmVmssWinRMListener</span><span class="sxs-lookup"><span data-stu-id="34297-163">Add-AzureRmVmssWinRMListener</span></span>](./Add-AzureRmVmssWinRMListener.md)

[<span data-ttu-id="34297-164">Add-AzureRmVMSshPublicKey</span><span class="sxs-lookup"><span data-stu-id="34297-164">Add-AzureRmVMSshPublicKey</span></span>](./Add-AzureRmVMSshPublicKey.md)

[<span data-ttu-id="34297-165">Add-AzureRmVmssSecret</span><span class="sxs-lookup"><span data-stu-id="34297-165">Add-AzureRmVmssSecret</span></span>](./Add-AzureRmVmssSecret.md)

[<span data-ttu-id="34297-166">Yeni-AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="34297-166">New-AzureRmVmssConfig</span></span>](./New-AzureRmVmssConfig.md)


