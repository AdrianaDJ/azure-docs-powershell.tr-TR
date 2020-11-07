---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBI.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/suspend-azpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Suspend-AzPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Suspend-AzPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 8a406ebfe6c919dad30e7a394b0b4a4c912cf557
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93759800"
---
# <span data-ttu-id="2573d-101">Suspend-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="2573d-101">Suspend-AzPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="2573d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2573d-102">SYNOPSIS</span></span>
<span data-ttu-id="2573d-103">PowerBI Embedded kapasitesi örneğini askıya alır.</span><span class="sxs-lookup"><span data-stu-id="2573d-103">Suspends an instance of PowerBI Embedded Capacity.</span></span>

## <span data-ttu-id="2573d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2573d-104">SYNTAX</span></span>

### <span data-ttu-id="2573d-105">Binaik Vseçresourcegroup (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="2573d-105">ByNameAndResourceGroup (Default)</span></span>
```
Suspend-AzPowerBIEmbeddedCapacity [-Name] <String> [-ResourceGroupName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2573d-106">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="2573d-106">ByResourceId</span></span>
```
Suspend-AzPowerBIEmbeddedCapacity [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2573d-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="2573d-107">ByInputObject</span></span>
```
Suspend-AzPowerBIEmbeddedCapacity [-InputObject] <PSPowerBIEmbeddedCapacity> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2573d-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="2573d-108">DESCRIPTION</span></span>
<span data-ttu-id="2573d-109">Suspend-AzPowerBIEmbeddedCapacity cmdlet 'i PowerBI Embedded kapasitesi örneğini askıya alır</span><span class="sxs-lookup"><span data-stu-id="2573d-109">The Suspend-AzPowerBIEmbeddedCapacity cmdlet suspends an instance of PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="2573d-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2573d-110">EXAMPLES</span></span>

### <span data-ttu-id="2573d-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="2573d-111">Example 1</span></span>
```
PS C:\> Suspend-AzPowerBIEmbeddedCapacity -Name "testcapacity" -ResourceGroupName "testRG" -PassThru
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

<span data-ttu-id="2573d-112">Bu komut, resourcegroup test grubundaki testcapacity adındaki etkin kapasiteyi askıya alır</span><span class="sxs-lookup"><span data-stu-id="2573d-112">This command will suspend an active capacity named testcapacity in the resourcegroup testgroup</span></span>

## <span data-ttu-id="2573d-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2573d-113">PARAMETERS</span></span>

### <span data-ttu-id="2573d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2573d-114">-DefaultProfile</span></span>
<span data-ttu-id="2573d-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2573d-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2573d-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2573d-116">-InputObject</span></span>
<span data-ttu-id="2573d-117">Boru için giriş nesnesi</span><span class="sxs-lookup"><span data-stu-id="2573d-117">Input object for Piping</span></span>

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

### <span data-ttu-id="2573d-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="2573d-118">-Name</span></span>
<span data-ttu-id="2573d-119">PowerBI Embedded Capacity 'in adı</span><span class="sxs-lookup"><span data-stu-id="2573d-119">Name of the PowerBI Embedded Capacity</span></span>

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

### <span data-ttu-id="2573d-120">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="2573d-120">-PassThru</span></span>
<span data-ttu-id="2573d-121">{{Dolgu geçiş açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="2573d-121">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="2573d-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2573d-122">-ResourceGroupName</span></span>
<span data-ttu-id="2573d-123">Kapasitenin ait olduğu Azure Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="2573d-123">Name of the Azure resource group to which the capacity belongs</span></span>

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

### <span data-ttu-id="2573d-124">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="2573d-124">-ResourceId</span></span>
<span data-ttu-id="2573d-125">Azure Kaynak KIMLIĞI</span><span class="sxs-lookup"><span data-stu-id="2573d-125">Azure resource ID</span></span>

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

### <span data-ttu-id="2573d-126">-Onay</span><span class="sxs-lookup"><span data-stu-id="2573d-126">-Confirm</span></span>
<span data-ttu-id="2573d-127">Kullanıcıya işlemi gerçekleştirmeyi onaylamanızı ister</span><span class="sxs-lookup"><span data-stu-id="2573d-127">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="2573d-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2573d-128">-WhatIf</span></span>
<span data-ttu-id="2573d-129">Geçerli işlemin gerçekte gerçekleştirmesi gerekmeden gerçekleştireceği işlemleri açıklar</span><span class="sxs-lookup"><span data-stu-id="2573d-129">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="2573d-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2573d-130">CommonParameters</span></span>
<span data-ttu-id="2573d-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2573d-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2573d-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2573d-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2573d-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2573d-133">INPUTS</span></span>

### <span data-ttu-id="2573d-134">System. String</span><span class="sxs-lookup"><span data-stu-id="2573d-134">System.String</span></span>

### <span data-ttu-id="2573d-135">Microsoft. Azure. Commands. PowerBI. modeller. PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="2573d-135">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="2573d-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2573d-136">OUTPUTS</span></span>

### <span data-ttu-id="2573d-137">Microsoft. Azure. Commands. PowerBI. modeller. PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="2573d-137">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="2573d-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2573d-138">NOTES</span></span>

## <span data-ttu-id="2573d-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2573d-139">RELATED LINKS</span></span>

[<span data-ttu-id="2573d-140">Get-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="2573d-140">Get-AzPowerBIEmbeddedCapacity</span></span>](./Get-AzPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="2573d-141">Özgeçmiş-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="2573d-141">Resume-AzPowerBIEmbeddedCapacity</span></span>](./Resume-AzPowerBIEmbeddedCapacity.md)

