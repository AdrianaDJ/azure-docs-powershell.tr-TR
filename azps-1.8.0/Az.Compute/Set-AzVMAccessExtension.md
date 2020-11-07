---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: D93666EC-C252-4E3B-B311-50B6EEA6D4BF
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmaccessextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMAccessExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMAccessExtension.md
ms.openlocfilehash: b0b91e2892f087da6eb510d087980e6f31dd67ef
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93761238"
---
# <span data-ttu-id="2d2f7-101">Set-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="2d2f7-101">Set-AzVMAccessExtension</span></span>

## <span data-ttu-id="2d2f7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2d2f7-102">SYNOPSIS</span></span>
<span data-ttu-id="2d2f7-103">Sanal makineye VMAccess uzantısını ekler.</span><span class="sxs-lookup"><span data-stu-id="2d2f7-103">Adds the VMAccess extension to a virtual machine.</span></span>

## <span data-ttu-id="2d2f7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2d2f7-104">SYNTAX</span></span>

```
Set-AzVMAccessExtension [-Credential <PSCredential>] [-ResourceGroupName] <String> [-VMName] <String>
 [-Name <String>] [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion]
 [-ForceRerun <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2d2f7-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="2d2f7-105">DESCRIPTION</span></span>
<span data-ttu-id="2d2f7-106">**Set-Azvmaccessextenkomutçuğu** sanal makine erişimi (VMAccess) sanal makine VMAccess uzantısını bir sanal makineye ekler.</span><span class="sxs-lookup"><span data-stu-id="2d2f7-106">The **Set-AzVMAccessExtension** cmdlet adds the Virtual Machine Access (VMAccess) Virtual Machine VMAccess Extension to a virtual machine.</span></span> <span data-ttu-id="2d2f7-107">VMAccess uzantısı geçici bir parola ayarlamak için kullanılabilir ve bu, makinede oturum açıldıktan sonra hemen değiştirilmelidir.</span><span class="sxs-lookup"><span data-stu-id="2d2f7-107">VMAccess Extension can be used to set a temporary password and this should be immediately changed it after logging into the machine.</span></span> <span data-ttu-id="2d2f7-108">Bu, Windows etki alanı denetleyicilerinde desteklenmez.</span><span class="sxs-lookup"><span data-stu-id="2d2f7-108">This is not supported on Windows Domain Controllers.</span></span>

## <span data-ttu-id="2d2f7-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2d2f7-109">EXAMPLES</span></span>

### <span data-ttu-id="2d2f7-110">Örnek 1: VMAccess uzantısı ekleme</span><span class="sxs-lookup"><span data-stu-id="2d2f7-110">Example 1: Add a VMAccess extension</span></span>
```
PS C:\> Set-AzVMAccessExtension -ResourceGroupName "ResrouceGroup11" -Location "Central US" -VMName "VirtualMachine07" -Name "ContosoTest" -TypeHandlerVersion "2.0" -UserName "PFuller" -Password "Password"
```

<span data-ttu-id="2d2f7-111">Bu komut, ResrouceGroup11 'da VirtualMachine07 adındaki sanal makine için bir VMAccess uzantısı ekler.</span><span class="sxs-lookup"><span data-stu-id="2d2f7-111">This command adds a VMAccess extension for the virtual machine named VirtualMachine07 in ResrouceGroup11.</span></span>
<span data-ttu-id="2d2f7-112">Komut, VMAccess için ad ve tür işleyicisi sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="2d2f7-112">The command specifies the name and type handler version for VMAccess.</span></span>

## <span data-ttu-id="2d2f7-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2d2f7-113">PARAMETERS</span></span>

### <span data-ttu-id="2d2f7-114">-Credential</span><span class="sxs-lookup"><span data-stu-id="2d2f7-114">-Credential</span></span>
<span data-ttu-id="2d2f7-115">Sanal makinenin bir **PSCredential** nesnesi olarak Kullanıcı adını ve parolasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2d2f7-115">Specifies the user name and password for the virtual machine as a **PSCredential** object.</span></span>
<span data-ttu-id="2d2f7-116">VM 'nizde geçerli yerel yönetici hesabından farklı bir ad yazarsanız, VMAccess uzantısı bu ada sahip bir yerel yönetici hesabı ekler ve bu hesaba belirtilen şifrenizi atar.</span><span class="sxs-lookup"><span data-stu-id="2d2f7-116">If you type a different name than the current local administrator account on your VM, the VMAccess extension will add a local administrator account with that name, and assign your specified password to that account.</span></span> <span data-ttu-id="2d2f7-117">VM 'nizde yerel yönetici hesabı varsa, parolayı sıfırlar ve hesap devre dışıysa, VMAccess uzantısı etkinleştirilir.</span><span class="sxs-lookup"><span data-stu-id="2d2f7-117">If the local administrator account on your VM exists, it will reset the password and if the account is disabled, the VMAccess extension enables it.</span></span>
<span data-ttu-id="2d2f7-118">Kimlik bilgilerini almak için Get-Credential cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="2d2f7-118">To obtain a credential, use the Get-Credential cmdlet.</span></span>
<span data-ttu-id="2d2f7-119">Daha fazla bilgi için yazın `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="2d2f7-119">For more information, type `Get-Help Get-Credential`.</span></span>

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

### <span data-ttu-id="2d2f7-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d2f7-120">-DefaultProfile</span></span>
<span data-ttu-id="2d2f7-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2d2f7-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2d2f7-122">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="2d2f7-122">-DisableAutoUpgradeMinorVersion</span></span>
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

