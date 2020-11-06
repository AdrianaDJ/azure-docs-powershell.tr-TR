---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: B2B4E132-4A71-4DB8-A7B9-9ED3FE7EB292
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMBginfoExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMBginfoExtension.md
ms.openlocfilehash: c52be698b216d206fe95ba5ea3aefc810f22fff2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587604"
---
# <span data-ttu-id="59b18-101">Set-AzureRmVMBginfoExtension</span><span class="sxs-lookup"><span data-stu-id="59b18-101">Set-AzureRmVMBginfoExtension</span></span>

## <span data-ttu-id="59b18-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="59b18-102">SYNOPSIS</span></span>
<span data-ttu-id="59b18-103">Bir sanal makineye BgInfo uzantısını ekler.</span><span class="sxs-lookup"><span data-stu-id="59b18-103">Adds the BGInfo extension to a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="59b18-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="59b18-104">SYNTAX</span></span>

```
Set-AzureRmVMBginfoExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="59b18-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="59b18-105">DESCRIPTION</span></span>
<span data-ttu-id="59b18-106">**Set-AzureRmVMBGInfoExtension** cmdlet 'ı, BgInfo uzantısını bir sanal makineye ekler.</span><span class="sxs-lookup"><span data-stu-id="59b18-106">The **Set-AzureRmVMBGInfoExtension** cmdlet adds the BGInfo extension to a virtual machine.</span></span>

## <span data-ttu-id="59b18-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="59b18-107">EXAMPLES</span></span>

### <span data-ttu-id="59b18-108">Örnek 1: bir sanal makineye BgInfo uzantısını ekleme</span><span class="sxs-lookup"><span data-stu-id="59b18-108">Example 1: Add the BGInfo extension to a virtual machine</span></span>
```
PS C:\> Set-AzureRmVMBgInfoExtension -ResourceGroupName "ContosoRG" -VMName "ContosoVM"
```
<span data-ttu-id="59b18-109">Bu komut, BgInfo uzantısını kaynak grup ContosoRG ContosoVM adındaki bir sanal makineye ekler.</span><span class="sxs-lookup"><span data-stu-id="59b18-109">This command adds the BGInfo extension to a virtual machine named ContosoVM in the resource group ContosoRG.</span></span>

### <span data-ttu-id="59b18-110">Örnek 2: bir sanal makineye BgInfo uzantısının belirli bir sürümünü ekleme</span><span class="sxs-lookup"><span data-stu-id="59b18-110">Example 2: Add a specific version of BGInfo extension to a virtual machine</span></span>
```
PS C:\> Set-AzureRmVMBgInfoExtension -ResourceGroupName "ContosoRG" -VMName "ContosoVM" -Name "ExtensionName" -TypeHandlerVersion "2.1" -Location "West Europe"
```

<span data-ttu-id="59b18-111">Bu komut, bir BgInfo uzantısını ContosoVM adındaki sanal makineye ekler.</span><span class="sxs-lookup"><span data-stu-id="59b18-111">This command adds the BGInfo extension to virtual machine named ContosoVM.</span></span>
<span data-ttu-id="59b18-112">Komut sanal makinenin kaynak grubunu ve konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="59b18-112">The command specifies the resource group and location of the virtual machine.</span></span>
<span data-ttu-id="59b18-113">Komut, uzantının adını ve sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="59b18-113">The command specifies the name and version of the extension.</span></span>

## <span data-ttu-id="59b18-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="59b18-114">PARAMETERS</span></span>

### <span data-ttu-id="59b18-115">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="59b18-115">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="59b18-116">Bu cmdlet 'in, Azure Konuk aracısının uzantıyı daha yeni bir alt sürüme otomatik olarak güncelleştirmesini engellediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="59b18-116">Indicates that this cmdlet prevents the Azure guest agent from automatically updating the extension to a newer minor version.</span></span>
<span data-ttu-id="59b18-117">Varsayılan olarak, bu cmdlet Konuk aracısının uzantıyı güncelleştirmesini olanaklı kılar.</span><span class="sxs-lookup"><span data-stu-id="59b18-117">By default, this cmdlet enables the guest agent to update the extension.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59b18-118">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="59b18-118">-ForceRerun</span></span>
<span data-ttu-id="59b18-119">Uzantının aynı genel veya korumalı ayarlarla yeniden çalıştırılması gerektiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="59b18-119">Specifies that the extension should be run again with the same public or protected settings.</span></span>
<span data-ttu-id="59b18-120">Değer, geçerli değerden farklı olabilir.</span><span class="sxs-lookup"><span data-stu-id="59b18-120">The value can be any string different from the current value.</span></span>

<span data-ttu-id="59b18-121">ForceUpdateTag değiştirilirse, genel veya korumalı ayarlara yönelik güncelleştirmeler işleyici tarafından uygulanır.</span><span class="sxs-lookup"><span data-stu-id="59b18-121">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59b18-122">-Konum</span><span class="sxs-lookup"><span data-stu-id="59b18-122">-Location</span></span>
<span data-ttu-id="59b18-123">Sanal makinenin konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="59b18-123">Specifies the location of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59b18-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="59b18-124">-Name</span></span>
<span data-ttu-id="59b18-125">Bu cmdlet 'in sanal makineye eklediği BgInfo uzantısının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="59b18-125">Specifies the name of the BGInfo extension that this cmdlet adds to a virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59b18-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="59b18-126">-ResourceGroupName</span></span>
<span data-ttu-id="59b18-127">Bu cmdlet 'in uzantısı eklediği sanal makinenin kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="59b18-127">Specifies the name of the resource group of the virtual machine to which this cmdlet adds an extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59b18-128">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="59b18-128">-TypeHandlerVersion</span></span>
<span data-ttu-id="59b18-129">Bu cmdlet 'in sanal makineye eklediği uzantının sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="59b18-129">Specifies the version of the extension that this cmdlet adds to the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59b18-130">-VMName</span><span class="sxs-lookup"><span data-stu-id="59b18-130">-VMName</span></span>
<span data-ttu-id="59b18-131">Bu cmdlet 'in BgInfo uzantısını eklediği sanal makinenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="59b18-131">Specifies the name of the virtual machine to which this cmdlet adds the BGInfo extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59b18-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="59b18-132">-Confirm</span></span>
<span data-ttu-id="59b18-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="59b18-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59b18-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="59b18-134">-WhatIf</span></span>
<span data-ttu-id="59b18-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="59b18-135">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="59b18-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="59b18-136">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59b18-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59b18-137">CommonParameters</span></span>
<span data-ttu-id="59b18-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="59b18-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59b18-139">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59b18-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59b18-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="59b18-140">INPUTS</span></span>

### <span data-ttu-id="59b18-141">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="59b18-141">None</span></span>
<span data-ttu-id="59b18-142">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="59b18-142">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="59b18-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="59b18-143">OUTPUTS</span></span>

## <span data-ttu-id="59b18-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="59b18-144">NOTES</span></span>

## <span data-ttu-id="59b18-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="59b18-145">RELATED LINKS</span></span>

