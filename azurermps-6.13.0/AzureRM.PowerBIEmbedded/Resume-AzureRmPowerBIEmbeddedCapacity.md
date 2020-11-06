---
external help file: Microsoft.Azure.Commands.PowerBI.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.powerbiembedded/resume-azurermpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Resume-AzureRmPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Resume-AzureRmPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 29113eecc02443fe2fbc8f57ada1fcfa8e7a2d98
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588413"
---
# <span data-ttu-id="2e535-101">Resume-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="2e535-101">Resume-AzureRmPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="2e535-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2e535-102">SYNOPSIS</span></span>
<span data-ttu-id="2e535-103">PowerBI Embedded kapasitesi örneğini sürdürür.</span><span class="sxs-lookup"><span data-stu-id="2e535-103">Resumes an instance of PowerBI Embedded Capacity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2e535-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2e535-104">SYNTAX</span></span>

### <span data-ttu-id="2e535-105">Binaik Vseçresourcegroup (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="2e535-105">ByNameAndResourceGroup (Default)</span></span>
```
Resume-AzureRmPowerBIEmbeddedCapacity [-Name] <String> [-ResourceGroupName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2e535-106">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="2e535-106">ByResourceId</span></span>
```
Resume-AzureRmPowerBIEmbeddedCapacity [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2e535-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="2e535-107">ByInputObject</span></span>
```
Resume-AzureRmPowerBIEmbeddedCapacity [-InputObject] <PSPowerBIEmbeddedCapacity> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2e535-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="2e535-108">DESCRIPTION</span></span>
<span data-ttu-id="2e535-109">Resume-AzureRmPowerBIEmbeddedCapacity cmdlet 'i, PowerBI Embedded kapasitesini sürdürür</span><span class="sxs-lookup"><span data-stu-id="2e535-109">The Resume-AzureRmPowerBIEmbeddedCapacity cmdlet resumes an instance of PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="2e535-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2e535-110">EXAMPLES</span></span>

### <span data-ttu-id="2e535-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="2e535-111">Example 1</span></span>
```
PS C:\> Resume-AzureRmPowerBIEmbeddedCapacity -Name "testcapacity" -ResourceGroupName "testRG" -PassThru
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

<span data-ttu-id="2e535-112">Bu komut, resourcegroup testRG 'da testcapacity adlı duraklatılan kapasiteyi sürdürür</span><span class="sxs-lookup"><span data-stu-id="2e535-112">This command will resume a paused capacity named testcapacity in the resourcegroup testRG</span></span>

## <span data-ttu-id="2e535-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2e535-113">PARAMETERS</span></span>

### <span data-ttu-id="2e535-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e535-114">-DefaultProfile</span></span>
<span data-ttu-id="2e535-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2e535-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2e535-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2e535-116">-InputObject</span></span>
<span data-ttu-id="2e535-117">Boru için giriş nesnesi</span><span class="sxs-lookup"><span data-stu-id="2e535-117">Input object for Piping</span></span>

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

### <span data-ttu-id="2e535-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="2e535-118">-Name</span></span>
<span data-ttu-id="2e535-119">PowerBI Embedded Capacity 'in adı</span><span class="sxs-lookup"><span data-stu-id="2e535-119">Name of the PowerBI Embedded Capacity</span></span>

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

### <span data-ttu-id="2e535-120">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="2e535-120">-PassThru</span></span>
<span data-ttu-id="2e535-121">{{Dolgu geçiş açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="2e535-121">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="2e535-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e535-122">-ResourceGroupName</span></span>
<span data-ttu-id="2e535-123">Kapasitenin ait olduğu Azure Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="2e535-123">Name of the Azure resource group to which the capacity belongs</span></span>

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

### <span data-ttu-id="2e535-124">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="2e535-124">-ResourceId</span></span>
<span data-ttu-id="2e535-125">Azure Kaynak KIMLIĞI</span><span class="sxs-lookup"><span data-stu-id="2e535-125">Azure resource ID</span></span>

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

### <span data-ttu-id="2e535-126">-Onay</span><span class="sxs-lookup"><span data-stu-id="2e535-126">-Confirm</span></span>
<span data-ttu-id="2e535-127">Kullanıcıya işlemi gerçekleştirmeyi onaylamanızı ister</span><span class="sxs-lookup"><span data-stu-id="2e535-127">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="2e535-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2e535-128">-WhatIf</span></span>
<span data-ttu-id="2e535-129">Geçerli işlemin gerçekte gerçekleştirmesi gerekmeden gerçekleştireceği işlemleri açıklar</span><span class="sxs-lookup"><span data-stu-id="2e535-129">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="2e535-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e535-130">CommonParameters</span></span>
<span data-ttu-id="2e535-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2e535-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e535-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2e535-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e535-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2e535-133">INPUTS</span></span>

### <span data-ttu-id="2e535-134">System. String</span><span class="sxs-lookup"><span data-stu-id="2e535-134">System.String</span></span>

### <span data-ttu-id="2e535-135">Microsoft. Azure. Commands. PowerBI. modeller. PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="2e535-135">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>
<span data-ttu-id="2e535-136">Parametreler: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="2e535-136">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="2e535-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2e535-137">OUTPUTS</span></span>

### <span data-ttu-id="2e535-138">Microsoft. Azure. Commands. PowerBI. modeller. PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="2e535-138">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="2e535-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2e535-139">NOTES</span></span>

## <span data-ttu-id="2e535-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2e535-140">RELATED LINKS</span></span>

[<span data-ttu-id="2e535-141">Get-Azurermpowerbibidedcapacity</span><span class="sxs-lookup"><span data-stu-id="2e535-141">Get-AzureRmPowerBIEmbeddedCapacity</span></span>](./Get-AzureRmPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="2e535-142">Askıya al-Azurermpowerbibidedcapacity</span><span class="sxs-lookup"><span data-stu-id="2e535-142">Suspend-AzureRmPowerBIEmbeddedCapacity</span></span>](./Suspend-AzureRmPowerBIEmbeddedCapacity.md)
