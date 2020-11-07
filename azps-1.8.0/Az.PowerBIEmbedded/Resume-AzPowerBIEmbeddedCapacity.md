---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBI.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/resume-azpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Resume-AzPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Resume-AzPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 83d6dd250865bc8f1fc7fd70256742a58bd68de0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93759802"
---
# <span data-ttu-id="f0333-101">Resume-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="f0333-101">Resume-AzPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="f0333-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f0333-102">SYNOPSIS</span></span>
<span data-ttu-id="f0333-103">PowerBI Embedded kapasitesi örneğini sürdürür.</span><span class="sxs-lookup"><span data-stu-id="f0333-103">Resumes an instance of PowerBI Embedded Capacity.</span></span>

## <span data-ttu-id="f0333-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f0333-104">SYNTAX</span></span>

### <span data-ttu-id="f0333-105">Binaik Vseçresourcegroup (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="f0333-105">ByNameAndResourceGroup (Default)</span></span>
```
Resume-AzPowerBIEmbeddedCapacity [-Name] <String> [-ResourceGroupName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f0333-106">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="f0333-106">ByResourceId</span></span>
```
Resume-AzPowerBIEmbeddedCapacity [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f0333-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="f0333-107">ByInputObject</span></span>
```
Resume-AzPowerBIEmbeddedCapacity [-InputObject] <PSPowerBIEmbeddedCapacity> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f0333-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="f0333-108">DESCRIPTION</span></span>
<span data-ttu-id="f0333-109">Resume-AzPowerBIEmbeddedCapacity cmdlet 'i, PowerBI Embedded kapasitesini sürdürür</span><span class="sxs-lookup"><span data-stu-id="f0333-109">The Resume-AzPowerBIEmbeddedCapacity cmdlet resumes an instance of PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="f0333-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f0333-110">EXAMPLES</span></span>

### <span data-ttu-id="f0333-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="f0333-111">Example 1</span></span>
```
PS C:\> Resume-AzPowerBIEmbeddedCapacity -Name "testcapacity" -ResourceGroupName "testRG" -PassThru
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

<span data-ttu-id="f0333-112">Bu komut, resourcegroup testRG 'da testcapacity adlı duraklatılan kapasiteyi sürdürür</span><span class="sxs-lookup"><span data-stu-id="f0333-112">This command will resume a paused capacity named testcapacity in the resourcegroup testRG</span></span>

## <span data-ttu-id="f0333-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f0333-113">PARAMETERS</span></span>

### <span data-ttu-id="f0333-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0333-114">-DefaultProfile</span></span>
<span data-ttu-id="f0333-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f0333-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f0333-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f0333-116">-InputObject</span></span>
<span data-ttu-id="f0333-117">Boru için giriş nesnesi</span><span class="sxs-lookup"><span data-stu-id="f0333-117">Input object for Piping</span></span>

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

### <span data-ttu-id="f0333-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="f0333-118">-Name</span></span>
<span data-ttu-id="f0333-119">PowerBI Embedded Capacity 'in adı</span><span class="sxs-lookup"><span data-stu-id="f0333-119">Name of the PowerBI Embedded Capacity</span></span>

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

### <span data-ttu-id="f0333-120">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="f0333-120">-PassThru</span></span>
<span data-ttu-id="f0333-121">{{Dolgu geçiş açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="f0333-121">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="f0333-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f0333-122">-ResourceGroupName</span></span>
<span data-ttu-id="f0333-123">Kapasitenin ait olduğu Azure Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="f0333-123">Name of the Azure resource group to which the capacity belongs</span></span>

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

### <span data-ttu-id="f0333-124">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="f0333-124">-ResourceId</span></span>
<span data-ttu-id="f0333-125">Azure Kaynak KIMLIĞI</span><span class="sxs-lookup"><span data-stu-id="f0333-125">Azure resource ID</span></span>

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

### <span data-ttu-id="f0333-126">-Onay</span><span class="sxs-lookup"><span data-stu-id="f0333-126">-Confirm</span></span>
<span data-ttu-id="f0333-127">Kullanıcıya işlemi gerçekleştirmeyi onaylamanızı ister</span><span class="sxs-lookup"><span data-stu-id="f0333-127">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="f0333-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f0333-128">-WhatIf</span></span>
<span data-ttu-id="f0333-129">Geçerli işlemin gerçekte gerçekleştirmesi gerekmeden gerçekleştireceği işlemleri açıklar</span><span class="sxs-lookup"><span data-stu-id="f0333-129">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="f0333-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0333-130">CommonParameters</span></span>
<span data-ttu-id="f0333-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f0333-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0333-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f0333-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0333-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f0333-133">INPUTS</span></span>

### <span data-ttu-id="f0333-134">System. String</span><span class="sxs-lookup"><span data-stu-id="f0333-134">System.String</span></span>

### <span data-ttu-id="f0333-135">Microsoft. Azure. Commands. PowerBI. modeller. PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="f0333-135">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="f0333-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f0333-136">OUTPUTS</span></span>

### <span data-ttu-id="f0333-137">Microsoft. Azure. Commands. PowerBI. modeller. PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="f0333-137">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="f0333-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f0333-138">NOTES</span></span>

## <span data-ttu-id="f0333-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f0333-139">RELATED LINKS</span></span>

[<span data-ttu-id="f0333-140">Get-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="f0333-140">Get-AzPowerBIEmbeddedCapacity</span></span>](./Get-AzPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="f0333-141">Askıya al-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="f0333-141">Suspend-AzPowerBIEmbeddedCapacity</span></span>](./Suspend-AzPowerBIEmbeddedCapacity.md)