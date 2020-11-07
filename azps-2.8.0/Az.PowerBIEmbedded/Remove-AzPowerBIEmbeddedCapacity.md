---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBI.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/remove-azpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Remove-AzPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Remove-AzPowerBIEmbeddedCapacity.md
ms.openlocfilehash: fff76d83c3cb80c620414d07808e473ac3892e99
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93932803"
---
# <span data-ttu-id="baa95-101">Remove-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="baa95-101">Remove-AzPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="baa95-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="baa95-102">SYNOPSIS</span></span>
<span data-ttu-id="baa95-103">PowerBI Embedded kapasitesi örneğini siler.</span><span class="sxs-lookup"><span data-stu-id="baa95-103">Deletes an instance of PowerBI Embedded Capacity.</span></span>

## <span data-ttu-id="baa95-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="baa95-104">SYNTAX</span></span>

### <span data-ttu-id="baa95-105">Binaik Vseçresourcegroup (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="baa95-105">ByNameAndResourceGroup (Default)</span></span>
```
Remove-AzPowerBIEmbeddedCapacity [-Name] <String> [-ResourceGroupName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="baa95-106">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="baa95-106">ByResourceId</span></span>
```
Remove-AzPowerBIEmbeddedCapacity [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="baa95-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="baa95-107">ByInputObject</span></span>
```
Remove-AzPowerBIEmbeddedCapacity [-InputObject] <PSPowerBIEmbeddedCapacity> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="baa95-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="baa95-108">DESCRIPTION</span></span>
<span data-ttu-id="baa95-109">Remove-AzPowerBIEmbeddedCapacity cmdlet 'i, PowerBI eklenmiş kapasitenin bir örneğini siler</span><span class="sxs-lookup"><span data-stu-id="baa95-109">The Remove-AzPowerBIEmbeddedCapacity cmdlet deletes an instance of PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="baa95-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="baa95-110">EXAMPLES</span></span>

### <span data-ttu-id="baa95-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="baa95-111">Example 1</span></span>
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

<span data-ttu-id="baa95-112">Bu komut, resourcegroup testRG 'daki testcapacity adındaki kapasiteyi kaldırır</span><span class="sxs-lookup"><span data-stu-id="baa95-112">This command will remove the capacity named testcapacity in the resourcegroup testRG</span></span>

## <span data-ttu-id="baa95-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="baa95-113">PARAMETERS</span></span>

### <span data-ttu-id="baa95-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="baa95-114">-DefaultProfile</span></span>
<span data-ttu-id="baa95-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="baa95-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="baa95-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="baa95-116">-InputObject</span></span>
<span data-ttu-id="baa95-117">Boru için giriş nesnesi</span><span class="sxs-lookup"><span data-stu-id="baa95-117">Input object for Piping</span></span>

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

### <span data-ttu-id="baa95-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="baa95-118">-Name</span></span>
<span data-ttu-id="baa95-119">PowerBI Embedded Capacity 'in adı</span><span class="sxs-lookup"><span data-stu-id="baa95-119">Name of the PowerBI Embedded Capacity</span></span>

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

### <span data-ttu-id="baa95-120">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="baa95-120">-PassThru</span></span>
<span data-ttu-id="baa95-121">İşlem başarıyla tamamlandığında silinen kapasite ayrıntılarını döndürür</span><span class="sxs-lookup"><span data-stu-id="baa95-121">Will return the deleted capacity details if the operation completes successfully</span></span>

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

### <span data-ttu-id="baa95-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="baa95-122">-ResourceGroupName</span></span>
<span data-ttu-id="baa95-123">Kapasitenin ait olduğu Azure Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="baa95-123">Name of the Azure resource group to which the capacity belongs</span></span>

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

### <span data-ttu-id="baa95-124">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="baa95-124">-ResourceId</span></span>
<span data-ttu-id="baa95-125">Azure Kaynak KIMLIĞI</span><span class="sxs-lookup"><span data-stu-id="baa95-125">Azure resource ID</span></span>

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

### <span data-ttu-id="baa95-126">-Onay</span><span class="sxs-lookup"><span data-stu-id="baa95-126">-Confirm</span></span>
<span data-ttu-id="baa95-127">Kullanıcıya işlemi gerçekleştirmeyi onaylamanızı ister</span><span class="sxs-lookup"><span data-stu-id="baa95-127">Prompts user to confirm whether to perform the operation</span></span>

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

### <span data-ttu-id="baa95-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="baa95-128">-WhatIf</span></span>
<span data-ttu-id="baa95-129">Geçerli işlemin gerçekte gerçekleştirmesi gerekmeden gerçekleştireceği işlemleri açıklar</span><span class="sxs-lookup"><span data-stu-id="baa95-129">Describes the actions the current operation will perform without actually performing them</span></span>

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

### <span data-ttu-id="baa95-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="baa95-130">CommonParameters</span></span>
<span data-ttu-id="baa95-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="baa95-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="baa95-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="baa95-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="baa95-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="baa95-133">INPUTS</span></span>

### <span data-ttu-id="baa95-134">System. String</span><span class="sxs-lookup"><span data-stu-id="baa95-134">System.String</span></span>

### <span data-ttu-id="baa95-135">Microsoft. Azure. Commands. PowerBI. modeller. PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="baa95-135">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="baa95-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="baa95-136">OUTPUTS</span></span>

### <span data-ttu-id="baa95-137">Microsoft. Azure. Commands. PowerBI. modeller. PSPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="baa95-137">Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="baa95-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="baa95-138">NOTES</span></span>

## <span data-ttu-id="baa95-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="baa95-139">RELATED LINKS</span></span>

[<span data-ttu-id="baa95-140">Get-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="baa95-140">Get-AzPowerBIEmbeddedCapacity</span></span>](./Get-AzPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="baa95-141">Yeni-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="baa95-141">New-AzPowerBIEmbeddedCapacity</span></span>](./New-AzPowerBIEmbeddedCapacity.md)
