---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: 3D2E9FAE-FE34-457A-BE95-BC61D025B07A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Remove-AzureRmDataFactory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Remove-AzureRmDataFactory.md
ms.openlocfilehash: 59f1eabbadda682c87917f41d96959c691b9e593
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593157"
---
# <span data-ttu-id="c0ab3-101">Remove-AzureRmDataFactory</span><span class="sxs-lookup"><span data-stu-id="c0ab3-101">Remove-AzureRmDataFactory</span></span>

## <span data-ttu-id="c0ab3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c0ab3-102">SYNOPSIS</span></span>
<span data-ttu-id="c0ab3-103">Veri Fabrikası kaldırır.</span><span class="sxs-lookup"><span data-stu-id="c0ab3-103">Removes a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c0ab3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c0ab3-104">SYNTAX</span></span>

### <span data-ttu-id="c0ab3-105">ByFactoryName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="c0ab3-105">ByFactoryName (Default)</span></span>
```
Remove-AzureRmDataFactory [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c0ab3-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="c0ab3-106">ByFactoryObject</span></span>
```
Remove-AzureRmDataFactory [-DataFactory] <PSDataFactory> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c0ab3-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="c0ab3-107">DESCRIPTION</span></span>
<span data-ttu-id="c0ab3-108">**Remove-AzureRmDataFactory** cmdlet 'i Veri Fabrikası çıkarır.</span><span class="sxs-lookup"><span data-stu-id="c0ab3-108">The **Remove-AzureRmDataFactory** cmdlet removes a data factory.</span></span>

## <span data-ttu-id="c0ab3-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c0ab3-109">EXAMPLES</span></span>

### <span data-ttu-id="c0ab3-110">Örnek 1: Veri Fabrikası kaldırma</span><span class="sxs-lookup"><span data-stu-id="c0ab3-110">Example 1: Remove a data factory</span></span>
```
PS C:\>Remove-AzureRmDataFactory -Name "WikiADF" -ResourceGroupName "ADF"
Confirm
Are you sure you want to remove data factory 'WikiADF' in resource group 'ADF'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
True
```

<span data-ttu-id="c0ab3-111">Bu komut, Obkiadf adındaki</span><span class="sxs-lookup"><span data-stu-id="c0ab3-111">This command removes the data factory named WikiADF from the resource group named ADF.</span></span>
<span data-ttu-id="c0ab3-112">Bu komut $True değerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="c0ab3-112">This command returns a value of $True.</span></span>

## <span data-ttu-id="c0ab3-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c0ab3-113">PARAMETERS</span></span>

### <span data-ttu-id="c0ab3-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="c0ab3-114">-DataFactory</span></span>
<span data-ttu-id="c0ab3-115">Kaldırılacak **Psdatafactory** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="c0ab3-115">Specifies the **PSDataFactory** object to remove.</span></span>

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

### <span data-ttu-id="c0ab3-116">-Force</span><span class="sxs-lookup"><span data-stu-id="c0ab3-116">-Force</span></span>
<span data-ttu-id="c0ab3-117">Bu cmdlet 'in bir veri fabrikası onaylamanızı istemeden kaldırmadığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c0ab3-117">Indicates that this cmdlet removes a data factory without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="c0ab3-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="c0ab3-118">-Name</span></span>
<span data-ttu-id="c0ab3-119">Kaldırılacak Veri Fabrikası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c0ab3-119">Specifies the name of the data factory to remove.</span></span>

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

### <span data-ttu-id="c0ab3-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0ab3-120">-ResourceGroupName</span></span>
<span data-ttu-id="c0ab3-121">Bir Azure Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c0ab3-121">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="c0ab3-122">Bu cmdlet, bu parametrenin belirttiği gruptan bir veri fabrikası kaldırır.</span><span class="sxs-lookup"><span data-stu-id="c0ab3-122">This cmdlet removes a data factory from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="c0ab3-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="c0ab3-123">-Confirm</span></span>
<span data-ttu-id="c0ab3-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="c0ab3-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c0ab3-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c0ab3-125">-WhatIf</span></span>
<span data-ttu-id="c0ab3-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c0ab3-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c0ab3-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="c0ab3-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c0ab3-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0ab3-128">-DefaultProfile</span></span>
<span data-ttu-id="c0ab3-129">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c0ab3-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c0ab3-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0ab3-130">CommonParameters</span></span>
<span data-ttu-id="c0ab3-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c0ab3-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0ab3-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c0ab3-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0ab3-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c0ab3-133">INPUTS</span></span>

## <span data-ttu-id="c0ab3-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c0ab3-134">OUTPUTS</span></span>

### <span data-ttu-id="c0ab3-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c0ab3-135">System.Boolean</span></span>

## <span data-ttu-id="c0ab3-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c0ab3-136">NOTES</span></span>
* <span data-ttu-id="c0ab3-137">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, veri, fabrikalar</span><span class="sxs-lookup"><span data-stu-id="c0ab3-137">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="c0ab3-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c0ab3-138">RELATED LINKS</span></span>

[<span data-ttu-id="c0ab3-139">Get-AzureRmDataFactory</span><span class="sxs-lookup"><span data-stu-id="c0ab3-139">Get-AzureRmDataFactory</span></span>](./Get-AzureRmDataFactory.md)

[<span data-ttu-id="c0ab3-140">Yeni-AzureRmDataFactory</span><span class="sxs-lookup"><span data-stu-id="c0ab3-140">New-AzureRmDataFactory</span></span>](./New-AzureRmDataFactory.md)


