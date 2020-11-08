---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: D93666EC-C252-4E3B-B311-50B6EEA6D4BF
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmaccessextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMAccessExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMAccessExtension.md
ms.openlocfilehash: 5eaf09aec561ed1fff37d2687253634bd1efc921
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096393"
---
# <span data-ttu-id="15138-101">Set-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="15138-101">Set-AzVMAccessExtension</span></span>

## <span data-ttu-id="15138-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="15138-102">SYNOPSIS</span></span>
<span data-ttu-id="15138-103">Sanal makineye VMAccess uzantısını ekler.</span><span class="sxs-lookup"><span data-stu-id="15138-103">Adds the VMAccess extension to a virtual machine.</span></span>

## <span data-ttu-id="15138-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="15138-104">SYNTAX</span></span>

```
Set-AzVMAccessExtension [-Credential <PSCredential>] [-ResourceGroupName] <String> [-VMName] <String>
 [-Name <String>] [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion]
 [-ForceRerun <String>] [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="15138-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="15138-105">DESCRIPTION</span></span>
<span data-ttu-id="15138-106">**Set-Azvmaccessextenkomutçuğu** sanal makine erişimi (VMAccess) sanal makine VMAccess uzantısını bir sanal makineye ekler.</span><span class="sxs-lookup"><span data-stu-id="15138-106">The **Set-AzVMAccessExtension** cmdlet adds the Virtual Machine Access (VMAccess) Virtual Machine VMAccess Extension to a virtual machine.</span></span> <span data-ttu-id="15138-107">VMAccess uzantısı geçici bir parola ayarlamak için kullanılabilir ve bu, makinede oturum açıldıktan sonra hemen değiştirilmelidir.</span><span class="sxs-lookup"><span data-stu-id="15138-107">VMAccess Extension can be used to set a temporary password and this should be immediately changed it after logging into the machine.</span></span> <span data-ttu-id="15138-108">Bu, Windows etki alanı denetleyicilerinde desteklenmez.</span><span class="sxs-lookup"><span data-stu-id="15138-108">This is not supported on Windows Domain Controllers.</span></span>

## <span data-ttu-id="15138-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="15138-109">EXAMPLES</span></span>

### <span data-ttu-id="15138-110">Örnek 1: VMAccess uzantısı ekleme</span><span class="sxs-lookup"><span data-stu-id="15138-110">Example 1: Add a VMAccess extension</span></span>
```
PS C:\> Set-AzVMAccessExtension -ResourceGroupName "ResourceGroup11" -Location "Central US" -VMName "VirtualMachine07" -Name "ContosoTest" -TypeHandlerVersion "2.4" -UserName "PFuller" -Password "Password"
```

<span data-ttu-id="15138-111">Bu komut, ResourceGroup11 'da VirtualMachine07 adındaki sanal makine için bir VMAccess uzantısı ekler.</span><span class="sxs-lookup"><span data-stu-id="15138-111">This command adds a VMAccess extension for the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>
<span data-ttu-id="15138-112">Komut, VMAccess için ad ve tür işleyicisi sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="15138-112">The command specifies the name and type handler version for VMAccess.</span></span>

## <span data-ttu-id="15138-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="15138-113">PARAMETERS</span></span>

### <span data-ttu-id="15138-114">-Credential</span><span class="sxs-lookup"><span data-stu-id="15138-114">-Credential</span></span>
<span data-ttu-id="15138-115">Sanal makinenin bir **PSCredential** nesnesi olarak Kullanıcı adını ve parolasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="15138-115">Specifies the user name and password for the virtual machine as a **PSCredential** object.</span></span>
<span data-ttu-id="15138-116">VM 'nizde geçerli yerel yönetici hesabından farklı bir ad yazarsanız, VMAccess uzantısı bu ada sahip bir yerel yönetici hesabı ekler ve bu hesaba belirtilen şifrenizi atar.</span><span class="sxs-lookup"><span data-stu-id="15138-116">If you type a different name than the current local administrator account on your VM, the VMAccess extension will add a local administrator account with that name, and assign your specified password to that account.</span></span> <span data-ttu-id="15138-117">VM 'nizde yerel yönetici hesabı varsa, parolayı sıfırlar ve hesap devre dışıysa, VMAccess uzantısı etkinleştirilir.</span><span class="sxs-lookup"><span data-stu-id="15138-117">If the local administrator account on your VM exists, it will reset the password and if the account is disabled, the VMAccess extension enables it.</span></span>
<span data-ttu-id="15138-118">Kimlik bilgilerini almak için Get-Credential cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="15138-118">To obtain a credential, use the Get-Credential cmdlet.</span></span>
<span data-ttu-id="15138-119">Daha fazla bilgi için yazın `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="15138-119">For more information, type `Get-Help Get-Credential`.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15138-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15138-120">-DefaultProfile</span></span>
<span data-ttu-id="15138-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="15138-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="15138-122">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="15138-122">-DisableAutoUpgradeMinorVersion</span></span>
```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15138-123">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="15138-123">-ForceRerun</span></span>
<span data-ttu-id="15138-124">Bu cmdlet 'in, uzantıyı kaldırıp yeniden yüklemeden sanal makinede aynı uzantı yapılandırmasını yeniden çalıştırmayı zortığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="15138-124">Indicates that this cmdlet forces a rerun of the same extension configuration on the virtual machine without uninstalling and reinstalling the extension.</span></span>
<span data-ttu-id="15138-125">Değer, geçerli değerden farklı olabilir.</span><span class="sxs-lookup"><span data-stu-id="15138-125">The value can be any string different from the current value.</span></span>
<span data-ttu-id="15138-126">ForceUpdateTag değiştirilirse, genel veya korumalı ayarlara yönelik güncelleştirmeler işleyici tarafından uygulanır.</span><span class="sxs-lookup"><span data-stu-id="15138-126">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15138-127">-Konum</span><span class="sxs-lookup"><span data-stu-id="15138-127">-Location</span></span>
<span data-ttu-id="15138-128">Sanal makinenin konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="15138-128">Specifies the location of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15138-129">-Ad</span><span class="sxs-lookup"><span data-stu-id="15138-129">-Name</span></span>
<span data-ttu-id="15138-130">Bu cmdlet 'in eklediği uzantının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="15138-130">Specifies the name of the extension that this cmdlet adds.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15138-131">-NoWait</span><span class="sxs-lookup"><span data-stu-id="15138-131">-NoWait</span></span>
<span data-ttu-id="15138-132">İşlemi başlatır ve işlem tamamlanmadan hemen döner.</span><span class="sxs-lookup"><span data-stu-id="15138-132">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="15138-133">İşlemin başarıyla tamamlanıp tamamlanmadığını belirlemek için başka bir mekanizma kullanın.</span><span class="sxs-lookup"><span data-stu-id="15138-133">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15138-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="15138-134">-ResourceGroupName</span></span>
<span data-ttu-id="15138-135">Sanal makinenin kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="15138-135">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15138-136">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="15138-136">-TypeHandlerVersion</span></span>
<span data-ttu-id="15138-137">Bu sanal makine için kullanılacak uzantının sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="15138-137">Specifies the version of the extension to use for this virtual machine.</span></span>
<span data-ttu-id="15138-138">Sürümü edinmek için, *tür* parametresinde Microsoft. *PublisherName* parametresi ve VMAccessAgent değerini içeren Get-AzVMExtensionImage cmdlet 'ini çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="15138-138">To obtain the version, run the Get-AzVMExtensionImage cmdlet with a value of Microsoft.Compute for the *PublisherName* parameter and VMAccessAgent for the *Type* parameter.</span></span> <span data-ttu-id="15138-139">Sürüm 1 kullanım dışı olduğundan, typeHandlerVersion 2,0 veya üzeri olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="15138-139">The typeHandlerVersion must be 2.0 or greater, as version 1 is deprecated.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15138-140">-VMName</span><span class="sxs-lookup"><span data-stu-id="15138-140">-VMName</span></span>
<span data-ttu-id="15138-141">Sanal makinenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="15138-141">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="15138-142">Bu cmdlet, bu parametrenin belirttiği sanal makine için VMAccess öğesini ekler.</span><span class="sxs-lookup"><span data-stu-id="15138-142">This cmdlet adds VMAccess for the virtual machine that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15138-143">-Onay</span><span class="sxs-lookup"><span data-stu-id="15138-143">-Confirm</span></span>
<span data-ttu-id="15138-144">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="15138-144">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15138-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="15138-145">-WhatIf</span></span>
<span data-ttu-id="15138-146">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="15138-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="15138-147">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="15138-147">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15138-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15138-148">CommonParameters</span></span>
<span data-ttu-id="15138-149">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="15138-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15138-150">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="15138-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15138-151">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="15138-151">INPUTS</span></span>

### <span data-ttu-id="15138-152">System. Management. Automation. PSCredential</span><span class="sxs-lookup"><span data-stu-id="15138-152">System.Management.Automation.PSCredential</span></span>

### <span data-ttu-id="15138-153">System. String</span><span class="sxs-lookup"><span data-stu-id="15138-153">System.String</span></span>

### <span data-ttu-id="15138-154">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="15138-154">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="15138-155">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="15138-155">OUTPUTS</span></span>

### <span data-ttu-id="15138-156">Microsoft. Azure. Commands. COMPUTE. modeller. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="15138-156">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="15138-157">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="15138-157">NOTES</span></span>

## <span data-ttu-id="15138-158">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="15138-158">RELATED LINKS</span></span>

[<span data-ttu-id="15138-159">Get-azvmaccessexten</span><span class="sxs-lookup"><span data-stu-id="15138-159">Get-AzVMAccessExtension</span></span>](./Get-AzVMAccessExtension.md)

[<span data-ttu-id="15138-160">Remove-azvmaccessexten</span><span class="sxs-lookup"><span data-stu-id="15138-160">Remove-AzVMAccessExtension</span></span>](./Remove-AzVMAccessExtension.md)

[<span data-ttu-id="15138-161">Set-Azvmexgeri</span><span class="sxs-lookup"><span data-stu-id="15138-161">Set-AzVMExtension</span></span>](./Set-AzVMExtension.md)

[<span data-ttu-id="15138-162">Get-Azvmextensionımage</span><span class="sxs-lookup"><span data-stu-id="15138-162">Get-AzVMExtensionImage</span></span>](./Get-AzVMExtensionImage.md)


