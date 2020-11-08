---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/new-aziothub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/New-AzIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/New-AzIotHub.md
ms.openlocfilehash: ad9c032a4384a82e03704529796a209e8c88f4c5
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94274913"
---
# <span data-ttu-id="2b208-101">New-AzIotHub</span><span class="sxs-lookup"><span data-stu-id="2b208-101">New-AzIotHub</span></span>

## <span data-ttu-id="2b208-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2b208-102">SYNOPSIS</span></span>
<span data-ttu-id="2b208-103">Yeni bir IotHub.</span><span class="sxs-lookup"><span data-stu-id="2b208-103">Creates a new IotHub.</span></span>

## <span data-ttu-id="2b208-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2b208-104">SYNTAX</span></span>

```
New-AzIotHub -ResourceGroupName <String> -Name <String> -SkuName <PSIotHubSku> -Units <Int64>
 -Location <String> [-Properties <PSIotHubInputProperties>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2b208-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="2b208-105">DESCRIPTION</span></span>
<span data-ttu-id="2b208-106">Yeni bir IotHub.</span><span class="sxs-lookup"><span data-stu-id="2b208-106">Creates a new IotHub.</span></span>
<span data-ttu-id="2b208-107">IotHub 'i varsayılan özellikler ile oluşturabilir veya giriş özelliklerini belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="2b208-107">You can create the IotHub with either the default properties or specify the input properties.</span></span>

## <span data-ttu-id="2b208-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2b208-108">EXAMPLES</span></span>

### <span data-ttu-id="2b208-109">Örnek 1 varsayılan özelliklerle yeni bir IotHub oluşturma</span><span class="sxs-lookup"><span data-stu-id="2b208-109">Example 1 Create a new IotHub with default properties</span></span>
```
PS C:\> New-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub" -SkuName "S1" -Units 1 -Location "northeurope"
```

<span data-ttu-id="2b208-110">"S1" SKU 'su "myiothub" adlı yeni bir IotHub, kapasite 1 ve konum "northeurope" oluşturur.</span><span class="sxs-lookup"><span data-stu-id="2b208-110">Creates a new IotHub named "myiothub" of the sku "S1", capacity 1 and location "northeurope".</span></span>

### <span data-ttu-id="2b208-111">Örnek 2 9 ' da, CloudToDevice sırasının MaxDeliveryCount ile yeni bir IotHub oluşturma</span><span class="sxs-lookup"><span data-stu-id="2b208-111">Example 2 Create a new IotHub with the MaxDeliveryCount of the CloudToDevice Queue set to 20</span></span>
```
PS C:\> New-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub" -SkuName "S1" -Units 1 -Location "northeurope" -Properties $properties
```

<span data-ttu-id="2b208-112">$Properties tarafından temsil edilen gelişmiş giriş özelliklerini içeren SKU "S1", kapasite 1 ve konum "northeurope" adlı yeni bir IotHub oluşturur.</span><span class="sxs-lookup"><span data-stu-id="2b208-112">Creates a new IotHub named "myiothub" of the sku "S1", capacity 1 and location "northeurope" with advanced input properties represented by $properties.</span></span>
<span data-ttu-id="2b208-113">$psCloudToDeviceProperties = New-Object Microsoft. Azure. Commands. Management. IotHub. modeller. Pscses Todeviceproperties-Property @ {MaxDeliveryCount = 20} $properties = New-Object Microsoft. Azure. Commands. Management. IotHub. modeller. Psisuuzubınputproperties-Property @ {CloudToDevice = $psCloudToDeviceProperties} New-AzIotHub-ResourceGroupName "myresourcegroup"-Name "myiothub"-SkuName "S1"-birimler 1-Location "northeurope"-Özellikler $properties</span><span class="sxs-lookup"><span data-stu-id="2b208-113">$psCloudToDeviceProperties = New-Object Microsoft.Azure.Commands.Management.IotHub.Models.PSCloudToDeviceProperties -Property @{MaxDeliveryCount=20} $properties = New-Object Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties -Property @{CloudToDevice=$psCloudToDeviceProperties} New-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub" -SkuName "S1" -Units 1 -Location "northeurope" -Properties $properties</span></span>

## <span data-ttu-id="2b208-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2b208-114">PARAMETERS</span></span>

### <span data-ttu-id="2b208-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b208-115">-DefaultProfile</span></span>
<span data-ttu-id="2b208-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="2b208-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2b208-117">-Konum</span><span class="sxs-lookup"><span data-stu-id="2b208-117">-Location</span></span>
<span data-ttu-id="2b208-118">IoT Hub 'ın oluşturulması gerektiği konum.</span><span class="sxs-lookup"><span data-stu-id="2b208-118">Location where the IoT hub needs to be created.</span></span> 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b208-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="2b208-119">-Name</span></span>
<span data-ttu-id="2b208-120">IotHub adı</span><span class="sxs-lookup"><span data-stu-id="2b208-120">Name of the IotHub</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b208-121">-Özellikler</span><span class="sxs-lookup"><span data-stu-id="2b208-121">-Properties</span></span>
<span data-ttu-id="2b208-122">IoT Hub özellikleri.</span><span class="sxs-lookup"><span data-stu-id="2b208-122">Properties of the IoT hub.</span></span> 

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b208-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2b208-123">-ResourceGroupName</span></span>
<span data-ttu-id="2b208-124">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="2b208-124">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b208-125">-SkuName</span><span class="sxs-lookup"><span data-stu-id="2b208-125">-SkuName</span></span>
<span data-ttu-id="2b208-126">SKU 'nun adı</span><span class="sxs-lookup"><span data-stu-id="2b208-126">Name of the sku</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubSku
Parameter Sets: (All)
Aliases:
Accepted values: F1, S1, S2, S3, B1, B2, B3

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b208-127">-Birimler</span><span class="sxs-lookup"><span data-stu-id="2b208-127">-Units</span></span>
<span data-ttu-id="2b208-128">Birim sayısı</span><span class="sxs-lookup"><span data-stu-id="2b208-128">Number of units</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b208-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="2b208-129">-Confirm</span></span>
<span data-ttu-id="2b208-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="2b208-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b208-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2b208-131">-WhatIf</span></span>
<span data-ttu-id="2b208-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="2b208-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2b208-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="2b208-133">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b208-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b208-134">CommonParameters</span></span>
<span data-ttu-id="2b208-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2b208-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b208-136">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2b208-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b208-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2b208-137">INPUTS</span></span>

### <span data-ttu-id="2b208-138">System. String</span><span class="sxs-lookup"><span data-stu-id="2b208-138">System.String</span></span>

## <span data-ttu-id="2b208-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2b208-139">OUTPUTS</span></span>

### <span data-ttu-id="2b208-140">Microsoft. Azure. Commands. Management. IotHub. modeller. Psiçotub</span><span class="sxs-lookup"><span data-stu-id="2b208-140">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

## <span data-ttu-id="2b208-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2b208-141">NOTES</span></span>

## <span data-ttu-id="2b208-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2b208-142">RELATED LINKS</span></span>
