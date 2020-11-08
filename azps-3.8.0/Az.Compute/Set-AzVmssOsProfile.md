---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 3E7B9EFA-8BC2-46EB-9AD7-43EAB7FF3891
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmssosprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssOsProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssOsProfile.md
ms.openlocfilehash: 3d3fdb53bf6dd0338f89bd03f11786bc9942acaa
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94104610"
---
# <span data-ttu-id="27799-101">Set-AzVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="27799-101">Set-AzVmssOsProfile</span></span>

## <span data-ttu-id="27799-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="27799-102">SYNOPSIS</span></span>
<span data-ttu-id="27799-103">VMSS işletim sistemi profili özelliklerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="27799-103">Sets the VMSS operating system profile properties.</span></span>

## <span data-ttu-id="27799-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="27799-104">SYNTAX</span></span>

```
Set-AzVmssOsProfile [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-ComputerNamePrefix] <String>]
 [[-AdminUsername] <String>] [[-AdminPassword] <String>] [[-CustomData] <String>]
 [[-WindowsConfigurationProvisionVMAgent] <Boolean>] [[-WindowsConfigurationEnableAutomaticUpdate] <Boolean>]
 [[-TimeZone] <String>] [[-AdditionalUnattendContent] <AdditionalUnattendContent[]>]
 [[-Listener] <WinRMListener[]>] [[-LinuxConfigurationDisablePasswordAuthentication] <Boolean>]
 [[-PublicKey] <SshPublicKey[]>] [[-Secret] <VaultSecretGroup[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="27799-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="27799-105">DESCRIPTION</span></span>
<span data-ttu-id="27799-106">**Set-AzVmssOsProfile** cmdlet 'ı, sanal makine ölçeğini ayarlama işletim sistemi profili özelliklerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="27799-106">The **Set-AzVmssOsProfile** cmdlet sets the Virtual Machine Scale Set operating system profile properties.</span></span>

## <span data-ttu-id="27799-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="27799-107">EXAMPLES</span></span>

### <span data-ttu-id="27799-108">Örnek 1: bir VMSS için işletim sistemi profili özelliklerini ayarlama</span><span class="sxs-lookup"><span data-stu-id="27799-108">Example 1: Set the operating system profile properties for a VMSS</span></span>
```
PS C:\> Set-AzVmssOSProfile -VirtualMachineScaleSet "ContosoVMSS" -ComputerNamePrefix "Test" -AdminUsername $AdminUsername -AdminPassword $AdminPassword
```

<span data-ttu-id="27799-109">Bu komut, ContosoVMSS adlı VMSS 'ye ait sanal makinelerin işletim sistemi profili özelliklerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="27799-109">This command sets operating system profile properties for the virtual machines that belong to the VMSS named ContosoVMSS.</span></span>
<span data-ttu-id="27799-110">Bu komut, VMSS 'deki tüm sanal makine örneklerinin bilgisayar adı önekini, yöneticinin kullanıcı adını ve parolasını test etmek üzere ayarlar.</span><span class="sxs-lookup"><span data-stu-id="27799-110">The command sets the computer name prefix for all the virtual machine instances in the VMSS to Test and supplies the administrator username and password.</span></span>

## <span data-ttu-id="27799-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="27799-111">PARAMETERS</span></span>

### <span data-ttu-id="27799-112">-Additionalunattenvseçcontent</span><span class="sxs-lookup"><span data-stu-id="27799-112">-AdditionalUnattendContent</span></span>
<span data-ttu-id="27799-113">Bir katılımsız içerik nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="27799-113">Specifies an unattended content object.</span></span>
<span data-ttu-id="27799-114">Nesneyi oluşturmak için Add-AzVMAdditionalUnattendContent kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="27799-114">You can use the Add-AzVMAdditionalUnattendContent to create the object.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.AdditionalUnattendContent[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27799-115">-AdminPassword</span><span class="sxs-lookup"><span data-stu-id="27799-115">-AdminPassword</span></span>
<span data-ttu-id="27799-116">VMSS 'deki tüm sanal makine örnekleri için kullanılacak yönetici parolasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="27799-116">Specifies the administrator password to use for all the virtual machine instances in the VMSS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27799-117">-AdminUsername</span><span class="sxs-lookup"><span data-stu-id="27799-117">-AdminUsername</span></span>
<span data-ttu-id="27799-118">VMSS 'deki tüm sanal makine örnekleri için kullanılacak yönetici hesap adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="27799-118">Specifies the administrator account name to use for all the virtual machine instances in the VMSS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27799-119">-ComputerNamePrefix</span><span class="sxs-lookup"><span data-stu-id="27799-119">-ComputerNamePrefix</span></span>
<span data-ttu-id="27799-120">VMSS 'deki tüm sanal makine örneklerinin bilgisayar adı önekini belirtir.</span><span class="sxs-lookup"><span data-stu-id="27799-120">Specifies the computer name prefix for all the virtual machine instances in the VMSS.</span></span>
<span data-ttu-id="27799-121">Bilgisayar adları 1-15 karakter uzunluğunda olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="27799-121">Computer names must be 1 to 15 characters long.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27799-122">-CustomData</span><span class="sxs-lookup"><span data-stu-id="27799-122">-CustomData</span></span>
<span data-ttu-id="27799-123">Özel verilerin Base-64 kodlu dizesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="27799-123">Specifies a base-64 encoded string of custom data.</span></span>
<span data-ttu-id="27799-124">Bu, sanal makinede dosya olarak kaydedilmiş bir ikili diziye çözülür.</span><span class="sxs-lookup"><span data-stu-id="27799-124">This is decoded to a binary array that is saved as a file on the virtual machine.</span></span>
<span data-ttu-id="27799-125">İkili dizinin en fazla uzunluğu 65535 bayttır.</span><span class="sxs-lookup"><span data-stu-id="27799-125">The maximum length of the binary array is 65535 bytes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27799-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27799-126">-DefaultProfile</span></span>
<span data-ttu-id="27799-127">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="27799-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27799-128">-LinuxConfigurationDisablePasswordAuthentication</span><span class="sxs-lookup"><span data-stu-id="27799-128">-LinuxConfigurationDisablePasswordAuthentication</span></span>
<span data-ttu-id="27799-129">Bu cmdlet 'in parola kimlik doğrulamasını devre dışı bırakacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="27799-129">Indicates that this cmdlet disables password authentication.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27799-130">-Listener</span><span class="sxs-lookup"><span data-stu-id="27799-130">-Listener</span></span>
<span data-ttu-id="27799-131">Windows Uzaktan Yönetim (WinRM) dinleyicilerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="27799-131">Specifies the Windows Remote Management (WinRM) listeners.</span></span>
<span data-ttu-id="27799-132">Bu, uzak Windows PowerShell 'i etkinleştirmiştir.</span><span class="sxs-lookup"><span data-stu-id="27799-132">This enables remote Windows PowerShell.</span></span>
<span data-ttu-id="27799-133">Dinleyiciyi oluşturmak için Add-AzVmssWinRMListener cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="27799-133">You can use the Add-AzVmssWinRMListener cmdlet to create the listener.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.WinRMListener[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27799-134">-PublicKey</span><span class="sxs-lookup"><span data-stu-id="27799-134">-PublicKey</span></span>
<span data-ttu-id="27799-135">Güvenli Kabuk (SSH) ortak anahtar nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="27799-135">Specifies the Secure Shell (SSH) public key object.</span></span>
<span data-ttu-id="27799-136">Nesneyi oluşturmak için Add-AzVMSshPublicKey cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="27799-136">You can use the Add-AzVMSshPublicKey cmdlet to create the object.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.SshPublicKey[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 11
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27799-137">-Parola</span><span class="sxs-lookup"><span data-stu-id="27799-137">-Secret</span></span>
<span data-ttu-id="27799-138">Sanal makineye yerleştirilecek sertifika başvurularını içeren gizli nesne türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="27799-138">Specifies the secrets object which contains the certificate references to place on the virtual machine.</span></span>
<span data-ttu-id="27799-139">Gizli nesneleri oluşturmak için Add-AzVmssSecret cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="27799-139">You can use the Add-AzVmssSecret cmdlet to create the secrets object.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.VaultSecretGroup[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 12
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27799-140">-TimeZone</span><span class="sxs-lookup"><span data-stu-id="27799-140">-TimeZone</span></span>
<span data-ttu-id="27799-141">Sanal makinenin saat dilimini belirtir.</span><span class="sxs-lookup"><span data-stu-id="27799-141">Specifies the time zone for the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27799-142">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="27799-142">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="27799-143">VMSS nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="27799-143">Specifies the VMSS object.</span></span>
<span data-ttu-id="27799-144">Nesneyi oluşturmak için New-AzVmssConfig cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="27799-144">You can use the New-AzVmssConfig cmdlet to create the object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="27799-145">-WindowsConfigurationEnableAutomaticUpdate</span><span class="sxs-lookup"><span data-stu-id="27799-145">-WindowsConfigurationEnableAutomaticUpdate</span></span>
<span data-ttu-id="27799-146">VMSS 'deki sanal makinelerin otomatik güncelleştirmeler için etkinleştirilip etkinleştirilmediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="27799-146">Indicates whether the virtual machines in the VMSS are enabled for automatic updates.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27799-147">-WindowsConfigurationProvisionVMAgent</span><span class="sxs-lookup"><span data-stu-id="27799-147">-WindowsConfigurationProvisionVMAgent</span></span>
<span data-ttu-id="27799-148">VMSS 'deki sanal makinelerde sanal makine aracısının sağlanması gerekip gerekmediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="27799-148">Indicates whether virtual machine agent should be provisioned on the virtual machines in the VMSS.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27799-149">-Onay</span><span class="sxs-lookup"><span data-stu-id="27799-149">-Confirm</span></span>
<span data-ttu-id="27799-150">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="27799-150">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27799-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="27799-151">-WhatIf</span></span>
<span data-ttu-id="27799-152">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="27799-152">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="27799-153">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="27799-153">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27799-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27799-154">CommonParameters</span></span>
<span data-ttu-id="27799-155">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="27799-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27799-156">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="27799-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27799-157">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="27799-157">INPUTS</span></span>

### <span data-ttu-id="27799-158">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="27799-158">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="27799-159">System. String</span><span class="sxs-lookup"><span data-stu-id="27799-159">System.String</span></span>

### <span data-ttu-id="27799-160">System. Nullable ' 1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85vseç7val 7798e]]</span><span class="sxs-lookup"><span data-stu-id="27799-160">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="27799-161">Microsoft. Azure. Management. COMPUTE. modeller. Addiunattenvseçcontent []</span><span class="sxs-lookup"><span data-stu-id="27799-161">Microsoft.Azure.Management.Compute.Models.AdditionalUnattendContent[]</span></span>

### <span data-ttu-id="27799-162">Microsoft. Azure. Management. COMPUTE. model. WinRMListener []</span><span class="sxs-lookup"><span data-stu-id="27799-162">Microsoft.Azure.Management.Compute.Models.WinRMListener[]</span></span>

### <span data-ttu-id="27799-163">Microsoft. Azure. Management. COMPUTE. model. SshPublicKey []</span><span class="sxs-lookup"><span data-stu-id="27799-163">Microsoft.Azure.Management.Compute.Models.SshPublicKey[]</span></span>

### <span data-ttu-id="27799-164">Microsoft. Azure. Management. COMPUTE. modeller. VaultSecretGroup []</span><span class="sxs-lookup"><span data-stu-id="27799-164">Microsoft.Azure.Management.Compute.Models.VaultSecretGroup[]</span></span>

## <span data-ttu-id="27799-165">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="27799-165">OUTPUTS</span></span>

### <span data-ttu-id="27799-166">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="27799-166">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="27799-167">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="27799-167">NOTES</span></span>

## <span data-ttu-id="27799-168">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="27799-168">RELATED LINKS</span></span>

[<span data-ttu-id="27799-169">Add-AzVMAdditionalUnattendContent</span><span class="sxs-lookup"><span data-stu-id="27799-169">Add-AzVMAdditionalUnattendContent</span></span>](./Add-AzVMAdditionalUnattendContent.md)

[<span data-ttu-id="27799-170">Add-AzVmssWinRMListener</span><span class="sxs-lookup"><span data-stu-id="27799-170">Add-AzVmssWinRMListener</span></span>](./Add-AzVmssWinRMListener.md)

[<span data-ttu-id="27799-171">Add-AzVMSshPublicKey</span><span class="sxs-lookup"><span data-stu-id="27799-171">Add-AzVMSshPublicKey</span></span>](./Add-AzVMSshPublicKey.md)

[<span data-ttu-id="27799-172">Add-AzVmssSecret</span><span class="sxs-lookup"><span data-stu-id="27799-172">Add-AzVmssSecret</span></span>](./Add-AzVmssSecret.md)

[<span data-ttu-id="27799-173">Yeni-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="27799-173">New-AzVmssConfig</span></span>](./New-AzVmssConfig.md)


