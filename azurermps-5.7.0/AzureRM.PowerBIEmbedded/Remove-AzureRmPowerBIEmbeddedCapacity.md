---
external help file: Microsoft.Azure.Commands.PowerBI.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.powerbiembedded/remove-azurermpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Remove-AzureRmPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Remove-AzureRmPowerBIEmbeddedCapacity.md
ms.openlocfilehash: bbdfe43b4f6cad72432c85876c71bcd34a9a371c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763254"
---
# <span data-ttu-id="3eb84-101">Remove-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="3eb84-101">Remove-AzureRmPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="3eb84-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3eb84-102">SYNOPSIS</span></span>
<span data-ttu-id="3eb84-103">PowerBI Embedded kapasitesi örneğini siler.</span><span class="sxs-lookup"><span data-stu-id="3eb84-103">Deletes an instance of PowerBI Embedded Capacity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3eb84-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3eb84-104">SYNTAX</span></span>

```
Remove-AzureRmPowerBIEmbeddedCapacity 
    [-Name] <String> 
    [[-ResourceGroupName] <String>] 
    [-PassThru] 
    [-WhatIf]
    [-Confirm] 
    [<CommonParameters>]
```

## <span data-ttu-id="3eb84-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="3eb84-105">DESCRIPTION</span></span>
<span data-ttu-id="3eb84-106">Remove-AzureRmPowerBIEmbeddedCapacity cmdlet 'i, PowerBI eklenmiş kapasitenin bir örneğini siler</span><span class="sxs-lookup"><span data-stu-id="3eb84-106">The Remove-AzureRmPowerBIEmbeddedCapacity cmdlet deletes an instance of PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="3eb84-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3eb84-107">EXAMPLES</span></span>

### <span data-ttu-id="3eb84-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="3eb84-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmPowerBIEmbeddedCapacity -Name "testcapacity" -ResourceGroupName "testRG"
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

<span data-ttu-id="3eb84-109">Bu komut, resourcegroup testRG 'daki testcapacity adındaki kapasiteyi kaldırır</span><span class="sxs-lookup"><span data-stu-id="3eb84-109">This command will remove the capacity named testcapacity in the resourcegroup testRG</span></span>

## <span data-ttu-id="3eb84-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3eb84-110">PARAMETERS</span></span>

### <span data-ttu-id="3eb84-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3eb84-111">-ResourceGroupName</span></span>
<span data-ttu-id="3eb84-112">Kapasitenin ait olduğu Azure Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="3eb84-112">Name of the Azure resource group to which the capacity belongs</span></span>

```yaml
Type: String
Parameter Sets: ByNameAndResourceGroup
Aliases: 

Required: False
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="3eb84-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="3eb84-113">-Name</span></span>
<span data-ttu-id="3eb84-114">PowerBI Embedded Capacity 'in adı</span><span class="sxs-lookup"><span data-stu-id="3eb84-114">Name of the PowerBI Embedded Capacity</span></span>

```yaml
Type: String
Parameter Sets: ByNameAndResourceGroup
Aliases: 

Required: False
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="3eb84-115">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="3eb84-115">-ResourceId</span></span>
<span data-ttu-id="3eb84-116">Azure Kaynak KIMLIĞI</span><span class="sxs-lookup"><span data-stu-id="3eb84-116">Azure resource ID</span></span>

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

### <span data-ttu-id="3eb84-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3eb84-117">-InputObject</span></span>
<span data-ttu-id="3eb84-118">Boru için giriş nesnesi</span><span class="sxs-lookup"><span data-stu-id="3eb84-118">Input object for Piping</span></span>

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

### <span data-ttu-id="3eb84-119">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="3eb84-119">-PassThru</span></span>
<span data-ttu-id="3eb84-120">İşlem başarıyla tamamlandığında silinen kapasite ayrıntılarını döndürür</span><span class="sxs-lookup"><span data-stu-id="3eb84-120">Will return the deleted capacity details if the operation completes successfully</span></span>

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

### <span data-ttu-id="3eb84-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="3eb84-121">-Confirm</span></span>
<span data-ttu-id="3eb84-122">Kullanıcıya işlemi gerçekleştirmeyi onaylamanızı ister</span><span class="sxs-lookup"><span data-stu-id="3eb84-122">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="3eb84-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3eb84-123">-WhatIf</span></span>
<span data-ttu-id="3eb84-124">Geçerli işlemin gerçekte gerçekleştirmesi gerekmeden gerçekleştireceği işlemleri açıklar</span><span class="sxs-lookup"><span data-stu-id="3eb84-124">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="3eb84-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3eb84-125">CommonParameters</span></span>
<span data-ttu-id="3eb84-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3eb84-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3eb84-127">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3eb84-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3eb84-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3eb84-128">INPUTS</span></span>

### <span data-ttu-id="3eb84-129">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="3eb84-129">None</span></span>
<span data-ttu-id="3eb84-130">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="3eb84-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3eb84-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3eb84-131">OUTPUTS</span></span>

### <span data-ttu-id="3eb84-132">Microsoft. Azure. Commands. PowerBI. modeller. PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="3eb84-132">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="3eb84-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3eb84-133">NOTES</span></span>

## <span data-ttu-id="3eb84-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3eb84-134">RELATED LINKS</span></span>

[<span data-ttu-id="3eb84-135">Get-Azurermpowerbibidedcapacity</span><span class="sxs-lookup"><span data-stu-id="3eb84-135">Get-AzureRmPowerBIEmbeddedCapacity</span></span>](./Get-AzureRmPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="3eb84-136">Yeni-Azurermpowerbibidedcapacity</span><span class="sxs-lookup"><span data-stu-id="3eb84-136">New-AzureRmPowerBIEmbeddedCapacity</span></span>](./New-AzureRmPowerBIEmbeddedCapacity.md)
