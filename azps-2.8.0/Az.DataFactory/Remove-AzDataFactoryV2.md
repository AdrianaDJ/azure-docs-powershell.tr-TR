---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactoryv2
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2.md
ms.openlocfilehash: af16571402f3740c14e70433d82d494ca9f2b700
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93752481"
---
# <span data-ttu-id="0c7da-101">Remove-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="0c7da-101">Remove-AzDataFactoryV2</span></span>

## <span data-ttu-id="0c7da-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0c7da-102">SYNOPSIS</span></span>
<span data-ttu-id="0c7da-103">Veri Fabrikası kaldırır.</span><span class="sxs-lookup"><span data-stu-id="0c7da-103">Removes a data factory.</span></span>

## <span data-ttu-id="0c7da-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0c7da-104">SYNTAX</span></span>

### <span data-ttu-id="0c7da-105">ByFactoryName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="0c7da-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryV2 [-ResourceGroupName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0c7da-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="0c7da-106">ByFactoryObject</span></span>
```
Remove-AzDataFactoryV2 [-InputObject] <PSDataFactory> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0c7da-107">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="0c7da-107">ByResourceId</span></span>
```
Remove-AzDataFactoryV2 [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0c7da-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="0c7da-108">DESCRIPTION</span></span>
<span data-ttu-id="0c7da-109">Remove-AzDataFactoryV2 cmdlet 'i Veri Fabrikası çıkarır.</span><span class="sxs-lookup"><span data-stu-id="0c7da-109">The Remove-AzDataFactoryV2 cmdlet removes a data factory.</span></span>

## <span data-ttu-id="0c7da-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0c7da-110">EXAMPLES</span></span>

### <span data-ttu-id="0c7da-111">Örnek 1: Veri Fabrikası kaldırma</span><span class="sxs-lookup"><span data-stu-id="0c7da-111">Example 1: Remove a data factory</span></span>
```
PS C:\> Remove-AzDataFactoryV2 -Name "WikiADF" -ResourceGroupName "ADF"
          Confirm
          Are you sure you want to remove data factory 'WikiADF' in resource group 'ADF'?
          [Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
          True
```

<span data-ttu-id="0c7da-112">Bu komut, Obkiadf adındaki</span><span class="sxs-lookup"><span data-stu-id="0c7da-112">This command removes the data factory named WikiADF from the resource group named ADF.</span></span>
<span data-ttu-id="0c7da-113">Bu komut $True değerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="0c7da-113">This command returns a value of $True.</span></span>

## <span data-ttu-id="0c7da-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0c7da-114">PARAMETERS</span></span>

### <span data-ttu-id="0c7da-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c7da-115">-DefaultProfile</span></span>
<span data-ttu-id="0c7da-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0c7da-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0c7da-117">-Force</span><span class="sxs-lookup"><span data-stu-id="0c7da-117">-Force</span></span>
<span data-ttu-id="0c7da-118">Onay istemeden cmdlet 'i çalıştırır.</span><span class="sxs-lookup"><span data-stu-id="0c7da-118">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="0c7da-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0c7da-119">-InputObject</span></span>
<span data-ttu-id="0c7da-120">Kaldırılacak DataFactory nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="0c7da-120">Specifies the DataFactory object to remove.</span></span>

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

### <span data-ttu-id="0c7da-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="0c7da-121">-Name</span></span>
<span data-ttu-id="0c7da-122">Kaldırılacak Veri Fabrikası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0c7da-122">Specifies the name of the data factory to remove.</span></span>

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

### <span data-ttu-id="0c7da-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0c7da-123">-ResourceGroupName</span></span>
<span data-ttu-id="0c7da-124">Bir Azure Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0c7da-124">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="0c7da-125">Bu cmdlet, bu parametrenin belirttiği gruptan bir veri fabrikası kaldırır.</span><span class="sxs-lookup"><span data-stu-id="0c7da-125">This cmdlet removes a data factory from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="0c7da-126">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="0c7da-126">-ResourceId</span></span>
<span data-ttu-id="0c7da-127">Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="0c7da-127">The Azure resource ID.</span></span>

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

### <span data-ttu-id="0c7da-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="0c7da-128">-Confirm</span></span>
<span data-ttu-id="0c7da-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="0c7da-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0c7da-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0c7da-130">-WhatIf</span></span>
<span data-ttu-id="0c7da-131">Cmdlet çalışırsa ne olacağını gösterir, ancak cmdlet 'i çalıştırmaz.</span><span class="sxs-lookup"><span data-stu-id="0c7da-131">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="0c7da-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c7da-132">CommonParameters</span></span>
<span data-ttu-id="0c7da-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0c7da-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c7da-134">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0c7da-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c7da-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0c7da-135">INPUTS</span></span>

### <span data-ttu-id="0c7da-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDAtafabrikası</span><span class="sxs-lookup"><span data-stu-id="0c7da-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

### <span data-ttu-id="0c7da-137">System. String</span><span class="sxs-lookup"><span data-stu-id="0c7da-137">System.String</span></span>

## <span data-ttu-id="0c7da-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0c7da-138">OUTPUTS</span></span>

### <span data-ttu-id="0c7da-139">System. void</span><span class="sxs-lookup"><span data-stu-id="0c7da-139">System.Void</span></span>

## <span data-ttu-id="0c7da-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0c7da-140">NOTES</span></span>
<span data-ttu-id="0c7da-141">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, veri, fabrikalar</span><span class="sxs-lookup"><span data-stu-id="0c7da-141">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="0c7da-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0c7da-142">RELATED LINKS</span></span>

[<span data-ttu-id="0c7da-143">Get-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="0c7da-143">Get-AzDataFactoryV2</span></span>]()

[<span data-ttu-id="0c7da-144">Set-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="0c7da-144">Set-AzDataFactoryV2</span></span>]()
