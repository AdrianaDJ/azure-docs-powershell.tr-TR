---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 3E7B9EFA-8BC2-46EB-9AD7-43EAB7FF3891
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmssosprofile
schema: 2.0.0
ms.openlocfilehash: ff2b46c661640221326d50aa71c2659bd5672ab1
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939404"
---
# <span data-ttu-id="75c52-101">Set-AzureRmVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="75c52-101">Set-AzureRmVmssOsProfile</span></span>

## <span data-ttu-id="75c52-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="75c52-102">SYNOPSIS</span></span>
<span data-ttu-id="75c52-103">VMSS işletim sistemi profili özelliklerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="75c52-103">Sets the VMSS operating system profile properties.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="75c52-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="75c52-104">SYNTAX</span></span>

```
Set-AzureRmVmssOsProfile [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-ComputerNamePrefix] <String>]
 [[-AdminUsername] <String>] [[-AdminPassword] <String>] [[-CustomData] <String>]
 [[-WindowsConfigurationProvisionVMAgent] <Boolean>] [[-WindowsConfigurationEnableAutomaticUpdate] <Boolean>]
 [[-TimeZone] <String>] [[-AdditionalUnattendContent] <AdditionalUnattendContent[]>]
 [[-Listener] <WinRMListener[]>] [[-LinuxConfigurationDisablePasswordAuthentication] <Boolean>]
 [[-PublicKey] <SshPublicKey[]>] [[-Secret] <VaultSecretGroup[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="75c52-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="75c52-105">DESCRIPTION</span></span>
<span data-ttu-id="75c52-106">**Set-AzureRmVmssOsProfile** cmdlet 'ı, sanal makine ölçeğini ayarlama işletim sistemi profili özelliklerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="75c52-106">The **Set-AzureRmVmssOsProfile** cmdlet sets the Virtual Machine Scale Set operating system profile properties.</span></span>

## <span data-ttu-id="75c52-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="75c52-107">EXAMPLES</span></span>

### <span data-ttu-id="75c52-108">Örnek 1: bir VMSS için işletim sistemi profili özelliklerini ayarlama</span><span class="sxs-lookup"><span data-stu-id="75c52-108">Example 1: Set the operating system profile properties for a VMSS</span></span>
```
PS C:\> Set-AzureRmVmssOSProfile -VirtualMachineScaleSet "ContosoVMSS" -ComputerNamePrefix "Test" -AdminUsername $AdminUsername -AdminPassword $AdminPassword
```

<span data-ttu-id="75c52-109">Bu komut, ContosoVMSS adlı VMSS 'ye ait sanal makinelerin işletim sistemi profili özelliklerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="75c52-109">This command sets operating system profile properties for the virtual machines that belong to the VMSS named ContosoVMSS.</span></span>
<span data-ttu-id="75c52-110">Bu komut, VMSS 'deki tüm sanal makine örneklerinin bilgisayar adı önekini, yöneticinin kullanıcı adını ve parolasını test etmek üzere ayarlar.</span><span class="sxs-lookup"><span data-stu-id="75c52-110">The command sets the computer name prefix for all the virtual machine instances in the VMSS to Test and supplies the administrator username and password.</span></span>

## <span data-ttu-id="75c52-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="75c52-111">PARAMETERS</span></span>

### <span data-ttu-id="75c52-112">-Additionalunattenvseçcontent</span><span class="sxs-lookup"><span data-stu-id="75c52-112">-AdditionalUnattendContent</span></span>
<span data-ttu-id="75c52-113">Bir katılımsız içerik nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="75c52-113">Specifies an unattended content object.</span></span>
<span data-ttu-id="75c52-114">Nesneyi oluşturmak için Add-AzureRmVMAdditionalUnattendContent kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="75c52-114">You can use the Add-AzureRmVMAdditionalUnattendContent to create the object.</span></span>

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

### <span data-ttu-id="75c52-115">-AdminPassword</span><span class="sxs-lookup"><span data-stu-id="75c52-115">-AdminPassword</span></span>
<span data-ttu-id="75c52-116">VMSS 'deki tüm sanal makine örnekleri için kullanılacak yönetici parolasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="75c52-116">Specifies the administrator password to use for all the virtual machine instances in the VMSS.</span></span>

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

### <span data-ttu-id="75c52-117">-AdminUsername</span><span class="sxs-lookup"><span data-stu-id="75c52-117">-AdminUsername</span></span>
<span data-ttu-id="75c52-118">VMSS 'deki tüm sanal makine örnekleri için kullanılacak yönetici hesap adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="75c52-118">Specifies the administrator account name to use for all the virtual machine instances in the VMSS.</span></span>

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

### <span data-ttu-id="75c52-119">-ComputerNamePrefix</span><span class="sxs-lookup"><span data-stu-id="75c52-119">-ComputerNamePrefix</span></span>
<span data-ttu-id="75c52-120">VMSS 'deki tüm sanal makine örneklerinin bilgisayar adı önekini belirtir.</span><span class="sxs-lookup"><span data-stu-id="75c52-120">Specifies the computer name prefix for all the virtual machine instances in the VMSS.</span></span>
<span data-ttu-id="75c52-121">Bilgisayar adları 1-15 karakter uzunluğunda olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="75c52-121">Computer names must be 1 to 15 characters long.</span></span>

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

### <span data-ttu-id="75c52-122">-CustomData</span><span class="sxs-lookup"><span data-stu-id="75c52-122">-CustomData</span></span>
<span data-ttu-id="75c52-123">Özel verilerin Base-64 kodlu dizesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="75c52-123">Specifies a base-64 encoded string of custom data.</span></span>
<span data-ttu-id="75c52-124">Bu, sanal makinede dosya olarak kaydedilmiş bir ikili diziye çözülür.</span><span class="sxs-lookup"><span data-stu-id="75c52-124">This is decoded to a binary array that is saved as a file on the virtual machine.</span></span>
<span data-ttu-id="75c52-125">İkili dizinin en fazla uzunluğu 65535 bayttır.</span><span class="sxs-lookup"><span data-stu-id="75c52-125">The maximum length of the binary array is 65535 bytes.</span></span>

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

### <span data-ttu-id="75c52-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75c52-126">-DefaultProfile</span></span>
<span data-ttu-id="75c52-127">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="75c52-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="75c52-128">-LinuxConfigurationDisablePasswordAuthentication</span><span class="sxs-lookup"><span data-stu-id="75c52-128">-LinuxConfigurationDisablePasswordAuthentication</span></span>
<span data-ttu-id="75c52-129">Bu cmdlet 'in parola kimlik doğrulamasını devre dışı bırakacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="75c52-129">Indicates that this cmdlet disables password authentication.</span></span>

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

### <span data-ttu-id="75c52-130">-Listener</span><span class="sxs-lookup"><span data-stu-id="75c52-130">-Listener</span></span>
<span data-ttu-id="75c52-131">Windows Uzaktan Yönetim (WinRM) dinleyicilerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="75c52-131">Specifies the Windows Remote Management (WinRM) listeners.</span></span>
<span data-ttu-id="75c52-132">Bu, uzak Windows PowerShell 'i etkinleştirmiştir.</span><span class="sxs-lookup"><span data-stu-id="75c52-132">This enables remote Windows PowerShell.</span></span>
<span data-ttu-id="75c52-133">Dinleyiciyi oluşturmak için Add-AzureRmVmssWinRMListener cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="75c52-133">You can use the Add-AzureRmVmssWinRMListener cmdlet to create the listener.</span></span>

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

### <span data-ttu-id="75c52-134">-PublicKey</span><span class="sxs-lookup"><span data-stu-id="75c52-134">-PublicKey</span></span>
<span data-ttu-id="75c52-135">Güvenli Kabuk (SSH) ortak anahtar nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="75c52-135">Specifies the Secure Shell (SSH) public key object.</span></span>
<span data-ttu-id="75c52-136">Nesneyi oluşturmak için Add-AzureRmVMSshPublicKey cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="75c52-136">You can use the Add-AzureRmVMSshPublicKey cmdlet to create the object.</span></span>

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

### <span data-ttu-id="75c52-137">-Parola</span><span class="sxs-lookup"><span data-stu-id="75c52-137">-Secret</span></span>
<span data-ttu-id="75c52-138">Sanal makineye yerleştirilecek sertifika başvurularını içeren gizli nesne türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="75c52-138">Specifies the secrets object which contains the certificate references to place on the virtual machine.</span></span>
<span data-ttu-id="75c52-139">Gizli nesneleri oluşturmak için Add-AzureRmVmssSecret cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="75c52-139">You can use the Add-AzureRmVmssSecret cmdlet to create the secrets object.</span></span>

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

### <span data-ttu-id="75c52-140">-TimeZone</span><span class="sxs-lookup"><span data-stu-id="75c52-140">-TimeZone</span></span>
<span data-ttu-id="75c52-141">Sanal makinenin saat dilimini belirtir.</span><span class="sxs-lookup"><span data-stu-id="75c52-141">Specifies the time zone for the virtual machine.</span></span>

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

### <span data-ttu-id="75c52-142">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="75c52-142">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="75c52-143">VMSS nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="75c52-143">Specifies the VMSS object.</span></span>
<span data-ttu-id="75c52-144">Nesneyi oluşturmak için New-AzureRmVmssConfig cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="75c52-144">You can use the New-AzureRmVmssConfig cmdlet to create the object.</span></span>

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

### <span data-ttu-id="75c52-145">-WindowsConfigurationEnableAutomaticUpdate</span><span class="sxs-lookup"><span data-stu-id="75c52-145">-WindowsConfigurationEnableAutomaticUpdate</span></span>
<span data-ttu-id="75c52-146">VMSS 'deki sanal makinelerin otomatik güncelleştirmeler için etkinleştirilip etkinleştirilmediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="75c52-146">Indicates whether the virtual machines in the VMSS are enabled for automatic updates.</span></span>

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

### <span data-ttu-id="75c52-147">-WindowsConfigurationProvisionVMAgent</span><span class="sxs-lookup"><span data-stu-id="75c52-147">-WindowsConfigurationProvisionVMAgent</span></span>
<span data-ttu-id="75c52-148">VMSS 'deki sanal makinelerde sanal makine aracısının sağlanması gerekip gerekmediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="75c52-148">Indicates whether virtual machine agent should be provisioned on the virtual machines in the VMSS.</span></span>

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

### <span data-ttu-id="75c52-149">-Onay</span><span class="sxs-lookup"><span data-stu-id="75c52-149">-Confirm</span></span>
<span data-ttu-id="75c52-150">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="75c52-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="75c52-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="75c52-151">-WhatIf</span></span>
<span data-ttu-id="75c52-152">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="75c52-152">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="75c52-153">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="75c52-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="75c52-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75c52-154">CommonParameters</span></span>
<span data-ttu-id="75c52-155">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="75c52-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75c52-156">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="75c52-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75c52-157">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="75c52-157">INPUTS</span></span>

### <span data-ttu-id="75c52-158">VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="75c52-158">VirtualMachineScaleSet</span></span>
<span data-ttu-id="75c52-159">' VirtualMachineScaleSet ' parametresi ardışık düzen için ' VirtualMachineScaleSet ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="75c52-159">Parameter 'VirtualMachineScaleSet' accepts value of type 'VirtualMachineScaleSet' from the pipeline</span></span>

## <span data-ttu-id="75c52-160">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="75c52-160">OUTPUTS</span></span>

### <span data-ttu-id="75c52-161">Bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="75c52-161">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="75c52-162">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="75c52-162">NOTES</span></span>

## <span data-ttu-id="75c52-163">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="75c52-163">RELATED LINKS</span></span>

[<span data-ttu-id="75c52-164">Add-AzureRmVMAdditionalUnattendContent</span><span class="sxs-lookup"><span data-stu-id="75c52-164">Add-AzureRmVMAdditionalUnattendContent</span></span>](./Add-AzureRmVMAdditionalUnattendContent.md)

[<span data-ttu-id="75c52-165">Add-AzureRmVmssWinRMListener</span><span class="sxs-lookup"><span data-stu-id="75c52-165">Add-AzureRmVmssWinRMListener</span></span>](./Add-AzureRmVmssWinRMListener.md)

[<span data-ttu-id="75c52-166">Add-AzureRmVMSshPublicKey</span><span class="sxs-lookup"><span data-stu-id="75c52-166">Add-AzureRmVMSshPublicKey</span></span>](./Add-AzureRmVMSshPublicKey.md)

[<span data-ttu-id="75c52-167">Add-AzureRmVmssSecret</span><span class="sxs-lookup"><span data-stu-id="75c52-167">Add-AzureRmVmssSecret</span></span>](./Add-AzureRmVmssSecret.md)

[<span data-ttu-id="75c52-168">Yeni-AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="75c52-168">New-AzureRmVmssConfig</span></span>](./New-AzureRmVmssConfig.md)


