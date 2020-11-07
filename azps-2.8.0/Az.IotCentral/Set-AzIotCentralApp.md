---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotCentral.dll-Help.xml
Module Name: Az.IotCentral
online version: https://docs.microsoft.com/en-us/powershell/module/az.iotcentral/set-aziotcentralapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/Set-AzIotCentralApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/Set-AzIotCentralApp.md
ms.openlocfilehash: 78fdf68ecb8c50d0eebf4611b51a2fad14c66e5d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93751785"
---
# <span data-ttu-id="536b6-101">Set-AzIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="536b6-101">Set-AzIotCentralApp</span></span>

## <span data-ttu-id="536b6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="536b6-102">SYNOPSIS</span></span>
<span data-ttu-id="536b6-103">IoT Merkezi uygulaması için meta verileri güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="536b6-103">Updates the metadata for an IoT Central Application.</span></span>

## <span data-ttu-id="536b6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="536b6-104">SYNTAX</span></span>

### <span data-ttu-id="536b6-105">Resourceıdparameterset (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="536b6-105">ResourceIdParameterSet (Default)</span></span>
```
Set-AzIotCentralApp [-DisplayName <String>] [-Subdomain <String>] [-Tag <Hashtable>] -ResourceId <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="536b6-106">Inputobjectparameterset</span><span class="sxs-lookup"><span data-stu-id="536b6-106">InputObjectParameterSet</span></span>
```
Set-AzIotCentralApp [-DisplayName <String>] [-Subdomain <String>] [-Tag <Hashtable>]
 -InputObject <PSIotCentralApp> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="536b6-107">Interactiveıotmerkezileştirme Parametrekümesi</span><span class="sxs-lookup"><span data-stu-id="536b6-107">InteractiveIotCentralParameterSet</span></span>
