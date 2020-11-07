---
external help file: Microsoft.Azure.Commands.PowerBI.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.powerbiembedded/suspend-azurermpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Suspend-AzureRmPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Suspend-AzureRmPowerBIEmbeddedCapacity.md
ms.openlocfilehash: c95019c253a4ecb6c442c9f88262f536c4590a83
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762588"
---
# <span data-ttu-id="60234-101">Suspend-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="60234-101">Suspend-AzureRmPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="60234-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="60234-102">SYNOPSIS</span></span>
<span data-ttu-id="60234-103">PowerBI Embedded kapasitesi örneğini askıya alır.</span><span class="sxs-lookup"><span data-stu-id="60234-103">Suspends an instance of PowerBI Embedded Capacity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="60234-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="60234-104">SYNTAX</span></span>

### <span data-ttu-id="60234-105">Binaik Vseçresourcegroup (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="60234-105">ByNameAndResourceGroup (Default)</span></span>
```
Suspend-AzureRmPowerBIEmbeddedCapacity [-Name] <String> [-ResourceGroupName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="60234-106">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="60234-106">ByResourceId</span></span>
```
Suspend-AzureRmPowerBIEmbeddedCapacity [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="60234-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="60234-107">ByInputObject</span></span>
```
Suspend-AzureRmPowerBIEmbeddedCapacity [-InputObject] <PSPowerBIEmbeddedCapacity> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="60234-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="60234-108">DESCRIPTION</span></span>
<span data-ttu-id="60234-109">Suspend-AzureRmPowerBIEmbeddedCapacity cmdlet 'i PowerBI Embedded kapasitesi örneğini askıya alır</span><span class="sxs-lookup"><span data-stu-id="60234-109">The Suspend-AzureRmPowerBIEmbeddedCapacity cmdlet suspends an instance of PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="60234-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="60234-110">EXAMPLES</span></span>

### <span data-ttu-id="60234-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="60234-111">Example 1</span></span>
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

<span data-ttu-id="60234-112">Bu komut, resourcegroup test grubundaki testcapacity adındaki etkin kapasiteyi askıya alır</span><span class="sxs-lookup"><span data-stu-id="60234-112">This command will suspend an active capacity named testcapacity in the resourcegroup testgroup</span></span>

## <span data-ttu-id="60234-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="60234-113">PARAMETERS</span></span>

### <span data-ttu-id="60234-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60234-114">-DefaultProfile</span></span>
<span data-ttu-id="60234-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="60234-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="60234-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="60234-116">-InputObject</span></span>
<span data-ttu-id="60234-117">Boru için giriş nesnesi</span><span class="sxs-lookup"><span data-stu-id="60234-117">Input object for Piping</span></span>

```yaml
Type: Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="60234-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="60234-118">-Name</span></span>
<span data-ttu-id="60234-119">PowerBI Embedded Capacity 'in adı</span><span class="sxs-lookup"><span data-stu-id="60234-119">Name of the PowerBI Embedded Capacity</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameAndResourceGroup
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60234-120">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="60234-120">-PassThru</span></span>
<span data-ttu-id="60234-121">{{Dolgu geçiş açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="60234-121">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="60234-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60234-122">-ResourceGroupName</span></span>
<span data-ttu-id="60234-123">Kapasitenin ait olduğu Azure Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="60234-123">Name of the Azure resource group to which the capacity belongs</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameAndResourceGroup
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60234-124">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="60234-124">-ResourceId</span></span>
<span data-ttu-id="60234-125">Azure Kaynak KIMLIĞI</span><span class="sxs-lookup"><span data-stu-id="60234-125">Azure resource ID</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60234-126">-Onay</span><span class="sxs-lookup"><span data-stu-id="60234-126">-Confirm</span></span>
<span data-ttu-id="60234-127">Kullanıcıya işlemi gerçekleştirmeyi onaylamanızı ister</span><span class="sxs-lookup"><span data-stu-id="60234-127">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="60234-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="60234-128">-WhatIf</span></span>
<span data-ttu-id="60234-129">Geçerli işlemin gerçekte gerçekleştirmesi gerekmeden gerçekleştireceği işlemleri açıklar</span><span class="sxs-lookup"><span data-stu-id="60234-129">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="60234-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60234-130">CommonParameters</span></span>
<span data-ttu-id="60234-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="60234-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60234-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="60234-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60234-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="60234-133">INPUTS</span></span>

### <span data-ttu-id="60234-134">System. String</span><span class="sxs-lookup"><span data-stu-id="60234-134">System.String</span></span>

### <span data-ttu-id="60234-135">Microsoft. Azure. Commands. PowerBI. modeller. PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="60234-135">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>
<span data-ttu-id="60234-136">Parametreler: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="60234-136">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="60234-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="60234-137">OUTPUTS</span></span>

### <span data-ttu-id="60234-138">Microsoft. Azure. Commands. PowerBI. modeller. PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="60234-138">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="60234-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="60234-139">NOTES</span></span>

## <span data-ttu-id="60234-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="60234-140">RELATED LINKS</span></span>

[<span data-ttu-id="60234-141">Get-Azurermpowerbibidedcapacity</span><span class="sxs-lookup"><span data-stu-id="60234-141">Get-AzureRmPowerBIEmbeddedCapacity</span></span>](./Get-AzureRmPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="60234-142">Özgeçmiş-Azurermpowerbibidedcapacity</span><span class="sxs-lookup"><span data-stu-id="60234-142">Resume-AzureRmPowerBIEmbeddedCapacity</span></span>](./Resume-AzureRmPowerBIEmbeddedCapacity.md)

