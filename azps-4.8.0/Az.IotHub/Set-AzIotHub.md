---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/set-aziothub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHub.md
ms.openlocfilehash: 9011adbbfc7d23c2b9737e315fbec6001428d53c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94109991"
---
# <span data-ttu-id="74173-101">Set-AzIotHub</span><span class="sxs-lookup"><span data-stu-id="74173-101">Set-AzIotHub</span></span>

## <span data-ttu-id="74173-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="74173-102">SYNOPSIS</span></span>
<span data-ttu-id="74173-103">Bir IotHub özelliklerini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="74173-103">Updates the properties of an IotHub.</span></span>

## <span data-ttu-id="74173-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="74173-104">SYNTAX</span></span>

### <span data-ttu-id="74173-105">UpdateSku (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="74173-105">UpdateSku (Default)</span></span>
```
Set-AzIotHub -ResourceGroupName <String> -Name <String> -SkuName <PSIotHubSku> [-Units <Int64>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="74173-106">UpdateEventHubEndpointProperties</span><span class="sxs-lookup"><span data-stu-id="74173-106">UpdateEventHubEndpointProperties</span></span>
```
Set-AzIotHub -ResourceGroupName <String> -Name <String> -EventHubRetentionTimeInDays <Int64>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="74173-107">UpdateFileUploadProperties</span><span class="sxs-lookup"><span data-stu-id="74173-107">UpdateFileUploadProperties</span></span>
```
Set-AzIotHub -ResourceGroupName <String> -Name <String> [-FileUploadStorageConnectionString <String>]
 [-FileUploadContainerName <String>] [-FileUploadSasUriTtl <TimeSpan>] [-FileUploadNotificationTtl <TimeSpan>]
 [-FileUploadNotificationMaxDeliveryCount <Int32>] -EnableFileUploadNotifications <Boolean>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="74173-108">UpdateCloudToDeviceProperties</span><span class="sxs-lookup"><span data-stu-id="74173-108">UpdateCloudToDeviceProperties</span></span>
```
Set-AzIotHub -ResourceGroupName <String> -Name <String> -CloudToDevice <PSCloudToDeviceProperties>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="74173-109">UpdateRoutingProperties</span><span class="sxs-lookup"><span data-stu-id="74173-109">UpdateRoutingProperties</span></span>
```
Set-AzIotHub -ResourceGroupName <String> -Name <String> [-RoutingProperties <PSRoutingProperties>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="74173-110">UpdateRouteProperties</span><span class="sxs-lookup"><span data-stu-id="74173-110">UpdateRouteProperties</span></span>
```
Set-AzIotHub -ResourceGroupName <String> -Name <String>
 [-Routes <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteMetadata]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="74173-111">UpdateFallbackRouteProperty</span><span class="sxs-lookup"><span data-stu-id="74173-111">UpdateFallbackRouteProperty</span></span>
