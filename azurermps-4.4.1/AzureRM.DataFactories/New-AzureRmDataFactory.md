---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: 7B18FA1B-F616-4479-B2F0-620FC0E3E962
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/New-AzureRmDataFactory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/New-AzureRmDataFactory.md
ms.openlocfilehash: 13e9a8de97ee19e53c31a76516fef7c9fcfcaedd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93586913"
---
# <span data-ttu-id="32173-101">New-AzureRmDataFactory</span><span class="sxs-lookup"><span data-stu-id="32173-101">New-AzureRmDataFactory</span></span>

## <span data-ttu-id="32173-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="32173-102">SYNOPSIS</span></span>
<span data-ttu-id="32173-103">Veri fabrikası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="32173-103">Creates a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="32173-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="32173-104">SYNTAX</span></span>

```
New-AzureRmDataFactory [-Name] <String> [-Location] <String> [[-Tags] <Hashtable>] [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="32173-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="32173-105">DESCRIPTION</span></span>
<span data-ttu-id="32173-106">**Yeni-AzureRmDataFactory** cmdlet 'i, belirtilen kaynak grubu adı ve konumuyla bir veri fabrikası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="32173-106">The **New-AzureRmDataFactory** cmdlet creates a data factory with the specified resource group name and location.</span></span>

<span data-ttu-id="32173-107">Bu işlemleri aşağıdaki sırada gerçekleştirin:</span><span class="sxs-lookup"><span data-stu-id="32173-107">Perform these operations in the following order:</span></span> 

- <span data-ttu-id="32173-108">Veri Fabrikası oluşturma.</span><span class="sxs-lookup"><span data-stu-id="32173-108">Create a data factory.</span></span> 
- <span data-ttu-id="32173-109">Bağlantılı hizmetler oluşturma.</span><span class="sxs-lookup"><span data-stu-id="32173-109">Create linked services.</span></span> 
- <span data-ttu-id="32173-110">Veri kümeleri oluşturma.</span><span class="sxs-lookup"><span data-stu-id="32173-110">Create datasets.</span></span> 
- <span data-ttu-id="32173-111">Ardışık düzen oluşturma.</span><span class="sxs-lookup"><span data-stu-id="32173-111">Create a pipeline.</span></span>

## <span data-ttu-id="32173-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="32173-112">EXAMPLES</span></span>

### <span data-ttu-id="32173-113">Örnek 1: Veri Fabrikası oluşturma</span><span class="sxs-lookup"><span data-stu-id="32173-113">Example 1: Create a data factory</span></span>
```
PS C:\>New-AzureRmDataFactory -ResourceGroupName "ADF" -Name "WikiADF" -Location "WestUS"
DataFactoryName   : WikiADF
ResourceGroupName : ADF
Location          : WestUS
Tags              : {}
Properties        : Microsoft.WindowsAzure.Commands.Utilities.PSDataFactoryConfiguration
```

<span data-ttu-id="32173-114">Bu komut, WestUS konumunda ADF adlı kaynak grubunda WikiADF adlı bir veri fabrikası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="32173-114">This command creates a data factory named WikiADF in the resource group named ADF in the WestUS location.</span></span>

## <span data-ttu-id="32173-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="32173-115">PARAMETERS</span></span>

### <span data-ttu-id="32173-116">-Force</span><span class="sxs-lookup"><span data-stu-id="32173-116">-Force</span></span>
<span data-ttu-id="32173-117">Bu cmdlet 'in varolan bir veri fabrikası yerine sizden onay istemeden değiştirildiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="32173-117">Indicates that this cmdlet replaces an existing data factory without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="32173-118">-Konum</span><span class="sxs-lookup"><span data-stu-id="32173-118">-Location</span></span>
<span data-ttu-id="32173-119">WestUS veya EastUS gibi veri fabrikası konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="32173-119">Specifies the location for the data factory, such as WestUS or EastUS.</span></span>
<span data-ttu-id="32173-120">Şu anda yalnızca WestUS destekleniyor.</span><span class="sxs-lookup"><span data-stu-id="32173-120">Only WestUS is currently supported.</span></span>

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

### <span data-ttu-id="32173-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="32173-121">-Name</span></span>
<span data-ttu-id="32173-122">Oluşturulacak Veri Fabrikası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="32173-122">Specifies the name of the data factory to create.</span></span>

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

### <span data-ttu-id="32173-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="32173-123">-ResourceGroupName</span></span>
<span data-ttu-id="32173-124">Bir Azure Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="32173-124">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="32173-125">Bu cmdlet, bu parametrenin belirttiği gruba ait bir veri fabrikası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="32173-125">This cmdlet creates a data factory that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="32173-126">-Etiketler</span><span class="sxs-lookup"><span data-stu-id="32173-126">-Tags</span></span>
<span data-ttu-id="32173-127">Veri Fabrikası için Etiketler belirtir.</span><span class="sxs-lookup"><span data-stu-id="32173-127">Specifies tags for the data factory.</span></span>

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

### <span data-ttu-id="32173-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="32173-128">-Confirm</span></span>
<span data-ttu-id="32173-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="32173-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="32173-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="32173-130">-WhatIf</span></span>
<span data-ttu-id="32173-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="32173-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="32173-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="32173-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="32173-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32173-133">-DefaultProfile</span></span>
<span data-ttu-id="32173-134">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="32173-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="32173-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32173-135">CommonParameters</span></span>
<span data-ttu-id="32173-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="32173-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32173-137">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="32173-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32173-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="32173-138">INPUTS</span></span>

## <span data-ttu-id="32173-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="32173-139">OUTPUTS</span></span>

### <span data-ttu-id="32173-140">Microsoft.WindowsAzure.Commands.Utilities.PSDAtafabrikası</span><span class="sxs-lookup"><span data-stu-id="32173-140">Microsoft.WindowsAzure.Commands.Utilities.PSDataFactory</span></span>

## <span data-ttu-id="32173-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="32173-141">NOTES</span></span>
* <span data-ttu-id="32173-142">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, veri, fabrikalar</span><span class="sxs-lookup"><span data-stu-id="32173-142">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="32173-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="32173-143">RELATED LINKS</span></span>

[<span data-ttu-id="32173-144">Get-AzureRmDataFactory</span><span class="sxs-lookup"><span data-stu-id="32173-144">Get-AzureRmDataFactory</span></span>](./Get-AzureRmDataFactory.md)

[<span data-ttu-id="32173-145">Remove-AzureRmDataFactory</span><span class="sxs-lookup"><span data-stu-id="32173-145">Remove-AzureRmDataFactory</span></span>](./Remove-AzureRmDataFactory.md)


