---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/new-azurermiothub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/New-AzureRmIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/New-AzureRmIotHub.md
ms.openlocfilehash: c24f8f9e95db65b464da6586d9e3499358fc3edd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594076"
---
# <span data-ttu-id="e35d4-101">New-AzureRmIotHub</span><span class="sxs-lookup"><span data-stu-id="e35d4-101">New-AzureRmIotHub</span></span>

## <span data-ttu-id="e35d4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e35d4-102">SYNOPSIS</span></span>
<span data-ttu-id="e35d4-103">Yeni bir IotHub.</span><span class="sxs-lookup"><span data-stu-id="e35d4-103">Creates a new IotHub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e35d4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e35d4-104">SYNTAX</span></span>

```
New-AzureRmIotHub -ResourceGroupName <String> -Name <String> -SkuName <PSIotHubSku> -Units <Int64>
 -Location <String> [-Properties <PSIotHubInputProperties>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e35d4-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e35d4-105">DESCRIPTION</span></span>
<span data-ttu-id="e35d4-106">Yeni bir IotHub.</span><span class="sxs-lookup"><span data-stu-id="e35d4-106">Creates a new IotHub.</span></span>
<span data-ttu-id="e35d4-107">IotHub 'i varsayılan özellikler ile oluşturabilir veya giriş özelliklerini belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e35d4-107">You can create the IotHub with either the default properties or specify the input proerties.</span></span>

## <span data-ttu-id="e35d4-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e35d4-108">EXAMPLES</span></span>

### <span data-ttu-id="e35d4-109">Örnek 1 varsayılan özelliklerle yeni bir IotHub oluşturma</span><span class="sxs-lookup"><span data-stu-id="e35d4-109">Example 1 Create a new IotHub with default properties</span></span>
```
PS C:\> New-AzureRmIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub" -SkuName "S1" -Units 1 -Location "northeurope"
```

<span data-ttu-id="e35d4-110">"S1" SKU 'su "myiothub" adlı yeni bir IotHub, kapasite 1 ve konum "northeurope" oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e35d4-110">Creates a new IotHub named "myiothub" of the sku "S1", capacity 1 and location "northeurope".</span></span>

### <span data-ttu-id="e35d4-111">Örnek 2 9 ' da, CloudtoDevice sırasının MaxDeliveryCount ile yeni bir IotHub oluşturma</span><span class="sxs-lookup"><span data-stu-id="e35d4-111">Example 2 Create a new IotHub with the MaxDeliveryCount of the CloudtoDevice Queue set to 20</span></span>
```
PS C:\> New-AzureRmIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub" -SkuName "S1" -Units 1 -Location "northeurope" -Properties $properties
```

<span data-ttu-id="e35d4-112">$Properties tarafından temsil edilen gelişmiş giriş özelliklerini içeren SKU "S1", kapasite 1 ve konum "northeurope" adlı yeni bir IotHub oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e35d4-112">Creates a new IotHub named "myiothub" of the sku "S1", capacity 1 and location "northeurope" with advanced input properties represented by $properties.</span></span>

<span data-ttu-id="e35d4-113">$psCloudToDeviceProperties = New-Object Microsoft. Azure. Commands. Management. IotHub. modeller. Pscses Todeviceproperties-Property @ {MaxDeliveryCount = 20} $properties = New-Object Microsoft. Azure. Commands. Management. IotHub. modeller. Psisuuzubınputproperties-Property @ {CloudToDevice = $psCloudToDeviceProperties} New-AzureRmIotHub-ResourceGroupName "myresourcegroup"-Name "myiothub"-SkuName "S1"-birimler 1-Location "northeurope"-Özellikler $properties</span><span class="sxs-lookup"><span data-stu-id="e35d4-113">$psCloudToDeviceProperties = New-Object Microsoft.Azure.Commands.Management.IotHub.Models.PSCloudToDeviceProperties -Property @{MaxDeliveryCount=20} $properties = New-Object Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties -Property @{CloudToDevice=$psCloudToDeviceProperties} New-AzureRmIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub" -SkuName "S1" -Units 1 -Location "northeurope" -Properties $properties</span></span>

## <span data-ttu-id="e35d4-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e35d4-114">PARAMETERS</span></span>

### <span data-ttu-id="e35d4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e35d4-115">-DefaultProfile</span></span>
<span data-ttu-id="e35d4-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="e35d4-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e35d4-117">-Konum</span><span class="sxs-lookup"><span data-stu-id="e35d4-117">-Location</span></span>
<span data-ttu-id="e35d4-118">IoT Hub 'ın oluşturulması gerektiği konum.</span><span class="sxs-lookup"><span data-stu-id="e35d4-118">Location where the IoT hub needs to be created.</span></span> 

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e35d4-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="e35d4-119">-Name</span></span>
<span data-ttu-id="e35d4-120">IotHub adı</span><span class="sxs-lookup"><span data-stu-id="e35d4-120">Name of the IotHub</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e35d4-121">-Özellikler</span><span class="sxs-lookup"><span data-stu-id="e35d4-121">-Properties</span></span>
<span data-ttu-id="e35d4-122">IoT Hub özellikleri.</span><span class="sxs-lookup"><span data-stu-id="e35d4-122">Properties of the IoT hub.</span></span> 

```yaml
Type: PSIotHubInputProperties
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e35d4-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e35d4-123">-ResourceGroupName</span></span>
<span data-ttu-id="e35d4-124">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="e35d4-124">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e35d4-125">-SkuName</span><span class="sxs-lookup"><span data-stu-id="e35d4-125">-SkuName</span></span>
<span data-ttu-id="e35d4-126">SKU 'nun adı</span><span class="sxs-lookup"><span data-stu-id="e35d4-126">Name of the sku</span></span>

```yaml
Type: PSIotHubSku
Parameter Sets: (All)
Aliases: 
Accepted values: F1, S1, S2, S3

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e35d4-127">-Birimler</span><span class="sxs-lookup"><span data-stu-id="e35d4-127">-Units</span></span>
<span data-ttu-id="e35d4-128">Birim sayısı</span><span class="sxs-lookup"><span data-stu-id="e35d4-128">Number of units</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e35d4-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="e35d4-129">-Confirm</span></span>
<span data-ttu-id="e35d4-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e35d4-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e35d4-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e35d4-131">-WhatIf</span></span>
<span data-ttu-id="e35d4-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e35d4-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e35d4-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e35d4-133">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e35d4-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e35d4-134">CommonParameters</span></span>
<span data-ttu-id="e35d4-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e35d4-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e35d4-136">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e35d4-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e35d4-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e35d4-137">INPUTS</span></span>

### <span data-ttu-id="e35d4-138">System. String</span><span class="sxs-lookup"><span data-stu-id="e35d4-138">System.String</span></span>
<span data-ttu-id="e35d4-139">Microsoft. Azure. Commands. Management. IotHub. modeller. Psiotubsku System. Int64 Microsoft. Azure. Commands. Management. IotHub. modeller. Psiotubınputproperties</span><span class="sxs-lookup"><span data-stu-id="e35d4-139">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubSku System.Int64 Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties</span></span>

## <span data-ttu-id="e35d4-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e35d4-140">OUTPUTS</span></span>

### <span data-ttu-id="e35d4-141">Microsoft. Azure. Commands. Management. IotHub. modeller. Psiçotub</span><span class="sxs-lookup"><span data-stu-id="e35d4-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

## <span data-ttu-id="e35d4-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e35d4-142">NOTES</span></span>

## <span data-ttu-id="e35d4-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e35d4-143">RELATED LINKS</span></span>

