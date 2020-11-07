---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 3D2E9FAE-FE34-457A-BE95-BC61D025B07A
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactory.md
ms.openlocfilehash: 39a05b943e0255162948476a9da1c9a2c55f17a3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93752492"
---
# <span data-ttu-id="fa0ce-101">Remove-AzDataFactory</span><span class="sxs-lookup"><span data-stu-id="fa0ce-101">Remove-AzDataFactory</span></span>

## <span data-ttu-id="fa0ce-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fa0ce-102">SYNOPSIS</span></span>
<span data-ttu-id="fa0ce-103">Veri Fabrikası kaldırır.</span><span class="sxs-lookup"><span data-stu-id="fa0ce-103">Removes a data factory.</span></span>

## <span data-ttu-id="fa0ce-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fa0ce-104">SYNTAX</span></span>

### <span data-ttu-id="fa0ce-105">ByFactoryName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="fa0ce-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactory [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fa0ce-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="fa0ce-106">ByFactoryObject</span></span>
```
Remove-AzDataFactory [-DataFactory] <PSDataFactory> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fa0ce-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="fa0ce-107">DESCRIPTION</span></span>
<span data-ttu-id="fa0ce-108">**Remove-AzDataFactory** cmdlet 'i Veri Fabrikası çıkarır.</span><span class="sxs-lookup"><span data-stu-id="fa0ce-108">The **Remove-AzDataFactory** cmdlet removes a data factory.</span></span>

## <span data-ttu-id="fa0ce-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fa0ce-109">EXAMPLES</span></span>

### <span data-ttu-id="fa0ce-110">Örnek 1: Veri Fabrikası kaldırma</span><span class="sxs-lookup"><span data-stu-id="fa0ce-110">Example 1: Remove a data factory</span></span>
```
PS C:\>Remove-AzDataFactory -Name "WikiADF" -ResourceGroupName "ADF"
Confirm
Are you sure you want to remove data factory 'WikiADF' in resource group 'ADF'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
True
```

<span data-ttu-id="fa0ce-111">Bu komut, Obkiadf adındaki</span><span class="sxs-lookup"><span data-stu-id="fa0ce-111">This command removes the data factory named WikiADF from the resource group named ADF.</span></span>
<span data-ttu-id="fa0ce-112">Bu komut $True değerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="fa0ce-112">This command returns a value of $True.</span></span>

## <span data-ttu-id="fa0ce-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fa0ce-113">PARAMETERS</span></span>

### <span data-ttu-id="fa0ce-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="fa0ce-114">-DataFactory</span></span>
<span data-ttu-id="fa0ce-115">Kaldırılacak **Psdatafactory** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="fa0ce-115">Specifies the **PSDataFactory** object to remove.</span></span>

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

### <span data-ttu-id="fa0ce-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa0ce-116">-DefaultProfile</span></span>
<span data-ttu-id="fa0ce-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="fa0ce-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fa0ce-118">-Force</span><span class="sxs-lookup"><span data-stu-id="fa0ce-118">-Force</span></span>
<span data-ttu-id="fa0ce-119">Bu cmdlet 'in bir veri fabrikası onaylamanızı istemeden kaldırmadığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="fa0ce-119">Indicates that this cmdlet removes a data factory without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="fa0ce-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="fa0ce-120">-Name</span></span>
<span data-ttu-id="fa0ce-121">Kaldırılacak Veri Fabrikası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fa0ce-121">Specifies the name of the data factory to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: DataFactoryName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa0ce-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fa0ce-122">-ResourceGroupName</span></span>
<span data-ttu-id="fa0ce-123">Bir Azure Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fa0ce-123">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="fa0ce-124">Bu cmdlet, bu parametrenin belirttiği gruptan bir veri fabrikası kaldırır.</span><span class="sxs-lookup"><span data-stu-id="fa0ce-124">This cmdlet removes a data factory from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="fa0ce-125">-Onay</span><span class="sxs-lookup"><span data-stu-id="fa0ce-125">-Confirm</span></span>
<span data-ttu-id="fa0ce-126">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="fa0ce-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fa0ce-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fa0ce-127">-WhatIf</span></span>
<span data-ttu-id="fa0ce-128">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="fa0ce-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fa0ce-129">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="fa0ce-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fa0ce-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa0ce-130">CommonParameters</span></span>
<span data-ttu-id="fa0ce-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fa0ce-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa0ce-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fa0ce-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa0ce-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fa0ce-133">INPUTS</span></span>

### <span data-ttu-id="fa0ce-134">System. String</span><span class="sxs-lookup"><span data-stu-id="fa0ce-134">System.String</span></span>

### <span data-ttu-id="fa0ce-135">Microsoft.Azure.Commands.DataFactories.Models.PSDAtafabrikası</span><span class="sxs-lookup"><span data-stu-id="fa0ce-135">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="fa0ce-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fa0ce-136">OUTPUTS</span></span>

### <span data-ttu-id="fa0ce-137">System. void</span><span class="sxs-lookup"><span data-stu-id="fa0ce-137">System.Void</span></span>

## <span data-ttu-id="fa0ce-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fa0ce-138">NOTES</span></span>
* <span data-ttu-id="fa0ce-139">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, veri, fabrikalar</span><span class="sxs-lookup"><span data-stu-id="fa0ce-139">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="fa0ce-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fa0ce-140">RELATED LINKS</span></span>

[<span data-ttu-id="fa0ce-141">Get-AzDataFactory</span><span class="sxs-lookup"><span data-stu-id="fa0ce-141">Get-AzDataFactory</span></span>](./Get-AzDataFactory.md)

[<span data-ttu-id="fa0ce-142">New-AzDataFactory</span><span class="sxs-lookup"><span data-stu-id="fa0ce-142">New-AzDataFactory</span></span>](./New-AzDataFactory.md)

