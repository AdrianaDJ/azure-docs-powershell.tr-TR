---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/remove-azurermdatafactoryv2
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Remove-AzureRmDataFactoryV2.md
ms.openlocfilehash: 330bcf3622faa515a58ea8f1e087d1383b9f154a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93586733"
---
# <span data-ttu-id="fef3d-101">Remove-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="fef3d-101">Remove-AzureRmDataFactoryV2</span></span>

## <span data-ttu-id="fef3d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fef3d-102">SYNOPSIS</span></span>
<span data-ttu-id="fef3d-103">Veri Fabrikası kaldırır.</span><span class="sxs-lookup"><span data-stu-id="fef3d-103">Removes a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fef3d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fef3d-104">SYNTAX</span></span>

### <span data-ttu-id="fef3d-105">ByFactoryName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="fef3d-105">ByFactoryName (Default)</span></span>
```
Remove-AzureRmDataFactoryV2 [-ResourceGroupName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fef3d-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="fef3d-106">ByFactoryObject</span></span>
```
Remove-AzureRmDataFactoryV2 [-InputObject] <PSDataFactory> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fef3d-107">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="fef3d-107">ByResourceId</span></span>
```
Remove-AzureRmDataFactoryV2 [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fef3d-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="fef3d-108">DESCRIPTION</span></span>
<span data-ttu-id="fef3d-109">Remove-AzureRmDataFactoryV2 cmdlet 'i Veri Fabrikası çıkarır.</span><span class="sxs-lookup"><span data-stu-id="fef3d-109">The Remove-AzureRmDataFactoryV2 cmdlet removes a data factory.</span></span>

## <span data-ttu-id="fef3d-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fef3d-110">EXAMPLES</span></span>

### <span data-ttu-id="fef3d-111">Örnek 1: Veri Fabrikası kaldırma</span><span class="sxs-lookup"><span data-stu-id="fef3d-111">Example 1: Remove a data factory</span></span>
```
PS C:\> Remove-AzureRmDataFactoryV2 -Name "WikiADF" -ResourceGroupName "ADF"
          Confirm
          Are you sure you want to remove data factory 'WikiADF' in resource group 'ADF'?
          [Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
          True
```

<span data-ttu-id="fef3d-112">Bu komut, Obkiadf adındaki</span><span class="sxs-lookup"><span data-stu-id="fef3d-112">This command removes the data factory named WikiADF from the resource group named ADF.</span></span>
<span data-ttu-id="fef3d-113">Bu komut $True değerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="fef3d-113">This command returns a value of $True.</span></span>

## <span data-ttu-id="fef3d-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fef3d-114">PARAMETERS</span></span>

### <span data-ttu-id="fef3d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fef3d-115">-DefaultProfile</span></span>
<span data-ttu-id="fef3d-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="fef3d-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fef3d-117">-Force</span><span class="sxs-lookup"><span data-stu-id="fef3d-117">-Force</span></span>
<span data-ttu-id="fef3d-118">Onay istemeden cmdlet 'i çalıştırır.</span><span class="sxs-lookup"><span data-stu-id="fef3d-118">Runs the cmdlet without prompting for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fef3d-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fef3d-119">-InputObject</span></span>
<span data-ttu-id="fef3d-120">Kaldırılacak DataFactory nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="fef3d-120">Specifies the DataFactory object to remove.</span></span>

```yaml
Type: PSDataFactory
Parameter Sets: ByFactoryObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fef3d-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="fef3d-121">-Name</span></span>
<span data-ttu-id="fef3d-122">Kaldırılacak Veri Fabrikası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fef3d-122">Specifies the name of the data factory to remove.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: DataFactoryName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fef3d-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fef3d-123">-ResourceGroupName</span></span>
<span data-ttu-id="fef3d-124">Bir Azure Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fef3d-124">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="fef3d-125">Bu cmdlet, bu parametrenin belirttiği gruptan bir veri fabrikası kaldırır.</span><span class="sxs-lookup"><span data-stu-id="fef3d-125">This cmdlet removes a data factory from the group that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fef3d-126">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="fef3d-126">-ResourceId</span></span>
<span data-ttu-id="fef3d-127">Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="fef3d-127">The Azure resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fef3d-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="fef3d-128">-Confirm</span></span>
<span data-ttu-id="fef3d-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="fef3d-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fef3d-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fef3d-130">-WhatIf</span></span>
<span data-ttu-id="fef3d-131">Cmdlet çalışırsa ne olacağını gösterir, ancak cmdlet 'i çalıştırmaz.</span><span class="sxs-lookup"><span data-stu-id="fef3d-131">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fef3d-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fef3d-132">CommonParameters</span></span>
<span data-ttu-id="fef3d-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fef3d-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fef3d-134">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fef3d-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fef3d-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fef3d-135">INPUTS</span></span>

### <span data-ttu-id="fef3d-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDAtafabrikası</span><span class="sxs-lookup"><span data-stu-id="fef3d-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>
<span data-ttu-id="fef3d-137">System. String</span><span class="sxs-lookup"><span data-stu-id="fef3d-137">System.String</span></span>

## <span data-ttu-id="fef3d-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fef3d-138">OUTPUTS</span></span>

### <span data-ttu-id="fef3d-139">System. Object</span><span class="sxs-lookup"><span data-stu-id="fef3d-139">System.Object</span></span>

## <span data-ttu-id="fef3d-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fef3d-140">NOTES</span></span>
<span data-ttu-id="fef3d-141">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, veri, fabrikalar</span><span class="sxs-lookup"><span data-stu-id="fef3d-141">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="fef3d-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fef3d-142">RELATED LINKS</span></span>

[<span data-ttu-id="fef3d-143">Get-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="fef3d-143">Get-AzureRmDataFactoryV2</span></span>]()

[<span data-ttu-id="fef3d-144">Set-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="fef3d-144">Set-AzureRmDataFactoryV2</span></span>]()
