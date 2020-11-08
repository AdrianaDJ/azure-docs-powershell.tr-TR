---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 7B18FA1B-F616-4479-B2F0-620FC0E3E962
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/new-azdatafactory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/New-AzDataFactory.md
ms.openlocfilehash: 450a833656f6508f70ebd97f5387075c1711c5f9
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93938342"
---
# <span data-ttu-id="033c7-101">New-AzDataFactory</span><span class="sxs-lookup"><span data-stu-id="033c7-101">New-AzDataFactory</span></span>

## <span data-ttu-id="033c7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="033c7-102">SYNOPSIS</span></span>
<span data-ttu-id="033c7-103">Veri fabrikası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="033c7-103">Creates a data factory.</span></span>

## <span data-ttu-id="033c7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="033c7-104">SYNTAX</span></span>

```
New-AzDataFactory [-Name] <String> [-Location] <String> [[-Tag] <Hashtable>] [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="033c7-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="033c7-105">DESCRIPTION</span></span>
<span data-ttu-id="033c7-106">**New-AzDataFactory** cmdlet 'i, belirtilen kaynak grubu adı ve konumuyla bir veri fabrikası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="033c7-106">The **New-AzDataFactory** cmdlet creates a data factory with the specified resource group name and location.</span></span>
<span data-ttu-id="033c7-107">Bu işlemleri aşağıdaki sırada gerçekleştirin:</span><span class="sxs-lookup"><span data-stu-id="033c7-107">Perform these operations in the following order:</span></span> 
- <span data-ttu-id="033c7-108">Veri Fabrikası oluşturma.</span><span class="sxs-lookup"><span data-stu-id="033c7-108">Create a data factory.</span></span> 
- <span data-ttu-id="033c7-109">Bağlantılı hizmetler oluşturma.</span><span class="sxs-lookup"><span data-stu-id="033c7-109">Create linked services.</span></span> 
- <span data-ttu-id="033c7-110">Veri kümeleri oluşturma.</span><span class="sxs-lookup"><span data-stu-id="033c7-110">Create datasets.</span></span> 
- <span data-ttu-id="033c7-111">Ardışık düzen oluşturma.</span><span class="sxs-lookup"><span data-stu-id="033c7-111">Create a pipeline.</span></span>

## <span data-ttu-id="033c7-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="033c7-112">EXAMPLES</span></span>

### <span data-ttu-id="033c7-113">Örnek 1: Veri Fabrikası oluşturma</span><span class="sxs-lookup"><span data-stu-id="033c7-113">Example 1: Create a data factory</span></span>
```
PS C:\>New-AzDataFactory -ResourceGroupName "ADF" -Name "WikiADF" -Location "WestUS"
DataFactoryName   : WikiADF
ResourceGroupName : ADF
Location          : WestUS
Tags              : {}
Properties        : Microsoft.WindowsAzure.Commands.Utilities.PSDataFactoryConfiguration
```

<span data-ttu-id="033c7-114">Bu komut, WestUS konumunda ADF adlı kaynak grubunda WikiADF adlı bir veri fabrikası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="033c7-114">This command creates a data factory named WikiADF in the resource group named ADF in the WestUS location.</span></span>

## <span data-ttu-id="033c7-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="033c7-115">PARAMETERS</span></span>

### <span data-ttu-id="033c7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="033c7-116">-DefaultProfile</span></span>
<span data-ttu-id="033c7-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="033c7-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="033c7-118">-Force</span><span class="sxs-lookup"><span data-stu-id="033c7-118">-Force</span></span>
<span data-ttu-id="033c7-119">Bu cmdlet 'in varolan bir veri fabrikası yerine sizden onay istemeden değiştirildiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="033c7-119">Indicates that this cmdlet replaces an existing data factory without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="033c7-120">-Konum</span><span class="sxs-lookup"><span data-stu-id="033c7-120">-Location</span></span>
<span data-ttu-id="033c7-121">WestUS veya EastUS gibi veri fabrikası konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="033c7-121">Specifies the location for the data factory, such as WestUS or EastUS.</span></span>
<span data-ttu-id="033c7-122">Şu anda yalnızca WestUS destekleniyor.</span><span class="sxs-lookup"><span data-stu-id="033c7-122">Only WestUS is currently supported.</span></span>

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

### <span data-ttu-id="033c7-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="033c7-123">-Name</span></span>
<span data-ttu-id="033c7-124">Oluşturulacak Veri Fabrikası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="033c7-124">Specifies the name of the data factory to create.</span></span>

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

### <span data-ttu-id="033c7-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="033c7-125">-ResourceGroupName</span></span>
<span data-ttu-id="033c7-126">Bir Azure Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="033c7-126">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="033c7-127">Bu cmdlet, bu parametrenin belirttiği gruba ait bir veri fabrikası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="033c7-127">This cmdlet creates a data factory that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="033c7-128">Etiketli</span><span class="sxs-lookup"><span data-stu-id="033c7-128">-Tag</span></span>
<span data-ttu-id="033c7-129">Veri Fabrikası 'nin etiketleri.</span><span class="sxs-lookup"><span data-stu-id="033c7-129">The tags of the data factory.</span></span>

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

### <span data-ttu-id="033c7-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="033c7-130">-Confirm</span></span>
<span data-ttu-id="033c7-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="033c7-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="033c7-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="033c7-132">-WhatIf</span></span>
<span data-ttu-id="033c7-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="033c7-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="033c7-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="033c7-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="033c7-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="033c7-135">CommonParameters</span></span>
<span data-ttu-id="033c7-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="033c7-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="033c7-137">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="033c7-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="033c7-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="033c7-138">INPUTS</span></span>

### <span data-ttu-id="033c7-139">System. String</span><span class="sxs-lookup"><span data-stu-id="033c7-139">System.String</span></span>

### <span data-ttu-id="033c7-140">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="033c7-140">System.Collections.Hashtable</span></span>

## <span data-ttu-id="033c7-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="033c7-141">OUTPUTS</span></span>

### <span data-ttu-id="033c7-142">Microsoft.Azure.Commands.DataFactories.Models.PSDAtafabrikası</span><span class="sxs-lookup"><span data-stu-id="033c7-142">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="033c7-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="033c7-143">NOTES</span></span>
* <span data-ttu-id="033c7-144">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, veri, fabrikalar</span><span class="sxs-lookup"><span data-stu-id="033c7-144">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="033c7-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="033c7-145">RELATED LINKS</span></span>

[<span data-ttu-id="033c7-146">Get-AzDataFactory</span><span class="sxs-lookup"><span data-stu-id="033c7-146">Get-AzDataFactory</span></span>](./Get-AzDataFactory.md)

[<span data-ttu-id="033c7-147">Remove-AzDataFactory</span><span class="sxs-lookup"><span data-stu-id="033c7-147">Remove-AzDataFactory</span></span>](./Remove-AzDataFactory.md)

