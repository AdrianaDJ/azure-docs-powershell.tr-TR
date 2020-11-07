---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotCentral.dll-Help.xml
Module Name: Az.IotCentral
online version: https://docs.microsoft.com/en-us/powershell/module/az.iotcentral/new-aziotcentralapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/New-AzIotCentralApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/New-AzIotCentralApp.md
ms.openlocfilehash: 636c40763c69a4c39ca0bbf8b15fe04fad318d84
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93916519"
---
# <span data-ttu-id="5d2db-101">New-AzIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="5d2db-101">New-AzIotCentralApp</span></span>

## <span data-ttu-id="5d2db-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5d2db-102">SYNOPSIS</span></span>
<span data-ttu-id="5d2db-103">Yeni bir IoT Merkezi uygulaması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="5d2db-103">Creates a new IoT Central Application.</span></span>

## <span data-ttu-id="5d2db-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5d2db-104">SYNTAX</span></span>

```
New-AzIotCentralApp [-Subdomain] <String> [-DisplayName <String>] [-Template <String>] [-Sku <String>]
 [-Location <String>] [-Tag <Hashtable>] [-AsJob] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5d2db-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="5d2db-105">DESCRIPTION</span></span>
<span data-ttu-id="5d2db-106">Sağlanan özellikler ve meta veriler ile yeni bir IoT Merkezi uygulaması oluşturur.</span><span class="sxs-lookup"><span data-stu-id="5d2db-106">Creates a new IoT Central Application with the provided properties and metadata.</span></span> <span data-ttu-id="5d2db-107">IoT merkezi 'ne giriş için bkz https://docs.microsoft.com/en-us/azure/iot-central/ .</span><span class="sxs-lookup"><span data-stu-id="5d2db-107">For an introduction to IoT Central, see https://docs.microsoft.com/en-us/azure/iot-central/.</span></span>

## <span data-ttu-id="5d2db-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5d2db-108">EXAMPLES</span></span>

### <span data-ttu-id="5d2db-109">Örnek 1 basit IoT Merkezi uygulaması oluşturun.</span><span class="sxs-lookup"><span data-stu-id="5d2db-109">Example 1 Create simple IoT Central Application.</span></span>
```powershell
PS C:\> New-AzIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName" -Subdomain "MyAppSubdomain"
```

<span data-ttu-id="5d2db-110">Örnek çıktı:</span><span class="sxs-lookup"><span data-stu-id="5d2db-110">Example Output:</span></span>

<span data-ttu-id="5d2db-111">RESOURCEID:/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. Iotcentral/ıotapps/MyAppResourceName adı: MyAppResourceName türü: Microsoft. ıotcentral/ıotapps konumu: westus etiket: SKU: Microsoft. Azure. Commands. ıotcentral. modeller. PSIotCentralAppSkuInfo ApplicationId: MyApp-XXXX-XXXX-XXXX-XXXXXXXXXXXX iotc-default@1.0.0 DisplayName:</span><span class="sxs-lookup"><span data-stu-id="5d2db-111">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : MyAppResourceName Subdomain         : MyAppSubdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

<span data-ttu-id="5d2db-112">Standart fiyatlandırma katmanı S1 içinde kaynak grubunun bölgesinde bir IoT Merkezi uygulaması oluşturun.</span><span class="sxs-lookup"><span data-stu-id="5d2db-112">Create an IoT Central application in the standard pricing tier S1, in the region of the resource group.</span></span>

### <span data-ttu-id="5d2db-113">Örnek 2 basit IoT Merkezi uygulaması oluşturun.</span><span class="sxs-lookup"><span data-stu-id="5d2db-113">Example 2 Create simple IoT Central Application.</span></span>
```powershell
PS C:\> New-AzIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName" -Subdomain "MyAppSubdomain" -Sku "S1" -DisplayName "My Custom Display Name" -Template "iotc-default" -Location "westus"
```

<span data-ttu-id="5d2db-114">Örnek çıktı:</span><span class="sxs-lookup"><span data-stu-id="5d2db-114">Example Output:</span></span>

<span data-ttu-id="5d2db-115">RESOURCEID:/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. Iotcentral/ıotapps/MyAppResourceName adı: MyAppResourceName türü: Microsoft. ıotcentral/ıotapps konumu: westus etiket: SKU: Microsoft. Azure. Commands. ıotcentral. modeller. PSIotCentralAppSkuInfo ApplicationId: Dizinim-XXXX-XXXX-XXXX-XXXXXXXXXXXX iotc-default@1.0.0 DisplayName:</span><span class="sxs-lookup"><span data-stu-id="5d2db-115">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : My Custom Display Name Subdomain         : MyAppSubdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

<span data-ttu-id="5d2db-116">' Westus ' bölgesinde, ıotc-default şablonunu temel alan özel bir görünen ad ile standart fiyatlandırma katmanı S1 ile IoT Merkezi uygulaması oluşturun.</span><span class="sxs-lookup"><span data-stu-id="5d2db-116">Create an IoT Central application with the standard pricing tier S1 in the 'westus' region, with a custom display name, based on the iotc-default template.</span></span>

## <span data-ttu-id="5d2db-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5d2db-117">PARAMETERS</span></span>

### <span data-ttu-id="5d2db-118">-Iş</span><span class="sxs-lookup"><span data-stu-id="5d2db-118">-AsJob</span></span>
<span data-ttu-id="5d2db-119">Cmdlet 'i arka planda iş olarak çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="5d2db-119">Run cmdlet as a job in the background.</span></span>

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

### <span data-ttu-id="5d2db-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d2db-120">-DefaultProfile</span></span>
<span data-ttu-id="5d2db-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="5d2db-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5d2db-122">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="5d2db-122">-DisplayName</span></span>
<span data-ttu-id="5d2db-123">IoT Merkezi uygulaması için özel görünen ad.</span><span class="sxs-lookup"><span data-stu-id="5d2db-123">Custom display name for the IoT Central application.</span></span>
<span data-ttu-id="5d2db-124">Varsayılan kaynak adıdır.</span><span class="sxs-lookup"><span data-stu-id="5d2db-124">Default is resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d2db-125">-Konum</span><span class="sxs-lookup"><span data-stu-id="5d2db-125">-Location</span></span>
<span data-ttu-id="5d2db-126">IoT merkezi uygulamanızın konumu.</span><span class="sxs-lookup"><span data-stu-id="5d2db-126">Location of your IoT Central application.</span></span>
<span data-ttu-id="5d2db-127">Varsayılan hedef kaynak grubunun konumudur.</span><span class="sxs-lookup"><span data-stu-id="5d2db-127">Default is the location of target resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d2db-128">-Ad</span><span class="sxs-lookup"><span data-stu-id="5d2db-128">-Name</span></span>
<span data-ttu-id="5d2db-129">IoT Merkezi uygulama kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="5d2db-129">Name of the Iot Central Application Resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d2db-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5d2db-130">-ResourceGroupName</span></span>
<span data-ttu-id="5d2db-131">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="5d2db-131">Name of the Resource Group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d2db-132">-SKU</span><span class="sxs-lookup"><span data-stu-id="5d2db-132">-Sku</span></span>
<span data-ttu-id="5d2db-133">IoT merkezi uygulamaları için fiyatlandırma katmanı.</span><span class="sxs-lookup"><span data-stu-id="5d2db-133">Pricing tier for IoT Central applications.</span></span>
<span data-ttu-id="5d2db-134">Varsayılan değer S1 değeridir.</span><span class="sxs-lookup"><span data-stu-id="5d2db-134">Default value is S1.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d2db-135">-Alt etki alanı</span><span class="sxs-lookup"><span data-stu-id="5d2db-135">-Subdomain</span></span>
<span data-ttu-id="5d2db-136">IoT merkezi URL 'SI için alt etki alanı.</span><span class="sxs-lookup"><span data-stu-id="5d2db-136">Subdomain for the IoT Central URL.</span></span>
<span data-ttu-id="5d2db-137">Her uygulamanın benzersiz bir alt etki alanı olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="5d2db-137">Each application must have a unique subdomain.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d2db-138">Etiketli</span><span class="sxs-lookup"><span data-stu-id="5d2db-138">-Tag</span></span>
<span data-ttu-id="5d2db-139">IoT Merkezi uygulama kaynağı etiketleri.</span><span class="sxs-lookup"><span data-stu-id="5d2db-139">Iot Central Application Resource Tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d2db-140">-Şablon</span><span class="sxs-lookup"><span data-stu-id="5d2db-140">-Template</span></span>
<span data-ttu-id="5d2db-141">IoT Merkezi uygulama şablonu adı.</span><span class="sxs-lookup"><span data-stu-id="5d2db-141">IoT Central application template name.</span></span>
<span data-ttu-id="5d2db-142">Varsayılan özel bir uygulamadır.</span><span class="sxs-lookup"><span data-stu-id="5d2db-142">Default is a custom application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d2db-143">-Onay</span><span class="sxs-lookup"><span data-stu-id="5d2db-143">-Confirm</span></span>
<span data-ttu-id="5d2db-144">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="5d2db-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5d2db-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5d2db-145">-WhatIf</span></span>
<span data-ttu-id="5d2db-146">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="5d2db-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5d2db-147">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="5d2db-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5d2db-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d2db-148">CommonParameters</span></span>
<span data-ttu-id="5d2db-149">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5d2db-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d2db-150">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5d2db-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d2db-151">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5d2db-151">INPUTS</span></span>

### <span data-ttu-id="5d2db-152">System. String</span><span class="sxs-lookup"><span data-stu-id="5d2db-152">System.String</span></span>

### <span data-ttu-id="5d2db-153">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="5d2db-153">System.Collections.Hashtable</span></span>

## <span data-ttu-id="5d2db-154">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5d2db-154">OUTPUTS</span></span>

### <span data-ttu-id="5d2db-155">Microsoft. Azure. Commands. ıotcentral. modeller. PSIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="5d2db-155">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span></span>

## <span data-ttu-id="5d2db-156">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5d2db-156">NOTES</span></span>

## <span data-ttu-id="5d2db-157">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5d2db-157">RELATED LINKS</span></span>
