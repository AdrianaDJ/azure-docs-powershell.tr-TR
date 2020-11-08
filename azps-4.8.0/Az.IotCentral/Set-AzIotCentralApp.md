---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotCentral.dll-Help.xml
Module Name: Az.IotCentral
online version: https://docs.microsoft.com/en-us/powershell/module/az.iotcentral/set-aziotcentralapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/Set-AzIotCentralApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/Set-AzIotCentralApp.md
ms.openlocfilehash: 94a6e4d2b140487b279d85db1a8b663e03523ce4
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94273561"
---
# <span data-ttu-id="de6af-101">Set-AzIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="de6af-101">Set-AzIotCentralApp</span></span>

## <span data-ttu-id="de6af-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="de6af-102">SYNOPSIS</span></span>
<span data-ttu-id="de6af-103">IoT Merkezi uygulaması için meta verileri güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="de6af-103">Updates the metadata for an IoT Central Application.</span></span>

## <span data-ttu-id="de6af-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="de6af-104">SYNTAX</span></span>

### <span data-ttu-id="de6af-105">Resourceıdparameterset (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="de6af-105">ResourceIdParameterSet (Default)</span></span>
```
Set-AzIotCentralApp [-DisplayName <String>] [-Subdomain <String>] [-Tag <Hashtable>] [-Sku <String>]
 -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="de6af-106">Inputobjectparameterset</span><span class="sxs-lookup"><span data-stu-id="de6af-106">InputObjectParameterSet</span></span>
```
Set-AzIotCentralApp [-DisplayName <String>] [-Subdomain <String>] [-Tag <Hashtable>] [-Sku <String>]
 -InputObject <PSIotCentralApp> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="de6af-107">Interactiveıotmerkezileştirme Parametrekümesi</span><span class="sxs-lookup"><span data-stu-id="de6af-107">InteractiveIotCentralParameterSet</span></span>
