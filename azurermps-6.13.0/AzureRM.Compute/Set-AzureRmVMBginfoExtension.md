---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: B2B4E132-4A71-4DB8-A7B9-9ED3FE7EB292
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmbginfoextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmVMBginfoExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmVMBginfoExtension.md
ms.openlocfilehash: ac2a4e4e7d05aa23a5870f8a07ded2c7a43fcdae
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587256"
---
# <span data-ttu-id="d790b-101">Set-AzureRmVMBginfoExtension</span><span class="sxs-lookup"><span data-stu-id="d790b-101">Set-AzureRmVMBginfoExtension</span></span>

## <span data-ttu-id="d790b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d790b-102">SYNOPSIS</span></span>
<span data-ttu-id="d790b-103">Bir sanal makineye BgInfo uzantısını ekler.</span><span class="sxs-lookup"><span data-stu-id="d790b-103">Adds the BGInfo extension to a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d790b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d790b-104">SYNTAX</span></span>

```
Set-AzureRmVMBginfoExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d790b-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="d790b-105">DESCRIPTION</span></span>
<span data-ttu-id="d790b-106">**Set-AzureRmVMBGInfoExtension** cmdlet 'ı, BgInfo uzantısını bir sanal makineye ekler.</span><span class="sxs-lookup"><span data-stu-id="d790b-106">The **Set-AzureRmVMBGInfoExtension** cmdlet adds the BGInfo extension to a virtual machine.</span></span>

## <span data-ttu-id="d790b-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d790b-107">EXAMPLES</span></span>

### <span data-ttu-id="d790b-108">Örnek 1: sanal makine için BgInfo uzantısını ekleme</span><span class="sxs-lookup"><span data-stu-id="d790b-108">Example 1: Add the BGInfo extension for a virtual machine</span></span>
```
PS C:\> Set-AzureRmVMBgInfoExtension -ResourceGroupName "ContosoRG" -VMName "ContosoVM" -Name "ExtensionName" -TypeHandlerVersion "2.1" -Location "West Europe"
```

<span data-ttu-id="d790b-109">Bu komut, bir BgInfo uzantısını ContosoVM adındaki sanal makineye ekler.</span><span class="sxs-lookup"><span data-stu-id="d790b-109">This command adds the BGInfo extension to virtual machine named ContosoVM.</span></span>
<span data-ttu-id="d790b-110">Komut sanal makinenin kaynak grubunu ve konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="d790b-110">The command specifies the resource group and location of the virtual machine.</span></span>
<span data-ttu-id="d790b-111">Komut, uzantının adını ve sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="d790b-111">The command specifies the name and version of the extension.</span></span>

## <span data-ttu-id="d790b-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d790b-112">PARAMETERS</span></span>

### <span data-ttu-id="d790b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d790b-113">-DefaultProfile</span></span>
<span data-ttu-id="d790b-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d790b-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d790b-115">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="d790b-115">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="d790b-116">Bu cmdlet 'in, Azure Konuk aracısının uzantıyı daha yeni bir alt sürüme otomatik olarak güncelleştirmesini engellediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="d790b-116">Indicates that this cmdlet prevents the Azure guest agent from automatically updating the extension to a newer minor version.</span></span>
<span data-ttu-id="d790b-117">Varsayılan olarak, bu cmdlet Konuk aracısının uzantıyı güncelleştirmesini olanaklı kılar.</span><span class="sxs-lookup"><span data-stu-id="d790b-117">By default, this cmdlet enables the guest agent to update the extension.</span></span>

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

### <span data-ttu-id="d790b-118">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="d790b-118">-ForceRerun</span></span>
<span data-ttu-id="d790b-119">Uzantının aynı genel veya korumalı ayarlarla yeniden çalıştırılması gerektiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="d790b-119">Specifies that the extension should be run again with the same public or protected settings.</span></span>
<span data-ttu-id="d790b-120">Değer, geçerli değerden farklı olabilir.</span><span class="sxs-lookup"><span data-stu-id="d790b-120">The value can be any string different from the current value.</span></span>
<span data-ttu-id="d790b-121">ForceUpdateTag değiştirilirse, genel veya korumalı ayarlara yönelik güncelleştirmeler işleyici tarafından uygulanır.</span><span class="sxs-lookup"><span data-stu-id="d790b-121">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

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

### <span data-ttu-id="d790b-122">-Konum</span><span class="sxs-lookup"><span data-stu-id="d790b-122">-Location</span></span>
<span data-ttu-id="d790b-123">Sanal makinenin konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="d790b-123">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="d790b-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="d790b-124">-Name</span></span>
<span data-ttu-id="d790b-125">Bu cmdlet 'in sanal makineye eklediği BgInfo uzantısının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d790b-125">Specifies the name of the BGInfo extension that this cmdlet adds to a virtual machine.</span></span>

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

### <span data-ttu-id="d790b-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d790b-126">-ResourceGroupName</span></span>
<span data-ttu-id="d790b-127">Bu cmdlet 'in uzantısı eklediği sanal makinenin kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d790b-127">Specifies the name of the resource group of the virtual machine to which this cmdlet adds an extension.</span></span>

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

### <span data-ttu-id="d790b-128">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="d790b-128">-TypeHandlerVersion</span></span>
<span data-ttu-id="d790b-129">Bu cmdlet 'in sanal makineye eklediği uzantının sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="d790b-129">Specifies the version of the extension that this cmdlet adds to the virtual machine.</span></span>

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

### <span data-ttu-id="d790b-130">-VMName</span><span class="sxs-lookup"><span data-stu-id="d790b-130">-VMName</span></span>
<span data-ttu-id="d790b-131">Bu cmdlet 'in BgInfo uzantısını eklediği sanal makinenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d790b-131">Specifies the name of the virtual machine to which this cmdlet adds the BGInfo extension.</span></span>

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

### <span data-ttu-id="d790b-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="d790b-132">-Confirm</span></span>
<span data-ttu-id="d790b-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d790b-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d790b-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d790b-134">-WhatIf</span></span>
<span data-ttu-id="d790b-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d790b-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d790b-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d790b-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d790b-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d790b-137">CommonParameters</span></span>
<span data-ttu-id="d790b-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d790b-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d790b-139">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d790b-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d790b-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d790b-140">INPUTS</span></span>

### <span data-ttu-id="d790b-141">System. String</span><span class="sxs-lookup"><span data-stu-id="d790b-141">System.String</span></span>

### <span data-ttu-id="d790b-142">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="d790b-142">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="d790b-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d790b-143">OUTPUTS</span></span>

### <span data-ttu-id="d790b-144">Microsoft. Azure. Commands. COMPUTE. modeller. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="d790b-144">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="d790b-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d790b-145">NOTES</span></span>

## <span data-ttu-id="d790b-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d790b-146">RELATED LINKS</span></span>
