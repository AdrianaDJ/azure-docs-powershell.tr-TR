---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 3E7B9EFA-8BC2-46EB-9AD7-43EAB7FF3891
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmssosprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssOsProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssOsProfile.md
ms.openlocfilehash: 71bd8ca26755118a4bb9c075ae89bad765922f3d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94110006"
---
# <span data-ttu-id="4ff06-101">Set-AzVmssOsProfile</span><span class="sxs-lookup"><span data-stu-id="4ff06-101">Set-AzVmssOsProfile</span></span>

## <span data-ttu-id="4ff06-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4ff06-102">SYNOPSIS</span></span>
<span data-ttu-id="4ff06-103">VMSS işletim sistemi profili özelliklerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="4ff06-103">Sets the VMSS operating system profile properties.</span></span>

## <span data-ttu-id="4ff06-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4ff06-104">SYNTAX</span></span>

```
Set-AzVmssOsProfile [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-ComputerNamePrefix] <String>]
 [[-AdminUsername] <String>] [[-AdminPassword] <String>] [[-CustomData] <String>]
 [[-WindowsConfigurationProvisionVMAgent] <Boolean>] [[-WindowsConfigurationEnableAutomaticUpdate] <Boolean>]
 [[-TimeZone] <String>] [[-AdditionalUnattendContent] <AdditionalUnattendContent[]>]
 [[-Listener] <WinRMListener[]>] [[-LinuxConfigurationDisablePasswordAuthentication] <Boolean>]
 [[-PublicKey] <SshPublicKey[]>] [[-Secret] <VaultSecretGroup[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4ff06-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="4ff06-105">DESCRIPTION</span></span>
<span data-ttu-id="4ff06-106">**Set-AzVmssOsProfile** cmdlet 'ı, sanal makine ölçeğini ayarlama işletim sistemi profili özelliklerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="4ff06-106">The **Set-AzVmssOsProfile** cmdlet sets the Virtual Machine Scale Set operating system profile properties.</span></span>

## <span data-ttu-id="4ff06-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4ff06-107">EXAMPLES</span></span>

### <span data-ttu-id="4ff06-108">Örnek 1: bir VMSS için işletim sistemi profili özelliklerini ayarlama</span><span class="sxs-lookup"><span data-stu-id="4ff06-108">Example 1: Set the operating system profile properties for a VMSS</span></span>
```
PS C:\> Set-AzVmssOSProfile -VirtualMachineScaleSet "ContosoVMSS" -ComputerNamePrefix "Test" -AdminUsername $AdminUsername -AdminPassword $AdminPassword
```

<span data-ttu-id="4ff06-109">Bu komut, ContosoVMSS adlı VMSS 'ye ait sanal makinelerin işletim sistemi profili özelliklerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="4ff06-109">This command sets operating system profile properties for the virtual machines that belong to the VMSS named ContosoVMSS.</span></span>
<span data-ttu-id="4ff06-110">Bu komut, VMSS 'deki tüm sanal makine örneklerinin bilgisayar adı önekini, yöneticinin kullanıcı adını ve parolasını test etmek üzere ayarlar.</span><span class="sxs-lookup"><span data-stu-id="4ff06-110">The command sets the computer name prefix for all the virtual machine instances in the VMSS to Test and supplies the administrator username and password.</span></span>

## <span data-ttu-id="4ff06-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4ff06-111">PARAMETERS</span></span>

### <span data-ttu-id="4ff06-112">-Additionalunattenvseçcontent</span><span class="sxs-lookup"><span data-stu-id="4ff06-112">-AdditionalUnattendContent</span></span>
<span data-ttu-id="4ff06-113">Bir katılımsız içerik nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="4ff06-113">Specifies an unattended content object.</span></span>
<span data-ttu-id="4ff06-114">Nesneyi oluşturmak için Add-AzVMAdditionalUnattendContent kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4ff06-114">You can use the Add-AzVMAdditionalUnattendContent to create the object.</span></span>

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

### <span data-ttu-id="4ff06-115">-AdminPassword</span><span class="sxs-lookup"><span data-stu-id="4ff06-115">-AdminPassword</span></span>
<span data-ttu-id="4ff06-116">VMSS 'deki tüm sanal makine örnekleri için kullanılacak yönetici parolasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4ff06-116">Specifies the administrator password to use for all the virtual machine instances in the VMSS.</span></span>

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

### <span data-ttu-id="4ff06-117">-AdminUsername</span><span class="sxs-lookup"><span data-stu-id="4ff06-117">-AdminUsername</span></span>
<span data-ttu-id="4ff06-118">VMSS 'deki tüm sanal makine örnekleri için kullanılacak yönetici hesap adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4ff06-118">Specifies the administrator account name to use for all the virtual machine instances in the VMSS.</span></span> <br>
<span data-ttu-id="4ff06-119">**Yalnızca Windows sınırlaması:** Bitemez \" .\"</span><span class="sxs-lookup"><span data-stu-id="4ff06-119">**Windows-only restriction:** Cannot end in \".\"</span></span> <br>
<span data-ttu-id="4ff06-120">**Izin verilmeyen değerler:** \" yönetici \" , \" yönetici \" , \" Kullanıcı \" , \" kullanıcı1 \" , \" Test \" , \" kullanıcı2 \" , \" test1 \" , \" User3 \" , \" admin1 \" , \" 1 \" , \" 123 \" , \" a \" , \" ACTUser \" , \" ADM \" , \" Admin2 \" , \" ASPNET \" , \" Yedekleme \" , \" konsol \" , \" David \" , \" Guest \" , \" barış \" , \" Owner \" , \" root \" , \" Server \" , \" SQL \" , \" Destek \" , \" SUPPORT_388945a0 \" , \" sys \" , \" test2 \" , \" test3 \" , \" User4 \" , \" user5 \" .</span><span class="sxs-lookup"><span data-stu-id="4ff06-120">**Disallowed values:** \"administrator\", \"admin\", \"user\", \"user1\", \"test\", \"user2\", \"test1\", \"user3\", \"admin1\", \"1\", \"123\", \"a\", \"actuser\", \"adm\", \"admin2\", \"aspnet\", \"backup\", \"console\", \"david\", \"guest\", \"john\", \"owner\", \"root\", \"server\", \"sql\", \"support\", \"support_388945a0\", \"sys\", \"test2\", \"test3\", \"user4\", \"user5\".</span></span> <br>
<span data-ttu-id="4ff06-121">**Minimum uzunluk (Linux):** 1 karakter</span><span class="sxs-lookup"><span data-stu-id="4ff06-121">**Minimum-length (Linux):** 1  character</span></span> <br>
<span data-ttu-id="4ff06-122">**En büyük uzunluk (Linux):** 64 karakterler</span><span class="sxs-lookup"><span data-stu-id="4ff06-122">**Max-length (Linux):** 64 characters</span></span> <br>
<span data-ttu-id="4ff06-123">**En büyük uzunluk (Windows):** 20 karakter</span><span class="sxs-lookup"><span data-stu-id="4ff06-123">**Max-length (Windows):** 20 characters</span></span>  <br>
<li> <span data-ttu-id="4ff06-124">Linux VM 'ye kök erişimi için, [Azure 'Daki Linux sanal makinelerde kök ayrıcalıklarını kullanma](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-use-root-privileges?toc=%2fazure%2fvirtual-machines%2flinux%2ftoc.json)konusuna bakın.</span><span class="sxs-lookup"><span data-stu-id="4ff06-124">For root access to the Linux VM, see [Using root privileges on Linux virtual machines in Azure](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-use-root-privileges?toc=%2fazure%2fvirtual-machines%2flinux%2ftoc.json).</span></span><br>
<li> <span data-ttu-id="4ff06-125">Linux 'taki, bu alanda kullanılması gereken yerleşik sistem kullanıcıları listesi için, [bkz.](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-usernames?toc=%2fazure%2fvirtual-machines%2flinux%2ftoc.json)</span><span class="sxs-lookup"><span data-stu-id="4ff06-125">For a list of built-in system users on Linux that should not be used in this field, see [Selecting User Names for Linux on Azure](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-usernames?toc=%2fazure%2fvirtual-machines%2flinux%2ftoc.json).</span></span>

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

### <span data-ttu-id="4ff06-126">-ComputerNamePrefix</span><span class="sxs-lookup"><span data-stu-id="4ff06-126">-ComputerNamePrefix</span></span>
<span data-ttu-id="4ff06-127">VMSS 'deki tüm sanal makine örneklerinin bilgisayar adı önekini belirtir.</span><span class="sxs-lookup"><span data-stu-id="4ff06-127">Specifies the computer name prefix for all the virtual machine instances in the VMSS.</span></span>
<span data-ttu-id="4ff06-128">Bilgisayar adları 1-15 karakter uzunluğunda olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="4ff06-128">Computer names must be 1 to 15 characters long.</span></span>

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

### <span data-ttu-id="4ff06-129">-CustomData</span><span class="sxs-lookup"><span data-stu-id="4ff06-129">-CustomData</span></span>
<span data-ttu-id="4ff06-130">Özel verilerin Base-64 kodlu dizesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="4ff06-130">Specifies a base-64 encoded string of custom data.</span></span>
<span data-ttu-id="4ff06-131">Bu, sanal makinede dosya olarak kaydedilmiş bir ikili diziye çözülür.</span><span class="sxs-lookup"><span data-stu-id="4ff06-131">This is decoded to a binary array that is saved as a file on the virtual machine.</span></span>
<span data-ttu-id="4ff06-132">İkili dizinin en fazla uzunluğu 65535 bayttır.</span><span class="sxs-lookup"><span data-stu-id="4ff06-132">The maximum length of the binary array is 65535 bytes.</span></span> <br>
<span data-ttu-id="4ff06-133">VM 'unuzda bulut-init kullanmak için, [oluşturma sırasında bir LINUX VM 'yi özelleştirmek amacıyla Cloud-Init kullanma](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-using-cloud-init?toc=%2fazure%2fvirtual-machines%2flinux%2ftoc.json)konusuna bakın.</span><span class="sxs-lookup"><span data-stu-id="4ff06-133">For using cloud-init for your VM, see [Using cloud-init to customize a Linux VM during creation](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-using-cloud-init?toc=%2fazure%2fvirtual-machines%2flinux%2ftoc.json).</span></span>

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

### <span data-ttu-id="4ff06-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ff06-134">-DefaultProfile</span></span>
<span data-ttu-id="4ff06-135">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4ff06-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4ff06-136">-LinuxConfigurationDisablePasswordAuthentication</span><span class="sxs-lookup"><span data-stu-id="4ff06-136">-LinuxConfigurationDisablePasswordAuthentication</span></span>
<span data-ttu-id="4ff06-137">Bu cmdlet 'in parola kimlik doğrulamasını devre dışı bırakacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="4ff06-137">Indicates that this cmdlet disables password authentication.</span></span>

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

### <span data-ttu-id="4ff06-138">-Listener</span><span class="sxs-lookup"><span data-stu-id="4ff06-138">-Listener</span></span>
<span data-ttu-id="4ff06-139">Windows Uzaktan Yönetim (WinRM) dinleyicilerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="4ff06-139">Specifies the Windows Remote Management (WinRM) listeners.</span></span>
<span data-ttu-id="4ff06-140">Bu, uzak Windows PowerShell 'i etkinleştirmiştir.</span><span class="sxs-lookup"><span data-stu-id="4ff06-140">This enables remote Windows PowerShell.</span></span>
<span data-ttu-id="4ff06-141">Dinleyiciyi oluşturmak için Add-AzVmssWinRMListener cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4ff06-141">You can use the Add-AzVmssWinRMListener cmdlet to create the listener.</span></span>

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

### <span data-ttu-id="4ff06-142">-PublicKey</span><span class="sxs-lookup"><span data-stu-id="4ff06-142">-PublicKey</span></span>
<span data-ttu-id="4ff06-143">Güvenli Kabuk (SSH) ortak anahtar nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="4ff06-143">Specifies the Secure Shell (SSH) public key object.</span></span>
<span data-ttu-id="4ff06-144">Nesneyi oluşturmak için Add-AzVMSshPublicKey cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4ff06-144">You can use the Add-AzVMSshPublicKey cmdlet to create the object.</span></span>

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

### <span data-ttu-id="4ff06-145">-Parola</span><span class="sxs-lookup"><span data-stu-id="4ff06-145">-Secret</span></span>
<span data-ttu-id="4ff06-146">Sanal makineye yerleştirilecek sertifika başvurularını içeren gizli nesne türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="4ff06-146">Specifies the secrets object which contains the certificate references to place on the virtual machine.</span></span>
<span data-ttu-id="4ff06-147">Gizli nesneleri oluşturmak için Add-AzVmssSecret cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4ff06-147">You can use the Add-AzVmssSecret cmdlet to create the secrets object.</span></span>

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

### <span data-ttu-id="4ff06-148">-TimeZone</span><span class="sxs-lookup"><span data-stu-id="4ff06-148">-TimeZone</span></span>
<span data-ttu-id="4ff06-149">Sanal makinenin saat dilimini belirtir.</span><span class="sxs-lookup"><span data-stu-id="4ff06-149">Specifies the time zone of the virtual machine.</span></span> <span data-ttu-id="4ff06-150">Örneğin \" Pasifik standart saati \" .</span><span class="sxs-lookup"><span data-stu-id="4ff06-150">e.g. \"Pacific Standard Time\".</span></span> <br>
<span data-ttu-id="4ff06-151">Olası değerler, [TimeZoneInfo. GetSystemTimeZones](https://docs.microsoft.com/en-us/dotnet/api/system.timezoneinfo.getsystemtimezones)tarafından döndürülen saat dilimlerinde [TimeZoneInfo.ID](https://docs.microsoft.com/en-us/dotnet/api/system.timezoneinfo.id?#System_TimeZoneInfo_Id) değeri olabilir.</span><span class="sxs-lookup"><span data-stu-id="4ff06-151">Possible values can be [TimeZoneInfo.Id](https://docs.microsoft.com/en-us/dotnet/api/system.timezoneinfo.id?#System_TimeZoneInfo_Id) value from time zones returned by [TimeZoneInfo.GetSystemTimeZones](https://docs.microsoft.com/en-us/dotnet/api/system.timezoneinfo.getsystemtimezones).</span></span>

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

### <span data-ttu-id="4ff06-152">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="4ff06-152">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="4ff06-153">VMSS nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="4ff06-153">Specifies the VMSS object.</span></span>
<span data-ttu-id="4ff06-154">Nesneyi oluşturmak için New-AzVmssConfig cmdlet 'ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="4ff06-154">You can use the New-AzVmssConfig cmdlet to create the object.</span></span>

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

### <span data-ttu-id="4ff06-155">-WindowsConfigurationEnableAutomaticUpdate</span><span class="sxs-lookup"><span data-stu-id="4ff06-155">-WindowsConfigurationEnableAutomaticUpdate</span></span>
<span data-ttu-id="4ff06-156">VMSS 'deki sanal makinelerin otomatik güncelleştirmeler için etkinleştirilip etkinleştirilmediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="4ff06-156">Indicates whether the virtual machines in the VMSS are enabled for automatic updates.</span></span>

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

### <span data-ttu-id="4ff06-157">-WindowsConfigurationProvisionVMAgent</span><span class="sxs-lookup"><span data-stu-id="4ff06-157">-WindowsConfigurationProvisionVMAgent</span></span>
<span data-ttu-id="4ff06-158">VMSS 'deki sanal makinelerde sanal makine aracısının sağlanması gerekip gerekmediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="4ff06-158">Indicates whether virtual machine agent should be provisioned on the virtual machines in the VMSS.</span></span>

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

### <span data-ttu-id="4ff06-159">-Onay</span><span class="sxs-lookup"><span data-stu-id="4ff06-159">-Confirm</span></span>
<span data-ttu-id="4ff06-160">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="4ff06-160">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4ff06-161">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4ff06-161">-WhatIf</span></span>
<span data-ttu-id="4ff06-162">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="4ff06-162">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4ff06-163">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="4ff06-163">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4ff06-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ff06-164">CommonParameters</span></span>
<span data-ttu-id="4ff06-165">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4ff06-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ff06-166">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="4ff06-166">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ff06-167">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4ff06-167">INPUTS</span></span>

### <span data-ttu-id="4ff06-168">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="4ff06-168">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="4ff06-169">System. String</span><span class="sxs-lookup"><span data-stu-id="4ff06-169">System.String</span></span>

### <span data-ttu-id="4ff06-170">System. Nullable ' 1 [[System. Boolean, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85vseç7val 7798e]]</span><span class="sxs-lookup"><span data-stu-id="4ff06-170">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="4ff06-171">Microsoft. Azure. Management. COMPUTE. modeller. Addiunattenvseçcontent []</span><span class="sxs-lookup"><span data-stu-id="4ff06-171">Microsoft.Azure.Management.Compute.Models.AdditionalUnattendContent[]</span></span>

### <span data-ttu-id="4ff06-172">Microsoft. Azure. Management. COMPUTE. model. WinRMListener []</span><span class="sxs-lookup"><span data-stu-id="4ff06-172">Microsoft.Azure.Management.Compute.Models.WinRMListener[]</span></span>

### <span data-ttu-id="4ff06-173">Microsoft. Azure. Management. COMPUTE. model. SshPublicKey []</span><span class="sxs-lookup"><span data-stu-id="4ff06-173">Microsoft.Azure.Management.Compute.Models.SshPublicKey[]</span></span>

### <span data-ttu-id="4ff06-174">Microsoft. Azure. Management. COMPUTE. modeller. VaultSecretGroup []</span><span class="sxs-lookup"><span data-stu-id="4ff06-174">Microsoft.Azure.Management.Compute.Models.VaultSecretGroup[]</span></span>

## <span data-ttu-id="4ff06-175">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4ff06-175">OUTPUTS</span></span>

### <span data-ttu-id="4ff06-176">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="4ff06-176">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="4ff06-177">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4ff06-177">NOTES</span></span>

## <span data-ttu-id="4ff06-178">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4ff06-178">RELATED LINKS</span></span>

[<span data-ttu-id="4ff06-179">Add-AzVMAdditionalUnattendContent</span><span class="sxs-lookup"><span data-stu-id="4ff06-179">Add-AzVMAdditionalUnattendContent</span></span>](./Add-AzVMAdditionalUnattendContent.md)

[<span data-ttu-id="4ff06-180">Add-AzVmssWinRMListener</span><span class="sxs-lookup"><span data-stu-id="4ff06-180">Add-AzVmssWinRMListener</span></span>](./Add-AzVmssWinRMListener.md)

[<span data-ttu-id="4ff06-181">Add-AzVMSshPublicKey</span><span class="sxs-lookup"><span data-stu-id="4ff06-181">Add-AzVMSshPublicKey</span></span>](./Add-AzVMSshPublicKey.md)

[<span data-ttu-id="4ff06-182">Add-AzVmssSecret</span><span class="sxs-lookup"><span data-stu-id="4ff06-182">Add-AzVmssSecret</span></span>](./Add-AzVmssSecret.md)

[<span data-ttu-id="4ff06-183">Yeni-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="4ff06-183">New-AzVmssConfig</span></span>](./New-AzVmssConfig.md)


