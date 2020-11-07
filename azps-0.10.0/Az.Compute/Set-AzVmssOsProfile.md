---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 3E7B9EFA-8BC2-46EB-9AD7-43EAB7FF3891
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmssosprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVmssOsProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVmssOsProfile.md
ms.openlocfilehash: 98ebce4e139d230607da77536492d0ba40d0760f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936809"
---
# <span data-ttu-id="5c106-101">Set-AzVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="5c106-101">Set-AzVmssOsProfile</span></span>

## <span data-ttu-id="5c106-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5c106-102">SYNOPSIS</span></span>
<span data-ttu-id="5c106-103">VMSS işletim sistemi profili özelliklerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="5c106-103">Sets the VMSS operating system profile properties.</span></span>

## <span data-ttu-id="5c106-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5c106-104">SYNTAX</span></span>

```
Set-AzVmssOsProfile [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-ComputerNamePrefix] <String>]
 [[-AdminUsername] <String>] [[-AdminPassword] <String>] [[-CustomData] <String>]
 [[-WindowsConfigurationProvisionVMAgent] <Boolean>] [[-WindowsConfigurationEnableAutomaticUpdate] <Boolean>]
 [[-TimeZone] <String>] [[-AdditionalUnattendContent] <AdditionalUnattendContent[]>]
 [[-Listener] <WinRMListener[]>] [[-LinuxConfigurationDisablePasswordAuthentication] <Boolean>]
 [[-PublicKey] <SshPublicKey[]>] [[-Secret] <VaultSecretGroup[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5c106-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="5c106-105">DESCRIPTION</span></span>
<span data-ttu-id="5c106-106">**Set-AzVmssOsProfile** cmdlet 'ı, sanal makine ölçeğini ayarlama işletim sistemi profili özelliklerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="5c106-106">The **Set-AzVmssOsProfile** cmdlet sets the Virtual Machine Scale Set operating system profile properties.</span></span>

## <span data-ttu-id="5c106-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5c106-107">EXAMPLES</span></span>

### <span data-ttu-id="5c106-108">Örnek 1: bir VMSS için işletim sistemi profili özelliklerini ayarlama</span><span class="sxs-lookup"><span data-stu-id="5c106-108">Example 1: Set the operating system profile properties for a VMSS</span></span>
```
PS C:\> Set-AzVmssOSProfile -VirtualMachineScaleSet "ContosoVMSS" -ComputerNamePrefix "Test" -AdminUsername $AdminUsername -AdminPassword $AdminPassword
```

<span data-ttu-id="5c106-109">Bu komut, ContosoVMSS adlı VMSS 'ye ait sanal makinelerin işletim sistemi profili özelliklerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="5c106-109">This command sets operating system profile properties for the virtual machines that belong to the VMSS named ContosoVMSS.</span></span>
<span data-ttu-id="5c106-110">Bu komut, VMSS 'deki tüm sanal makine örneklerinin bilgisayar adı önekini, yöneticinin kullanıcı adını ve parolasını test etmek üzere ayarlar.</span><span class="sxs-lookup"><span data-stu-id="5c106-110">The command sets the computer name prefix for all the virtual machine instances in the VMSS to Test and supplies the administrator username and password.</span></span>

## <span data-ttu-id="5c106-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5c106-111">PARAMETERS</span></span>

### <span data-ttu-id="5c106-112">-Additionalunattenvseçcontent</span><span class="sxs-lookup"><span data-stu-id="5c106-112">-AdditionalUnattendContent</span></span>
<span data-ttu-id="5c106-113">Bir katılımsız içerik nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="5c106-113">Specifies an unattended content object.</span></span>
<span data-ttu-id="5c106-114">Nesneyi oluşturmak için Add-AzVMAdditionalUnattendContent kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5c106-114">You can use the Add-AzVMAdditionalUnattendContent to create the object.</span></span>

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

### <span data-ttu-id="5c106-115">-AdminPassword</span><span class="sxs-lookup"><span data-stu-id="5c106-115">-AdminPassword</span></span>
<span data-ttu-id="5c106-116">VMSS 'deki tüm sanal makine örnekleri için kullanılacak yönetici parolasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5c106-116">Specifies the administrator password to use for all the virtual machine instances in the VMSS.</span></span>

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

### <span data-ttu-id="5c106-117">-AdminUsername</span><span class="sxs-lookup"><span data-stu-id="5c106-117">-AdminUsername</span></span>
<span data-ttu-id="5c106-118">VMSS 'deki tüm sanal makine örnekleri için kullanılacak yönetici hesap adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5c106-118">Specifies the administrator account name to use for all the virtual machine instances in the VMSS.</span></span>

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

### <span data-ttu-id="5c106-119">-ComputerNamePrefix</span><span class="sxs-lookup"><span data-stu-id="5c106-119">-ComputerNamePrefix</span></span>
<span data-ttu-id="5c106-120">VMSS 'deki tüm sanal makine örneklerinin bilgisayar adı önekini belirtir.</span><span class="sxs-lookup"><span data-stu-id="5c106-120">Specifies the computer name prefix for all the virtual machine instances in the VMSS.</span></span>
<span data-ttu-id="5c106-121">Bilgisayar adları 1-15 karakter uzunluğunda olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="5c106-121">Computer names must be 1 to 15 characters long.</span></span>

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

### <span data-ttu-id="5c106-122">-CustomData</span><span class="sxs-lookup"><span data-stu-id="5c106-122">-CustomData</span></span>
<span data-ttu-id="5c106-123">Özel verilerin Base-64 kodlu dizesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="5c106-123">Specifies a base-64 encoded string of custom data.</span></span>
<span data-ttu-id="5c106-124">Bu, sanal makinede dosya olarak kaydedilmiş bir ikili diziye çözülür.</span><span class="sxs-lookup"><span data-stu-id="5c106-124">This is decoded to a binary array that is saved as a file on the virtual machine.</span></span>
<span data-ttu-id="5c106-125">İkili dizinin en fazla uzunluğu 65535 bayttır.</span><span class="sxs-lookup"><span data-stu-id="5c106-125">The maximum length of the binary array is 65535 bytes.</span></span>

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

### <span data-ttu-id="5c106-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c106-126">-DefaultProfile</span></span>
<span data-ttu-id="5c106-127">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="5c106-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c106-128">-LinuxConfigurationDisablePasswordAuthentication</span><span class="sxs-lookup"><span data-stu-id="5c106-128">-LinuxConfigurationDisablePasswordAuthentication</span></span>
<span data-ttu-id="5c106-129">Bu cmdlet 'in parola kimlik doğrulamasını devre dışı bırakacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="5c106-129">Indicates that this cmdlet disables password authentication.</span></span>

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

### <span data-ttu-id="5c106-130">-Listener</span><span class="sxs-lookup"><span data-stu-id="5c106-130">-Listener</span></span>
<span data-ttu-id="5c106-131">Windows Uzaktan Yönetim (WinRM) dinleyicilerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="5c106-131">Specifies the Windows Remote Management (WinRM) listeners.</span></span>
<span data-ttu-id="5c106-132">Bu, uzak Windows PowerShell 'i etkinleştirmiştir.</span><span class="sxs-lookup"><span data-stu-id="5c106-132">This enables remote Windows PowerShell.</span></span>
<span data-ttu-id="5c106-133">Dinleyiciyi oluşturmak için Add-AzVmssWinRMListener cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5c106-133">You can use the Add-AzVmssWinRMListener cmdlet to create the listener.</span></span>

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

### <span data-ttu-id="5c106-134">-PublicKey</span><span class="sxs-lookup"><span data-stu-id="5c106-134">-PublicKey</span></span>
<span data-ttu-id="5c106-135">Güvenli Kabuk (SSH) ortak anahtar nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="5c106-135">Specifies the Secure Shell (SSH) public key object.</span></span>
<span data-ttu-id="5c106-136">Nesneyi oluşturmak için Add-AzVMSshPublicKey cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5c106-136">You can use the Add-AzVMSshPublicKey cmdlet to create the object.</span></span>

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

### <span data-ttu-id="5c106-137">-Parola</span><span class="sxs-lookup"><span data-stu-id="5c106-137">-Secret</span></span>
<span data-ttu-id="5c106-138">Sanal makineye yerleştirilecek sertifika başvurularını içeren gizli nesne türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="5c106-138">Specifies the secrets object which contains the certificate references to place on the virtual machine.</span></span>
<span data-ttu-id="5c106-139">Gizli nesneleri oluşturmak için Add-AzVmssSecret cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5c106-139">You can use the Add-AzVmssSecret cmdlet to create the secrets object.</span></span>

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

### <span data-ttu-id="5c106-140">-TimeZone</span><span class="sxs-lookup"><span data-stu-id="5c106-140">-TimeZone</span></span>
<span data-ttu-id="5c106-141">Sanal makinenin saat dilimini belirtir.</span><span class="sxs-lookup"><span data-stu-id="5c106-141">Specifies the time zone for the virtual machine.</span></span>

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

### <span data-ttu-id="5c106-142">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="5c106-142">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="5c106-143">VMSS nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="5c106-143">Specifies the VMSS object.</span></span>
<span data-ttu-id="5c106-144">Nesneyi oluşturmak için New-AzVmssConfig cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5c106-144">You can use the New-AzVmssConfig cmdlet to create the object.</span></span>

```yaml
Type: PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5c106-145">-WindowsConfigurationEnableAutomaticUpdate</span><span class="sxs-lookup"><span data-stu-id="5c106-145">-WindowsConfigurationEnableAutomaticUpdate</span></span>
<span data-ttu-id="5c106-146">VMSS 'deki sanal makinelerin otomatik güncelleştirmeler için etkinleştirilip etkinleştirilmediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="5c106-146">Indicates whether the virtual machines in the VMSS are enabled for automatic updates.</span></span>

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