```
Set-AzIotHub -ResourceGroupName <String> -Name <String> [-FallbackRoute <PSFallbackRouteMetadata>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="74173-112">Tanım</span><span class="sxs-lookup"><span data-stu-id="74173-112">DESCRIPTION</span></span>
<span data-ttu-id="74173-113">Bir IotHub özelliklerini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="74173-113">Updates the properties of an IotHub.</span></span>

## <span data-ttu-id="74173-114">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="74173-114">EXAMPLES</span></span>

### <span data-ttu-id="74173-115">Örnek 1 STB 'yi güncelleyin</span><span class="sxs-lookup"><span data-stu-id="74173-115">Example 1 Update the sku</span></span>
```
PS C:\> Set-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub" -SkuName S1 -Units 5
```

<span data-ttu-id="74173-116">"Myiothub" adlı IotHub için STB 'yi S1 ve birimler 'i 5 olarak güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="74173-116">Update the sku to S1 and units to 5 for the IotHub named "myiothub"</span></span>

### <span data-ttu-id="74173-117">Örnek 2 eventhub özelliklerini güncelleyin</span><span class="sxs-lookup"><span data-stu-id="74173-117">Example 2 Update the eventhub properties</span></span>
```
PS C:\> Set-AzIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubRetentionTimeInDays 4
```

<span data-ttu-id="74173-118">IotHub "myiothub" adlı için telemetri bekletme süresini gün olarak güncelleyin</span><span class="sxs-lookup"><span data-stu-id="74173-118">Update the retention time of telemetry in days to 4 for the IotHub named "myiothub"</span></span>

## <span data-ttu-id="74173-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="74173-119">PARAMETERS</span></span>

### <span data-ttu-id="74173-120">-CloudToDevice</span><span class="sxs-lookup"><span data-stu-id="74173-120">-CloudToDevice</span></span>
<span data-ttu-id="74173-121">Cihaza bulut için komut sırası özellikleri.</span><span class="sxs-lookup"><span data-stu-id="74173-121">The properties for the cloud to device command queue.</span></span> 

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSCloudToDeviceProperties
Parameter Sets: UpdateCloudToDeviceProperties
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74173-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74173-122">-DefaultProfile</span></span>
<span data-ttu-id="74173-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="74173-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="74173-124">-EnableFileUploadNotifications</span><span class="sxs-lookup"><span data-stu-id="74173-124">-EnableFileUploadNotifications</span></span>
<span data-ttu-id="74173-125">Dosyanın karşıya yüklenmesi için bildirimlerin etkinleştirilip etkinleştirilmeyeceğini belirten bayrak.</span><span class="sxs-lookup"><span data-stu-id="74173-125">Flag that specifies whether notifications should be enabled for file upload.</span></span> 

```yaml
Type: System.Boolean
Parameter Sets: UpdateFileUploadProperties
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74173-126">-EventHubRetentionTimeInDays</span><span class="sxs-lookup"><span data-stu-id="74173-126">-EventHubRetentionTimeInDays</span></span>
<span data-ttu-id="74173-127">Gün içinde bekletme süresi.</span><span class="sxs-lookup"><span data-stu-id="74173-127">Retention time in days.</span></span> 

```yaml
Type: System.Int64
Parameter Sets: UpdateEventHubEndpointProperties
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74173-128">-FallbackRoute</span><span class="sxs-lookup"><span data-stu-id="74173-128">-FallbackRoute</span></span>
<span data-ttu-id="74173-129">Yönlendirme için geri dönüş rotası</span><span class="sxs-lookup"><span data-stu-id="74173-129">Fallback Route for Routing</span></span>

```yaml
Type: Microsoft.Azure.Management.IotHub.Models.PSFallbackRouteMetadata
Parameter Sets: UpdateFallbackRouteProperty
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74173-130">-FileUploadContainerName</span><span class="sxs-lookup"><span data-stu-id="74173-130">-FileUploadContainerName</span></span>
<span data-ttu-id="74173-131">Dosyaların yükleneceği kapsayıcının adı.</span><span class="sxs-lookup"><span data-stu-id="74173-131">The name of the container to upload the files to.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateFileUploadProperties
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74173-132">-FileUploadNotificationMaxDeliveryCount</span><span class="sxs-lookup"><span data-stu-id="74173-132">-FileUploadNotificationMaxDeliveryCount</span></span>
<span data-ttu-id="74173-133">Karşıya yükleme bildirimlerinin en yüksek teslim sayısı.</span><span class="sxs-lookup"><span data-stu-id="74173-133">The maximum delivery count for file upload notifications.</span></span>  

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: UpdateFileUploadProperties
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74173-134">-FileUploadNotificationTtl</span><span class="sxs-lookup"><span data-stu-id="74173-134">-FileUploadNotificationTtl</span></span>
<span data-ttu-id="74173-135">Dosya karşıya yükleme bildirim sırasındaki iletilerin yaşam süresi.</span><span class="sxs-lookup"><span data-stu-id="74173-135">Time to live value for the messages in the file upload notification queue.</span></span> 