```
Set-AzIotCentralApp [-DisplayName <String>] [-Subdomain <String>] [-Tag <Hashtable>] [-Sku <String>] [-AsJob]
 [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="de6af-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="de6af-108">DESCRIPTION</span></span>
<span data-ttu-id="de6af-109">IoT Merkezi uygulamasının meta verilerini güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="de6af-109">Update the metadata for an IoT Central Application.</span></span> 

## <span data-ttu-id="de6af-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="de6af-110">EXAMPLES</span></span>

### <span data-ttu-id="de6af-111">Örnek 1 güncelleştirme görünen adı</span><span class="sxs-lookup"><span data-stu-id="de6af-111">Example 1 Update Display Name</span></span>
```powershell
PS C:\> Set-AzureRmIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName" -DisplayName "My New Custom Display Name"
```

<span data-ttu-id="de6af-112">Var olan IoT merkezi uygulamasında görünen adı güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="de6af-112">Update the Display name on an existing IoT Central Application.</span></span>

<span data-ttu-id="de6af-113">Örnek çıktı:</span><span class="sxs-lookup"><span data-stu-id="de6af-113">Example Output:</span></span>

<span data-ttu-id="de6af-114">RESOURCEID:/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. Iotcentral/ıotapps/MyAppResourceName adı: MyAppResourceName türü: Microsoft. ıotcentral/ıotapps konumu: westus Tag: SKU: Microsoft. Azure. Commands. ıotcentral. modeller. PSIotCentralAppSkuInfo ApplicationId: XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX Ida: iotc-default@1.0.0 SubscriptionID: xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx ResourceGroupName: MyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="de6af-114">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : My New Custom Display Name Subdomain         : MyAppSubdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

### <span data-ttu-id="de6af-115">Örnek 2 güncelleştirme alt etki alanı</span><span class="sxs-lookup"><span data-stu-id="de6af-115">Example 2 Update Subdomain</span></span>
```powershell
PS C:\> Set-AzureRmIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName" -Subdomain "new-subdomain"
```

<span data-ttu-id="de6af-116">Var olan IoT merkezi uygulamasında görünen adı güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="de6af-116">Update the Display name on an existing IoT Central Application.</span></span>

<span data-ttu-id="de6af-117">Örnek çıktı:</span><span class="sxs-lookup"><span data-stu-id="de6af-117">Example Output:</span></span>

<span data-ttu-id="de6af-118">RESOURCEID:/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. Iotcentral/ıotapps/MyAppResourceName adı: MyAppResourceName türü: Microsoft. ıotcentral/ıotapps konumu: westus Tag: SKU: Microsoft. Azure. Commands. ıotcentral. modeller. PSIotCentralAppSkuInfo ApplicationId: New-XXXX-XXXX-XXXX-XXXXXXXXXXXX iotc-default@1.0.0 DisplayName:</span><span class="sxs-lookup"><span data-stu-id="de6af-118">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : Display Name Subdomain         : new-subdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

### <span data-ttu-id="de6af-119">Örnek 3 App SKU bilgisini güncelleştir</span><span class="sxs-lookup"><span data-stu-id="de6af-119">Example 3 Update App Sku Info</span></span>
```powershell
PS C:\> Set-AzureRmIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName" -Sku "ST2"
```

<span data-ttu-id="de6af-120">Var olan bir IoT merkezi uygulamasında STB 'yi güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="de6af-120">Update the sku on an existing IoT Central Application.</span></span>

<span data-ttu-id="de6af-121">Örnek çıktı:</span><span class="sxs-lookup"><span data-stu-id="de6af-121">Example Output:</span></span>

<span data-ttu-id="de6af-122">RESOURCEID:/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. Iotcentral/ıotapps/MyAppResourceName adı: MyAppResourceName türü: Microsoft. ıotcentral/ıotapps konumu: westus Tag: SKU: Microsoft. Azure. Commands. ıotcentral. modeller. PSIotCentralAppSkuInfo ApplicationId: Uygulamaadı şablonu: iotc-default@1.0.0 SubscriptionID: xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx ResourceGroupName: MyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="de6af-122">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : Display Name Subdomain         : MyAppSubdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

## <span data-ttu-id="de6af-123">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="de6af-123">PARAMETERS</span></span>

### <span data-ttu-id="de6af-124">-Iş</span><span class="sxs-lookup"><span data-stu-id="de6af-124">-AsJob</span></span>
<span data-ttu-id="de6af-125">Cmdlet 'i arka planda iş olarak çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="de6af-125">Run cmdlet as a job in the background.</span></span>

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

### <span data-ttu-id="de6af-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de6af-126">-DefaultProfile</span></span>
<span data-ttu-id="de6af-127">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="de6af-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="de6af-128">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="de6af-128">-DisplayName</span></span>
<span data-ttu-id="de6af-129">IoT Merkezi uygulamasının özel görünen adı.</span><span class="sxs-lookup"><span data-stu-id="de6af-129">Custom Display Name of the Iot Central Application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de6af-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="de6af-130">-InputObject</span></span>
<span data-ttu-id="de6af-131">IoT Merkezi uygulama giriş nesnesi.</span><span class="sxs-lookup"><span data-stu-id="de6af-131">Iot Central Application Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="de6af-132">-Ad</span><span class="sxs-lookup"><span data-stu-id="de6af-132">-Name</span></span>
<span data-ttu-id="de6af-133">IoT Merkezi uygulama kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="de6af-133">Name of the Iot Central Application Resource.</span></span>

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

### <span data-ttu-id="de6af-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="de6af-134">-ResourceGroupName</span></span>
<span data-ttu-id="de6af-135">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="de6af-135">Name of the Resource Group.</span></span>

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

### <span data-ttu-id="de6af-136">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="de6af-136">-ResourceId</span></span>
<span data-ttu-id="de6af-137">IoT Merkezi uygulama kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="de6af-137">Iot Central Application Resource Id.</span></span>

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

### <span data-ttu-id="de6af-138">-SKU</span><span class="sxs-lookup"><span data-stu-id="de6af-138">-Sku</span></span>
<span data-ttu-id="de6af-139">IoT merkezi uygulamaları için fiyatlandırma katmanı.</span><span class="sxs-lookup"><span data-stu-id="de6af-139">Pricing tier for IoT Central applications.</span></span>
<span data-ttu-id="de6af-140">Varsayılan değer ST2.</span><span class="sxs-lookup"><span data-stu-id="de6af-140">Default value is ST2.</span></span>

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

### <span data-ttu-id="de6af-141">-Alt etki alanı</span><span class="sxs-lookup"><span data-stu-id="de6af-141">-Subdomain</span></span>
<span data-ttu-id="de6af-142">IoT Merkezi uygulamasının alt etki alanı.</span><span class="sxs-lookup"><span data-stu-id="de6af-142">Subdomain of the IoT Central Application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de6af-143">Etiketli</span><span class="sxs-lookup"><span data-stu-id="de6af-143">-Tag</span></span>
<span data-ttu-id="de6af-144">IoT Merkezi uygulama kaynağı etiketleri.</span><span class="sxs-lookup"><span data-stu-id="de6af-144">Iot Central Application Resource Tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de6af-145">-Onay</span><span class="sxs-lookup"><span data-stu-id="de6af-145">-Confirm</span></span>
<span data-ttu-id="de6af-146">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="de6af-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="de6af-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="de6af-147">-WhatIf</span></span>
<span data-ttu-id="de6af-148">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="de6af-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="de6af-149">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="de6af-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="de6af-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de6af-150">CommonParameters</span></span>
<span data-ttu-id="de6af-151">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="de6af-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de6af-152">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="de6af-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de6af-153">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="de6af-153">INPUTS</span></span>

### <span data-ttu-id="de6af-154">System. String</span><span class="sxs-lookup"><span data-stu-id="de6af-154">System.String</span></span>

### <span data-ttu-id="de6af-155">Microsoft. Azure. Commands. ıotcentral. modeller. PSIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="de6af-155">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span></span>

## <span data-ttu-id="de6af-156">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="de6af-156">OUTPUTS</span></span>

### <span data-ttu-id="de6af-157">Microsoft. Azure. Commands. ıotcentral. modeller. PSIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="de6af-157">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span></span>

## <span data-ttu-id="de6af-158">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="de6af-158">NOTES</span></span>

## <span data-ttu-id="de6af-159">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="de6af-159">RELATED LINKS</span></span>
