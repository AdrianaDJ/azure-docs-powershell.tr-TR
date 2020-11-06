---
external help file: Microsoft.Azure.Commands.PowerBI.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.powerbiembedded/suspend-azurermpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Suspend-AzureRmPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Suspend-AzureRmPowerBIEmbeddedCapacity.md
ms.openlocfilehash: fd50133d4919c52f314ccb7e306a022712e552c9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93573394"
---
# <span data-ttu-id="d6f31-101">Suspend-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="d6f31-101">Suspend-AzureRmPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="d6f31-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d6f31-102">SYNOPSIS</span></span>
<span data-ttu-id="d6f31-103">PowerBI Embedded kapasitesi örneğini askıya alır.</span><span class="sxs-lookup"><span data-stu-id="d6f31-103">Suspends an instance of PowerBI Embedded Capacity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d6f31-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d6f31-104">SYNTAX</span></span>

```
Suspend-AzureRmPowerBIEmbeddedCapacity 
    [-Name] <String> 
    [[-ResourceGroupName] <String>] 
    [-PassThru] 
    [-WhatIf]
    [-Confirm] 
    [<CommonParameters>]
```

## <span data-ttu-id="d6f31-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="d6f31-105">DESCRIPTION</span></span>
<span data-ttu-id="d6f31-106">Suspend-AzureRmPowerBIEmbeddedCapacity cmdlet 'i PowerBI Embedded kapasitesi örneğini askıya alır</span><span class="sxs-lookup"><span data-stu-id="d6f31-106">The Suspend-AzureRmPowerBIEmbeddedCapacity cmdlet suspends an instance of PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="d6f31-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d6f31-107">EXAMPLES</span></span>

### <span data-ttu-id="d6f31-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="d6f31-108">Example 1</span></span>
```
PS C:\> Suspend-AzureRmPowerBIEmbeddedCapacity -Name "testcapacity" -ResourceGroupName "testRG" -PassThru
Type                   : Microsoft.PowerBIDedicated/capacities
Id                     : /subscriptions/78e47976-.../resourceGroups/testRG/providers/Microsoft.PowerBIDedicated/capacities/testcapacity
ResourceGroup          : testRG
Name                   : testcapacity
Location               : West Central US
State                  : Paused
Administrator          : {admin@microsoft.com}
Sku                    : A1
Tier                   : PBIE_Azure
Tag                    : {}
```

<span data-ttu-id="d6f31-109">Bu komut, resourcegroup test grubundaki testcapacity adındaki etkin kapasiteyi askıya alır</span><span class="sxs-lookup"><span data-stu-id="d6f31-109">This command will suspend an active capacity named testcapacity in the resourcegroup testgroup</span></span>

## <span data-ttu-id="d6f31-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d6f31-110">PARAMETERS</span></span>

### <span data-ttu-id="d6f31-111">-Ad</span><span class="sxs-lookup"><span data-stu-id="d6f31-111">-Name</span></span>
<span data-ttu-id="d6f31-112">PowerBI Embedded Capacity 'in adı</span><span class="sxs-lookup"><span data-stu-id="d6f31-112">Name of the PowerBI Embedded Capacity</span></span>

```yaml
Type: String
Parameter Sets: ByNameAndResourceGroup
Aliases: 

Required: True
Position: 0
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="d6f31-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6f31-113">-ResourceGroupName</span></span>
<span data-ttu-id="d6f31-114">Kapasitenin ait olduğu Azure Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="d6f31-114">Name of the Azure resource group to which the capacity belongs</span></span>

```yaml
Type: String
Parameter Sets: ByNameAndResourceGroup
Aliases: 

Required: False
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="d6f31-115">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="d6f31-115">-ResourceId</span></span>
<span data-ttu-id="d6f31-116">Azure Kaynak KIMLIĞI</span><span class="sxs-lookup"><span data-stu-id="d6f31-116">Azure resource ID</span></span>

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

### <span data-ttu-id="d6f31-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d6f31-117">-InputObject</span></span>
<span data-ttu-id="d6f31-118">Boru için giriş nesnesi</span><span class="sxs-lookup"><span data-stu-id="d6f31-118">Input object for Piping</span></span>

```yaml
Type: PSPowerBIEmbeddedCapacity
Parameter Sets: ByInputObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d6f31-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="d6f31-119">-Confirm</span></span>
<span data-ttu-id="d6f31-120">Kullanıcıya işlemi gerçekleştirmeyi onaylamanızı ister</span><span class="sxs-lookup"><span data-stu-id="d6f31-120">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="d6f31-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d6f31-121">-WhatIf</span></span>
<span data-ttu-id="d6f31-122">Geçerli işlemin gerçekte gerçekleştirmesi gerekmeden gerçekleştireceği işlemleri açıklar</span><span class="sxs-lookup"><span data-stu-id="d6f31-122">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="d6f31-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6f31-123">CommonParameters</span></span>
<span data-ttu-id="d6f31-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d6f31-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6f31-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d6f31-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6f31-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d6f31-126">INPUTS</span></span>

### <span data-ttu-id="d6f31-127">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="d6f31-127">None</span></span>
<span data-ttu-id="d6f31-128">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="d6f31-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d6f31-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d6f31-129">OUTPUTS</span></span>

### <span data-ttu-id="d6f31-130">Microsoft. Azure. Commands. PowerBI. modeller. PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="d6f31-130">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="d6f31-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d6f31-131">NOTES</span></span>

## <span data-ttu-id="d6f31-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d6f31-132">RELATED LINKS</span></span>

[<span data-ttu-id="d6f31-133">Get-Azurermpowerbibidedcapacity</span><span class="sxs-lookup"><span data-stu-id="d6f31-133">Get-AzureRmPowerBIEmbeddedCapacity</span></span>](./Get-AzureRmPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="d6f31-134">Özgeçmiş-Azurermpowerbibidedcapacity</span><span class="sxs-lookup"><span data-stu-id="d6f31-134">Resume-AzureRmPowerBIEmbeddedCapacity</span></span>](./Resume-AzureRmPowerBIEmbeddedCapacity.md)