```
Set-AzIotCentralApp [-DisplayName <String>] [-Subdomain <String>] [-Tag <Hashtable>] [-AsJob]
 [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="536b6-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="536b6-108">DESCRIPTION</span></span>
<span data-ttu-id="536b6-109">IoT Merkezi uygulamasının meta verilerini güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="536b6-109">Update the metadata for an IoT Central Application.</span></span> 

## <span data-ttu-id="536b6-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="536b6-110">EXAMPLES</span></span>

### <span data-ttu-id="536b6-111">Örnek 1 güncelleştirme görünen adı</span><span class="sxs-lookup"><span data-stu-id="536b6-111">Example 1 Update Display Name</span></span>
```powershell
PS C:\> Set-AzureRmIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName" -DisplayName "My New Custom Display Name"
```

<span data-ttu-id="536b6-112">Var olan IoT merkezi uygulamasında görünen adı güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="536b6-112">Update the Display name on an existing IoT Central Application.</span></span>

<span data-ttu-id="536b6-113">Örnek çıktı:</span><span class="sxs-lookup"><span data-stu-id="536b6-113">Example Output:</span></span>

<span data-ttu-id="536b6-114">RESOURCEID:/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. Iotcentral/ıotapps/MyAppResourceName adı: MyAppResourceName türü: Microsoft. ıotcentral/ıotapps konumu: westus Tag: SKU: Microsoft. Azure. Commands. ıotcentral. modeller. PSIotCentralAppSkuInfo ApplicationId: XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX Ida: iotc-default@1.0.0 SubscriptionID: xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx ResourceGroupName: MyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="536b6-114">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : My New Custom Display Name Subdomain         : MyAppSubdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

### <span data-ttu-id="536b6-115">Örnek 2 güncelleştirme alt etki alanı</span><span class="sxs-lookup"><span data-stu-id="536b6-115">Example 2 Update Subdomain</span></span>
```powershell
PS C:\> Set-AzureRmIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName" -Subdomain "new-subdomain"
```

<span data-ttu-id="536b6-116">Var olan IoT merkezi uygulamasında görünen adı güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="536b6-116">Update the Display name on an existing IoT Central Application.</span></span>

<span data-ttu-id="536b6-117">Örnek çıktı:</span><span class="sxs-lookup"><span data-stu-id="536b6-117">Example Output:</span></span>

<span data-ttu-id="536b6-118">RESOURCEID:/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft. Iotcentral/ıotapps/MyAppResourceName adı: MyAppResourceName türü: Microsoft. ıotcentral/ıotapps konumu: westus Tag: SKU: Microsoft. Azure. Commands. ıotcentral. modeller. PSIotCentralAppSkuInfo ApplicationId: New-XXXX-XXXX-XXXX-XXXXXXXXXXXX iotc-default@1.0.0 DisplayName:</span><span class="sxs-lookup"><span data-stu-id="536b6-118">ResourceId        : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name              : MyAppResourceName Type              : Microsoft.IoTCentral/IoTApps Location          : westus Tag               : Sku               : Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralAppSkuInfo ApplicationId     : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName       : Display Name Subdomain         : new-subdomain Template          : iotc-default@1.0.0 SubscriptionId    : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX ResourceGroupName : MyResourceGroupName</span></span>

## <span data-ttu-id="536b6-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="536b6-119">PARAMETERS</span></span>

### <span data-ttu-id="536b6-120">-Iş</span><span class="sxs-lookup"><span data-stu-id="536b6-120">-AsJob</span></span>
<span data-ttu-id="536b6-121">Cmdlet 'i arka planda iş olarak çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="536b6-121">Run cmdlet as a job in the background.</span></span>

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

### <span data-ttu-id="536b6-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="536b6-122">-DefaultProfile</span></span>
<span data-ttu-id="536b6-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="536b6-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="536b6-124">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="536b6-124">-DisplayName</span></span>
<span data-ttu-id="536b6-125">IoT Merkezi uygulamasının özel görünen adı.</span><span class="sxs-lookup"><span data-stu-id="536b6-125">Custom Display Name of the Iot Central Application.</span></span>

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

### <span data-ttu-id="536b6-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="536b6-126">-InputObject</span></span>
<span data-ttu-id="536b6-127">IoT Merkezi uygulama giriş nesnesi.</span><span class="sxs-lookup"><span data-stu-id="536b6-127">Iot Central Application Input Object.</span></span>

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

### <span data-ttu-id="536b6-128">-Ad</span><span class="sxs-lookup"><span data-stu-id="536b6-128">-Name</span></span>
<span data-ttu-id="536b6-129">IoT Merkezi uygulama kaynağının adı.</span><span class="sxs-lookup"><span data-stu-id="536b6-129">Name of the Iot Central Application Resource.</span></span>

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

### <span data-ttu-id="536b6-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="536b6-130">-ResourceGroupName</span></span>
<span data-ttu-id="536b6-131">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="536b6-131">Name of the Resource Group.</span></span>

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

### <span data-ttu-id="536b6-132">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="536b6-132">-ResourceId</span></span>
<span data-ttu-id="536b6-133">IoT Merkezi uygulama kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="536b6-133">Iot Central Application Resource Id.</span></span>

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

### <span data-ttu-id="536b6-134">-Alt etki alanı</span><span class="sxs-lookup"><span data-stu-id="536b6-134">-Subdomain</span></span>
<span data-ttu-id="536b6-135">IoT Merkezi uygulamasının alt etki alanı.</span><span class="sxs-lookup"><span data-stu-id="536b6-135">Subdomain of the IoT Central Application.</span></span>

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

### <span data-ttu-id="536b6-136">Etiketli</span><span class="sxs-lookup"><span data-stu-id="536b6-136">-Tag</span></span>
<span data-ttu-id="536b6-137">IoT Merkezi uygulama kaynağı etiketleri.</span><span class="sxs-lookup"><span data-stu-id="536b6-137">Iot Central Application Resource Tags.</span></span>

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

### <span data-ttu-id="536b6-138">-Onay</span><span class="sxs-lookup"><span data-stu-id="536b6-138">-Confirm</span></span>
<span data-ttu-id="536b6-139">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="536b6-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="536b6-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="536b6-140">-WhatIf</span></span>
<span data-ttu-id="536b6-141">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="536b6-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="536b6-142">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="536b6-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="536b6-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="536b6-143">CommonParameters</span></span>
<span data-ttu-id="536b6-144">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="536b6-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="536b6-145">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="536b6-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="536b6-146">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="536b6-146">INPUTS</span></span>

### <span data-ttu-id="536b6-147">System. String</span><span class="sxs-lookup"><span data-stu-id="536b6-147">System.String</span></span>

### <span data-ttu-id="536b6-148">Microsoft. Azure. Commands. ıotcentral. modeller. PSIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="536b6-148">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span></span>

## <span data-ttu-id="536b6-149">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="536b6-149">OUTPUTS</span></span>

### <span data-ttu-id="536b6-150">Microsoft. Azure. Commands. ıotcentral. modeller. PSIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="536b6-150">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span></span>

## <span data-ttu-id="536b6-151">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="536b6-151">NOTES</span></span>

## <span data-ttu-id="536b6-152">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="536b6-152">RELATED LINKS</span></span>