```yaml
Type: System.TimeSpan
Parameter Sets: UpdateFileUploadProperties
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74173-136">-FileUploadSasUriTtl</span><span class="sxs-lookup"><span data-stu-id="74173-136">-FileUploadSasUriTtl</span></span>
<span data-ttu-id="74173-137">Dosya karşıya yükleme için oluşturulan SAS URI 'Si için yaşam süresi.</span><span class="sxs-lookup"><span data-stu-id="74173-137">Time to live for the for the SAS Uri thats generated for file upload.</span></span> 

```yaml
Type: System.TimeSpan
Parameter Sets: UpdateFileUploadProperties
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74173-138">-FileUploadStorageConnectionString</span><span class="sxs-lookup"><span data-stu-id="74173-138">-FileUploadStorageConnectionString</span></span>
<span data-ttu-id="74173-139">Dosyaların karşıya yükleneceği depolama bağlantı dizesi.</span><span class="sxs-lookup"><span data-stu-id="74173-139">The storage connection string to upload the files to.</span></span> 

```yaml
Type: System.String
Parameter Sets: UpdateFileUploadProperties
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74173-140">-Ad</span><span class="sxs-lookup"><span data-stu-id="74173-140">-Name</span></span>
<span data-ttu-id="74173-141">IotHub adı</span><span class="sxs-lookup"><span data-stu-id="74173-141">Name of the IotHub</span></span>

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

### <span data-ttu-id="74173-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="74173-142">-ResourceGroupName</span></span>
<span data-ttu-id="74173-143">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="74173-143">Resource Group Name</span></span>

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

### <span data-ttu-id="74173-144">-Rotalar</span><span class="sxs-lookup"><span data-stu-id="74173-144">-Routes</span></span>
<span data-ttu-id="74173-145">Yönlendirme için eklenecek yollar</span><span class="sxs-lookup"><span data-stu-id="74173-145">Routes to be added for Routing</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Management.IotHub.Models.PSRouteMetadata]
Parameter Sets: UpdateRouteProperties
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74173-146">-RoutingProperties</span><span class="sxs-lookup"><span data-stu-id="74173-146">-RoutingProperties</span></span>
<span data-ttu-id="74173-147">İletileri dış uç noktalara yönlendirmek için yönlendirme özellikleri</span><span class="sxs-lookup"><span data-stu-id="74173-147">The Routing properties for routing messages to external endpoints</span></span> 

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSRoutingProperties
Parameter Sets: UpdateRoutingProperties
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74173-148">-SkuName</span><span class="sxs-lookup"><span data-stu-id="74173-148">-SkuName</span></span>
<span data-ttu-id="74173-149">SKU 'nun adı.</span><span class="sxs-lookup"><span data-stu-id="74173-149">Name of the Sku.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubSku
Parameter Sets: UpdateSku
Aliases:
Accepted values: F1, S1, S2, S3, B1, B2, B3

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74173-150">-Birimler</span><span class="sxs-lookup"><span data-stu-id="74173-150">-Units</span></span>
<span data-ttu-id="74173-151">Birim sayısı</span><span class="sxs-lookup"><span data-stu-id="74173-151">Number of Units</span></span>

```yaml
Type: System.Int64
Parameter Sets: UpdateSku
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74173-152">-Onay</span><span class="sxs-lookup"><span data-stu-id="74173-152">-Confirm</span></span>
<span data-ttu-id="74173-153">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="74173-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="74173-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="74173-154">-WhatIf</span></span>
<span data-ttu-id="74173-155">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="74173-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="74173-156">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="74173-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="74173-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74173-157">CommonParameters</span></span>
<span data-ttu-id="74173-158">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="74173-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74173-159">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="74173-159">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74173-160">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="74173-160">INPUTS</span></span>

### <span data-ttu-id="74173-161">System. String</span><span class="sxs-lookup"><span data-stu-id="74173-161">System.String</span></span>

## <span data-ttu-id="74173-162">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="74173-162">OUTPUTS</span></span>

### <span data-ttu-id="74173-163">Microsoft. Azure. Commands. Management. IotHub. modeller. Psiçotub</span><span class="sxs-lookup"><span data-stu-id="74173-163">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

## <span data-ttu-id="74173-164">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="74173-164">NOTES</span></span>

## <span data-ttu-id="74173-165">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="74173-165">RELATED LINKS</span></span>
