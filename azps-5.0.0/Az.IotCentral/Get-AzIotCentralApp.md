---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotCentral.dll-Help.xml
Module Name: Az.IotCentral
online version: https://docs.microsoft.com/en-us/powershell/module/az.iotcentral/get-aziotcentralapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/Get-AzIotCentralApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/Get-AzIotCentralApp.md
ms.openlocfilehash: cbc7e255f74943ea2aff3518d278035f72394235
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94277798"
---
# <span data-ttu-id="50660-101">Get-AzIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="50660-101">Get-AzIotCentralApp</span></span>

## <span data-ttu-id="50660-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="50660-102">SYNOPSIS</span></span>
<span data-ttu-id="50660-103">Bir veya birkaç IoT Merkezi uygulamasının özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="50660-103">Gets properties for either one or several IoT Central Applications.</span></span>

## <span data-ttu-id="50660-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="50660-104">SYNTAX</span></span>

### <span data-ttu-id="50660-105">ListIotCentralAppsParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="50660-105">ListIotCentralAppsParameterSet (Default)</span></span>
```
Get-AzIotCentralApp [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="50660-106">Interactiveıotmerkezileştirme Parametrekümesi</span><span class="sxs-lookup"><span data-stu-id="50660-106">InteractiveIotCentralParameterSet</span></span>
```
Get-AzIotCentralApp [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="50660-107">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="50660-107">ResourceIdParameterSet</span></span>
```
Get-AzIotCentralApp -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="50660-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="50660-108">DESCRIPTION</span></span>
<span data-ttu-id="50660-109">Belirli bir IoT Merkezi uygulamasının meta verilerini veya parametre kümesine bağlı olarak bir kaynak grubundaki veya abonelikteki tüm uygulamaları alır.</span><span class="sxs-lookup"><span data-stu-id="50660-109">Gets the metadata for either a specific IoT Central Application, or all the applications in a Resource Group or Subscription, depending on Parameter Set.</span></span> 

## <span data-ttu-id="50660-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="50660-110">EXAMPLES</span></span>

### <span data-ttu-id="50660-111">Örnek 1 belirli IoT Merkezi uygulaması alın.</span><span class="sxs-lookup"><span data-stu-id="50660-111">Example 1 Get Specific IoT Central Application.</span></span>
```powershell
PS C:\> Get-AzIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName"
```

<span data-ttu-id="50660-112">Belirtilen IoT Merkezi uygulamasının meta verilerini alır.</span><span class="sxs-lookup"><span data-stu-id="50660-112">Gets the metadata for the specified IoT Central Application.</span></span>

<span data-ttu-id="50660-113">Örnek çıktı:</span><span class="sxs-lookup"><span data-stu-id="50660-113">Example Output:</span></span>

<span data-ttu-id="50660-114">RESOURCEID:/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. Iotmerkezi/ıotapps/Myappkaynakadı: MyAppResourceName türü: Microsoft. ıotmerkezi/ıotapps konumu: westus etiket: {[key, Val]} SKU: Microsoft. Azure. Commands. ıotcentral. modeller. PSIotCentralAppSkuInfo ApplicationId (%. ApplicationId): Myappalt etki alanı şablonu: iotc-default@1.0.0 SubscriptionID: xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx resourcegroupname: MyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="50660-114">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : {[key, val]} Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : My Custom Display Name Subdomain         : MyAppSubdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

### <span data-ttu-id="50660-115">Örnek 2;</span><span class="sxs-lookup"><span data-stu-id="50660-115">Example 2 Get IoT Central Applications in Subscription.</span></span>
```powershell
PS C:\> Get-AzIotCentralApp
```

<span data-ttu-id="50660-116">Geçerli abonelikteki tüm IoT merkezi uygulamaları için meta verileri alır.</span><span class="sxs-lookup"><span data-stu-id="50660-116">Gets the metadata for all the IoT Central Applications in the current Subscription.</span></span>

<span data-ttu-id="50660-117">Örnek çıktı:</span><span class="sxs-lookup"><span data-stu-id="50660-117">Example Output:</span></span>

<span data-ttu-id="50660-118">RESOURCEID:/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. Iotmerkezi/ıotapps/Myappkaynakadı: MyAppResourceName türü: Microsoft. ıotmerkezi/ıotapps konumu: westus etiket: {[key, Val]} SKU: Microsoft. Azure. Commands. ıotcentral. modeller. PSIotCentralAppSkuInfo ApplicationId (%. ApplicationId): Myappalt etki alanı şablonu: iotc-default@1.0.0 SubscriptionID: xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx resourcegroupname: MyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="50660-118">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : {[key, val]} Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : My Custom Display Name Subdomain         : MyAppSubdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

<span data-ttu-id="50660-119">RESOURCEID:/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName2/providers/Microsoft. Iotcentral/ıotapps/MyAppResourceName2 adı: MyAppResourceName2 türü: Microsoft. ıotmerkezi/ıotapps konumu: westus etiket: {[key, Val]} SKU: Microsoft. Azure. Commands. ıotcentral. modeller. PSIotCentralAppSkuInfo ApplicationId 1 alt etki alanı: MyAppSubdomain2 Template: SubscriptionID: XXXXXXXX-xxxx-xxxx-xxxx- iotc-default@1.0.0 xxxxxxxxxxxx ResourceGroupName: MyResourceGroupName2</span><span class="sxs-lookup"><span data-stu-id="50660-119">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName2/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName2 Name              : MyAppResourceName2 Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : {[key, val]} Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : My Custom Display Name 2 Subdomain         : MyAppSubdomain2 Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName2</span></span>

### <span data-ttu-id="50660-120">Örnek 3 kaynak grubunda IoT merkezi uygulamalarını alın.</span><span class="sxs-lookup"><span data-stu-id="50660-120">Example 3 Get IoT Central Applications in Resource Group.</span></span>
```powershell
PS C:\> Get-AzIotCentralApp -ResourceGroupName "MyResourceGroupName"
```

<span data-ttu-id="50660-121">Sağlanan kaynak grubundaki tüm IoT merkezi uygulamaları için meta verileri alır.</span><span class="sxs-lookup"><span data-stu-id="50660-121">Gets the metadata for all IoT Central Applications in the provided Resource Group.</span></span>

<span data-ttu-id="50660-122">Örnek çıktı:</span><span class="sxs-lookup"><span data-stu-id="50660-122">Example Output:</span></span>

<span data-ttu-id="50660-123">RESOURCEID:/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. Iotmerkezi/ıotapps/Myappkaynakadı: MyAppResourceName türü: Microsoft. ıotmerkezi/ıotapps konumu: westus etiket: {[key, Val]} SKU: Microsoft. Azure. Commands. ıotcentral. modeller. PSIotCentralAppSkuInfo ApplicationId (%. ApplicationId): Myappalt etki alanı şablonu: iotc-default@1.0.0 SubscriptionID: xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx resourcegroupname: MyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="50660-123">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : {[key, val]} Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : My Custom Display Name Subdomain         : MyAppSubdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

<span data-ttu-id="50660-124">RESOURCEID:/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. Iotcentral/ıotapps/MyAppResourceName2 adı: MyAppResourceName2 türü: Microsoft. ıotmerkezi/ıotapps konumu: westus etiket: {[key, Val]} SKU: Microsoft. Azure. Commands. ıotcentral. modeller. PSIotCentralAppSkuInfo ApplicationId (XXXXXXXX): MyAppSubdomain2 Template: iotc-default@1.0.0 SubscriptionID: xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx ResourceGroupName: MyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="50660-124">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName2 Name              : MyAppResourceName2 Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : {[key, val]} Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : My Custom Display Name 2 Subdomain         : MyAppSubdomain2 Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

## <span data-ttu-id="50660-125">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="50660-125">PARAMETERS</span></span>

### <span data-ttu-id="50660-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50660-126">-DefaultProfile</span></span>
<span data-ttu-id="50660-127">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="50660-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="50660-128">-Ad</span><span class="sxs-lookup"><span data-stu-id="50660-128">-Name</span></span>
<span data-ttu-id="50660-129">IoT Merkezi uygulama kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="50660-129">Name of the Iot Central Application Resource.</span></span>

```yaml
Type: System.String
Parameter Sets: InteractiveIotCentralParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50660-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="50660-130">-ResourceGroupName</span></span>
<span data-ttu-id="50660-131">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="50660-131">Name of the Resource Group.</span></span>

```yaml
Type: System.String
Parameter Sets: ListIotCentralAppsParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: InteractiveIotCentralParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50660-132">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="50660-132">-ResourceId</span></span>
<span data-ttu-id="50660-133">IoT Merkezi uygulama kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="50660-133">Iot Central Application Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50660-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50660-134">CommonParameters</span></span>
<span data-ttu-id="50660-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="50660-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50660-136">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="50660-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50660-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="50660-137">INPUTS</span></span>

### <span data-ttu-id="50660-138">System. String</span><span class="sxs-lookup"><span data-stu-id="50660-138">System.String</span></span>

## <span data-ttu-id="50660-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="50660-139">OUTPUTS</span></span>

### <span data-ttu-id="50660-140">Microsoft. Azure. Commands. ıotcentral. modeller. PSIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="50660-140">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span></span>

## <span data-ttu-id="50660-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="50660-141">NOTES</span></span>

## <span data-ttu-id="50660-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="50660-142">RELATED LINKS</span></span>