### <span data-ttu-id="5c106-147">-WindowsConfigurationProvisionVMAgent</span><span class="sxs-lookup"><span data-stu-id="5c106-147">-WindowsConfigurationProvisionVMAgent</span></span>
<span data-ttu-id="5c106-148">VMSS 'deki sanal makinelerde sanal makine aracısının sağlanması gerekip gerekmediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="5c106-148">Indicates whether virtual machine agent should be provisioned on the virtual machines in the VMSS.</span></span>

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

### <span data-ttu-id="5c106-149">-Onay</span><span class="sxs-lookup"><span data-stu-id="5c106-149">-Confirm</span></span>
<span data-ttu-id="5c106-150">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="5c106-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5c106-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5c106-151">-WhatIf</span></span>
<span data-ttu-id="5c106-152">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="5c106-152">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5c106-153">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="5c106-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5c106-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c106-154">CommonParameters</span></span>
<span data-ttu-id="5c106-155">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5c106-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c106-156">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5c106-156">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c106-157">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5c106-157">INPUTS</span></span>

### <span data-ttu-id="5c106-158">VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="5c106-158">VirtualMachineScaleSet</span></span>
<span data-ttu-id="5c106-159">' VirtualMachineScaleSet ' parametresi ardışık düzen için ' VirtualMachineScaleSet ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="5c106-159">Parameter 'VirtualMachineScaleSet' accepts value of type 'VirtualMachineScaleSet' from the pipeline</span></span>

