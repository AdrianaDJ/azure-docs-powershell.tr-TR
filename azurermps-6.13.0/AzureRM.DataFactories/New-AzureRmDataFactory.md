---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: 7B18FA1B-F616-4479-B2F0-620FC0E3E962
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/new-azurermdatafactory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/New-AzureRmDataFactory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/New-AzureRmDataFactory.md
ms.openlocfilehash: 1636dd6b101a7639c84b0cd7c2659eac23a10b11
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593701"
---
# <span data-ttu-id="c6499-101">New-AzureRmDataFactory</span><span class="sxs-lookup"><span data-stu-id="c6499-101">New-AzureRmDataFactory</span></span>

## <span data-ttu-id="c6499-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c6499-102">SYNOPSIS</span></span>
<span data-ttu-id="c6499-103">Veri fabrikası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c6499-103">Creates a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c6499-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c6499-104">SYNTAX</span></span>

```
New-AzureRmDataFactory [-Name] <String> [-Location] <String> [[-Tag] <Hashtable>] [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c6499-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="c6499-105">DESCRIPTION</span></span>
<span data-ttu-id="c6499-106">**Yeni-AzureRmDataFactory** cmdlet 'i, belirtilen kaynak grubu adı ve konumuyla bir veri fabrikası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c6499-106">The **New-AzureRmDataFactory** cmdlet creates a data factory with the specified resource group name and location.</span></span>
<span data-ttu-id="c6499-107">Bu işlemleri aşağıdaki sırada gerçekleştirin:</span><span class="sxs-lookup"><span data-stu-id="c6499-107">Perform these operations in the following order:</span></span> 
- <span data-ttu-id="c6499-108">Veri Fabrikası oluşturma.</span><span class="sxs-lookup"><span data-stu-id="c6499-108">Create a data factory.</span></span> 
- <span data-ttu-id="c6499-109">Bağlantılı hizmetler oluşturma.</span><span class="sxs-lookup"><span data-stu-id="c6499-109">Create linked services.</span></span> 
- <span data-ttu-id="c6499-110">Veri kümeleri oluşturma.</span><span class="sxs-lookup"><span data-stu-id="c6499-110">Create datasets.</span></span> 
- <span data-ttu-id="c6499-111">Ardışık düzen oluşturma.</span><span class="sxs-lookup"><span data-stu-id="c6499-111">Create a pipeline.</span></span>

## <span data-ttu-id="c6499-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c6499-112">EXAMPLES</span></span>

### <span data-ttu-id="c6499-113">Örnek 1: Veri Fabrikası oluşturma</span><span class="sxs-lookup"><span data-stu-id="c6499-113">Example 1: Create a data factory</span></span>
```
PS C:\>New-AzureRmDataFactory -ResourceGroupName "ADF" -Name "WikiADF" -Location "WestUS"
DataFactoryName   : WikiADF
ResourceGroupName : ADF
Location          : WestUS
Tags              : {}
Properties        : Microsoft.WindowsAzure.Commands.Utilities.PSDataFactoryConfiguration
```

<span data-ttu-id="c6499-114">Bu komut, WestUS konumunda ADF adlı kaynak grubunda WikiADF adlı bir veri fabrikası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c6499-114">This command creates a data factory named WikiADF in the resource group named ADF in the WestUS location.</span></span>

## <span data-ttu-id="c6499-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c6499-115">PARAMETERS</span></span>

### <span data-ttu-id="c6499-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6499-116">-DefaultProfile</span></span>
<span data-ttu-id="c6499-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="c6499-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c6499-118">-Force</span><span class="sxs-lookup"><span data-stu-id="c6499-118">-Force</span></span>
<span data-ttu-id="c6499-119">Bu cmdlet 'in varolan bir veri fabrikası yerine sizden onay istemeden değiştirildiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="c6499-119">Indicates that this cmdlet replaces an existing data factory without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="c6499-120">-Konum</span><span class="sxs-lookup"><span data-stu-id="c6499-120">-Location</span></span>
<span data-ttu-id="c6499-121">WestUS veya EastUS gibi veri fabrikası konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="c6499-121">Specifies the location for the data factory, such as WestUS or EastUS.</span></span>
<span data-ttu-id="c6499-122">Şu anda yalnızca WestUS destekleniyor.</span><span class="sxs-lookup"><span data-stu-id="c6499-122">Only WestUS is currently supported.</span></span>

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

### <span data-ttu-id="c6499-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="c6499-123">-Name</span></span>
<span data-ttu-id="c6499-124">Oluşturulacak Veri Fabrikası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c6499-124">Specifies the name of the data factory to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6499-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c6499-125">-ResourceGroupName</span></span>
<span data-ttu-id="c6499-126">Bir Azure Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c6499-126">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="c6499-127">Bu cmdlet, bu parametrenin belirttiği gruba ait bir veri fabrikası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c6499-127">This cmdlet creates a data factory that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="c6499-128">Etiketli</span><span class="sxs-lookup"><span data-stu-id="c6499-128">-Tag</span></span>
<span data-ttu-id="c6499-129">Veri Fabrikası 'nin etiketleri.</span><span class="sxs-lookup"><span data-stu-id="c6499-129">The tags of the data factory.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6499-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="c6499-130">-Confirm</span></span>
<span data-ttu-id="c6499-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="c6499-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c6499-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c6499-132">-WhatIf</span></span>
<span data-ttu-id="c6499-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c6499-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c6499-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="c6499-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c6499-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6499-135">CommonParameters</span></span>
<span data-ttu-id="c6499-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c6499-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6499-137">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c6499-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6499-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c6499-138">INPUTS</span></span>

### <span data-ttu-id="c6499-139">System. String</span><span class="sxs-lookup"><span data-stu-id="c6499-139">System.String</span></span>

### <span data-ttu-id="c6499-140">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="c6499-140">System.Collections.Hashtable</span></span>

## <span data-ttu-id="c6499-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c6499-141">OUTPUTS</span></span>

### <span data-ttu-id="c6499-142">Microsoft.Azure.Commands.DataFactories.Models.PSDAtafabrikası</span><span class="sxs-lookup"><span data-stu-id="c6499-142">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="c6499-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c6499-143">NOTES</span></span>
* <span data-ttu-id="c6499-144">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, veri, fabrikalar</span><span class="sxs-lookup"><span data-stu-id="c6499-144">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="c6499-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c6499-145">RELATED LINKS</span></span>

[<span data-ttu-id="c6499-146">Get-AzureRmDataFactory</span><span class="sxs-lookup"><span data-stu-id="c6499-146">Get-AzureRmDataFactory</span></span>](./Get-AzureRmDataFactory.md)

[<span data-ttu-id="c6499-147">Remove-AzureRmDataFactory</span><span class="sxs-lookup"><span data-stu-id="c6499-147">Remove-AzureRmDataFactory</span></span>](./Remove-AzureRmDataFactory.md)


