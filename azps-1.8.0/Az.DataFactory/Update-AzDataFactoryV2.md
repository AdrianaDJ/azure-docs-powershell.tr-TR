---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/update-azdatafactoryv2
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Update-AzDataFactoryV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Update-AzDataFactoryV2.md
ms.openlocfilehash: 85bd5f6eef9c4f10d8a40ee58817f531a542d9ff
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93917003"
---
# <span data-ttu-id="eaaaa-101">Update-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="eaaaa-101">Update-AzDataFactoryV2</span></span>

## <span data-ttu-id="eaaaa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eaaaa-102">SYNOPSIS</span></span>
<span data-ttu-id="eaaaa-103">Veri Fabrikası özelliklerini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="eaaaa-103">Updates the properties of a data factory.</span></span>

## <span data-ttu-id="eaaaa-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="eaaaa-104">SYNTAX</span></span>

### <span data-ttu-id="eaaaa-105">ByFactoryName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="eaaaa-105">ByFactoryName (Default)</span></span>
```
Update-AzDataFactoryV2 [-ResourceGroupName] <String> [-Name] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eaaaa-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="eaaaa-106">ByFactoryObject</span></span>
```
Update-AzDataFactoryV2 [-InputObject] <PSDataFactory> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eaaaa-107">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="eaaaa-107">ByResourceId</span></span>
```
Update-AzDataFactoryV2 [-ResourceId] <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eaaaa-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="eaaaa-108">DESCRIPTION</span></span>
<span data-ttu-id="eaaaa-109">**Update-AzDataFactoryV2** cmdlet 'i Veri Fabrikası için etiketleri veya kimlik özelliklerini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="eaaaa-109">The **Update-AzDataFactoryV2** cmdlet updates tags or identity properties of a data factory.</span></span>

## <span data-ttu-id="eaaaa-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="eaaaa-110">EXAMPLES</span></span>

### <span data-ttu-id="eaaaa-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="eaaaa-111">Example 1</span></span>
```
PS C:\> Update-AzDataFactoryV2 -ResourceGroupName "ADF" -Name "WikiADF" -Tag @{myNewTagName = "myTagValue"}

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

<span data-ttu-id="eaaaa-112">Bu komut, fabrimilkadf 'deki etiketleri myTagValue değerine sahip Yenontagname adlı bir etikete sahip bir sözlüğe güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="eaaaa-112">This command updates the tags for the factory WikiADF to a dictionary containing a tag named myNewTagName with value myTagValue.</span></span>

## <span data-ttu-id="eaaaa-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="eaaaa-113">PARAMETERS</span></span>

### <span data-ttu-id="eaaaa-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eaaaa-114">-DefaultProfile</span></span>
<span data-ttu-id="eaaaa-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="eaaaa-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eaaaa-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="eaaaa-116">-InputObject</span></span>
<span data-ttu-id="eaaaa-117">Veri fabrikası nesnesi.</span><span class="sxs-lookup"><span data-stu-id="eaaaa-117">The data factory object.</span></span>

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

### <span data-ttu-id="eaaaa-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="eaaaa-118">-Name</span></span>
<span data-ttu-id="eaaaa-119">Veri Fabrikası adı.</span><span class="sxs-lookup"><span data-stu-id="eaaaa-119">The data factory name.</span></span>

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

### <span data-ttu-id="eaaaa-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eaaaa-120">-ResourceGroupName</span></span>
<span data-ttu-id="eaaaa-121">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="eaaaa-121">The resource group name.</span></span>

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

### <span data-ttu-id="eaaaa-122">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="eaaaa-122">-ResourceId</span></span>
<span data-ttu-id="eaaaa-123">Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="eaaaa-123">The Azure resource ID.</span></span>

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

### <span data-ttu-id="eaaaa-124">Etiketli</span><span class="sxs-lookup"><span data-stu-id="eaaaa-124">-Tag</span></span>
<span data-ttu-id="eaaaa-125">Veri Fabrikası 'nin etiketleri.</span><span class="sxs-lookup"><span data-stu-id="eaaaa-125">The tags of the data factory.</span></span>

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

### <span data-ttu-id="eaaaa-126">-Onay</span><span class="sxs-lookup"><span data-stu-id="eaaaa-126">-Confirm</span></span>
<span data-ttu-id="eaaaa-127">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="eaaaa-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eaaaa-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eaaaa-128">-WhatIf</span></span>
<span data-ttu-id="eaaaa-129">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="eaaaa-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="eaaaa-130">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="eaaaa-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eaaaa-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eaaaa-131">CommonParameters</span></span>
<span data-ttu-id="eaaaa-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="eaaaa-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eaaaa-133">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eaaaa-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eaaaa-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="eaaaa-134">INPUTS</span></span>

### <span data-ttu-id="eaaaa-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDAtafabrikası</span><span class="sxs-lookup"><span data-stu-id="eaaaa-135">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

### <span data-ttu-id="eaaaa-136">System. String</span><span class="sxs-lookup"><span data-stu-id="eaaaa-136">System.String</span></span>

## <span data-ttu-id="eaaaa-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="eaaaa-137">OUTPUTS</span></span>

### <span data-ttu-id="eaaaa-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDAtafabrikası</span><span class="sxs-lookup"><span data-stu-id="eaaaa-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="eaaaa-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="eaaaa-139">NOTES</span></span>

## <span data-ttu-id="eaaaa-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="eaaaa-140">RELATED LINKS</span></span>