---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: 3D2E9FAE-FE34-457A-BE95-BC61D025B07A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/remove-azurermdatafactory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Remove-AzureRmDataFactory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Remove-AzureRmDataFactory.md
ms.openlocfilehash: 212e0c2ee4863c6d18873a717ff25f6940c34a15
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588961"
---
# <span data-ttu-id="ade54-101">Remove-AzureRmDataFactory</span><span class="sxs-lookup"><span data-stu-id="ade54-101">Remove-AzureRmDataFactory</span></span>

## <span data-ttu-id="ade54-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ade54-102">SYNOPSIS</span></span>
<span data-ttu-id="ade54-103">Veri Fabrikası kaldırır.</span><span class="sxs-lookup"><span data-stu-id="ade54-103">Removes a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ade54-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ade54-104">SYNTAX</span></span>

### <span data-ttu-id="ade54-105">ByFactoryName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="ade54-105">ByFactoryName (Default)</span></span>
```
Remove-AzureRmDataFactory [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ade54-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="ade54-106">ByFactoryObject</span></span>
```
Remove-AzureRmDataFactory [-DataFactory] <PSDataFactory> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ade54-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="ade54-107">DESCRIPTION</span></span>
<span data-ttu-id="ade54-108">**Remove-AzureRmDataFactory** cmdlet 'i Veri Fabrikası çıkarır.</span><span class="sxs-lookup"><span data-stu-id="ade54-108">The **Remove-AzureRmDataFactory** cmdlet removes a data factory.</span></span>

## <span data-ttu-id="ade54-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ade54-109">EXAMPLES</span></span>

### <span data-ttu-id="ade54-110">Örnek 1: Veri Fabrikası kaldırma</span><span class="sxs-lookup"><span data-stu-id="ade54-110">Example 1: Remove a data factory</span></span>
```
PS C:\>Remove-AzureRmDataFactory -Name "WikiADF" -ResourceGroupName "ADF"
Confirm
Are you sure you want to remove data factory 'WikiADF' in resource group 'ADF'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
True
```

<span data-ttu-id="ade54-111">Bu komut, Obkiadf adındaki</span><span class="sxs-lookup"><span data-stu-id="ade54-111">This command removes the data factory named WikiADF from the resource group named ADF.</span></span>
<span data-ttu-id="ade54-112">Bu komut $True değerini döndürür.</span><span class="sxs-lookup"><span data-stu-id="ade54-112">This command returns a value of $True.</span></span>

## <span data-ttu-id="ade54-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ade54-113">PARAMETERS</span></span>

### <span data-ttu-id="ade54-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="ade54-114">-DataFactory</span></span>
<span data-ttu-id="ade54-115">Kaldırılacak **Psdatafactory** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ade54-115">Specifies the **PSDataFactory** object to remove.</span></span>

```yaml
Type: PSDataFactory
Parameter Sets: ByFactoryObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ade54-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ade54-116">-DefaultProfile</span></span>
<span data-ttu-id="ade54-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="ade54-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ade54-118">-Force</span><span class="sxs-lookup"><span data-stu-id="ade54-118">-Force</span></span>
<span data-ttu-id="ade54-119">Bu cmdlet 'in bir veri fabrikası onaylamanızı istemeden kaldırmadığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ade54-119">Indicates that this cmdlet removes a data factory without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="ade54-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="ade54-120">-Name</span></span>
<span data-ttu-id="ade54-121">Kaldırılacak Veri Fabrikası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ade54-121">Specifies the name of the data factory to remove.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: DataFactoryName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ade54-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ade54-122">-ResourceGroupName</span></span>
<span data-ttu-id="ade54-123">Bir Azure Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ade54-123">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="ade54-124">Bu cmdlet, bu parametrenin belirttiği gruptan bir veri fabrikası kaldırır.</span><span class="sxs-lookup"><span data-stu-id="ade54-124">This cmdlet removes a data factory from the group that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ade54-125">-Onay</span><span class="sxs-lookup"><span data-stu-id="ade54-125">-Confirm</span></span>
<span data-ttu-id="ade54-126">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ade54-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ade54-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ade54-127">-WhatIf</span></span>
<span data-ttu-id="ade54-128">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ade54-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ade54-129">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ade54-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ade54-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ade54-130">CommonParameters</span></span>
<span data-ttu-id="ade54-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ade54-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ade54-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ade54-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ade54-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ade54-133">INPUTS</span></span>

### <span data-ttu-id="ade54-134">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="ade54-134">None</span></span>
<span data-ttu-id="ade54-135">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="ade54-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ade54-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ade54-136">OUTPUTS</span></span>

### <span data-ttu-id="ade54-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ade54-137">System.Boolean</span></span>

## <span data-ttu-id="ade54-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ade54-138">NOTES</span></span>
* <span data-ttu-id="ade54-139">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, veri, fabrikalar</span><span class="sxs-lookup"><span data-stu-id="ade54-139">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="ade54-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ade54-140">RELATED LINKS</span></span>

[<span data-ttu-id="ade54-141">Get-AzureRmDataFactory</span><span class="sxs-lookup"><span data-stu-id="ade54-141">Get-AzureRmDataFactory</span></span>](./Get-AzureRmDataFactory.md)

[<span data-ttu-id="ade54-142">Yeni-AzureRmDataFactory</span><span class="sxs-lookup"><span data-stu-id="ade54-142">New-AzureRmDataFactory</span></span>](./New-AzureRmDataFactory.md)


