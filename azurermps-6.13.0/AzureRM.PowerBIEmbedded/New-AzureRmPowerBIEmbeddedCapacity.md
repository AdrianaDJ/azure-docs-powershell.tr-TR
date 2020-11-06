---
external help file: Microsoft.Azure.Commands.PowerBI.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.powerbiembedded/new-azurermpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/New-AzureRmPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/New-AzureRmPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 8546dbfbe8da12cd61c8b03d8aca64772d032b60
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590099"
---
# <span data-ttu-id="dea71-101">New-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="dea71-101">New-AzureRmPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="dea71-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dea71-102">SYNOPSIS</span></span>
<span data-ttu-id="dea71-103">Yeni bir PowerBI Embedded kapasitesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="dea71-103">Creates a new PowerBI Embedded Capacity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dea71-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="dea71-104">SYNTAX</span></span>

```
New-AzureRmPowerBIEmbeddedCapacity [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [-Sku] <String> [-Administrator] <String[]> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dea71-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="dea71-105">DESCRIPTION</span></span>
<span data-ttu-id="dea71-106">New-AzureRmPowerBIEmbeddedCapacity cmdlet 'i yeni bir PowerBI Embedded kapasitesi oluşturur</span><span class="sxs-lookup"><span data-stu-id="dea71-106">The New-AzureRmPowerBIEmbeddedCapacity cmdlet creates a new PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="dea71-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="dea71-107">EXAMPLES</span></span>

### <span data-ttu-id="dea71-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="dea71-108">Example 1</span></span>
```
PS C:\> New-AzureRmPowerBIEmbeddedCapacity -ResourceGroupName "testRG" -Name "testcapacity" -Location "West Central US" -Sku "A1" -Administrator admin@microsoft.com
Type                   : Microsoft.PowerBIDedicated/capacities
Id                     : /subscriptions/78e47976-.../resourceGroups/testRG/providers/Microsoft.PowerBIDedicated/capacities/testcapacity
ResourceGroup          : testRG
Name                   : testcapacity
Location               : West Central US
State                  : Succeeded
Administrator          : {admin@microsoft.com}
Sku                    : A1
Tier                   : PBIE_Azure
Tag                    : {}
```

<span data-ttu-id="dea71-109">ABD merkezi merkezi 'nde ve kaynak grubu testRG 'de testcapacity adlı bir kapasite oluşturur.</span><span class="sxs-lookup"><span data-stu-id="dea71-109">Creates a capacity named testcapacity in the Azure region West Central US and in resource group testRG.</span></span> <span data-ttu-id="dea71-110">Kapasite için SKU düzeyi a1 olur.</span><span class="sxs-lookup"><span data-stu-id="dea71-110">The sku level for the capacity will be A1.</span></span>

## <span data-ttu-id="dea71-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="dea71-111">PARAMETERS</span></span>

### <span data-ttu-id="dea71-112">-Yönetici</span><span class="sxs-lookup"><span data-stu-id="dea71-112">-Administrator</span></span>
<span data-ttu-id="dea71-113">Kapasitede yönetici olarak ayarlanacak, virgülle ayrılmış kapasite adları</span><span class="sxs-lookup"><span data-stu-id="dea71-113">A comma separated capacity names to set as administrator on the capacity</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dea71-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dea71-114">-DefaultProfile</span></span>
<span data-ttu-id="dea71-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="dea71-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dea71-116">-Konum</span><span class="sxs-lookup"><span data-stu-id="dea71-116">-Location</span></span>
<span data-ttu-id="dea71-117">PowerBI Embedded kapasitesinin barındırıldığı Azure bölgesi</span><span class="sxs-lookup"><span data-stu-id="dea71-117">The Azure region where the PowerBI Embedded Capacity is hosted</span></span>

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

### <span data-ttu-id="dea71-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="dea71-118">-Name</span></span>
<span data-ttu-id="dea71-119">PowerBI Embedded Capacity 'in adı</span><span class="sxs-lookup"><span data-stu-id="dea71-119">Name of the PowerBI Embedded Capacity</span></span>

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

### <span data-ttu-id="dea71-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dea71-120">-ResourceGroupName</span></span>
<span data-ttu-id="dea71-121">Kapasitenin ait olduğu Azure Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="dea71-121">Name of the Azure resource group to which the capacity belongs</span></span>

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

### <span data-ttu-id="dea71-122">-SKU</span><span class="sxs-lookup"><span data-stu-id="dea71-122">-Sku</span></span>
<span data-ttu-id="dea71-123">Kapasite SKU 'nun adı.</span><span class="sxs-lookup"><span data-stu-id="dea71-123">The name of the Sku for the capacity.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: A1, A2, A3, A4, A5, A6

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dea71-124">Etiketli</span><span class="sxs-lookup"><span data-stu-id="dea71-124">-Tag</span></span>
<span data-ttu-id="dea71-125">Kapasitede etiket olarak ayarlanan karma tablo biçimindeki anahtar değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="dea71-125">Key-value pairs in the form of a hash table set as tags on the capacity.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dea71-126">-Onay</span><span class="sxs-lookup"><span data-stu-id="dea71-126">-Confirm</span></span>
<span data-ttu-id="dea71-127">Kullanıcıya işlemi gerçekleştirmeyi onaylamanızı ister</span><span class="sxs-lookup"><span data-stu-id="dea71-127">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="dea71-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dea71-128">-WhatIf</span></span>
<span data-ttu-id="dea71-129">Geçerli işlemin gerçekte gerçekleştirmesi gerekmeden gerçekleştireceği işlemleri açıklar</span><span class="sxs-lookup"><span data-stu-id="dea71-129">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="dea71-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dea71-130">CommonParameters</span></span>
<span data-ttu-id="dea71-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="dea71-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dea71-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dea71-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dea71-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="dea71-133">INPUTS</span></span>

### <span data-ttu-id="dea71-134">System. String</span><span class="sxs-lookup"><span data-stu-id="dea71-134">System.String</span></span>

### <span data-ttu-id="dea71-135">System. String []</span><span class="sxs-lookup"><span data-stu-id="dea71-135">System.String[]</span></span>

### <span data-ttu-id="dea71-136">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="dea71-136">System.Collections.Hashtable</span></span>

## <span data-ttu-id="dea71-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="dea71-137">OUTPUTS</span></span>

### <span data-ttu-id="dea71-138">Microsoft. Azure. Commands. PowerBI. modeller. PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="dea71-138">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="dea71-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="dea71-139">NOTES</span></span>

## <span data-ttu-id="dea71-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="dea71-140">RELATED LINKS</span></span>

[<span data-ttu-id="dea71-141">Get-Azurermpowerbibidedcapacity</span><span class="sxs-lookup"><span data-stu-id="dea71-141">Get-AzureRmPowerBIEmbeddedCapacity</span></span>](./Get-AzureRmPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="dea71-142">Remove-Azurermpowerbibidedcapacity</span><span class="sxs-lookup"><span data-stu-id="dea71-142">Remove-AzureRmPowerBIEmbeddedCapacity</span></span>](./Remove-AzureRmPowerBIEmbeddedCapacity.md)
