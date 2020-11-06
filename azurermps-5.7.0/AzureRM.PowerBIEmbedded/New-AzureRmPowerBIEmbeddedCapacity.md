---
external help file: Microsoft.Azure.Commands.PowerBI.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.powerbiembedded/new-azurermpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/New-AzureRmPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/New-AzureRmPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 6badeec8b2425a5ca8e10dc88039a1d28e055cc4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588120"
---
# <span data-ttu-id="7ec67-101">New-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="7ec67-101">New-AzureRmPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="7ec67-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7ec67-102">SYNOPSIS</span></span>
<span data-ttu-id="7ec67-103">Yeni bir PowerBI Embedded kapasitesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7ec67-103">Creates a new PowerBI Embedded Capacity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7ec67-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7ec67-104">SYNTAX</span></span>

```
New-AzureRmPowerBIEmbeddedCapacity 
    [-ResourceGroupName] <String> 
    [-Name] <String> 
    [-Location] <String>
    [-Sku] <String> 
    [-Administrator] <String>
    [[-Tag] <Hashtable>] 
    [-WhatIf] 
    [-Confirm] 
    [<CommonParameters>]
```

## <span data-ttu-id="7ec67-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="7ec67-105">DESCRIPTION</span></span>
<span data-ttu-id="7ec67-106">New-AzureRmPowerBIEmbeddedCapacity cmdlet 'i yeni bir PowerBI Embedded kapasitesi oluşturur</span><span class="sxs-lookup"><span data-stu-id="7ec67-106">The New-AzureRmPowerBIEmbeddedCapacity cmdlet creates a new PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="7ec67-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7ec67-107">EXAMPLES</span></span>

### <span data-ttu-id="7ec67-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="7ec67-108">Example 1</span></span>
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

<span data-ttu-id="7ec67-109">ABD merkezi merkezi 'nde ve kaynak grubu testRG 'de testcapacity adlı bir kapasite oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7ec67-109">Creates a capacity named testcapacity in the Azure region West Central US and in resource group testRG.</span></span> <span data-ttu-id="7ec67-110">Kapasite için SKU düzeyi a1 olur.</span><span class="sxs-lookup"><span data-stu-id="7ec67-110">The sku level for the capacity will be A1.</span></span>

## <span data-ttu-id="7ec67-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7ec67-111">PARAMETERS</span></span>

### <span data-ttu-id="7ec67-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7ec67-112">-ResourceGroupName</span></span>
<span data-ttu-id="7ec67-113">Kapasitenin ait olduğu Azure Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="7ec67-113">Name of the Azure resource group to which the capacity belongs</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="7ec67-114">-Ad</span><span class="sxs-lookup"><span data-stu-id="7ec67-114">-Name</span></span>
<span data-ttu-id="7ec67-115">PowerBI Embedded Capacity 'in adı</span><span class="sxs-lookup"><span data-stu-id="7ec67-115">Name of the PowerBI Embedded Capacity</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="7ec67-116">-Konum</span><span class="sxs-lookup"><span data-stu-id="7ec67-116">-Location</span></span>
<span data-ttu-id="7ec67-117">PowerBI Embedded kapasitesinin barındırıldığı Azure bölgesi</span><span class="sxs-lookup"><span data-stu-id="7ec67-117">The Azure region where the PowerBI Embedded Capacity is hosted</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="7ec67-118">-SKU</span><span class="sxs-lookup"><span data-stu-id="7ec67-118">-Sku</span></span>
<span data-ttu-id="7ec67-119">Kapasite SKU 'nun adı.</span><span class="sxs-lookup"><span data-stu-id="7ec67-119">The name of the Sku for the capacity.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: A1, A2, A3, A4, A5, A6

Required: True
Position: 3
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="7ec67-120">-Yönetici</span><span class="sxs-lookup"><span data-stu-id="7ec67-120">-Administrator</span></span>
<span data-ttu-id="7ec67-121">Kapasitede yönetici olarak ayarlanacak, virgülle ayrılmış kapasite adları</span><span class="sxs-lookup"><span data-stu-id="7ec67-121">A comma separated capacity names to set as administrator on the capacity</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="7ec67-122">Etiketli</span><span class="sxs-lookup"><span data-stu-id="7ec67-122">-Tag</span></span>
<span data-ttu-id="7ec67-123">Kapasitede etiket olarak ayarlanan karma tablo biçimindeki anahtar değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="7ec67-123">Key-value pairs in the form of a hash table set as tags on the capacity.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="7ec67-124">-Onay</span><span class="sxs-lookup"><span data-stu-id="7ec67-124">-Confirm</span></span>
<span data-ttu-id="7ec67-125">Kullanıcıya işlemi gerçekleştirmeyi onaylamanızı ister</span><span class="sxs-lookup"><span data-stu-id="7ec67-125">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="7ec67-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7ec67-126">-WhatIf</span></span>
<span data-ttu-id="7ec67-127">Geçerli işlemin gerçekte gerçekleştirmesi gerekmeden gerçekleştireceği işlemleri açıklar</span><span class="sxs-lookup"><span data-stu-id="7ec67-127">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="7ec67-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ec67-128">CommonParameters</span></span>
<span data-ttu-id="7ec67-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7ec67-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ec67-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7ec67-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ec67-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7ec67-131">INPUTS</span></span>

### <span data-ttu-id="7ec67-132">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="7ec67-132">None</span></span>
<span data-ttu-id="7ec67-133">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="7ec67-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="7ec67-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7ec67-134">OUTPUTS</span></span>

### <span data-ttu-id="7ec67-135">Microsoft. Azure. Commands. PowerBI. modeller. PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="7ec67-135">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="7ec67-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7ec67-136">NOTES</span></span>

## <span data-ttu-id="7ec67-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7ec67-137">RELATED LINKS</span></span>

[<span data-ttu-id="7ec67-138">Get-Azurermpowerbibidedcapacity</span><span class="sxs-lookup"><span data-stu-id="7ec67-138">Get-AzureRmPowerBIEmbeddedCapacity</span></span>](./Get-AzureRmPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="7ec67-139">Remove-Azurermpowerbibidedcapacity</span><span class="sxs-lookup"><span data-stu-id="7ec67-139">Remove-AzureRmPowerBIEmbeddedCapacity</span></span>](./Remove-AzureRmPowerBIEmbeddedCapacity.md)
