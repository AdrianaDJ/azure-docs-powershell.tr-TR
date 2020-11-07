---
external help file: Microsoft.Azure.Commands.IotCentral.dll-Help.xml
Module Name: AzureRM.IotCentral
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iotcentral/get-azurermiotcentralapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotCentral/Commands.IotCentral/help/Get-AzureRmIotCentralApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotCentral/Commands.IotCentral/help/Get-AzureRmIotCentralApp.md
ms.openlocfilehash: fdf674b5ec2dfcefe8fcada92cfaf0fd1073f7f3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764955"
---
# <span data-ttu-id="317f7-101">Get-AzureRmIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="317f7-101">Get-AzureRmIotCentralApp</span></span>

## <span data-ttu-id="317f7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="317f7-102">SYNOPSIS</span></span>
<span data-ttu-id="317f7-103">Bir veya birkaç IoT Merkezi uygulamasının özelliklerini alır.</span><span class="sxs-lookup"><span data-stu-id="317f7-103">Gets properties for either one or several IoT Central Applications.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="317f7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="317f7-104">SYNTAX</span></span>

### <span data-ttu-id="317f7-105">ListIotCentralAppsParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="317f7-105">ListIotCentralAppsParameterSet (Default)</span></span>
```
Get-AzureRmIotCentralApp [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="317f7-106">Interactiveıotmerkezileştirme Parametrekümesi</span><span class="sxs-lookup"><span data-stu-id="317f7-106">InteractiveIotCentralParameterSet</span></span>
```
Get-AzureRmIotCentralApp [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="317f7-107">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="317f7-107">ResourceIdParameterSet</span></span>
```
Get-AzureRmIotCentralApp -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="317f7-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="317f7-108">DESCRIPTION</span></span>
<span data-ttu-id="317f7-109">Belirli bir IoT Merkezi uygulamasının meta verilerini veya parametre kümesine bağlı olarak bir kaynak grubundaki veya abonelikteki tüm uygulamaları alır.</span><span class="sxs-lookup"><span data-stu-id="317f7-109">Gets the metadata for either a specific IoT Central Application, or all the applications in a Resource Group or Subscription, depending on Parameter Set.</span></span> 

## <span data-ttu-id="317f7-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="317f7-110">EXAMPLES</span></span>

### <span data-ttu-id="317f7-111">Örnek 1 belirli IoT Merkezi uygulaması alın.</span><span class="sxs-lookup"><span data-stu-id="317f7-111">Example 1 Get Specific IoT Central Application.</span></span>
```powershell
PS C:\> Get-AzureRmIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName"
```

<span data-ttu-id="317f7-112">Belirtilen IoT Merkezi uygulamasının meta verilerini alır.</span><span class="sxs-lookup"><span data-stu-id="317f7-112">Gets the metadata for the specified IoT Central Application.</span></span>

<span data-ttu-id="317f7-113">Örnek çıktı:</span><span class="sxs-lookup"><span data-stu-id="317f7-113">Example Output:</span></span>

<span data-ttu-id="317f7-114">RESOURCEID:/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. Iotmerkezi/ıotapps/Myappkaynakadı: MyAppResourceName türü: Microsoft. ıotmerkezi/ıotapps konumu: westus etiket: {[key, Val]} SKU: Microsoft. Azure. Commands. ıotcentral. modeller. PSIotCentralAppSkuInfo ApplicationId (%. ApplicationId): Myappalt etki alanı şablonu: iotc-default@1.0.0 SubscriptionID: xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx resourcegroupname: MyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="317f7-114">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : {[key, val]} Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : My Custom Display Name Subdomain         : MyAppSubdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

### <span data-ttu-id="317f7-115">Örnek 2;</span><span class="sxs-lookup"><span data-stu-id="317f7-115">Example 2 Get IoT Central Applications in Subscription.</span></span>
```powershell
PS C:\> Get-AzureRmIotCentralApp
```

<span data-ttu-id="317f7-116">Geçerli abonelikteki tüm IoT merkezi uygulamaları için meta verileri alır.</span><span class="sxs-lookup"><span data-stu-id="317f7-116">Gets the metadata for all the IoT Central Applications in the current Subscription.</span></span>

<span data-ttu-id="317f7-117">Örnek çıktı:</span><span class="sxs-lookup"><span data-stu-id="317f7-117">Example Output:</span></span>

<span data-ttu-id="317f7-118">RESOURCEID:/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. Iotmerkezi/ıotapps/Myappkaynakadı: MyAppResourceName türü: Microsoft. ıotmerkezi/ıotapps konumu: westus etiket: {[key, Val]} SKU: Microsoft. Azure. Commands. ıotcentral. modeller. PSIotCentralAppSkuInfo ApplicationId (%. ApplicationId): Myappalt etki alanı şablonu: iotc-default@1.0.0 SubscriptionID: xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx resourcegroupname: MyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="317f7-118">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : {[key, val]} Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : My Custom Display Name Subdomain         : MyAppSubdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

<span data-ttu-id="317f7-119">RESOURCEID:/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName2/providers/Microsoft. Iotcentral/ıotapps/MyAppResourceName2 adı: MyAppResourceName2 türü: Microsoft. ıotmerkezi/ıotapps konumu: westus etiket: {[key, Val]} SKU: Microsoft. Azure. Commands. ıotcentral. modeller. PSIotCentralAppSkuInfo ApplicationId 1 alt etki alanı: MyAppSubdomain2 Template: SubscriptionID: XXXXXXXX-xxxx-xxxx-xxxx- iotc-default@1.0.0 xxxxxxxxxxxx ResourceGroupName: MyResourceGroupName2</span><span class="sxs-lookup"><span data-stu-id="317f7-119">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName2/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName2 Name              : MyAppResourceName2 Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : {[key, val]} Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : My Custom Display Name 2 Subdomain         : MyAppSubdomain2 Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName2</span></span>

### <span data-ttu-id="317f7-120">Örnek 3 kaynak grubunda IoT merkezi uygulamalarını alın.</span><span class="sxs-lookup"><span data-stu-id="317f7-120">Example 3 Get IoT Central Applications in Resource Group.</span></span>
```powershell
PS C:\> Get-AzureRmIotCentralApp -ResourceGroupName "MyResourceGroupName"
```

<span data-ttu-id="317f7-121">Sağlanan kaynak grubundaki tüm IoT merkezi uygulamaları için meta verileri alır.</span><span class="sxs-lookup"><span data-stu-id="317f7-121">Gets the metadata for all IoT Central Applications in the provided Resource Group.</span></span>

<span data-ttu-id="317f7-122">Örnek çıktı:</span><span class="sxs-lookup"><span data-stu-id="317f7-122">Example Output:</span></span>

<span data-ttu-id="317f7-123">RESOURCEID:/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. Iotmerkezi/ıotapps/Myappkaynakadı: MyAppResourceName türü: Microsoft. ıotmerkezi/ıotapps konumu: westus etiket: {[key, Val]} SKU: Microsoft. Azure. Commands. ıotcentral. modeller. PSIotCentralAppSkuInfo ApplicationId (%. ApplicationId): Myappalt etki alanı şablonu: iotc-default@1.0.0 SubscriptionID: xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx resourcegroupname: MyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="317f7-123">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : {[key, val]} Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : My Custom Display Name Subdomain         : MyAppSubdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

<span data-ttu-id="317f7-124">RESOURCEID:/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. Iotcentral/ıotapps/MyAppResourceName2 adı: MyAppResourceName2 türü: Microsoft. ıotmerkezi/ıotapps konumu: westus etiket: {[key, Val]} SKU: Microsoft. Azure. Commands. ıotcentral. modeller. PSIotCentralAppSkuInfo ApplicationId (XXXXXXXX): MyAppSubdomain2 Template: iotc-default@1.0.0 SubscriptionID: xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx ResourceGroupName: MyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="317f7-124">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName2 Name              : MyAppResourceName2 Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : {[key, val]} Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : My Custom Display Name 2 Subdomain         : MyAppSubdomain2 Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

## <span data-ttu-id="317f7-125">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="317f7-125">PARAMETERS</span></span>

### <span data-ttu-id="317f7-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="317f7-126">-DefaultProfile</span></span>
<span data-ttu-id="317f7-127">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="317f7-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="317f7-128">-Ad</span><span class="sxs-lookup"><span data-stu-id="317f7-128">-Name</span></span>
<span data-ttu-id="317f7-129">IoT Merkezi uygulama kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="317f7-129">Name of the Iot Central Application Resource.</span></span>

```yaml
Type: String
Parameter Sets: InteractiveIotCentralParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="317f7-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="317f7-130">-ResourceGroupName</span></span>
<span data-ttu-id="317f7-131">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="317f7-131">Name of the Resource Group.</span></span>

```yaml
Type: String
Parameter Sets: ListIotCentralAppsParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: InteractiveIotCentralParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="317f7-132">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="317f7-132">-ResourceId</span></span>
<span data-ttu-id="317f7-133">IoT Merkezi uygulama kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="317f7-133">Iot Central Application Resource Id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="317f7-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="317f7-134">CommonParameters</span></span>
<span data-ttu-id="317f7-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="317f7-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="317f7-136">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="317f7-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="317f7-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="317f7-137">INPUTS</span></span>

### <span data-ttu-id="317f7-138">System. String</span><span class="sxs-lookup"><span data-stu-id="317f7-138">System.String</span></span>
## <span data-ttu-id="317f7-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="317f7-139">OUTPUTS</span></span>

### <span data-ttu-id="317f7-140">Microsoft. Azure. Commands. ıotcentral. modeller. PSIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="317f7-140">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span></span>
## <span data-ttu-id="317f7-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="317f7-141">NOTES</span></span>

## <span data-ttu-id="317f7-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="317f7-142">RELATED LINKS</span></span>