### <span data-ttu-id="2d2f7-123">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="2d2f7-123">-ForceRerun</span></span>
<span data-ttu-id="2d2f7-124">Bu cmdlet 'in, uzantıyı kaldırıp yeniden yüklemeden sanal makinede aynı uzantı yapılandırmasını yeniden çalıştırmayı zortığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="2d2f7-124">Indicates that this cmdlet forces a rerun of the same extension configuration on the virtual machine without uninstalling and reinstalling the extension.</span></span>
<span data-ttu-id="2d2f7-125">Değer, geçerli değerden farklı olabilir.</span><span class="sxs-lookup"><span data-stu-id="2d2f7-125">The value can be any string different from the current value.</span></span>
<span data-ttu-id="2d2f7-126">ForceUpdateTag değiştirilirse, genel veya korumalı ayarlara yönelik güncelleştirmeler işleyici tarafından uygulanır.</span><span class="sxs-lookup"><span data-stu-id="2d2f7-126">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

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

### <span data-ttu-id="2d2f7-127">-Konum</span><span class="sxs-lookup"><span data-stu-id="2d2f7-127">-Location</span></span>
<span data-ttu-id="2d2f7-128">Sanal makinenin konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="2d2f7-128">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="2d2f7-129">-Ad</span><span class="sxs-lookup"><span data-stu-id="2d2f7-129">-Name</span></span>
<span data-ttu-id="2d2f7-130">Bu cmdlet 'in eklediği uzantının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2d2f7-130">Specifies the name of the extension that this cmdlet adds.</span></span>

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

### <span data-ttu-id="2d2f7-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2d2f7-131">-ResourceGroupName</span></span>
<span data-ttu-id="2d2f7-132">Sanal makinenin kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2d2f7-132">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="2d2f7-133">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="2d2f7-133">-TypeHandlerVersion</span></span>
<span data-ttu-id="2d2f7-134">Bu sanal makine için kullanılacak uzantının sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="2d2f7-134">Specifies the version of the extension to use for this virtual machine.</span></span>
<span data-ttu-id="2d2f7-135">Sürümü edinmek için, *tür* parametresinde Microsoft. *PublisherName* parametresi ve VMAccessAgent değerini içeren Get-AzVMExtensionImage cmdlet 'ini çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="2d2f7-135">To obtain the version, run the Get-AzVMExtensionImage cmdlet with a value of Microsoft.Compute for the *PublisherName* parameter and VMAccessAgent for the *Type* parameter.</span></span> <span data-ttu-id="2d2f7-136">Sürüm 1 kullanım dışı olduğundan, typeHandlerVersion 2,0 veya üzeri olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="2d2f7-136">The typeHandlerVersion must be 2.0 or greater, as version 1 is deprecated.</span></span>

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

### <span data-ttu-id="2d2f7-137">-VMName</span><span class="sxs-lookup"><span data-stu-id="2d2f7-137">-VMName</span></span>
<span data-ttu-id="2d2f7-138">Sanal makinenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2d2f7-138">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="2d2f7-139">Bu cmdlet, bu parametrenin belirttiği sanal makine için VMAccess öğesini ekler.</span><span class="sxs-lookup"><span data-stu-id="2d2f7-139">This cmdlet adds VMAccess for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="2d2f7-140">-Onay</span><span class="sxs-lookup"><span data-stu-id="2d2f7-140">-Confirm</span></span>
<span data-ttu-id="2d2f7-141">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="2d2f7-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2d2f7-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2d2f7-142">-WhatIf</span></span>
<span data-ttu-id="2d2f7-143">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="2d2f7-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2d2f7-144">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="2d2f7-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2d2f7-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d2f7-145">CommonParameters</span></span>
<span data-ttu-id="2d2f7-146">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2d2f7-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d2f7-147">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2d2f7-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d2f7-148">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2d2f7-148">INPUTS</span></span>

### <span data-ttu-id="2d2f7-149">System. Management. Automation. PSCredential</span><span class="sxs-lookup"><span data-stu-id="2d2f7-149">System.Management.Automation.PSCredential</span></span>

### <span data-ttu-id="2d2f7-150">System. String</span><span class="sxs-lookup"><span data-stu-id="2d2f7-150">System.String</span></span>

### <span data-ttu-id="2d2f7-151">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="2d2f7-151">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="2d2f7-152">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2d2f7-152">OUTPUTS</span></span>

### <span data-ttu-id="2d2f7-153">Microsoft. Azure. Commands. COMPUTE. modeller. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="2d2f7-153">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="2d2f7-154">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2d2f7-154">NOTES</span></span>

## <span data-ttu-id="2d2f7-155">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2d2f7-155">RELATED LINKS</span></span>

[<span data-ttu-id="2d2f7-156">Get-azvmaccessexten</span><span class="sxs-lookup"><span data-stu-id="2d2f7-156">Get-AzVMAccessExtension</span></span>](./Get-AzVMAccessExtension.md)

[<span data-ttu-id="2d2f7-157">Remove-azvmaccessexten</span><span class="sxs-lookup"><span data-stu-id="2d2f7-157">Remove-AzVMAccessExtension</span></span>](./Remove-AzVMAccessExtension.md)

[<span data-ttu-id="2d2f7-158">Set-Azvmexgeri</span><span class="sxs-lookup"><span data-stu-id="2d2f7-158">Set-AzVMExtension</span></span>](./Set-AzVMExtension.md)

[<span data-ttu-id="2d2f7-159">Get-Azvmextensionımage</span><span class="sxs-lookup"><span data-stu-id="2d2f7-159">Get-AzVMExtensionImage</span></span>](./Get-AzVMExtensionImage.md)