## <span data-ttu-id="5c106-160">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5c106-160">OUTPUTS</span></span>

### <span data-ttu-id="5c106-161">Bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="5c106-161">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="5c106-162">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5c106-162">NOTES</span></span>

## <span data-ttu-id="5c106-163">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5c106-163">RELATED LINKS</span></span>

[<span data-ttu-id="5c106-164">Add-AzVMAdditionalUnattendContent</span><span class="sxs-lookup"><span data-stu-id="5c106-164">Add-AzVMAdditionalUnattendContent</span></span>](./Add-AzVMAdditionalUnattendContent.md)

[<span data-ttu-id="5c106-165">Add-AzVmssWinRMListener</span><span class="sxs-lookup"><span data-stu-id="5c106-165">Add-AzVmssWinRMListener</span></span>](./Add-AzVmssWinRMListener.md)

[<span data-ttu-id="5c106-166">Add-AzVMSshPublicKey</span><span class="sxs-lookup"><span data-stu-id="5c106-166">Add-AzVMSshPublicKey</span></span>](./Add-AzVMSshPublicKey.md)

[<span data-ttu-id="5c106-167">Add-AzVmssSecret</span><span class="sxs-lookup"><span data-stu-id="5c106-167">Add-AzVmssSecret</span></span>](./Add-AzVmssSecret.md)

[<span data-ttu-id="5c106-168">Yeni-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="5c106-168">New-AzVmssConfig</span></span>](./New-AzVmssConfig.md)


