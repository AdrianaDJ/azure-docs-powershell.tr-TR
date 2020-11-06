---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/update-azurermdatafactoryv2
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Update-AzureRmDataFactoryV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Update-AzureRmDataFactoryV2.md
ms.openlocfilehash: 09e13e973178444496604843336c8f483508c59e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590317"
---
# <span data-ttu-id="f1e9f-101">Update-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="f1e9f-101">Update-AzureRmDataFactoryV2</span></span>

## <span data-ttu-id="f1e9f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f1e9f-102">SYNOPSIS</span></span>
<span data-ttu-id="f1e9f-103">Veri Fabrikası özelliklerini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="f1e9f-103">Updates the properties of a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f1e9f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f1e9f-104">SYNTAX</span></span>

### <span data-ttu-id="f1e9f-105">ByFactoryName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="f1e9f-105">ByFactoryName (Default)</span></span>
```
Update-AzureRmDataFactoryV2 [-ResourceGroupName] <String> [-Name] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f1e9f-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="f1e9f-106">ByFactoryObject</span></span>
```
Update-AzureRmDataFactoryV2 [-InputObject] <PSDataFactory> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f1e9f-107">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="f1e9f-107">ByResourceId</span></span>
```
Update-AzureRmDataFactoryV2 [-ResourceId] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f1e9f-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="f1e9f-108">DESCRIPTION</span></span>
<span data-ttu-id="f1e9f-109">**Update-AzureRmDataFactoryV2** cmdlet 'i Veri Fabrikası için etiketleri veya kimlik özelliklerini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="f1e9f-109">The **Update-AzureRmDataFactoryV2** cmdlet updates tags or identity properties of a data factory.</span></span>

## <span data-ttu-id="f1e9f-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f1e9f-110">EXAMPLES</span></span>

### <span data-ttu-id="f1e9f-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="f1e9f-111">Example 1</span></span>
```
PS C:\> Update-AzureRmDataFactoryV2 -ResourceGroupName "ADF" -Name "WikiADF" -Tag @{myNewTagName = "myTagValue"}

Confirm
Are you sure you want to update properties of the data factory 'WikiADF' in resource group 'ADF'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y


DataFactoryName   : WikiADF
DataFactoryId     : /subscriptions/1e42591f-1f0c-4c5a-b7f2-a268f6105ec5/resourceGroups/adf/providers/Microsoft.DataF
                    actory/factories/wikiadf
ResourceGroupName : ADF
Location          : EastUS
Tags              : {[myNewTagName, myTagValue]}
Identity          :
ProvisioningState : Succeeded
```

<span data-ttu-id="f1e9f-112">Bu komut, fabrimilkadf 'deki etiketleri myTagValue değerine sahip Yenontagname adlı bir etikete sahip bir sözlüğe güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="f1e9f-112">This command updates the tags for the factory WikiADF to a dictionary containing a tag named myNewTagName with value myTagValue.</span></span>

## <span data-ttu-id="f1e9f-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f1e9f-113">PARAMETERS</span></span>

### <span data-ttu-id="f1e9f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1e9f-114">-DefaultProfile</span></span>
<span data-ttu-id="f1e9f-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f1e9f-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f1e9f-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f1e9f-116">-InputObject</span></span>
<span data-ttu-id="f1e9f-117">Veri fabrikası nesnesi.</span><span class="sxs-lookup"><span data-stu-id="f1e9f-117">The data factory object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f1e9f-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="f1e9f-118">-Name</span></span>
<span data-ttu-id="f1e9f-119">Veri Fabrikası adı.</span><span class="sxs-lookup"><span data-stu-id="f1e9f-119">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: DataFactoryName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1e9f-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f1e9f-120">-ResourceGroupName</span></span>
<span data-ttu-id="f1e9f-121">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="f1e9f-121">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1e9f-122">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="f1e9f-122">-ResourceId</span></span>
<span data-ttu-id="f1e9f-123">Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="f1e9f-123">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1e9f-124">Etiketli</span><span class="sxs-lookup"><span data-stu-id="f1e9f-124">-Tag</span></span>
<span data-ttu-id="f1e9f-125">Veri Fabrikası 'nin etiketleri.</span><span class="sxs-lookup"><span data-stu-id="f1e9f-125">The tags of the data factory.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1e9f-126">-Onay</span><span class="sxs-lookup"><span data-stu-id="f1e9f-126">-Confirm</span></span>
<span data-ttu-id="f1e9f-127">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="f1e9f-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f1e9f-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f1e9f-128">-WhatIf</span></span>
<span data-ttu-id="f1e9f-129">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f1e9f-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f1e9f-130">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="f1e9f-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f1e9f-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1e9f-131">CommonParameters</span></span>
<span data-ttu-id="f1e9f-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f1e9f-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1e9f-133">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f1e9f-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1e9f-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f1e9f-134">INPUTS</span></span>

### <span data-ttu-id="f1e9f-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDAtafabrikası</span><span class="sxs-lookup"><span data-stu-id="f1e9f-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>
<span data-ttu-id="f1e9f-136">Parametreler: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="f1e9f-136">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="f1e9f-137">System. String</span><span class="sxs-lookup"><span data-stu-id="f1e9f-137">System.String</span></span>

## <span data-ttu-id="f1e9f-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f1e9f-138">OUTPUTS</span></span>

### <span data-ttu-id="f1e9f-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDAtafabrikası</span><span class="sxs-lookup"><span data-stu-id="f1e9f-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="f1e9f-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f1e9f-140">NOTES</span></span>

## <span data-ttu-id="f1e9f-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f1e9f-141">RELATED LINKS</span></span>
