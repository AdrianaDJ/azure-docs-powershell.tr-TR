---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 3E7B9EFA-8BC2-46EB-9AD7-43EAB7FF3891
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVmssOsProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVmssOsProfile.md
ms.openlocfilehash: 59a50a9138cec99aae8c9f999bf1fa7415655d2b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93586918"
---
# <span data-ttu-id="cc25d-101">Set-AzureRmVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="cc25d-101">Set-AzureRmVmssOsProfile</span></span>

## <span data-ttu-id="cc25d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cc25d-102">SYNOPSIS</span></span>
<span data-ttu-id="cc25d-103">VMSS işletim sistemi profili özelliklerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="cc25d-103">Sets the VMSS operating system profile properties.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cc25d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="cc25d-104">SYNTAX</span></span>

```
Set-AzureRmVmssOsProfile [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-ComputerNamePrefix] <String>]
 [[-AdminUsername] <String>] [[-AdminPassword] <String>] [[-CustomData] <String>]
 [[-WindowsConfigurationProvisionVMAgent] <Boolean>] [[-WindowsConfigurationEnableAutomaticUpdate] <Boolean>]
 [[-TimeZone] <String>] [[-AdditionalUnattendContent] <AdditionalUnattendContent[]>]
 [[-Listener] <WinRMListener[]>] [[-LinuxConfigurationDisablePasswordAuthentication] <Boolean>]
 [[-PublicKey] <SshPublicKey[]>] [[-Secret] <VaultSecretGroup[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cc25d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="cc25d-105">DESCRIPTION</span></span>
<span data-ttu-id="cc25d-106">**Set-AzureRmVmssOsProfile** cmdlet 'ı, sanal makine ölçeğini ayarlama işletim sistemi profili özelliklerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="cc25d-106">The **Set-AzureRmVmssOsProfile** cmdlet sets the Virtual Machine Scale Set operating system profile properties.</span></span>

## <span data-ttu-id="cc25d-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="cc25d-107">EXAMPLES</span></span>

### <span data-ttu-id="cc25d-108">Örnek 1: bir VMSS için işletim sistemi profili özelliklerini ayarlama</span><span class="sxs-lookup"><span data-stu-id="cc25d-108">Example 1: Set the operating system profile properties for a VMSS</span></span>
```
PS C:\> Set-AzureRmVmssOSProfile -VirtualMachineScaleSet "ContosoVMSS" -ComputerNamePrefix "Test" -AdminUsername $AdminUsername -AdminPassword $AdminPassword
```

<span data-ttu-id="cc25d-109">Bu komut, ContosoVMSS adlı VMSS 'ye ait sanal makinelerin işletim sistemi profili özelliklerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="cc25d-109">This command sets operating system profile properties for the virtual machines that belong to the VMSS named ContosoVMSS.</span></span>
<span data-ttu-id="cc25d-110">Bu komut, VMSS 'deki tüm sanal makine örneklerinin bilgisayar adı önekini, yöneticinin kullanıcı adını ve parolasını test etmek üzere ayarlar.</span><span class="sxs-lookup"><span data-stu-id="cc25d-110">The command sets the computer name prefix for all the virtual machine instances in the VMSS to Test and supplies the administrator username and password.</span></span>

## <span data-ttu-id="cc25d-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="cc25d-111">PARAMETERS</span></span>

### <span data-ttu-id="cc25d-112">-Additionalunattenvseçcontent</span><span class="sxs-lookup"><span data-stu-id="cc25d-112">-AdditionalUnattendContent</span></span>
<span data-ttu-id="cc25d-113">Bir katılımsız içerik nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="cc25d-113">Specifies an unattended content object.</span></span>
<span data-ttu-id="cc25d-114">Nesneyi oluşturmak için Add-AzureRmVMAdditionalUnattendContent kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="cc25d-114">You can use the Add-AzureRmVMAdditionalUnattendContent to create the object.</span></span>

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

### <span data-ttu-id="cc25d-115">-AdminPassword</span><span class="sxs-lookup"><span data-stu-id="cc25d-115">-AdminPassword</span></span>
<span data-ttu-id="cc25d-116">VMSS 'deki tüm sanal makine örnekleri için kullanılacak yönetici parolasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="cc25d-116">Specifies the administrator password to use for all the virtual machine instances in the VMSS.</span></span>

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

### <span data-ttu-id="cc25d-117">-AdminUsername</span><span class="sxs-lookup"><span data-stu-id="cc25d-117">-AdminUsername</span></span>
<span data-ttu-id="cc25d-118">VMSS 'deki tüm sanal makine örnekleri için kullanılacak yönetici hesap adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="cc25d-118">Specifies the administrator account name to use for all the virtual machine instances in the VMSS.</span></span>

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

### <span data-ttu-id="cc25d-119">-ComputerNamePrefix</span><span class="sxs-lookup"><span data-stu-id="cc25d-119">-ComputerNamePrefix</span></span>
<span data-ttu-id="cc25d-120">VMSS 'deki tüm sanal makine örneklerinin bilgisayar adı önekini belirtir.</span><span class="sxs-lookup"><span data-stu-id="cc25d-120">Specifies the computer name prefix for all the virtual machine instances in the VMSS.</span></span>
<span data-ttu-id="cc25d-121">Bilgisayar adları 1-15 karakter uzunluğunda olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="cc25d-121">Computer names must be 1 to 15 characters long.</span></span>

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

### <span data-ttu-id="cc25d-122">-CustomData</span><span class="sxs-lookup"><span data-stu-id="cc25d-122">-CustomData</span></span>
<span data-ttu-id="cc25d-123">Özel verilerin Base-64 kodlu dizesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="cc25d-123">Specifies a base-64 encoded string of custom data.</span></span>
<span data-ttu-id="cc25d-124">Bu, sanal makinede dosya olarak kaydedilmiş bir ikili diziye çözülür.</span><span class="sxs-lookup"><span data-stu-id="cc25d-124">This is decoded to a binary array that is saved as a file on the virtual machine.</span></span>
<span data-ttu-id="cc25d-125">İkili dizinin en fazla uzunluğu 65535 bayttır.</span><span class="sxs-lookup"><span data-stu-id="cc25d-125">The maximum length of the binary array is 65535 bytes.</span></span>

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

### <span data-ttu-id="cc25d-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc25d-126">-DefaultProfile</span></span>
<span data-ttu-id="cc25d-127">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="cc25d-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc25d-128">-LinuxConfigurationDisablePasswordAuthentication</span><span class="sxs-lookup"><span data-stu-id="cc25d-128">-LinuxConfigurationDisablePasswordAuthentication</span></span>
<span data-ttu-id="cc25d-129">Bu cmdlet 'in parola kimlik doğrulamasını devre dışı bırakacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="cc25d-129">Indicates that this cmdlet disables password authentication.</span></span>

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

### <span data-ttu-id="cc25d-130">-Listener</span><span class="sxs-lookup"><span data-stu-id="cc25d-130">-Listener</span></span>
<span data-ttu-id="cc25d-131">Windows Uzaktan Yönetim (WinRM) dinleyicilerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="cc25d-131">Specifies the Windows Remote Management (WinRM) listeners.</span></span>
<span data-ttu-id="cc25d-132">Bu, uzak Windows PowerShell 'i etkinleştirmiştir.</span><span class="sxs-lookup"><span data-stu-id="cc25d-132">This enables remote Windows PowerShell.</span></span>
<span data-ttu-id="cc25d-133">Dinleyiciyi oluşturmak için Add-AzureRmVmssWinRMListener cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="cc25d-133">You can use the Add-AzureRmVmssWinRMListener cmdlet to create the listener.</span></span>

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

### <span data-ttu-id="cc25d-134">-PublicKey</span><span class="sxs-lookup"><span data-stu-id="cc25d-134">-PublicKey</span></span>
<span data-ttu-id="cc25d-135">Güvenli Kabuk (SSH) ortak anahtar nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="cc25d-135">Specifies the Secure Shell (SSH) public key object.</span></span>
<span data-ttu-id="cc25d-136">Nesneyi oluşturmak için Add-AzureRmVMSshPublicKey cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="cc25d-136">You can use the Add-AzureRmVMSshPublicKey cmdlet to create the object.</span></span>

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

### <span data-ttu-id="cc25d-137">-Parola</span><span class="sxs-lookup"><span data-stu-id="cc25d-137">-Secret</span></span>
<span data-ttu-id="cc25d-138">Sanal makineye yerleştirilecek sertifika başvurularını içeren gizli nesne türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="cc25d-138">Specifies the secrets object which contains the certificate references to place on the virtual machine.</span></span>
<span data-ttu-id="cc25d-139">Gizli nesneleri oluşturmak için Add-AzureRmVmssSecret cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="cc25d-139">You can use the Add-AzureRmVmssSecret cmdlet to create the secrets object.</span></span>

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

### <span data-ttu-id="cc25d-140">-TimeZone</span><span class="sxs-lookup"><span data-stu-id="cc25d-140">-TimeZone</span></span>
<span data-ttu-id="cc25d-141">Sanal makinenin saat dilimini belirtir.</span><span class="sxs-lookup"><span data-stu-id="cc25d-141">Specifies the time zone for the virtual machine.</span></span>

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

### <span data-ttu-id="cc25d-142">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="cc25d-142">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="cc25d-143">VMSS nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="cc25d-143">Specifies the VMSS object.</span></span>
<span data-ttu-id="cc25d-144">Nesneyi oluşturmak için New-AzureRmVmssConfig cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="cc25d-144">You can use the New-AzureRmVmssConfig cmdlet to create the object.</span></span>

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

### <span data-ttu-id="cc25d-145">-WindowsConfigurationEnableAutomaticUpdate</span><span class="sxs-lookup"><span data-stu-id="cc25d-145">-WindowsConfigurationEnableAutomaticUpdate</span></span>
<span data-ttu-id="cc25d-146">VMSS 'deki sanal makinelerin otomatik güncelleştirmeler için etkinleştirilip etkinleştirilmediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="cc25d-146">Indicates whether the virtual machines in the VMSS are enabled for automatic updates.</span></span>

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

### <span data-ttu-id="cc25d-147">-WindowsConfigurationProvisionVMAgent</span><span class="sxs-lookup"><span data-stu-id="cc25d-147">-WindowsConfigurationProvisionVMAgent</span></span>
<span data-ttu-id="cc25d-148">VMSS 'deki sanal makinelerde sanal makine aracısının sağlanması gerekip gerekmediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="cc25d-148">Indicates whether virtual machine agent should be provisioned on the virtual machines in the VMSS.</span></span>

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

### <span data-ttu-id="cc25d-149">-Onay</span><span class="sxs-lookup"><span data-stu-id="cc25d-149">-Confirm</span></span>
<span data-ttu-id="cc25d-150">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="cc25d-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cc25d-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cc25d-151">-WhatIf</span></span>
<span data-ttu-id="cc25d-152">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="cc25d-152">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cc25d-153">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="cc25d-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cc25d-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc25d-154">CommonParameters</span></span>
<span data-ttu-id="cc25d-155">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="cc25d-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc25d-156">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cc25d-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc25d-157">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="cc25d-157">INPUTS</span></span>

## <span data-ttu-id="cc25d-158">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="cc25d-158">OUTPUTS</span></span>

### <span data-ttu-id="cc25d-159">Bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="cc25d-159">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="cc25d-160">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="cc25d-160">NOTES</span></span>

## <span data-ttu-id="cc25d-161">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="cc25d-161">RELATED LINKS</span></span>

[<span data-ttu-id="cc25d-162">Add-AzureRmVMAdditionalUnattendContent</span><span class="sxs-lookup"><span data-stu-id="cc25d-162">Add-AzureRmVMAdditionalUnattendContent</span></span>](./Add-AzureRmVMAdditionalUnattendContent.md)

[<span data-ttu-id="cc25d-163">Add-AzureRmVmssWinRMListener</span><span class="sxs-lookup"><span data-stu-id="cc25d-163">Add-AzureRmVmssWinRMListener</span></span>](./Add-AzureRmVmssWinRMListener.md)

[<span data-ttu-id="cc25d-164">Add-AzureRmVMSshPublicKey</span><span class="sxs-lookup"><span data-stu-id="cc25d-164">Add-AzureRmVMSshPublicKey</span></span>](./Add-AzureRmVMSshPublicKey.md)

[<span data-ttu-id="cc25d-165">Add-AzureRmVmssSecret</span><span class="sxs-lookup"><span data-stu-id="cc25d-165">Add-AzureRmVmssSecret</span></span>](./Add-AzureRmVmssSecret.md)

[<span data-ttu-id="cc25d-166">Yeni-AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="cc25d-166">New-AzureRmVmssConfig</span></span>](./New-AzureRmVmssConfig.md)


