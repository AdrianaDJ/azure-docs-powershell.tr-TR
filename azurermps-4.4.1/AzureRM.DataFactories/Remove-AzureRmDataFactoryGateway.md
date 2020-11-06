---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: E1461540-DEAE-43C3-83DF-7DF3FE8D4EC0
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Remove-AzureRmDataFactoryGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Remove-AzureRmDataFactoryGateway.md
ms.openlocfilehash: d9ae03325afbfe81c47847cb27df75973221667b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591114"
---
# <span data-ttu-id="4cca5-101">Remove-AzureRmDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="4cca5-101">Remove-AzureRmDataFactoryGateway</span></span>

## <span data-ttu-id="4cca5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4cca5-102">SYNOPSIS</span></span>
<span data-ttu-id="4cca5-103">Azure Veri Fabrikası 'ndan ağ geçidini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="4cca5-103">Removes a gateway from Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4cca5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4cca5-104">SYNTAX</span></span>

### <span data-ttu-id="4cca5-105">ByFactoryName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="4cca5-105">ByFactoryName (Default)</span></span>
```
Remove-AzureRmDataFactoryGateway [-DataFactoryName] <String> [-Name] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4cca5-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="4cca5-106">ByFactoryObject</span></span>
```
Remove-AzureRmDataFactoryGateway [-DataFactory] <PSDataFactory> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4cca5-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="4cca5-107">DESCRIPTION</span></span>
<span data-ttu-id="4cca5-108">**Remove-AzureRmDataFactoryGateway** cmdlet 'ı Azure Veri Fabrikası 'ndan belirtilen ağ geçidini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="4cca5-108">The **Remove-AzureRmDataFactoryGateway** cmdlet removes the specified gateway from Azure Data Factory.</span></span>

## <span data-ttu-id="4cca5-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4cca5-109">EXAMPLES</span></span>

### <span data-ttu-id="4cca5-110">Örnek 1: ağ geçidini kaldırma</span><span class="sxs-lookup"><span data-stu-id="4cca5-110">Example 1: Remove a gateway</span></span>
```
PS C:\>Remove-AzureRmDataFactoryGateway -Name "ContosoGateway" -DataFactoryName "WikiADF" -ResourceGroupName "ADF"
Confirm
Are you sure you want to remove gateway 'ContosoGateway' in data factory 'WikiADF'? 
 [Y] Yes  [N] No  [S] Suspend  [?] Help (default is Y): Y
True
```

<span data-ttu-id="4cca5-111">Bu komut, WikiADF adlı veri fabrikası</span><span class="sxs-lookup"><span data-stu-id="4cca5-111">This command removes the gateway named ContosoGateway from the data factory named WikiADF.</span></span>

## <span data-ttu-id="4cca5-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4cca5-112">PARAMETERS</span></span>

### <span data-ttu-id="4cca5-113">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="4cca5-113">-DataFactory</span></span>
<span data-ttu-id="4cca5-114">**Psdatafactory** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="4cca5-114">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="4cca5-115">Bu cmdlet, bu parametrenin belirttiği veri fabrikaından gelen ağ geçidini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="4cca5-115">This cmdlet removes a gateway from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="4cca5-116">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="4cca5-116">-DataFactoryName</span></span>
<span data-ttu-id="4cca5-117">Veri Fabrikası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4cca5-117">Specifies the name of a data factory.</span></span>
<span data-ttu-id="4cca5-118">Bu cmdlet, bu parametrenin belirttiği veri fabrikaından gelen ağ geçidini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="4cca5-118">This cmdlet removes a gateway from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="4cca5-119">-Force</span><span class="sxs-lookup"><span data-stu-id="4cca5-119">-Force</span></span>
<span data-ttu-id="4cca5-120">Bu cmdlet 'in bir ağ geçidini onaylamanızı istemeden kaldırmadığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="4cca5-120">Indicates that this cmdlet removes a gateway without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="4cca5-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="4cca5-121">-Name</span></span>
<span data-ttu-id="4cca5-122">Kaldırılacak ağ geçidinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4cca5-122">Specifies the name of the gateway to remove.</span></span>

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

### <span data-ttu-id="4cca5-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4cca5-123">-ResourceGroupName</span></span>
<span data-ttu-id="4cca5-124">Bir Azure Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4cca5-124">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="4cca5-125">Bu cmdlet, bu parametrenin belirttiği gruba ait bir ağ geçidini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="4cca5-125">This cmdlet removes a gateway that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="4cca5-126">-Onay</span><span class="sxs-lookup"><span data-stu-id="4cca5-126">-Confirm</span></span>
<span data-ttu-id="4cca5-127">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="4cca5-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4cca5-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4cca5-128">-WhatIf</span></span>
<span data-ttu-id="4cca5-129">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="4cca5-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4cca5-130">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="4cca5-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4cca5-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4cca5-131">-DefaultProfile</span></span>
<span data-ttu-id="4cca5-132">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4cca5-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4cca5-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4cca5-133">CommonParameters</span></span>
<span data-ttu-id="4cca5-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4cca5-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4cca5-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4cca5-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4cca5-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4cca5-136">INPUTS</span></span>

## <span data-ttu-id="4cca5-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4cca5-137">OUTPUTS</span></span>

### <span data-ttu-id="4cca5-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4cca5-138">System.Boolean</span></span>

## <span data-ttu-id="4cca5-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4cca5-139">NOTES</span></span>
* <span data-ttu-id="4cca5-140">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, veri, fabrikalar</span><span class="sxs-lookup"><span data-stu-id="4cca5-140">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="4cca5-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4cca5-141">RELATED LINKS</span></span>

[<span data-ttu-id="4cca5-142">Get-AzureRmDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="4cca5-142">Get-AzureRmDataFactoryGateway</span></span>](./Get-AzureRmDataFactoryGateway.md)

[<span data-ttu-id="4cca5-143">Yeni-AzureRmDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="4cca5-143">New-AzureRmDataFactoryGateway</span></span>](./New-AzureRmDataFactoryGateway.md)

[<span data-ttu-id="4cca5-144">Set-AzureRmDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="4cca5-144">Set-AzureRmDataFactoryGateway</span></span>](./Set-AzureRmDataFactoryGateway.md)


