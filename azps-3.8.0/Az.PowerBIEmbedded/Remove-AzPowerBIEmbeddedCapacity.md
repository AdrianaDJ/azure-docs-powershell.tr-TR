---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBI.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/remove-azpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Remove-AzPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Remove-AzPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 1f0f3a9986f69be082a91606d07e86d493f4a269
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94097816"
---
# <span data-ttu-id="a32b3-101">Remove-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="a32b3-101">Remove-AzPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="a32b3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a32b3-102">SYNOPSIS</span></span>
<span data-ttu-id="a32b3-103">PowerBI Embedded kapasitesi örneğini siler.</span><span class="sxs-lookup"><span data-stu-id="a32b3-103">Deletes an instance of PowerBI Embedded Capacity.</span></span>

## <span data-ttu-id="a32b3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a32b3-104">SYNTAX</span></span>

### <span data-ttu-id="a32b3-105">Binaik Vseçresourcegroup (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="a32b3-105">ByNameAndResourceGroup (Default)</span></span>
```
Remove-AzPowerBIEmbeddedCapacity [-Name] <String> [-ResourceGroupName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a32b3-106">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="a32b3-106">ByResourceId</span></span>
```
Remove-AzPowerBIEmbeddedCapacity [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a32b3-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="a32b3-107">ByInputObject</span></span>
```
Remove-AzPowerBIEmbeddedCapacity [-InputObject] <PSPowerBIEmbeddedCapacity> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a32b3-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="a32b3-108">DESCRIPTION</span></span>
<span data-ttu-id="a32b3-109">Remove-AzPowerBIEmbeddedCapacity cmdlet 'i, PowerBI eklenmiş kapasitenin bir örneğini siler</span><span class="sxs-lookup"><span data-stu-id="a32b3-109">The Remove-AzPowerBIEmbeddedCapacity cmdlet deletes an instance of PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="a32b3-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a32b3-110">EXAMPLES</span></span>

### <span data-ttu-id="a32b3-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="a32b3-111">Example 1</span></span>
```
PS C:\> Remove-AzPowerBIEmbeddedCapacity -Name "testcapacity" -ResourceGroupName "testRG"
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

<span data-ttu-id="a32b3-112">Bu komut, resourcegroup testRG 'daki testcapacity adındaki kapasiteyi kaldırır</span><span class="sxs-lookup"><span data-stu-id="a32b3-112">This command will remove the capacity named testcapacity in the resourcegroup testRG</span></span>

## <span data-ttu-id="a32b3-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a32b3-113">PARAMETERS</span></span>

### <span data-ttu-id="a32b3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a32b3-114">-DefaultProfile</span></span>
<span data-ttu-id="a32b3-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a32b3-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a32b3-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a32b3-116">-InputObject</span></span>
<span data-ttu-id="a32b3-117">Boru için giriş nesnesi</span><span class="sxs-lookup"><span data-stu-id="a32b3-117">Input object for Piping</span></span>

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

### <span data-ttu-id="a32b3-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="a32b3-118">-Name</span></span>
<span data-ttu-id="a32b3-119">PowerBI Embedded Capacity 'in adı</span><span class="sxs-lookup"><span data-stu-id="a32b3-119">Name of the PowerBI Embedded Capacity</span></span>

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

### <span data-ttu-id="a32b3-120">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="a32b3-120">-PassThru</span></span>
<span data-ttu-id="a32b3-121">İşlem başarıyla tamamlandığında silinen kapasite ayrıntılarını döndürür</span><span class="sxs-lookup"><span data-stu-id="a32b3-121">Will return the deleted capacity details if the operation completes successfully</span></span>

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

### <span data-ttu-id="a32b3-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a32b3-122">-ResourceGroupName</span></span>
<span data-ttu-id="a32b3-123">Kapasitenin ait olduğu Azure Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="a32b3-123">Name of the Azure resource group to which the capacity belongs</span></span>

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

### <span data-ttu-id="a32b3-124">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="a32b3-124">-ResourceId</span></span>
<span data-ttu-id="a32b3-125">Azure Kaynak KIMLIĞI</span><span class="sxs-lookup"><span data-stu-id="a32b3-125">Azure resource ID</span></span>

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

### <span data-ttu-id="a32b3-126">-Onay</span><span class="sxs-lookup"><span data-stu-id="a32b3-126">-Confirm</span></span>
<span data-ttu-id="a32b3-127">Kullanıcıya işlemi gerçekleştirmeyi onaylamanızı ister</span><span class="sxs-lookup"><span data-stu-id="a32b3-127">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="a32b3-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a32b3-128">-WhatIf</span></span>
<span data-ttu-id="a32b3-129">Geçerli işlemin gerçekte gerçekleştirmesi gerekmeden gerçekleştireceği işlemleri açıklar</span><span class="sxs-lookup"><span data-stu-id="a32b3-129">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="a32b3-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a32b3-130">CommonParameters</span></span>
<span data-ttu-id="a32b3-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a32b3-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a32b3-132">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a32b3-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a32b3-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a32b3-133">INPUTS</span></span>

### <span data-ttu-id="a32b3-134">System. String</span><span class="sxs-lookup"><span data-stu-id="a32b3-134">System.String</span></span>

### <span data-ttu-id="a32b3-135">Microsoft. Azure. Commands. PowerBI. modeller. PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="a32b3-135">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="a32b3-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a32b3-136">OUTPUTS</span></span>

### <span data-ttu-id="a32b3-137">Microsoft. Azure. Commands. PowerBI. modeller. PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="a32b3-137">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="a32b3-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a32b3-138">NOTES</span></span>

## <span data-ttu-id="a32b3-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a32b3-139">RELATED LINKS</span></span>

[<span data-ttu-id="a32b3-140">Get-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="a32b3-140">Get-AzPowerBIEmbeddedCapacity</span></span>](./Get-AzPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="a32b3-141">Yeni-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="a32b3-141">New-AzPowerBIEmbeddedCapacity</span></span>](./New-AzPowerBIEmbeddedCapacity.md)
