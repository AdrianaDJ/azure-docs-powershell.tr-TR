---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: B2B4E132-4A71-4DB8-A7B9-9ED3FE7EB292
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmbginfoextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMBginfoExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMBginfoExtension.md
ms.openlocfilehash: a98a2f5cbc8034e8cec4d324bb7ecaa28297e772
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94097673"
---
# <span data-ttu-id="f9835-101">Set-AzVMBginfoExtension</span><span class="sxs-lookup"><span data-stu-id="f9835-101">Set-AzVMBginfoExtension</span></span>

## <span data-ttu-id="f9835-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f9835-102">SYNOPSIS</span></span>
<span data-ttu-id="f9835-103">Bir sanal makineye BgInfo uzantısını ekler.</span><span class="sxs-lookup"><span data-stu-id="f9835-103">Adds the BGInfo extension to a virtual machine.</span></span>

## <span data-ttu-id="f9835-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f9835-104">SYNTAX</span></span>

```
Set-AzVMBginfoExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f9835-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="f9835-105">DESCRIPTION</span></span>
<span data-ttu-id="f9835-106">**Set-AzVMBGInfoExtension** cmdlet 'ı, BgInfo uzantısını bir sanal makineye ekler.</span><span class="sxs-lookup"><span data-stu-id="f9835-106">The **Set-AzVMBGInfoExtension** cmdlet adds the BGInfo extension to a virtual machine.</span></span>

## <span data-ttu-id="f9835-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f9835-107">EXAMPLES</span></span>

### <span data-ttu-id="f9835-108">Örnek 1: sanal makine için BgInfo uzantısını ekleme</span><span class="sxs-lookup"><span data-stu-id="f9835-108">Example 1: Add the BGInfo extension for a virtual machine</span></span>
```
PS C:\> Set-AzVMBgInfoExtension -ResourceGroupName "ContosoRG" -VMName "ContosoVM" -Name "ExtensionName" -TypeHandlerVersion "2.1" -Location "West Europe"
```

<span data-ttu-id="f9835-109">Bu komut, bir BgInfo uzantısını ContosoVM adındaki sanal makineye ekler.</span><span class="sxs-lookup"><span data-stu-id="f9835-109">This command adds the BGInfo extension to virtual machine named ContosoVM.</span></span>
<span data-ttu-id="f9835-110">Komut sanal makinenin kaynak grubunu ve konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="f9835-110">The command specifies the resource group and location of the virtual machine.</span></span>
<span data-ttu-id="f9835-111">Komut, uzantının adını ve sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="f9835-111">The command specifies the name and version of the extension.</span></span>

## <span data-ttu-id="f9835-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f9835-112">PARAMETERS</span></span>

### <span data-ttu-id="f9835-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9835-113">-DefaultProfile</span></span>
<span data-ttu-id="f9835-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f9835-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f9835-115">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="f9835-115">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="f9835-116">Bu cmdlet 'in, Azure Konuk aracısının uzantıyı daha yeni bir alt sürüme otomatik olarak güncelleştirmesini engellediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="f9835-116">Indicates that this cmdlet prevents the Azure guest agent from automatically updating the extension to a newer minor version.</span></span>
<span data-ttu-id="f9835-117">Varsayılan olarak, bu cmdlet Konuk aracısının uzantıyı güncelleştirmesini olanaklı kılar.</span><span class="sxs-lookup"><span data-stu-id="f9835-117">By default, this cmdlet enables the guest agent to update the extension.</span></span>

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

### <span data-ttu-id="f9835-118">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="f9835-118">-ForceRerun</span></span>
<span data-ttu-id="f9835-119">Uzantının aynı genel veya korumalı ayarlarla yeniden çalıştırılması gerektiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="f9835-119">Specifies that the extension should be run again with the same public or protected settings.</span></span>
<span data-ttu-id="f9835-120">Değer, geçerli değerden farklı olabilir.</span><span class="sxs-lookup"><span data-stu-id="f9835-120">The value can be any string different from the current value.</span></span>
<span data-ttu-id="f9835-121">ForceUpdateTag değiştirilirse, genel veya korumalı ayarlara yönelik güncelleştirmeler işleyici tarafından uygulanır.</span><span class="sxs-lookup"><span data-stu-id="f9835-121">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

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

### <span data-ttu-id="f9835-122">-Konum</span><span class="sxs-lookup"><span data-stu-id="f9835-122">-Location</span></span>
<span data-ttu-id="f9835-123">Sanal makinenin konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="f9835-123">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="f9835-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="f9835-124">-Name</span></span>
<span data-ttu-id="f9835-125">Bu cmdlet 'in sanal makineye eklediği BgInfo uzantısının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f9835-125">Specifies the name of the BGInfo extension that this cmdlet adds to a virtual machine.</span></span>

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

### <span data-ttu-id="f9835-126">-NoWait</span><span class="sxs-lookup"><span data-stu-id="f9835-126">-NoWait</span></span>
<span data-ttu-id="f9835-127">İşlemi başlatır ve işlem tamamlanmadan hemen döner.</span><span class="sxs-lookup"><span data-stu-id="f9835-127">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="f9835-128">İşlemin başarıyla tamamlanıp tamamlanmadığını belirlemek için başka bir mekanizma kullanın.</span><span class="sxs-lookup"><span data-stu-id="f9835-128">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="f9835-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f9835-129">-ResourceGroupName</span></span>
<span data-ttu-id="f9835-130">Bu cmdlet 'in uzantısı eklediği sanal makinenin kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f9835-130">Specifies the name of the resource group of the virtual machine to which this cmdlet adds an extension.</span></span>

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

### <span data-ttu-id="f9835-131">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="f9835-131">-TypeHandlerVersion</span></span>
<span data-ttu-id="f9835-132">Bu cmdlet 'in sanal makineye eklediği uzantının sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="f9835-132">Specifies the version of the extension that this cmdlet adds to the virtual machine.</span></span>

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

### <span data-ttu-id="f9835-133">-VMName</span><span class="sxs-lookup"><span data-stu-id="f9835-133">-VMName</span></span>
<span data-ttu-id="f9835-134">Bu cmdlet 'in BgInfo uzantısını eklediği sanal makinenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f9835-134">Specifies the name of the virtual machine to which this cmdlet adds the BGInfo extension.</span></span>

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

### <span data-ttu-id="f9835-135">-Onay</span><span class="sxs-lookup"><span data-stu-id="f9835-135">-Confirm</span></span>
<span data-ttu-id="f9835-136">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="f9835-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f9835-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f9835-137">-WhatIf</span></span>
<span data-ttu-id="f9835-138">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f9835-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f9835-139">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="f9835-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f9835-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9835-140">CommonParameters</span></span>
<span data-ttu-id="f9835-141">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f9835-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9835-142">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="f9835-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9835-143">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f9835-143">INPUTS</span></span>

### <span data-ttu-id="f9835-144">System. String</span><span class="sxs-lookup"><span data-stu-id="f9835-144">System.String</span></span>

### <span data-ttu-id="f9835-145">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="f9835-145">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="f9835-146">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f9835-146">OUTPUTS</span></span>

### <span data-ttu-id="f9835-147">Microsoft. Azure. Commands. COMPUTE. modeller. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="f9835-147">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="f9835-148">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f9835-148">NOTES</span></span>

## <span data-ttu-id="f9835-149">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f9835-149">RELATED LINKS</span></span>
