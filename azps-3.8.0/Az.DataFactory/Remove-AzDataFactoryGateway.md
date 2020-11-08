---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: E1461540-DEAE-43C3-83DF-7DF3FE8D4EC0
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactorygateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryGateway.md
ms.openlocfilehash: 6831395c4f3d63dc056729b22573a16d863013e1
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93938319"
---
# <span data-ttu-id="d5ba0-101">Remove-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="d5ba0-101">Remove-AzDataFactoryGateway</span></span>

## <span data-ttu-id="d5ba0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d5ba0-102">SYNOPSIS</span></span>
<span data-ttu-id="d5ba0-103">Azure Veri Fabrikası 'ndan ağ geçidini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="d5ba0-103">Removes a gateway from Azure Data Factory.</span></span>

## <span data-ttu-id="d5ba0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d5ba0-104">SYNTAX</span></span>

### <span data-ttu-id="d5ba0-105">ByFactoryName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="d5ba0-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryGateway [-DataFactoryName] <String> [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d5ba0-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="d5ba0-106">ByFactoryObject</span></span>
```
Remove-AzDataFactoryGateway [-DataFactory] <PSDataFactory> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d5ba0-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="d5ba0-107">DESCRIPTION</span></span>
<span data-ttu-id="d5ba0-108">**Remove-AzDataFactoryGateway** cmdlet 'ı, Azure Veri Fabrikası 'ndan belirtilen ağ geçidini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="d5ba0-108">The **Remove-AzDataFactoryGateway** cmdlet removes the specified gateway from Azure Data Factory.</span></span>

## <span data-ttu-id="d5ba0-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d5ba0-109">EXAMPLES</span></span>

### <span data-ttu-id="d5ba0-110">Örnek 1: ağ geçidini kaldırma</span><span class="sxs-lookup"><span data-stu-id="d5ba0-110">Example 1: Remove a gateway</span></span>
```
PS C:\>Remove-AzDataFactoryGateway -Name "ContosoGateway" -DataFactoryName "WikiADF" -ResourceGroupName "ADF"
Confirm
Are you sure you want to remove gateway 'ContosoGateway' in data factory 'WikiADF'? 
 [Y] Yes  [N] No  [S] Suspend  [?] Help (default is Y): Y
True
```

<span data-ttu-id="d5ba0-111">Bu komut, WikiADF adlı veri fabrikası</span><span class="sxs-lookup"><span data-stu-id="d5ba0-111">This command removes the gateway named ContosoGateway from the data factory named WikiADF.</span></span>

## <span data-ttu-id="d5ba0-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d5ba0-112">PARAMETERS</span></span>

### <span data-ttu-id="d5ba0-113">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="d5ba0-113">-DataFactory</span></span>
<span data-ttu-id="d5ba0-114">**Psdatafactory** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="d5ba0-114">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="d5ba0-115">Bu cmdlet, bu parametrenin belirttiği veri fabrikaından gelen ağ geçidini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="d5ba0-115">This cmdlet removes a gateway from the data factory that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d5ba0-116">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="d5ba0-116">-DataFactoryName</span></span>
<span data-ttu-id="d5ba0-117">Veri Fabrikası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d5ba0-117">Specifies the name of a data factory.</span></span>
<span data-ttu-id="d5ba0-118">Bu cmdlet, bu parametrenin belirttiği veri fabrikaından gelen ağ geçidini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="d5ba0-118">This cmdlet removes a gateway from the data factory that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d5ba0-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5ba0-119">-DefaultProfile</span></span>
<span data-ttu-id="d5ba0-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="d5ba0-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d5ba0-121">-Force</span><span class="sxs-lookup"><span data-stu-id="d5ba0-121">-Force</span></span>
<span data-ttu-id="d5ba0-122">Bu cmdlet 'in bir ağ geçidini onaylamanızı istemeden kaldırmadığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d5ba0-122">Indicates that this cmdlet removes a gateway without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="d5ba0-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="d5ba0-123">-Name</span></span>
<span data-ttu-id="d5ba0-124">Kaldırılacak ağ geçidinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d5ba0-124">Specifies the name of the gateway to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d5ba0-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d5ba0-125">-ResourceGroupName</span></span>
<span data-ttu-id="d5ba0-126">Bir Azure Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="d5ba0-126">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="d5ba0-127">Bu cmdlet, bu parametrenin belirttiği gruba ait bir ağ geçidini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="d5ba0-127">This cmdlet removes a gateway that belongs to the group that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d5ba0-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="d5ba0-128">-Confirm</span></span>
<span data-ttu-id="d5ba0-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d5ba0-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d5ba0-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d5ba0-130">-WhatIf</span></span>
<span data-ttu-id="d5ba0-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d5ba0-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d5ba0-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d5ba0-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d5ba0-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5ba0-133">CommonParameters</span></span>
<span data-ttu-id="d5ba0-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d5ba0-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5ba0-135">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d5ba0-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5ba0-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d5ba0-136">INPUTS</span></span>

### <span data-ttu-id="d5ba0-137">Microsoft.Azure.Commands.DataFactories.Models.PSDAtafabrikası</span><span class="sxs-lookup"><span data-stu-id="d5ba0-137">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="d5ba0-138">System. String</span><span class="sxs-lookup"><span data-stu-id="d5ba0-138">System.String</span></span>

## <span data-ttu-id="d5ba0-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d5ba0-139">OUTPUTS</span></span>

### <span data-ttu-id="d5ba0-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d5ba0-140">System.Boolean</span></span>

## <span data-ttu-id="d5ba0-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d5ba0-141">NOTES</span></span>
* <span data-ttu-id="d5ba0-142">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, veri, fabrikalar</span><span class="sxs-lookup"><span data-stu-id="d5ba0-142">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="d5ba0-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d5ba0-143">RELATED LINKS</span></span>

[<span data-ttu-id="d5ba0-144">Get-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="d5ba0-144">Get-AzDataFactoryGateway</span></span>](./Get-AzDataFactoryGateway.md)

[<span data-ttu-id="d5ba0-145">New-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="d5ba0-145">New-AzDataFactoryGateway</span></span>](./New-AzDataFactoryGateway.md)

[<span data-ttu-id="d5ba0-146">Set-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="d5ba0-146">Set-AzDataFactoryGateway</span></span>](./Set-AzDataFactoryGateway.md)

